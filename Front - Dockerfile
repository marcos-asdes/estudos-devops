#Nosso front roda em node, logo
FROM node:16 

#Vamos especificar para onde queremos trabalhar dentro do docker
WORKDIR /app 

#Agora queremos passar/copiar as coisas do front pra essa pasta acima
COPY . .
RUN npm i
RUN npm run build 
#Passamos, instalamos a node_modules e fazemos o build

RUN mkdir -p /var/www/html
#no mkdir, criamos uma pasta naquele caminho (-p cria se nao existir), caminho do nginx
RUN mv build/* /var/www/html
#Agora vamos mover (mv) tudo que estiver na pasta build para essa pasta do nginx que criamos

WORKDIR /
#Vamos voltar o 'terminal' para o inicio para rodar outro comando

RUN rm -rf /app
#Agora vamos deletar (rm) a pasta /app, a intenção era fazer o build, passar para o nginx e depois deletar o 'resto'