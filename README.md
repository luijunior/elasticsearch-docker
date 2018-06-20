
# README #

Este repositorio possui dados para uso do Elasticsearch para estudo e desenvolvimento
https://www.elastic.co
A Stack aqui é o logstash/elasticsearch/kibana

### Como utilizar ###

### Elasticsearch

Baixar e instalar [docker](https://docs.docker.com/install/)
	
Baixar e instalar [docker-compose](https://docs.docker.com/compose/install/)
	
Executar o arquivo docker-compose

```bash
	docker-compose up
```

Na pasta logstash/pipeline estão os arquivos que serão transformados em pipeline do logstash, é importante adaptar para a configuração da sua aplicação para correto funcionamento, verificar este [link](https://www.elastic.co/guide/en/logstash/current/configuration-file-structure.html)

No arquivo docker-compose.yaml é importante adaptar a linha de volumes para incluir o diretório dos logs de sua aplicação
```bash
#Trecho original
volumes:
      - ./logstash/pipeline/:/usr/share/logstash/pipeline/
      - ./elastic-sample-logs/:/logs/

#Trecho com diretorio da minha aplicação
volumes:
      - ./logstash/pipeline/:/usr/share/logstash/pipeline/
      - ./minha-aplicacao/logs/:/logs/
```

### Com que falar ###
Luiz Antonio Guimaraes Junior
* luizlagj@gmail.com
* luizgj@ipiranga.com.br