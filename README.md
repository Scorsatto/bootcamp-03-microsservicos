# Microsserviços

Sistema distribuído em microsserviços.

#### Tecnologias/bibliotecas abordadas:

- Spring boot
- Spring Cloud
- Eureka
- elasticsearch
- redis

------

#### Para rodar esta aplicação é necessário:

- Instalar e configurar o docker:
  - [Instalar Docker no Windows - Passo a Passo](https://youtu.be/sYsIoWtS5LY)
  - [Install Docker Desktop on Windows](https://docs.docker.com/desktop/windows/install/)
  - [Windows Subsystem for Linux Installation Guide for Windows 10](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- Após instalar o docker rodar o arquivo `docker-compose.yml` que esta na raiz do projeto, o mesmo irá baixar e configurar as imagens de banco de dados necessárias, ambas contem a configuração de limite de memória RAM para 1gb, para facilitar o deploy sem o consumo excessivo da mesma.
  - Comando: `docker-compose up`
- Abrir o projeto com a sua IDE predileta.
  - O primeiro modulo a ser executado é o `config-server` o mesmo é responsável por pegar os configurações para os demais módulos no github e posteriormente distribui-los.
  - O segundo modulo é o do `service-discovery` onde os demais serviços serão registrados.
  - Os demais módulos podem ser executados na ordem desejada.



