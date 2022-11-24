
Для проверки первого этапа реализована возможность локально развернуть проект с заполненными тестовыми данными:

```
git clone https://github.com/Ivan-Grebennikov/foodgram-project-react.git
```

```
cd foodgram-project-react
```

Перейти в папку, содержащую файлы для развертывания проекта:

```
cd infra
```

Создать файл ``` .env ```, содержащий значения переменных среды для развертывания проекта:

```
touch .env
```

Заполнить файл ``` .env ``` по образцу:

```
DJANGO_SECRET_KEY='django-insecure-wvmy15xk2o9&5&$*%uopxvf%j3o9%0y7jtpx+$_!#ll7xug$pw' # приватный ключ Django
```

Ключ ``` DJANGO_SECRET_KEY ``` можно сгенерировать с помощью сервиса https://djecrety.ir/

Значение ключа при заполении файла ``` .env ``` стоит обернуть в кавычки.

Запустить скрипт для локального развертывания проекта:

```
./deploy.sh
```

Проект будет запущен по локальному адресу:

http://localhost/

Для доступа в админ-зону проекта необходимо перейти по адресу:

http://localhost/admin/

На данном этапе проект будет заполнен следующими тестовыми данными:

В системе зарегистрировано 3 пользователя

1) user-one@yandex.ru
2) user-two@yandex.ru
3) user-three@yandex.ru

Пароль для входа в учетные записи: Kzs4RDNya2EK49T

Для входа в админ зону необходимо воспользоваться учетной записью

Логин: admin
Пароль: 1234567890

Для остановки работы проекта необходимо выполнить команду:

```
sudo docker compose down -v
```
