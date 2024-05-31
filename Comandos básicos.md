# Comandos Básicos e Dicas
Nesta seção, apresentamos alguns dos comandos básicos de SQL e dicas úteis para trabalhar com eles.


## Comando ´SELECT´
O comando SELECT é usado para consultar dados de uma tabela. Aqui está um exemplo de como usar o comando SELECT:

### Selecionar Todas as Colunas

Para selecionar todas as colunas de uma tabela, use o caractere *:

```sql
SELECT * FROM tabela;
```


### Selecionar Colunas Específicas
Para selecionar colunas específicas, liste os nomes das colunas separadas por vírgulas:

```sql
SELECT coluna1, coluna2 FROM tabela;
```


### Filtrar Resultados com WHERE
Use a cláusula WHERE para filtrar os resultados com base em uma condição:

```sql
SELECT coluna1, coluna2 FROM tabela WHERE coluna3 = 'valor';
```


### Ordenar Resultados com ORDER BY

Use ORDER BY para ordenar os resultados por uma ou mais colunas:
```sql
SELECT coluna1, coluna2 FROM tabela ORDER BY coluna1 ASC;
```


### Limitar o Número de Resultados com LIMIT

Use a cláusula LIMIT para limitar o número de resultados retornados:
```sql
SELECT coluna1, coluna2 FROM tabela LIMIT 10;
```


### Usar Alias para Renomear Colunas

Você pode usar AS para renomear colunas no resultado:

**SELECT coluna1 AS alias1, coluna2 AS alias2 FROM tabela;**

### Exemplo 

```sql
SELECT coluna1 AS alias1, coluna2 
FROM tabela 
WHERE coluna3 = 'valor' 
ORDER BY coluna1 ASC 
LIMIT 10;
```

Este exemplo seleciona coluna1 (renomeada para alias1) e coluna2 da tabela onde coluna3 é igual a 'valor', ordena os resultados por coluna1 em ordem ascendente e limita a saída a 10 resultados.


____
## Exemplo de ´INSERT´

O comando INSERT é usado para adicionar novos dados a uma tabela. Aqui está um exemplo de como usar o comando INSERT:

### Inserir um Único Registro

Para inserir um único registro na tabela, você pode usar o seguinte comando:

**INSERT INTO tabela (coluna1, coluna2, coluna3) VALUES (valor1, valor2, valor3);**

### Exemplo 

```sql
INSERT INTO funcionarios (nome, cargo, salario) VALUES ('João', 'Analista de Dados', 5000);
```

Neste exemplo, estamos inserindo um novo funcionário na tabela 'funcionarios', especificando o nome como 'João', o cargo como 'Analista de Dados' e o salário como 5000.


### Inserção de Múltiplos Registros

Você também pode inserir múltiplos registros de uma vez usando o seguinte formato:

```sql
INSERT INTO tabela (coluna1, coluna2, coluna3) VALUES
(valor1_1, valor2_1, valor3_1),
(valor1_2, valor2_2, valor3_2),
(valor1_3, valor2_3, valor3_3);
```

Neste caso, cada conjunto de valores entre parênteses representa um novo registro a ser inserido na tabela.

Lembre-se sempre de substituir 'tabela', 'coluna1', 'coluna2', 'coluna3', 'valor1', 'valor2', 'valor3', etc., pelos nomes reais da sua tabela e das colunas, bem como pelos valores que você deseja inserir.


____
## Exemplo de `UPDATE`

O comando UPDATE é usado para atualizar dados existentes em uma tabela. Aqui está um exemplo de como usar o comando UPDATE:

### Atualizar um Único Registro

Para atualizar um único registro na tabela, você pode usar o seguinte comando:

**UPDATE tabela SET coluna1 = novo_valor WHERE condição;**

### Exemplo 

```sql
UPDATE funcionarios SET salario = 5500 WHERE nome = 'João';
```

Neste exemplo, estamos atualizando o salário do funcionário com o nome 'João' para 5500.

Lembre-se sempre de substituir 'tabela', 'coluna1', 'novo_valor', 'condição', etc., pelos nomes reais da sua tabela e das colunas, bem como pelos valores que você deseja atualizar.


____
## Exemplo de DELETE

O comando DELETE é usado para excluir dados de uma tabela. Aqui está um exemplo de como usar o comando DELETE:

### Excluir um Único Registro

Para excluir um único registro da tabela, você pode usar o seguinte comando:

***DELETE FROM tabela WHERE condição;**

### Exemplo 

```sql
DELETE FROM funcionarios WHERE nome = 'João';
```

Neste exemplo, estamos excluindo o registro do funcionário com o nome 'João' da tabela 'funcionarios'.

Lembre-se sempre de substituir 'tabela', 'condição', etc., pelos nomes reais da sua tabela e pelas condições específicas que você deseja usar para excluir os registros.


____
## Exemplo de CREATE TABLE

O comando CREATE TABLE é usado para criar uma nova tabela. Aqui está um exemplo de como usar o comando CREATE TABLE:
Para criar uma nova tabela, você pode usar o seguinte comando:

```sql
CREATE TABLE tabela (
    coluna1 tipo_dado,
    coluna2 tipo_dado,
    ...
);
```

### Exemplo 

Aqui está um exemplo completo de como usar o comando CREATE TABLE:

```sql
CREATE TABLE funcionarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(50),
    cargo VARCHAR(50),
    salario DECIMAL(10, 2)
);
```

Neste exemplo, estamos criando uma nova tabela chamada 'funcionarios' com as colunas 'id', 'nome', 'cargo' e 'salario'.

Lembre-se sempre de substituir 'tabela', 'coluna1', 'coluna2', etc., pelos nomes reais da sua tabela e das colunas, bem como pelos tipos de dados que você deseja usar para cada coluna.


____
## Exemplo de DROP TABLE
O comando DROP TABLE é usado para excluir uma tabela existente. Aqui está um exemplo de como usar o comando DROP TABLE:
Para excluir uma tabela existente, você pode usar o seguinte comando:

```sql
DROP TABLE tabela;
```

### Exemplo

Aqui está um exemplo completo de como usar o comando DROP TABLE:

```sql
DROP TABLE funcionarios;
```
Neste exemplo, estamos excluindo a tabela 'funcionarios' do banco de dados.

Lembre-se sempre de substituir 'tabela' pelo nome real da tabela que você



