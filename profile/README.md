## /login
Kullanıcı kendi bilgileriyle sisteme giriş yapabilir. Email ve password kısmını doldurduktan sonra "Login" butonu aktifleşir. Email'in doğruluğu için Regular Expression kullanılmıştır. RegExp testini geçtiğinde buton aktifleşir.
> _/api/login_ endpoint'ini kullanarak sisteme giriş yapar.

![image](https://github.com/talentsphere/.github/assets/79156797/51161abb-31d5-4822-9dfe-fac89c0e6496)

---
## /forgot-password
Kullanıcı _/login_ ekranından **"Forgot Password?"**'e tıklarsa /forgot-password sayfasına yani, şifre değiştirme akışının ilk aşamasına yönlendirilir. Burda da RegExp kullanılmıştır.

![image](https://github.com/talentsphere/.github/assets/79156797/d3b22583-d39e-4070-98f2-62ec1d535526)

---
## /verify-email
Şifre değiştirme akışının 2. adımı olan bu aşamada, kullanıcı mail'ine gönderilen kodu burada girer ve mail'ini doğrular. Butonun aktif olması için 6 haneli kod girilmesi gerekiyor. 6 karakterden fazla yazılamıyor.
> _/api/sendMail_ endpoint'i ile entegrasyonu yapılacaktır.
> 
![image](https://github.com/talentsphere/.github/assets/79156797/09495396-c28c-4638-9118-dffd9d808da6)

---
## /reset-password
Şifre değiştirme akışının son adımı. Yeni şifreyi giren kullanıcı bu ekrandan şifresini doğrudan değiştirebilir. Ekranın alt kısmında yer alan kriterleri sağladıktan sonra buton aktif olur ve kullanıcı şifreyi yeniler. Sağlanan şartlar yeşil ile, sağlanmayan şartlar kırmızı ile gösterilir.
Bu adımdan sonra kullanıcı tekrardan _/login_ sayfasına yönlendirilir

![image](https://github.com/talentsphere/.github/assets/79156797/5fa93a3d-d081-4ec9-8280-053bf27f5ab5)

---
## /recent-activities
Kullanıcı sisteme log-in olduktan sonra rolüne göre sayfaya yönlendirilir. Admin hariç tüm roller için bu sayfa _/recent-activities_'dir. Daha sonrasında kullanıcı sol taraftaki sidebar'dan istediği sayfaya yönlendirilir. Bu sidebar kullanıcının rolüne göre açılır. 
> Şu an rollere göre açılan sidebar menüleri statiktir. İlerleyen süreçte permission'lara göre sidebar açılacaktır.

Kullanıcı header'da bulunan (avatarın hemen sağında) log-out butonu ile sistemdeki oturumunu kapatabilir.

![image](https://github.com/talentsphere/.github/assets/79156797/04b01809-c3dc-430e-bc8c-9389b6f61f20)
