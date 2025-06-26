# Text-Classification-and-Summarization-of-Amazon-Reviews
![image](https://github.com/user-attachments/assets/a8c12b76-f893-4c00-a1f3-ca58ad8e06bd)

## 🧩 Project Overview
### Latar Belakang
Dalam era digital, ulasan pelanggan memainkan peran krusial dalam membentuk persepsi terhadap suatu produk. Ulasan ini dapat memberikan wawasan berharga bagi bisnis untuk meningkatkan kualitas produk dan layanan. Namun, dengan volume data yang besar, proses analisis manual menjadi tidak efisien.

### Tujuan Proyek
Proyek ini bertujuan untuk:
- Mengklasifikasikan sentimen dari ulasan pelanggan (positif atau negatif).
- Menyusun ringkasan otomatis dari konten ulasan.
- Memberikan insight berbasis data untuk mendukung pengambilan keputusan.

### Permasalahan
Perusahaan menghadapi tantangan dalam memahami persepsi pelanggan secara cepat dan akurat dari ribuan ulasan. Diperlukan sistem otomatis untuk mengklasifikasikan dan menyarikan informasi penting dari ulasan tersebut.

### Pendekatan
Analisis dilakukan menggunakan Python di Google Colab. Sentiment analysis dilakukan dengan TextBlob, klasifikasi dengan Naive Bayes, visualisasi dengan WordCloud, dan summarization dibantu oleh model AI. IBM Granite atau LLM digunakan untuk membandingkan efektivitas summarization AI terhadap metode manual.

## 🔍 Analysis Process
### Data Loading dan Preprocessing
- Dataset amazon.csv dimuat dan dibersihkan (menghapus review kosong).
- Semua review dikonversi ke tipe data string.

### Sentiment Analysis
![image](https://github.com/user-attachments/assets/c39ac16a-a5de-4304-b7e1-e350f68f69f5)

- Menggunakan TextBlob untuk menghitung polaritas sentimen.
- Hasilnya dikategorikan menjadi positive (> 0) dan negative (≤ 0).
- Visualisasi distribusi sentimen dilakukan dengan grafik batang.

### Text Visualization
![image](https://github.com/user-attachments/assets/67c63199-5379-4ea7-a4de-35ac23f37ba6)
- WordCloud digunakan untuk menampilkan kata-kata yang paling sering muncul dalam ulasan.

### Text Classification
![image](https://github.com/user-attachments/assets/20bc073c-977b-412e-bd89-8eb9efa5a771)
- Ulasan diubah menjadi fitur numerik menggunakan CountVectorizer (Bag-of-Words).
- Model klasifikasi Multinomial Naive Bayes dilatih pada 80% data dan diuji pada 20%.
- Evaluasi dilakukan menggunakan classification report.

### Summarization
![image](https://github.com/user-attachments/assets/fc27ebd2-e5f1-458f-b061-e7c8b0e8ea0c)
- 100 ulasan positif dan negatif digabungkan dan disarikan secara manual.
- Hasil ini kemudian dibandingkan dengan hasil ringkasan dari AI (LLM/IBM Granite).


## Insight & Findings
- Mayoritas review yang dianalisis memiliki sentimen positif, menandakan tingkat kepuasan pelanggan yang tinggi.
- WordCloud menampilkan kata-kata dominan seperti "great", "good", "easy", dan "love", menunjukkan aspek-aspek produk yang dihargai.
- Model klasifikasi Naive Bayes mampu memisahkan sentimen dengan cukup akurat, menunjukkan bahwa klasifikasi otomatis bisa diandalkan.

- Ringkasan dari ulasan menunjukkan bahwa:
Pelanggan positif menghargai kualitas produk, harga yang wajar, dan pengiriman cepat.
Pelanggan negatif mengeluhkan kerusakan produk, pengiriman lambat, atau ekspektasi yang tidak terpenuhi.

## ✅ 4. Conclusion & Recommendation
### Kesimpulan
Proyek ini menunjukkan bahwa analisis sentimen dan summarization terhadap ulasan pelanggan dapat memberikan insight yang kaya dan bernilai. Kombinasi metode NLP tradisional dan AI modern membantu memahami persepsi pelanggan dalam skala besar.

### Rekomendasi
- Tindak Lanjut Positif: Perkuat aspek yang dihargai pelanggan seperti kecepatan pengiriman dan kualitas produk.
- Perbaikan Negatif: Tinjau kembali rantai pasok dan kontrol kualitas untuk mengurangi keluhan.
- Integrasi Sistem Otomatis: Implementasikan sistem klasifikasi sentimen otomatis ke dalam dashboard manajemen produk.
- Customer Service: Gunakan hasil analisis untuk melatih tim layanan pelanggan berdasarkan topik keluhan yang sering muncul.

## 🤖 AI Support Explanation
Dalam proyek ini, AI digunakan pada dua titik penting:
1. Sentiment Analysis dengan TextBlob

- AI rule-based berbasis leksikal untuk menilai polaritas kalimat.
- Efektif sebagai baseline karena ringan dan cepat meski memiliki keterbatasan dalam menangani sarkasme atau konteks kompleks.

2. Summarization dengan LLM (GPT-style)
- Large Language Models digunakan untuk menyarikan ulasan panjang menjadi ringkasan padat dan informatif.
- Dibandingkan dengan ringkasan manual atau rule-based, AI mampu menangkap konteks dan menyajikan narasi yang lebih alami dan komprehensif.

3. Contoh prompt yang digunakan untuk LLM:
- "Ringkas ulasan pelanggan berikut dalam tidak lebih dari 5 poin, menyoroti pendapat kunci, keluhan, dan sentimen positif."

AI membantu mempercepat proses analisis dan menghasilkan ringkasan yang scalable untuk jumlah data yang besar.


  
