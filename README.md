# protheus-docker
Stack para criação de um ambiente Protheus em Linux com PostgreSQL para estudos/desenvolvimentos.

Vídeo: <a href="https://youtu.be/KMpcaNdLOVI" target="_blank">https://youtu.be/KMpcaNdLOVI</a>

Tempo total estimado para ambiente estar disponível: 20 minutos

Pré requisitos: Docker previamente instalado.

Como instalar Docker Desktop:
 - <a href="https://docs.docker.com/desktop/install/windows-install/" target="_blank">Windows</a>
 - <a href="https://docs.docker.com/desktop/install/linux-install/" target="_blank">Linux</a>
 - <a href="https://docs.docker.com/desktop/install/mac-install/" target="_blank">Mac</a>

Após realizada a instalação do Docker, baixar os arquivos necessários em: <a href="https://drive.google.com/file/d/1ssxFDbzeSKJOhdHfDncnZPulRvyu8RrJ/view?usp=sharing" target="_black">https://drive.google.com/file/d/1ssxFDbzeSKJOhdHfDncnZPulRvyu8RrJ/view?usp=sharing</a>

- 0 - Baixe os arquivos .env-sample e stack_protheus.yml, presentes neste repositório, clicando em "Code > Download ZIP" (caso possua git instalado, basta clonar este repositório com o comando: git clone https://github.com/lucascience/protheus-docker.git);
- 1 - Crie uma cópia do arquivo .env-sample chamada .env;
- 2 - Se necessário, edite o arquivo .env e altere as variáveis de ambiente. ATENÇÃO: Caso mude o nome do banco (DB_NAME), nome de usuário (DB_USER) ou senha (DB_PASS) no arquivo .env, as mesmas informações deverão ser replicadas no arquivo odbc.ini, presente na pasta odbc, em seus respectivos campos (username, password ou database);
- 3 - Descompacte o arquivo totvs.zip (baixado anteriormente);
- 4 - Abra um terminal (cmd, powershell, bash, etc);
- 5 - No terminal, execute o comando para criação da stack: docker compose -f stack_protheus.yml up -d (Neste ponto, o docker irá baixar as imagens necessárias, com tempo variável conforme a velocidade de sua conexão. No caso do vídeo, eu já possuia as imagens baixadas.);
- 6 - Após finalizado a execução do comando, abra um navegador e acesse a URL: <a href="http://localhost:8000" target="_blank">http://localhost:8000</a>
- 7 - Na tela que irá carregar, realize a configuração da empresa 99 - Teste (o tempo de execução dependerá do poder computacional);
- 8 - Após a finalização, basta utilizar o usuário e senha padrão: admin, sem senha.

Pronto! Você já tem o Protheus executando em containers para estudo e/ou desenvolvimentos.
