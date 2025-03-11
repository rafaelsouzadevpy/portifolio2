#monitoramentoveiculos
# 🚗 Monitoramento de Veículos com Python & FastAPI

## 📌 Visão Geral
Este projeto é uma API para monitoramento de veículos, desenvolvida com **Python** e **FastAPI**. O sistema permite cadastrar, listar, atualizar e deletar veículos, além de fornecer informações sobre cada um.

## 🚀 Tecnologias Utilizadas
- **Python** 3.10+
- **FastAPI**
- **SQLAlchemy** (para interação com banco de dados)
- **SQLite** (pode ser substituído por outro banco, como PostgreSQL)
- **Uvicorn** (servidor ASGI para rodar a API)
- **Pydantic** (para validação de dados)

## 📂 Estrutura do Projeto
```
monitoramento-veiculos/
│-- app/
│   │-- main.py  # Arquivo principal da API
│   │-- models.py  # Modelos do banco de dados
│   │-- schemas.py  # Definição dos esquemas Pydantic
│   │-- database.py  # Configuração do banco de dados
│   │-- routes/
│   │   │-- vehicles.py  # Rotas para CRUD de veículos
│-- tests/
│   │-- test_vehicles.py  # Testes para API
│-- requirements.txt  # Dependências do projeto
│-- README.md  # Documentação do projeto
```

## ⚙️ Como Configurar o Projeto
### 1️⃣ Clonar o repositório
```bash
git clone https://github.com/seu-usuario/monitoramento-veiculos.git
cd monitoramento-veiculos
```

### 2️⃣ Criar e ativar um ambiente virtual
```bash
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
```

### 3️⃣ Instalar as dependências
```bash
pip install -r requirements.txt
```

### 4️⃣ Rodar a API
```bash
uvicorn app.main:app --reload
```
A API ficará disponível em `http://127.0.0.1:8000`.

## 🔥 Endpoints da API
### Criar um veículo
```http
POST /vehicles/
```
**Body (JSON):**
```json
{
  "placa": "ABC-1234",
  "marca": "Toyota",
  "modelo": "Corolla",
  "ano": 2022
}
```

### Listar veículos
```http
GET /vehicles/
```

### Buscar um veículo por ID
```http
GET /vehicles/{id}
```

### Atualizar um veículo
```http
PUT /vehicles/{id}
```

### Deletar um veículo
```http
DELETE /vehicles/{id}
```

## ✅ Testes
Para rodar os testes automatizados:
```bash
pytest tests/
```

## 📜 Licença
Este projeto está sob a licença MIT.

