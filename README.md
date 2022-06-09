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



