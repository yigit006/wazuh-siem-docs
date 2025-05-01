## ✍🏻 Proje Açıklaması

Bu proje, açık kaynaklı **Wazuh** SIEM (Security Information and Event Management) çözümünü sıfırdan kurup yapılandırarak hem Linux hem de Windows istemcilerden gerçek zamanlı güvenlik verisi toplamanıza, izlemenize ve analiz etmenize imkân tanıyan eksiksiz bir rehber sunar. Aşağıdaki aşamaları içerir:

1. **📦 Sanal Makine Kurulumu**  
   - VirtualBox üzerinde Ubuntu, Windows Server ve Kali Linux VM’lerinin hazırlanması  
   - Ağ ayarları (NAT, Köprü, Promiscuous Mode) ve statik IP konfigürasyonu  

2. **⚙️ Wazuh Manager & Agent Kurulumu**  
   - Ubuntu üzerinde Wazuh Manager, Indexer ve Dashboard bileşenlerinin tek komutla kurulumu  
   - Windows ve Linux agent’larının manager ile güvenli bağlantı kuracak şekilde yapılandırılması  

3. **👀 Güvenlik İzleme ve Saldırı Simülasyonu**  
   - SSH brute-force saldırı simülasyonu (Hydra)  
   - Wazuh logları ve uyarılarının CLI ve Dashboard üzerinden takibi  

4. **🧾 Dokümantasyon ve Hata Giderme**  
   - Karşılaşılabilecek yaygın sorunlar için çözümler  
   - Sanal makineler arası ping testleri, güvenlik duvarı ayarları notları  

### 🤔 Neden Bu Proje?

- **Adım Adım Kılavuz**: Yeni başlayanlar için bile anlaşılır, her adımı ekran görüntüleri ve komut satırı örnekleriyle desteklenmiş.  
- **Gerçek Dünyaya Yakın Simülasyon**: Saldırı ve tespit pratiği yaparak SIEM’in nasıl çalıştığını deneyimleme.  
- **Esnek ve Genişletilebilir**: Farklı ağ topolojileri veya ek güvenlik araçlarıyla entegre edilebilecek temel bir altyapı.

> Bu dokümanı takip ederek kendi test ortamınızı hızla kurabilir, Wazuh’un sunduğu gelişmiş tehdit izleme yeteneklerini keşfedebilir ve kendi ihtiyaçlarınıza göre özelleştirebilirsiniz.  


---


## ✍🏻 Project Description

This project provides a comprehensive guide to installing and configuring the open-source **Wazuh** SIEM solution from scratch, enabling you to collect, monitor, and analyze security data in real time from both Linux and Windows clients. It covers the following stages:

1. **📦 Virtual Machine Setup**  
   - Provision Ubuntu, Windows Server, and Kali Linux VMs in VirtualBox  
   - Network configuration (NAT, Bridged Adapter, Promiscuous Mode) and static IP assignment  

2. **⚙️ Wazuh Manager & Agent Installation**  
   - Install Wazuh Manager, Indexer, and Dashboard on Ubuntu with a single command  
   - Configure Windows and Linux agents to connect securely to the manager  

3. **👀 Security Monitoring & Attack Simulation**  
   - Simulate SSH brute-force attacks using Hydra  
   - Track Wazuh logs and alerts via CLI and the Dashboard  

4. **🧾 Documentation & Troubleshooting**  
   - Solutions for common issues and error messages  
   - Notes on inter-VM ping tests, firewall adjustments, and best practices  

### 🤔 Why This Project?

- **Step-by-Step Guide**: Clear, beginner-friendly instructions backed by screenshots and command-line examples.  
- **Realistic Simulation**: Hands-on practice with attack and detection cycles to experience how a SIEM operates in real environments.  
- **Flexible & Extensible**: A solid foundation you can extend with different network topologies or additional security tools.  

> By following this guide, you’ll quickly build your own test environment, explore Wazuh’s advanced threat-monitoring capabilities, and tailor it to your specific needs.  



---

<details>
<summary>🇹🇷 Türkçe Dökümantasyon</summary>

### 📦 VirtualBox Kurulumu ve Temel Kullanımı


Bu belgede, VirtualBox programının nasıl indirileceğinizi, kurulacağınızı ve temel arayüz kullanımını açıklamaya çalıştım. Bu bilgiler, Wazuh tabanlı SIEM ortamı için sanal makineleri oluştururken size yardımcı olacaktır.

---

## 📥 1. VirtualBox İndirme

VirtualBox'u resmi sitesinden indirin:

