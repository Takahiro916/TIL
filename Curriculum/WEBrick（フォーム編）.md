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
