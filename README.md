# KVKK için Web Geliştirici Rehberi

> Türkiye'de web sitesi ve uygulama geliştiren yazılımcılar için **6698 sayılı Kişisel Verilerin Korunması Kanunu (KVKK)** uyum rehberi.
> Hukuki danışmanlık değildir; teknik uygulama bakış açısıyla hazırlanmış açıklamalı bir kaynaktır.

Bu rehber, bir web projesinde kişisel veri işleyen herkesin (geliştirici, proje yöneticisi, ajans) bilmesi gereken KVKK gerekliliklerini sade Türkçe ile toplar. Amaç, "uyumlu görünmek" değil, gerçekten uyumlu sistemler kurmaktır.

İçerik tamamen **kavramsal ve eğitici**dir. Hiçbir kuruluşa ait kod, altyapı veya iç sistem bilgisi içermez.

---

## İçindekiler

1. [KVKK Nedir, Kimi Bağlar?](#1-kvkk-nedir-kimi-bağlar)
2. [Temel Kavramlar](#2-temel-kavramlar)
3. [Açık Rıza Yönetimi](#3-açık-rıza-yönetimi)
4. [Aydınlatma Yükümlülüğü](#4-aydınlatma-yükümlülüğü)
5. [Çerez (Cookie) Yönetimi](#5-çerez-cookie-yönetimi)
6. [Veri Sahibi Hakları ve Başvuru](#6-veri-sahibi-hakları-ve-başvuru)
7. [Veri Silme, Yok Etme, Anonimleştirme](#7-veri-silme-yok-etme-anonimleştirme)
8. [Log Tutma ve Saklama Süreleri](#8-log-tutma-ve-saklama-süreleri)
9. [Veri Güvenliği Teknik Tedbirleri](#9-veri-güvenliği-teknik-tedbirleri)
10. [VERBİS Kaydı](#10-verbis-kaydı)
11. [Veri İhlali Bildirimi](#11-veri-i̇hlali-bildirimi)
12. [Yurt Dışına Veri Aktarımı](#12-yurt-dışına-veri-aktarımı)
13. [İYS ve Ticari Elektronik İleti](#13-i̇ys-ve-ticari-elektronik-i̇leti)
14. [Geliştirici Kontrol Listesi](#14-geliştirici-kontrol-listesi)
15. [Resmi Kaynaklar](#15-resmi-kaynaklar)

---

## 1. KVKK Nedir, Kimi Bağlar?

KVKK, 6698 sayılı kanunla 2016'da yürürlüğe girdi ve büyük ölçüde Avrupa'nın GDPR'ı ile benzer bir mantık taşır. Türkiye'de **gerçek kişilere ait kişisel veri işleyen** her web sitesi, uygulama ve sistem bu kanuna tabidir — sitenin ticari olup olmaması fark etmez.

Bir iletişim formu, bir üyelik kaydı, bir sipariş süreci ya da yalnızca ziyaretçi IP'sini loglayan bir analiz aracı bile "kişisel veri işleme" sayılır. Yani neredeyse her web projesi KVKK kapsamındadır.

Denetim ve yaptırım yetkisi **Kişisel Verileri Koruma Kurumu (KVKK Kurumu)** ve karar organı olan **Kurul**'dadır. İdari para cezaları her yıl yeniden değerleme oranıyla artar ve azımsanmayacak rakamlara ulaşır.

---

## 2. Temel Kavramlar

| Terim | Anlamı |
|---|---|
| **Kişisel veri** | Kimliği belirli veya belirlenebilir gerçek kişiye ilişkin her bilgi (ad, e-posta, telefon, IP, konum, çerez ID'si). |
| **Özel nitelikli kişisel veri** | Sağlık, din, etnik köken, biyometrik, cinsel hayat, ceza mahkûmiyeti gibi hassas veriler. Daha katı korunur. |
| **Veri sorumlusu** | İşleme amaç ve araçlarını belirleyen taraf (genellikle site sahibi işletme). |
| **Veri işleyen** | Sorumlu adına veri işleyen taraf (hosting firması, ajans, bulut sağlayıcı). |
| **İşleme** | Verinin toplanması, kaydı, saklanması, değiştirilmesi, aktarılması, silinmesi — kısaca verinin başına gelen her şey. |
| **Açık rıza** | Belirli bir konuya ilişkin, bilgilendirilmeye dayanan, özgür iradeyle verilen onay. |

**Geliştirici için kritik ayrım:** Çoğu zaman müşteri "veri sorumlusu", geliştirici/ajans ise "veri işleyen"dir. Bu ayrım, sorumlulukların kimde olduğunu belirler ve aranızdaki sözleşmede netleştirilmelidir.

---

## 3. Açık Rıza Yönetimi

Açık rıza KVKK'nın en çok yanlış uygulanan noktasıdır. Doğru açık rızanın üç şartı vardır:

1. **Belirli bir konuya ilişkin** — "Her türlü işleme onay veriyorum" geçersizdir. Her amaç ayrı belirtilmelidir.
2. **Bilgilendirmeye dayalı** — Kişi neye onay verdiğini bilmelidir.
3. **Özgür irade** — Hizmet almak için zorunlu tutulan rıza, özgür irade sayılmaz.

### Yapılması gerekenler

- Onay kutuları **varsayılan olarak boş** olmalı (pre-checked kutu geçersizdir).
- Farklı amaçlar için **ayrı kutular** kullanılmalı (ör. üyelik ≠ pazarlama izni).
- Rıza **geri alınabilir** olmalı ve geri alma, vermek kadar kolay olmalı.
- Her rıza kaydı **kanıtlanabilir** olmalı: kim, ne zaman, hangi metne, hangi versiyonla onay verdi.

### Önemli nüans: Her işleme rıza gerektirmez

KVKK'da rıza tek hukuki sebep değildir. Sözleşmenin ifası, kanuni yükümlülük, meşru menfaat gibi sebeplerle rıza olmadan da veri işlenebilir. **Mevcut bir hizmet için zaten gerekli olan veriyi işlerken gereksiz yere rıza istemek hatadır** — çünkü o veri zaten sözleşme gereği işlenir. Rızayı sadece gerçekten rızaya dayanan işlemeler için kullanın (tipik örnek: pazarlama).

---

## 4. Aydınlatma Yükümlülüğü

Rızadan **ayrı** bir yükümlülüktür. Veri toplanırken kişiye şunlar bildirilmelidir:

- Veri sorumlusunun kimliği
- Verinin hangi amaçla işleneceği
- Kimlere, hangi amaçla aktarılabileceği
- Toplama yöntemi ve hukuki sebebi
- Veri sahibinin hakları

Pratikte bu, sitede erişilebilir bir **Aydınlatma Metni / Gizlilik Politikası** sayfası demektir. Form gönderilen her noktadan (üyelik, iletişim, sipariş) bu metne bağlantı verilmelidir.

> Aydınlatma "rıza" değildir. Onay kutusu olmadan da gösterilmesi gereken bir bilgilendirmedir. İkisini karıştırmak yaygın bir hatadır.

---

## 5. Çerez (Cookie) Yönetimi

Çerezler tek başına bir KVKK ve elektronik haberleşme gizliliği konusudur.

### Çerez kategorileri

| Tür | Rıza gerekir mi? |
|---|---|
| **Zorunlu / teknik çerezler** (oturum, sepet, güvenlik) | Hayır — hizmetin çalışması için zorunlu. |
| **Analitik / performans çerezleri** | Evet (kişiyi tanımlıyorsa). |
| **Pazarlama / hedefleme çerezleri** | Evet — açık rıza şart. |

### Doğru çerez banner'ı

- Sayfa açılır açılmaz **rıza gerektiren çerezler çalıştırılmamalı**; kullanıcı onay verene kadar beklemeli.
- "Kabul Et" kadar görünür bir **"Reddet"** seçeneği olmalı.
- "Ayarları yönet" ile kategori bazlı seçim sunulmalı.
- Seçim **kaydedilmeli** ve tekrar tekrar sorulmamalı.

Sadece "Bu site çerez kullanır [Tamam]" diyen bilgilendirme banner'ı tek başına yeterli değildir; gerçek bir tercih mekanizması gerekir.

---

## 6. Veri Sahibi Hakları ve Başvuru

KVKK madde 11, kişiye şu hakları verir: verisinin işlenip işlenmediğini öğrenme, bilgi talep etme, düzeltilmesini, silinmesini isteme, aktarıldığı yerleri öğrenme, işlemeye itiraz etme ve zarar görmüşse tazminat isteme.

### Geliştiricinin sağlaması gerekenler

- Bir **başvuru kanalı** (KEP, noter, sistemde kayıtlı e-posta veya ıslak imzalı başvuru).
- Başvuruları **en geç 30 gün** içinde yanıtlama altyapısı.
- Bir kişinin tüm verisini **bulup raporlayabilme** yeteneği. Veri birden çok tabloya/sisteme dağıldıysa, bunları kişi bazında toplayabilmek önemlidir — bu, mimaride baştan düşünülmesi gereken bir şeydir.

---

## 7. Veri Silme, Yok Etme, Anonimleştirme

İşleme amacı ortadan kalktığında veya kişi talep ettiğinde veri ortadan kaldırılmalıdır. KVKK üç yöntem tanımlar:

- **Silme:** Verinin ilgili kullanıcılar için erişilemez/kullanılamaz hale getirilmesi.
- **Yok etme:** Verinin hiçbir şekilde geri getirilemeyecek şekilde imhası.
- **Anonimleştirme:** Verinin, başka verilerle eşleştirilse dahi kimliği belirli bir kişiye bağlanamayacak hale getirilmesi.

### Teknik notlar

- **"Soft delete" tek başına silme sayılmaz.** Sadece bir `silindi` bayrağı işaretlemek, veri hâlâ okunabilir durumdaysa KVKK anlamında silme değildir.
- **Yedekler unutulmamalı.** Canlı veritabanından silinen veri, yedeklerde aylarca kalabilir. Saklama politikası yedekleri de kapsamalıdır.
- **Anonimleştirme geri döndürülemez olmalı.** Bir eşleştirme tablosu sakladıysanız, bu artık anonimleştirme değil takma adlandırmadır (pseudonymization).
- Silme talepleri için bir **periyodik imha süreci** (örneğin saklama süresi dolan kayıtların düzenli temizliği) kurulması beklenir.

---

## 8. Log Tutma ve Saklama Süreleri

Loglar iki yönlü bir sorundur: bazı loglar **tutulmak zorundadır**, bazıları da **fazla tutulmamalıdır**.

### Tutulması gerekenler

- **5651 sayılı kanun** kapsamında, yer/erişim sağlayıcı niteliğindeki sistemler belirli trafik/erişim loglarını **kanunla belirlenen süre** boyunca, bütünlüğü bozulmadan saklamak zorundadır.
- KVKK işleme faaliyetlerine dair **işleme kayıtları** denetimde gerekebilir.

### Fazla tutulmaması gerekenler

- Kişisel veri içeren uygulama logları (IP, kullanıcı ID, davranış) **süresiz** saklanmamalı.
- Her log türü için bir **saklama süresi** tanımlanmalı ve süre dolunca otomatik temizlenmelidir.

### Pratik yaklaşım

Her veri ve log türü için bir **saklama matrisi** oluşturun: ne, neden, ne kadar süreyle, hangi hukuki sebeple tutuluyor. Süre dolduğunda silme/anonimleştirme otomatik tetiklenmelidir. "Her ihtimale karşı sonsuza kadar saklamak" KVKK'ya aykırıdır — veri minimizasyonu ilkesi gereği yalnızca gerekli olan, gerektiği kadar tutulur.

---

## 9. Veri Güvenliği Teknik Tedbirleri

KVKK, veri sorumlusundan "uygun güvenlik düzeyini sağlamayı" ister. KVKK Kurumu'nun rehberlerinde sıralanan teknik tedbirlerin web tarafına düşenleri:

- **Aktarımda şifreleme:** Tüm site HTTPS (güncel TLS) üzerinden sunulmalı.
- **Saklamada koruma:** Parolalar geri döndürülemez güçlü algoritmalarla özetlenmeli; hassas veriler şifrelenmeli.
- **Yetki ve erişim kontrolü:** En az yetki ilkesi; herkesin her veriye erişmemesi.
- **Erişim kayıtları:** Hassas verilere kimin eriştiğinin izlenebilmesi.
- **Güncel tutma:** Bağımlılıkların ve sunucu yazılımının güvenlik yamalarının takibi.
- **Yedekleme:** Düzenli, güvenli ve geri dönüşü test edilmiş yedekler.
- **Saldırı yüzeyini azaltma:** Gereksiz servislerin kapatılması, girdi doğrulama, yaygın güvenlik açıklarına karşı önlem.

Bunlar aynı zamanda iyi mühendislik pratiğidir; KVKK bunları yasal bir zorunluluğa dönüştürür.

---

## 10. VERBİS Kaydı

**VERBİS (Veri Sorumluları Sicil Bilgi Sistemi)**, belirli eşikleri aşan veri sorumlularının kaydolmak zorunda olduğu kamu sicilidir. Çalışan sayısı, yıllık mali bilanço ve işlenen verinin niteliği gibi kriterlere göre kayıt zorunluluğu doğar; bazı küçük ölçekli işletmeler muaf olabilir.

Bu, geliştiricinin doğrudan sorumluluğu değildir ama **müşteriyi bilgilendirmek** profesyonel bir davranıştır: "Şu kriterleri aşıyorsanız VERBİS kaydı gerekebilir, bir hukukçuya danışın."

---

## 11. Veri İhlali Bildirimi

Bir veri ihlali (sızıntı, yetkisiz erişim) gerçekleştiğinde:

- Veri sorumlusu, ihlali öğrendiğinden itibaren **en kısa sürede ve makul olan en geç süre içinde** KVKK Kurumu'na bildirmekle yükümlüdür.
- Etkilenen kişilere de uygun yöntemle bildirim yapılmalıdır.

Geliştirici tarafında bunun anlamı: bir ihlali **fark edebilecek** izleme (anormal erişim, sızıntı tespiti) ve ihlal anında hızlı tepki verebilecek bir süreç bulunmalıdır. İhlali aylarca fark etmemek başlı başına bir tedbir eksikliğidir.

---

## 12. Yurt Dışına Veri Aktarımı

Birçok web projesi yurt dışı hizmet kullanır: bulut hosting, e-posta servisi, analitik, CDN, üçüncü taraf API'ler. Bunların çoğu kişisel veriyi yurt dışına aktarır.

KVKK, yurt dışına aktarımı belirli koşullara bağlar (ilgilinin açık rızası, ya da uygun güvencelerin/şartların sağlanması). Pratikte:

- Hangi üçüncü taraf hizmetlerin veriyi yurt dışına taşıdığını **envanterleyin**.
- Mümkün olan yerde **Türkiye/yerel barındırma** tercih edin.
- Aydınlatma metninde bu aktarımları **şeffafça belirtin**.

Bu alandaki kurallar zamanla güncellenmektedir; güncel mevzuatı ve Kurul kararlarını takip etmek gerekir.

---

## 13. İYS ve Ticari Elektronik İleti

Pazarlama amaçlı SMS, e-posta ve arama yapıyorsanız iki katman vardır:

- **6563 sayılı kanun** kapsamında ticari elektronik ileti için **önceden onay** (opt-in) zorunludur.
- **İYS (İleti Yönetim Sistemi)** üzerinden onayların kaydı ve ret (opt-out) yönetimi gerekir.

Geliştirici tarafında:

- Pazarlama onayı, hizmet için zorunlu olmayan **ayrı bir kutu** olmalı.
- Her iletide **kolay abonelikten çıkma** yolu bulunmalı.
- Onay ve ret kayıtları İYS ile uyumlu tutulmalı.

KVKK açık rızası ile İYS onayı **farklı şeylerdir**; pazarlama yapıyorsanız ikisi de gerekir.

---

## 14. Geliştirici Kontrol Listesi

Bir web projesini teslim etmeden önce:

- [ ] Site tamamen HTTPS, güncel TLS ile sunuluyor
- [ ] Parolalar güçlü, geri döndürülemez algoritmayla saklanıyor
- [ ] Aydınlatma Metni / Gizlilik Politikası sayfası var ve formlardan erişilebiliyor
- [ ] Açık rıza kutuları varsayılan boş, amaç bazında ayrık
- [ ] Rıza kayıtları (kim/ne zaman/hangi versiyon) saklanıyor
- [ ] Çerez yönetimi gerçek tercih sunuyor (kabul = reddet kadar kolay)
- [ ] Rıza gerektiren çerezler onaydan önce çalışmıyor
- [ ] Veri sahibi başvurusu için bir kanal ve 30 gün içinde yanıt süreci var
- [ ] Bir kişinin tüm verisi bulunup raporlanabiliyor
- [ ] Silme işlemi gerçek silme (sadece bayrak değil), yedekleri de kapsıyor
- [ ] Her veri/log türü için saklama süresi ve otomatik imha tanımlı
- [ ] Yurt dışına veri aktaran üçüncü taraf servisler envanterlenmiş
- [ ] İhlali fark edebilecek izleme ve müdahale süreci mevcut
- [ ] Pazarlama yapılıyorsa İYS uyumu ve opt-out var
- [ ] Veri işleyen rolü üstleniliyorsa müşteriyle sözleşmede sorumluluklar net

---

## 15. Resmi Kaynaklar

> Mevzuat zamanla değişir. Karar vermeden önce daima güncel resmi kaynağa bakın ve gerektiğinde hukuki danışmanlık alın.

- **KVKK Kurumu:** https://www.kvkk.gov.tr
- **6698 sayılı Kanun (mevzuat metni):** https://www.mevzuat.gov.tr
- **İYS (İleti Yönetim Sistemi):** https://iys.org.tr
- **KVKK Kurul Kararları ve Rehberler:** kvkk.gov.tr üzerinden yayımlanır

---

## Lisans

Bu rehber MIT lisansı altında dağıtılır. Eğitim amaçlıdır; hukuki danışmanlık yerine geçmez.

## Katkı

Mevzuat güncellendikçe içerik de güncellenmelidir. Düzeltme ve eklemeler için issue açabilirsiniz.