🔗 [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

İşletim sisteminize uygun olan sürümü seçin:
- Windows Hosts
- macOS Hosts
- Linux Distributions

---

## ⚙️ 2. Kurulum Adımları

**Windows için:**

1. `.exe` dosyasını indirin ve çift tıklayarak çalıştırın.
2. "Next" butonuna tıklayarak adımları takip edin.
3. Ağ bileşenlerini yüklemek için gelen uyarıya "Evet" deyin.
4. "Install" ile kurulumu tamamlayın.
5. Kurulum sonrası VirtualBox'ı başlatın.

---

## 🖥️ 3. Temel Arayüz Kullanımı

VirtualBox arayüzü oldukça basit ve kullanımı kolaydır:

### ➕ Yeni Makine Oluşturma

1. `Yeni` butonuna tıklayın.
2. Makine adını yazın (örnek: `Wazuh-Manager`).
3. İşletim sistemini ve versiyonunu seçin (örnek: Ubuntu 64-bit).
4. RAM miktarını belirleyin (örnek: 2048 MB).
5. Sanal disk oluşturun ve önerilen ayarlarla devam edin.

### ⚙️ Ayarlar

Oluşturduğunuz sanal makineye sağ tıklayıp `Ayarlar` seçeneğine girerek:

- **Sistem:** RAM, işlemci sayısı
- **Ağ:** Bağlantı türü (örneğin, Internal Network)
- **Depolama:** ISO dosyası bağlama
- **Görüntü:** Ekran bellek miktarı

ayarlarını yapabilirsiniz.

### ▶️ Makineyi Başlatma

Hazır olan makineyi seçip `Başlat` butonuna basarak çalıştırabilirsiniz.

---

## ✅ Özet

- VirtualBox, sanal makineler oluşturmak için kullanılır.
- Arayüzü basittir: Yeni makine ekleme, ayar yapma ve başlatma işlemleri birkaç tıklama ile gerçekleşir.
- ISO dosyaları kurulum sırasında bağlanabilir.

---

Bu adımlar tamamlandıktan sonra, Ubuntu Sanal Makine Kurulumu ve Ağ Yapılandırması'na (VirtualBox) geçebilirsiniz.



---




---


---

### 🐧 Ubuntu Sanal Makine Kurulumu ve Ağ Yapılandırması (VirtualBox)


Bu dokümanda, VirtualBox kullanarak Ubuntu işletim sistemi kurulumunun nasıl yapacağınızı ve ağ ayarlarının nasıl yapılandırılacağınızı açıklamaya çalıştım.

---

## 📥 1. Ubuntu ISO Dosyasını İndirme

Ubuntu Server ya da Desktop sürümünü aşağıdaki bağlantıdan indirebilirsiniz:

🔗 [https://ubuntu.com/download](https://ubuntu.com/download)

SIEM projeleri için **Ubuntu Server LTS** sürümünü öneriyorum.

---

## 🖥️ 2. ISO Dosyasını VirtualBox'a Ekleme

1. VirtualBox'ı açın ve "Yeni" butonuna tıklayın.
2. Makine ismi: `Ubuntu-SIEM`
3. Tip: `Linux`, Versiyon: `Ubuntu (64-bit)`
4. Bellek (RAM): Minimum **2048 MB**, tercihen **4096 MB**
5. Sanal sabit disk oluşturun (VDI, dinamik tahsisli, minimum 20 GB)
6. Makineyi oluşturduktan sonra:
   - Sağ tıklayıp **Ayarlar > Depolama** sekmesine gidin.
   - "Denetleyici: IDE" altında **Boş** seçeneğini seçin.
   - Sağda CD simgesine tıklayıp, **Ubuntu ISO dosyasını** seçin.

---

## 🌐 3. Ağ Ayarlarını Yapılandırma

### 🧱 Bağlantı Türü: NAT Network ve Köprü Bağdaştırıcısı

#### 🔹 NAT Network
- VirtualBox'ın yerel ağ erişimi sağlar.
- İnternet erişimi sağlar.
- Diğer sanal makinelerle aynı NAT ağına bağlanır.
- **Avantajı**: Dış dünya ile sınırlı ama internet bağlantısı var.

#### 🔹 Köprü Bağdaştırıcısı 
- Sanal makine fiziksel ağ kartını doğrudan kullanır.
- Gerçek ağdaki diğer cihazlarla aynı düzeyde iletişim kurabilir.
- **Avantajı**: Gerçek bir makine gibi davranır. Diğer fiziksel cihazlarla haberleşebilir.

> 🔄 Projede bazı makineleri NAT Network, bazılarını Bridged Adapter ile yapılandırmak gerekebilir. Wazuh Manager dış dünya ile konuşacaksa Bridged Adapter tercih edebilirsiniz.

---

## 🔐 Karma Tipi: "Tümü" ve "VM'lere izin ver" Seçenekleri

- **Karma Tipi (Promiscuous Mode):**  
  Varsayılan olarak "Yoktur". Ancak log trafiğini veya saldırı simülasyonunu dinlemek isterseniz:
  
  - Ayar: **Tümü (Allow All)**  
    → Bu, VM'nin kendi dışındaki trafiği de dinlemesine izin verir.

- **"VM'lere izin ver (Allow VMs)" Seçeneği:**  
  - Sanal makinelerin birbirleriyle haberleşmesine izin verir.
  - Özellikle **Internal Network** veya **Host-only** gibi yapılar kullanıldığında **gerekli** hale gelir.

---

## ✅ Kurulumdan Sonra

- ISO ile başlatılan makinede Ubuntu kurulumu ekranı gelecektir.
- Kurulumu yaptıktan sonra ISO'yu çıkarın.


---

Bu adımlar tamamlandığınızda Ubuntu sisteminiz sanal ortamda çalışmaya hazır olacaktır.



---




---


---

### 🪟 Windows Server 2019 Sanal Makine Kurulumu


Bu dokümanda, VirtualBox kullanarak Windows Server 2019 kurulumunun nasıl yapacağınızı ve temel ağ ayarlarının nasıl yapılandıracağınızı adım adım açıklamaya çalıştım.

---

## 📥 1. ISO Dosyasını İndirme

Windows Server 2019 ISO dosyasını Microsoft'un resmi sayfasından veya MSDN üyeliğiniz aracılığıyla edinebilirsiniz.

🔗 [https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019)

---

## 🖥️ 2. VirtualBox'ta Yeni Makine Oluşturma

1. VirtualBox'ı açın ve "Yeni" butonuna tıklayın.
2. Makine Adı: `WinServer2019`
3. Tip: `Microsoft Windows`, Versiyon: `Windows Server 2019 (64-bit)`
4. Bellek (RAM): Minimum **4096 MB** önerilir
5. Sanal sabit disk oluşturun (VDI, dinamik tahsisli, en az 40 GB)

---

## 💿 3. ISO Dosyasını Ekleme

1. Makineyi oluşturduktan sonra sağ tıklayıp **Ayarlar > Depolama** sekmesine girin.
2. "Denetleyici: IDE" altında "Boş" seçeneğine tıklayın.
3. Sağdaki CD simgesinden **Windows Server 2019 ISO dosyasını** seçin.

---

## 🌐 4. Ağ Ayarları

- Makine ayarlarından **Ağ > Bağlantı Türü** kısmına gelin.
- **Bağlantı Türü olarak NAT Network veya Köprü Bağdaştırıcısı (Bridged Adapter)** seçin.
- Gerekirse "Gelişmiş" bölümünden **Karma Tipi → VM'lere izin ver (Allow VMs)** seçeneğini aktif hale getirin.(Karma Tipi'ni neye göre seçeceğiniz Ubuntu Sanal Makine Kurulumu kısmında açıklamaya çalıştım.)

---

## ⚙️ 5. Kurulum ve Etkinleştirme

1. Makineyi başlatın ve ISO'dan boot edilmesini sağlayın.
2. Windows Server kurulum ekranı açılacaktır.
3. Ürün anahtarını girin ya da deneme sürümü olarak ilerleyin.
4. Sistem kurulumunu tamamlayın.

---

## ✅ Kurulumdan Sonra

- Guest Additions yüklemeyi unutmayın (ek sürücü ve entegrasyonlar için).
- Ağ bağlantısını test edin (ping, internet erişimi vs.)
- Gerekirse statik IP ataması yaparak sonraki adımlara geçebilirsiniz.(Bu projede statik IP ataması yapmayı tercih ettim.)

---

Bu adımlar tamamlandığında Windows Server sisteminiz sanal ortamda çalışmaya hazır olacaktır.



---




---


---

### 🐍 Kali Linux Sanal Makine Kurulumu


Bu dokümanda, VirtualBox kullanarak Kali Linux işletim sisteminin kurulumu ve temel ağ ayarlarının yapılandırılmasını adım adım açıklamaya çalıştım.

---

## 📥 1. Kali ISO Dosyasını İndirme

Kali Linux ISO dosyasını resmi sitesinden indirin:

🔗 [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)

> **Not:** "Installer" seçeneği üzerinden indirmenizi tavsiye ederim. Live versiyon değil!

---

## 🖥️ 2. VirtualBox'ta Yeni Makine Oluşturma

1. VirtualBox'ı açın ve "Yeni" butonuna tıklayın.
2. Makine Adı: `Kali-Linux`
3. Tip: `Linux`, Versiyon: `Debian (64-bit)`
4. Bellek (RAM): Minimum **2048 MB**, tercihen **4096 MB**
5. Sanal disk oluşturun: VDI, Dinamik, en az 20 GB

---

## 💿 3. ISO Dosyasını Ekleme

1. Makineyi oluşturduktan sonra:
   - Sağ tıklayıp **Ayarlar > Depolama** sekmesine girin.
   - "Boş" seçeneğine tıklayın ve sağdaki CD simgesinden Kali ISO'yu seçin.
2. ISO bağlandıktan sonra `Başlat` diyerek kuruluma geçebilirsiniz.

---

## 💬 4. Türkçe Klavye ve Dil Desteği

> **Not:** Kurulumdan sonra terminalde Türkçe karakter (ç, ı, ş...) kullanmak istiyorsanız, şu adımları takip edin:


**Applications > Session and Startup > Application Autostart > add** 

Name: keyword tr
Command:
```bash
setxkbmap tr
```
Trigger: on login

Bu komut, Türkçe Q klavye düzenini etkinleştirir.

---

## 🌐 5. Ağ Ayarları

- Makine ayarlarından **Ağ > Bağlantı Türü** kısmına gelin.
- **Bağlantı Türü olarak NAT Network veya Köprü Bağdaştırıcısı (Bridged Adapter)** seçin.
- Gerekirse "Gelişmiş" bölümünden **Karma Tipi → VM'lere izin ver (Allow VMs)** seçeneğini aktif hale getirin.(Karma Tipi'ni neye göre seçeceğiniz Ubuntu Sanal Makine Kurulumu kısmında açıklamaya çalıştım.)

---

## ✅ Kurulumdan Sonra

