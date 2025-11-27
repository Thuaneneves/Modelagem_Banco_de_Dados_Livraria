🏪 Projeto Livraria Saber – Scripts SQL

Este repositório contém os arquivos SQL desenvolvidos para a Experiência Prática de Modelagem e Manipulação de Dados, utilizando MySQL como SGBD.
O projeto implementa a criação, povoamento e manipulação dos dados de um sistema de gestão para uma livraria e papelaria, incluindo vendas, estoque, fornecedores, autores, editoras e relacionamento entre livros e autores.

📁 Estrutura do Repositório – Projeto Livraria Saber

- 📄 **livraria_saber_autor.sql** — Tabela e dados de autores  
- 📄 **livraria_saber_cliente.sql** — Tabela e dados de clientes  
- 📄 **livraria_saber_editora.sql** — Tabela e dados de editoras  
- 📄 **livraria_saber_fornecedor.sql** — Tabela e dados de fornecedores  
- 📄 **livraria_saber_item_venda.sql** — Tabela e dados dos itens de venda  
- 📄 **livraria_saber_livro.sql** — Tabela e dados dos livros  
- 📄 **livraria_saber_livro_autor.sql** — Tabela relacional livro–autor  
- 📄 **livraria_saber_papelaria.sql** — Tabela e dados de produtos de papelaria  
- 📄 **livraria_saber_venda.sql** — Tabela e dados das vendas  
- 📄 **livraria_saber_vendedor.sql** — Tabela e dados dos vendedores  
- 🗄️ **livraria_saber.sql** — Backup completo do banco de dados (estrutura + dados)


📄 Descrição dos Arquivos
livraria_saber_autor.sql
Contém a criação e inserção de dados da tabela autor, incluindo:

- nome
- nacionalidade
- data de nascimento

livraria_saber_cliente.sql
Define a tabela cliente e insere dados como:

- nome
- cpf (único)
- telefone
- email
- endereço

livraria_saber_editora.sql
Criação e povoamento da tabela editora, com informações como:

- nome
- CNPJ
- contato
- telefone
- livraria_saber_fornecedor.sql

Tabela fornecedor contendo fornecedores de itens de papelaria, com:

- nome
- CNPJ
- contato
- telefone

livraria_saber_item_venda.sql

- Tabela associativa dos itens das vendas, contendo:
- quantidade
- preço unitário
- referência para livro ou papelaria

chave composta (id_venda + seq_item)
Inclui uma constraint para garantir que um item seja livro XOR papelaria.

livraria_saber_livro.sql
Criação da tabela de livros, com:

- título
- ISBN (único)
- preço
- estoque
- id da editora

livraria_saber_livro_autor.sql
Tabela de relacionamento N:N entre livros e autores.

livraria_saber_papelaria.sql
Define os produtos de papelaria vendidos pela livraria:

- nome
- marca
- categoria
- preço
- estoque
- fornecedor vinculado

livraria_saber_venda.sql
Tabela responsável pelos registros de vendas:

- data e hora
- forma de pagamento
- valor total
- cliente
- vendedor

livraria_saber_vendedor.sql
Tabela com os vendedores da livraria:

- nome
- cargo
- telefone
- comissão

livraria_saber.sql
Backup completo contendo:

- estrutura de todas as tabelas
- dados inseridos
- relacionamentos e restrições

🛠️ Tecnologias Utilizadas

- MySQL Server 8.x
- MySQL Workbench
- VS Code
- GitHub

▶️ Como Executar os Arquivos
1. Criar o Banco de Dados

No MySQL Workbench:

CREATE DATABASE livraria_saber;
USE livraria_saber;

2. Executar os Scripts

Execute os arquivos na seguinte ordem recomendada:

1. Autores
2. Editoras
3. Fornecedores
4. Clientes
5. Vendedores
6. Livros
7. Papelaria
8. Venda
9. Item Venda
10. Livro_Autor

Ou simplesmente importe o arquivo livraria_saber.sql, que já contém tudo pronto.
