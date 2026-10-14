<div align="center">

# 📊 Meus Investimentos

**Dashboard pessoal para acompanhar o patrimônio mês a mês, com cotação de criptomoedas ao vivo.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React_18-61DAFB?logo=react&logoColor=black)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?logo=pwa&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)

### 🔗 [Ver o projeto funcionando](https://dashboardinvest.vercel.app)

</div>

<!-- Para mostrar uma imagem do painel: salve um print como screenshot.png na raiz do projeto e remova os comentários da linha abaixo.
<p align="center"><img src="screenshot.png" alt="Painel do Meus Investimentos" width="800"></p>
-->

## 💡 Sobre

Um painel simples e rápido para registrar quanto você tem em cada investimento a cada mês e enxergar a evolução ao longo do tempo. Fundo preto, **verde** para o que subiu e **vermelho** para o que caiu.

Foi feito como projeto de portfólio: sem backend, sem build e sem instalação. É só abrir a página.

## ✨ Funcionalidades

**Controle mensal**
- Registro mês a mês: você digita quanto entrou em cada categoria e o valor é somado ao mês anterior (use sinal de menos para saídas ou quedas)
- Categorias iniciais: Reserva Emergencial, Bitcoin, Ethereum e USDC
- Categorias personalizadas: adicione, renomeie e remova as suas (Tesouro, Ouro, Dólar, o que quiser)
- Calendário para escolher o mês, com marcação dos meses já registrados
- Variação de cada mês em R$ e %, em verde ou vermelho

**Visualização**
- Patrimônio atual e variação do último mês
- Resumo por categoria com ▲ e ▼
- Gráfico de evolução do patrimônio
- Botão de dados de exemplo para explorar o painel sem digitar nada

**Cripto ao vivo**
- Bitcoin, Ethereum, BNB, Solana e USDC em R$ e US$, com variação de 24h
- Atualização automática a cada 30 segundos, usando a API pública da Binance
- Opção de ocultar as moedas que você não quer ver

**Excel**
- Exporta uma planilha `.xlsx` do mês (por categoria, com variação) e uma aba com todo o histórico
- Aviso automático quando um mês termina, oferecendo o download

**App**
- Responsivo: celular, tablet e computador
- Instalável como app (PWA) e funciona offline
- Confirmações dentro da própria tela, sem caixas de diálogo do navegador

## 🚀 Como usar

1. Abra o [site](https://dashboardinvest.vercel.app) (ou clique em **Carregar dados de exemplo** para ver como funciona).
2. Em **Registrar mês**, escolha o mês no calendário.
3. Digite quanto entrou em cada categoria. Campo vazio não muda nada.
4. Toque em **Salvar mês**. O patrimônio, o gráfico e o histórico se atualizam.
5. No **Histórico**, use **⬇ Excel** para baixar a planilha de qualquer mês.

> A variação mostrada inclui o dinheiro novo que você colocou. Se você investir R$ 500 e nada render, o painel mostra +R$ 500.

## 🛠️ Tecnologias

| Tecnologia | Uso |
|---|---|
| HTML, CSS e JavaScript | Tudo em um único arquivo (`index.html`), sem build |
| React 18 (via CDN) | Componentes e estado, escritos com `React.createElement` (sem JSX) |
| Binance API (pública) | Cotações ao vivo; o preço em R$ é calculado pelo par USDT/BRL |
| SheetJS (via CDN) | Geração do arquivo Excel no navegador |
| Service Worker + Manifest | Instalação como app e uso offline |
| `localStorage` | Armazenamento dos dados no próprio navegador |

## 📁 Estrutura

```
index.html            página, estilos e lógica do app
sw.js                 service worker (atualização e cache offline)
manifest.webmanifest  configuração do app instalável
icon-192.png          ícones do app e da aba do navegador
icon-512.png
```

## 💻 Como rodar localmente

Não precisa instalar nada. Sirva a pasta com qualquer servidor estático:

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000`.

## 📲 Instalar como app

No Chrome ou no Edge, abra o site e clique no ícone de instalar na barra de endereço (ou menu → **Instalar página como app**). No celular, use **Adicionar à tela inicial**.

## 🔒 Privacidade

Os valores que você digita ficam salvos **apenas no navegador do seu dispositivo** (`localStorage`). Nenhum valor é enviado a servidores. O app só consulta a API da Binance para buscar as cotações.

Como não há backup nem login, limpar os dados do navegador apaga o histórico, e os dados não aparecem em outros aparelhos.

## 🧭 Ideias para o futuro

- [ ] Sincronização entre aparelhos, com login e banco de dados
- [ ] Meta da reserva emergencial com barra de progresso
- [ ] Gráfico de distribuição por categoria
- [ ] Separar aporte e rendimento no cálculo da variação

## 👤 Autor

Feito por [@lucasmechinha123](https://github.com/lucasmechinha123).
https://dashboardinvest.vercel.app/
