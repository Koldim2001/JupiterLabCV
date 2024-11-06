# JupiterLabCV
### Готовый сервис JupiterLab для разработок в сфере компьютерного зрения:


Для начала склонируйте репозиторий на свой компьютер. После клонирования откройте терминал и перейдите в директорию с репозиторием. 

Далее вам нужно выбрать один из трех вариантов установки и выполнить соответствующую команду. После установки запустите команду, которая сгенерирует вам токен. Скопируйте полученный токен.

Затем перейдите в браузере по адресу http://localhost:8789. На этой странице вы сможете создать свой собственный пароль, используя скопированный токен. После этого ресурс с JupiterLab будет доступен вам по адресу http://localhost:8789, и вы сможете использовать его с созданным паролем.

---
### Запуск сервиса JupiterLab:

1) Тежелый образ, в котором имеется сразу TensorFlow и PyTorch с доступом к GPU:

```
docker-compose -f docker-compose-gpu-torch-tf.yml -p jupiter_lab_cv up -d --build
```

2) Более легкий образ, в котором имеется сразу PyTorch с доступом к GPU:

```
docker-compose -f docker-compose-gpu-torch.yml -p jupiter_lab_cv up -d --build
```

3) Самый легкий образ без доступа к GPU (CPU лишь имеется):

```
docker-compose -f docker-compose-cpu.yml -p jupiter_lab_cv up -d --build
```


---

### Получение токена чтобы авторизоваться и создать пароль в среде JupiterLab:
```
docker exec jupiterlab jupyter server list
```

---

### Туториал по настройке Linux сервера
Помимо туториала по установке и запуску JupiterLab в репозитории содержится инструкция по настройке Linux сервера, которая поможет вам установить следующие компоненты: NVIDIA драйверы, CUDA Toolkit, Docker, NVIDIA Container Toolkit и Git. 

Инструкция находится в файле [**server_setup.md**](https://github.com/Koldim2001/JupiterLabCV/blob/main/server_setup.md). Следуя этой инструкции, вы сможете легко настроить ваш сервер для работы с GPU и другими необходимыми инструментами.
