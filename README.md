# DESAFIO QA - BEEDOO 2026

## 1. Introdução

Este repositório contém a execução do desafio técnico para a vaga de Analista de Qualidade (QA).

O objetivo foi analisar o módulo de cadastro e listagem de cursos da aplicação disponibilizada, criando cenários de teste, executando testes e registrando possíveis falhas encontradas no sistema.

Aplicação analisada:
https://creative-sherbet-a51eac.netlify.app/

---

# 2. Análise inicial da aplicação

A aplicação apresenta um módulo simples de gerenciamento de cursos, permitindo que usuários realizem o cadastro de novos cursos e visualizem cursos cadastrados em uma lista.

Cada curso possui informações como:

- Nome do curso
- Descrição
- Instrutor
- URL de imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso

A aplicação possui duas funcionalidades principais:

- Cadastro de cursos
- Listagem de cursos cadastrados

---

# 3. Principais fluxos da aplicação

Durante a exploração da aplicação foram identificados dois fluxos principais:

### Fluxo 1 — Cadastro de curso

1. Usuário acessa a página **Cadastrar Curso**
2. Preenche os dados do curso
3. Clica no botão **Cadastrar Curso**
4. O curso é registrado no sistema

### Fluxo 2 — Listagem de cursos

1. Usuário acessa a página **Listar Cursos**
2. O sistema exibe os cursos cadastrados

---

# 4. Pontos críticos identificados para testes

Durante a análise da aplicação, foram identificados alguns pontos críticos que podem impactar diretamente o funcionamento do sistema:

- Validação de campos obrigatórios
- Consistência entre data de início e data de fim
- Validação de formatos de entrada (URL, números, textos)
- Controle de valores inválidos (número de vagas negativo)
- Validação de seleção de tipo de curso
- Comportamento do sistema diante de dados inválidos ou inesperados

Esses pontos foram priorizados na criação dos cenários de teste.

---

# 5. Estratégia de testes

Para garantir uma boa cobertura da funcionalidade, os cenários de teste foram elaborados considerando diferentes tipos de testes:

- Cenários positivos (fluxo principal de cadastro)
- Validações de campos
- Cenários negativos
- Testes de consistência de dados
- Comportamentos inesperados do sistema

Os testes foram documentados em formato estruturado utilizando uma planilha no Google Sheets.

---

# 6. Casos de teste

Os cenários e casos de teste criados para o módulo de cursos estão disponíveis na planilha abaixo:

📄 Planilha de Casos de Teste  
https://docs.google.com/spreadsheets/d/1n-xTduxy2n7QYqAZvuLuntsKo0p-jSyV7SRJkJRQGPg/edit?usp=sharing

---

# 7. Execução dos testes

Os cenários de teste foram executados manualmente na aplicação.

Durante a execução foram registrados:

- Resultado esperado
- Resultado obtido
- Status do teste (PASS / FAIL)

As evidências de execução (prints de tela) podem ser acessadas no link abaixo:

📂 Evidências de Testes  
https://drive.google.com/drive/folders/1OPuk_cuSZK8pJMoO9EE8c02KCN00nlSw?usp=sharing

---

# 8. Bugs encontrados

Durante a execução dos testes foram identificados alguns problemas relacionados principalmente a validações de campos e consistência de dados.

Os bugs encontrados estão documentados no arquivo abaixo:

📄 Relatório de Bugs  
[bugs/relatorio_bugs.md](bugs/relatorio_bugs.md)

Cada bug contém:

- Título
- Passos para reprodução
- Resultado atual
- Resultado esperado
- Severidade

---

# 9. Uso de Inteligência Artificial

Ferramentas de Inteligência Artificial foram utilizadas como apoio durante o desenvolvimento do desafio para:

- Auxiliar na organização da documentação
- Revisar estrutura de cenários de teste
- Sugerir melhorias na clareza da documentação

As sugestões geradas foram analisadas criticamente e adaptadas conforme o contexto da aplicação e da estratégia de testes adotada.

---

# 10. Considerações finais

O desafio permitiu exercitar atividades essenciais de QA como análise de requisitos, criação de cenários de teste, execução de testes e documentação de defeitos.

A abordagem utilizada priorizou a identificação de problemas relacionados a validações de entrada e consistência de dados, buscando demonstrar pensamento crítico e organização na condução dos testes.
