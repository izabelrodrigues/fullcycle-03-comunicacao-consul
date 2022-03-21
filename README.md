# Estudo service discovery consul

#### Todos os ips usados são ips temporários gerados por cada instância de máquina que foi inicializada no momento da execução

## Comandos importantes

### Inicializar máquinas
* De dentro do diretório raiz do projeto, execute o compando abaixo para inicializar as máquinas via docker-compose: 
```
docker-compose up -d
```
### Acessar o shell das máquinas
* Para acessar o shell de cada máquina execute *docker exec -it <nome_maquina> sh* . Exemplo da máquina consul-server-01:
```
docker exec -it consul-server-01 sh
```
### Instalação de ferramentas úteis:
-  bind-tools para dar acesso ao comando dig:
```
apk -U add bind-tools
```
-  tcpdump para analisar e capturar informações de pacotes:
```
apk add tcpdump
```
### Obter o ip da máquina ( a cada execução após um down nos containers é preciso obter os novos ips para substituir nos arquivos de configuração das máquinas)

```
ifconfig
```

### Criação dos diretórios usados nos consul agent em modo client

```
mkdir /var/lib/consul
```

