# Nginx bazasından istifadə edirik
FROM nginx:latest

# Statik faylları konteynerə kopyalayırıq
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Nginx konfiqurasiyasını kopyalayırıq (default olanı əvəz edirik)
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf