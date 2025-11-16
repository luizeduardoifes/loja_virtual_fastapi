# 🛒 LojaVirtual - FastAPI

Projeto educacional desenvolvido com o professor de programação **Ricardo Maroquio** com objetivo de aprender **FastAPI**, aplicações de banco de dados e conceitos de negócio com rotas de back-end.

## 📚 Objetivos de Aprendizado

✅ Aprender **FastAPI** - framework web moderno para Python  
✅ Integração com **Banco de Dados** - CRUD operations  
✅ Desenvolvimento de **Backend** - APIs RESTful  
✅ Conceitos de **Rotas** - mapeamento de endpoints HTTP  
✅ **Arquitetura em Camadas** - separação de responsabilidades  
✅ Conceitos de **Negócio** - modelagem de domínio

---

## 📁 Estrutura do Projeto

```
PW20251_LojaVirtual/
│
├── 📄 main.py                    # Ponto de entrada da aplicação
├── 📄 README.md                  # Este arquivo
├── 📄 requirements.txt           # Dependências do projeto
├── 📄 pytest.ini                 # Configuração de testes
├── 📄 .coveragerc                # Cobertura de testes
│
├── 📂 models/                    # Camada de Modelos
│   ├── categoria.py              # Modelo de Categoria
│   ├── endereco.py               # Modelo de Endereço
│   ├── produto.py                # Modelo de Produto
│   └── usuario.py                # Modelo de Usuário
│
├── 📂 sql/                       # Camada SQL (Queries)
│   ├── categoria_sql.py          # Queries de Categoria
│   ├── endereco_sql.py           # Queries de Endereço
│   ├── produto_sql.py            # Queries de Produto
│   └── usuario_sql.py            # Queries de Usuário
│
├── 📂 repo/                      # Camada de Repositório
│   ├── categoria_repo.py         # Repositório de Categoria
│   ├── endereco_repo.py          # Repositório de Endereço
│   ├── produto_repo.py           # Repositório de Produto
│   └── usuario_repo.py           # Repositório de Usuário
│
├── 📂 templates/                 # Camada de Apresentação (HTML)
│   ├── index.html                # Página inicial
│   ├── categorias.html           # Página de categorias
│   ├── produtos.html             # Página de produtos
│   └── usuarios.html             # Página de usuários
│
├── 📂 data/                      # Dados Iniciais
│   ├── categorias.sql            # Script SQL de categorias
│   ├── produtos.sql              # Script SQL de produtos
│   └── usuarios.sql              # Script SQL de usuários
│
└── 📂 tests/                     # Testes Unitários
    ├── test_categoria.py         # Testes de Categoria
    ├── test_produto.py           # Testes de Produto
    └── test_usuario.py           # Testes de Usuário
```

---

## 🏗️ Arquitetura em Camadas

### 1️⃣ Camada de Modelos (`models/`)
Define as estruturas de dados que representam as entidades do negócio:
- **Categoria**: Classificação de produtos
- **Produto**: Itens disponíveis na loja
- **Usuário**: Clientes da plataforma
- **Endereço**: Dados de entrega

### 2️⃣ Camada SQL (`sql/`)
Contém as consultas SQL (queries) para operações no banco de dados:
- CREATE, READ, UPDATE, DELETE
- Operações específicas do negócio

### 3️⃣ Camada de Repositório (`repo/`)
Implementa a lógica de acesso aos dados:
- Comunica-se com o banco de dados
- Valida dados antes de persistir
- Trata erros e exceções

### 4️⃣ Camada de Rotas (`main.py`)
Define os endpoints FastAPI:
- Recebe requisições HTTP
- Chama métodos do repositório
- Retorna respostas em JSON

### 5️⃣ Camada de Apresentação (`templates/`)
Interface web para interação com o usuário:
- HTML/CSS/JavaScript
- Consome as APIs do backend

---

## 🚀 Fluxo de Funcionamento

```
┌─────────────┐
│ Requisição  │
│   HTTP      │
└──────┬──────┘
       │
       ▼
┌─────────────────────────┐
│ FastAPI (main.py)       │
│ ├─ Rotas                │
│ └─ Controllers          │
└──────┬──────────────────┘
       │
       ▼
┌─────────────────────────┐
│ Camada Repositório      │
│ (repo/)                 │
└──────┬──────────────────┘
       │
       ▼
┌─────────────────────────┐
│ Camada SQL (sql/)       │
│ ├─ SELECT               │
│ ├─ INSERT               │
│ ├─ UPDATE               │
│ └─ DELETE               │
└──────┬──────────────────┘
       │
       ▼
┌─────────────────────────┐
│ Banco de Dados          │
└──────┬──────────────────┘
       │
       ▼
┌─────────────────────────┐
│ Response JSON           │
└─────────────────────────┘
```

---

## 🔧 Instalação e Execução

### Pré-requisitos
- Python 3.8+
- pip (gerenciador de pacotes)

### Passos

1. **Clone o repositório**
```bash
git clone <url-do-repositorio>
cd PW20251_LojaVirtual-main
```

2. **Crie um ambiente virtual**
```bash
python -m venv venv
venv\Scripts\activate
```

3. **Instale as dependências**
```bash
pip install -r requirements.txt
```

4. **Execute a aplicação**
```bash
uvicorn main:app --reload
```

5. **Acesse a aplicação**
- Frontend: `http://localhost:8000`
- API Docs: `http://localhost:8000/docs`

---

## 🧪 Testes

Execute os testes unitários:
```bash
pytest
```

Com cobertura:
```bash
pytest --cov=.
```

---

## 📚 Conceitos de Negócio

### Entidades Principais

- **Usuário**: Cliente que compra na loja
- **Produto**: Item disponível para compra
- **Categoria**: Agrupamento de produtos
- **Endereço**: Local de entrega do pedido

### Rotas Principais

- `GET /categorias` - Listar categorias
- `GET /produtos` - Listar produtos
- `POST /usuarios` - Criar novo usuário
- `GET /usuarios/{id}` - Obter dados do usuário

---

## 👨‍🏫 Desenvolvimento

Desenvolvido com o professor **Ricardo Maroquio** como projeto educacional para aprender:
- Arquitetura em camadas
- FastAPI
- Integração com banco de dados
- Conceitos RESTful
- Modelagem de negócio

---

## 📝 Licença

Este projeto é para fins educacionais.

