# Infrastructure and Cloud Computing
# Professor: João Henrique Victorino da Silva 

## Atividade 1
### Decrição
#### Subir uma máquina virtual, usando Vagrant, com MySQL instalado e que esteja acessível no host da máquina na porta 3306. Enviar a URL Github do código. Atividade individual ou em grupo, vocês que definem.

# Box Utilizada
## Nome: anhdht/mysql
## Versão: 0.0.1
## Descrição da VM utilizada: CentOS 7.3.1611 com Mysql5.7

# Passos

1. Clone o repositório: https://github.com/vinicius-schulz/vagrant-mysql57.git
2. Navegue até o diretório
3. Execute o comando para subir o box

`vagrant up`

4. Execute o comando para acessar o terminal via ssh

`vagrant ssh`

5. Execute o comando para entrar logar no Mysql via terminal

`mysql -u root -p`

6. Informe o password

 `F&Bb7_T!$RNkgMKn`

7. Execute os comandos a seguir para criar um banco de dados e uma tabela

CREATE DATABASE dbvagrant;
USE dbvagrant;
CREATE TABLE Exercicio (
  idExercicio mediumint(8) unsigned NOT NULL auto_increment,
  descricao varchar(255),
  dataEntrega DATE,
  nomeProfessor varchar(255),
  PRIMARY KEY (`idExercicio`)
) AUTO_INCREMENT=1;

INSERT INTO Exercicio(descricao,dataEntrega,nomeProfessor) VALUES ('Exercicio 1', STR_TO_DATE('21-04-2021', '%d-%m-%Y'), "Joao Henrique Victorino da Silva");

SELECT * FROM Exercicio;
