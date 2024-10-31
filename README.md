# JupiterLabCV
Готовый сервис JupiterLab для разработок в сфере компьютерного зрения


```
docker-compose -f docker-compose-gpu-torch-tf.yml -p traffic_analyzer up -d --build
```

Как получить токен чтобы авторизоваться и создать пароль в среде Jupiter:
```
docker exec jupiterlab jupyter server list
```