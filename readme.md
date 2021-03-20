# wp

## 概要
wordpress と mysql を docker compose で起動するサンプル

参考  
https://docs.docker.jp/compose/wordpress.html
<br>
<br>

## 起動・終了

### 起動
```
% cd ./wp   
% docker-compose up -d

ブラウザで
http://localhost:8000  
id/pw: （install後の初回セットアップ設定値）  ←volume消したら変わっちゃうけど
```
<br>

### 起動中プロセスの確認
```% docker-compose ps```  
<br>

### 終了
```% docker-compose stop```  
<br>

### 削除
```% docker-compose rm```  
<br>

### おまけ
各種設定地は db_data という名称でvolumeに保存しているため、削除したいときは    
```
% docker image ls    
% docker image rm [image-id]  
```
や、  
```
% docker volume ls  
% docker volume rm [image-id]  
```
で削除をしてみる  
<br>

### wordpress管理画面

http://localhost:8000/wp-admin/


