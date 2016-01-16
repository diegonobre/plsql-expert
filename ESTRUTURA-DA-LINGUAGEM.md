
Estrutura da Linguagem
===

# Bloco Anônimo

> Roda em: [Oracle] [PostgreSQL]

Em PL/SQL é possível executar um trecho de código anônimamente (sem que o código faça parte de algum objeto como triggers, functions ou procedures), para isso é necessário seguir algumas regras.

Um bloco anônimo deve possuir início e fim:
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

> Written with [StackEdit](https://stackedit.io/).