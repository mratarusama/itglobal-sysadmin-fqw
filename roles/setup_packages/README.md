# roles/setup_packages

В данной роли происходит обновление всех и установка новых программ.

## Требования

Нет

## Переменные роли

- `packages` (list): Список наименований программ, которые необходимо установить
  - Значение по умолчанию:
    - mc
    - htop
    - atop
    - ncdu

## Зависимости

Нет

## Пример запуска

```bash
ansible-playbook -i inventory playbook.yml -t setup_packages -e "{'packages': ['mc','cowsay','htop']}"
```
