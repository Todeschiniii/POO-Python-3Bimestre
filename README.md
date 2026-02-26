# 🎓 Sistema Univap – Gerenciador Acadêmico em Python + MySQL

> Sistema completo de gerenciamento acadêmico via terminal, com integração MySQL e exibição estruturada de dados.

---

# 📑 Sumário

- [📌 Sobre o Projeto](#-sobre-o-projeto)
- [🚀 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [🏗️ Arquitetura do Sistema](#️-arquitetura-do-sistema)
- [💡 Funcionalidades](#-funcionalidades)
- [🗄️ Estrutura do Banco de Dados](#️-estrutura-do-banco-de-dados)
- [🖥️ Exemplo de Uso](#️-exemplo-de-uso)
- [🔐 Validações e Segurança](#-validações-e-segurança)
- [📈 Diferenciais Técnicos](#-diferenciais-técnicos)
- [⚙️ Como Executar](#️-como-executar)
- [📊 Melhorias Futuras](#-melhorias-futuras)
- [👨‍💻 Autor](#-autor)
- [📄 Licença](#-licença)
- [👥 Créditos & Contatos](#-créditos--contatos)

---

# 📌 Sobre o Projeto

O **Sistema Univap** é uma aplicação desenvolvida em Python para gerenciamento de dados acadêmicos utilizando MySQL como banco de dados relacional.

O sistema permite:

- 📚 Gerenciamento de Disciplinas  
- 👨‍🏫 Controle de Professores  
- 🔗 Associação entre Disciplinas e Professores  
- 📊 Visualização formatada de dados no terminal  
- 🔍 Operações completas de CRUD (Create, Read, Update, Delete)  

O projeto demonstra domínio em:

- Integração Python + MySQL
- Estruturação modular de código
- Tratamento de exceções
- Validação de dados
- Organização de sistemas backend

---

# 🚀 Tecnologias Utilizadas

- Python 3
- MySQL
- mysql-connector-python
- PrettyTable

Instalação das dependências:

```bash
pip install mysql-connector-python prettytable
```

---

# 🏗️ Arquitetura do Sistema

O sistema foi estruturado em camadas lógicas:

```
Banco de Dados
    ↓
Camada de Conexão
    ↓
Funções CRUD
    ↓
Menu Interativo
```

### Organização interna

- Função de conexão centralizada
- Funções específicas para cada operação
- Sistema de formatação desacoplado via dicionário
- Validação antes de operações críticas

---

# 💡 Funcionalidades

## ✔ Conexão com Banco de Dados

- Conexão com MySQL
- Verificação de status
- Tratamento de erros

## ✔ Exibição de Tabelas

- Visualização formatada com PrettyTable
- Aplicação automática de formatação:

| Campo                     | Formatação Aplicada       |
|---------------------------|---------------------------|
| Telefone do Professor     | (XX) XXXXX-XXXX           |
| Idade do Professor        | XX anos                   |
| Sálario do Professor      | R$ XX.XX                  |
| Ano Letivo                | Xº ano                    |
| Carga Horária             | XXmin                     |

## ✔ CRUD Completo

- Cadastrar
- Consultar
- Alterar
- Excluir

Com validações:

- Verificação de código existente
- Confirmação antes da exclusão
- Bloqueio de alteração de chave primária
- Tratamento de exceções SQL

---

# 🗄️ Estrutura do Banco de Dados

O sistema utiliza três tabelas principais:

## 📘 disciplinas

- codigodisc
- nomedisc

## 👨‍🏫 professores

- registro
- nomeprof
- telefoneprof
- idadeprof
- salarioprof

## 🔗 disciplinasxprofessores

- codigodisciplinanocurso
- codigoprof
- codigodisc
- curso
- cargahoraria
- anoletivo

---

# 🖥️ Exemplo de Uso

Entrada inicial:

```bash
Deseja entrar no Sistema Univap?
[S] - Sim
```

Menu de visualização:

```
<=== MOSTRAR TABELAS ===>
[D] - disciplinas
[P] - professores
[DXP] - disciplinasxprofessores
```

Menu de operações:

```
[C] - Cadastrar
[CO] - Consultar
[A] - Alterar
[E] - Excluir
```

Exemplo de comando:

```
CO/P
```

---

# 🔐 Validações e Segurança

- Validação de entrada numérica
- Verificação prévia antes de alterações
- Confirmação obrigatória para exclusão
- Uso de placeholders em INSERT e UPDATE
- Tratamento global de exceções

---

# 📈 Diferenciais Técnicos

- Estrutura modular organizada
- Sistema dinâmico de formatação via dicionário
- Separação clara de responsabilidades
- Código legível e escalável
- Interface amigável em terminal
- Aplicação prática de SQL integrado ao Python

---

# ⚙️ Como Executar

1️⃣ Configure o MySQL:

- Banco: `univap`
- Ajuste usuário e senha na função `abrebanco()`

2️⃣ Execute o programa:

```bash
python nome_do_arquivo.py
```

---

# 📊 Melhorias Futuras

- Interface gráfica (Tkinter)
- Versão Web com Flask
- Implementação de ORM (SQLAlchemy)
- Sistema de autenticação
- Arquitetura MVC
- API REST
- Logs estruturados

---

# 📄 Licença

Projeto desenvolvido para fins educacionais.

---

# # 👥 Créditos & contatos

1. <b>Mateus Todeschini</b> - GitHub: https://github.com/Todeschiniii<br>
2. <b>Heitor Pinheiro</b> - GitHub: https://github.com/HeitorPinheiro11<br>
3. <b>Davi Dancuart<b> - GitHub: https://github.com/DaviDancuart<br>

Repositório: https://github.com/AEV-autoescola-Virtual/Simulador-de-Carro-teste
