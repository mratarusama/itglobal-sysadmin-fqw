# itglobal-sysadmin-fqw

[Лист задания](task.md)

## Порядок запуска

1. Выгрузить репозиторий

```bash
git clone https://github.com/mratarusama/itglobal-sysadmin-fqw.git
cd ./itglobal-sysadmin-fqw
```

2. Изменение файла `inventory/inventory.yml`.

В файл "[инвертаризации](inventory/inventory.yml)" необходимо добавить адреса своих машин по аналогии с уже существующим файлом.

3. Запуск

  - Запустить весь плейбук

    ```bash
    ansible-playbook -i inventory playbook.yml
    ```

  - Запустить отдельную роль

    ```bash
    ansible-playbook -i inventory playbook.yml -t НАИМЕНОВАНИЕ_РОЛИ
    ```

Список доступных ролей:
- [Установка пакетов](roles/setup_packages/README.md) `setup_packages`
- [Создание пользователя](roles/create_user/README.md) `create_user`
- [Конфигурирование SSH](roles/configure_auth/README.md) `configure_auth`
- [Установка/конфигурирование Nginx](roles/configure_nginx/README.md) `configure_nginx`