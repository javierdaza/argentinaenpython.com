# Django 是什麼?

Django (*/ˈdʒæŋɡoʊ/ jang-goh*) 是用 Python 寫的一個自由和開放源碼的 web 應用程式框架。 Web 框架是一組可以説明您制定網站更快和更容易的元件。

當你建立一個網站時，你總是需要一套類似的組件: 一種方式來處理使用者身份驗證 (註冊、登入、登出)、管理小組為您的網站、 表格、 一種方式來上傳檔等。

幸運的是，其他人在很久以前已經注意到，當網頁程式設計師建立一個新的網站的時候，都會面臨類似的問題，所以他們聯手，創建了一些框架 (Django 是其中之一)，給你現成的元件讓您可以使用。

各種框架的存在就是節省您免於重新發明輪子，當你建立一個新的網站的時候可以減少重工。

## 你為什麼需要一個框架?

要真正了解 Django 有什麼作用，我們更需要去了解伺服器的運作。首先伺服器需要知道的是，你希望它能夠為你提供一個網頁。

想像一個信箱(埠 port) 會偵測寄來的信的郵箱 (請求 request)。 web 伺服器就是在做這件事 。 Web 伺服器讀這封信，然後寄出一個相對的網頁作為回應。 但是當你想要寄出某個東西，你需要一些內容 而 Django 就是在幫你產生相對應的內容。

## 當某個人向你的伺服器請求的時候發生了什麼事？

當伺服器收到某個請求，這個請求會通過 Django，Django 則負責判斷這個請求是什麼。 Django 會先收到網址然後來判斷應該要給出什麼回應。 這部分是由 Django 的 **urlresolver** 來處理(網址其實就是所謂的 URL - Uniform Resource Locator，所以這就是為什麼這裡取名為 *urlresolver*)。 它不聰明 - 他有一堆範例去判斷這個 URL 符合哪一個範例。 Django 則查看範本，如果 Url 符合某一個，Django 就送出這個請求相對應的函數們(在這裡稱為 *view*).

想像一個帶著信的郵差。 她在街上遊走，確認每家的地址把信送給他們。 如果地址對了，她就把信放進去。 這就是 urlresolver 在做的事情！

在 *view* 函數中會做一些有趣的事情：我們會去資料庫中找某些資料。 萬一使用者要求要更改某些資料呢？ 例如某封請求「拜託把我的工作敘述改一下吧」的信 - *view* 就會檢查你是不是允許他可以做這件事，然後你會在更新了他的工作敘述以後回傳給他一個「完成囉！」的訊息。 之後 *view* 就會產生一個回應，Django 就會將回應送到使用者的瀏覽器上。

當然了，以上的敘述已經簡化了很多，但你也不需要知道所有技術上的細節。有一個簡單的概念即可。

所以不糾結在太多細節敘述上，我們打算就簡單的開始用 Django 做點事，就可以從中學習到更多了。