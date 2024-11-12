# Steam Oyun İncelemeleri Üzerine Duygu Analizi

Bu proje, Steam platformundan oyun incelemelerini çekip, metin madenciliği ve duygu analizine tabi tutarak oyun incelemelerinden anlamlı sonuçlar çıkarmayı hedefler.

## İçindekiler
- [Proje Amacı](#proje-amacı)
- [Gereksinimler](#gereksinimler)
- [Adımlar](#adımlar)
  - [1. Problemin Belirlenmesi](#1-problemin-belirlenmesi)
  - [2. Selenium’u Hazırlama](#2-seleniumu-hazırlama)
  - [3. Selenium ile Veri Kazıma](#3-selenium-ile-veri-kazıma)
  - [4. Veri Temizleme Aşaması](#4-veri-temizleme-aşaması)
  - [5. Veriyi Tokenize Etme](#5-veriyi-tokenize-etme)
  - [6. Veriyi CSV’ye Çevirme](#6-veriyi-csvye-çevirme)
- [Kullanılan Kaynaklar](#kullanılan-kaynaklar)

---

## Proje Amacı
Bu projede, Steam oyun incelemelerinin duygu analizini yaparak, oyunlarla ilgili kullanıcı yorumlarını anlamlandırmayı hedefliyoruz. Metin madenciliği teknikleriyle işlenen veriler sayesinde oyun incelemelerindeki duygusal eğilimler belirlenebilir.

## Gereksinimler
- **Python 3.x**
- **Selenium**
- **pandas**
- **NLTK**
- **spaCy**

## Adımlar

### 1. Problemin Belirlenmesi
Öncelikle duygu analizi üzerine çalışılabilecek projeler araştırıldı. Bu bağlamda, Steam platformundaki oyun incelemeleri veri kaynağı olarak seçildi.

### 2. Selenium’u Hazırlama
Veri kazıma işlemi için **Selenium** kütüphanesi seçildi. Selenium’un Chrome tarayıcısı ile uyumlu **ChromeDriver** sürümü projeye dahil edildi.

### 3. Selenium ile Veri Kazıma
- Çalışma ortamına Selenium import edilerek driver çalıştırıldı.
- Veri çekilecek sayfanın URL’si driver’a tanıtıldı ve ilgili HTML etiketleri yardımıyla inceleme verileri toplandı.
- Sayfa kaydırma işlemi, **JavaScript** komutları ile gerçekleştirildi.

### 4. Veri Temizleme Aşaması
Duygu analizine uygun hale getirmek için aşağıdaki önişleme teknikleri kullanıldı:
- **Tokenizasyon** ve **Lemmatizasyon** (kelimelerin köklerini bulma)
- **POS Tagging** (kelime türlerinin belirlenmesi)
- Anlamsız karakterlerin **Regular Expression** (RegEx) ile temizlenmesi

### 5. Veriyi Tokenize Etme
Veriler, **NLTK** kütüphanesi yardımıyla tokenize edildi. Bu işlem, modelleme aşamasında kullanılmak üzere her bir kelimeyi belirli bir etiketle işaretlemeye olanak sağlar.

### 6. Veriyi CSV’ye Çevirme
İşlenmiş veriler **pandas** kütüphanesi kullanılarak CSV formatında dışa aktarıldı.

## Kullanılan Kaynaklar
1. [Pedro PAI - Text Analytics on YouTube](https://www.youtube.com/watch?v=Id2iYV3EfG4&t=209s)
2. [Rob Mulla - YouTube Tutorial](https://www.youtube.com/watch?v=QpzMWQvxXWk&t=775s)
3. [DataCamp - Text Analytics for Beginners](https://www.datacamp.com/tutorial/text-analytics-beginners-nltk)

---

Bu proje, Python kütüphanelerini kullanarak metin verisi üzerinde duygu analizi ve önişleme tekniklerini deneyimlemek isteyenler için uygun bir örnektir.

