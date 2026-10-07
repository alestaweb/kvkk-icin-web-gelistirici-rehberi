# Site yöneticileri için parola ve iki adımlı doğrulama: pratik rehber

Bir web sitesinin yönetim paneline giren hesap, sitedeki bütün kişisel verilere de ulaşır: üye listeleri, sipariş adresleri, iletişim formu mesajları. Saldırganların çoğu karmaşık açık aramaz; zayıf ya da başka yerde sızmış bir parolayla kapıdan girer. Bu yazı, küçük bir işletme sitesini, haber sitesini ya da e-ticaret mağazasını yöneten kişilerin bugün uygulayabileceği adımları anlatır.

KVKK'nın 12. maddesi veri sorumlusuna kişisel verilere hukuka aykırı erişimi önlemek için gerekli teknik ve idari tedbirleri alma yükümlülüğü verir. Yönetim hesaplarının korunması bu tedbirlerin en temel parçasıdır.

---

## 1. Parolada uzunluk, karmaşıklıktan önemlidir

"En az bir büyük harf, bir rakam, bir sembol" kuralı insanları "Sirket2024!" gibi tahmin edilebilir kalıplara iter. Saldırı araçları bu kalıpları ilk sırada dener.

Daha iyi yol:

- Yönetici hesaplarında en az 14–16 karakter hedefleyin.
- Birbiriyle ilgisiz dört-beş kelimeden oluşan bir parola cümlesi hem uzun hem akılda kalıcıdır.
- Firma adı, alan adı, doğum yılı, plaka, telefon numarası gibi kişiyle ilişkilendirilebilen bilgileri kullanmayın.
- Klavye dizileri (qwerty, 123456, asdfgh) ve tek harf değişikliğiyle türetilen parolalar (Parola1, Parola2) zayıftır.

ABD Ulusal Standartlar ve Teknoloji Enstitüsü'nün (NIST) dijital kimlik rehberi de aynı yönde: uzunluğu öne çıkarın, keyfi karmaşıklık kurallarından vazgeçin, parolayı bilinen sızıntı listelerine karşı kontrol edin.

## 2. Her hesap için ayrı parola

En sık görülen ihlal senaryosu şudur: yöneticinin yıllar önce üye olduğu bir forum ya da alışveriş sitesi sızdırılır, aynı e-posta ve parola site paneline denenir ve çalışır.

- Panel, e-posta, alan adı firması, barındırma hesabı, ödeme kuruluşu paneli: her birinin parolası farklı olmalı.
- Özellikle e-posta hesabı kritik: "parolamı unuttum" bağlantıları oraya gider. E-postayı ele geçiren, diğer hesapları da sıfırlayabilir.
- Kendi e-postanızın bilinen bir sızıntıda geçip geçmediğini "Have I Been Pwned" gibi herkese açık sızıntı sorgulama servisleriyle kontrol edebilirsiniz.

## 3. Parola yöneticisi kullanın

Onlarca farklı ve uzun parolayı akılda tutmak mümkün değil. Bir parola yöneticisi bu sorunu çözer:

- Tek bir ana parola (uzun bir parola cümlesi) ezberlenir, diğerleri rastgele üretilir.
- Tarayıcı eklentisi giriş sayfasının adresini kontrol eder; sahte bir giriş sayfasında otomatik doldurma yapmaz. Bu, oltalamaya karşı da bir koruma katmanıdır.
- Ekip içinde paylaşılan hesaplar varsa, parolayı mesajlaşma uygulamasından göndermek yerine yöneticinin paylaşım özelliği kullanılmalı.

Parolaları masaüstündeki bir metin dosyasında, e-posta taslaklarında ya da ekran görüntüsü olarak telefonda saklamak en sık rastlanan kötü alışkanlıktır.

## 4. İki adımlı doğrulama (2FA) mutlaka açılmalı

Parola sızsa bile ikinci adım olmadan hesaba girilemez. Seçenekler güvenlik sırasına göre:

1. **Donanım güvenlik anahtarı veya geçiş anahtarı (passkey):** Oltalamaya karşı en dayanıklı yöntemdir, çünkü anahtar yalnızca gerçek sitenin adresiyle çalışır.
2. **Doğrulayıcı uygulama (TOTP):** Telefondaki uygulama her 30 saniyede bir değişen 6 haneli kod üretir. İnternet bağlantısı gerektirmez, yaygın desteklenir.
3. **SMS ile kod:** Hiç olmamasından iyidir, ancak SIM kart değiştirme dolandırıcılığına ve mesaj yönlendirmeye açıktır. Başka seçenek varsa onu tercih edin.

Uygulamada dikkat edilecekler:

- 2FA'yı açarken verilen **yedek kodları** yazdırın ya da parola yöneticisinde saklayın. Telefon kaybolduğunda hesaba dönmenin tek yolu bunlardır.
- Doğrulayıcı uygulamayı yeni telefona taşımadan eski telefonu sıfırlamayın.
- Önce en kritik hesaplardan başlayın: e-posta, alan adı firması, barındırma hesabı, site paneli.

## 5. Yönetici hesaplarını sade tutun

