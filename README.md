## document
- [django_exercise 설명](#django_exercise-설명)
- [django_exercise説明](#django_exercise説明)
- [how to use django_exercise](#how-to-use-django_exercise)

## django_exercise 설명
django_exercise는 장고(django)를 이용하여 웹 서비스를 제작하고 헤로쿠(Heroku)에 배포(Deploy)하는 과정을 정리한 저장소(Repository)입니다. 이 저장소(Repository)를 제작하면서 작성한 블로그가 있습니다. 자세한 내용은 아래에 링크를 통해 확인하시기 바랍니다.

- [장고(django) 설치하기](https://dev-yakuza.github.io/ko/django/installation/)
- [장고(django) 프로젝트 시작하기](https://dev-yakuza.github.io/ko/django/start/)
- [장고(django) 모델(models) 사용해보기](https://dev-yakuza.github.io/ko/django/models/)
- [장고(django)의 관리자 페이지](https://dev-yakuza.github.io/ko/django/admin/)
- [장고(django)의 라우팅(Routing)](https://dev-yakuza.github.io/ko/django/routing/)
- [장고(django)의 ORM](https://dev-yakuza.github.io/ko/django/orm/)
- [장고(django)의 뷰(View)](https://dev-yakuza.github.io/ko/django/view/)
- [장고(django)의 폼(Form)](https://dev-yakuza.github.io/ko/django/form/)
- [장고(django) 프로젝트를 헤로쿠(heroku)에 업로드하기](https://dev-yakuza.github.io/ko/django/heroku/)

### 사용 방법
아래에 명령어를 통해 django_exercise 저장소(Repository)를 복사(Clone)합니다.

```bash
git clone https://github.com/dev-yakuza/django_exercise.git
```

아래에 명령어로 파이썬 가상 환경을 생성합니다.

```bash
virtualenv venv
```

아래에 명령어로 파이썬 가상 환경을 실행합니다.

```bash
source venv/bin/activate
```

아래에 명령어로 프로젝트에 필요한 모듈을 설치합니다.

```bash
pip install -r requirements.txt
```

데이터베이스 연동을 위해 `django_exercise/settings.py`를 열고 아래의 내용을 자신의 DB에 맞게 수정합니다.

```python
...
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django_exercise',  # DB name
        'USER': 'root',  # DB account
        'PASSWORD': '',  # DB account's password
        'HOST': '127.0.0.1',  # DB address(IP)
        'PORT': '3306',  # DB port(normally 3306)
    }
}
...
```

아래에 명령어로 데이터베이스를 생성합니다.

```bash
# python manage.py makemigrations
python manage.py migrate
```

아래에 명령어로 장고(django) 관리자를 생성합니다.

```bash
python manage.py createsuperuser
```

아래에 명령어로 테스트서버를 실행합니다.

```bash
python manage.py runserver
```

아래에 링크를 통해 프로젝트를 확인할 수 있습니다.

- 일반 페이지: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- 관리자 페이지: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

## django_exercise説明
django_exerciseはジャンゴ(django)を使ってウェブサービスを作成してヘロク(Heroku)へデプロイ(Deploy)するプロセスを纏めたレポジトリ(Repository)です。このレポジトリ(Repository)を作る時、作成したブログがあります。もっと詳し内容は下記のリンクで確認できます。

- [ジャンゴ(django)インストール](https://dev-yakuza.github.io/django/installation/)
- [ジャンゴ(django)のプロジェクト開始](https://dev-yakuza.github.io/django/start/)
- [ジャンゴ(django)のモデル(models)の使い方](https://dev-yakuza.github.io/django/models/)
- [ジャンゴ(django)の管理者ページ](https://dev-yakuza.github.io/django/admin/)
- [ジャンゴ(django)のルーティング(Routing)](https://dev-yakuza.github.io/django/routing/)
- [ジャンゴ(django)のORM](https://dev-yakuza.github.io/django/orm/)
- [ジャンゴ(django)のビュー(View)](https://dev-yakuza.github.io/django/view/)
- [ジャンゴ(django)のフォーム(Form)](https://dev-yakuza.github.io/django/form/)
- [ジャンゴ(django)プロジェクトをヘロク(Heroku)へアップロードする](https://dev-yakuza.github.io/django/heroku/)

### 使い方
下記のコマンドでdjango_exerciseレポジトリ(Repository)をコピー(Clone)します。

```bash
git clone https://github.com/dev-yakuza/django_exercise.git
```

下記のコマンドでパイソン仮想環境を作ります。

```bash
virtualenv venv
```

下記のコマンドでパイソンの仮想環境を実行します。

```bash
source venv/bin/activate
```

下記のコマンドでプロジェクトに必要なモジュールをインストールします。

```bash
pip install -r requirements.txt
```

データベースを連動するため、`django_exercise/settings.py`を開いて下記の内容を自分のDBに合わせて修正します。

```python
...
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django_exercise',  # DB name
        'USER': 'root',  # DB account
        'PASSWORD': '',  # DB account's password
        'HOST': '127.0.0.1',  # DB address(IP)
        'PORT': '3306',  # DB port(normally 3306)
    }
}
...
```

下記のコマンドでデーターベースを生成します。

```bash
# python manage.py makemigrations
python manage.py migrate
```

下記のコマンドでジャンゴ(django)の管理者を生成します。

```bash
python manage.py createsuperuser
```

下記のコマンドでテストサーバーを起動します。

```bash
python manage.py runserver
```

下記のリンクを使ってプロジェクトを確認します。

- ウェブページ: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- 管理者ページ: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

## how to use django_exercise
django_exercise is the repository about django web service for deploying Heroku service. there are blog posts about this repository. if you want to know more details, see the link below.

- [django installation](https://dev-yakuza.github.io/en/django/installation/){:target="_blank"}
- [Start django Project](https://dev-yakuza.github.io/en/django/start/){:target="_blank"}
- [Use Models in django](https://dev-yakuza.github.io/en/django/models/){:target="_blank"}
- [django Administrator Page](https://dev-yakuza.github.io/en/django/admin/){:target="_blank"}
- [django Routing](https://dev-yakuza.github.io/en/django/routing/){:target="_blank"}
- [django ORM](https://dev-yakuza.github.io/en/django/orm/){:target="_blank"}
- [django View](https://dev-yakuza.github.io/en/django/view/){:target="_blank"}
- [django Form](https://dev-yakuza.github.io/en/django/form/){:target="_blank"}
- [Upload django project to Heroku](https://dev-yakuza.github.io/en/django/heroku/)

### How to use
execute the command below to clone the django_exercise repository.

```bash
git clone https://github.com/dev-yakuza/django_exercise.git
```

execute the command below to start python virtual environment.

```bash
virtualenv venv
```

execute the command below to execute python virtual environment.

```bash
source venv/bin/activate
```

execute the command below to install modules for the project.

```bash
pip install -r requirements.txt
```

you need to modify `django_exercise/settings.py` to connect your database like below.

```python
...
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django_exercise',  # DB name
        'USER': 'root',  # DB account
        'PASSWORD': '',  # DB account's password
        'HOST': '127.0.0.1',  # DB address(IP)
        'PORT': '3306',  # DB port(normally 3306)
    }
}
...
```

execute the command below to migrate.

```bash
# python manage.py makemigrations
python manage.py migrate
```

execute the command below to create django administrator.

```bash
python manage.py createsuperuser
```

execute the command below to start django test server.

```bash
python manage.py runserver
```

click the links below to check the project.

- Web page: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- Administrator page: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)