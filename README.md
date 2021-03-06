# docker-compose para execução dos microsserviços do projeto app-pet

### Repositórios dos microsserviços: <br>
**Users:** https://github.com/app-pet/users-api <br>
**Providers:** https://github.com/app-pet/providers-api

### Passo-a-passo para execução dos microsserviços utilizando conteineres docker:

- Clonar o repositório: <br>
> git clone https://github.com/app-pet/docker-compose.git

- Abrir o prompt de comando de sua preferência na pasta na qual o repositório foi clonado e executar os seguintes comandos: <br>
> cd docker-compose <br>
> docker network create -d overlay appPet  
> docker stack deploy -c docker-compose.yml apppet

- Com isso, os microsserviços **users** e **providers** estarão disponíveis nas portas **3000** e **3001**, respectivamente, em seu **localhost**. <br>
> **Users:** http://localhost:3000/api/users <br>
> **Providers:** http://localhost:3001/api/providers <br>
> **Front:** http://localhost:3030

- Swagger
> **Users:** http://localhost:3000/api-docs/ <br>
> **Providers:** http://localhost:3001/api-docs/ <br>

- Visualizer
> http://localhost:8080/

- Para verificar o status do cluster: <br>
> docker stack ps apppet

- Para encerrar a execução dos conteineres do projeto, utilize o comando: <br>
> docker stack rm apppet
