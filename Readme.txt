Запуск nginx на удаленных серверах перечисленных в ansible/inventory.yaml
 - На удаленной машине используется логин root с правами sudo
 - Должен быть доступ по ssh

При переходе на http://167.99.41.253 показывает index.html, при любой другой картинку http://167.99.41.253/example

Запуск: ansible-playbook deploynginx.yml -i inventory.yaml


Структура:

Project
testtask_scorewarrior
.git
ansible
deploynginx.yml
inventory.yaml
nginx
conf
log
www
docker-compose.yml
Readme.txt
deploynginx.yml
inventory.yaml
Readme.txt
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
Запуск nginx на удаленных серверах перечисленных в ansible/inventory.yaml
 - На удаленной машине используется логин root с правами sudo
 - Должен быть доступ по ssh

При переходе на http://167.99.41.253 показывает index.html, при любой другой картинку http://167.99.41.253/example

Запуск: ansible-playbook deploynginx.yml -i inventory.yaml


Структура:
.
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
