# Data is getting bigger

---

Big data: 3Vs

- Volume
- Velocidade
- Variedade

Interações seguem infinitamente

Fontes de big data:

- Logs, sensores

  

## OTAP, OLAP

**Online transitioning processing**

Fast queries

**Online analytical processing**

Complex heavy queries

  

Matéria DCC: Processamento de dados massivos (Dorgival)

  

## Contenders

### OldSQLs 1970s(Oracle, MySQL, IBM DB2, MS SQL)

Clássicos, tabulares

Vantagens:

- Persistente
- Acesso concorrente
- Camada de integração
- Padronização

Desvantagens:

- Mismatch de impedância
    - Esquema a priori
    - Maior consistência
    - Data relacional, software orientado a objetos
        - ORM(Object-relational mapping): faz essa tradução
    - Custo de análise
        - Denormalization cara
    - Flexibilidade
        - Esquema é fixo
        - Alteração do esquema on-demand
- Escalabilidade:
    - Big data, big usage
    - Escalabilidade vertical
        - Hardware custoso
        - Limitado
        - Pode falhar
    - Escalabilidade horizontal
        - Diferentes orientações: dados, funcionalidade
        - Difícil sincronização/atualização

### NoSQL 2000s (MongoDB, Titan, Redis)

Não tabulares, menor garantia de integridade

Relaxam a consistência

Abandonam o SQL*

- Não relacional
- Cluster-friendly
- Sem esquema
- Open-source

4 tipos de modelos:

- Agregados
    - Key-value (tabela hash)
    - Column family (Google BigColumn)
    - Document JSON (MongoDB)
- Grafos

### NewSQL 2010s (VoltDB, Google Spanner)

Tentativa de adicionar mais integridade aos não tabulares.

Mantém o SQL*

  

# Qual o melhor sistema?

Depende.

- Informação normalizada, sensível:
    - Modelo relacional
- Session data, user profiles, shopping carts
    - Key-value model
- CMS, product profiles, search, analytics
    - Wide-column, document models
- Networked data
    
    - Graph model
    
      
    

NoSQL Distilled - Fowler, Sadalage