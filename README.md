# sergeikhrustalev_infra
sergeikhrustalev Infra repository

1.  Основное задание

Целевая команда:

    ssh -A  -J appuser@62.84.126.118 appuser@10.128.0.32

2. Дополнительное задание

Создаем конфигурационный файл ~/.ssh/config  вида:

    Host bastion
      HostName 62.84.126.118
      User appuser
      IdentityFile ~/.ssh/appuser

    Host someinternalhost
      HostName 10.128.0.32
      User appuser
      ProxyJump bastion

Подключаемся так:

    ssh someinternalhost


Конфигурация vpn

    bastion_IP = 62.84.126.118
    someinternalhost_IP = 10.128.0.32

