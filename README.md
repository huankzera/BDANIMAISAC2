# BDAnimais

## ETAPA 1
 -- Criando a tabela  "Animais" com as colunas, ID, NOME, NASC , PESO  e COR. --
 
CREATE TABLE Animais (
  ID INT,
  NOME VARCHAR(50),
  NASC DATE,
  PESO DECIMAL(10, 2),
  COR VARCHAR(50)
);

-- inserindo dados na tabela "Animais" --

insert into Animais values (01, 'Ágata', date'2016-06-06', 13.9, 'branco');
insert into Animais values (02, 'Félix', date'2016-06-06', 14.3, 'preto');
insert into Animais values (03, 'Tom', date'2013-02-08', 11.2, 'azul');
insert into Animais values (04, 'Garfield', date'2015-07-06', 17.1, 'laranja');
insert into Animais values (05, 'Frajola', date'2013-08-01', 13.7, 'preto');
insert into Animais values (06, 'Manda-chuva', date'2012-02-03', 12.3, 'amarelo');
insert into Animais values (07, 'Snowball', date'2014-04-06', 13.2, 'preto');
insert into Animais values (10, 'Ágata', date'2015-08-03', 11.9, 'azul');
insert into Animais values (11, 'Gato de Botas', date'2012-12-10', 11.6, 'amarelo');
insert into Animais values (12, 'Kitty', date'2020-04-06', 11.6, 'amarelo');
insert into Animais values (13, 'Milu', date'2013-02-04', 17.9, 'branco');
insert into Animais values (14, 'Pluto', date'2012-01-03', 12.3, 'amarelo');
insert into Animais values (15, 'Pateta', date'2015-05-01', 17.7, 'preto');
insert into Animais values (16, 'Snoopy', date'2013-07-02', 18.2, 'branco');
insert into Animais values (17, 'Rex', date'2019-11-03', 19.7, 'bege');
insert into Animais values (20, 'Bidu', date'2012-09-08', 12.4, 'azul');
insert into Animais values (21, 'Dum Dum', date'2015-04-06', 11.2, 'laranja');
insert into Animais values (22, 'Muttley', date'2011-02-03', 14.3, 'laranja');
insert into Animais values (23, 'Scooby', date'2012-01-02', 19.9, 'marrom');
insert into Animais values (24, 'Rufus', date'2014-04-05', 19.7, 'branco');
insert into Animais values (25, 'Rex', date'2021-08-19', 19.7, 'branco');
insert into Animais values (25, 'Cerato', date'2021-08-19', 19.7, 'branco');
insert into Animais values (25, 'Carlos', date'2021-08-19', 19.7, 'marrom');
insert into Animais values (25, 'Roberto', date'2021-08-20', 31.2, 'roxo');
insert into Animais values (25, 'Clayton', date'2021-12-28', 31.2, 'roxo');
insert into Animais values (25, 'Rircardo', date'2021-12-22', 31.2, 'roxo');

-- Mostra todos os animais inseridos --

SELECT * from Animais;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/d53e8f16-8d13-4d9f-bf2d-cf01996f6c02)



-- Mostra os animais da tabela onde o PESO é maior que 13.1. --

SELECT * FROM Animais WHERE PESO > 13.1;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/22eb0e42-a59d-4402-90a1-b9589f66d467)


-- Mostra os animais com a data de nascimento entre o intervalo de 1 de fevereiro de 2015 a 31 de dezembro de 2015. --

SELECT * FROM Animais Where NASC >= "2015-02-01" AND NASC <= "2015-12-31";
SELECT * FROM Animais Where NASC BETWEEN "2015-02-01" AND "2015-12-31";

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/f9cfeb99-bda0-4a4f-9904-c8696dcc4366)


--  Mostra os animais que tem a cor "branco" e o peso é maior que 15.0. --

SELECT * FROM Animais WHERE COR = "branco" AND PESO > 15.0;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/9a4d7c8a-d4e8-48ff-8d64-c3cbcf898b44)


-- Mostra os animais cujos nomes começam com a letra "b". --

SELECT NOME, COR, PESO FROM Animais Where NOME LIKE "b%";

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/fa6919a8-6534-4eea-8aa6-4afcd76a06ad)


--  Mostra os nomes, cores e pesos dos animais com cores "vermelho", "amarelo", "marrom" ou "laranja". --

SELECT NOME, COR, PESO FROM Animais  
WHERE COR = "vermelho" OR COR = "amarelo" OR  COR = "marrom" OR COR = "laranja";

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/aaa89452-44c2-4625-89ec-508ad334958f)


