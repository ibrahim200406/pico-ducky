# Wifi Şifrelerini Mail Olarak Gönderen Pico-Ducky Scripti

Rasspberry Pi Pico mikrodenetliyicinizi nasıl Pico-Ducky’ye dönüştüreceğinizi <a href="https://www.youtube.com/watch?v=26uxyjxVAm0" target="_blank">bu linkten</a> öğrenebilirsiniz.

#### Gerekli Malzemeler:
  - Rasspberry Pi Pico
  - USB to Micro-USB kablo
  - Dişi-dişi jumper(opsiyonel)

Raspberry Pi Pico’nun bilgisayara bağlandığında depolama aygıtı olarak tanınmasını engellemek için Pin 18 ile Pin 20 jumper kablosu aracılığıyla birbirine bağlanmalıdır.

Ayrıca, Rubber Ducky scriptini çalıştırmadan üzerinde değişiklik yapabilmek için Pin 1 ile Pin 3’ü birbirine bağlamanız yeterlidir.

### Uygulama Şifresi
Uygulama şifresi oluşturmak için ilk önce <a href="https://myaccount.google.com/" target="_blank">myaccount.google.com</a> adresine gidip sol taraftaki menüden “Güvenlik” seçeneği seçip 2 Adımda Doğrulama özelliğini etkinleştirin.Daha sonra arama kutusuna Uygulama Şifreleri yazarak ilgili yere Google şifreniz ile giriş yaptıktan sonra 16 haneli şifrenizi oluşturun ve kopyalayıp Tamamlandı seçeneğini seçin.

### Sistemde Minimum İz Bırakmak İçin Aldığımız Önlemler


`STRING (Set-ItemProperty -Path "HKLM:\Software\Policies\Microsoft\Windows\PowerShell\ScriptBlockLogging" -Name EnableScriptBlockLogging -Value 0)`

Yukarıdaki script “ScriptBlockLogging” açık ise poweshell loglarında bundan sonra yazılacak kodların kaydının tutulmasını engelliyor.

`STRING Remove-Item -Path .\wifi_list.txt -Force`

Yukarıdaki script masaüstünde oluşturmuş olduğumuz “wifi_list.txt” dosyasını Geri Dönüşüm Kutusu’na göndermeden kalıcı olarak silerek minimum iz bırakmamızı sağlıyor.

### Test Videosu İçin Aşağıdaki Görsele Tıklay
[![Test Videosu](https://www.youtube.com/watch?v=Xh_u0xwmcZA)


