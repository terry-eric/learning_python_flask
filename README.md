# leaning_python_flask

flask的基礎架設網站從以下程式碼開始：

```
from flask import Flask
def test():

   app = Flask(__name__)

   @app.route("/")
   def test():
       return render_template("test.html")
   app.run(debug=Ture)

if __name__ == '__main__':
    test()
```
因為我們要用到Flask這個物件，所以一開始就要做出宣告，* 是指引入所有flask內的函式，建議是只引入需要的函式，避免占空間和名字重複的問題。

```from flask import *```  

初始化Flask物件，並貼上app這個標籤。接著我們就可以很方便的使用這個物件裡面的各種功能。

```app = Flask(__name__)```

創造出主網域下的"/"這個網址，並定義了請求(request)該網址時可用的手段。舉例來說，主網域是.123.com/" ，那麼用@app.route("/")就是創造出了".123.com/" 。而用@app.route("/456")就是創造出了"123.com/456" 。

```@app.route("/")```

告訴你怎樣的url可以call怎樣的function，url會這樣顯示localhost:5000/，斜線後是接你的函式名稱，例如：def test()，出來就是localhost:5000/test。

```def home():```

def為定義一個函式，後方為函式的名稱。

```return render_template("test.html")```

reture將內文顯現於介面，render_template()則是呼叫HTML的檔案，通常不會在python裡撰寫html的架構，所以需要這個功能呼叫html的檔案；檔案方面須注意放置的位置和名稱會在下方做說明。

```app.run(debug=Ture)```

就是執行的意思，debug救世會將更改程式碼儲存、重啟，變為更新後的樣子。

```if __name__ == '__main__':```

如果這個程式碼是主要執行檔的話才會執行。


#HTML、CSS檔放置的位置

![image](https://user-images.githubusercontent.com/67619529/132873855-81f6c5a4-65c6-4df8-bd6d-4b2861048fc8.png)



