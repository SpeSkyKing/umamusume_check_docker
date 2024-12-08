**構築手順**
+ 開発環境の場合
+ local-docker-compose.yml →　docker-compose.yml
+ EC2等で他DBを使う場合
+ product-docker-compose.yml →　docker-compose.yml
+ ファイルの名前を変更する

1. mkdir docker
2. mkdir src
3. docker内でこのリポジトリをクローン
4. src内でsrc用リポジトリをクローン
5. dockerフォルダで docker-compose up -d
6. docker exec -it docker-app-1 bashでphpコンテナへ入る
7. composer installを実行
8. php artisan key:generateを実行
9. cp .env.example .env
10. php artisan migrateを実行
11. .envファイル内の以下項目を変更
+ ----------------------------------
+ DB_CONNECTION=mysql
+ DB_HOST ローカルの場合はdb その他は適切に 
+ DB_PORT ローカルの場合は3306 その他は適切に 
+ DB_DATABASE ローカルの場合は ymlファイルのMYSQL_DATABASE その他は適切に 
+ DB_USERNAME ローカルの場合は ymlファイルのMYSQL_USER その他は適切に 
+ DB_PASSWORD ローカルの場合は ymlファイルのMYSQL_PASSWORD その他は適切に 
+ ----------------------------------
  
