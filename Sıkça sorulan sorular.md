# Windows 10 - 11 sık sorulan sorular
### Windows 10'mu Windows 11'mi kurmalıyım?
Sistem gereksinimleri Windows 11'in ihtiyaçlarını karşılıyorsa Windows 11 kurabilirsiniz. Desteklemediği durumlarda TPM şartı arayan oyun veya uygulamalarda sorun yaşayabilirsiniz. Kurulum aşamalarında bu ihtiyaçları her ne kadar Bypass etme şansımız olsa da bu tarz durumlarda yaşayacağınız hatanın çözümü yoktur. Mecburen Windows 10 yüklemeniz gerekir. Windows 11'in en azından bir sürüm sonra daha kararlı olacağını düşünüyorum. 22H2 sürümünü beklemekte fayda var.

### Sistemleri nasıl düzenliyorum?
Sistemlerde yaptığım değişikliklerin bir kısmını kendi hazırladığım Builder.bat ile yapıyorum geri kalan bölümleri NTLite ile düzenliyorum. Builder'ı daha önceden isteyenler için paylaşıyordum ancak yaptığım değişikliklerden sonra paylaşmama kararı aldım. Yapılan değişiklikler hakkında çok detaylı bir rehber hazırlıyorum. Yayınladığımda oradan bakabilirsiniz. Lütfen Builder.bat için istekte bulunmayınız.

### Windows 8.1 sistem linkleri güncellenecek mi?
Windows 8.1 sistemler artık güncellenmeyecek. Bu bölümde güncellemeyi durdurduğum için Toolbox'a da güncelleme vermiyorum. 

### Windows 10-11 sistemlerde Microsoft Store ve Xbox yüklü mü?
Evet yüklüdür. Microsoft Store / Mail / Takvim / Hesap makinesi / Ekran Yakalama / Appx Installer ve Store için gerekli olan servisler yüklüdür. Uygulama veya oyunlarda herhangi bir hata almazsınız. 

### Windows 10-11 sistemlerinizde yazıcı çalışmıyor, nasıl düzeltirim?
Yazıcı hizmetleri kapalıdır. Yazıcı hizmeti otomatik ayarın dışında çalışırken hata verdiği için ve yazıcı cihazı her evde bulunmadığından gereksiz işlem yükünü engellemek için kapattım. Açmak için Toolbox'dan  'Hizmetleri Yönet' bölümünden yazıcı hizmetini aktifleştirebilirsiniz. CMD üzerinden etkinleştirmek için aşağıdaki komutları yönetici yetkili CMD ekranına yapıştırın. Hizmetlerden açmak istiyorsanız 'Yazdırma biriktiricisi' ayarını otomatiğe alıp başlatınız.

    • sc config UmRdpService start= demand
    • sc config Spooler start= auto
    • net start Spooler /y
    
### Windows 10-11 sistemlerinizde Fax cihazı çalışmıyor, nasıl düzeltirim?
Fax hizmeti kaldırılmıştır. Fax cihazı evde bulunmayı geçtim artık normal şartlarda bile bulunması zor olan bir cihaz bundan dolayı hizmeti tamamen sildim. yeniden yüklemek için aşağıdaki komutları yönetici yetkili CMD ekranına uygulayabilirsiniz. 
    • Dism /Online /Add-Capability /CapabilityName:Print.Fax.Scan~~~~0.0.1.0
    • sc config Fax start= demand
    • sc config UmRdpService start= demand
    
### Windows 10-11 sistemlerinizde tarayıcı cihazı çalışmıyor, nasıl düzeltirim?
Tarayıcı hizmetleri kapatılmıştır. Tarayıcı cihazıda maalesef her evde bulunmuyor. Gereksiz işlem yükünü önlemek için kapatılmıştır. Açmak için yönetici yetkili CMD ekranına aşağıdaki komutları uygulayın. Toolbox'dan açmak için Hizmetleri yönet bölümünden 'Kamera ve Tarayıcı hizmetini' açabilirsiniz.

    • sc config WiaRpc start= demand
    • sc config StiSvc start= demand
    • sc config FrameServer start= demand
    