- root ya da kali kullanıcısıyla oturum açın.
- Terminal üzerinden `ip a`, `ping` gibi komutlarla ağ bağlantısını test edin.
- Gerekirse statik IP ataması yaparak sonraki adımlara geçebilirsiniz.(Bu projede statik IP ataması yapmayı tercih ettim.)

---

Bu adım tamamlandığınızda Kali Linux, Agent ya da Saldırı makinesi olarak kullanmanız için hazır hale gelir.



---




---


---

### 🌐 Ubuntu Statik IP Adresi Ayarlama (Netplan)


Bu dokümanda, Ubuntu sistemlerde `netplan` aracı ile statik IP adresinin nasıl atanacağı adım adım açıklamaya çalıştım.

---

## 🧰 Gereksinimler

- Ubuntu 18.04 ve sonrası (Netplan varsayılan olarak gelir)
- Root yetkisine sahip kullanıcı

---

## 🔍 1. Ağ Arayüzünü Öğrenin

Terminali açın ve mevcut ağ arayüzünüzü görüntüleyin:

```bash
ip link show
```

Genellikle `enp0s3`, `ens33` veya `eth0` gibi bir isimle görünür.

---

## 📝 2. Netplan Yapılandırmasını Düzenleme

Aşağıdaki komutla yapılandırma dosyasını açın:

```bash
sudo nano /etc/netplan/00-installer-config.yaml
```

İçeriği örneğe göre düzenleyin:

```yaml
network:
  version: 2
  ethernets:
    enp0s3:
      dhcp4: no
      addresses: [192.168.100.10/24]
      gateway4: 192.168.100.1
      nameservers:
        addresses: [8.8.8.8, 1.1.1.1]
```

> ❗ `enp0s3` kısmını kendi ağ arayüz isminizle değiştirin.

---

## 💾 3. Ayarları Uygulama

Değişiklikleri kaydedip kapattıktan sonra aşağıdaki komutu çalıştırın:

```bash
sudo netplan apply
```

Ağ ayarlarının etkinleştiğini doğrulamak için:

```bash
ip a
```

---

## 🧪 4. Bağlantı Testi

Bağlantıyı test etmek için:

```bash
ping 8.8.8.8 -c 4
```

veya

```bash
ping google.com -c 4
```

---

## ✅ Özet

- Netplan dosyası ile manuel IP yapılandırması yapılır.
- DHCP kapatılır, IP – ağ geçidi – DNS sunucuları elle girilir.
- Bu yapılandırma, özellikle sanal ağ ortamlarında sabit iletişim için kritik önemdedir.

---

Bu adımı tamamladıktan sonra makineniz sabit bir IP ile ağda tanımlanabilir hale gelir.



---




---


---

### �� Windows Server 2019 Statik IP Adresi Ayarlama


Bu dokümanda, Windows Server 2019 sisteminde statik IP adresinin nasıl atanacağı adım adım açıklamaya çalıştım.

---

## 🎯 Amaç

Dinamik IP (DHCP) yerine sabit bir IP adresi tanımlayarak sanal makinenin ağda her zaman aynı IP ile tanınmasını sağlamak.

---

## 🧭 1. Ağ Ayarlarına Erişim

1. Görev çubuğundaki ağ simgesine sağ tıklayın ve **"Network and Sharing Center"** seçeneğine tıklayın.
2. Açılan pencerede **"Change adapter settings"** bölümüne girin.
3. Kullanılan ağ adaptörüne (örneğin: `Ethernet`) sağ tıklayıp **"Properties"** seçin.

---

## 🌐 2. IPv4 Ayarlarını Düzenleme

1. Açılan listede **"Internet Protocol Version 4 (TCP/IPv4)"** seçeneğini bulun ve çift tıklayın.
2. "Aşağıdaki IP adresini kullan" (Use the following IP address) seçeneğini işaretleyin.
3. Gerekli alanları doldurun:

| Alan               | Örnek Değer            |
|--------------------|------------------------|
| IP address         | 192.168.100.20         |
| Subnet mask        | 255.255.255.0          |
| Default gateway    | 192.168.100.1          |
| Preferred DNS      | 8.8.8.8                |
| Alternate DNS      | 1.1.1.1                |

4. "OK" tuşlarına basarak pencereleri kapatın.

---

## 🧪 3. Yapılandırmayı Test Etme

CMD'yi açarak aşağıdaki komutlarla IP ve bağlantıyı test edebilirsiniz:

```cmd
ipconfig
ping 8.8.8.8
```

---

## ✅ Özet

- Statik IP, özellikle SIEM ve ağ güvenliği projelerinde makinelerin sabit bir adresle çalışması için önemlidir.
- Ayarlar manuel girildiğinde kalıcı olur, DHCP'den etkilenmez.
- DNS ayarlarını girerek internet erişimi de sağlanabilir.

---

Bu adımları tamamladığınızda Windows sunucunuz sabit bir IP ile ağa dahil olmuş olacaktır.



---




---


---

### 🌐 Kali Linux Statik IP Adresi Ayarlama


Bu dokümanda, Kali Linux sistemine statik (sabit) IP adresinin nasıl atanacağınızı adım adım açıklamaya çalıştım.

---

## 🎯 Amaç

- Kali sisteminin her açılışta aynı IP adresini almasını sağlamak
- Ağ üzerinde güvenli ve tutarlı iletişim kurmak

---

## 🧭 1. Ağ Arayüz Adını Öğrenme

Terminalde aşağıdaki komutu çalıştırın:

```bash
ip a
```

Genellikle arayüz ismi `eth0`, `enp0s3` veya `ens33` şeklindedir.

---

## 📝 2. Ağ Yapılandırma Dosyasını Düzenleme

Aşağıdaki komutla ağ yapılandırma dosyasını açın:

```bash
sudo nano /etc/network/interfaces
```

Dosya içeriğini aşağıdaki örneğe göre düzenleyin:

```bash
auto eth0
iface eth0 inet static
    address 192.168.100.30
    netmask 255.255.255.0
    gateway 192.168.100.1
    dns-nameservers 8.8.8.8 1.1.1.1
```

> ❗ `eth0` yerine kendi ağ arayüzünüzün ismini yazın.

---

## 🔄 3. Ağ Servisini Yeniden Başlatma

```bash
sudo systemctl restart networking
```

Ya da aşağıdaki alternatif komutu kullanabilirsiniz:

```bash
sudo ifdown eth0 && sudo ifup eth0
```

---

## 🧪 4. Bağlantı Kontrolü

IP adresini ve bağlantıyı doğrulamak için:

```bash
ip a
ping 8.8.8.8 -c 4
```

---

## ✅ Özet

- Kali'de statik IP ayarı genellikle `/etc/network/interfaces` dosyasından yapılır.
- Ağ hizmeti yeniden başlatıldığında yapılandırma aktif olur.
- Bu ayar sanal makineler arası güvenli bağlantı kurmak için önemlidir.

---

Bu işlemleri tamamladıktan sonra Kali Linux sisteminiz sabit IP ile çalışmaya hazır hale gelir.



---




---


---

### 🔁 Sanal Makineler Arası Ping Testi ve Sorun Giderme


Bu dokümanda Kali, Ubuntu ve Windows sanal makineleri arasında `ping` komutu ile bağlantı testini nasıl yapacağınız ve bu işlemi engelleyebilecek durumları nasıl çözebileceğinizi açıklamaya çalıştım.

---

## 🎯 Amaç

- Sanal makinelerin aynı ağda olup olmadığını doğrulamak
- Her makinenin diğerine ICMP (ping) isteği gönderebildiğini test etmek
- Ağ yapılandırmasının başarılı olduğunu kontrol etmek

---

## ✅ 1. Temel Ping Denemeleri

Her makineden diğerlerine ping atmayı deneyin:

### Windows → Kali

```cmd
ping 192.168.100.30
```

### Kali → Windows

```bash
ping 192.168.100.20
```

### Ubuntu → Kali

```bash
ping 192.168.100.30
```
### Kali → Ubuntu

