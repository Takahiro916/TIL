# 【Webサーバを立ち上げてWebの仕組みを知る（動的ページ編）】  

## 【課題】  

```
require 'webrick'

server = WEBrick::HTTPServer.new({ 
  :DocumentRoot => './',
  :BindAddress => '127.0.0.1',
  :Port => 8000
})

server.mount_proc("/time") do |req, res|
 # レスポンス内容を出力
 body = "<html><body>#{Time.now}</body></html>"
 res.status = 200
 res['Content-Type'] = 'text/html'
 res.body = body
end
 
server.start
```
[![Image from Gyazo](https://i.gyazo.com/471279bef065e3948fcc05eb0c54fd49.gif)](https://gyazo.com/471279bef065e3948fcc05eb0c54fd49)

## 【表示を変えてみる】  
- レスポンス内容を変更して表示を変えてみる

```
now = Time.now
str = now.strftime("%Y年%m月%d日 %H:%M:%S")
  
body = "<html>
         <head>
          <meta charset=utf-8>
         </head>
         <body>#{str}</body>
        </html>"
```

[![Image from Gyazo](https://i.gyazo.com/781b8b9c1b3dc1ec8040e697f4d91e0e.png)](https://gyazo.com/781b8b9c1b3dc1ec8040e697f4d91e0e)

