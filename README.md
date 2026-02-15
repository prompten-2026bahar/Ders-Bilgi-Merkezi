🚀 PROJE STANDARTLARI VE GITHUB REPO REHBERİ
Değerli öğrenciler, bu ders kapsamında yapacağınız tüm çalışmaların (çeviri, vize ve final projeleri) yönetimi için GitHub kullanılacaktır. Her grubun tek bir repo (depo) üzerinden çalışması ve aşağıdaki standartlara uyması zorunludur.

1. Depo (Repository) Yapısı
Reponuzun düzeni, değerlendirme sürecinin hızı ve profesyonelliği açısından kritiktir. Aşağıdaki klasör yapısını birebir uygulayınız:
Plaintext
/
├── translation/            # Dokümantasyon çevirileri (.md formatında)
│   ├── giris.md
│   ├── temel-kavramlar.md
│   └── ...
├── vize_projesi/           # Vize dönemi bireysel uygulamaları
│   ├── ogrenci_adi_1/      # Her öğrenci kendi klasöründe çalışır
│   ├── ogrenci_adi_2/
│   └── ...
├── final_projesi/          # Final dönemi bireysel uygulamaları
│   ├── ogrenci_adi_1/
│   ├── ogrenci_adi_2/
│   └── ...
├── docs/                   # Sunum dosyaları (PDF) ve Ek raporlar
└── README.md               # Projenin ana tanıtım sayfası (Açılış ekranı)

2. README.md Standartları
Reponun ana sayfasındaki README.md dosyası, projenizin vitrinidir. Şu başlıkları içermelidir:
•	Grup Adı ve Üyeler: Her üyenin adı ve öğrenci numarası.
•	Kütüphane Tanıtımı: Atanan kütüphanenin kısa (3-4 cümlelik) teknik tanımı.
•	Hızlı Bağlantılar: Çeviri dosyalarına ve projelere giden linkler.
•	Kurulum: Projeyi yerel bilgisayarda çalıştırmak için gerekli komutlar (pip install ... vb.).

3. Markdown (Çeviri) Kuralları
Dokümantasyon çevirilerini yaparken aşağıdaki formatı kullanınız:
•	Kod Blokları: Kodları mutlaka dil belirterek yazın.
Python
# Örnek kullanım
from langchain import PromptTemplate
•	Teknik Terimler: Yaygın kullanılan teknik terimleri (Prompt, Embedding, RAG vb.) olduğu gibi bırakıp yanına parantez içinde Türkçe karşılığını yazabilirsiniz veya global literatüre sadık kalabilirsiniz.
•	Görseller: Çevirdiğiniz bölümlerde şema varsa, bunları Markdown içinde şu şekilde çağırın: ![Açıklama](resim_linki).

4. Bireysel Proje Raporu Formatı
Her öğrenci, vize ve final klasörünün içine bir RAPOR.md eklemelidir. Bu rapor şunları içermelidir:
1.	Problem Tanımı: Bu uygulama hangi sorunu çözüyor?
2.	Prompt Stratejisi: Hangi prompt tekniklerini (Few-shot, CoT vb.) kullandınız?
3.	Teknik Mimari: Hangi LLM modeli ve hangi kütüphane özellikleri kullanıldı?
4.	Ekran Görüntüsü/Demo: Uygulamanın çalıştığına dair bir GIF veya görsel.

5. Git Kullanım Kuralları (Mühendislik Etiği)
•	Commit Mesajları: "Güncelleme yaptım" gibi belirsiz mesajlar yerine; "LlamaIndex RAG pipeline eklendi" gibi açıklayıcı mesajlar yazın.
•	Katılım Takibi: Her öğrenci kendi kodunu ve çevirisini kendi GitHub hesabı üzerinden push etmelidir. Bu, vize/final notlandırmasında bireysel katkıyı ölçmek için kullanılacaktır.