```bash
ping 192.168.100.10
```

### Windows → Ubuntu

```cmd
ping 192.168.100.10
```

### Ubuntu → Windows

```bash
ping 192.168.100.20
```

---

## ⚠️ 2. Ping Başarısız Olursa – Olası Engelleyiciler

### 🛡️ Windows Güvenlik Duvarı

Windows sistemlerde ICMP istekleri (ping) güvenlik duvarı tarafından **varsayılan olarak engellenir**.

#### 🔧 Çözüm:

1. `Windows Defender Firewall` > `Advanced Settings` açılır.
2. Sol menüden **Inbound Rules** → sağda **File and Printer Sharing (Echo Request - ICMPv4-In)** bulun.
3. Sağ tıklayıp **Enable Rule** deyin (Private ve Domain profilleri için etkinleştirin).

---

### 🔥 Kali Linux Güvenlik Duvarı (iptables / nftables)

Kali'de gelen ICMP istekleri bazen iptables ya da nftables kuralları tarafından engellenebilir.

#### 🔧 Çözüm:

```bash
sudo iptables -A INPUT -p icmp --icmp-type echo-request -j ACCEPT
```

veya nftables için:

```bash
sudo nft add rule inet filter input icmp type echo-request accept
```

Not: Kalıcı yapmak isterseniz `iptables-persistent` veya `nftables.conf` dosyaları düzenlenmelidir.

---

### 🔌 Ağ Kartı Sorunu

Makinenin ağ adaptörü "Disconnected" olabilir.

#### 🔧 Çözüm:

- VirtualBox > Ayarlar > Ağ > **Bağlantı türü: Internal Network / Bridged** olduğundan emin olun.
- Aynı ağ adını (örneğin `SIEMnet`) tüm makinelerde kullanın.

---

### 🧩 Farklı Alt Ağlar

Statik IP'ler farklı ağ bloğundaysa (örneğin biri `192.168.100.x`, diğeri `192.168.1.x`) ping başarısız olur.

#### 🔧 Çözüm:

- Tüm makinelerin IP'lerini aynı subnet bloğunda ayarlayın (örneğin `192.168.100.10`, `.20`, `.30`)
- Subnet maskesi tüm sistemlerde `255.255.255.0` olmalı

---

## 🧪 Doğrulama

Her makineden diğerlerine tekrar `ping` komutları gönderin ve bağlantıyı test edin. 4 paket cevabı alınması bağlantının sağlıklı olduğunu gösterir.

---

## ✅ Özet

| Sorun Nedeni                | Çözüm                             |
|-----------------------------|------------------------------------|
| Windows ICMP engeli         | Güvenlik duvarı kuralı etkinleştirme |
| Kali ICMP engeli            | `iptables` veya `nftables` kuralı ekleme |
| Ağ ayarı eksikliği          | VirtualBox iç ağ/bridge kontrolü   |
| Alt ağ uyuşmazlığı          | IP/Subnet kontrolü                 |

---

Bu adımları tamamladıktan sonra makineleriniz arasında sorunsuz bir şekilde ping testi yapabilirsiniz.



---




---


---

### 🛡️ Wazuh Manager Kurulumu (Ubuntu)


Bu dokümanda, Ubuntu sunucusu üzerinde Wazuh Manager bileşenini nasıl kuracağınızı ve Windows/Linux istemcilerden bağlantı sağlamak için gerekli olan **agent key**'i nasıl oluşturacağınızı adım adım açıklamaya çalıştım.

---

## 🎯 Amaç

- Wazuh SIEM altyapısını başlatmak için Ubuntu sistemine Wazuh Manager kurmak
- Wazuh bileşenlerini tek komutla yüklemek
- Windows veya Linux agent'ların bağlantısı için gerekli olan `Agent Key`'i üretmek

---

## 🧰 Gereksinimler

- Ubuntu 20.04 LTS veya 22.04 LTS 
- En az 2 vCPU, 4 GB RAM
- root veya sudo yetkisi olan kullanıcı
- Statik IP yapılandırılmış olmalı

---

## 🔧 1. Sistem Güncelleme ve Temel Paketler

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl gnupg -y
```

**Neden bu paketler gerekli?**

- `curl`: Kurulum betiğini Wazuh'un sunucusundan indirmek için kullanılır.
- `gnupg`: Paketlerin dijital imzalarını doğrulamak için kullanılır.

---

## 📦 2. Wazuh Kurulum Betiğinin İndirilmesi ve Çalıştırılması

```bash
curl -sO https://packages.wazuh.com/4.8/wazuh-install.sh
chmod +x wazuh-install.sh
sudo bash ./wazuh-install.sh -a
```

Bu script sayesinde:
- Wazuh Manager
- Wazuh Indexer 
- Wazuh Dashboard

tek komutla kurulmuş olur.

---

## 🔍 3. Kurulum Sonrası Servislerin Kontrolü

```bash
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-dashboard
sudo systemctl status wazuh-indexer
```

---

## 🌐 4. Dashboard'a Erişim

Tarayıcınızdan şu adrese gidin:

```
https://<sunucu-ip>:5601
```

Varsayılan kullanıcı: `admin`  
Şifre: Terminalde kurulum tamamlandıktan sonra verilir.

> SSL uyarısını tarayıcıda "Gelişmiş > Devam et" diyerek geçebilirsiniz.

---

## 🔐 5. Agent Key Oluşturma

Agent'ların (Linux veya Windows) Wazuh Manager'a bağlanabilmesi için her birine özel bir **anahtar (key)** oluşturulması gerekir.

### Anahtar oluşturma aracı:

```bash
sudo /var/ossec/bin/manage_agents
```

### Menüde:

- `A` → Yeni agent eklemek için
- `E` → Anahtar oluşturmak için
- Anahtar (key) oluşturulur ve ekranda gösterilir

> ⚠️ **Bu key'i bir yere kaydedin.**
> Bu key, agent kurulumunda kullanılacaktır.

---

## 🧾 Notlar

- Her agent için ayrı bir key oluşturulmalıdır.
- `manage_agents` aracı sadece Wazuh Manager üzerinde çalıştırılır.
- Anahtarlar, agent'ın kimlik doğrulaması için zorunludur.

---

Bu aşamadan sonra ilgili istemcilerde Wazuh Agent kurulumu yapılarak bu key ile sunucuya bağlamanız sağlanabilir.



---




---


---

### 🪟 Wazuh Agent Kurulumu


Bu dokümanda, bir Windows sistem üzerinde Wazuh Agent kurulumunu nasıl yapacağınızı ve Wazuh Manager ile bağlantı kurmak için gerekli bilgileri nasıl girebileceğinizi açıklamaya çalıştım.

---

## 🎯 Amaç

- Windows sistemde Wazuh Agent'ı kurmak
- Daha önce Wazuh Manager üzerinde oluşturulmuş olan agent anahtarı ile bağlantıyı sağlamak

---

## 🧰 Gereksinimler

- Kurulmuş ve çalışan bir **Wazuh Manager**
- Önceden oluşturulmuş bir **agent key** 
- Windows 10 / 11 / Server 2016+ sistem

---

## 📦 1. Wazuh Agent Kurulum Dosyasını İndirme

🔗 En güncel Wazuh Agent MSI dosyasını indir:

[https://packages.wazuh.com/4.x/windows/wazuh-agent-4.x.x.msi](https://packages.wazuh.com/4.x/windows/wazuh-agent-4.x.x.msi)

---

## 💿 2. Kurulum Sihirbazı

Kurulum sırasında şu adımları takip ediniz:

- **Manager IP Address** alanına Wazuh Manager'ın IP adresini gir (örnek: `192.168.100.10`)
- **Authentication key** alanına, `manage_agents` aracıyla daha önce oluşturduğun key'i yapıştır
- Kurulumu tamamla ve **Save** butonuna bas


> GUI üzerinden IP ve key bilgilerini doğrudan girerek hızlı yapılandırma yapabilirsiniz.

---

## ▶️ 3. Servisi Başlatma

Kurulumdan sonra servis otomatik başlamazsa CMD'de şu komutu çalıştır:

```cmd
sc start wazuh-agent
```

veya Windows > Hizmetler (Services) menüsünden `Wazuh Agent` servisini manuel başlat.

---

## ✅ Doğrulama

Wazuh Manager üzerinde agent bağlantısını şu komutla doğrula:

```bash
sudo /var/ossec/bin/agent_control -l
```

Wazuh Dashboard > Agents sekmesinde Windows sistemin "Active" olarak görünmelidir.

---

## 📌 Notlar

- Agent key sadece GUI ekranına yapıştırılarak da girilebilir.
- Eğer bağlantı sağlanamıyorsa, Windows güvenlik duvarı ayarlarında 1514 ve 1515 TCP portlarının açık olduğundan emin olun.

---

Bu adımları tamamladıktan sonra Windows sistem SIEM ortamına başarıyla entegre olur.



---




---


---

### 🔐 SSH Brute-Force Saldırı Simülasyonu ve Wazuh Log İzleme


Bu doküman, Kali Linux üzerinden Wazuh Manager'ın kurulu olduğu Ubuntu sistemine karşı yapılan bir **brute-force parola denemesi saldırısı** simülasyonunu ve bu saldırının Wazuh tarafından nasıl izlendiğini adım adım açıklar.

---

## 🎯 Amaç

- `hydra` aracıyla Ubuntu'daki SSH servisine karşı parola denemesi yapmak
- Bu saldırının Wazuh tarafından algılanıp log'lara yansıdığını doğrulamak
- SIEM ortamında basit saldırı izleme pratiği kazanmak

---

## 🧰 Gereksinimler

- Wazuh Manager Ubuntu sistemine kurulu ve aktif olmalı
- SSH servisi Ubuntu sistemde çalışıyor olmalı
- Kali Linux sistemi, Ubuntu'ya ping atabiliyor olmalı
- Kali üzerinde `hydra` aracı kurulu olmalı

```bash
sudo apt install hydra -y
```

---

## 📄 1. Şifre Listesini Hazırlama

Kali sisteminde basit bir şifre listesi oluşturun:

```bash
nano Sifreler.txt
```

İçerik örneği:

```
123456
admin
root
password
toor
```

Kaydedip çıkın.

---

## 🧪 2. Brute-Force Saldırısını Başlatma

Kali terminalinden şu komutu çalıştırın:

```bash
hydra -l admin -P Sifreler.txt ssh://192.168.100.10
```

- `-l admin`: Denenecek kullanıcı adı
- `-P Sifreler.txt`: Denenecek şifrelerin bulunduğu dosya
- `ssh://<ip>`: Hedef sistemin IP adresi ve protokol

