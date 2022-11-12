Тестовое задание ansible+nginx+compose
--------------------------------------
> Запуск nginx на удаленных серверах перечисленных в ansible/inventory.yaml.
> На удаленной машине используется логин root с правами sudo.
> Должен быть доступ по ssh.

При переходе в [корень](http://167.99.41.253) показывает index.html, при другой ссылке [картинку](http://167.99.41.253/example)

Запуск:

      ansible-playbook deploynginx.yml -i inventory.yaml

Структура:

    ├── Readme.txt
    ├── ansible
    │   ├── deploynginx.yml
    │   └── inventory.yaml
    └── nginx
        ├── conf
        │   └── example.conf
        ├── docker-compose.yml
        ├── log
        └── www
            ├── cats.jpg
            └── index.html
