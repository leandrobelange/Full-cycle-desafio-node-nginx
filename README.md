# Full-cycle-desafio-node-nginx
Repositorio para armazenar os arquivos do desafio Docker do curso Full Cycle 3.0 docler com nginx


Desafio: Nginx, Nodejs e Mysql

Neste desafio coloquei em prática o que aprendi em relação a utilização do nginx como proxy reverso, além de poder aplicar todo o conhecimento que obtive quanto à utilização do docker, docker-compose, volumes, etc.

Como executar

    Faça o clone do projeto
    Acesse a pasta onde o projeto se encontra
    Execute com docker-compose up -d

O que ele faz?

Cria 3 containers:

    app - aplicação desenvolvida em nodejs
    db - banco de dados mysql
    nginx - que servirá de proxy reverso, recebendo as chamadas na porta 8080 e redirecionando para a aplicação e depois devolvendo a resposta para o usuário no navegador.

Conceito

A idéia principal é que quando um usuário acessar o nginx na porta 8080, este último fará uma chamada em nossa aplicação nodejs que roda na porta 3000. Essa aplicação por sua vez adicionará um registro (name: Leandro Belange) em nosso banco de dados mysql, cadastrando um nome na tabela people.

O retorno da aplicação nodejs para o nginx deverá ser:
Full Cycle Rocks!

    Lista de nomes cadastrada no banco de dados.
basta rodar: "docker-compose up -d" que tudo deverá estar funcionando e disponível na porta: 8080.
