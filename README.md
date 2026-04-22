# Quiz Practice Studio

單檔前端測驗練習工具，支援匯入 Markdown / TXT 題庫，提供「正式測驗」與「即時練習」兩種模式，適合在課堂、考前複習或自我測驗時使用。

## 功能特色

- 單一 `index.html` 即可執行，無需安裝套件
- 支援上傳 `.md`、`.txt` 題庫檔
- 兩種作答模式：
  - 正式測驗模式：可先全部作答後一次提交
  - 練習模式：每題可即時提交並鎖定答案
- 可選擇是否「隨機打亂題目」
- 顯示題數、已作答數、正確率與進度條
- 提供結果總表，並可從結果表跳回指定題目
- 自動儲存作答進度（`localStorage`），重開頁面可恢復
- 內建文字編碼 fallback（`utf-8` / `big5` / `gb18030` / `utf-16le`）

## 題庫格式

題目與答案可以放在同一份檔案中。

### 題目區塊

支援以下兩種題號格式：

```md
**1.** Linux 的作者是誰？
1. Linux 的作者是誰？
```

選項格式（A~D，至少 2 個選項）：

```md
- (A) Bill Gates
- (B) Linus Torvalds
- (C) Steve Jobs
- (D) Mark Zuckerberg
```

### 答案區塊

可用任一格式：

```md
1. B
2) C
3: A
4 D
```

或表格格式：

```md
| 題號 | 答案 |
| --- | --- |
| 1 | B |
| 2 | C |
```

## 快速開始

1. 下載或複製本專案
2. 直接用瀏覽器開啟 `index.html`
3. 匯入題庫檔（`.md` / `.txt`）
4. 選擇模式與是否打亂題目
5. 開始作答

若瀏覽器限制本機檔案行為，可改用本機伺服器：

```powershell
cd "D:\NCU\Others\Linux and Edge Computing\quiz-practice-studio"
python -m http.server 8000
```

然後開啟 [http://localhost:8000](http://localhost:8000)。

## 模式說明

- 正式測驗模式
  - 可自由切題後一次提交
  - 未完成時提交會先提醒未作答題目
  - 提交後顯示整體成績與各題對錯
- 練習模式
  - 每題提交後立即判斷正誤
  - 已提交題目會鎖定
  - 正確率以「已提交題目」計算

## 專案結構

```text
quiz-practice-studio/
├─ index.html   # 主程式（UI + 邏輯）
└─ README.md
```

## 已知限制

- 選項僅支援 `A`~`D`
- 每題需要有對應答案，且答案必須存在於該題選項中
- 題號不可重複

