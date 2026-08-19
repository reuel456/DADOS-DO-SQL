# DADOS-DO-SQL
# Projeto Banco de Dados MySQL

Este repositório contém os scripts SQL essenciais para a criação e manipulação do banco de dados `escola`.

## Estrutura do Repositório

- **schema.sql**: Script responsável por criar o banco de dados e a tabela `alunos`.
- **data.sql**: Script responsável por inserir, consultar, atualizar e deletar os registros (operações CRUD).

---

## Arquivo 1: schema.sql

CREATE DATABASE IF NOT EXISTS escola;
USE escola;

CREATE TABLE IF NOT EXISTS alunos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(100) NOT NULL,
    curso VARCHAR(50) NOT NULL,
    idade INT
);

---

## Arquivo 2: data.sql

USE escola;

INSERT INTO alunos (nome, curso, idade) VALUES 
('Ana Silva', 'Sistemas de Informação', 21),
('Carlos Souza', 'Engenharia de Software', 23),
('Mariana Lima', 'Análise de Sistemas', 19);

SELECT * FROM alunos;

UPDATE alunos SET curso = 'Ciência da Computação' WHERE id = 1;

DELETE FROM alunos WHERE id = 2;

SELECT * FROM alunos;

---

## Como Executar

### Via Terminal
```bash
# 1. Criar o banco e a tabela
mysql -u seu_usuario -p < schema.sql

# 2. Inserir e manipular dados
mysql -u seu_usuario -p < data.sql
