# DADOS-DO-SQL
# 🚀 Dominando MySQL em 1 Hora — Guia Prático

<p align="center">
  <b>Um guia visual e direto ao ponto para aprender Banco de Dados Relacional e comandos SQL.</b>
</p>

---

## 📌 Resumo dos Comandos Principais (CRUD)

| Comando | Operação | Exemplo Prático |
| :--- | :--- | :--- |
| **`CREATE`** | Cria banco ou tabelas | `CREATE TABLE alunos (id INT, nome VARCHAR(100));` |
| **`INSERT`** | Insere novos dados | `INSERT INTO alunos (nome) VALUES ('Ana');` |
| **`SELECT`** | Consulta registros | `SELECT * FROM alunos WHERE id = 1;` |
| **`UPDATE`** | Modifica dados existentes | `UPDATE alunos SET nome = 'Ana Souza' WHERE id = 1;` |
| **`DELETE`** | Remove registros | `DELETE FROM alunos WHERE id = 1;` |

---

## ⚡ Código Completo em uma Única Página

Abaixo está a síntese de todo o código necessário para criar o banco de dados, criar a tabela, cadastrar dados e realizar alterações:

```sql
-- =======================================================
-- 1. ESTRUTURA (schema)
-- =======================================================
CREATE DATABASE IF NOT EXISTS escola;
USE escola;

CREATE TABLE IF NOT EXISTS alunos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(100) NOT NULL,
    curso VARCHAR(50) NOT NULL,
    idade INT
);

-- =======================================================
-- 2. DADOS E OPERAÇÕES (data)
-- =======================================================
USE escola;

-- Inserindo registros
INSERT INTO alunos (nome, curso, idade) VALUES 
('Ana Silva', 'Sistemas de Informação', 21),
('Carlos Souza', 'Engenharia de Software', 23),
('Mariana Lima', 'Análise de Sistemas', 19);

-- Consultando todos os dados
SELECT * FROM alunos;

-- Atualizando registro (Sempre use WHERE!)
UPDATE alunos SET curso = 'Ciência da Computação' WHERE id = 1;

-- Deletando registro (Sempre use WHERE!)
DELETE FROM alunos WHERE id = 2;

-- Consultando o resultado final
SELECT * FROM alunos;
