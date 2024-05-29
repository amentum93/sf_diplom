**Конфигурация терраформа для выделения облачных ресурсов**

- провайдер: yandex.cloud
- 3 виртуальные машины: 
    - 4 ядра/4 гб RAM/30 гб HDD
    - ubuntu 22.04 lts (образ - из cloud.marketplace, free version)
- сеть:
    - публичные и внутренние ip-адреса (подсеть - subnet-1)
- метаданные:
    - файл "config-cloud" содержит необходимую информацию для создания дополнительного пользователя внутри ВМ

**Порядок исполнения**
- установка terraform 
- установка и настройка yandex CLI
- получение параметров service-account-key.json (от yandex.cloud) 
- исполнение файла main.tf (terraform plan -> terraform apply)