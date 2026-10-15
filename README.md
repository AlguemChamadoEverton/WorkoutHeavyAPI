# WorkoutHeavy

Aplicação web para montar e organizar rotinas de treino de musculação.
O usuário cria uma conta, cadastra exercícios e monta rotinas com eles.

Projeto pessoal de estudo, feito por Everton.

## O que dá pra fazer

- Criar conta e fazer login
- Cadastrar, listar e excluir exercícios
- Criar, editar e excluir rotinas de treino

Cada usuário só vê e altera os próprios exercícios e rotinas.

## Tecnologias

**Back-end** (este repositório)
- C# com ASP.NET Core 9 (Minimal API)
- Entity Framework Core com PostgreSQL
- Autenticação com JWT e senha guardada com hash (PasswordHasher)
- Documentação da API com Swagger e Scalar

**Front-end** (repositório WorkoutHeavyFront)
- HTML, CSS e JavaScript puro

## Endpoints principais

| Método | Rota | O que faz |
|---|---|---|
| POST | /register | Cria a conta |
| POST | /login | Faz login e devolve o token JWT |
| GET | /exercise | Lista os exercícios |
| POST | /exercise | Cadastra um exercício |
| DELETE | /exercise/{id} | Exclui um exercício |
| GET | /routine | Lista as rotinas |
| POST | /create-routine | Cria uma rotina |
| PUT | /edit-routine/{id} | Edita uma rotina |
| DELETE | /delete-routine/{id} | Exclui uma rotina |

## Como rodar

1. Ter o .NET 9 e o PostgreSQL instalados
2. Configurar a conexão com o banco no `appsettings.json`
3. Aplicar as migrations: `dotnet ef database update`
4. Rodar: `dotnet run`
5. Abrir o front-end (MeuPrimeiroFront) no navegador
