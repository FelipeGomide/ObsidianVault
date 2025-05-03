## **Ementa**:

- Conceitos básicos: Modelos, Conceitos, Instâncias, Arquitetura
- Modelos e linguagens: Modelo entidade-relacionamento, Modelo relacional, Álgebra relacional, SQL
- Projeto de bancos de dados: Projeto Lógico,
- Tópicos Avançados: Bancos de dados não-relacionais (NoSQL), aplicações em RI

## **Tópicos fora da ementa**:

- Estruturas armazenamento dados
- Processamento de consultas
- Controle de concorrência
- Segurança e integridade
- Recuperação de falhas

## **Avaliação**:

2 provas 30pts cada

TP1 10 pts: SQL (individual)

TP2 20 pts: projeto (grupos)

Exercícios 10pts

  

**Livro**: Sistemas de Banco de Dados

Elmasri e Navathe

Qualquer edição a partir da 4ª

  

# **Visão Geral**

“Um banco de dados é uma coleção de elementos relacionados”

  

**SGBD**: Sistema de Gerência de Banco de Dados

Programas que permitem criar e manter um banco de dados

Utilizaremos na disciplina o SQLite

  

**Catálogo de metadados**:

Acessório ao banco de dados

  

**APIs** facilitam a comunicação com o SGBD

  

**Vantagens SGBD**

Armazenamento persistente dos dados

Autodescrição dos dados (meta-dados)

Isolamento entre programas e dados

Múltiplas visões dos dados

Compartilhamento de dados

Garantias de consistência

  

# **Casos de Uso**

**Administrador (DBA)**: Administra o BD e o SGBD

Autoriza o acesso, coordena e monitora a utilização e aquisição de hardware adicional

  

**Projetista**: Identifica os dados e escolhe estruturas apropriadas para representar e armazenar dados

  

**Projeto de desenvolvimento:**

Análise de requisitos

Requisitos do BD:

Projeto Conceitual (Diagrama, alto nível) (Independe do SGBD)

Projeto Lógico (Depende da classe do SGBD)

Projeto Físico (Decisões de baixo nível no disco) (Depende do SGBD)

Requisitos funcionais:

Não deu tempo, matéria engenharia software

  

**Cientista de Dados:**

Acessa o BD via uma linguagem de consulta

Acesso direto (console do SGBD) ou indireto (API)