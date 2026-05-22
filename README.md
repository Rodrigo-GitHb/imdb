# IMDb Project

Projeto para consulta e manipulação de dados de filmes e séries a partir do IMDb (Internet Movie Database).  
Esse repositório pode conter scripts, APIs e/ou ferramentas para buscar informações sobre filmes, notas, gêneros, lançamentos, etc.

---

## Objetivo

- Facilitar a busca de informações de filmes e séries (títulos, notas, gêneros, ano, etc.).
- Servir como base para integrações (dashboards, scripts de automação, etc.).
- Aprender e testar consumo de APIs (ex: TMDb, IMDb data, ou similares) e boas práticas de código.

---

## Tecnologias utilizadas

- Linguagem principal: `Python` (ou outra, se for o caso — ajuste aqui).
- Bibliotecas comuns: `requests`, `pandas` (opcional), `tqdm` (opcional), etc.
- (Se usar) Banco de dados: `SQLite` / `PostgreSQL` / `MongoDB`.
- (Se usar) Framework web: `Flask` / `FastAPI`.

---

## Instalação e configuração

1. Clone o repositório:
   ```bash
   git clone https://github.com/Rodrigo-GitHb/imdb.git
   cd imdb
   ```

2. Crie um ambiente virtual (recomendado):
   ```bash
   python -m venv venv
   source venv/bin/activate    # Linux / macOS
   # ou
   venv\Scripts\activate       # Windows
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

4. Configure tokens de API (se necessário).  
   Copie o arquivo de exemplo:
   ```bash
   cp .env.example .env
   ```
   E edite `.env` com suas chaves (ex: `API_KEY=...`).

---

## Como usar

Execute o script principal ou a API:

```bash
python main.py
# ou, se for API:
python app.py
```

Se for uma API, acesse:
- `http://localhost:5000` (ou a porta configurada).

Exemplos de uso:
- Buscar por título:
  - `http://localhost:5000/search?title=The+Dark+Knight`
- Listar filmes por nota mínima:
  - `http://localhost:5000/movies?min_rating=7.5`

(Testes e exemplos específicos devem ser ajustados conforme o que seu código realmente faz.)

---

## Testes

Executar testes:

```bash
python -m pytest tests/
```

---

## Estrutura de arquivos

```txt
imdb/
├── main.py           # Script principal
├── api/              # Módulo da API (se houver)
├── models/           # Modelos de dados
├── utils/            # Funções utilitárias
├── tests/            # Testes automatizados
├── requirements.txt  # Dependências
├── .env.example      # Exemplo de variáveis de ambiente