- **Herkese ayrı hesap:** "admin" adında, parolası ekipçe bilinen ortak bir hesap olmamalı. Kim ne yaptı sorusunun cevabı ancak kişisel hesaplarla verilebilir.
- **En az yetki:** Haber yazan kişiye yazar yetkisi, sipariş hazırlayan kişiye sipariş yetkisi yeter. Herkes tam yönetici olmamalı.
- **Ayrılan çalışan:** İşten ayrılan ya da işi biten dış hizmet sağlayıcının hesabı aynı gün kapatılmalı; ortak bilinen parolalar değiştirilmeli.
- **Kullanıcı adı:** "admin", "yonetici", "test" gibi tahmin edilebilir kullanıcı adları kaba kuvvet denemelerinin ilk hedefidir.

## 6. Parolayı ne zaman değiştirmeli?

Belirli aralıklarla zorunlu parola değişimi artık önerilmiyor; insanlar sonuna rakam ekleyerek geçiştiriyor. Değiştirmeniz gereken durumlar:

- Parolanın sızdığından ya da başkası tarafından görüldüğünden şüpheleniyorsanız,
- Hesabı kullanan biri ayrıldıysa,
- Bilgisayarınızda zararlı yazılım bulunduysa,
- Parolayı bir başka hesapta da kullandığınızı fark ettiyseniz.

## 7. Giriş sayfasında bakılacaklar

Sitenizi siz yazmadıysanız bile geliştiricinize ya da hizmet sağlayıcınıza şu soruları sorabilirsiniz:

- Art arda hatalı girişlerde hesap ya da IP geçici olarak yavaşlatılıyor mu?
- Giriş sayfası yalnızca HTTPS üzerinden mi açılıyor?
- Başarılı ve başarısız girişler kayıt altına alınıyor mu, yeni bir cihazdan giriş yapıldığında bildirim geliyor mu?
- Parolalar veritabanında geri çözülemeyecek şekilde (güncel bir parola özetleme yöntemiyle) mi saklanıyor?
- "Parolamı unuttum" bağlantısı kısa süreli ve tek kullanımlık mı?
- Panelde iki adımlı doğrulama seçeneği var mı?

## 8. Oltalama: en iyi parolayı bile boşa çıkarır

- "Hesabınız askıya alınacak", "alan adınızın süresi doldu", "ödemeniz başarısız" gibi acele ettiren e-postalardaki bağlantılara tıklamayın; siteye adres çubuğuna kendiniz yazarak gidin.
- Gönderen adı tanıdık görünse bile e-posta adresinin alan adını kontrol edin.
- Telefonla arayıp doğrulama kodu isteyen hiçbir kuruma kod vermeyin. Gerçek kurumlar bu kodu sormaz.

## 9. Bir şeyler ters giderse

1. Ele geçirildiğinden şüphelendiğiniz hesabın parolasını temiz bir cihazdan değiştirin.
2. Aynı parolayı kullandığınız diğer hesapları da değiştirin.
3. Tüm açık oturumları kapatın, 2FA'yı yeniden kurun.
4. Panelde sizin oluşturmadığınız yeni bir kullanıcı ya da yetki değişikliği var mı bakın.
5. Kişisel veriler etkilendiyse, KVKK kapsamındaki veri ihlali bildirim yükümlülüğünü değerlendirmek için bir hukukçuya danışın.

---

## Kısa kontrol listesi

- [ ] Yönetici parolaları en az 14–16 karakter
- [ ] Her hesapta farklı parola
- [ ] Parola yöneticisi kullanılıyor, düz metin dosyada parola yok
- [ ] E-posta, alan adı, barındırma ve site panelinde 2FA açık
- [ ] Yedek kodlar güvenli bir yerde saklı
- [ ] Ortak "admin" hesabı yok, herkesin kendi hesabı var
- [ ] Yetkiler işe göre sınırlı
- [ ] Ayrılan kişilerin hesapları kapatıldı
- [ ] Hatalı giriş denemeleri sınırlanıyor ve kayıt altına alınıyor
- [ ] Ekip oltalama e-postalarını tanıyor

---

## Kaynaklar

- 6698 sayılı Kişisel Verilerin Korunması Kanunu, 12. madde — [mevzuat.gov.tr](https://www.mevzuat.gov.tr)
- Kişisel Verileri Koruma Kurumu, Kişisel Veri Güvenliği Rehberi (Teknik ve İdari Tedbirler) — [kvkk.gov.tr](https://www.kvkk.gov.tr)
- NIST SP 800-63B, Digital Identity Guidelines — [pages.nist.gov/800-63-4](https://pages.nist.gov/800-63-4/)
- Ulusal Siber Olaylara Müdahale Merkezi (USOM) — [usom.gov.tr](https://www.usom.gov.tr)

Bu yazı eğitim amaçlıdır, hukuki görüş değildir.

---

Bu yazı [kvkk-icin-web-gelistirici-rehberi](../README.md) deposunun bir parçasıdır. Soru ve önerileriniz için deponun **Discussions** bölümünü kullanabilirsiniz.

Hazırlayan: [Alesta WEB](https://alestaweb.com) — İzmir
