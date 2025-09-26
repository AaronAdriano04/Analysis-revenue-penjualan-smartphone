# 📱 Prediksi Total Revenue Penjualan Smartphone  

## 📌 Project Overview  
Proyek ini bertujuan untuk **menganalisis faktor-faktor yang mempengaruhi revenue penjualan smartphone** dan membangun **model prediksi** menggunakan pendekatan statistik serta machine learning.  

Pendekatan yang digunakan menggabungkan:  
- 📊 **Analisis Korelasi** → untuk mengukur hubungan antar variabel  
- 🧪 **ANOVA** → untuk menguji perbedaan signifikan antar kategori  
- 🌲 **Random Forest Regressor** → untuk membuat model prediktif revenue dengan akurasi tinggi  

---

## 🗂️ Dataset  
- **Sumber**: Data penjualan produk elektronik (smartphone & laptop)  
- **Fokus**: Hanya pada **produk smartphone**  
- **Fitur utama**:  
  - 📌 Brand  
  - 💲 Price  
  - 📦 Quantity Sold  
  - 🖥️ RAM, ROM, Processor  
  - 📅 Inward Date, Dispatch Date  
  - 🏬 Region  

---

## 🛠️ Tools & Libraries  
- 🐍 Python (Google Colab)  
- 🐼 Pandas, NumPy  
- 📊 Matplotlib, Seaborn  
- 🤖 Scikit-learn  

---

## 🔎 Workflow  

### 1️⃣ Data Preparation  
- Filter dataset hanya untuk smartphone  
- Konversi tanggal ke format datetime  
- Hitung lama penyimpanan produk di gudang (`DaysInStock`)  
- Bersihkan missing values & konversi storage (RAM, ROM, SSD) ke numerik  
- Tambahkan kolom `Revenue = Price × Quantity Sold`  

### 2️⃣ Exploratory Data Analysis (EDA)  
- 📊 **Bar Chart**: total penjualan per merek  
- 💲 **Average Revenue per Brand**  
- 🔥 **Correlation Heatmap** antar fitur numerik  

### 3️⃣ Model Building  
- Gunakan **Random Forest Regressor** dengan pipeline preprocessing  
- Train-test split (80% : 20%)  
- Feature scaling & one-hot encoding untuk categorical features  

### 4️⃣ Model Evaluation  
- 📈 **R² Score**: `0.99999`  
- 📉 **MAE**: `177.75` → rata-rata error prediksi sangat kecil  

### 5️⃣ Feature Importance  
- Faktor paling berpengaruh:  
  1. **Quantity Sold**  
  2. **Price**  
  3. **DaysInStock**  

- Fitur teknis (RAM, ROM, Processor) memberikan pengaruh yang jauh lebih kecil  

---

## 📊 Results & Insights  
- Brand seperti **Google, Huawei, Nokia** mendominasi jumlah unit terjual  
- Brand seperti **Microsoft & Dell** punya revenue rata-rata lebih tinggi (target segmen premium)  
- **Harga & jumlah unit terjual** adalah faktor terbesar yang memengaruhi revenue  
- Spesifikasi teknis (RAM, ROM, Processor) hanya berpengaruh kecil → strategi harga & distribusi lebih penting  

---

## 🚀 Future Work  
- Mengembangkan model prediktif untuk dataset lebih besar  
- Menambahkan variabel eksternal (misalnya tren pasar global, faktor ekonomi)  
- Membangun dashboard interaktif untuk analisis real-time  
- Mengeksplorasi algoritma lain (XGBoost, Gradient Boosting, Neural Networks)  

---

## ▶️ How to Run  
1. Clone repository:  
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Tambahkan dataset ke folder `data/`  
4. Jalankan notebook di Google Colab atau Jupyter:  
   ```bash
   jupyter notebook BigDataFinal.ipynb
   ```

---

## 📷 Example Visualizations  
| Total Penjualan per Brand | Korelasi Variabel | Feature Importance |  
|---------------------------|------------------|--------------------|  
| ![Brand Sales](visuals/brand_sales.png) | ![Heatmap](visuals/correlation_heatmap.png) | ![Feature Importance](visuals/feature_importance.png) |  

---