### Windows 10-11 sistemlerinizde kamera cihazı çalışmıyor, nasıl düzeltirim?
Kamera cihazının yönetimini sağlayan hizmet kapatılmıştır. Kameranızı çalışır ancak birden fazla kameraya erişmek istediğinden hata alabilirsiniz. Bunu engellemek için tarayıcı cihazları için uyguladığımız komutları burada da uyguluyoruz. Açmak için yönetici yetkili CMD ekranına aşağıdaki komutları uygulayın. Toolbox'dan açmak için Hizmetleri yönet bölümünden 'Kamera ve Tarayıcı hizmetini' açabilirsiniz.

    • sc config WiaRpc start= demand
    • sc config StiSvc start= demand
    • sc config FrameServer start= demand
    
### Windows 10 sistemde mikrofon ayarlarına girerken alınan 'bellek taşma hatası' nasıl düzeltilir?
Toolbox'dan Optimizasyon bölümünden SVChost Ram Optimizasyonu bölümünü uyguladıysanız bu sorunu yaşamanıza sebebiyet verebilir. Düzeltmek için aynı yerden kapatma komutunu uygulayınız. 

Bir diğer ihtimal ise driver'dan kaynaklanır. Bunu çözmek için driverı donanım kimliği ile tespit edip indirmeniz gerekiyor. Eski driverı sildikten sonra yeni indirdiğiniz driverı uygulayarak çözebilirsiniz. Donanım kimliğiyle driver bulmayı bilmiyorsanız Google'dan aratıp bilgi sahibi olabilirsiniz. Birçok açıklayıcı rehber bulunmaktadır.

Bu iki yolda çözüme ulaştırmadıysa PC'nizde farklı bir sorun söz konusudur. Bildiğim başka bir çözümü yoktur.

### Windows 10-11 sistemde Driverlar otomatik yüklenmedi, nasıl düzeltilir?
Bazı geri bildirimlerde donanımı sorunlu olup pasif halde bırakarak kullanan kişilerin bu ayardan dolayı blue screen hatası aldığını tespit ettiğim için kapattım. Buradaki Blue Screen kullanıcının bozuk donanımından kaynaklanmaktadır. Ayrıca Windows Update her zaman güncel driverları kurmadığından kapatmak daha uygun geldi. Ancak bu bölümü kullanmak isteyenler toolbox üzerinden 'Hizmetleri Yönet' bölümünden 'Driver Yükle/Güncelle hizmetini' açabilir. CMD ile açmak isteyenler yönetici yetkili CMD ekranına aşağıdaki komutları uygulamalıdır.

    • reg add "HKLM\SOFTWARE\Microsoft\PolicyManager\current\device\Update" /v "ExcludeWUDriversInQualityUpdate" /t REG_DWORD /d 0 /f
    • reg add "HKLM\SOFTWARE\Microsoft\PolicyManager\default\Update" /v "ExcludeWUDriversInQualityUpdate" /t REG_DWORD /d 0 /f
    • reg add "HKLM\SOFTWARE\Microsoft\PolicyManager\default\Update\ExcludeWUDriversInQualityUpdate" /v "value" /t REG_DWORD /d 0 /f
    • reg add "HKLM\SOFTWARE\Microsoft\WindowsUpdate\UX\Settings" /v "ExcludeWUDriversInQualityUpdate" /t REG_DWORD /d 0 /f 
    • reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate" /v "ExcludeWUDriversInQualityUpdate" /t REG_DWORD /d 0 /f 
    • reg add "HKLM\Software\Policies\Microsoft\Windows\DriverSearching" /v "SearchOrderConfig" /t REG_DWORD /d 1 /f 


























