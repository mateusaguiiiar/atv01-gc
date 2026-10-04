# Objetos Astronômicos | Atividade 01 - Gerência de Configuração

Projeto desenvolvido para a disciplina de **Gerência de Configuração**.

## Tema

O projeto consiste em um sistema para gerenciamento de **objetos astronômicos**, permitindo o cadastro, alteração, exclusão e consulta das informações relacionadas às entidades do sistema.

## Entidades

O sistema possui duas entidades:

* **Planetas**
* **Cometas**

Cada integrante da dupla é responsável pelo desenvolvimento de uma das entidades.

## Tecnologias utilizadas

* HTML5
* Bootstrap
* Docker
* Nginx
* Git
* GitHub

## Estrutura do projeto

```text
atv01-gc/
├── index.html
├── README.md
├── Dockerfile
├── planetas/
│   ├── inserir.html
│   ├── alterar.html
│   ├── excluir.html
│   └── procurar.html
├── cometas/
│   ├── inserir.html
│   ├── alterar.html
│   ├── excluir.html
│   └── procurar.html
├── assets/
│   ├── css/
│   │   └── bootstrap.min.css
│   └── js/
│       └── bootstrap.bundle.min.js
└── .github/
    └── workflows/
```

## Entidade Planetas

A entidade **Planetas** possui os seguintes atributos:

| Atributo         | Tipo    |
| ---------------- | ------- |
| Nome             | String  |
| Número de luas   | Integer |
| Massa (kg)       | Float   |
| Possui atmosfera | Boolean |

O sistema disponibiliza as operações de:

* Inserção de planetas
* Alteração de planetas
* Exclusão de planetas
* Consulta de planetas

## Entidade Cometas

A entidade **Cometas** será utilizada para o gerenciamento das informações relacionadas aos cometas, seguindo a mesma estrutura de operações CRUD do sistema.

## Bootstrap

O projeto utiliza **Bootstrap** para a construção da interface das páginas. Os componentes e estilos utilizados são baseados nas classes disponibilizadas pelo framework, sem utilização de CSS ou JavaScript personalizados.

## Docker

O projeto utiliza Docker com Nginx para disponibilizar as páginas da aplicação por meio de um servidor web.

Para criar a imagem:

```bash
docker build -t objetos-astronomicos .
```

Para executar o container:

```bash
docker run -d -p 8080:80 objetos-astronomicos
```

Após iniciar o container, a aplicação pode ser acessada em:

```text
http://localhost:8080
```

## Gerência de Configuração

O controle de versão do projeto é realizado utilizando **Git e GitHub**.

As principais branches utilizadas são:

* `main`: versão principal do projeto.
* `developer`: branch destinada ao desenvolvimento e integração das funcionalidades.
* Branches de funcionalidades e correções: utilizadas para desenvolver funcionalidades específicas antes de sua integração.

O projeto também utiliza **merge entre branches** para integração das funcionalidades e **GitHub Actions** para automação do projeto.

## Integrantes

* Mateus Aguiar — Planetas
* Carlos Eduardo — Cometas

```