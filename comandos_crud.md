## Comandos SQL para operações de dados (CRUD)

## Resumo

C: CREATE (criar dados usando o comando INSERT)
R: READ (ler dados usando o comando SELECT)
U: UPDATE (atualizar dados usando o comando UPDATE)
D: DELETE (excluir dados usando o comando DELETE)

## INSERT

### Tabela Fabricantes

```sql
INSERT INTO fabricantes (nome) VALUES ('Microsoft');
INSERT INTO fabricantes (nome) VALUES ('Asus');
INSERT INTO fabricantes (nome) VALUES ('Dell');
INSERT INTO fabricantes (nome) VALUES ('IBM');
INSERT INTO fabricantes (nome) VALUES ('Brastemp');

INSERT INTO fabricantes (nome) 
VALUES ('Apple'), ('Samsung'), ('LG'), ('HP');
```
### Tabela Produtos

```sql
INSERT INTO produtos (nome, descricao, fabricante_id) 
VALUES ('Ultrabook', 'Laptop de última geração com processador Intel Core I9 de 16GB RAM.', 3);

INSERT INTO produtos (nome, descricao, fabricante_id) 
VALUES ('Tablet Android', 'Tablet com a versão 13 do sistema Android, com tela de 10 plegadas e 64GB de Armazenamento', 6);

INSERT INTO produtos (nome, descricao, fabricante_id) 
VALUES ('iPhone 13 Pro Max
', 'Alta durabilidade, processador XYZ 14, 128 GB de armazenamento, 6 GB de RAM e caro pra caramba.
', 5);

INSERT INTO produtos (nome, descricao, fabricante_id) 
VALUES ('Geladeira', 'Refrigerador frost-free com acesso à Internet e bla bla bla.
', 9);

INSERT INTO produtos (nome, descricao, fabricante_id) 
VALUES ('Xbox 123', 'Vídeo-game de última geração.', 1);

INSERT INTO produtos (nome, descricao, fabricante_id) 
VALUES ('iPad Mini', 'Tablet Apple com tela retina de 4k.', 5);

INSERT INTO produtos (nome, descricao, fabricante_id) 
VALUES ('Ultrabook', 'Equipamento com processador AMD Ryzen, 12 GB de RAM.', 2);
```

## SELECT

### Ler dados da tabela Produtos

```sql
SELECT * FROM produtos;

SELECT nome FROM produtos;

SELECT nome, descricao FROM produtos;

SELECT nome FROM produtos WHERE fabricante_id = 5; 

-- OPERADOR DIFERENTE : != ou <>
SELECT nome FROM produtos WHERE fabricante_id != 5; 
SELECT nome FROM produtos WHERE fabricante_id <> 5; 

-- OPERADOR OU: OR
SELECT nome, descricao FROM produtos
WHERE fabricante_id = 2 OR fabricante_id = 3; 

```