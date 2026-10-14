# 📊 Meus Investimentos

Dashboard pessoal para acompanhar a evolução do patrimônio mês a mês, com cotação ao vivo de Bitcoin e Ethereum.

## Funcionalidades

- Registro mensal do valor de cada categoria (Reserva Emergencial, Renda Fixa, Ações, FIIs, Bitcoin, Ethereum, USDC e Outros)
- Variação de cada mês em R$ e % (verde = positivo, vermelho = negativo)
- Gráfico de evolução do patrimônio
- Cotação de Bitcoin e Ethereum em R$ e US$, atualizada a cada 30 segundos (CoinGecko API)
- Botão de dados de exemplo para explorar o painel
- Layout responsivo (celular, tablet e computador)
- Instalável como app (PWA) e funciona offline

## Tecnologias

- **HTML, CSS e JavaScript**, tudo em um único arquivo (`index.html`), sem build e sem instalar nada
- **React 18** carregado por CDN, com os componentes escritos em `React.createElement` (sem JSX)
- **PWA:** `manifest.webmanifest` e Service Worker (`sw.js`) para instalar o app e abrir offline
- **API:** [CoinGecko](https://www.coingecko.com/) para a cotação de Bitcoin e Ethereum
- **Armazenamento:** `localStorage`

## Estrutura

```
index.html            página, estilos e lógica
sw.js                 service worker (cache offline)
manifest.webmanifest  configuração do app instalável
icon-192.png          ícones do app
icon-512.png
```

## Privacidade

Os dados ficam salvos apenas no navegador de quem usa (`localStorage`). Nada é enviado a servidores.

## Como rodar

Sirva a pasta com qualquer servidor estático, por exemplo:

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000`.

## Demo

[Adicione aqui o link do deploy na Vercel]
