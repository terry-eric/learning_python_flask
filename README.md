# leaning_python_flask

flask的基礎架設網站從以下程式碼開始：

```
from flask import *
def test():

   app = Flask(__name__)

   @app.route("/")
   def home():
       return render_template("test.html")
   app.run(debug=Ture)

if __name__ == '__main__':
    test()

```
因為我們要用到Flask這個物件，所以一開始就要做出宣告，* 是指引入所有flask內的函式。

```from flask import *```  

初始化Flask物件，並貼上app這個標籤。接著我們就可以很方便的使用這個物件裡面的各種功能。

```app = Flask(__name__)```

創造出主網域下的"/"這個網址，並定義了請求(request)該網址時可用的手段。舉例來說，主網域是.123.com/" ，那麼用@app.route("/")就是創造出了".123.com/" 。而用@app.route("/456")就是創造出了"123.com/456" 。

```@app.route("/")```

告訴你怎樣的url可以call怎樣的function

```app.run(debug=Ture)```

就是執行的意思，debug救世會將更改程式碼儲存、重啟，變為更新後的樣子。

```
if __name__ == '__main__':
    test()
```

如果這個程式碼是主要執行檔的話才會執行

