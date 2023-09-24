
# Resolução exercício SQL

1ª Atividade relacionada ao arquivo ´banco_de_paises_paises´ acima. 


## 1ª Questão
Selecione todos os dados dos países da tabela_paises.

```sql
select * from tabela_paises;
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/25184791-e285-452b-abd9-333616168132)

## 2ª Questão
Selecione todas as cidades cujo país seja brazil.

```sql
select cidade 
from tabela_paises 
where pais = 'Brazil';
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/914b80c0-52cc-4428-9f83-a4e5ca6a5156)

## 3ª Questão
Selecione todas as cidades cuja região(estado) é ceará.

```sql
select cidade 
from tabela_paises 
where regiao = 'Ceará';
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/2ff27f6f-b7c3-4079-8b29-9bdad3588cdd)



## 4ª Questão
Utilize a função count para saber quantas regiões(estados) existem na China,
utilize também o group by.

```sql
select regiao, count (regiao)
from tabela_paises
where pais = 'China'
group by  regiao;
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/64dd172b-81bd-41c7-9596-0773f3a796fa)


## 5ª Questão
Quais regiões, diferentes, existem no Canadá?

```sql
select distinct regiao
from tabela_paises 
where pais = 'Canada';
```
## Resultado esperado
![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/29d2c116-ffc8-408a-959e-22751494f8c9)


## 6ª Questão
Quantos países diferentes existem na tabela 'tabela_paises'.

```sql
select distinct pais
from tabela_paises;
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/b0bdb511-bcd7-4cde-b7f8-840f201242ca)

## 7ª Questão
Quantas cidades diferentes existem no brazil.

```sql
select distinct cidade
from tabela_paises 
where pais = 'Brazil';
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/89769c5e-380a-4a7c-8335-cd9a8f079487)

## 8ª Questão
Selecione os países e quantas regiões cada país possui;

```sql
select pais, count (distinct regiao)
from tabela_paises
group by pais;
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/6062320f-fdb7-4067-99e7-6a9a67735f5b)


## 9ª Questão
Quantas pessoas com nome começando em 'João' existem no banco?

```sql
select count (nome)
from tabela_paises
where nome like 'João%';
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/e77b6783-e06d-4abb-b337-61e25f5fd2af)

## 10ª Questão
Quantas pessoas têm o nome John?

```sql
select count (nome)
from tabela_paises 
where nome = 'John';
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/3e0795c0-d059-4219-8fe3-90f8d21ee530)

## 11ª Questão
Ordene os nomes dos países sem repetição em ordem alfabética;
```sql
select distinct pais 
from tabela_paises
order by(pais);
```
## Resultado esperado

![image](https://github.com/AlanaLopes/banco_de_dados/assets/112038055/1911ebbf-035e-4ddf-9d45-a733af992750)
