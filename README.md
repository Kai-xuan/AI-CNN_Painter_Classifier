# 🎨 AI 藝術辨識專案：使用 CNN 模型判別畫家

本專案目標是透過卷積神經網路（CNN）模型訓練，來辨識畫作的創作者，解決來自《Best Artworks of All Time》資料集中 50 位畫家的多類別分類問題。

---

## 📌 專案目標

- 輸入一張畫作圖片，自動判斷是出自哪位畫家
- 使用 TensorFlow 自建 CNN 架構進行訓練
- 實作多分類圖像辨識應用

---

## 🖼️ 使用資料集

- 📂 資料來源：[Best Artworks of All Time](https://www.kaggle.com/ikarus777/best-artworks-of-all-time)
- 包含 50 位世界著名畫家，共數千張畫作
- 每張圖片檔名中包含作者資訊，需自行從檔名前處理出 label
- 分為訓練集 `train_resized/` 和測試集 `test_resized/`

---

## 🧠 使用技術

| 技術 | 說明 |
|------|------|
| Python | 主程式語言 |
| TensorFlow / Keras | CNN 架構實作 |
| Pandas | 資料整理 |
| Matplotlib / Seaborn | 資料與訓練結果視覺化 |
| OpenCV | 圖像讀取與前處理 |

---

## 🏗️ 模型架構

- 使用多層卷積層與 MaxPooling 層進行特徵提取
- Dense 層進行分類（共 50 類）
- 激活函數使用 ReLU、輸出層使用 Softmax
- optimizer：Adam

---

## 📈 訓練成果展示

- 最終測試集準確率（Test Accuracy）：`約 60~80%`（依實際訓練而定）
- 混淆矩陣與分類報表（可加入圖）
- 實測推論功能 `predict_author(img)` ✅

---

## ▶️ 執行方式

1. 安裝套件：

```bash
pip install tensorflow opencv-python pandas matplotlib seaborn
