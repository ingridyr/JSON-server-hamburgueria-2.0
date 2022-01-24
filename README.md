<p align="center">
    Essa "fake-API" foi desenvolvida para o projeto Kenzie-burguer 2.0
</p>

<p align="center">
   Url base da API: https://kenzie-burguer2.herokuapp.com/
</p>

<h2 align ='center'> Listagem de usuários </h2>

<blockquote>
  O usuário <b>logado</b> pode ver os demais usuários já cadastrados na plataforma, podemos acessar a lista dessa forma:
</blockquote>

<blockquote>
  Obs: não possui corpo de requisição, mas nessecita do token no headers para acesso.
</blockquote>

`GET /users - FORMATO DA RESPOSTA - STATUS 200`

```json
[
  {
    "email": "ingridy@mail.com",
    "password": "$2a$10$e2O7OmB0iVb.tJvcRV5kG.Zq8R9QVVUbksqe7rd7rPMgOo7iO5GXW",
    "name": "ingridy",
    "id": 1
  }
]
```

<h2 align ='center'> Cadastro de um novo usuário </h2>

`POST /register - FORMATO DA REQUISIÇÃO:`

```json
{
  "email": "kenzinho@mail.com",
  "password": "123456",
  "name": "Kenzinho"
}
```

`POST /register - FORMATO DA RESPOSTA - STATUS 201:`

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImtlbnppbmhvQG1haWwuY29tIiwiaWF0IjoxNjQzMDMxNDA5LCJleHAiOjE2NDMwMzUwMDksInN1YiI6IjIifQ.KhUQUWdYJ3sNGGehJgQaLtEBqhaG1zNOsUuYtlYH1Nw",
  "user": {
    "email": "kenzinho@mail.com",
    "name": "Kenzinho",
    "id": 2
  }
}
```

<h2 align ='center'> Login </h2>

`POST /login - FORMATO DA REQUISIÇÃO:`

```json
{
  "email": "ingridy@mail.com",
  "password": "123456"
}
```

`POST /register - FORMATO DA RESPOSTA - STATUS 200:`

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImluZ3JpZHlAbWFpbC5jb20iLCJpYXQiOjE2NDMwMzEzNjQsImV4cCI6MTY0MzAzNDk2NCwic3ViIjoiMSJ9.-ZpZEy_ZkpyDjizo8JEZF6gRIfOKMS6yWBHfdVGTSN4",
  "user": {
    "email": "ingridy@mail.com",
    "name": "ingridy",
    "id": 1
  }
}
```

<h2 align ='center'> Consultar lista de produtos: </h2>

<blockquote>
  O usuário logado pode ver a lista de produtos.
  Obs: não possui corpo de requisição, mas nessecita do token no headers para acesso.
</blockquote>

`GET /products - FORMATO DA RESPOSTA - STATUS 200:`

```json
[
  {
    "title": "Hamburguer",
    "category": "Sanduíches",
    "price": 14,
    "image": "https://i.ibb.co/R3M9m3R/Hamburguer.png",
    "id": 1
  },
  {
    "title": "X-Burguer",
    "category": "Sanduíches",
    "price": 16,
    "image": "https://i.ibb.co/G9JgTXk/X-Burguer.png",
    "id": 2
  },
  {
    "title": "Big Kenzie",
    "category": "Sanduíches",
    "price": 18,
    "image": "https://i.ibb.co/HGZYpmK/Big-Kenzie.png",
    "id": 3
  },
  {
    "title": "Combo Kenzie",
    "category": "Combos",
    "price": 26,
    "image": "https://i.ibb.co/Qj339P4/Combo-Kenzie.png",
    "id": 4
  },
  {
    "title": "Fanta Guaraná",
    "category": "Bebidas",
    "price": 5,
    "image": "https://i.ibb.co/Y21PRDt/Fanta-Guarana.png",
    "id": 5
  },
  {
    "title": "Coca Cola",
    "category": "Bebidas",
    "price": 7,
    "image": "https://i.ibb.co/ZKQqLYS/Coca-Cola.png",
    "id": 6
  },
  {
    "title": "McShake Ovomaltine",
    "category": "Sobremesas",
    "price": 10,
    "image": "https://i.ibb.co/qsG2Nqr/Mc-Shake-Ovomaltine.png",
    "id": 7
  },
  {
    "title": "Sunday Chocolate",
    "category": "Sobremesas",
    "price": 10,
    "image": "https://i.ibb.co/x83GRSN/Sunday-Ovomaltine.png",
    "id": 8
  }
]
```
