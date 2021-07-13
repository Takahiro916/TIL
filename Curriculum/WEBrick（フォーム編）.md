# Webサーバを立ち上げてWebの仕組みを知る（フォーム編）  
## 課題1  
- form.htmlを作成  
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
  </head>
  <body>
    GETで送る</br>
    <form action="/form_get" method="get">
        <label for ="name">ユーザー名</label>
        <input type="text" name="username"></br>
        <label for ="age">年齢</label>
        <input type="text" name="age"></br>
        <button type="submit">送信</button>
    </form>
    </br>
    POSTで送る</br>
    <form action="/form_post" method="post">
        <label for ="name">ユーザー名</label>
        <input type="text" name="username"></br>
        <label for ="age">年齢</label>
        <input type="text" name="age"></br>
        <button type="submit">送信</button>
    </form>
  </body>
</html>
```

- `http://localhost:8000/form.html`にアクセス  
</br>

[![Image from Gyazo](https://i.gyazo.com/76e036a52239ebfe633764ad40fd91c6.png)](https://gyazo.com/76e036a52239ebfe633764ad40fd91c6)

</br>

## 課題2  
- `req.query`を使用し入力値を取得

```
server.mount_proc("/form_get") do |req, res|
  h = req.query
  body = "<html><head><meta charset=utf-8></head>
  <body>クリエパラメータは#{h}です</br>こんにちは#{h["username"]}さん。あなたの年齢は#{h["age"]}ですね
  </body></html>"
  res.status = 200
  res['Content-Type'] = 'text/html'
  res.body = body
end

server.mount_proc("/form_post") do |req, res|
  h = req.query
  body = "<html><head><meta charset=utf-8></head>
  <body>クリエパラメータは#{h}です</br>こんにちは#{h["username"]}さん。あなたの年齢は#{h["age"]}ですね
  </body></html>"
  res.status = 200
  res['Content-Type'] = 'text/html'
  res.body = body
end
```
