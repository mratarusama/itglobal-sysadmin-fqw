# roles/create_user

В данной роли происходит создание пользователя и добавление ему прав администратора.

## Требования

Нет

## Переменные роли

- new_user_name: Имя создаваемого пользователя
  - Значение по умолчанию: `nginx`
= ssh_public_key_file: Название публичного SSH ключа, который будет добавлен к созданному пользователю.
  - Значение по умолчанию: `id_rsa.pub`

## Зависимости

Нет

## Пример запуска

```bash
ansible-playbook -i inventory playbook.yml -t create_user -e "new_user_name=dmitriy.semin"
```
