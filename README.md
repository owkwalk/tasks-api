# tasks-api

ローカルにて、python 実行環境「my-venv」を構築する。

```
% python3 -m venv my-venv
```

python 実行環境「my-venv」を起動する。

```
% source my-venv/bin/activate
```

pip を最新にし、python 実行環境「my-venv」内に、必要なパッケージをインストールする。

```
% pip install --upgrade pip
% pip install django==3.0.7 djangorestframework==3.10 djangorestframework-simplejwt==4.6.0 django-cors-headers djoser
```

マイグレーションを実行する。
（マイグレーションファイルはすでに作成済み）

```
% python manage.py migrate
```

スーパーユーザーを作る。

```
% python manage.py createsuperuser
Email:
Password:
```

ローカルサーバーを起動する。

```
% python manage.py runserver
```