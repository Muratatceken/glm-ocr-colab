# GLM-OCR Colab Test

Tıbbi belgelerde (anamnez formları, patoloji raporları) GLM-OCR ile OCR kalitesini test etmek için Google Colab notebook'u.

## Kullanım

1. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/glm-ocr-colab/blob/main/glm_ocr_test.ipynb) tıklayın
2. Runtime > Change runtime type > **T4 GPU** seçin
3. Hücreleri sırasıyla çalıştırın
4. PDF/görüntü dosyalarınızı yükleyin
5. GLM-OCR vs Tesseract karşılaştırmasını görün

## Pipeline

```
PDF/Görüntü → vLLM + GLM-OCR (T4 GPU) → Metin çıktısı
           → Tesseract OCR (karşılaştırma)  → Metin çıktısı
```

## Gereksinimler

- Google Colab (ücretsiz T4 GPU yeterli)
- PDF veya görüntü dosyaları

## Notlar

- GLM-OCR 0.9B parametre, T4'te ~10-30 sn/sayfa
- İlk çalıştırmada model indirme ~2 dk sürer
- Tüm işlem Colab'da yapılır, dosyalar dışarı gönderilmez
