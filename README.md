# SecuLLM: Monitoramento Inteligente de Vulnerabilidades em Dependências com LLM

## Resumo / Abstract

O projeto **SecuLLM** propõe uma solução baseada em Large Language Models (LLMs) para apoiar o processo de engenharia de software por meio da **análise automatizada e contextualizada de dependências externas** (bibliotecas e pacotes de terceiros). A ferramenta tem como foco detectar, descrever e orientar desenvolvedores quanto a vulnerabilidades conhecidas nas bibliotecas utilizadas, a partir da leitura de arquivos como `package.json`, `requirements.txt`, `pom.xml` e similares.
<br/>
O diferencial da proposta está na utilização de LLMs não apenas para buscar vulnerabilidades em bases públicas (como CVE, NVD e Snyk), mas também para gerar <strong>resumos explicativos, recomendações de correção e avaliação do impacto da vulnerabilidade no projeto específico</strong>, considerando o contexto da aplicação. Essa abordagem amplia a visibilidade de riscos de segurança em tempo real no ciclo de desenvolvimento, reduzindo a dependência de ferramentas convencionais e melhorando a tomada de decisão técnica.

## Objetivo

Melhorar o processo de engenharia de software com foco em segurança, utilizando LLMs para:

<ul>
  <li>Identificar vulnerabilidades em bibliotecas utilizadas no projeto.</li>
  <li>Gerar explicações em linguagem natural sobre os riscos.</li>
  <li>Recomendar estratégias de mitigação contextualizadas.</li>
  <li>Automatizar a análise contínua em pipelines de desenvolvimento.</li>
</ul>

## Arquitetura

O sistema será dividido em 5 módulos:

**1. Extração de Dependências**

<ul>
  <li>Analisar arquivos como `requirements.txt`, `package.json`, `pom.xml` etc.</li>
  <li>Coletar nome e versão das dependências.</li>
</ul>

**2. Consulta a Bases de Vulnerabilidades**

<ul>
  <li>Integra-se com APIs públicas como [CVE](<a>https://cve.org/</a>), [NVD](<a>https://nvd.nist.gov/</a>), [Snyk](<a>https://snyk.io/</a>).</li>
  <li>Recupera informações sobre falhas conhecidas relacionadas às bibliotecas usadas.</li>
</ul>

**3. Análise com LLM**

<ul>
  <li>Utiliza um modelo como GPT-4-turbo ou LLaMA 3 para:</li>
    <ul>
      <li>Explicar a falha de forma acessível.</li>
      <li>Avaliar o impacto específico da vulnerabilidade no projeto.</li>
      <li>Sugerir upgrades, patches ou bibliotecas alternativas.</li>
    </ul>
</ul>

**4. Geração de Relatórios**

<ul>
  <li>Cria relatórios em formatos como Markdown, JSON ou HTML.</li>
  <li>Suporte à integração com CI/CD para análise contínua.</li>
</ul>

**5. Feedback e Aprendizado Contínuo**

<ul>
  <li>Armazena decisões da equipe (ex: upgrade feito, falha ignorada).</li>
  <li>Gera um histórico que pode refinar futuras recomendações do LLM.</li>
</ul>

## Tecnologias e Ferramentas

- Python (backend / parser de dependências)
- OpenAI API ou HuggingFace (para uso do LLM)
- APIs públicas (CVE, NVD, Snyk)
- GitHub Actions (para integração CI/CD)
- Markdown/HTML para relatórios

## Equipe (Equipe 1)

<ul>
  <li>Gabriel Braz <gbcs></li>
  <li>Luiza Diniz Mendes Monteiro Luna <ldmml></li>
  <li>Maria Letícia Maranhão do Nascimento <mlmn3></li>
  <li>Paulo Rafael Barros de Aguiar <prba></li>
</ul>
