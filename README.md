# docker_django_test

### Djangoプロジェクトの作成
docker-compose run web django-admin startproject myproject .

### Dockerコンテナの再起動
docker-compose down
docker-compose up -d --build

### 静的ファイルの収集
docker-compose run web python manage.py collectstatic

### データベースのマイグレーション
docker-compose run web python3 manage.py migrate

### Djangoのログを確認する
docker-compose logs web

### コンテナに入る
docker-compose exec web bash