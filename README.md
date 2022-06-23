# Trabalho de Banco de dados sobre Clinica Odontológica

Descrição: Este trabalho tem como objetivo realizar um banco de dados funcional para uma clínica Odontológica.


## Estudo de caso 

### Descrição de problema

<p> Uma clínica odontológica deseja automatizar os dados dos pacientes e funcionários da empresa, bem como os procedimentos feitos no dia a dia para facilitar na organização dos dentistas e para melhorar o atendimento.</p>
<p>Cada paciente tem seu cadastro feito com seu nome, RG, CPF, data de nascimento, endereço e telefone para contato. Para uma maior familiaridade com cada caso, é atribuido um dentista responsável pelo paciente. Além disso, a pessoa pode ter ou não um convênio.</p>
<p>Para os funcionários é necessário armazenar seus dados essenciais como: nome, RG, CPF, data de nascimento, endereço e telefone; bem como dados sobre seu cargo dentro da empresa, como: função, data de admisão e salário. No caso dos dentistas, também é necessário o profissonal ter registro no Conselho Regional de Odontologia (CRO).</p>
<p>Para receber um atendimento a pessoa deve ligar ou ir até o local a realizar um agendamento com a secretária, esta que anotara na agenda do dentista responsável uma data e um horário. Um atendimento também pode ser marcado pelo destita como retorno, por exemplo. Cada atendimento é agrupado em um histórico vinculado a um determinado paciente.</p>
<p>A clínica realiza diversos tipos de tratamentos, cada um tendo um valor. Alguns dos tratamentos oferecidos são: restauração, exodontia, profilaxia e clareamento.
<p>Caso necessário, o dentista pode visualizar através de buscas, relatórios para saber sua agenda, ou até mesmo, os tipos de procedimentos que determinado paciente já realizou</p>
<p>Os pagamentos são feitos por atendimento, sendo somado os valores dos procedimentos realizados. As formas de pagamento são à vista (dinheiro e/ou pix), pelo cartão (crédito(sendo possível parcelar) ou débito) ou pelo plano de convênio.</p>
 

### Entidades

- Ficha de pacientes
- Ficha de funcionários: dentistas, secretaria, serviços gerais, assistente
- Ficha de atendimento
- Tratamentos 
- Endereço

### Dados usados

#### Paciente

- Nome
- RG
- PK.CPF
- Data de nascimento
- FK.endereço
- FK.historico
- idade(derivado)
- convenio
- Fk.funcionario.dentista
- telefone (multivalorado)

#### Funcionário

- nome
- RG
- PK.CPF
- Data de nascimento
- Fk.endereço
- data_de_admissao
- salario

##### Funcionário - Dentista

- Registro_cro


#### Atendimento

- Pk.codigo
- data
- horario
- Fk.paciente
- Fk.tratamento
- Fk.funcionario.dentista
- valorconsulta

#### Tratamentos

- PK.codigo
- nome
- descrição
- valor
- higienista

#### Endereço

- PK.nome_rua
- bairro
- PK.numero
- cidade
- complemento
- cep  


#### Pesquisas

- Historico
- Agenda

[Link DER - Lucidchart](https://lucid.app/lucidchart/34535290-0ab0-4b0e-8398-63a4e77c680c/edit?viewport_loc=-22%2C-63%2C1707%2C811%2C0_0&invitationId=inv_4a6fa071-3d2c-4ad0-8e58-d4ed4171b2cb#)

[Normas de modelo de trabalho](https://cpaq.ufms.br/files/2015/12/Manual-de-TCC-e-disserta%c3%a7%c3%a3o-CPAQ_2015-final.pdf)

[Relatório](https://docs.google.com/document/d/1PVSVij_mD9Wk7Evudv_OhAdMX3Gif6_4fMBisodMtHs/edit)

[Modelo Relacional](https://lucid.app/lucidchart/991b43b4-cc57-4913-b64f-381823e5b01c/edit?viewport_loc=-198%2C-148%2C2678%2C1247%2C0_0&invitationId=inv_4d1c43e7-5902-4e21-bee4-521856298d4b#)
