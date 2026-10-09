# Bài 5 - Khởi chạy dịch vụ với Docker Compose

## Nội dung docker-compose.yml
```yaml
services:
  web:
    image: nginx:alpine
    ports:
      - "8082:80"
```

## 1. Khởi chạy dịch vụ: docker compose up -d
```
```

## 2. Kiểm tra dịch vụ: docker compose ps
```
NAME        IMAGE          COMMAND                  SERVICE   CREATED          STATUS          PORTS
ex5-web-1   nginx:alpine   "/docker-entrypoint.…"   web       29 seconds ago   Up 28 seconds   0.0.0.0:8082->80/tcp, [::]:8082->80/tcp
```

## 3. Kiểm tra web: curl http://localhost:8082
```
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, nginx is successfully installed and working.
Further configuration is required for the web server, reverse proxy, 
API gateway, load balancer, content cache, or other features.</p>

<p>For online documentation and support please refer to
<a href="https://nginx.org/">nginx.org</a>.<br/>
To engage with the community please visit
<a href="https://community.nginx.org/">community.nginx.org</a>.<br/>
For enterprise grade support, professional services, additional 
security features and capabilities please refer to
<a href="https://f5.com/nginx">f5.com/nginx</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```
