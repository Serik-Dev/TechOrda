# nginx-auth

### Задание

1. Настройте `server` блок, который слушает 8080 порт.
2. Установите `server_name` значению `example.com`.
3. Добавьте `location` блок для пути `/`, который обслуживает файл [index.html](https://stepik.org/media/attachments/lesson/686238/index.html)
4. Добавьте `location` блок для пути `/images`, который обслуживает файлы из архива [cats.zip](https://stepik.org/media/attachments/lesson/686238/cats.zip). Установите авторизованный вход для учетки: `design:SteveJobs1955`, т.е. логин `design`, пароль `SteveJobs1955`.
5. Добавьте `location` блок для пути `/gifs`, который обслуживает файлы из архива [gifs.zip](https://stepik.org/media/attachments/lesson/686238/gifs.zip). Установите авторизованный вход для учетки: `marketing:marketingP@ssword`.
6. Учетка `design` не должна иметь доступ на другие пути, тоже самое касается других учеток.

---
```
server {
    listen 8082;
    server_name example.com;

    # Обслуживание файла index.html на пути /
    location / {
        root /var/www/html/nginx-location;  # Замените на путь к каталогу с файлом index.html
        index index.html;
    }

    # Обслуживание файлов из /images
    location /images {
        alias /var/www/html/nginx-location/images;  # Замените на путь к извлеченному содержимому cats.zip
    	auth_basic "Password access /images";
	auth_basic_user_file /etc/nginx/conf.d/passwd_desing;
    }

    # Обслуживание файлов из /gifs
    location /gifs {
        alias /var/www/html/nginx-location/gifs;  # Замените на путь к извлеченному содержимому gifs.zip
    	auth_basic "Password access /images";
	auth_basic_user_file /etc/nginx/conf.d/passwd_marketing;
    }
		
}
```
