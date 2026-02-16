# 🚀 PROJE STANDARTLARI VE GITHUB REPO REHBERİ

Değerli öğrenciler, bu ders kapsamında yapacağınız tüm çalışmaların (çeviri, vize ve final projeleri) yönetimi için **GitHub** kullanılacaktır. Her grubun tek bir repo (depo) üzerinden çalışması ve aşağıdaki standartlara uyması zorunludur.

---

## 1. Depo (Repository) Yapısı

Reponuzun düzeni, değerlendirme sürecinin hızı ve profesyonelliği açısından kritiktir. Aşağıdaki klasör yapısını birebir uygulayınız:

```text
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
```

## 2. README.md Standartları

Reponun ana sayfasındaki *README.md* dosyası, projenizin vitrinidir. Şu başlıkları içermelidir:

* **Grup Adı ve Üyeler:** Her üyenin adı ve öğrenci numarası.

* **Kütüphane Tanıtımı:** Atanan kütüphanenin kısa (3-4 cümlelik) teknik tanımı.

* **Hızlı Bağlantılar:** Çeviri dosyalarına ve projelere giden linkler.

* **Kurulum:** Projeyi yerel bilgisayarda çalıştırmak için gerekli komutlar (`pip install ...` vb.)

## 3. Markdown (Çeviri) Kuralları

Dokümantasyon çevirilerini yaparken aşağıdaki formatı kullanınız:

**Kod Blokları:** Kodları mutlaka dil belirterek yazın.

### Örnek kullanım

```py
from langchain import PromptTemplate
```

**Teknik Terimler:** Yaygın kullanılan teknik terimleri (Prompt, Embedding, RAG vb.) olduğu gibi bırakıp yanına parantez içinde Türkçe karşılığını yazabilirsiniz.

**Görseller:** Çevirdiğiniz bölümlerde şema varsa, bunları Markdown içinde şu şekilde çağırın:

`![Açıklama](resim_linki)`

## 4. Bireysel Proje Raporu Formatı

Her öğrenci, vize ve final klasörünün içine bir *RAPOR.md* eklemelidir. Bu rapor şunları içermelidir:

* **Problem Tanımı:** Bu uygulama hangi sorunu çözüyor?

* **Prompt Stratejisi:** Hangi prompt tekniklerini (Few-shot, CoT vb.) kullandınız?

* **Teknik Mimari:** Hangi LLM modeli ve hangi kütüphane özellikleri kullanıldı?

* **Ekran Görüntüsü/Demo:** Uygulamanın çalıştığına dair bir GIF veya görsel.

## 5. Git Kullanım Kuralları (Mühendislik Etiği)

* **Commit Mesajları:** "Güncelleme yaptım" gibi belirsiz mesajlar yerine; "LlamaIndex RAG pipeline eklendi" gibi açıklayıcı mesajlar yazın.

* **Katılım Takibi:** Her öğrenci kendi kodunu ve çevirisini kendi GitHub hesabı üzerinden push etmelidir. Bu, bireysel katkıyı ölçmek için kullanılacaktır.

## 6. Teams ve Dosya Teslimi

* **Kodlar:** Sadece GitHub üzerinde duracaktır.

* **Sunumlar:** Sunum günü kullanılacak .pptx veya .pdf dosyaları, sunumdan 1 saat önce Microsoft Teams üzerindeki ilgili haftanın kanalına yüklenmelidir.

> 💡 Önemli İpucu: Dönem sonunda reponuzun "Public" (açık) olması, iş görüşmelerinde bu projeyi bir referans olarak göstermenize olanak sağlar.

### PROMPT MÜHENDİSLİĞİ: HIZLI BAŞLANGIÇ VE KURULUM REHBERİ

#### 1. Python Kurulumu

Bilgisayarınızda Python 3.10+ kurulu olmalıdır.

Kontrol:

```bash
python --version
```

> Dikkat: Kurulumda "Add Python to PATH" seçeneğini işaretleyin.

#### 2. Sanal Ortam (Virtual Environment) Oluşturma

##### Proje klasörüne gidin

```bash
cd proje-klasorum
```

##### Ortamı oluşturun

```bash
python -m venv venv
```

##### Aktif edin (Windows)

```bash
.\venv\Scripts\activate
```

##### Aktif edin (Mac/Linux)

```bash
source venv/bin/activate
```

#### 3. Temel Kütüphanelerin Kurulumu

Grubunuza göre ilgili komutu çalıştırın:

Genel: `pip install python-dotenv openai anthropic`

1. Grup (LangChain): `pip install langchain langchain-openai`

2. Grup (LlamaIndex): `pip install llama-index`

3. Grup (CrewAI): `pip install crewai`

4. Grup (DSPy): `pip install dspy-ai`

5. Grup (promptfoo): `npm install -g promptfoo`

#### 4. API Anahtarları ve Güvenlik

Proje ana dizininde *.env* adlı bir dosya oluşturun:

```txt
OPENAI_API_KEY=sk-your-key-here
```

> UYARI: .env dosyasını asla GitHub'a yüklemeyin! .gitignore dosyanıza eklediğinizden emin olun.

#### 5. Kurulum Testi

```py
import os
from dotenv import load_dotenv
from openai import OpenAI

load_dotenv()
client = OpenAI()

response = client.chat.completions.create(
  model="gpt-4o-mini",
  messages=[{"role": "user", "content": "Merhaba AI, kurulumum tamam mı?"}]
)

print(response.choices[0].message.content)
```
