## /login
Kullanıcı kendi bilgileriyle sisteme giriş yapabilir. Email ve password kısmını doldurduktan sonra "Login" butonu aktifleşir. Email'in doğruluğu için Regular Expression kullanılmıştır. RegExp testini geçtiğinde buton aktifleşir.
> _/api/login_ endpoint'ini kullanarak sisteme giriş yapar.

![image](https://github.com/talentsphere/.github-private/assets/79156797/cc8bb116-98d8-4a32-8ca2-11404f851f5f)

---
## /forgot-password
Kullanıcı _/login_ ekranından **"Forgot Password?"**'e tıklarsa /forgot-password sayfasına yani, şifre değiştirme akışının ilk aşamasına yönlendirilir. Burda da RegExp kullanılmıştır.

![image](https://github.com/talentsphere/.github-private/assets/79156797/26c6fee9-c6f5-49c5-89ff-1571f1cf1844)

---
## /verify-email
Şifre değiştirme akışının 2. adımı olan bu aşamada, kullanıcı mail'ine gönderilen kodu burada girer ve mail'ini doğrular. Butonun aktif olması için 6 haneli kod girilmesi gerekiyor. 6 karakterden fazla yazılamıyor.
> _/api/sendMail_ endpoint'i ile entegrasyonu yapılacaktır.
![image](https://github.com/talentsphere/.github-private/assets/79156797/37cf68b0-649a-4f6a-85f9-3b966b84342d)

---
## /reset-password
Şifre değiştirme akışının son adımı. Yeni şifreyi giren kullanıcı bu ekrandan şifresini doğrudan değiştirebilir. Ekranın alt kısmında yer alan kriterleri sağladıktan sonra buton aktif olur ve kullanıcı şifreyi yeniler. Sağlanan şartlar yeşil ile, sağlanmayan şartlar kırmızı ile gösterilir.
Bu adımdan sonra kullanıcı tekrardan _/login_ sayfasına yönlendirilir

![image](https://github.com/talentsphere/.github-private/assets/79156797/37fd6d89-b7cc-4c98-a71c-5df139c25ded)

---
## /recent-activities
Kullanıcı sisteme log-in olduktan sonra rolüne göre sayfaya yönlendirilir. Admin hariç tüm roller için bu sayfa _/recent-activities_'dir. Daha sonrasında kullanıcı sol taraftaki sidebar'dan istediği sayfaya yönlendirilir. Bu sidebar kullanıcının rolüne göre açılır. 
> Şu an rollere göre açılan sidebar menüleri statiktir. İlerleyen süreçte permission'lara göre sidebar açılacaktır.

Kullanıcı header'da bulunan (avatarın hemen sağında) log-out butonu ile sistemdeki oturumunu kapatabilir.

![image](https://github.com/talentsphere/.github-private/assets/79156797/0f4a8365-3d90-4b0b-974a-ed7ede77e9df)