> 🔥 Bu saldırı Ubuntu'da başarısız giriş denemeleri oluşturur ve Wazuh tarafından tespit edilir.

---

## 👁️ 3. Ubuntu Sisteminde Wazuh Loglarını İzleme

Wazuh Manager (Ubuntu) sisteminde şu komutla canlı log takibi yapılabilir:

```bash
sudo tail -f /var/ossec/logs/alerts/alerts.json
```

Alternatif olarak Kibana Dashboard > Security Events sekmesinden de saldırı logları incelenebilir.

---

## ✅ Gözlemlenebilecek Log Örnekleri

- "Failed password for admin" from the **sshd** service
- Wazuh alarmı: `"Authentication failure"` veya `"Multiple failed login attempts"`

---

## 🧾 Notlar

- Hydra saldırısı kısa sürede çok sayıda parola denemesi yaptığı için, log dosyasında yoğunluk oluşabilir.
- Ubuntu üzerinde SSH servisi açık değilse, aşağıdaki komutla kurabilirsiniz:

```bash
sudo apt install openssh-server -y
sudo systemctl enable ssh
sudo systemctl start ssh
```

---

Bu simülasyon, gerçek saldırıların izini sürmek ve Wazuh'un nasıl tepki verdiğini gözlemlemek için değerli bir alıştırmadır.



---




---


---

### 🧾 Proje Özeti ve Genel Değerlendirme


Bu proje kapsamında açık kaynaklı SIEM çözümü olan **Wazuh** kullanılarak Linux ve Windows istemcileri izleyebilen bir güvenlik gözlem altyapısı kuruldu. Hem teknik kurulum hem de saldırı simülasyonlarıyla sistemin nasıl çalıştığı uygulamalı olarak gösterildi.

---

## 🧱 Projeyi Neler Oluşturdu?

- Ubuntu sistemine Wazuh Manager kurulumu
- Linux ve Windows sistemlere Wazuh Agent kurulumu
- Manager-Agent bağlantı konfigürasyonları
- Hydra ile brute-force saldırı simülasyonu
- Wazuh loglarının CLI ve dashboard üzerinden analizi

---

## 🎯 Hedeflere Ulaşıldı mı?

✅ Wazuh ortamı başarıyla kuruldu  
✅ Gerçek zamanlı log izleme sağlandı  
✅ Basit saldırılar tespit edildi  
✅ Windows ve Linux istemcilerden loglar toplandı  

---

## 🔍 Deneyimleyenler İçin Tavsiyeler

Bu projeyi uygulayan kullanıcıların bazı noktalarda farklı sistem yapılarına, ağ ayarlarına ya da yazılım sürümlerine bağlı olarak hatalarla karşılaşması mümkündür. Bu çok normaldir.

> 💡 **Unutma:** Gerçek öğrenme genellikle hata yaptığında başlar.

Karşılaşabileceğin olası problemler:

- Bağlantı sorunları (ping, port açık mı?)
- Güvenlik duvarı (Windows UFW/NFTables)
- SSH erişim sorunları
- Dashboard'a bağlantı kurulamaması

Bu gibi durumlarda:

