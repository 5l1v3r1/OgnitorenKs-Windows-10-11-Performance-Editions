# Windows 10 [Pro - Home - HomeSingleLangue] OgnitorenKs Performans Düzenlemesi
- Lisans durumunuza göre istediğinizi seçebilirsiniz. Sources klasörü içerisine eklenen ei.cfg nedeniyle kurulum ekranında lisanslı sürümü otomatik seçmez. Otomatik seçmesini istiyorsanız Rufus ile USB'ye yazdıktan sonra Sources klasörü içerisinde ei.cfg dosyasını silin.

- ISO kalıbı UUPDump sitesinden indirilmiştir.
 
### Sistemde Kapatılan Servisler
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
      
### Sistemde Çalışma Durumu Değiştirilen Servisler
    • StorSvc = Depolama hizmeti = (Otomatik > Manuel)
      ► sc config StorSvc start= auto&net start StorSvc /y

### Sistemde Kaldırılan Servisler
    • DiagTrack = Bağlı Kullanıcı Deneyimi ve Telemetrisi
    • dmwappushservice = Cihaz Yönetimi Kablosuz Uygulama Protokolü (WAP) Anında İleti Yönlendirme Hizmeti
    • diagnosticshub.standartcollector.service = Microsoft (R) Diagnostics Hub Standard Collector Service
    • SecurityHealthService = Windows Güvenlik Hizmeti
    • Sense = Windows Defender Advanced Threat Protection Service 
    • SgrmBroker = Sistem Koruma Çalışma Zamanı İzleyicisi Aracısı
    • WdNisSvc = Microsoft Defender Antivirüs Ağ İnceleme Hizmeti
    • WinDefend = Microsoft Defender Virüsten Koruma Hizmeti
    • wscsvc = Güvenlik Merkezi
    
### Görev Zamanlayıcısı Üzerinde Yapılan Değişiklikler
    • Microsoft\Windows\Windows Defender\Windows Defender Cache Maintenance
    • Microsoft\Windows\Windows Defender\Windows Defender Cleanup
    • Microsoft\Windows\Windows Defender\Windows Defender Scheduled Scan
    • Microsoft\Windows\Windows Defender\Windows Defender Verification
    • Microsoft\Windows\WindowsUpdate\Scheduled Start
    • Microsoft\Windows\Maps\MapsToastTask
    • Microsoft\Windows\Maps\MapsUpdateTask
    • Microsoft\Windows\DiskDiagnostic\Microsoft-Windows-DiskDiagnosticDataCollector
    • Microsoft\Windows\SystemRestore\SR
    • Microsoft\Windows\Speech\SpeechModelDownloadTask"
    • Microsoft\Windows\UpdateOrchestrator\UpdateModelTask
    • Microsoft\Windows\Application Experience\ProgramDataUpdater
    • Microsoft\Windows\Application Experience\StartupAppTask
    • Microsoft\Windows\Application Experience\Microsoft Compatibility Appraiser
    • Microsoft\Windows\Application Experience\ProgramDataUpdater
    • Microsoft\Windows\DiskCleanup\SilentCleanup
    • Microsoft\Windows\Windows Error Reporting\QueueReporting
    • Microsoft\Windows\WindowsUpdate\Scheduled Start
    • Microsoft\Windows\Power Efficiency Diagnostics\AnalyzeSystem
    • Microsoft\Windows\RemoteAssistance\RemoteAssistanceTask
    • Microsoft\Windows\Time Zone\SynchronizeTimeZone
    • Microsoft\Windows\UpdateOrchestrator\Schedule Scan
    • Microsoft\Windows\UpdateOrchestrator\Schedule Scan Static Task
    • Microsoft\Windows\UpdateOrchestrator\UpdateModelTask
    • Microsoft\Windows\WaaSMedic\PerformRemediation
 
 ### Regedit Üzerinde Yapılan Değişiklikler
 #### Silinenler
    • HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\MyComputer\NameSpace\{0DB7E03F-FC29-4DC6-9020-FF41B59E513A}
Call :delete "HKLM\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Explorer\MyComputer\NameSpace\{0DB7E03F-FC29-4DC6-9020-FF41B59E513A}" & :: 3D Nesneler

#### Eklenenler
    • HKCR\*\shell\runas" "Sahipliği Al"
