# docker-centos7-nginx

NGINX running on CentOS 7 preconfigured to work along with PHP-FPM image.


Map the output port number:

```yaml
  ports:
    - "8080:80"
```


Mount the root folder and the virtual host configuration file:

```yaml
  volumes:
    - ./src/public:/var/www/public
    - ./src/vhost.conf:/etc/nginx/conf.d/vhost.conf
```


Link to the PHP-FPM server:

```yaml
  links:
    - php
```

