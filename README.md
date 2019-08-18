# pythondiary

## 專案介紹

我就是想做個網站

## 成品展示

[網站網址(host by heroku)](https://pythondiary10730444.herokuapp.com/)

![](https://github.com/ying-an/pythondiary/blob/master/0818.png)

## 使用技術

工具名稱 | 用途
---------|--------
Python 3 | 不需要解釋
Flask(Python)   | 幫我建立伺服器
HTML/CSS  | 網頁表示和排版
Heroku   | 託管網頁
Github   | 存放原始碼

## 程式碼片段

```python
@app.route("/")
def home():
    temp = glob.glob("articles/*")
    fill = []
    for t in temp:
        length = len(glob.glob(t + "/*.txt"))
        category = t.replace("articles/", "")
        f = (category, length)
        fill.append(f)
    return render_template("index.html", cat=fill)

```