-- Mostra os animais ordenados por data de nascimento em ordem decrescente. --

SELECT NOME, COR, NASC, PESO FROM Animais ORDER BY NASC DESC;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/f835c052-9b56-43ee-9a36-126f7fd7807f)


-- Mostras os animais cujos nomes começam com "C" e cuja cor não é "branco". --
SELECT * FROM Animais WHERE NOME LIKE "C%" AND COR != "branco";

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/3dc738f8-6333-4e24-a234-545ce8c92f3d)


-- Mostra os animais onde o nome contém a sequência "ba" em qualquer posição. --
SELECT * FROM Animais WHERE NOME LIKE "%ba%";

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/42cb8ecd-84b4-4179-9df4-affa37a447f1)


-- Mostra os animais cujo peso está entre 13.0 e 15.0. --

SELECT * FROM Animais WHERE PESO >= 13.0 AND PESO <= 15.0;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/9a8acfc3-47a5-4c20-9a42-bcba9bb92200)


-- Mostra os animais com peso maior ou igual a 30.0 e que são da cor "amarelo", ou da cor "roxo" e com data de nascimento após 31 de dezembro de 2012. --

SELECT * FROM Animais 
WHERE PESO >= 30.0 AND COR = "amarelo" OR COR = "roxo" AND NASC > "2012-12-31";

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/99969e24-2c8f-4889-9c9a-12bdde43e7f3)


/*DESAFIO 1 - Capricornianos */

-- Mostra os animais cuja data de nascimento corresponde a 1º a 20 de janeiro ou 22 a 31 de dezembro. --

SELECT * FROM Animais 
WHERE MONTH(NASC) = 1 AND DAY(NASC) BETWEEN 1 AND 20 OR MONTH(NASC) = 12 
AND DAY(NASC) BETWEEN 22 AND 31;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/b9b9bbd1-028e-4860-bc16-0157df1a102c)


/*DESAFIO 2 - Nomes compostos*/

-- Mostra os animais cujos nomes contêm um espaço em branco ou seja são compostos. --

SELECT * FROM Animais WHERE NOME LIKE "% %";

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/849b552b-7eee-4f06-8c14-125e173ecbf2)


## ETAPA 2

-- EXERCÍCIO 1 --

/*Criando a tabela de Espécies*/
CREATE TABLE Especies (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Nome VARCHAR(60) NOT NULL,
    Descricao TEXT
);

/*Inserindo os dados na tabela de Espécies*/
INSERT INTO Especies (Nome, Descricao) VALUES
    ('Felinos', 'Mamíferos carnívoros da família Felidae'),
    ('Caninos', 'Mamíferos da família Canidae, incluindo cães e lobos'),
    ('Anfíbios', 'Animais vertebrados que passam parte de seu ciclo de vida na água e parte na terra');

/*Criando a tabela de Animais*/
CREATE TABLE Animais2 (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Nome VARCHAR(60) NOT NULL,
    Data_Nasc DATE,
    Peso DECIMAL(5, 2),
    Especie_ID INT,
    
    FOREIGN KEY (Especie_ID) REFERENCES Especies(ID)
);

/*Inserindo os dados na tabela de Animais*/
INSERT INTO Animais2 (Nome, Data_Nasc, Peso, Especie_ID) VALUES
    ('Tobby', DATE'2015-03-10', 150.5, 1),
    ('Tigrão', DATE'2016-05-20', 140.2, 1),
    ('Camila Cabelo', DATE'2018-01-15', 25.7, 2),
    ('Totó', DATE'2017-11-30', 35.2, 2),
    ('Morgana', DATE'2019-07-08', 0.5, 3),
    ('Jaré', DATE'2020-02-12', 0.3, 3),
    ('Ursa', DATE'2019-09-05', 120.0, 1),
    ('Melman', DATE'2020-04-25', 5.8, 1);

/* Vai juntar as informações das duas tabelas, "Animais2" e "Especies", com base na correspondência das colunas "ID" e "Especie_ID", retornando uma lista de animais com informações sobre suas espécies correspondente*/
SELECT * FROM Animais2 An
INNER JOIN Especies Esp ON Esp.ID = An.Especie_ID;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/5cb9d423-ed08-4328-adb4-a246f3d93dfc)

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/e128f542-e0cf-429c-822c-aad64e69a84e)


-- EXERCÍCIO 2 --

/* Criação da tabela de Marcas */
CREATE TABLE Marcas (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Nome VARCHAR(60) NOT NULL,
    SiteOficial VARCHAR(100),
    Telefone VARCHAR(15)
);

