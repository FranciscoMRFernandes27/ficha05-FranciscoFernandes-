Ficha 5 – Redes de Comunicação

App React que vai buscar as cartas a um server Express, através de uma API em JSON. A app também permite acrescentar cartas através de um formulário, e o server guarda-as em `cartas.json`.

Como correr

São precisos dois terminais.

Terminal 1 (server):

```bash
cd server
npm install
npm run dev
```

O server fica em http://localhost:3000.

Terminal 2 (client):

```bash
cd client
npm install
npm run dev
```

A app fica em http://localhost:5173.

API

| Método | URL | O que recebe | O que responde |
| --- | --- | --- | --- |
| GET | `/api/cartas` | nada | a lista de cartas, com status 200 |
| GET | `/api/cartas/aleatoria` | nada | uma carta escolhida ao acaso, com status 200 |
| POST | `/api/cartas` | JSON com `name`, `type` e `attack` | a carta criada, com status 201 |

O POST responde 400 com uma mensagem de erro quando a carta não tem nome ou tipo.
