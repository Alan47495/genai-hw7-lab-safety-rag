# 🧯 實驗室保命 RAG：問阿哲學長之前，先查守則

中興大學 生科3 蔡宸維｜生成式 AI 課程 HW7：打造自己的 RAG 對話機器人

## 資料

- 文件：《國立中興大學微生物暨公共衛生學研究所安全衛生工作守則》（104 年 3 月 2 日所務會議修訂名稱及全文通過）
- 原始 PDF：https://www.gimph.nchu.edu.tw/storage/upload/download/1040302.pdf
- 處理：只取中文版，依章／條／款切成 35 篇 TXT（一節一檔），只接回 PDF 換行、不改寫條文；每篇加上章節、類別、原文頁碼與一題檢索練習問題。

## 在 Colab 開啟

- RAG02（RAG 對話機器人＋Gradio，主要繳交）：[Open in Colab](https://colab.research.google.com/drive/1rayJ5b67XliKvi6EQgUWxb0NMAEG3vYU?usp=sharing)
- RAG01（建立向量資料庫）：[Open in Colab](https://colab.research.google.com/drive/1IFT1gKtsDeJjBzHFi4XrslNUJpclnZVI?usp=sharing)

## 檔案

| 檔案 | 說明 |
|---|---|
| `lab-safety-docs/` | 35 篇條文 TXT |
| `lab-safety-docs.zip` | 上面資料夾的 ZIP，RAG01 從這裡下載 |
| `rag-data.zip` | RAG01 匯出的向量資料庫（`index.faiss`、`documents.json`、`index_doc_ids.json`、`config.json`），RAG02 從這裡下載 |
| `*_RAG01.ipynb` | 讀取並向量化條文，建立 FAISS 向量資料庫，匯出 `rag-data.zip` |
| `*_RAG02.ipynb` | 讀入 `rag-data.zip`，用 AIsuite（Groq `openai/gpt-oss-120b`）做 RAG，以 Gradio 展示 |

條文版權屬原單位，本 repo 僅供課程作業使用；實際規定請以學校環安中心與各實驗室最新版本為準。
