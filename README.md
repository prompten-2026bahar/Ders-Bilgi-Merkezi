🚀 PROJE STANDARTLARI VE GITHUB REPO REHBERİ
Değerli öğrenciler, bu ders kapsamında yapacağınız tüm çalışmaların (çeviri, vize ve final projeleri) yönetimi için GitHub kullanılacaktır. Her grubun tek bir repo (depo) üzerinden çalışması ve aşağıdaki standartlara uyması zorunludur.
________________________________________
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
________________________________________
2. README.md Standartları
Reponun ana sayfasındaki README.md dosyası, projenizin vitrinidir. Şu başlıkları içermelidir:
•	Grup Adı ve Üyeler: Her üyenin adı ve öğrenci numarası.
•	Kütüphane Tanıtımı: Atanan kütüphanenin kısa (3-4 cümlelik) teknik tanımı.
•	Hızlı Bağlantılar: Çeviri dosyalarına ve projelere giden linkler.
•	Kurulum: Projeyi yerel bilgisayarda çalıştırmak için gerekli komutlar (pip install ... vb.).
________________________________________
3. Markdown (Çeviri) Kuralları
Dokümantasyon çevirilerini yaparken aşağıdaki formatı kullanınız:
•	Kod Blokları: Kodları mutlaka dil belirterek yazın.
Python
# Örnek kullanım
from langchain import PromptTemplate
•	Teknik Terimler: Yaygın kullanılan teknik terimleri (Prompt, Embedding, RAG vb.) olduğu gibi bırakıp yanına parantez içinde Türkçe karşılığını yazabilirsiniz veya global literatüre sadık kalabilirsiniz.
•	Görseller: Çevirdiğiniz bölümlerde şema varsa, bunları Markdown içinde şu şekilde çağırın: ![Açıklama](resim_linki).
________________________________________
4. Bireysel Proje Raporu Formatı
Her öğrenci, vize ve final klasörünün içine bir RAPOR.md eklemelidir. Bu rapor şunları içermelidir:
1.	Problem Tanımı: Bu uygulama hangi sorunu çözüyor?
2.	Prompt Stratejisi: Hangi prompt tekniklerini (Few-shot, CoT vb.) kullandınız?
3.	Teknik Mimari: Hangi LLM modeli ve hangi kütüphane özellikleri kullanıldı?
4.	Ekran Görüntüsü/Demo: Uygulamanın çalıştığına dair bir GIF veya görsel.
________________________________________
5. Git Kullanım Kuralları (Mühendislik Etiği)
•	Commit Mesajları: "Güncelleme yaptım" gibi belirsiz mesajlar yerine; "LlamaIndex RAG pipeline eklendi" gibi açıklayıcı mesajlar yazın.
•	Katılım Takibi: Her öğrenci kendi kodunu ve çevirisini kendi GitHub hesabı üzerinden push etmelidir. Bu, vize/final notlandırmasında bireysel katkıyı ölçmek için kullanılacaktır.
________________________________________
6. Teams ve Dosya Teslimi
•	Kodlar: Sadece GitHub üzerinde duracaktır.
•	Sunumlar: Sunum günü kullanılacak .pptx veya .pdf dosyaları, sunumdan 1 saat önce Microsoft Teams üzerindeki ilgili haftanın kanalına yüklenmelidir.
•	Final Raporu: Üniversite sistemine girilmesi gereken resmi raporlar Teams üzerinden PDF olarak toplanacaktır.
________________________________________
💡 Önemli İpucu
Dönem sonunda reponuzun "Public" (açık) olması, iş görüşmelerinde bu projeyi bir referans olarak göstermenize olanak sağlar. Bu yüzden kodlarınızın temiz ve dökümantasyonunuzun eksiksiz olmasına özen gösterin.
