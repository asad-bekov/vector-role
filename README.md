# Ansible Role: Vector

Роль устанавливает и настраивает [Vector](https://vector.dev/) для централизованного сбора логов.

## Переменные роли

| Переменная                | Описание                         | Значение по умолчанию   |
|-------------------------- |----------------------------------|-------------------------|
| vector_data_dir           | Директория данных Vector         | `/var/lib/vector`       |
| vector_source_type        | Тип источника логов              | `stdin`                 |
| vector_transform_type     | Тип трансформации                | `json_parser`           |
| vector_sink_type          | Тип приёмника логов              | `console`               |
| vector_codec              | Кодек для вывода                 | `json`                  |

## Пример использования

```yaml
- hosts: all
  roles:
    - role: vector-role
      vars:
        vector_source_type: "stdin"
        vector_sink_type: "console"
```

## Требования

- Debian/Ubuntu
