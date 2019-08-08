## mariadb
```
# yum install -y mariadb mariadb-server mariadb-devel(mysqlclient needed)
# systemctl enable mariadb; systemctl start mariadb
# mysql -u root -p
```

## create database
```
MariaDB [(none)]> DROP DATABASE polls;
MariaDB [(none)]> CREATE DATABASE polls CHARACTER SET UTF8;

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'polls',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': 'localhost',
        'PORT': '',
    }
}
```
## user
```
# python manage.py createsuperuser --email admin@example.com --username admin
# python manage.py makemigrations snippets
# python manage.py migrate
# python manage.py runserver
```
```
# cat mysite/polls/schema.sql 
INSERT INTO polls_question
VALUES 
  (1, 'sgao hansome?', '2019-06-28 02:47:24.000000');

INSERT INTO polls_choice
VALUES 
  (1, 'yes', 0, 1),
  (2, 'no', 0, 1);

MariaDB [(none)]> source mysite/polls/schema.sql
```
