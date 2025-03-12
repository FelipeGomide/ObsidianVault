# **Felipe Lopes Gomide**

  

  

## 1. Esquema não normalizado

$Movie(MovieID, Title, Year, \{ Genre(GenreID,Name)\},\\\{Actor(Actor ID, Name, Role)\},Plot, ProducerID, ProducerName)$

## 2. Dependências funcionais

$MovieID \rightarrow Title \\ GenreID \rightarrow Name \\ ActorID \rightarrow Name \\ ProducerID \rightarrow ProducerName \\ ActorID,MovieID \rightarrow Role$

## 3. Forma normal da questão 1

A tabela da questão 1 não se encontra em nenhuma das formas normais, já que fere os princípios primeira forma normal 1FN de que todos os atributos são atômicos, ou seja, são simples e monovalorados. O que não ocorre com $ Genre$﻿ e $Actor$﻿, que são multivalorados.

## 4. Normalização da tabela

### Primeira Forma Normal (1FN)

Todos atributos passam a ser atômicos

$Movie(MovieID, Title, Year,Plot, ProducerID, ProducerName) \\ Genre(MovieID, GenreID,Name)\\ Actor(MovieID, Actor ID, Name, Role)$

### Segunda Forma Normal (2FN)

$Movie(\underline{MovieID}, Title, Year,Plot, ProducerID, ProducerName) \\ Theme(\underline{MovieID}, GenreID) \\ Genre(\underline{GenreID},Name)\\ Cast(\underline{MovieID, ActorID, Role}) \\ Actor(\underline{Actor ID}, Name)$

### Terceira Forma Normal (3FN)

$Movie(\underline{MovieID}, Title, Year,Plot,ProducerID) \\ \\ \\Producer(\underline{ProducerID}, ProducerName) \\ Theme(\underline{MovieID}, GenreID) \\ Genre(\underline{GenreID},Name)\\ Cast(\underline{MovieID, ActorID, Role}) \\ Actor(\underline{Actor ID}, Name)$

## 5. Esquema ER

![[IBD_Normalizacao_EsquemaER.png]]