Учебная роль для установки Vector
=========

Выполняет установку Vector указанной версии.

Требования
------------

Предназначена для запуска на CentOS. Проверялась на CentOS 7.

Переменные роли
--------------

- vector_version - версия Vector
- vector_minor_version - минорная версия Vector, обычно 1

| Переменная | Тип     | Описание                                |
|------------|---------|-----------------------------------------|
| vector_version           | string  | Номер версии в формате SemVer, например 0.22.3 |
| vector_minor_version           | integer | минорная версия Vector, обычно 1 |


Зависимости
------------

Нет.

Пример playbook
----------------


    - name: Install Vector
      hosts: vector
      remote_user: centos
      tags: vector
      roles:
        - vector


