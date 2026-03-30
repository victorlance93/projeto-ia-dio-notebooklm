# projeto-ia-dio-notebooklm
# Caderno Temático com NotebookLM: Playwright

## 1. Contexto e Objetivos

Este projeto foi desenvolvido como parte do desafio prático da DIO, com o objetivo de utilizar a Inteligência Artificial como ferramenta de aprendizagem ativa na construção de um caderno temático no NotebookLM.

O tema escolhido foi **Playwright**, uma ferramenta moderna de automação de testes end-to-end, mantida pela Microsoft, que vem se destacando pela velocidade, confiabilidade, suporte a múltiplos navegadores e boa experiência de desenvolvimento. Escolhi esse tema porque é uma tecnologia que desejo aprender com mais profundidade e na qual quero me especializar para evoluir tecnicamente como profissional de QA.

Os principais objetivos deste estudo foram:

- entender como iniciar um projeto de automação do zero com Playwright;
- aprender a estrutura ideal de pastas para um projeto escalável;
- identificar os comandos mais importantes para começar a utilizar a ferramenta;
- descobrir um site adequado para praticar testes reais com apoio guiado;
- usar o NotebookLM para organizar informações, testar prompts, resumir conteúdo e consolidar aprendizado;
- transformar o estudo em um material reutilizável para futuras revisões.

Ao longo do processo, a IA foi utilizada como apoio para acelerar o entendimento da documentação, organizar respostas e transformar conteúdo técnico em um material de estudo mais claro. Ainda assim, ficou evidente que a validação nas fontes originais é essencial para garantir precisão técnica e evitar interpretações superficiais.

---

## 2. Curadoria de Fontes + Engenharia de Prompts e Cicatrizes

Para construir este caderno temático, foram utilizadas fontes abertas em diferentes formatos, combinando documentação oficial, artigo introdutório e vídeos práticos. A ideia foi equilibrar teoria, prática e visão de mercado.

### Referências utilizadas

- Documentação oficial do Playwright  
  https://playwright.dev/docs/intro

- Artigo da DIO: Criando o primeiro teste com Playwright  
  https://www.dio.me/articles/criando-o-primeiro-teste-com-playwright

- Vídeo no YouTube  
  https://www.youtube.com/watch?v=gaYP4cTJvqc

- Playlist no YouTube  
  https://www.youtube.com/playlist?list=PLeo6Q1inqlOdzwuW6ivlX_95682PfsGGG

- Vídeo no YouTube  
  https://www.youtube.com/watch?v=788GvvcfwTY

Essas fontes foram escolhidas porque se complementam bem:
- a **documentação oficial** foi a base principal do estudo;
- o **artigo da DIO** ajudou a contextualizar o primeiro contato com a ferramenta;
- os **vídeos** reforçaram a parte prática, visual e introdutória.

### Prompts utilizados no NotebookLM

Durante o estudo, os principais prompts utilizados foram:

- **Como começar uma automação do zero com Playwright?**
- **Qual a melhor estrutura de pastas para o projeto?**
- **Quais os comandos essenciais de aprender no Playwright?**
- **Existe algum site indicado para que possamos fazer um projeto inicial de teste onde você possa ser meu guia?**
- **Quais linguagens além de JavaScript o Playwright suporta?**
- **Como funciona o Codegen para gerar testes automaticamente?**
- **Qual a diferença entre o Playwright e o Selenium?**
- **Como organizar as classes de Page Objects no projeto?**
- **Quais são as melhores práticas para selecionar localizadores?**
- **Como integrar essa estrutura ao GitHub Actions?**
- **Como implementar o Page Object Model no Playwright?**
- **Como usar o Codegen para gerar código automaticamente?**
- **Quais cenários começar e quantos cenários conseguimos fazer no SauceDemo?**
- **Como fazer o teste de login com sucesso passo a passo?**

### O que foi aprendido com os prompts

