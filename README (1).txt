API de Livros com Flask

Essa é uma API simples feita em Python usando Flask para gerenciar uma lista de livros.
Ela permite criar, ler, atualizar e deletar livros.

Tecnologias usadas:
- Python 3.12
- Flask

Endpoints:

1. Obter todos os livros
GET /livros
Resposta:
[
  {
    "id": 1,
    "titulo": "O Senhor dos Anéis - A Sociedade do Anel",
    "autor": "J.R.R Tolkien"
  },
  ...
]

2. Obter um livro por ID
GET /livros/<id>
Exemplo: /livros/1
Resposta:
{
  "id": 1,
  "titulo": "O Senhor dos Anéis - A Sociedade do Anel",
  "autor": "J.R.R Tolkien"
}

3. Criar um novo livro
POST /livros
Corpo da requisição (JSON):
{
  "id": 4,
  "titulo": "Nome do Livro",
  "autor": "Autor"
}
Resposta: Lista de livros atualizada.

4. Editar um livro por ID
PUT /livros/<id>
Corpo da requisição (JSON):
{
  "titulo": "Novo Título",
  "autor": "Novo Autor"
}
Resposta: Livro atualizado.

5. Deletar um livro por ID
DELETE /livros/<id>
Resposta: Lista de livros atualizada.

Como rodar o projeto:
1. Clone o repositório:
   git clone https://github.com/SEU_USUARIO/meu-flask-api.git
   cd meu-flask-api

2. Instale o Flask (recomenda-se usar um ambiente virtual):
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\Scripts\activate     # Windows
   pip install Flask

3. Rode o servidor:
   python app.py

4. A API estará disponível em http://localhost:5000

Observações:
- Os dados são armazenados apenas em memória. Ao reiniciar o servidor, quaisquer livros adicionados ou alterados serão perdidos.
- Para persistência, é necessário integrar com um banco de dados ou salvar os dados em um arquivo JSON.
