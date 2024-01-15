# docker-compose for nginx-proxy-manager
> This needs : [dockerhost](https://github.com/ariadata/dockerhost-sh)
---
#### 1- Create nginx-proxy-manager bridge network :
```sh
docker network create nginx-proxy-manager
```
#### 2- Clone this repo and pull it's docker images:
```sh
git clone https://github.com/mohajer-hos/dc-nginxproxymanager.git nginx-proxy-manager && cd nginx-proxy-manager && rm -rf .git && docker-compose pull
```
#### 3- Run docker-compose file by using :
```sh
docker-compose up -d
```
#### 4- Goto : 
>  `http://YOUR-IP:8181`
>  
Use these credentials to first login and change it after logged in :

User : `admin@example.com`

Pass : `changeme`

Done!

#### Other Useful Tips! :
> for being behind another nginx, use these in parent nginx config
```conf
proxy_ssl_name $host;
proxy_ssl_server_name on;
```
