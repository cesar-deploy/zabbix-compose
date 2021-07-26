# Instalação do zabbix 5.4 utilizando docker #
<img src="https://assets.zabbix.com/img/logo/zabbix_logo_500x131.png" width="200px">

## Descrição ##
Este script em shell, automatiza a instalação do zabbix server utilizando containers.

Pré requesitos:
<ul>
  <li>Docker Engine instalado (disponível em: https://docs.docker.com/engine/install/)</li>
  <li>Conhecimentos básicos em Docker (Comandos básicos como: docker run, exec, pull, network)</li>
  <li>Contato anterior com o sistema zabbix</li>
</ul>

Antes de realizar a execução do script é necessário criar um rede em modo bridge, para suportar os containers do zabbix: <br>
*docker network create rede-interna --subnet 172.16.0.0/29*

Após o dowload do script, devemos executa-lo com permissão de root (admin, no caso do windows): <br>
*sudo ./zabbix.docker-postegre.sh*

Após execução do comando o docker criará 4 containers, responsável pela execução do módulos do zabbix
<ul>
  <li>Zabbix Server</li>
  <li>Zabbix Frontend</li>
  <li>Postgres Server</li>
  <li>Zabbix Trapper</li>
</ul>

Agora é possível acessar a interface web do zabbix através do endereço: <br>
*localhost/zabbix*

Assim temos um servidor zabbix plenamente funcional, ideal para ambiente de hologação e testes. Também sendo possível usar esta abordagem em ambiente menores, com baixa disponibilidade de recursos.

Mais detalhes em: https://www.youtube.com/watch?v=BxkRc8R1t-M&t=13s
