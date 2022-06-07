# Docker Tutorial
# docker ps
  lista coteiners ativos
# docker ps -a
  lista todos os conteineres
# docker run hello-world
  caso a imagem docker não exista será baixada e executada.
# docker run -it ubuntu bash
  caso a imagem ubunto não exista será baixada o objetivo desse comado e rodar a imagem e executar o bash do conteiner. O -i -t vai me permitir executar comando no bash. 
# docker run -it -d ubuntu bash
  caso a imagem ubunto não exista será baixada o objetivo desse comado e rodar a imagem e executar o bash do conteiner. O -i -t vai me permitir executar comando no bash. 
  -d não deixará o terminal travado.
# docker run -d -p 80:80 --name meuconteiner nginx
  caso a imagem nginx não exista será baixada o host conseguirá acessar a porta do conteiner e o nome será meuconteiner.
# docker exec -it meuconteiner bash
  executara o bash do meuconteiner. exec serve peara executar ações dentro do conteiner.
# docker rm -f nginx
  remove o conteiner o -f é para o caso de o conteiner está ativo.
# docker rm $(docker ps -aq) -f
  remove todos os conteires por id inclusivo os ativos.
# sudo docker cp nginx:/usr/share/nginx/html/index.html .
Copiar contetudo do conteiner para o host, nginx é o nome do conteiner
https://stackoverflow.com/questions/22049212/docker-copying-files-from-docker-container-to-host

# docker run -d --name meuconteiner -p 80:80 -v ~/fullcycle/curso_docker/modul01/html/:/usr/share/nginx/html nginx
# docker run -d --name nginx -p 80:80 --mount type=bind,source="$(pwd)"/html,target=/usr/share/nginx/html nginx
 compartilhar arquivo local com o conteiner.
