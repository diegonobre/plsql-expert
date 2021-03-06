
Estrutura da Linguagem
===

# Blocos de Código
![](https://img.shields.io/badge/Oracle-11g-red.svg) ![](https://img.shields.io/badge/PostgreSQL-9.0-blue.svg)

Um bloco de código é formado basicamente por:

 - Declaração de variáveis
 - Regra de negócio
 - Tipo de retorno

Um bloco de código pode possuir outros blocos aninhados infinitamente, desde que todos possuam início e fim:
```sql
BEGIN
END;
```
O trecho de código acima irá retornar uma exceção porque não foi incluída nenhuma regra de negócio no bloco de código.

O mesmo código não retorna erro caso seja informado qualquer trecho de código:
```sql
BEGIN
	NULL;
END;
```

Para utilizar variáveis é necessário incluir a declaração **DECLARE**
```sql
DECLARE
	-- declaração de variáveis
BEGIN
	-- regra de negócio
	NULL;
END;
```

> **Bloco Anônimo**
Em PL/SQL é possível executar um trecho de código anônimamente (sem que o código faça parte de algum objeto como triggers, functions ou procedures). 
Quando um bloco de código não faz parte de um objeto de banco, chamamos de "Bloco Anônimo".

# Comentários
As regras de inserção de comentários em PL/SQL seguem o padrão SQL

 - Comentários em linha
```sql
-- isso é um comentário
```
 - Comentários em bloco
```sql
/*
Isso é um bloco de comentários
É ideal quando você possui 
várias linhas para comentar
*/
```

# Variáveis
Como vimos, a declaração de variáveis é realizada logo abaixo da instrução **DECLARE**. Podemos utilizar como tipo de variável qualquer tipo de dado SQL, além de qualquer coluna, tabela ou type existente no banco de dados.

Alguns exemplos:
```sql
DECLARE
	-- valores padrão SQL
	v_inteiro INTEGER;
	v_string VARCHAR;
	v_data DATE;
	-- você pode criar a variável com um valor padrão
	v_hoje DATE := SYSDATE; -- oracle
	v_hoje DATE := CURRENT_DATE; -- postgres
	
	-- tipo de dado a partir de uma tabela
	v_tabela NOME_DA_TABELA%TYPE;
	-- tipo de dado da coluna
	v_coluna NOME_DA_TABELA.COLUNA%TYPE;
	
BEGIN
	...
END;
```

Para atribuir valor a uma variável dentro do bloco de execução você deve utilizar o operador **:=**

```sql
DECLARE
	v_nome VARCHAR;
BEGIN
	v_nome := 'Paulo Freire';
END;
```

> Written with [StackEdit](https://stackedit.io/).