Call :sz "HKCR\*\shell\runas" "Icon" "imageres.dll,73" & :: Sahipliği al
Call :sz "HKCR\*\shell\runas" "NoWorkingDirectory" "" & :: Sahipliği al
Call :vesz "HKCR\*\shell\runas\command" "cmd.exe /c takeown /f \"%1\" && ica \"%1\" /grant administrators:F" & :: Sahipliği al
Call :sz "HKCR\*\shell\runas\command" "IsolatedCommand" "cmd.exe /c takeown /f \"%1\" && ica \"%1\" /grant administrators:F" & :: Sahipliği al
Call :vesz "HKCR\Directory\shell\runas" "Sahipliği Al" & :: Sahipliği al
Call :sz "HKCR\Directory\shell\runas" "Icon" "imageres.dll,73" & :: Sahipliği al
Call :sz "HKCR\Directory\shell\runas" "NoWorkingDirectory" "" & :: Sahipliği al
Call :vesz "HKCR\Directory\shell\runas\command" "cmd.exe /c takeown /f \"%1\" /r /d y && ica \"%1\" /grant administrators:F /t" & :: Sahipliği al
Call :sz "HKCR\Directory\shell\runas\command" "IsolatedCommand" "cmd.exe /c takeown /f \"%1\" /r /d y && ica \"%1\" /grant administrators:F /t" & :: Sahipliği al
Call :sz "HKCR\.bat\ShellNew" "NullFile" "" & :: Sağ tık Yeni bölümüne Bat dosyası oluşturma ekle
Call :delete "HKCR\CABFolder\Shell\RunAs" & :: Sağ-tık CAB installer
Call :vesz "HKCR\CABFolder\Shell\RunAs" "Yükle" & :: Sağ-tık CAB installer
Call :sz "HKCR\CABFolder\Shell\RunAs" "HasLUAShield"  "" & :: Sağ-tık CAB installer
Call :vesz "HKCR\CABFolder\Shell\RunAs\Command" "cmd /k dism /online /add-package /packagepath:\"%%%%1\""  & :: Sağ-tık CAB installer
Call :dword "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\ContentDeliveryManager" "SubscribedContent-338393Enabled" 0
Call :dword "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\ContentDeliveryManager" "SubscribedContent-353694Enabled" 0
Call :dword "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\ContentDeliveryManager" "SubscribedContent-353696Enabled" 0
Call :sz "HKCU\Control Panel\Desktop" "AutoEndTasks" 1 
Call :sz "HKCU\Control Panel\Desktop" "HungAppTimeout" "10000" & :: Uygulamalar cevap vermediği zaman görevi sonlandır seçeneğine basılmadan önceki bekleme süresini kısaltır.
Call :sz "HKCU\Control Panel\Desktop" "WaitToKillAppTime" "20000" & :: Bilgisayar kapatılırken ya da oturumdan çıkılırken kullanıcı uygulamalarının kapatılması için sistem bekleme süresini kısaltır.
Call :sz "HKCU\Control Panel\Desktop" "LowLevelHooksTimeout" "1000" & :: Cevap vermeyen hizmetlerin kapatılmasından önceki sistem bekleme süresini kısaltır.
Call :sz "HKLM\SYSTEM\CurrentControlSet\Control" "WaitToKillServiceTimeout" "2000" & :: Bilgisayarın kapatılması sırasında durdurulacak hizmetler uyarısı geldiğinde, uygulamaların kapanması için beklenen süreyi kısaltır.
Call :sz "HKCU\Control Panel\Desktop" "MenuShowDelay" "8" & :: Menü gösterimi bekleme süresini azaltır. Böylelikle tıklandığı zaman menüler daha hızlı gelecek.
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" "NoLowDiskSpaceChecks" 1 & :: Düşük Depolama alanı uyarısı devre dışı bırakılıyor...
Call :dword "HKCU\Control Panel\Mouse" "MouseHoverTime" 8 & :: :: Farenizle birlikte bir nesnenin üzerine geldiğinizde görülen açıklamanın çıkış süresini kısaltır
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" "LinkResolveIgnoreLinkInfo" 1 & :: Bilgisayarınızda mevcut olmayan programlara ait kısayolların bağlantısının Windows tarafından boşa vakit harcanarak aranmasını önler
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" "NoResolveSearch" 1 & :: Kısayol bağlantı sorununu çözmek için Windows'un diski aramasını önler
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" "NoResolveTrack" 1 & :: Kısayol bağlantı sorununu çözmek için Windows'un NTFS dosya sisteminin izleme özelliğini kullanmasını engeller
Call :dword "HKCU\SOFTWARE\Policies\Microsoft\Windows\CurrentVersion\QuietHours" "Enable" 1 & :: Odak Yardımı aktifleştiriliyor
Call :dword "HKCU\Software\Microsoft\Narrator\QuickStart" "SkipQuickStart" 1 & :: Narrator QuickStart kapatılıyor.
Call :dword "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\BackgroundAccessApplications\Microsoft.Photos.8wekyb3d8bbwe" Disabled 1 & ::Fotoğraflar uygulaması arka planda çalışmaz
Call :dword "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\BackgroundAccessApplications\Microsoft.Photos.8wekyb3d8bbwe" SleepDisabled 1 & ::Fotoğraflar uygulaması arka planda çalışmaz
Call :dword "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\BackgroundAccessApplications\Microsoft.Photos.8wekyb3d8bbwe" DisabledByUser 1 & :: Fotoğraflar uygulaması arka planda çalışmaz
:: Driver Update
Call :dword "HKLM\SOFTWARE\Microsoft\PolicyManager\current\device\Update" "ExcludeWUDriversInQualityUpdate" "1"
Call :dword "HKLM\SOFTWARE\Microsoft\PolicyManager\default\Update" "ExcludeWUDriversInQualityUpdate" "1"
Call :dword "HKLM\SOFTWARE\Microsoft\PolicyManager\default\Update\ExcludeWUDriversInQualityUpdate" "value" "1"
Call :dword "HKLM\SOFTWARE\Microsoft\WindowsUpdate\UX\Settings" "ExcludeWUDriversInQualityUpdate" "1"
Call :dword "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate" "ExcludeWUDriversInQualityUpdate" "1"
Call :dword "HKLM\Software\Policies\Microsoft\Windows\DriverSearching" "SearchOrderConfig" "0"
:: -------------
:: Performans seçenekleri
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\VisualEffects" "VisualFXSetting" 3 & :: Performans seçeneklerini özel yapar
:: Pencerelerin içindeki kontrolleri ve öğeleri canlandırın
:: Menüleri soldurun veya görünüme kaydırın
:: Araç İpuçlarını soldurun veya görünüme kaydırın
:: Tıkladıktan sonra menü öğelerini karartın
:: Fare imlecinin altındaki gölgeleri göster
:: Pencerelerin altında gölgeleri göster
:: Açılan kutuları kaydırarak açın
:: Düzgün kaydırma liste kutuları 
Call :binary "HKCU\Control Panel\Desktop" "UserPreferencesMask" "9012038010000000"
Call :sz "HKEY_CURRENT_USER\Control Panel\Desktop\WindowMetrics" "MinAnimate" 0 & :: Küçültme ve büyütme sırasında pencereleri canlandırın 
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" "TaskbarAnimations" 0 & :: Görev çubuğu animasyonlarını devre dışı bırakır
Call :dword "HKCU\Software\Microsoft\Windows\DWM" "EnableAeroPeek" 0 & :: Peek kapat
Call :dword "HKCU\Software\Microsoft\Windows\DWM" "AlwaysHibernateThumbnails" 0 & :: Görev çubuğu küçük resim önizlemelerini kaydet 
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" "IconsOnly" 1 & :: Görev çubuğu küçük resim önizlemelerini kaydet, kapat
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" "ListviewAlphaSelect" 1 & :: Yarı saydam seçim dikdörtgenini göster 
Call :sz "HKCU\Control Panel\Desktop" "DragFullWindows" 0 & :: Sürüklerken pencere içeriğini göster 
Call :sz "HKCU\Control Panel\Desktop" "FontSmoothing" 2 & :: Ekran yazı tiplerinin pürüzsüz kenarları 
Call :dword "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" "ListviewShadow" 1 & :: Masaüstündeki simge etiketleri için alt gölgeler kullanın 
Call :binary "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer" "ShellState" "240000003E28000000000000000000000000000001000000130000000000000062000000"
:: -------------
Call :dword "HKLM\SYSTEM\CurrentControlSet\Services\GpuEnergyDrv" "Start" "4" & :: Gpu enerji tasarrufunu kapatır.
Call :dword "HKLM\SYSTEM\CurrentControlSet\Control\Power\PowerThrottling" "PowerThrottlingOff" "1" & :: Gpu enerji tasarrufunu kapatır.
Call :sz "HKCU\Control Panel\Accessibility\StickyKeys" "Flags" 506 & :: Yapışkan tuşları kapatır
Call :sz "HKCU\Control Panel\Accessibility\ToggleKeys" "Flags" "58" & :: Yapışkan tuşları kapatır
Call :sz "HKCU\Control Panel\Accessibility\Keyboard Response" "Flags" "122" & :: Filtre tuşlarını kapatır

