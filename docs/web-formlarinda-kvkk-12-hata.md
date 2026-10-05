# Web Formlarında KVKK: Sık Yapılan 12 Hata ve Doğrusu

İletişim formu, üyelik, bülten aboneliği, sipariş, iş başvurusu... Bir web sitesindeki her form kişisel veri toplar. Formların çoğu teknik olarak çalışır ama KVKK açısından aynı hataları tekrar eder. Bu yazı, geliştiricinin ve site sahibinin form tasarlarken kontrol etmesi gereken noktaları sırayla anlatıyor.

> Bu yazı eğitim amaçlıdır, hukuki görüş değildir. Kendi durumunuz için bir hukukçuya danışın.

---

## 1. Aydınlatma metni ile açık rızayı tek metinde birleştirmek

En yaygın hata. **Aydınlatma** bir bilgilendirmedir: hangi veriyi, hangi amaçla, hangi hukuki sebeple işlediğinizi, kime aktardığınızı ve kişinin haklarını anlatırsınız. Kişiden onay istemezsiniz, sadece bilgi verirsiniz.

**Açık rıza** ise ayrı bir irade beyanıdır ve yalnızca kanunda sayılan diğer işleme şartları (sözleşmenin ifası, kanuni yükümlülük, meşru menfaat vb.) yoksa gerekir.

Doğrusu: Aydınlatma metni ayrı bir sayfa ya da açılır pencere olur. Açık rıza gerekiyorsa ayrı bir onay kutusuyla, ayrı bir cümleyle istenir. "Aydınlatma metnini okudum ve kabul ediyorum" ifadesi iki kavramı karıştırır; aydınlatma "kabul edilmez", okunur.

## 2. Her form için açık rıza istemek

Bir iletişim formunda kişi size kendisi yazıyor ve cevap bekliyor. Bu veriyi cevap vermek için işlemek zaten ilgili kişinin talebinin gereğidir. Buna açık rıza kutusu eklemek hem gereksizdir hem de kişi rızasını geri çektiğinde ne yapacağınız sorusunu doğurur.

Doğrusu: Önce işleme şartını belirleyin. Sipariş için sözleşmenin ifası, fatura için kanuni yükümlülük, iletişim formu için talebe cevap verme amacı genellikle yeterlidir. Açık rızayı yalnızca gerçekten gereken işlemler için isteyin: pazarlama iletisi, yurt dışına aktarım (şartları varsa), özel nitelikli veri gibi.

## 3. Hizmeti açık rızaya bağlamak

"Formu göndermek için tüm koşulları kabul etmelisiniz" kutusu işaretlenmeden gönder düğmesi çalışmıyorsa ve bu kutu pazarlama izni de içeriyorsa, verilen rıza özgür iradeye dayanmaz.

Doğrusu: Zorunlu olanla isteğe bağlı olanı ayırın. Pazarlama izni kutusu işaretlenmese de form gönderilebilmelidir.

## 4. Önceden işaretlenmiş onay kutuları

Kutunun varsayılan olarak işaretli gelmesi, kişinin bilinçli bir eylemde bulunmadığı anlamına gelir.

Doğrusu: İsteğe bağlı tüm onay kutuları boş gelir. Kişi kendisi işaretler.

## 5. Gereğinden fazla alan toplamak

İletişim formunda T.C. kimlik numarası, doğum tarihi, açık adres... Amaç için gerekli olmayan her alan, veri minimizasyonu ilkesine aykırıdır ve sızıntı durumunda riskinizi büyütür.

Doğrusu: Her alan için "bu olmadan işi yapabilir miyim?" diye sorun. Yapabiliyorsanız alanı kaldırın ya da isteğe bağlı yapın. Fatura için gereken bilgiler sipariş adımında istenir, iletişim formunda değil.

## 6. Özel nitelikli veriyi fark etmeden toplamak

Sağlık durumu, din, mezhep, dernek ve sendika üyeliği, biyometrik veri, ceza mahkûmiyeti gibi bilgiler özel nitelikli kişisel veridir ve daha sıkı kurallara tabidir. İş başvurusu formundaki "sağlık durumunuz" ya da üyelik formundaki "sendika üyeliği" alanı bu kapsama girer.

Doğrusu: Bu tür alanları gerçekten gerekmedikçe koymayın. Gerekiyorsa işleme şartını hukukçunuzla netleştirin ve bu verilere ek güvenlik önlemi uygulayın (erişim kısıtlaması, ayrı saklama, kayıt tutma).

## 7. Aydınlatma metninin formdan ulaşılamaması

Aydınlatma metni sitenin altbilgisinde bir yerde duruyor ama formun yanında bağlantısı yok. Kişi veriyi verirken bilgilendirilmiş olmalıdır.