/* Inserção de dados nas tabelas de Marcas */
INSERT INTO Marcas (Nome, SiteOficial, Telefone) VALUES
    ('Nestle', 'https://www.nestle.com', '32437070'),
    ('Dell', 'https://www.dell.com', '32439090'),
    ('AOC', 'https://www.aoc.com', '+32436060');

/* Criação da tabela de Produtos */
CREATE TABLE Produtos2 (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Nome VARCHAR(100) NOT NULL,
    PrecoCusto DECIMAL(10, 2),
    PrecoVenda DECIMAL(10, 2),
    DataValidade DATE,
    Marca_ID INT,
    FOREIGN KEY (Marca_ID) REFERENCES Marcas(ID)
);

/* Inserção de dados nas tabelas de Produtos */
INSERT INTO Produtos2 (Nome, PrecoCusto, PrecoVenda, DataValidade, Marca_ID) VALUES
    ('Chocolate em Barra', 10.50, 19.99, '2023-12-31', 1),
    ('Notebook Dell G15', 599.99, 899.99, '2023-10-15', 2),
    ('Caixa de BomBom', 5.25, 12.49, '2023-11-30', 1),
    ('Smart TV 32', 599.99, 899.99, '2024-02-28', 3),
    ('Achocolatado', 12.00, 24.99, '2023-09-30', 1),
    ('Notebook Dell G 15 RTX 4060', 999.99, 999.99, '2023-12-31', 2),
    ('Café Cremoso em pó', 9.50, 19.99, '2024-01-15', 1),
    ('Smart TV 24', 299.99, 600.99, '2023-10-31', 3);

/* Vai juntar as informações das duas tabelas "Produtos" e "Marcas" com base na correspondência das colunas "Marca_ID" na tabela "Produtos" e "ID" na tabela "Marcas". O resultado é uma lista de produtos e suas respectivas marcas.*/
SELECT * FROM Produtos2 P
INNER JOIN Marcas M ON M.ID = P.Marca_ID;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/a612202a-6faf-4c2c-a5d3-37363d94e49f)

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/6e441bd9-36f4-45f8-8c38-62c0dc930b93)

-- EXERCÍCIO 3 --

/* Criação da tabela de Categorias */
CREATE TABLE Categorias (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Nome VARCHAR(60) NOT NULL,
    PublicoAlvo VARCHAR(30)
);

/* Inserção de dados nas tabelas de Categorias */
INSERT INTO Categorias (Nome, PublicoAlvo) VALUES
    ('Ação', 'Adulto'),
    ('Comédia', 'Família'),
    ('Mágia', 'Livre');

/* Criação da tabela de Filmes */
CREATE TABLE Filmes (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Titulo VARCHAR(100) NOT NULL,
    Sinopse TEXT,
    Estudio VARCHAR(60),
    Categoria_ID INT,
    FOREIGN KEY (Categoria_ID) REFERENCES Categorias(ID)
);

/* Inserção de dados nas tabelas de Filmes */
INSERT INTO Filmes (Titulo, Sinopse, Estudio, Categoria_ID) VALUES
    ('Mercenarios 1', 'Sinopse: Geral matando geral', 'Globo', 1),
    ('Mercenarios 2', 'Sinopse: Geral matando só que mais legal', 'Globo', 1),
    ('Ben 10', 'Sinopse: Garoto pega relogio esquisito e salva o mundo', 'Cartoon Network', 3),
    ('Ben 10 2', 'Sinopse:  Garoto continua com relogio esquisito e salva o mundo de novo ', 'Cartoon Network', 3),
    ('Barbie 1', 'Sinopse: Mulher conta historias ficticias de uma boneca', 'Warner Bros', 3),
    ('Barbie 2', 'Sinopse: Mulher continua a contar historias ficticias de uma boneca', 'Warner Bros', 3),
    ('Era do gelo', 'Sinopse: Animais vivem tranquilamente até que precisam fazer uma migração', 'BlueSky', 2),
    ('Era do gelo 2', 'Sinopse: Animais sofrem com o aquecimento global', 'BlueSky', 2);
    
/* Juntando as tabelas "Filmes" e "Categorias", relacionando filmes com suas categorias por meio da coluna "Categoria_ID".*/
SELECT * FROM Filmes F
INNER JOIN Categorias C ON C.ID = F.Categoria_ID;

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/04d6f959-ff3e-4f79-a57b-6115b3c6d872)

![image](https://github.com/huankzera/BDANIMAISAC2/assets/126423433/16e2e2e6-e273-456d-b719-cd226c55a371)
