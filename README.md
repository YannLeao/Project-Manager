# Sistema de Gerenciamento de Projetos

## Ferramentas utilizadas

<div align="left">
  <img src="https://img.shields.io/badge/Java-F89820?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Java_Swing-007396?style=for-the-badge&logo=java&logoColor=white" alt="Java Swing">
</div>

## 📝 Descrição

Este repositório contém a implementação de um sistema de gerenciamento de projetos, desenvolvido como parte da disciplina de Programação 2 da Universidade Federal Ruaral de Pernambuco (UFRPE). 

## 📋 Parte I - CRUD e Estrutura

Baseado no sistema de aplicações CRUD, acrônimo para Create (criar), Read (ler), Update (atualizar) e Delete (apagar).
O sistema permite a criação de projetos e o gerenciamento das respectivas tarefas, oferecendo funcionalidades como adicionar tarefas, atualizar status, e buscar projetos. 
Cada projeto e tarefa possui um identificador único, além de informações relevantes como descrição, status e datas de início e término.


### ⚙️ Funcionalidades Principais

- **Adicionar um novo projeto**: O sistema permite criar novos projetos, fornecendo nome, descrição e a lista inicial de tarefas.
- **Adicionar tarefas a um projeto**: Dentro de cada projeto, o usuário pode adicionar múltiplas tarefas, cada uma com informações detalhadas.
- **Atualizar o status de uma tarefa**: O status de uma tarefa pode ser alterado entre "Pendente", "Em Andamento" e "Concluída".
- **Listar todos os projetos com suas tarefas**: Exibe uma visão geral de todos os projetos cadastrados e suas respectivas tarefas.
- **Buscar um projeto pelo ID**: Possibilita a busca rápida e eficiente de projetos através de seu identificador único.
- **Remover um projeto ou tarefa**: Usuários podem excluir projetos completos ou tarefas específicas.

### 🛠️ Estruturas de Dados

- **Map<Integer, Projeto>**: Utilizado para armazenar os projetos, permitindo uma busca eficiente pelo ID do projeto.
- **List<Tarefa>**: Cada projeto mantém uma lista de suas respectivas tarefas, facilitando a manipulação e consulta.

### 📂 Classes e Responsabilidades

#### GerenciadorDeProjetos

Essa classe atua como o núcleo do sistema, sendo responsável pela gestão central dos projetos. Suas principais responsabilidades incluem:

- Armazenar os projetos em um `Map<Integer, Projeto>`, garantindo buscas eficientes.
- Métodos para adicionar, remover e buscar projetos.
- Listar todos os projetos e suas tarefas.

#### Projeto

A classe `Projeto` representa um projeto individual, contendo:

- Uma lista de tarefas (`List<Tarefa>`).
- Métodos para adicionar e remover tarefas ao projeto.
- Informações como nome e descrição do projeto.

#### Tarefa

Cada `Tarefa` é parte de um projeto e inclui informações como:

- Nome, descrição e status (usando um enum que pode ser "Pendente", "Em Andamento" ou "Concluída").
- Datas de início e término (manipuladas usando `LocalDate`).
- Métodos para atualizar o status da tarefa.

### 🔧 Estrutura do Projeto

- **GerenciadorDeProjetos.java**: Implementa o controle principal do sistema.
- **Projeto.java**: Define a classe para os projetos, contendo métodos para gerenciar as tarefas.
- **Tarefa.java**: Define a classe para as tarefas com suas respectivas propriedades e métodos.
- **Main.java**: Contém o ponto de entrada do programa, lidando com a interação do usuário.
- **Menu.java**: Classe auxiliar para exibir o menu de opções e capturar as interações do usuário.

### 🚀 Otimizações Implementadas

Durante o desenvolvimento, realizei algumas melhorias para otimizar o código:

- **Eficiência de busca**: A escolha de um `Map` para armazenar os projetos permite uma recuperação rápida e eficiente dos projetos pelo ID.
- **Validação de dados**: Foram implementadas validações nos métodos de manipulação de tarefas e projetos, como checagem de IDs e verificação de status.
- **Modularidade**: O sistema foi estruturado em classes separadas, cada uma com responsabilidades claras, facilitando a manutenção e expansão futura do código.
- **Enum para Status**: Utilização de um enum para o status das tarefas, garantindo maior controle sobre os valores permitidos e prevenindo erros de entrada.

## ▶️ Como Executar

1. Clone o repositório para sua máquina:
   ```bash
   git clone https://github.com/seu-usuario/sistema-gerenciamento-projetos.git
   ```
2. Compile e execute o programa principal:
   ```bash
   javac Main.java
   java Main
   ```

## 👨‍💻 Desenvolvedor

Este projeto foi desenvolvido por **Yann Leão** em setembro de 2024.
