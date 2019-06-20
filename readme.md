:octocat: Os testes no servidor foram feitos utilizando o programa de teste Postman. 
O mesmo está configurado para aceitar os dados no formato JSON. :octocat:

Comando para efetuar um clone desse repositório:

```sh
https://github.com/Binotto/node-boilerplate-user-registration-v1.git

```

Instalar as dependencias:

```sh

npm install

```

Para iniciar o processo no modo de Desenvolvimento rode o comando abaixo:(O Nodemon está instalado como uma dependencia de desenvolvimento :D ):


```sh

npm run dev

```

{{url}}=localhost:3000

Rotas:

Adicionar um novo usuário:

```sh
POST: {{url}}/user
Example:
{
	"name": "Binotto",
	"email": "binottos@example.com",
	"password": "123teste"
}

```

Login
Necessário fazer o Login para iniciar a autenticação das outras rotas(Menos a da criação de usuário).
POST: {{url}}/users/login

```sh
Example:
{
	"email": "binottos@example.com",
	"password": "123teste"
}

```

Rota para autenticar o token de acesso retornando os dados do usuário

```sh
GET: {{url}}/users/me
```

Buscar os dados de um usuário em especifico

```sh
GET: {{url}}/3000/users/:id
Example:
{{url}}/users/5d02f5235753fd0cf2798837
```

Buscar a lista de usuários, deletados, não deletados, e também tem a paginação se for necessário:

```sh
GET: {{url}}/users/
GET /users?deleted=false or true
GET /users?limit=10&skip=20
```

Edita um usuário pelo id:

```sh
PATCH: {{url}}/users/:id
Example:
{{url}}/users/5d02f5235753fd0cf2798837
{
	"age": "25",
	"name": "Matheus Binotto - Back End Web Developer",
	"password": "123testando"
}
```

Edita o perfil do usuário, verificando pela autenticação:

```sh
PATCH: {{url}}/users/me
Example:
{
	"age": "25",
	"name": "Matheus Binotto - Full Stack Web Developer",
	"password": "123testando"
}
```

Remove um usuário pelo id:

```sh
DELETE: {{url}}/users/:id
Example:
{{url}}/users/5d02f5235753fd0cf2798837
```

Remove o usuário que está logado:

```sh
DELETE: {{url}}/users/me
```

Filtrar usuários com base em uma query passada pela url:

```sh
GET: {{url}}/users/filter/:name
Example:
{{url}}/users/filter/Matheus
```

Todas as requisições acima precisam ser autenticadas pelo token de acesso (com exceção da rota "/login").


Made by Matheus Binotto
```sh
https://www.linkedin.com/in/matheus-binotto-a51787143/

```




