Запуск nginx на удаленных серверах перечисленных в ansible/inventory.yaml
 - На удаленной машине используется логин root с правами sudo
 - Должен быть доступ по ssh

При переходе на http://167.99.41.253 показывает index.html, при любой другой картинку http://167.99.41.253/example

Запуск: ansible-playbook deploynginx.yml -i inventory.yaml


Структура:
├── Readme.txt
├── ansible
│   ├── deploynginx.yml
│   └── inventory.yaml
├── docker-compose.yml
└── nginx
    ├── conf
    │   └── example.conf
    ├── log
    └── www
        ├── cats.jpg
        └── index.html
