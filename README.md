# demo_scripts
Repositório para dockerização da aplicação demo

-Para rodar o app é necessário ter acesso aos demais repos:

- API Externa (ASP .NET): [Repositório da API](https://github.com/Brunogomes97/demo_api)
-  O Frontend da aplicação, pode ser acessada por aqui: [demo_app](https://github.com/Brunogomes97/demo_app)

```text
demo_app/
demo_scripts/
demo_api/
```

## ⚙️ Pré-requisitos
Antes de começar, você vai precisar ter instalado:

* ✅ .NET SDK 8.0+
* ✅ Docker
* ✅ Docker Compose
* NodeJs


Tendo a estrutura em mesmo nivel de diretório temos:


### Clonando o Repositório

```bash
git clone https://github.com/Brunogomes97/demo_app.git
git clone https://github.com/Brunogomes97/demo_api.git
git clone https://github.com/Brunogomes97/demo_scripts.git
```


### Montando compose

```bash
 cd demo_scripts
 docker-compose up --build
```

### Atualizando migrations
- É fundamental atualizar as migrações do banco antes de testar o app

```bash
 cd demo_api
 dotnet ef database update --project src/project.API
```

- O app estará disponivel em http://localhost:3002
- A api está disponivel com o swagger em http://localhost:5014/swagger/index.html
  
