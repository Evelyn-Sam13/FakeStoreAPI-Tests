# Fake Store API - Testes

Este projeto é de estudo e laboratório de **testes automatizados de API** utilizando a Fake Store API com **Postman**.  
O objetivo é praticar operações comuns de API, como login, listagem de produtos, busca por ID e criação de produtos.

Projeto de estudo e prática de **testes de API** utilizando a Fake Store API com **Postman** (JSON, API REST).


---

## Casos de Teste

| ID   | Descrição                                   | Método | Endpoint       | Entrada                                                                                         | Resultado Esperado                              | Status HTTP |
|------|--------------------------------------------|--------|----------------|-------------------------------------------------------------------------------------------------|------------------------------------------------|-------------|
| TC01 | Login com credenciais corretas retorna token JWT | POST   | /auth/login    | `{ "username": "mor_2314", "password": "83r5^_" }`                                            | Token JWT válido no body                        | 200         |
| TC02 | Login com credenciais incorretas retorna erro   | POST   | /auth/login    | `{ "username": "mor_2314", "password": "senhaErrada" }`                                       | Mensagem de erro                                | 401 ou 403  |
| TC03 | Listar todos os produtos retorna lista não vazia | GET    | /products      | -                                                                                               | Array de produtos com pelo menos 1 item        | 200         |
| TC04 | Buscar produto existente por ID retorna dados corretos | GET    | /products/1    | ID = 1                                                                                          | Objeto com campos `title`, `price`, `category`| 200         |
| TC05 | Adicionar produto                           | POST   | /products      | `{ "title": "Produto Teste", "price": 50, "description": "Descrição teste", "image": "https://i.pravatar.cc", "category": "eletronics" }` | Produto criado com sucesso                      | 200         |

---

## Ferramentas Utilizadas

- [Postman](https://www.postman.com/)  
- **Collection Runner** para automação dos testes

---

## Observações

- Todos os testes foram feitos **apenas para estudo e aprendizado**.  
- Nenhuma alteração em ambiente de produção é realizada.  
- O projeto é inicial e voltado para iniciantes em **testes de API**.

---


