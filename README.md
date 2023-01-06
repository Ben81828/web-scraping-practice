## 這是一個爬取「古騰堡計劃」中文電子書的練習(資策會網路爬蟲課程作業)

### 實作以下功能:
1.	取得每一本書的內文，至少 200 本。
2.	依照書名，將內文存在 txt 當中，檔案以書名命名。
3.	將所有 txt 集中放置在同一個目錄當中，不要跟其它程式檔案混在一起，目錄名稱自訂。

### 作業要求
1.	請依觀察，評估是否使用 requests 或 selenium 來爬取資料，沒有特別限制。
2.	沒有限定要透過「Read this book online: HTML (no images)」、「EPUB (no images)」、「Kindle (no images)」、「Plain Text UTF-8」等格式取得資料，方便剖析資料內容即可。
3.	以 Plain Text UTF-8 連結為例：
a.	從中文書的連結進去，看到許多中文書的書名，以下以「三字經」為例。
b.	滑鼠移過去，瀏覽器左下角有該書的超連結(例如 https://www.gutenberg.org/ebooks/12479)。
c.	同時觀察 b. 裡面的連結，得知連結字串的格式，以及尾端的號碼。
d.	點進連結後，會看到「Download This eBook」下面的表格，有列出內文的格式與內文連結。
e.	可以選擇自己方便解析的檔案結構，例如「Plain Text UTF-8」。
f.	僅將中文內文爬回來即可，頁面前後若有英文文字，則不要爬。
g.	若是你選擇 Plain Text UTF-8 格式，Regex 請參考:
i.	正則表達式-全型英數中文字、常用符號unicode對照表
https://reurl.cc/ZrMoWA
ii.	匹配中文字符的正則表達式： [\u4E00-\u9FFF]
https://www.itread01.com/content/1513168876.html
h.	透過正規表達式，有可能配對的句子會變成 list 結構，此時透過 ''.join(listSentences) 將所有配對到的文字變成字串，即是中文全文。
i.	可以選一篇文章，把前述的正規表達式，一起放到 regex101 裡面檢視。

