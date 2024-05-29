# Docker部署mysql

tag：mysql



本文采用docker-compose的形式部署mysql，旨在学习、本地开发使用。



1、准备docker-compose.yml，内容如下

```yaml
version: '3.8'

services:
  mysql:
    image: mysql:8.0.37
    environment:
      MYSQL_ROOT_PASSWORD: 123456
      MYSQL_DATABASE: coder
      MYSQL_USER: coder
      MYSQL_PASSWORD: 123456
    ports:
      - "3306:3306"
    volumes:
      - ./data:/var/lib/mysql
```



2、创建docker容器。执行如下命令

```bash
docker-compose up -d
```

