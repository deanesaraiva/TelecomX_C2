![Banner](banner.png)

<h1 tabindex="0" align="center">Projeto de Previsão de Churn de Clientes</h1>
<div>
  <p>
    Este repositório apresenta o desenvolvimento de um <strong>modelo de Machine Learning para previsão de Churn</strong>,
    com foco em identificar clientes com maior probabilidade de cancelamento(Churn) e apoiar estratégias de retenção.
    Todo o processo foi conduzido de forma estruturada, desde o tratamento dos dados até a comparação de modelos preditivos.
  </p>
 <p>
  <h2 id="indice">📑 Índice</h2>
 <ul>
   <li><a href="#indice">indice</a></li>
   <li><a href="#objetivo-do-projeto">Objetivo do Projeto</a></li>
   <li><a href="#tratamento-e-preparacao-dos-dados">Tratamento e Preparação dos Dados</a></li>
   <li><a href="#normalizacao-dos-dados">Normalização dos Dados</a></li>
   <li><a href="#selecao-das-variaveis-explicativas">Seleção das Variáveis Explicativas</a></li>
   <li><a href="#modelos-de-machine-learning">Modelos de Machine Learning</a></li>
   <li><a href="#comparacao-dos-resultados">Comparação dos Resultados</a></li>
   <li><a href="#perfil-do-cliente-com-alto-risco-de-churn">Perfil do Cliente com Alto Risco de Churn</a></li>
   <li><a href="#medidas-estrategicas-para-retencao-de-clientes">Medidas Estratégicas para Retenção</a></li>
   <li><a href="#instrucoes-para-notebook">Instruções para acessar o Notebook</a></li>
 </ul>
 </p>
</div>

<hr>

<h2 align="center" id="objetivo-do-projeto"><strong>Objetivo do Projeto</strong></h2>
<div>
  <p>
    O objetivo principal deste projeto é <strong>prever o comportamento de Churn dos clientes</strong>,
    utilizando dados cadastrais, contratuais e financeiros.
  </p>
  <p>
    A variável alvo <strong>Churn</strong> foi tratada como um problema de <strong>classificação binária</strong>, onde:
  </p>
  <ul>
    <li><strong>1</strong> representa clientes que cancelaram o serviço</li>
    <li><strong>0</strong> representa clientes que permaneceram ativos</li>
  </ul>
  <p>
    Busquei não apenas a previsão, mas também a <strong>interpretação dos fatores que influenciam o cancelamento</strong>.
  </p>
</div>
<h4 align="right" id="indice"> ⬆️Índice</h4>
<hr>

<h2 align="center" id="tratamento-e-preparacao-dos-dados">Etapa 1 — Tratamento e Preparação dos Dados</h2>

<h3>Limpeza e tipagem das variáveis</h3>
<div>
  <p>
    O conjunto de dados passou inicialmente por um processo estruturado de preparação, que incluiu:
  </p>
  <ul>
    <li>Identificação e tratamento de valores ausentes</li>
    <li>Correção de tipos de dados inconsistentes</li>
    <li>Conversão de variáveis numéricas armazenadas como texto</li>
    <li>Ajustes de colunas categóricas para o tipo <code>Numérico</code></li>
  </ul>
  <p>
    Essas etapas foram fundamentais para garantir a integridade dos dados,
    evitar erros de execução e assegurar a coerência estatística durante a modelagem.
  </p>
</div>
<h4 align="right" id="indice"> ⬆️Índice</h4>
<h3>Codificação das variáveis categóricas</h3>
<div>
  <p>
    As variáveis categóricas foram transformadas por meio de <strong>One-Hot Encoding</strong>,
    gerando colunas binárias representativas de cada categoria.
  </p>
  <p>
    Também foram identificadas variáveis <strong>binárias</strong>, contendo apenas dois valores únicos,
    o que permitiu uma codificação mais eficiente e sem perda de informação.
  </p>
  <p>
    Esse processo foi essencial para que os algoritmos de Machine Learning interpretassem corretamente
    informações qualitativas, como tipo de contrato, método de pagamento e serviços contratados.
  </p>
