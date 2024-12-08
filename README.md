環境構築手順
1 mkdir docker　
2 mkdir src　
3 docker内でこのリポジトリをクローン　
4 src内でsrc用リポジトリをクローン　
5 dockerフォルダで docker-compose up -d　
6 docker exec -it docker-app-1 bashでphpコンテナへ入る　
7 composer installを実行　
8 php artisan key:generateを実行　
9 cp .env.example .env　
