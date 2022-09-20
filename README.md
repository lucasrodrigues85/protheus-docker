# protheus-docker
Stack para criação de um ambiente Protheus em Linux com PostgreSQL para estudos/desenvolvimentos.

Pré requisitos: Docker previamente instalado.

Como instalar Docker Desktop:
 - Windows: https://docs.docker.com/desktop/install/windows-install/
 - Linux: https://docs.docker.com/desktop/install/linux-install/
 - Mac: https://docs.docker.com/desktop/install/mac-install/

Após realizada a instalação do Docker, baixar os arquivos necessários em: https://drive.google.com/file/d/1ssxFDbzeSKJOhdHfDncnZPulRvyu8RrJ/view?usp=sharing

- 1. Crie uma cópia do arquivo .env-sample chamada .env;
- 2. Se necessário, edite o arquivo .env e altere as variáveis de ambiente. ATENÇÃO: Caso mude o nome do banco (DB_NAME), nome de usuário (DB_USER) ou senha (DB_PASS) no arquivo .env, as mesmas informações deverão ser replicadas no arquivo odbc.ini, presente na pasta odbc, em seus respectivos campos (username, password ou database);
- 3. Descompacte o arquivo totvs.zip (baixado anteriormente);
- 4. Abra um terminal (cmd, powershell, bash, etc);
- 5. No terminal, execute o comando para criação da stack: docker compose -f stack_protheus.yml up -d (Neste ponto, o docker irá baixar as imagens necessárias, com tempo variável conforme a velocidade de sua conexão. No caso do vídeo, eu já possuia as imagens baixadas.);
- 6. Após finalizado a execução do comando, abra um navegador e acesse a URL: http://localhost:8000
- 7. Na tela que irá carregar, realize a configuração da empresa 99 - Teste (o tempo de execução dependerá do poder computacional);
- 8. Após a finalização, basta utilizar o usuário e senha padrão: admin, sem senha.

Pronto! Você já tem o Protheus executando em containers para estudo e/ou desenvolvimentos.
