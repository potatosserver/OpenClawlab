# 🦞 OpenClawlab: OpenClaw on Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](你的_COLAB_連結)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

**OpenClawlab** 是一個開源專案，旨在讓任何人都能在 **Google Colab** 的雲端環境中輕鬆運行 **OpenClaw** AI Agent。透過整合 **Ollama**，你可以在不消耗本地硬體資源、完全免費且保護隱私的情況下，跑起強大的自動化網頁代理人。

## ✨ 特色
- 🚀 **一鍵啟動**：針對 Colab 環境優化的啟動腳本。
- 🧠 **輕量模型優化**：預設使用 `qwen2.5-coder` 或 `qwen3` 等高效能輕量模型。
- 🌐 **Discord 整合**：內建 Discord Bot 支援，隨時隨地操控你的 Agent。
- 💸 **零成本**：無需昂貴的 GPU，利用 Colab 提供的免費 CPU/RAM 資源。

## 🚀 快速開始

1. **開啟 Notebook**: 點擊上方的 "Open in Colab" 按鈕。
2. **設定 Token**: 在 `openclaw.json` 或環境變數中填入你的 Discord Token。
3. **執行所有儲存格**: 腳本會自動安裝 Ollama、拉取模型並啟動 OpenClaw。

## 🛠️ 硬體建議 (Colab 免費版)
- **CPU**: 2 Cores (建議設定 `OLLAMA_NUM_THREADS=1`)
- **RAM**: 12GB
- **推薦模型**: 
  - `qwen2.5-coder:1.5b` (最穩定)
  - `qwen3:1.7b` (支援思考鏈)

## ⚙️ 設定檔說明
本專案預設使用 `/root/.openclaw/openclaw.json` 作為設定路徑，主要優化了：
- 限制 `maxConcurrent: 1` 以防止 CPU 過載。
- 設定 `contextWindow: 16000` 以符合 OpenClaw 最低運行要求。
- 關閉 `reasoning` (思考鏈) 以提升在雲端 CPU 上的反應速度。

## ⚠️ 安全提醒
請勿在 `openclaw.json` 中直接公開你的 Discord Token。建議使用 Colab 的 `Secrets` (左側鑰匙圖示) 功能來管理敏感資訊。

## 🤝 貢獻
歡迎提交 Pull Request 或回報 Issue 來改進這個專案！

## 📜 授權
本專案採用 [MIT License](LICENSE).
