# Windows 10 [Pro - Home - HomeSingleLangue] OgnitorenKs Performans Düzenlemesi
- Lisans durumunuza göre istediğinizi seçebilirsiniz. Sources klasörü içerisine eklenen ei.cfg nedeniyle kurulum ekranında lisanslı sürümü otomatik seçmez. Otomatik seçmesini istiyorsanız Rufus ile USB'ye yazdıktan sonra Sources klasörü içerisinde ei.cfg dosyasını silin.

- ISO kalıbı UUPDump sitesinden indirilmiştir.
 
#### Sistemde Kapatılan Servisler
Aşağıda ► işaretinde yazdığım komutlar servisleri varsayılan haline getirip açmaktadır. Kullanmak için CMD yönetici olarak açtıktan sonra kopyala,yapıştır yapıp uygulamanız gerekmektedir.
 
    • SCardSvr = Akıllı Kart
      ► sc config SCardSvr start= demand&net start SCardSvr /y
      
    • ScDeviceEnum = Akıllı Kart Cihaz Numaralandırma İlkesi
      ► sc config ScDeviceEnum start= demand&net start ScDeviceEnum /y
      
    • SCPolicySvc = Akıllı Kart Kaldırma İlkesi
      ► sc config SCPolicySvc start= demand&net start SCPolicySvc /y
      
    • AJRouter = AllJoyn Yönlendirici Hizmeti
      ► sc config AJRouter start= demand&net start AJRouter /y
      
    • BDESVC = Bitlocker Sürücü Şifreleme Hizmeti 
      ► sc config BDESVC start= demand&net start BDESVC /y
      
    • lfsvc = Coğrafi Konum Hizmeti 
      ► sc config lfsvc start= demand&net start lfsvc /y
      
    • WalletService = Cüzdan Hizmeti 
      ► sc config WalletService start= demand&net start WalletService /y
      
    • TrkWks = Dağıtılmış Bağlantı İzleme İstemcisi
      ► sc config TrkWks start= auto&net start TrkWks /y
      
    • diagsvc = Tanılama Yürütme Hizmeti
      ► sc config diagsvc start= demand&net start diagsvc /y
      
    • TabletInputService = Dokunmatik Klavye ve El yazısı hizmeti
      ► sc config TabletInputService start= demand&net start TabletInputService /y
    
    • Fax
      ► sc config Fax start= demand&net start Fax /y
      
    • fhsvc = Dosya Geçmişi Hizmeti
      ► sc config fhsvc start= demand&net start fhsvc /y
      
    • PimIndexMaintenanceSvc = Kişi Verileri
      ► sc config PimIndexMaintenanceSvc start= demand&net start PimIndexMaintenanceSvc /y
      
    • EntAppSvc = Kurumsal Uygulama Yönetimi Hizmeti
      ► sc config EntAppSvc start= demand&net start EntAppSvc /y
      
    • edgeupdate / edgeupdatem / MicrosoftEdgeElevationService = Microsoft Edge Güncelleştirme Servisi
      ► sc config edgeupdate start= auto&net start edgeupdate /y
      ► sc config edgeupdatem start= demand&net start edgeupdatem /y
      ► sc config MicrosoftEdgeElevationService start= demand&net start MicrosoftEdgeElevationService /y
      
    • NaturalAuthentication = Natural Kimlik Doğrulaması
      ► sc config NaturalAuthentication start= demand&net start NaturalAuthentication /y
      
    • RetailDemo = Perakende Gösteri Hizmeti
      ► sc config RetailDemo start= demand&net start RetailDemo /y
      
    • PrintWorkflowUserSvc = 
      ► sc config PrintWorkflowUserSvc start= demand&net start PrintWorkflowUserSvc /y
      
    • PcaSvc = Program Uyumluluk Yardımcısı Hizmeti
      ► sc config PcaSvc start= demand&net start PcaSvc /y
      
    • RmSvc = Radyo Yönetimi Hizmeti
      ► sc config RmSvc start= demand&net start RmSvc /y
    
    • WiaRpc = Resim Alma Olayları
      ► sc config WiaRpc start= demand&net start WiaRpc /y
      
    • CertPropSvc = Sertifika Yayma
      ► sc config CertPropSvc start= demand&net start CertPropSvc /y
    
    • SysMain = Hızlı Getir
      ► sc config SysMain start= auto&net start SysMain /y
    
    • TapiSrv = Telefon hizmeti
      ► sc config TapiSrv start= demand&net start TapiSrv /y
      
    • PhoneSvc = Telefon hizmeti
      ► sc config PhoneSvc start= demand&net start PhoneSvc /y
    
    • TermService = Uzak Masaüstü Hizmetleri
      ► sc config TermService start= demand&net start TermService /y
      
    • SharedRealitySvc = Uzamsal Veri Hizmeti
      ► sc config SharedRealitySvc start= demand&net start SharedRealitySvc /y
      
    • DusmSvc = Veri Kullanımı
      ► sc config DusmSvc start= auto&net start DusmSvc /y
      
    • VacSvc = Volumetrik Ses Oluşturucu Hizmeti
      ► sc config VacSvc start= demand&net start VacSvc /y
      
    • perceptionsimulation = Windows Algılama Benzetimi hizmeti
      ► sc config perceptionsimulation start= demand&net start perceptionsimulation /y
      
    • spectrum = Windows Algılama Hizmeti
      ► sc config spectrum start= demand&net start spectrum /y
      
    • WbioSrvc = Windows Biyometrik Hizmeti
      ► sc config WbioSrvc start= demand&net start WbioSrvc /y
    
    • WerSvc = Windows Hata Raporlama Hizmeti
      ► sc config WerSvc start= demand&net start WerSvc /y
      
    • wisvc = Windows Insider Hizmeti
      ► sc config wisvc start= demand&net start wisvc /y
      
    • FrameServer = Kamera Çerçeve Sunucusu
      ► sc config FrameServer start= demand&net start FrameServer /y
      
    • MixedRealityOpenXRSvc = Karma Gerçeklik Hizmeti
      ► sc config MixedRealityOpenXRSvc start= demand&net start MixedRealityOpenXRSvc /y
    
    • stisvc = Windows Resim Alma (WIA)
      ► sc config stisvc start= demand&net start stisvc /y
    
    • WSearch = Windows Search
      ► sc config WSearch start= auto&net start WSearch /y
      
    • FontCache = Windows Yazı Tipi önbelleği hizmeti
      ► sc config FontCache start= auto&net start FontCache /y
      
    • SDRSVC = Windows Yedekleme
      ► sc config SDRSVC start= demand&net start SDRSVC /y
      
    • Spooler = Yazdırma Biriktiricisi
      ► sc config SDRSVC start= demand&net start SDRSVC /y
      
    • SEMgrSvc = Ödeme NFC/SE Yöneticisi
      ► sc config SEMgrSvc start= demand&net start SEMgrSvc /y
      
    • TroubleshootingSvc = Önerilen Sorun Giderme Hizmeti
      ► sc config TroubleshootingSvc start= demand&net start TroubleshootingSvc /y
      
    • seclogon = İkincil Oturum Açma
      ► sc config seclogon start= demand&net start seclogon /y
      
    • MapsBroker = İndirilen Haritalar Yöneticisi
      ► sc config MapsBroker start= auto&net start MapsBroker /y
      
    • workfolderssvc = Çalışma klasörleri istemcisi
      ► sc config workfolderssvc start= demand&net start workfolderssvc /y
      
    • PeerDistSvc = BrancCache
      ► sc config PeerDistSvc start= demand&net start PeerDistSvc /y
      
    • IpxlatCfgSvc = IP Yardımcısı hizmeti
      ► sc config IpxlatCfgSvc start= auto&net start IpxlatCfgSvc /y
      
    • iphlpsvc = IP Çeviri Yapılandırma Hizmeti
      ► sc config iphlpsvc start= demand&net start iphlpsvc /y
      
    • swprv = Microsoft Yazılımı Gölge Kopya Sağlayıcısı
      ► sc config swprv start= demand&net start swprv /y
      
    • wbengine = Blok Düzeyinde Yedekleme Altyapı Hizmeti
      ► sc config wbengine start= demand&net start wbengine /y
      
    • VSS = Birim Gölge Kopyası
      ► sc config VSS start= demand&net start VSS /y
      
    • CscService = Çevrimdışı Hizmetler
      ► sc config CscService start= demand&net start CscService /y
      
    • Themes = Tema hizmeti
      ► sc config Themes start= auto&net start Themes /y
      
    • DPS = Tanı ilkesi hizmeti
      ► sc config DPS start= auto&net start DPS /y
      
#### Sistemde Çalışma Durumu Değiştirilen Servisler
    • StorSvc = Depolama hizmeti = (Otomatik > Manuel)
      ► sc config StorSvc start= auto&net start StorSvc /y

#### Sistemde Kaldırılan Servisler
    • DiagTrack = Bağlı Kullanıcı Deneyimi ve Telemetrisi
    • dmwappushservice = Cihaz Yönetimi Kablosuz Uygulama Protokolü (WAP) Anında İleti Yönlendirme Hizmeti
    • diagnosticshub.standartcollector.service = Microsoft (R) Diagnostics Hub Standard Collector Service
    • SecurityHealthService = Windows Güvenlik Hizmeti
    • Sense = Windows Defender Advanced Threat Protection Service 
    • SgrmBroker = Sistem Koruma Çalışma Zamanı İzleyicisi Aracısı
    • WdNisSvc = Microsoft Defender Antivirüs Ağ İnceleme Hizmeti
    • WinDefend = Microsoft Defender Virüsten Koruma Hizmeti
    • wscsvc = Güvenlik Merkezi
    