Doğrusu: Formun hemen yanında, gönder düğmesinden önce aydınlatma metnine açık bir bağlantı olsun. Her form türü için ayrı amaç varsa (iş başvurusu, bülten, sipariş) ayrı aydınlatma metni ya da ayrı bölüm hazırlayın.

## 8. Toplanan veriyi sonsuza kadar saklamak

İletişim formundan gelen mesajlar yıllarca veritabanında ve e-posta kutusunda birikir. Saklama süresi belirlenmemiştir.

Doğrusu: Her veri türü için saklama süresi belirleyin ve bu süreyi aydınlatma metninde yazın. Süre dolunca silme, yok etme ya da anonim hale getirme işlemini düzenli olarak yapın. Bu işi bir kez elle yapıp bırakmak yerine sitenin yönetim panelinde ya da zamanlanmış bir görevle düzenli hale getirin.

## 9. Form verisini e-postayla düz metin olarak dolaştırmak

Form gönderildiğinde içerik birkaç kişinin kişisel e-posta adresine gider, oradan iletilir, telefona düşer. Verinin nerede olduğu artık kontrol edilemez.

Doğrusu: Form verisini yönetim panelinde tutun. Bildirim e-postasında yalnızca "yeni mesaj var" bilgisi ve panele bağlantı olsun. Kimlerin bu verilere eriştiğini sınırlayın ve kayıt altına alın.

## 10. Üçüncü taraf hizmetleri aydınlatma metninde anmamak

Form gönderimi bir e-posta gönderim hizmetinden, robot doğrulama bir dış servisten, istatistik bir analiz aracından geçiyor. Bu hizmetler veriyi işliyor, bir kısmı yurt dışında.

Doğrusu: Formdaki verinin geçtiği her hizmeti listeleyin. Aydınlatma metninde aktarım yapılan alıcı gruplarını ve yurt dışı aktarımı belirtin. 2024'te yürürlüğe giren değişikliklerle yurt dışına aktarımda yeterlilik kararı, standart sözleşme ve bağlayıcı şirket kuralları gibi yollar öne çıktı; standart sözleşme kullanıldığında Kurul'a bildirim yükümlülüğü de var. Bu konuyu hukukçunuzla birlikte netleştirin.

## 11. Pazarlama izni ile İYS'yi ayrı düşünmek

Bülten formunda "kampanyalardan haberdar olmak istiyorum" kutusu var, işaretleyen kişilere ticari ileti gönderiliyor, ama izin İleti Yönetim Sistemi'ne (İYS) kaydedilmiyor.

Doğrusu: Ticari elektronik ileti izni KVKK'nın yanında 6563 sayılı Kanun ve İYS kurallarına da tabidir. Formdan alınan izni, tarihi ve kanalıyla birlikte saklayın ve İYS'ye iletin. Ret ve geri çekme taleplerini de aynı şekilde işleyin.

## 12. Başvuru kanalını göstermemek

Kişi verisinin silinmesini ya da düzeltilmesini istemek istiyor ama nereye yazacağını bulamıyor.

Doğrusu: Aydınlatma metninde ilgili kişinin haklarını ve başvuru yollarını açıkça yazın. Gelen başvuruları kayıt altına alın ve kanunda öngörülen süre içinde (en geç otuz gün) sonuçlandırın.

---

## Kısa kontrol listesi

- [ ] Her form için işleme amacı ve hukuki sebep belirlendi
- [ ] Aydınlatma metni formun yanından tek tıkla açılıyor
- [ ] Aydınlatma ile açık rıza ayrı
- [ ] Açık rıza yalnızca gereken yerde ve ayrı kutuyla isteniyor
- [ ] İsteğe bağlı kutular boş geliyor, işaretlenmeden form gönderilebiliyor
- [ ] Gereksiz alan yok
- [ ] Özel nitelikli veri alanı yok ya da gerekçesi belirlendi
- [ ] Saklama süresi belirlendi ve düzenli siliniyor
- [ ] Form verisi panelde, e-postada yalnızca bildirim
- [ ] Veri işleyen üçüncü taraf hizmetler aydınlatma metninde
- [ ] Pazarlama izni İYS'ye iletiliyor
- [ ] Başvuru kanalı açıkça yazılı

---

## Kaynaklar

- Kişisel Verileri Koruma Kurumu — [kvkk.gov.tr](https://www.kvkk.gov.tr)
- Aydınlatma Yükümlülüğünün Yerine Getirilmesinde Uyulacak Usul ve Esaslar Hakkında Tebliğ
- KVKK Çerez Uygulamaları Hakkında Rehber
- İleti Yönetim Sistemi — [iys.org.tr](https://iys.org.tr)

---

Bu yazı [kvkk-icin-web-gelistirici-rehberi](../README.md) deposunun bir parçasıdır. Soru ve önerileriniz için deponun **Discussions** bölümünü kullanabilirsiniz.

Hazırlayan: [Alesta WEB](https://alestaweb.com) — İzmir
