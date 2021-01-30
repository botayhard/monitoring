steps:
1. clone
2. edit ./masterhost/config/prometheus.yml and ./masterhost/nginx/grafana.conf
3. run `docker run -it --rm --name certbot_new -v "$(pwd)/certbot/conf:/etc/letsencrypt" -v "$(pwd)/certbot/www:/var/www/certbot" -p 80:80 certbot/certbot certonly`
4. run `docker-compose up -d`