Ao perguntar **como começar uma automação do zero com Playwright**, ficou claro que a ferramenta possui uma inicialização bastante amigável, especialmente com o comando `npm init playwright@latest`, que já gera a estrutura base do projeto, instala navegadores e prepara o ambiente. Também foi reforçado que o uso com **TypeScript** tende a ser mais recomendado para projetos mais robustos.

Ao investigar **a melhor estrutura de pastas para o projeto**, foi possível entender que, para um projeto pequeno, a estrutura padrão gerada já funciona bem, mas para algo mais profissional o ideal é separar melhor responsabilidades, com diretórios como:
- `tests/` para os arquivos de teste;
- `pages/` ou `src/pages/` para Page Objects;
- `fixtures/` para objetos e setups reutilizáveis;
- `test-data/` para massa de dados;
- `playwright-report/` e `test-results/` para relatórios e evidências;
- arquivos centrais como `playwright.config.ts`, `package.json` e `tsconfig.json`.

Ao explorar **os comandos essenciais do Playwright**, os mais importantes para início do aprendizado foram:
- `npm init playwright@latest`
- `npx playwright test`
- `npx playwright test --headed`
- `npx playwright test --ui`
- `npx playwright codegen`
- `npx playwright show-report`

Também foram destacados comandos e métodos muito usados no código, como:
- `page.goto()`
- `getByRole()`
- `getByText()`
- `getByLabel()`
- `getByTestId()`
- `locator()`
- `click()`
- `fill()`
- `expect().toBeVisible()`
- `expect().toHaveText()`
- `expect().toHaveURL()`

Ao perguntar **sobre um site indicado para começar um projeto inicial**, o principal recomendado foi o **SauceDemo**, por ser um ambiente simples, estável e muito usado para prática de automação. Ele permite validar fluxos clássicos de e-commerce, como:
- login com sucesso;
- login inválido;
- listagem de produtos;
- adição ao carrinho;
- remoção de item;
- checkout;
- logout.

Além do SauceDemo, também apareceram como boas opções:
- **The Internet (Herokuapp)** para cenários variados;
- **ToDo List Apps** para operações de CRUD;
- **jQuery UI** para interações mais complexas.

### Cicatrizes e troubleshooting

Durante o processo de estudo com IA, algumas dificuldades ficaram claras:

- quando o prompt era muito genérico, a resposta vinha ampla demais;
- algumas respostas pareciam completas, mas precisavam ser confirmadas nas fontes oficiais;
- a qualidade da resposta melhorava muito quando a pergunta era mais específica;
- prompts com foco prático, como “passo a passo” ou “melhores práticas”, geraram resultados mais úteis;
- a IA foi ótima para resumir e organizar o conteúdo, mas não substituiu a leitura da documentação.

A principal “cicatriz” do processo foi perceber que **não basta perguntar**, é preciso saber **como perguntar**. Quanto mais claro e específico o prompt, melhor a qualidade do material gerado.

---

## 3. Miniguia de Estudo (Entrega Final)

O **Playwright** é um framework moderno de automação voltado para testes end-to-end em aplicações web. Ele permite automação em diferentes navegadores, como Chromium, Firefox e WebKit, com recursos nativos que ajudam a tornar os testes mais confiáveis, rápidos e legíveis.

Uma das maiores vantagens do Playwright é que ele já nasce com várias capacidades importantes integradas, como:
- test runner nativo;
- paralelismo;
- suporte a múltiplos navegadores;
- auto-waiting;
- assertions inteligentes;
- ferramentas de debug;
- geração de relatórios;
- possibilidade de gravação de interações com Codegen.

### Resumo estruturado do assunto

#### Como começar uma automação do zero com Playwright

Para iniciar um projeto do zero, é recomendado instalar:
- **Node.js**
- **VS Code**
- **extensão Playwright Test for VS Code**

Depois disso, basta executar no terminal:

```bash
npm init playwright@latest
