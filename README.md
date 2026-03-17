# DESAFIO QA - BEEDOO 2026

## 1. Introdução

Este repositório contém a execução do desafio técnico para a vaga de Analista de Qualidade (QA).

O objetivo foi analisar criticamente a aplicação, identificar riscos, validar comportamentos e documentar falhas que impactam a qualidade, segurança e consistência dos dados.

Aplicação analisada:  
https://creative-sherbet-a51eac.netlify.app/

---

## 2. Análise inicial da aplicação

A aplicação apresenta um módulo simples de gerenciamento de cursos, permitindo o cadastro e a visualização de cursos.

Cada curso possui:

- Nome do curso
- Descrição
- Instrutor
- URL de imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso

Funcionalidades principais:

- Cadastro de cursos
- Listagem de cursos cadastrados

---

## 3. Principais fluxos da aplicação

### Fluxo 1 — Cadastro de curso

1. Acessar a página **Cadastrar Curso**
2. Preencher os dados
3. Clicar em **Cadastrar Curso**
4. Sistema registra o curso

### Fluxo 2 — Listagem de cursos

1. Acessar **Listar Cursos**
2. Sistema exibe os cursos cadastrados

---

## 4. Pontos críticos para testes

- Validação de campos obrigatórios
- Consistência entre datas
- Validação de formatos (URL, números, texto)
- Controle de valores inválidos
- Seleção de tipo de curso
- Comportamento diante de dados inesperados

---

## 5. Estratégia de testes

Foram considerados:

- Cenários positivos
- Cenários negativos
- Validações de campos
- Testes de consistência
- Comportamentos inesperados

Os testes foram documentados em Google Sheets.

---

## 6. Casos de teste

📄 Planilha:  
https://docs.google.com/spreadsheets/d/1n-xTduxy2n7QYqAZvuLuntsKo0p-jSyV7SRJkJRQGPg/edit

---

## 7. Execução dos testes

Foram registrados:

- Resultado esperado
- Resultado obtido
- Status (PASS / FAIL)

📂 Evidências:  
https://drive.google.com/drive/folders/1OPuk_cuSZK8pJMoO9EE8c02KCN00nlSw

---

## 8. Bugs encontrados

📄 Relatório:  
[bugs/relatorio_bugs.md](bugs/relatorio_bugs.md)

Cada bug contém:

- Título
- Passos
- Resultado atual
- Resultado esperado
- Severidade

---

## 9. Análise de riscos

- Falta de validação robusta → registros inconsistentes
- Persistência de dados inválidos
- Possível inserção de scripts (XSS)
- Ausência de controle de duplicidade
- Falta de consistência após reload

---

## 10. Priorização de riscos

### Alta criticidade
- Dados inválidos → comprometem integridade da base e funcionalidades dependentes
- Falta de validação → permite estados inconsistentes
- Execução de scripts → risco de segurança

### Média criticidade
- Inconsistência de datas → afeta lógica de negócio
- Valores negativos → quebra regras do sistema

### Baixa criticidade
- Problemas de usabilidade

---

## 11. Testes de segurança

- Inserção de scripts (XSS)
- Falta de sanitização
- Aceitação de dados fora do padrão

---

## 12. Impacto no negócio

- Dados inconsistentes comprometem decisões
- Falhas reduzem confiança no sistema
- Vulnerabilidades expõem a riscos
- Má experiência impacta adoção

---

## 13. Estratégia de regressão

Após correções:

- Validar fluxo completo de cadastro
- Validar campos obrigatórios
- Verificar persistência
- Garantir consistência de regras

---

## 14. Sugestões de melhoria

- Validação robusta frontend/backend
- Feedback claro ao usuário
- Bloqueio de dados inválidos
- Sanitização contra XSS
- Controle de duplicidade

---

## 15. Próximos passos

- Automação de testes críticos
- Criação de suíte de regressão
- Definição de critérios de aceitação
- Integração em CI/CD
- Monitoramento em produção

---

## 16. Uso de Inteligência Artificial

Utilizada para:

- Organização da documentação
- Revisão de estrutura
- Sugestões de melhoria

Todas as sugestões foram analisadas criticamente.

---

## 17. Considerações finais

O desafio foi utilizado para avaliar a aplicação sob a ótica de qualidade, risco e consistência.

Foram identificadas falhas relevantes que impactam diretamente a confiabilidade do sistema.

A abordagem adotada priorizou não apenas execução de testes, mas análise crítica, identificação de riscos e melhorias alinhadas à qualidade do produto.
