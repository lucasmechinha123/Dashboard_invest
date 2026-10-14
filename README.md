📊 Meus Investimentos

Dashboard pessoal para acompanhar a evolução do patrimônio mês a mês, com cotação ao vivo de criptomoedas.

Funcionalidades
Registro mensal do valor de cada categoria, com categorias personalizadas (adicionar, renomear e remover)
Exportação de planilha Excel (.xlsx) do mês, com aviso quando o mês termina
Variação de cada mês em R$ e % (verde = positivo, vermelho = negativo)
Gráfico de evolução do patrimônio
Cotação ao vivo de Bitcoin, Ethereum, BNB, Solana e USDC em R$ e US$, atualizada a cada 30 segundos (API pública da Binance), com opção de ocultar moedas
Botão de dados de exemplo para explorar o painel
Layout responsivo (celular, tablet e computador)
Instalável como app (PWA) e funciona offline
Tecnologias
HTML, CSS e JavaScript, tudo em um único arquivo (index.html), sem build e sem instalar nada
React 18 carregado por CDN, com os componentes escritos em React.createElement (sem JSX)
PWA: manifest.webmanifest e Service Worker (sw.js) para instalar o app e abrir offline
API: Binance (dados públicos de mercado) para as cotações
SheetJS carregado por CDN para gerar o arquivo Excel
Armazenamento: localStorage
Estrutura
index.html            página, estilos e lógica
sw.js                 service worker (cache offline)
manifest.webmanifest  configuração do app instalável
icon-192.png          ícones do app
icon-512.png
Privacidade

Os dados ficam salvos apenas no navegador de quem usa (localStorage). Nenhum valor digitado é enviado a servidores. O app só consulta a API da Binance para buscar as cotações.

Como rodar

Sirva a pasta com qualquer servidor estático, por exemplo:

bash
python -m http.server 8000

Depois abra http://localhost:8000.

Demo

https://dashboardinvest.vercel.app
