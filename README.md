# sergeikhrustalev_infra
sergeikhrustalev Infra repository

bastion_IP = 51.250.10.188
someinternalhost_IP = 10.128.0.27

Способ подключения
ssh -i ~/.ssh/appuser -J admin@51.250.10.188 admin@10.128.0.27

testapp_IP = 51.250.7.24
testapp_port = 9292

Packer:
Сделал все по инструкции, однако сначала образ собирался с ошибкой
Could not get lock /var/lib/dpkg/lock-frontend - open (11: Resource temporarily unavailable)

Чтобы предотвратить ее возникновение, добавил sleep 20 в скрипт  install_ruby.sh

Terraform:
Установил  terraform
Описал вм в файле main.tf
Описал output и input переменные в файлах output.tf и input.tf
Задал значения переменных в файле terraform.tfvars

