Тестовое задание ansible+nginx+compose
--------------------------------------
>  Запуск nginx на удаленных серверах перечисленных в inventory.yaml.
>  На удаленной машине нужен sudo.
>  Должен быть доступ по ssh.

При переходе в [корень](http://167.99.41.253) показывает картинку, при любой другой ссылке [index.html](http://167.99.41.253/example)

Запуск:

      ansible all -m ping -i inventory.yml -e @secrets_file.enc --vault-password-file password_file --limit test,prod
      ansible-playbook -i inventory.yml -e @secrets_file.enc --vault-password-file password_file playbook.yml --limit test,prod

Vault:
      Пароль для vault'a лежит password_file, пароль от sudo лежит в secrets_file.


Структура:


    ├── Readme.md
    ├── ansible
    │   ├── inventory.yml
    │   ├── password_file
    │   ├── playbook.yml
    │   └── secrets_file.enc
    └── nginx
        ├── conf
        │   ├── example.com.bak
        │   └── example.conf
        ├── docker-compose.yml
        ├── log
        └── www
            ├── cats.jpg
            └── index.html
