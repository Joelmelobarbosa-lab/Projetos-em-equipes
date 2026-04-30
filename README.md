# MicroEmprise💲


📝 **Resumo**
#
Este projeto visa a criação de uma plataforma de redes para pequenos negócios, contendo funcionalidades para divulgação, localização de microempresas, requisição de vagas,  contatos por contas e telefones comerciais. O projeto tem o estruturamento focado em segurança, usabilidade e escalabilidade, representando uma simulação de uma plataforma para pequenos negócios modernos

---

🔍 **Metodologia** 
Para o projeto será efetuado as seguintes metodologia ágil:

-  Analise de Requisitos

-  Diagramas

-  Dados

-  Wireframe


# 


🖥️ **Infraestrutura técnica:**  

🖌️ **Frontend**



>![Static Badge](https://img.shields.io/badge/React-lightblue?style=flat&logo=react&logoColor=grey&logoSize=auto&color=lightblue) ![Static Badge](https://img.shields.io/badge/HTML%205-F06529?style=flat&logo=html5&logoColor=white&labelColor=F06529&color=F06529) ![Static Badge](https://img.shields.io/badge/CSS-663399?style=flat&logo=css&logoColor=white&logoSize=auto&labelColor=663399&color=663399)



⚙️ **Backend**

>![Static Badge](https://img.shields.io/badge/Python-FFD43B?style=flat&logo=Python&logoColor=white&labelColor=4B8BBE&color=FFD43B)


📗 **Banco de Dados:**

>![Static Badge](https://img.shields.io/badge/Mysql-FFB74D?style=flat&logo=mysql&logoColor=blue&logoSize=auto&color=FFB74D)

⚙️**API:**
>![Static Badge](https://img.shields.io/badge/PHP-B0B3D6?style=flat&logo=Php&logoColor=white&logoSize=auto&color=B0B3D6)

***
# 
Links:

#
Figma:

https://www.figma.com/site/cAaLpDDzVVnwDMzIleBnWR/Pagina-da-Loja?node-id=0-1&p=f&t=zzLp9eq6hu864sln-0

https://www.figma.com/design/8LXnelaVwPsWJ20fdDzQJB/Untitled?node-id=0-1&t=HkXyw90WrRvsFW0C-1

#

#
**Equipe**

- Joel de Melo Barbosa
- Isabelly Cristina Martins
- Fernando Henrique Hiroshi Waki

---
*Diagramas:*

___
_Caso(`graph TD`)_

```mermaid
graph TD
A[Cliente]-->C[Pesquisa os sites]
A-->D(Visualiza os site)

B[Empresário]-->E(Armazena o site) 
B-->F(Editar o site) 
B-->G(Ver informações do site)
`````
***
_Estado(`stateDiagram`)_
```mermaid
stateDiagram
[*]-->Armazenar : novo site adicionado na plataforma
Armazenar--> Editar : Modificação da interface de apresentação do site
Editar--> Tela : Adição de informações da interface do site
Tela-->[*] : Site finalizado
`````
```mermaid
stateDiagram
[*]-->Pesquisa : Busca pelo site solicitado
Pesquisa --> Visualizar : Site achado
Visualizar--> [*]

`````
***
_Sequencia(`sequenceDiagram`)_

**Banho&tosa**
#

%%Cadastor_clientes
```mermaid
sequenceDiagram
actor empresario
participant sistema
participant banco

empresario->>sistema: Cadastrar cliente
sistema->>banco: Permissão de adição de novo cliente
banco-->>banco: examina se dados novos já existem
banco-->>sistema: confirmar a adição
sistema-->>empresario: "cliente cadastrado com sucesso"

`````

%%Agenda


_Agendamento de horário e escolhas de espécies de pets e pedidos_
```mermaid
sequenceDiagram
actor cliente
participant sistema
participant agenda 
participant evento

cliente->>sistema: agenda o horário com o dados do pet e a do pedido 
sistema->>agenda: Requere o agendamento do novo pedido 
agenda->>evento:  Requisita a implementação do pedido
evento-->>evento: Checa se há vaga disponível e adicionar dados
evento-->>agenda: Confirma o horário livre e de adição de dados
agenda-->>sistema: Aprova o novo pedido
sistema-->>cliente: "horário agendado com sucesso" 
`````
#
**Panificadora da Alameda (Sem nome)**
```mermaid
sequenceDiagram
actor padeira
participant sistema
participant dados

padeira->>sistema: Cadastrar produtos
sistema->>dados: Solicita o acréscimo de novos produtos
dados-->>dados: Verifica se produto existe
dados-->>sistema: Confirma cadastro de produto
sistema-->> padeira: "Produto acrescentado com sucesso"


`````
_Envio de Notificações_
```mermaid
sequenceDiagram
actor padeira
participant sistema
actor cliente

padeira->>sistema: Solicita o envio da notificação 
sistema->>cliente: Envia a notificação
cliente-->> sistema: confirma o envio
sistema-->>padeira: Notificação enviado com sucesso

`````

#

**Melina Fóz - Psicoclínica**
#
```mermaid
sequenceDiagram
actor proprietaria
participant sistema
participant banco

proprietaria->>sistema: Cadastrar paciente
sistema->>banco: Salvar dados pessoais
banco-->>banco: Verifica os dados pessoais
banco-->>sistema: Confirma cadastro
sistema-->>proprietaria: "Cadastro feito com sucesso"

proprietaria->>sistema: Registrar anamnese
sistema->>banco: Salvar anamnese
banco->>banco: Verifica anamnese existente
banco-->>sistema: Registro concluído
sistema-->>proprietaria: "Registro feito com sucesso"

`````
%% Consulta

```mermaid
sequenceDiagram
actor proprietaria
participant sistema
participant banco

proprietaria->>sistema: Registrar resultado da consulta
sistema->>banco: Salvar evolução do paciente
banco-->>sistema: Confirma salvamento
sistema-->>proprietaria: "Consulta marcada com sucesso"
`````

%% Agenda

```mermaid
sequenceDiagram
actor proprietaria
participant sistema
participant banco

proprietaria->>sistema: Criar consulta/tarefa na agenda
sistema->>banco: Salvar evento
banco-->>sistema: Evento armazenado
sistema-->>proprietaria: "Evento agendado com sucesso"
`````
%% Documentos

##Salvar_Arquivo
```mermaid
sequenceDiagram
actor proprietaria
participant sistema
participant banco

proprietaria->>sistema: Criar documento
sistema->>banco: Salvar arquivo
banco-->>sistema: Arquivo salvo
sistema-->>proprietaria: "Arquivo salvo com sucesso"
`````
##Enviar_Arquivo

```mermaid
sequenceDiagram
actor proprietaria
participant sistema
actor paciente

proprietaria->>sistema: Enviar documento ao paciente
sistema->>paciente: Documento enviado
paciente-->>sistema: Confirmação de envio
sistema-->>proprietaria:"Documento enviado com sucesso"

`````
