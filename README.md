
PL/SQL Expert
==========
Neste guia utilizaremos os ícones abaixo para identificar em que plataforma/versão a instrução foi testada.

![](https://img.shields.io/badge/Oracle-9g-red.svg) ![](https://img.shields.io/badge/PostgreSQL-9.0-blue.svg) ![](https://img.shields.io/badge/MySQL-5.0-green.svg) ![](https://img.shields.io/badge/SQLServer-2010-yellow.svg)

# Apresentação
> **PL/SQL** é uma linguagem de programação que executa de forma ordenada uma série de comandos buscando atender a uma finalidade.

SQL e PL/SQL são linguagens criadas para interagir com o banco de Dados. A linguagem SQL acessa e modifica os dados relacionais. Exemplo: 
```sql
SELECT * FROM Tabela1;
```
SQL é uma linguagem declarativa (você descreve que dados você deseja, mas não como serão obtidos).

> Problema: existem limites em relação a **o que** você pode fazer com a linguagem

Já a linguagem PL/SQL, fornece um mecanismo para os desenvolvedores adicionarem um componente de procedimento no nível de servidor. 

PL/SQL realiza a integração de blocos procedurais com a linguagem SQL. É uma linguagem de quarta geração (4GL).

# Vantagens
**Suporte às linguagens procedurais:** não é utilizada apenas para manipulação de dados. Fornece também operações comuns em linguagens de programação como: validações, loops, operações aninhadas, etc.
	
**Redução do trafego de rede:** devido a natureza do PL/SQL, pode-se fazer com que o mesmo execute um bloco inteiro no engine do banco Oracle de uma unica vez, propiciando uma redução significativa do trafego.

**Tratamento de erros:** permite lidar com o tratamento de erros de maneira inteligente.

**Portabilidade:** aplicações escritas em PL/SQL podem ser executadas em qualquer sistema operacional

# Tópicos abordados

 1. Primeiros passos
 2. Funções definidas pelo usuário
 2. Estrutura da linguagem
 3. Controle de fluxo
 4. Cursores em PL/pgSQL
 5. SQL dinâmico
 6. Tratamento de erros
 7. Manipulação de Operadores
 8. Gatilhos (Triggers)

> Written with [StackEdit](https://stackedit.io/).