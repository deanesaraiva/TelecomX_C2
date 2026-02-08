![Banner](assets/banner.png)

<h1 align="center">📊teste</h1>

<p align="center">
Modelo de Machine Learning para identificar clientes com risco de cancelamento.
</p>

<br>
<h1 tabindex="-1">Challenge TelecomX</h1>
<p>O objetivo deste projeto é fazer uma análise dos fatores que levaram a empresa a enfrentar um alto índice de cancelamentos(Churn), identificando categorias com maiores índices de Churn e padrões que possam /n
contribuir para prever ou reduzir a saída dos futuros clientes. Ao analisar os dados, serviços e comportamentos, busco gerar insights acionáveis para ações de retenção./n
Este é um projeto feito para o curso de Especialização em Data Science, do Alura Latam em parceria com o Programa ONE (Oracle Next Education). 

<br>
<h1 align="left" tabindex="-1">Tecnologias utilizadas:</h1>
<ul>
<li>Python: A linguagem de programação central para o desenvolvimento do projeto.</li>
<li>Pandas: Para a manipulação, e organização estruturada dos dados das lojas analisadas. </li>
<li>Matplotlib: Biblioteca com representações visuais dos dados, facilitando a identificação de padrões e insights. </li>
<li>Google COLAB: Plataforma onde o usuário pode fazer o download, reeditar e salvar o Notebook criado com o código completo, texto explicativo e visualizações que embasaram o relatório final.</li>
</ul>
<br>
<h1 align="left" tabindex="-1">Tratamento de Dados:</h1>
<div>
  <ul>
    <li>Os dados foram importados de um arquivo JSON e convertidos para DataFrames do pandas para facilitar a manipulação.</li>
    <li>As principais etapas incluíram:</li>
      <ul>
        <li>Normalização de estruturas aninhadas (ex.: customer, internet, phone, account)</li>
        <li>Padronização de colunas</li>
        <li>Tratamento de valores ausentes</li>
        <li>Conversão de tipos: ajuste de colunas numéricas (ex.: tenure, Charges.Monthly, Charges.Total).</li>
      </ul>
  </ul>
</div>

<br>
<h1 align="left">📊Analise:</h1> 
<div>
  <p>
    <img  height="300" alt="Contract x Churn" src="https://github.com/deanesaraiva/TelecomX/blob/main/grafico_prop_clientes.png" />
    <img  height="300" alt="Contract x Churn" src="https://github.com/deanesaraiva/TelecomX/blob/main/grafico_perfil.png" />
</p>

<li>Dos 7266 contratos ativos, 1869 cancelaram. Desse nicho percebeu-se que:</li>
<ol>
  <li>O gênero, dependentes e parcerias não influenciam no índice de cancelamento </li>
  <li>Clientes mais novos tendem a cancelar contrato mais vezes </li>
  <li>O índice de cancelamento é muito maior em clientes com pouco tempo de contrato ativo</li>
  <li>Fibra Ótica e Eletronick Check, categoria InsternetService e Método de Pagamento, respectivamente, são os mais impactantes em relação ao Churn</li>
  <li>Contratos Mensais tem maior risco de evasão</li>
</ol>

<br>
<img  height="300" alt="Contract x Churn" src="https://github.com/deanesaraiva/TelecomX/blob/main/grafico_tenure.png" />
<img  height="300" alt="Métodos de pagamento" src="https://github.com/deanesaraiva/TelecomX/blob/main/grafico_perfil_clientes.png" />
</br>
</div>

<br>
<h1 align="left">💡Recomendacao final:</h1>
<div>
<li>Como clientes com pouco tempo de contrato apresentam maior índice de churn, isso indica uma possível falha na fase inicial do relacionamento.</li>
  <br>
 <ol>Sugestões de ações:
  <li>Implementar programas de onboarding estruturados, com comunicações claras sobre benefícios, serviços disponíveis e canais de suporte;</li>
  <li>Estratégias de retenção devem focar nos primeiros meses de contrato;</li>
  <li>Oferecer benefícios temporários, como upgrades ou descontos iniciais;</li>
  <li>Incentivos à migração de contrato (mensal → anual/bianual)</li>
 </ol>
</div>

<br>
<h2 align="left">👉Instruções para acessar o Relatório</h2>
<div>
Abra o repositório no GitHub → Clique no arquivo Analise-do-Comportamento-do-Churn.pdf → Faça o download ou abra no seu navegador.

<br>
<h2 align="left">👉Instruções para executar o notebook</h2>
<div>
Abra o repositório no GitHub → Clique no arquivo Projeto_Aprimorado.ipynb → Copie a URL da página → 
Acesse:
 https://colab.research.google.com → Clique em Arquivo → Abrir notebook → Aba GitHub
→ Cole a URL do repositório ou do notebook → Selecione TelecomX.ipynb e clique em Abrir → Execute as células
</div>

<br></br>

<h3 align="left">📬Contato</h3>
<div>
Em caso de dúvidas ou sugestões, sinta-se à vontade pra entrar em contato!
</div>
<br></br>
<a href="https://instagram.com/portifoliodeanesaraiva?igsh=MpleXXV5ejBqcDQwa==" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<a href = "mailto:contato@deanesaraiva"><img loading="lazy" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
<a href="https://www.linkedin.com/in/deanesaraivacarvalho" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>
