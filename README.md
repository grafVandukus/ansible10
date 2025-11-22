Скриншоты по заданию находятся в соответствующей папке



Ansible роль для установки и настройки веб-сервера Nginx.

## Требования

- Ansible 2.13+
- Docker (для Molecule)
- Тестируемые системы:
  - Ubuntu 22.04 (Jammy)
  - Debian 11 (Bullseye)

## Переменные роли

- `nginx_worker_processes` — количество worker-процессов nginx (по умолчанию: `"auto"`)
- `nginx_port` — порт для прослушивания HTTP (по умолчанию: `80`)
- `nginx_root` — корневая директория сайта (по умолчанию: `/var/www/html`)
- `nginx_user` — пользователь nginx (по умолчанию: `www-data`)
- `nginx_package_name` — имя пакета nginx
- `nginx_conf_path` — путь к основному конфигурационному файлу nginx

## Пример использования

```yaml
- name: Install nginx via role
  hosts: web
  become: true
  roles:
    - role: nginx-server
      vars:
        nginx_port: 8080
        nginx_root: /var/www/myapp
