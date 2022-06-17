# Windows 10 - 11 sık sorulan sorular
### Windows 10'mu Windows 11'mi kurmalıyım?
Sistem gereksinimleri Windows 11'in ihtiyaçlarını karşılıyorsa Windows 11 kurabilirsiniz. Desteklemediği durumlarda TPM şartı arayan oyun veya uygulamalarda sorun yaşayabilirsiniz. Kurulum aşamalarında bu ihtiyaçları her ne kadar Bypass etme şansımız olsa da bu tarz durumlarda yaşayacağınız hatanın çözümü yoktur. Mecburen Windows 10 yüklemeniz gerekir. Windows 11'in en azından bir sürüm sonra daha kararlı olacağını düşünüyorum. 22H2 sürümünü beklemekte fayda var.
### Sistemleri nasıl düzenliyorum?
Sistemlerde yaptığım değişikliklerin bir kısmını kendi hazırladığım Builder.bat ile yapıyorum geri kalan bölümleri NTLite ile düzenliyorum. Builder'ı daha önceden isteyenler için paylaşıyordum ancak yaptığım değişikliklerden sonra paylaşmama kararı aldım. Yapılan değişiklikler hakkında çok detaylı bir rehber hazırlıyorum. Yayınladığımda oradan bakabilirsiniz. Lütfen Builder.bat için istekte bulunmayınız.
### Windows 8.1 sistem linkleri güncellenecek mi?
Windows 8.1 sistemler artık güncellenmeyecek. Bu bölümde güncellemeyi durdurduğum için Toolbox'a da güncelleme vermiyorum. 
### Windows 10-11 sistemlerde Microsoft Store ve Xbox yüklü mü?
Evet yüklüdür. Microsoft Store / Mail / Takvim / Hesap makinesi / Ekran Yakalama / Appx Installer ve Store için gerekli olan servisler yüklüdür. Uygulama veya oyunlarda herhangi bir hata almazsınız. 
### Windows 10-11 sistemlerinizde yazıcım çalışmıyor, nasıl düzeltirim?
Yazıcı hizmetleri kapalıdır. Açmak için Toolbox'dan  'Hizmetleri Yönet' bölümünden yazıcı hizmetini aktifleştirebilirsiniz. CMD üzerinden etkinleştirmek için aşağıdaki komutları yönetici yetkili CMD ekranına yapıştırın.

    • sc config Spooler start= auto
    • net start Spooler /y