</div>
<h4 align="right" id="indice"> ⬆️Índice</h4>
<hr>

<h2 align="center" id="normalizacao-dos-dados"><strong>Etapa 2 — Normalização dos Dados</strong></h2>
<div>
  <p>
    As variáveis numéricas foram normalizadas utilizando técnicas como <strong>StandardScaler</strong>.
  </p>
  <p>
    A normalização foi necessária principalmente para modelos sensíveis à escala dos dados,
    como a <strong>Regressão Logística</strong>.
  </p>
  <p><strong>Principais motivos para a normalização:</strong></p>
  <ul>
    <li>Evitar que variáveis com grande magnitude dominassem o processo de treinamento</li>
    <li>Melhorar a convergência do modelo</li>
    <li>Tornar os coeficientes comparáveis entre si</li>
  </ul>
  <p>
    Embora modelos baseados em árvores, como o <strong>Random Forest</strong>,
    não exijam normalização, o procedimento foi mantido para garantir consistência
    e permitir uma comparação justa entre os modelos.
  </p>
</div>
<h4 align="right" id="indice">⬆️ Índice</h4>
<hr>

<h2 align="center" id="selecao-das-variaveis-explicativas"><strong>Etapa 3 — Seleção das Variáveis Explicativas</strong></h2>
<h3>Critérios de escolha</h3>
<div>
  <p>
    A seleção das variáveis explicativas foi baseada nos seguintes critérios:
  </p>
  <ul>
    <li>Relevância teórica para o problema de Churn</li>
    <li>Impacto estatístico observado na variável alvo</li>
    <li>Eliminação de variáveis identificadoras, como <code>customerID</code></li>
    <li>Redução de redundância e multicolinearidade</li>
  </ul>
</div>

<h4 align="right" id="indice"> ⬆️Índice</h4>
<h3>Justificativa para exclusão de variáveis</h3>
<div>
  <p>
    As variáveis descartadas apresentavam pelo menos um dos seguintes problemas:
  </p>
  <ul>
    <li>Funcionavam apenas como identificadores únicos</li>
    <li>Representavam informações duplicadas</li>
    <li>Apresentavam baixa variabilidade</li>
    <li>Não demonstravam impacto relevante no Churn</li>
  </ul>
  <p>
    A restrição do conjunto de variáveis tornou o modelo mais interpretável,
    menos suscetível a overfitting e computacionalmente mais eficiente.
  </p>
</div>
<h4 align="right" id="indice"> ⬆️Índice</h4>

<h3>Impacto das variáveis selecionadas no Churn</h3>
<div>
  <p>
    As variáveis escolhidas capturam fatores críticos relacionados ao Churn, como:
  </p>
  <ul>
    <li><strong>Tempo de relacionamento do cliente com a empresa</strong></li>
    <li><strong>Tipo de contrato firmado</strong></li>
    <li><strong>Custo mensal do serviço</strong></li>
    <li><strong>Forma de pagamento</strong></li>
    <li><strong>Adesão a serviços adicionais</strong></li>
  </ul>
  <p>
    Esses fatores refletem diretamente o nível de comprometimento,
    satisfação e percepção de valor por parte do cliente.
  </p>
</div>
<h4 align="right" id="indice">⬆️ Índice</h4>
<hr>

<h2 align="center" id="modelos-de-machine-learning"><strong>Etapa 4 - Escolha dos Modelos de Machine Learning</strong></h2>
<h3><strong>Regressão Logística: </strong>usada como modelo base de classificação binária</h3>
<div>
 <ul>
    <li>Alta interpretabilidade</li>
    <li>Permite análise direta do impacto das variáveis</li>
    <li>Funciona como baseline para comparação</li>
  </ul>
