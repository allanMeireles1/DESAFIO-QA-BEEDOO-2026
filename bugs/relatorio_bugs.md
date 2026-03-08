# Relatório de Bugs
Este documento descreve os bugs identificados durante a execução dos testes no módulo de **Cadastro de Cursos** da aplicação.

---

# BUG 01 - Sistema aceita URL de imagem inválida no cadastro de curso

## Severidade
Média

## Passos para reproduzir

1. Acessar a página **Cadastrar Curso**
2. Preencher todos os campos obrigatórios
3. No campo **URL da imagem de capa**, inserir:
    abc123
4. Clicar em **Cadastrar Curso**

## Resultado atual

O sistema aceita a URL inválida e permite o cadastro do curso.

## Resultado esperado

O sistema deveria validar o formato da URL e impedir o cadastro caso a URL seja inválida.

---

# BUG 02 - Sistema permite cadastrar curso com número de vagas negativo

## Severidade
Alta

## Passos para reproduzir

1. Acessar a página **Cadastrar Curso**
2. Preencher os campos obrigatórios
3. No campo **Número de vagas**, inserir:
    -2
4. Clicar em **Cadastrar Curso**

## Resultado atual

O sistema permite o cadastro com número de vagas negativo.

## Resultado esperado

O sistema deveria impedir o cadastro e validar que o número de vagas seja maior que zero.

---

# BUG 03 - Sistema permite cadastrar curso com data de início posterior à data de fim

## Severidade
Alta

## Passos para reproduzir

1. Acessar a página **Cadastrar Curso**
2. Preencher os campos obrigatórios
3. Inserir as seguintes datas:

Data início: **20/12/2026**  
Data fim: **10/12/2026**

4. Clicar em **Cadastrar Curso**

## Resultado atual

O sistema permite cadastrar o curso com datas inconsistentes.

## Resultado esperado

O sistema deveria validar as datas e impedir que a data de início seja posterior à data de término.

---

# BUG 04 - Sistema permite envio do formulário de cadastro completamente vazio

## Severidade
Crítica

## Passos para reproduzir

1. Acessar a página **Cadastrar Curso**
2. Não preencher nenhum campo
3. Clicar em **Cadastrar Curso**

## Resultado atual

O sistema permite a submissão do formulário vazio.

## Resultado esperado

O sistema deveria validar os campos obrigatórios e impedir o envio do formulário.

---

# BUG 05 - Sistema permite cadastro com nome de curso extremamente longo

## Severidade
Média

## Passos para reproduzir

1. Acessar a página **Cadastrar Curso**
2. Inserir um nome com mais de **1000 caracteres** no campo **Nome do curso**
3. Preencher os demais campos obrigatórios
4. Clicar em **Cadastrar Curso**

## Resultado atual

O sistema aceita o nome extremamente longo.

## Resultado esperado

O sistema deveria limitar o número máximo de caracteres permitidos no campo **Nome do curso**.

---

# BUG 06 - Sistema permite cadastro de curso sem selecionar o tipo/modalidade

## Severidade
Alta

## Passos para reproduzir

1. Acessar a página **Cadastrar Curso**
2. Preencher todos os campos obrigatórios
3. Não selecionar o campo **Tipo de curso**
4. Clicar em **Cadastrar Curso**

## Resultado atual

O sistema permite o cadastro do curso sem que o tipo/modalidade seja selecionado.

## Resultado esperado

O sistema deveria exigir a seleção do **Tipo de curso** antes de permitir o cadastro.

---
