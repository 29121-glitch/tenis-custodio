# API de Tenis- WebAPI

Está é uma API RESTful desenvolvida para o gerenciamento de informações de tenis, utilizando **pythom** e **flask**. A API permite criar, ler, atualizar e excluir tenis, com validação dos dados utilizando a biblioteca **Joi**.

Este é um projeto inicial de CRUD (Create, Read, Update, Delete),que será expandido no futuro. Este é apenas o escopo inical.

## Funcionalidades

- **GET /**: Retorna a lista completa de tenis.
- **POST /**: Adiciona um novo tenis à lista.
- **PUT /:sigla**: Atualiza as informações de um tenis específico, identificado pela sigla.
- **DELETE /:sigla**: Remove um tenis específico pela sigla.

## Estrutura do Projeto

- **app.py**: Arquivo principal que configura o servidor Express e as rotas da API.
- **tenis_controllers.py**: Contém a lista de tenis (dados fictícios).
- **tensi_models.py**: Contém as validações Joi para os dados dos tenis.
- **tenis_routes.py**
**db.py**
## Endpoints

### 1. **GET /**

Retorna a lista completa de tenis disponíveis.

#### Exemplo de Resposta:

```json
[{
  "marca": "Nike",
  "modelo": "Air Force 1 '07",
  "tamanho": 42
},
{
  "marca": "Nike",
  "modelo": "Air Max 90",
  "tamanho": 41
}
]
```
### 2. **GET /:sigla**

Retorna as informações de um tenis específico, identifado pela sigla.

### Exemplo de Requisição:

`GET /FER`

### Exemplo de Resposta:

```json
{
  "marca": "Nike",
  "modelo": "Dunk Low Retro",
  "tamanho": 43
}
```
### 3. **POST /**

Adiciona um novo tenis à lista.

#### Exemplo de Requisição:

`POST \`

**Content-Type:** application/json

```json
{
  "marca": "Nike",
  "modelo": "Air Jordan 1 Mid",
  "tamanho": 44
}
```

#### Exemplo de Resposta:

```json
{
  "marca": "Nike",
  "modelo": "Blazer Mid '77 Vintage",
  "tamanho": 40
}
```

### 4. **PUT /:sigla**

Atualiza as informações de um tenis específica.

#### Exemplo de Requisição:

`PUT /FK`

**Content-Type:** application/json

```json
{
  "tamanho": "41"
}
```

#### Exemplo de resposta:

```json
{
  "marca": "Nike",
  "modelo": "React Infinity Run Flyknit 3",
  "tamanho": 42
}
```

### 5. **DELETE /:sigla**

Remove um tenis específica pela sigla.

#### Exemplo de Requisição:

`DELETE /FK`

#### Exemplo de Resposta:

```json
{
  "marca": "Nike",
  "modelo": "ZoomX Vaporfly Next% 2",
  "tamanho": 41
}
```

## Como Rodar o Projeto

1. **Clone este repositório:**

  ```bash
  git clone https://github.com/mariaeduarda883/musica.vscode.git
  ```

2. **Instale as dependências:**

  Navegue até o diretório do projeto e execute o comando:

  ```bash
  npm install
  ```
3. **Inicie o servidor**
  Após a instalação das dependências, inicie o servidor:

  ```bash
  node ./app.js
  ```
4. **Acesse a API**

A API está disponível em [http://localhost:3000]

## Validações 

Os dados enviados para API são validados com **Joi** para garantir que todos os campos sejam fornecidos corretamente. As validações incluem:

- O nome do tenis deve ter pelo menos 3 caracteres.
- A Sigla deve ter exatamente 3 caracteres.
- O marca, modelo e tamanho devem ser números válidos.
- Durante a atualização, pelo menos um campo precisa ser fornecido.

Dicas:
https://dillinger.io/ - Para ler a formatação na Web, antes de subir no Git
https://readme.so/pt/editor - Para fazer "Automatico" somente editando

## Autor

Desenvolvido por Gabriel Custódio e Murilo Neto 