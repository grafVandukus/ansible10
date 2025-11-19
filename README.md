# Nginx Server Role

Ansible роль для установки и настройки веб-сервера Nginx.

## Требования

- Ansible 2.9+
- Docker (для тестирования)
- Python и pip

## Переменные роли

- `nginx_worker_processes`: количество worker процессов (по умолчанию: 1)
- `nginx_port`: порт для прослушивания (по умолчанию: 80)
- `nginx_root`: корневая директория (по умолчанию: /var/www/html)

