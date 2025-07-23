# API de Busca de Produtos com N8N

> **Desenvolvido por**: Lázaro Claudino  
> **Projeto**: Automação de API para busca de produtos  
> **Tecnologias**: N8N, Docker, JavaScript  

## 📋 Sobre o Projeto

Este projeto demonstra a criação de uma API REST usando N8N (ferramenta de automação) que permite buscar produtos em um arquivo JSON através de requisições HTTP POST.

## 📡 Como Usar a API

### Endpoint
```
POST http://localhost:5678/webhook/api/buscar-produtos
```

### Exemplo de Requisição
```json
{
  "termo": "açaí"
}
```

### Exemplo de Resposta
```json
{
  "possiveis_produtos": {
    "termo_pesquisado": "açaí",
    "qtde": 2,
    "produtos_encontrados": [
      {
        "codigo": "68799as",
        "descricao": "ACAI 200ML NATURAL COM GUARANA C/9"
      },
      {
        "codigo": "12345",
        "descricao": "AÇAÍ POLPA CONGELADA 1KG"
      }
    ]
  }
}
```

## 🐳 Instalação e Execução

### Pré-requisitos
- Docker Desktop instalado
- PowerShell ou CMD

### Passos para executar:

1. **Clone/baixe o projeto**
2. **Execute o comando:**
   ```bash
   docker-compose up -d
   ```
3. **Acesse o N8N:** http://localhost:5678
4. **Importe o workflow** usando o arquivo JSON fornecido
5. **Teste a API** com Postman ou curl

### Credenciais padrão:
- **Usuário**: admin
- **Senha**: admin123

## 🧪 Testando com Postman

1. Crie uma requisição POST
2. URL: `http://localhost:5678/webhook/api/buscar-produtos`
3. Header: `Content-Type: application/json`
4. Body: `{"termo": "produto desejado"}`