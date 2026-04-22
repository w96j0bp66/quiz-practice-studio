# Quiz Practice Studio

這是一個本機網頁版練習系統，目標是像 Quizlet 一樣做題，但支援你自行上傳題庫檔案（Markdown / TXT）。

## 你可以做什麼

- 上傳自製題庫檔案
- 自動解析題目、選項、答案
- 若缺題目或缺答案會阻擋並提示錯誤
- 線上作答（單題提交、立即看對錯）
- 顯示進度、正確率、完整作答總覽
- 支援隨機題目順序

## 支援的題庫格式（範例）

```md
**1.** Linux 的作者是誰？
- (A) Bill Gates
- (B) Linus Torvalds
- (C) Steve Jobs
- (D) Mark Zuckerberg
```

答案可使用下列任一格式：

```md
| 題號 | 答案 |
| 1    | B    |
| 2    | C    |
```

或

```md
1. B
2. C
```

## 如何啟動

1. 進到專案資料夾：

```powershell
cd "C:\Users\yyys\Documents\New project"
```

2. 用瀏覽器打開 `index.html`。  
若你想用本機伺服器（推薦），可用：

```powershell
python -m http.server 8000
```

再開啟：

[http://localhost:8000](http://localhost:8000)

3. 在頁面上傳你的題庫（例如：`C:\Users\yyys\Downloads\linux_quiz_120.md`），按「載入並開始練習」。

