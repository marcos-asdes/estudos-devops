#Criamos as configurações no outro arquivo, agora vamos criar o container com o docker

FROM nginx:1.15.0

#Vai rodar a imagem acima e rodar um comando: deletar (rm) o arquivo default.conf - fazemos isso pq queremos usar o nosso conf
RUN rm /etc/nginx/conf.d/default.conf
#Agora vamos passar nosso arquivo para essa pasta:
COPY nginx.conf /etc/nginx/conf.d
