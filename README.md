# Desafio de Modelagem – DIO

Este projeto refere-se ao Desafio da DIO que consiste em refinar um modelo Entidade-Relacionamento (ER) para um sistema de e-commerce.

## 🎯 Objetivo

O desafio consiste em:

- Replicar o modelo apresentado no curso;
- Refinar o modelo com os seguintes ajustes:
  - **Cliente PJ e PF** - uma conta pode ser PJ ou PF, não pode ter as duas informações
  - **Pagamento** - pode ter cadastrado mais de uma forma de pagamento
  - **Entrega** - deve possuir status e código de rastreio

## 🛠️ Tarefas Realizadas

### 📌 Réplica do modelo

O modelo apresentado pela instrutora foi replicado fielmente e está disponível neste repositório.  
🔗 Arquivo com o modelo original: `ER_Replica.png`

### 🔧 Refinamento do modelo

O modelo proposto foi aprimorado para atender às exigências do desafio, com os seguintes ajustes:

  - **Especialização da entidade Cliente**: criação das tabelas: `Cliente_PJ` e `Cliente_PF`.
  **Importante**: o MySQL não impede que um Cliente esteja em ambas as tabelas. O controle deve ser feito na aplicação ou com o uso de *triggers*.

  - **Criação da tabela `Formas_Pagto`** para representar as formas de pagamento disponíveis.

  - **Criação da tabela `Entregas`**, com os campos `status_entrega`, `cod_rastreio`, `dt_envio`, `dt_entrega` e referência ao *parceiro* responsável.

Além dos refinamentos solicitados, também foram implementados os seguintes aprimoramentos:

  - **Relacionamento 1:N entre Fornecedores e Produtos**, conforme descrito na narrativa original.
  - **Padronização de nomes de tabelas e atributos**, adotando convenções consistentes.
  - **Adequação de tipos e tamanhos dos atributos**, conforme boas práticas de modelagem.

🔗 Arquivo com o modelo refinado: `ER_Refinado.png`

---

## ✅ Considerações Finais

O modelo refinado considera que o ecommerce funciona como um **marketplace**, por isso inclui as entidades `Fornecedores` e `Parceiros`, com regras de entrega separadas por parceiro.

A prática de desenvolver e refinar modelos ER é essencial para garantir a qualidade e escalabilidade de sistemas reais. Este desafio propocionou uma excelente oportunidade para aplicar conceitos teóricos em um cenário prático.

---
