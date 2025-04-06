# ICRT News Scraper

此程式旨在從 ICRT 網站（https://www.icrt.com.tw）擷取特定新聞內容，並將其格式化後保存為 Word 文件。此工具會抓取來自「News for Kids（國小）」與「News Bites（國中）」等區塊的新聞資料，並將其整理後儲存成 `.docx` 檔案，便於日後查看或分享。

## 功能

- 從指定的 ICRT 網站 URL 擷取最新的新聞。
- 擷取新聞的發佈日期和內容。
- 支援處理不同的新聞區塊，包括「News for Kids（國小）」和「News Bites（國中）」。
- 將擷取的資料儲存為 `.docx` 文件，並格式化為合適的標題結構。
- 剖析和清理內容，過濾不需要的部分。

## 需求

此程式需要以下 Python 函式庫：

- `requests`: 用來發送 HTTP 請求並獲取網頁內容。
- `beautifulsoup4`: 用來解析 HTML 頁面並擷取所需資料。
- `python-docx`: 用來創建和編輯 `.docx` 文件。

你可以使用以下命令安裝這些函式庫：

```bash
pip install requests beautifulsoup4 python-docx
```

## 使用方式

1. 下載或複製本程式的 Python 檔案。
2. 確保已安裝所需的依賴庫（`requests`, `beautifulsoup4`, `python-docx`）。
3. 在程式中執行：

```bash
python ICRT_News_Scraper.py
```

4. 程式將會從 ICRT 網站抓取最新的新聞資料，並儲存為名為 `ICRT_News.docx` 的 Word 檔案。
5. 檢查生成的 `.docx` 文件，查看最新的新聞內容。

## 程式邏輯

1. 程式首先發送 GET 請求到指定的 ICRT 網頁 URL，並接收返回的 HTML 頁面內容。
2. 使用 BeautifulSoup 解析 HTML 並提取包含新聞的區塊，特別是有關「News for Kids（國小）」與「News Bites（國中）」的區域。
3. 程式會將每一個新聞區塊的標題和內容擷取出來，並剖析內容以去除不需要的部分（如 Quiz）。
4. 擷取到的資料會被儲存成一個 Word 文件，並按照標題層級結構格式化。
5. 最後，將結果存儲為 `ICRT_News.docx` 文件。