6. Teams ve Dosya Teslimi
•	Kodlar: Sadece GitHub üzerinde duracaktır.
•	Sunumlar: Sunum günü kullanılacak .pptx veya .pdf dosyaları, sunumdan 1 saat önce Microsoft Teams üzerindeki ilgili haftanın kanalına yüklenmelidir.
•	Final Raporu: Üniversite sistemine girilmesi gereken resmi raporlar Teams üzerinden PDF olarak toplanacaktır.
________________________________________
💡 Önemli İpucu
Dönem sonunda reponuzun "Public" (açık) olması, iş görüşmelerinde bu projeyi bir referans olarak göstermenize olanak sağlar. Bu yüzden kodlarınızın temiz ve dökümantasyonunuzun eksiksiz olmasına özen gösterin.

 
"Sıfırdan Kurulum Kılavuzu"
________________________________________
🛠️ PROMPT MÜHENDİSLİĞİ: HIZLI BAŞLANGIÇ VE KURULUM REHBERİ
Bu rehber, derste kullanacağımız araçların bilgisayarınıza sorunsuz kurulması için hazırlanmıştır.
1. Python Kurulumu
Bilgisayarınızda Python 3.10 veya daha yeni bir sürüm kurulu olmalıdır.
•	Kontrol: Terminal/PowerShell açın ve python --version yazın.
•	Yükleme: Eğer yüklü değilse python.org üzerinden en güncel kararlı sürümü indirin.
•	Dikkat: Kurulum sırasında "Add Python to PATH" seçeneğini işaretlediğinizden emin olun.
2. IDE (Geliştirme Ortamı) Önerisi
Kod yazmak ve projeleri yönetmek için aşağıdaki araçlardan birini kullanmanız tavsiye edilir:
•	VS Code (Önerilen): Python ve Jupyter eklentileriyle birlikte.
•	Cursor: AI destekli kod yazımı için (Prompt mühendisliğine giriş için harika bir deneyim sunar).
3. Sanal Ortam (Virtual Environment) Oluşturma
Projelerinizin birbirine karışmaması için her grup/öğrenci bir sanal ortam oluşturmalıdır:
Bash
# Proje klasörünüze gidin
cd proje-klasorum

# Sanal ortam oluşturun
python -m venv venv

# Aktif hale getirin:
# Windows için:
.\venv\Scripts\activate
# Mac/Linux için:
source venv/bin/activate
4. Temel Kütüphanelerin Kurulumu
Grubunuza atanan kütüphaneye göre aşağıdaki komutu çalıştırın:
•	Genel (Herkes İçin): pip install python-dotenv openai anthropic
•	1. Grup (LangChain): pip install langchain langchain-openai
•	2. Grup (LlamaIndex): pip install llama-index
•	3. Grup (CrewAI): pip install crewai
•	4. Grup (DSPy): pip install dspy-ai
•	5. Grup (promptfoo): npm install -g promptfoo (Not: promptfoo Node.js gerektirir)
5. API Anahtarları ve Güvenlik (Kritik!)
Prompt mühendisliği için bir model sağlayıcısına (OpenAI, Anthropic veya Google Gemini) ihtiyacınız olacak.
•	.env Dosyası Kullanımı: API anahtarlarınızı asla doğrudan kodun içine yazmayın!
•	Proje klasörünüzde .env adlı bir dosya oluşturun ve içine şunu yazın:
Kod snippet'i
OPENAI_API_KEY=sk-your-key-here
•	.gitignore Kontrolü: GitHub'a dosya yüklerken .env dosyasının gitmediğinden emin olun. (Bu, not kırma sebebidir!)
6. Kurulum Testi (Hello World)
Her şeyin doğru çalıştığını test etmek için aşağıdaki küçük Python kodunu çalıştırın:
Python
import os
from dotenv import load_dotenv
from openai import OpenAI

load_dotenv() # .env dosyasındaki anahtarı yükler
client = OpenAI()

response = client.chat.completions.create(
  model="gpt-4o-mini",
  messages=[{"role": "user", "content": "Merhaba AI, kurulumum tamam mı?"}]
)

print(response.choices[0].message.content)
________________________________________
Notlar:
1.	Node.js Notu: promptfoo grubu için bilgisayarlarında Node.js yüklü olması gerekir
2.	Maliyet Yönetimi: Öğrencilere OpenAI'ın "Usage" kısmından limit belirleyin. 

