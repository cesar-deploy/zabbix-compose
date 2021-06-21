#Configurções iniciais

Necessário possuir docker-cli instalado
https://docs.docker.com/docker-for-windows/install/

Após instalação do dokcer, é necessário criar uma rede interna do tipo bridge para hospedar os container criados. Neste caso optei por um /29
# docker network create rede-interna --subnet 172.16.0.0/29

Após a criação da rede virtual, iremos copiar o conteúdo da pasta do git contendo script de instlação dos containers
# git clone https://github.com/Italo-Roberto/zabbix-docker.git

Com os arquivos na máquina local, iremos executar o script
# ./zabbix.docker-postegre.sh

Com isso teremos o zabbix server com todas suas funcionalidades disponível para acesso atráves do ip de loopback
# 127.0.0.1/zabbix
Com as credenciais:
Usuário: Admin
senha: zabbix

