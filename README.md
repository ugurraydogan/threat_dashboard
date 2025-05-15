# 🛡️ Malware Detection & Live Threat Dashboard

Bu proje, gerçek zamanlı olarak ağ trafiğini izleyen, sistem kaynaklarını gözlemleyen ve verilen URL'nin iç bağlantılarını derinlemesine analiz ederek potansiyel tehditleri renk kodlu şekilde gösteren, koyu temalı bir güvenlik dashboard'udur.

## 🚀 Özellikler

- 📡 **Gerçek zamanlı ağ paketi izleme** (Scapy)
- 🔍 **URL ve bağlantı tarama** (tüm iç linkleri analiz eder)
- ⚠️ **Renk kodlu zafiyet gösterimi**:
  - 🟩 Temiz bağlantılar
  - 🟧 Şüpheli uzantılar
  - 🟥 Zararlı içerikler (örnek: `.zip`, `base64`, `payload`)
- 💻 **Sistem durumu izleme**: CPU, RAM, Disk
- 💡 Koyu temalı, responsive, tek sayfa uygulama (Flask + SocketIO)

---

## 📦 Gereksinimler

- Python 3.8+
- Windows işletim sistemi
- [Npcap](https://nmap.org/npcap/) yüklü olmalı (WinPcap Compatibility Mode açık!)

### 🔧 Gerekli Python kütüphaneleri:

pip install flask flask-socketio scapy psutil requests beautifulsoup4

🗂️ Kurulum
Bu projeyi klonla:

git clone https://github.com/kullanici-adi/malware-dashboard.git
cd malware-dashboard

Gerekli bağımlılıkları yükle:

pip install -r requirements.txt

Eğer requirements.txt yoksa yukarıdaki tek tek kurulum komutunu kullan.

Npcap kurulu değilse indir ve yükle:
👉 Npcap İndir ( https://nmap.org/npcap/ )

Kurulum sırasında "WinPcap Compatibility Mode" kutusunu işaretle.

Uygulamayı çalıştır:

bash
Kopyala
Düzenle

python malware_dashboard.py

🖥️ Kullanım
Dashboard açıldığında:

Ağ trafiği gerçek zamanlı listelenmeye başlar.

CPU / RAM / Disk bilgileri sürekli güncellenir.

URL taraması yapmak için:

Üstteki kutuya https://ornek.com gibi bir adres yaz

"Taramayı Başlat" → Yüzeysel güvenlik taraması

"Derin Taramayı Başlat" → Tüm bağlantılar analiz edilir

Sonuçlar:

🟢 Temiz bağlantılar

🟧 Şüpheli uzantılar (eski JS, iframe vb.)

🟥 Zararlı içerikler (trojan, zip, payload vb.)

📸 Görseller
Canlı Trafik	URL Taraması

📌 Notlar
Dashboard, sadece yerel ağınızdaki trafik için çalışır.

Bu uygulama eğitim/demonstrasyon amaçlıdır. Gerçek dünya saldırı tespiti için antivirüs ve SIEM sistemleriyle entegre edilmelidir.

Gelişmiş özellikler için:

Virustotal API entegrasyonu

Kara liste yönetimi

Ağ üzerindeki cihazları tarama

🤝 instagram.com/ugurayydogan
Pull request'ler ve öneriler memnuniyetle karşılanır!
Yıldız vermeyi ve forku unutma ⭐
