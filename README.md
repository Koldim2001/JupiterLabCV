# JupiterLabCV
### Готовый сервис JupiterLab для разработок в сфере компьютерного зрения:

1) Тежелый образ, в котором имеется сразу TF и PyTorch с доступом к GPU:

```
docker-compose -f docker-compose-gpu-torch-tf.yml -p jupiter_lab_cv up -d --build
```

2) Более легкий образ, в котором имеется сразу PyTorch с доступом к GPU:

```
docker-compose -f docker-compose-gpu-torch.yml -p jupiter_lab_cv up -d --build
```

3) Самый легкий образ без доступа к GPU (CPU лишь имеется)

```
docker-compose -f docker-compose-cpu.yml -p jupiter_lab_cv up -d --build
```


---

### Получение токена чтобы авторизоваться и создать пароль в среде JupiterLab:
```
docker exec jupiterlab jupyter server list
```