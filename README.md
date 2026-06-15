# Sistemas Distribuídos

Projeto desenvolvido no âmbito da unidade curricular de Sistemas Distribuídos.

O projeto consiste numa aplicação cliente-servidor em Java, baseada numa ligação por frames, que permite a vários clientes interagir com um serviço de armazenamento de pares chave-valor.

## Autores

* João Pedro Carvalho - a104533
* Diogo Ferreira - a104266
* David Figueiredo - a104360

## Descrição

A aplicação permite que um cliente se ligue ao servidor, faça autenticação e execute operações sobre um sistema de armazenamento distribuído.

O cliente comunica com o servidor através de uma ligação estruturada por frames, permitindo enviar pedidos e receber respostas de forma organizada. O sistema suporta operações simples e múltiplas sobre pares chave-valor.

## Funcionalidades

* Registo de utilizadores.
* Login de utilizadores.
* Alteração de password.
* Inserção de valores com `put`.
* Consulta de valores com `get`.
* Inserção múltipla com `multiPut`.
* Consulta múltipla com `multiGet`.
* Consulta condicionada com `getWhen`.
* Comunicação cliente-servidor através de uma ligação framed.
* Interface de consola para interação com o utilizador.

## Tecnologias utilizadas

* Java
* Sockets
* Programação cliente-servidor
* Comunicação por frames
* Makefile

## Estrutura do projeto

```text id="x18s9p"
.
├── README.md
├── Makefile
├── META-INF
│   └── MANIFEST.MF
├── client
├── connection
└── server
```

## Como compilar

A partir da raiz do projeto, executar:

```bash id="a2n41s"
make
```

ou:

```bash id="yt82h8"
make compile
```

Para limpar os ficheiros `.class` gerados:

```bash id="ri84bz"
make clean
```

## Como executar

Depois de compilar o projeto, deve ser iniciado primeiro o servidor e só depois o cliente.

Exemplo para executar o cliente:

```bash id="p2fwk7"
java client.Client
```

No cliente, o utilizador pode criar conta, iniciar sessão, alterar a password e aceder ao menu principal com as operações disponíveis.

## Menu principal do cliente

Após a autenticação, o cliente apresenta opções como:

```text id="x9e4ji"
1. Put
2. Get
3. MultiPut
4. MultiGet
5. GetWhen
6. Exit
```

## Operações suportadas

### Put

Permite guardar um valor associado a uma chave.

### Get

Permite obter o valor associado a uma chave.

### MultiPut

Permite guardar vários pares chave-valor de uma só vez.

### MultiGet

Permite obter vários valores a partir de um conjunto de chaves.

### GetWhen

Permite obter um valor apenas quando uma determinada condição sobre outra chave for satisfeita.

## Estado do projeto

O projeto contém a implementação base de uma aplicação distribuída cliente-servidor, com autenticação de utilizadores, comunicação por frames e operações sobre armazenamento chave-valor.