</div>
<br>
<h3><strong>Random Forest: </strong>capacidade de capturar relações não lineares entre as variáveis.</h3>
<div>
  <ul>
    <li>Melhor desempenho preditivo</li>
    <li>Menor sensibilidade a ruídos</li>
    <li>Capacidade de identificar interações entre variáveis</li>
  </ul>
</div>
<h4 align="right" id="indice">⬆️ Índice</h4>
<hr>

<h2 align="center" id="comparacao-dos-resultados"><strong>Etapa 5 — Comparação dos Resultados</strong></h2>
<div>
  <p>
    Os modelos foram avaliados utilizando métricas como:
  </p>
  <ul>
    <li>Acurácia</li>
    <li>Precisão</li>
    <li>Recall</li>
    <li>F1-score</li>
  </ul>
  <p>
    A Regressão Logística apresentou desempenho consistente e alta interpretabilidade,
    enquanto o Random Forest obteve resultados que identificavam um overfiting.
  </p>
  <p>
    Dessa forma, a <strong>Regressão Logistica</strong> foi considerado o modelo mais adequado
    para aplicação prática.
  </p>
</div>
<h4 align="right" id="indice">⬆️ Índice</h4>
<hr>

<h2 align="center" id="perfil-do-cliente-com-alto-risco-de-churn"><strong>Perfil do Cliente com Alto Risco de Churn</strong></h2>
<ul>
  <li>Contrato mensal (<em>Month-to-month</em>)</li>
  <li>Baixo tempo de permanência (Tenure reduzido)</li>
  <li>Altas cobranças mensais</li>
  <li>Método de pagamento manual</li>
  <li>Ausência de serviços adicionais (segurança, suporte técnico)</li>
</ul>
<h4 align="right" id="indice">⬆️ Índice</h4>
<hr>

<h2 align="center" id="medidas-estrategicas-para-retencao-de-clientes"><strong>Medidas Estratégicas para Retenção de Clientes</strong></h2>
<ul>
  <li>Incentivar migração para contratos de longo prazo</li>
  <li>Oferecer descontos progressivos para clientes de alto custo</li>
  <li>Criar pacotes de serviços adicionais</li>
  <li>Atuar nos primeiros meses do cliente com ações de engajamento</li>
  <li>Reavaliar a experiência de pagamento eletrônico</li>
  <li>Desenvolver campanhas personalizadas para clientes com baixo tenure</li>
</ul>
<h4 align="right" id="indice">⬆️ Índice</h4>
<hr>

<h2 align="left" id="instrucoes-para-notebook"><strong>Instruções para executar o notebook</strong></h2>
<p>Para executar o notebook diretamente no Google Colab, siga os passos abaixo:</p>
<ul>
  <li>Acesse este repositório no GitHub</li>
  <li>Clique no arquivo <strong>TelecomX_2.ipynb</strong></li>
  <li>Copie a URL da página do notebook</li>
  <li>Acesse <a href="https://colab.research.google.com" target="_blank">https://colab.research.google.com</a></li>
  <li>Clique em <strong>Arquivo</strong> → <strong>Abrir notebook</strong></li>
  <li>Selecione a aba <strong>GitHub</strong></li>
  <li>Cole a URL do notebook e clique em <strong>Abrir</strong></li>
  <li>Execute as células em ordem</li>
</ul>

<br>
<strong>Um relatório resumido também esta disponivel neste repositório, no formato PDF. </strong>
<h4 align="right" id="indice">⬆️ Índice</h4>
<hr>

<h4 align="left">📬Contato</h4>
<div>
Em caso de dúvidas ou sugestões, sinta-se à vontade pra entrar em contato!
</div>
<br></br>
<a href="https://instagram.com/portifoliodeanesaraiva?igsh=MpleXXV5ejBqcDQwa==" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<a href = "mailto:contato@deanesaraiva"><img loading="lazy" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
<a href="https://www.linkedin.com/in/deanesaraivacarvalho" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>
