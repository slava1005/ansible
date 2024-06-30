###Установка clickhouse и vector

####Playbook:

- Загружается дистрибутивы указанные в group_vars
- Устанавливается clickhouse
- Запускает clickhouse-server
- Устанавливается vector на основе шаблонов
- Запускается vector
  
####Чтобы работал playbook:

- Необходимо предоставить доступы для работы ansible на хостах через ssh
- Добавить ip-адрес серверов в inventory
- Указать имя пользователя в inventory
- В файлах vars необходимо указать версии дистрибутивов

Запустить playbook:
```
$ ansible-playbook -i inventory/prod.yml site.yml
```