- Hatanın tam çıktısını analiz et
- Wazuh dokümantasyonunu incele → [https://documentation.wazuh.com/](https://documentation.wazuh.com/)
- StackOverflow, Wazuh forumları ve GitHub Issues bölümlerinden benzer hataları ara
- Ve tabii ki: Deneme-yanılma yoluyla çözüm üret!

---

## 🧡 Kapanış Notu

Umarım bu proje sayesinde sadece Wazuh değil, genel olarak SIEM sistemleri hakkında da fikir edinmişsindir.

Eğer sorunsuz ilerlediysen ne mutlu! Eğer birkaç hata ile karşılaştıysan, o da çok güzel — çünkü öğrendin. 🙂

Bu projeyi denediğin için teşekkür ederim. Umarım sende yeni bir merak uyandırmıştır. 🚀

---

İyi çalışmalar ve logların hep okunabilir olması dileğiyle!


---

### 🇬🇧 English Documentation



---




---


</details>

---

<details>
<summary>🇬🇧 English Documentation</summary>

### 📦 VirtualBox Installation and Basic Usage

In this document, I explain how to download, install, and use the basic interface of VirtualBox. This information will help you when creating virtual machines for a Wazuh-based SIEM environment.

---

## 📥 1. Download VirtualBox

Download VirtualBox from the official website:

🔗 [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

Choose the version suitable for your operating system:
- Windows Hosts
- macOS Hosts
- Linux Distributions

---

## ⚙️ 2. Installation Steps

**For Windows:**

1. Download the `.exe` file and double-click to run.
2. Follow the steps by clicking "Next".
3. Accept the prompt to install network components.
4. Complete the installation by clicking "Install".
5. After installation, start VirtualBox.

---

## 🖥️ 3. Basic Interface Usage

The VirtualBox interface is quite simple and easy to use:

### ➕ Creating a New Machine

1. Click the `New` button.
2. Enter the machine name (example: `Wazuh-Manager`).
3. Choose the operating system and version (example: Ubuntu 64-bit).
4. Specify the amount of RAM (example: 2048 MB).
5. Create a virtual disk and proceed with the recommended settings.

### ⚙️ Settings

Right-click the created virtual machine and go to `Settings`:

- **System:** RAM, number of processors
- **Network:** Connection type (e.g., Internal Network)
- **Storage:** Attach ISO file
- **Display:** Screen memory amount

### ▶️ Starting the Machine

Select the machine that is ready and click the `Start` button to run it.

---

## ✅ Summary

- VirtualBox is used to create virtual machines.
- The interface is simple: adding a new machine, setting it up, and starting it are done with a few clicks.
- ISO files can be attached during installation.

---

After completing these steps, you can proceed to the Ubuntu Virtual Machine Setup and Network Configuration (VirtualBox).



---


---

### 🐧 Ubuntu Virtual Machine Installation and Network Configuration (VirtualBox)

This document explains step-by-step how to install the Ubuntu operating system using VirtualBox and configure the network settings.

---

## 📥 1. Download the Ubuntu ISO File

You can download the Ubuntu Server or Desktop version from the following link:

🔗 [https://ubuntu.com/download](https://ubuntu.com/download)

I recommend **Ubuntu Server LTS** version for SIEM projects.

---

## 🖥️ 2. Add the ISO File to VirtualBox

1. Open VirtualBox and click the `New` button.
2. Machine name: `Ubuntu-SIEM`
3. Type: `Linux`, Version: `Ubuntu (64-bit)`
4. Memory (RAM): Minimum **2048 MB**, preferably **4096 MB**
5. Create a virtual hard disk (VDI, dynamically allocated, minimum 20 GB)
6. After creating the machine:
   - Right-click and go to **Settings > Storage** tab.
   - Under "Controller: IDE", select **Empty**.
   - Click the CD icon on the right and choose the **Ubuntu ISO file**.

---

## 🌐 3. Configure Network Settings

### 🧱 Connection Type: NAT Network and Bridged Adapter

#### 🔹 NAT Network
- Provides local network access for VirtualBox.
- Provides internet access.
- Connects to the same NAT network as other virtual machines.
- **Advantage**: Limited to the outside world but has internet access.

#### 🔹 Bridged Adapter
- The virtual machine uses the physical network card directly.
- Can communicate with other devices on the real network.
- **Advantage**: Acts like a real machine. Can communicate with other physical devices.

> 🔄 Some machines in the project may need to be configured with NAT Network, while others may require Bridged Adapter. You can prefer Bridged Adapter if the Wazuh Manager needs to communicate with the outside world.

---

## 🔐 Promiscuous Mode: "Allow All" and "Allow VMs" Options

- **Promiscuous Mode:**  
  By default, it's "None". However, if you want to listen to log traffic or simulate attacks:

  - Setting: **Allow All**  
    → This allows the VM to listen to traffic outside its own.

- **Allow VMs Option:**  
  - Allows virtual machines to communicate with each other.
  - This is **necessary** when using setups like **Internal Network** or **Host-only**.

---

## ✅ After Installation

- The Ubuntu installation screen will appear when booting with the ISO.
- After installation, remove the ISO.


---

Bu adımlar tamamlandığınızda Ubuntu sisteminiz sanal ortamda çalışmaya hazır olacaktır.



---


---

### 🪟 Windows Server 2019 Virtual Machine Installation

This document explains how to install Windows Server 2019 using VirtualBox and configure basic network settings.

---

## 📥 1. Download the ISO File

Windows Server 2019 ISO file can be obtained from the official Microsoft page or through your MSDN membership.

🔗 [https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019)

---

## 🖥️ 2. Create a New Machine in VirtualBox

1. Open VirtualBox and click the `New` button.
2. Machine Name: `WinServer2019`
3. Type: `Microsoft Windows`, Version: `Windows Server 2019 (64-bit)`
4. Memory (RAM): Minimum **4096 MB** recommended
5. Create a virtual hard disk (VDI, dynamically allocated, at least 40 GB)

---

## 💿 3. Add the ISO File

1. After creating the machine, right-click and go to **Settings > Storage** tab.
2. Under "Controller: IDE", click **Empty**.
3. Choose the **Windows Server 2019 ISO file** from the CD icon on the right.

---

## 🌐 4. Network Settings

- In the machine settings, go to **Network > Connection Type**.
- Select **NAT Network or Bridged Adapter** as the connection type.
- If necessary, enable **Promiscuous Mode → Allow VMs** in the "Advanced" section (Promiscuous Mode selection explanation is provided in the Ubuntu Virtual Machine Setup section).

---

## ⚙️ 5. Installation and Activation

1. Start the machine and ensure it boots from the ISO.
2. The Windows Server installation screen will appear.
3. Enter the product key or proceed with the trial version.
4. Complete the system installation.

---

## ✅ After Installation

- Don't forget to install Guest Additions (for additional drivers and integrations).
- Test the network connection (ping, internet access, etc.).
- If necessary, assign a static IP before proceeding to the next steps (I preferred using a static IP in this project).

---

Bu adımlar tamamlandığında Windows Server sisteminiz sanal ortamda çalışmaya hazır olacaktır.



---


---

### 🐍 Kali Linux Virtual Machine Installation

This document explains step-by-step how to install the Kali Linux operating system using VirtualBox and configure basic network settings.

---

## 📥 1. Download the Kali ISO File

Download the Kali Linux ISO file from the official website:

🔗 [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)

> **Note:** I recommend downloading the "Installer" version. Not the Live version!

---

## 🖥️ 2. Create a New Machine in VirtualBox

1. Open VirtualBox and click the `New` button.
2. Machine Name: `Kali-Linux`
3. Type: `Linux`, Version: `Debian (64-bit)`
4. Memory (RAM): Minimum **2048 MB**, preferably **4096 MB**
5. Create a virtual disk: VDI, Dynamically allocated, at least 20 GB

---

## 💿 3. Add the ISO File

1. After creating the machine:
   - Right-click and go to **Settings > Storage** tab.
   - Select **Empty** and choose the Kali ISO from the CD icon on the right.
2. Once the ISO is attached, click `Start` to begin the installation.

---

## 💬 4. Turkish Keyboard and Language Support

> **Note:** If you want to use Turkish characters (ç, ı, ş...) in the terminal after installation, follow these steps:

**Applications > Session and Startup > Application Autostart > add**

Name: keyword tr
Command:
```bash
setxkbmap tr
```
Trigger: on login

This command activates the Turkish Q keyboard layout.

---

## 🌐 5. Network Settings

- In the machine settings, go to **Network > Connection Type**.
- Select **NAT Network or Bridged Adapter** as the connection type.
- If necessary, enable **Promiscuous Mode → Allow VMs** in the "Advanced" section (you can refer to the explanation in the Ubuntu Virtual Machine Setup section for Promiscuous Mode selection).

---

## ✅ After Installation

- root ya da kali kullanıcısıyla oturum açın.
- Terminal üzerinden `ip a`, `ping` gibi komutlarla ağ bağlantısını test edin.
- Gerekirse statik IP ataması yaparak sonraki adımlara geçebilirsiniz.(Bu projede statik IP ataması yapmayı tercih ettim.)

---

Bu adım tamamlandığınızda Kali Linux, Agent ya da Saldırı makinesi olarak kullanmanız için hazır hale gelir.



---


---

### 🌐 Configuring Static IP Address on Ubuntu (Netplan)

This document explains step-by-step how to assign a static IP address using the `netplan` tool on Ubuntu systems.

---

## 🧰 Requirements

- Ubuntu 18.04 or later (Netplan is included by default)
- A user with root privileges

---

## 🔍 1. Identify the Network Interface

Open the terminal and view your current network interface:

```bash
ip link show
```

It usually appears with a name like `enp0s3`, `ens33`, or `eth0`.

---

## 📝 2. Edit the Netplan Configuration

Open the configuration file with the following command:

```bash
sudo nano /etc/netplan/00-installer-config.yaml
```

Edit the content as shown in the example below:

```yaml
network:
  version: 2
  ethernets:
    enp0s3:
      dhcp4: no
      addresses: [192.168.100.10/24]
      gateway4: 192.168.100.1
      nameservers:
        addresses: [8.8.8.8, 1.1.1.1]
```

> ❗ Replace `enp0s3` with your own network interface name.

---

## 💾 3. Apply the Settings

After saving and closing the file, run the following command:

```bash
sudo netplan apply
```

To verify that the network settings are active:

```bash
ip a
```

---

## 🧪 4. Test the Connection

To test the connection, use:

```bash
ping 8.8.8.8 -c 4
```

or

```bash
ping google.com -c 4
```

---

## ✅ Summary

- Static IP is configured manually using a Netplan YAML file.
- DHCP is disabled, and IP, gateway, and DNS settings are manually defined.
- This configuration is especially critical in virtual network environments for stable communication.

---

Once you complete these steps, your machine will be recognized on the network with a fixed IP address.



---


---

### 🌐 Configuring Static IP Address on Windows Server 2019

This document explains step-by-step how to assign a static IP address on a Windows Server 2019 system.

---

## 🎯 Purpose

Define a static IP address instead of using dynamic IP (DHCP) to ensure the virtual machine is always recognized with the same IP on the network.

---

## 🧭 1. Access Network Settings

1. Right-click the network icon on the taskbar and select **"Network and Sharing Center"**.
2. In the window that opens, go to **"Change adapter settings"**.
3. Right-click the network adapter in use (e.g., `Ethernet`) and select **"Properties"**.

---

## 🌐 2. Edit IPv4 Settings

1. Find and double-click **"Internet Protocol Version 4 (TCP/IPv4)"** in the list.
2. Select the option **Use the following IP address**.
3. Fill in the required fields:

| Field            | Example Value         |
|------------------|-----------------------|
| IP address       | 192.168.100.20        |
| Subnet mask      | 255.255.255.0         |
| Default gateway  | 192.168.100.1         |
| Preferred DNS    | 8.8.8.8               |
| Alternate DNS    | 1.1.1.1               |

4. Click **OK** on all windows to apply the changes.

---

## 🧪 3. Test the Configuration

Open CMD and use the following commands to test the IP and network connection:

```cmd
ipconfig
ping 8.8.8.8
```

---

## ✅ Summary

- Static IP, özellikle SIEM ve ağ güvenliği projelerinde makinelerin sabit bir adresle çalışması için önemlidir.
- Ayarlar manuel girildiğinde kalıcı olur, DHCP'den etkilenmez.
- DNS ayarlarını girerek internet erişimi de sağlanabilir.

---

Once these steps are completed, your Windows server will be connected to the network with a static IP address.



---


---

### 🌐 Kali Linux Statik IP Adresi Ayarlama

This document explains step-by-step how to assign a static IP address to a Kali Linux system.

---

## 🎯 Purpose

- Ensure the Kali system always receives the same IP address on startup
- Enable secure and consistent communication on the network

---

## 🧭 1. Identify the Network Interface Name

Run the following command in the terminal:

```bash
ip a
```

The interface is usually named `eth0`, `enp0s3`, or `ens33`.

---

## 📝 2. Edit the Network Configuration File

Open the network configuration file with the following command:

```bash
sudo nano /etc/network/interfaces
```

Modify the content based on the following example:

```bash
auto eth0
iface eth0 inet static
    address 192.168.100.30
    netmask 255.255.255.0
    gateway 192.168.100.1
    dns-nameservers 8.8.8.8 1.1.1.1
```

> ❗ Replace `eth0` with the name of your own network interface.

---

## 🔄 3. Restart the Network Service

```bash
sudo systemctl restart networking
```

Alternatively, you can use:

```bash
sudo ifdown eth0 && sudo ifup eth0
```

---

## 🧪 4. Connection Verification

IP address and connection verification:

```bash
ip a
ping 8.8.8.8 -c 4
```

---

## ✅ Summary

- Kali'de statik IP ayarı genellikle `/etc/network/interfaces` dosyasından yapılır.
- Ağ hizmeti yeniden başlatıldığında yapılandırma aktif olur.
- Bu ayar sanal makineler arası güvenli bağlantı kurmak için önemlidir.

---

After completing these steps, your Kali Linux system will be ready to operate with a static IP address.



---


---

### 🔁 Ping Test and Troubleshooting Between Virtual Machines

This document explains how to perform a `ping` connection test between Kali, Ubuntu, and Windows virtual machines and how to troubleshoot potential blockers.

---

## 🎯 Purpose

- Verify whether the virtual machines are on the same network
- Test whether each machine can send ICMP (ping) requests to the others
- Ensure network configuration is successful

---

## ✅ 1. Basic Ping Tests

Try pinging other machines from each machine:

### Windows → Kali

```cmd
ping 192.168.100.30
```

### Kali → Windows

```bash
ping 192.168.100.20
```

### Ubuntu → Kali

```bash
ping 192.168.100.30
```

### Kali → Ubuntu

```bash
ping 192.168.100.10
```

### Windows → Ubuntu

```cmd
ping 192.168.100.10
```

### Ubuntu → Windows

```bash
ping 192.168.100.20
```

---

## ⚠️ 2. If Ping Fails – Possible Blockers

### 🛡️ Windows Firewall

On Windows systems, ICMP requests (ping) are **blocked by default**.

#### 🔧 Solution:

1. Go to `Windows Defender Firewall` > `Advanced Settings`.
2. From the left menu, select **Inbound Rules** → then find **File and Printer Sharing (Echo Request - ICMPv4-In)** on the right.
3. Right-click and select **Enable Rule** (make sure it's enabled for Private and Domain profiles).

---

### 🔥 Kali Linux Firewall (iptables / nftables)

On Kali, incoming ICMP requests might be blocked by iptables or nftables rules.

#### 🔧 Solution:

```bash
sudo iptables -A INPUT -p icmp --icmp-type echo-request -j ACCEPT
```

Or for nftables:

```bash
sudo nft add rule inet filter input icmp type echo-request accept
```

Note: To make it persistent, edit `iptables-persistent` or `nftables.conf`.

---

### 🔌 Network Adapter Issue

The VM's network adapter might be "Disconnected".

#### 🔧 Solution:

- Go to VirtualBox > Settings > Network > ensure **Connection Type: Internal Network / Bridged** is selected.
- Make sure all VMs are using the same network name (e.g., `SIEMnet`).

---

### 🧩 Different Subnets

If static IPs are on different subnets (e.g., one is `192.168.100.x`, another is `192.168.1.x`), ping will fail.

#### 🔧 Solution:

- Set all VM IPs within the same subnet block (e.g., `192.168.100.10`, `.20`, `.30`)
- Subnet mask should be `255.255.255.0` on all systems

---

## 🧪 Verification

Ping the other machines again and test the connection. Receiving 4 replies indicates a healthy connection.

---

## ✅ Summary

| Cause                        | Solution                                   |
|-----------------------------|--------------------------------------------|
| Windows ICMP block          | Enable the inbound firewall rule           |
| Kali ICMP block             | Add rule via `iptables` or `nftables`      |
| Network misconfiguration    | Check VirtualBox internal/bridged settings |
| Subnet mismatch             | Align IP/subnet settings                   |

---

After these steps, you should be able to ping between your virtual machines without issues.



---


---

### 🛡️ Wazuh Manager Kurulumu (Ubuntu)

This document explains how to install the Wazuh Manager component on an Ubuntu server and how to create the **agent key** needed for Windows/Linux clients to connect.

---

## 🎯 Purpose

- Install Wazuh Manager on an Ubuntu system to initiate the Wazuh SIEM environment
- Install Wazuh components with a single command
- Generate the required `Agent Key` for client connections (Windows/Linux)

---

## 🧰 Requirements

- Ubuntu 20.04 LTS or 22.04 LTS
- At least 2 vCPUs, 4 GB RAM
- A user with root or sudo privileges
- Static IP should be configured

---

## 🔧 1. System Update and Basic Packages

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl gnupg -y
```

**Why are these packages needed?**

- `curl`: Used to download the installation script from Wazuh's servers
- `gnupg`: Used to verify the digital signatures of packages

---

## 📦 2. Download and Run the Wazuh Installation Script

```bash
curl -sO https://packages.wazuh.com/4.8/wazuh-install.sh
chmod +x wazuh-install.sh
sudo bash ./wazuh-install.sh -a
```

This script installs:
- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard

in one go.

---

## 🔍 3. Check Services After Installation

```bash
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-dashboard
sudo systemctl status wazuh-indexer
```

---

## 🌐 4. Access the Dashboard

Go to the following address in your browser:

```
https://<server-ip>:5601
```

Default username: `admin`  
Password: Shown in the terminal after installation

> You may bypass the SSL warning via "Advanced > Proceed".

---

## 🔐 5. Generate Agent Key

Each agent (Linux or Windows) must have a unique **key** to connect to the Wazuh Manager.

### Key generation tool:

```bash
sudo /var/ossec/bin/manage_agents
```

### In the menu:

- `A` → Add new agent
- `E` → Extract the key
- The key is generated and shown on screen

> ⚠️ **Save this key somewhere safe.**
> You will need it during agent installation.

---

## 🧾 Notes

- A separate key must be generated for each agent.
- `manage_agents` should only be run on the Wazuh Manager.
- Keys are essential for agent authentication.

---

After this step, you can proceed to install the Wazuh Agent on the client systems using the generated key.



---


---

### 🪟 Wazuh Agent Kurulumu

This document explains how to install the Wazuh Agent on a Windows system and how to configure it to connect with the Wazuh Manager.

---

## 🎯 Purpose

- Install Wazuh Agent on a Windows system
- Use the agent key previously generated on the Wazuh Manager to establish the connection

---

## 🧰 Requirements

- A running **Wazuh Manager**
- A previously generated **agent key**
- Windows 10 / 11 / Server 2016+ system

---

## 📦 1. Download the Wazuh Agent Installer

🔗 Download the latest Wazuh Agent MSI:

[https://packages.wazuh.com/4.x/windows/wazuh-agent-4.x.x.msi](https://packages.wazuh.com/4.x/windows/wazuh-agent-4.x.x.msi)

---

## 💿 2. Installation Wizard

Follow these steps during installation:

- Enter the IP address of the Wazuh Manager in the **Manager IP Address** field (e.g., `192.168.100.10`)
- Paste the key generated using `manage_agents` into the **Authentication key** field
- Complete the setup and click **Save**


> You can quickly configure the agent by entering the IP and key directly in the GUI.

---

## ▶️ 3. Start the Service

If the service does not start automatically after installation, run the following command in CMD:

```cmd
sc start wazuh-agent
```

Or manually start the `Wazuh Agent` service from Windows > Services.

---

## ✅ Verification

Verify the agent connection on the Wazuh Manager with the following command:

```bash
sudo /var/ossec/bin/agent_control -l
```

Your Windows system should appear as "Active" under the Agents tab in the Wazuh Dashboard.

---

## 📌 Notes

- The agent key can also be entered directly in the GUI.
- If the connection fails, ensure that TCP ports 1514 and 1515 are open in the Windows Firewall.

---

After completing these steps, your Windows system will be successfully integrated into the SIEM environment.



---


---

### 🔐 SSH Brute-Force Attack Simulation and Wazuh Log Monitoring

This document provides a step-by-step explanation of how to simulate a **brute-force password attack** from Kali Linux against an Ubuntu system running Wazuh Manager, and how Wazuh logs this activity.

---

## 🎯 Purpose

- Perform a password brute-force attack against the SSH service on Ubuntu using the `hydra` tool
- Confirm that Wazuh detects the attack and logs it
- Gain hands-on experience with simple attack monitoring in a SIEM environment

---

## 🧰 Requirements

- Wazuh Manager must be installed and active on the Ubuntu system
- SSH service must be running on the Ubuntu system
- Kali Linux must be able to ping the Ubuntu system
- `hydra` tool must be installed on Kali

```bash
sudo apt install hydra -y
```

---

## 📄 1. Create a Password List

Create a simple password list on the Kali system:

```bash
nano Passwords.txt
```

Example content:

```
123456
admin
root
password
toor
```

Save and exit.

---

## 🧪 2. Launch the Brute-Force Attack

Run the following command in the Kali terminal:

```bash
hydra -l admin -P Passwords.txt ssh://192.168.100.10
```

- `-l admin`: The username to try
- `-P Passwords.txt`: The file containing the list of passwords to try
- `ssh://<ip>`: The target system's IP address and protocol

> 🔥 This attack results in failed login attempts on Ubuntu, which are detected by Wazuh.

---

## 👁️ 3. Monitor Wazuh Logs on Ubuntu

You can monitor Wazuh logs live on the Ubuntu (Wazuh Manager) system using the following command:

```bash
sudo tail -f /var/ossec/logs/alerts/alerts.json
```

Alternatively, you can view the logs in Kibana Dashboard > Security Events.

---

## ✅ Example Logs You May Observe

- "Failed password for admin" from the **sshd** service
- Wazuh alert: `"Authentication failure"` or `"Multiple failed login attempts"`

---

## 🧾 Notes

- Since the Hydra attack sends multiple password attempts quickly, the log file may become large.
- If SSH is not installed on Ubuntu, use the following commands:

```bash
sudo apt install openssh-server -y
sudo systemctl enable ssh
sudo systemctl start ssh
```

---

This simulation is a valuable exercise for tracking real-world attacks and observing Wazuh's response.



---


---

### 🧾 Proje Özeti ve Genel Değerlendirme

In this project, a security monitoring infrastructure capable of observing both Linux and Windows clients was built using the open-source SIEM solution **Wazuh**. Through both technical setup and attack simulations, the system's functionality was demonstrated in practice.

---

## 🧱 What Did the Project Include?

- Installing Wazuh Manager on Ubuntu
- Installing Wazuh Agent on Linux and Windows systems
- Manager-Agent connection configuration
- Brute-force attack simulation using Hydra
- Analyzing Wazuh logs via CLI and dashboard

---

## 🎯 Were the Goals Achieved?

✅ Wazuh environment was successfully installed  
✅ Real-time log monitoring was established  
✅ Basic attacks were detected  
✅ Logs were collected from both Windows and Linux clients  

---

## 🔍 Tips for Future Users

Users attempting this project may encounter errors due to different system setups, network configurations, or software versions. That's completely normal.

> 💡 **Remember:** Real learning often begins when you make mistakes.

Possible issues you might face:

- Connectivity issues (ping, port açık mı?)
- Firewall issues (Windows UFW/NFTables)
- SSH access problems
- Dashboard access failure

In such cases:

- Analyze the full error output
- Review Wazuh documentation → [https://documentation.wazuh.com/](https://documentation.wazuh.com/)
- Search for similar issues on StackOverflow, Wazuh forums, and GitHub Issues
- And of course: Try solving it through trial and error!

---

## 🧡 Final Note

I hope this project helped you not only understand Wazuh, but also gain insights into SIEM systems in general.

If everything went smoothly — great! If you encountered some issues, that's also wonderful — it means you learned something. 🙂

Thank you for trying this project. I hope it sparked a new curiosity in you. 🚀

---

Wishing you productive work and clear, readable logs always!



</details>
