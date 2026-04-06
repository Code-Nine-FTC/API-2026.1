<div align="center">
  <h1>VISIONA - Sistema para Análises Ambientais, Sociais e de Governança (ASG)</h1>
  <h3>Projeto de API - Fatec Prof° Jessen Vidal - 1º Semestre de 2026</h3>
</div>

<p align="center">
  Projeto acadêmico desenvolvido por alunos do curso de Desenvolvimento de Software Multiplataforma (DSM),
  com o objetivo de analisar dados ambientais, sociais e de governança (ASG) de propriedades rurais do
  estado de São Paulo, utilizando dados geoespaciais e inteligência analítica.
</p>

<div align="center">

![Badge](https://img.shields.io/badge/status-Em%20Desenvolvimento-yellow)
![Badge](https://img.shields.io/badge/metodologia-Scrum-blue)

</div>

---

## 🗂️ Índice
- [Metodologia Utilizada](#-metodologia-utilizada)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Descrição do Projeto](#-descrição-do-projeto)
- [Product Backlog](#-product-backlog)
- [Histórico de Sprints](#-histórico-de-sprints)
- [Definition of Ready (DoR)](#-definition-of-ready-dor)
- [Definition of Done (DoD)](#-definition-of-done-dod)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Links da API](#-links-da-api)
- [Integrantes do Grupo](#-integrantes-do-grupo)

---

## 📋 Metodologia Utilizada

O projeto utiliza o framework ágil **Scrum**, permitindo organização iterativa e incremental
do desenvolvimento. As entregas são divididas em Sprints, com cerimônias como Planning,
Daily, Review e Retrospective, garantindo evolução contínua e alinhamento com os objetivos do projeto.

---

## 🖥️ Tecnologias Utilizadas

### ⚙️ Backend / Serviços
<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Alembic-000000?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/GeoServer-2C7FB8?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge"/>
</div>

---

### 🗄️ Banco de Dados
<div align="center">
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/pgvector-000000?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/PostGIS-336791?style=for-the-badge"/>
</div>

---

### 🎨 Frontend
<div align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
</div>

---

## 📖 Descrição do Projeto

A crescente preocupação com sustentabilidade tem impulsionado a necessidade de ferramentas que
permitam analisar aspectos **Ambientais, Sociais e de Governança (ASG)**.

O VISIONA propõe uma solução que:

- Integra dados geoespaciais de diversas fontes (SICAR, INPE, ICMBio, etc.)
- Permite análises automatizadas de propriedades rurais
- Identifica riscos ambientais (desmatamento, queimadas, sobreposição de áreas)
- Responde perguntas do usuário por meio de consultas inteligentes
- Apresenta dados de forma visual, interativa e intuitiva

---

## 📌 Requisitos do Sistema

### ✅ Requisitos Funcionais (RF)

| ID   | Descrição                                                                                                  |
| ---- | ---------------------------------------------------------------------------------------------------------- |
| RF01 | Permitir a ingestão e armazenamento de dados geoespaciais de diferentes fontes (INPE, ICMBio, FUNAI, etc.) |
| RF02 | Disponibilizar APIs para consulta de dados geográficos por município e camadas                             |
| RF03 | Permitir a visualização de dados em mapas interativos com múltiplas camadas                                |
| RF04 | Realizar análises espaciais (interseção, proximidade e sobreposição)                                       |
| RF05 | Interpretar perguntas em linguagem natural e convertê-las em consultas SQL                                 |
| RF06 | Registrar consultas, fontes de dados e histórico de interações do usuário                                  |
| RF07 | Gerar relatórios analíticos em PDF com base nos dados filtrados                                            |
| RF08 | Calcular score ambiental (ASG) para imóveis rurais                                                         |
| RF09 | Classificar o risco ambiental com base nos dados analisados                                                |
| RF10 | Disponibilizar serviços geoespaciais (WMS/WFS) para integração externa                                     |
| RF11 | Permitir consultas geográficas por bounding box (bbox)                                                     |

### ⚙️ Requisitos Não Funcionais (RNF)

| ID    | Descrição                                                                                          |
| ----- | -------------------------------------------------------------------------------------------------- |
| RNF01 | O sistema deve responder às requisições da API em até 2 segundos, em condições normais             |
| RNF02 | O sistema deve suportar grande volume de dados geoespaciais com uso de índices espaciais (PostGIS) |
| RNF03 | As APIs devem seguir o padrão REST                                                                 |
| RNF04 | O sistema deve garantir consistência e integridade dos dados geográficos (padronização de CRS)     |
| RNF05 | O sistema deve possuir escalabilidade para crescimento do volume de dados                          |
| RNF06 | O sistema deve garantir rastreabilidade das consultas realizadas                                   |
| RNF07 | O sistema deve ser compatível com ferramentas geoespaciais como QGIS                               |
| RNF08 | O sistema deve garantir segurança no acesso às APIs                   |
| RNF09 | O sistema deve possuir alta disponibilidade durante o uso                                          |
| RNF10 | O sistema deve ser modular, facilitando manutenção e evolução                                      |

---

## 🗃️ Product Backlog

| *Rank* | *Prioridade* | *User Story* | *Estimativa* | *Sprint* |
|--------|--------------|-------------|--------------|----------|
| RF01 | Alta | Como sistema, quero configurar um banco de dados geoespacial utilizando PostGIS para armazenamento de dados geográficos | 5 | 1 |
| RF01 | Alta | Como sistema, quero padronizar sistemas de coordenadas (CRS) e geometrias para consistência dos dados | 3 | 1 |
| RF01 | Alta | Como sistema, quero indexar espacialmente os dados para otimizar consultas geográficas | 5 | 1 |
| RF02 | Alta | Como sistema, quero disponibilizar uma API para consulta por município | 5 | 1 |
| RF02 | Alta | Como sistema, quero disponibilizar uma API para retorno de features geográficas | 5 | 1 |
| RF02 | Média | Como sistema, quero tratar dados para exibição em gráficos analíticos | 3 | 1 |
| RF02 | Média | Como usuário, quero visualizar um dashboard interativo baseado em filtros selecionados | 5 | 1 |
| RF05 | Alta | Como sistema, quero registrar a consulta SQL executada para rastreabilidade | 3 | 1 |
| RF04 | Alta | Como sistema, quero extrair entidades geográficas (como município) das perguntas | 5 | 1 |
| RF04 | Alta | Como sistema, quero converter perguntas em consultas SQL automaticamente | 5 | 1 |
| RF05 | Alta | Como sistema, quero exibir as fontes utilizadas nas respostas ao usuário | 3 | 1 |
| RF05 | Alta | Como sistema, quero manter log das perguntas realizadas pelos usuários | 3 | 1 |
| RF04 | Alta | Como sistema, quero interpretar perguntas simples feitas pelo usuário | 3 | 1 |
| RF02 | Alta | Como usuário, quero realizar zoom por município no mapa | 3 | 1 |
| RF05 | Alta | Como sistema, quero registrar a fonte de dados utilizada nas respostas | 3 | 1 |
| RF05 | Alta | Como sistema, quero registrar a consulta SQL executada para rastreabilidade | 3 | 1 |
| RF05 | Alta | Como sistema, quero exibir as fontes utilizadas nas respostas ao usuário | 3 | 1 |
| RF05 | Alta | Como sistema, quero permitir consultas por bounding box (bbox) para visualização em mapas | 3 | 1 |
| RF02 | Alta | Como usuário, quero alternar entre diferentes layers no mapa | 3 | 2 |
| RF03 | Alta | Como sistema, quero detectar interseção entre imóveis rurais e unidades de conservação | 5 | 2 |
| RF03 | Alta | Como sistema, quero detectar proximidade entre imóveis e áreas de queimadas | 5 | 2 |
| RF03 | Alta | Como sistema, quero calcular áreas sobrepostas entre entidades geográficas | 5 | 2 |
| RF04 | Alta | Como sistema, quero mapear a intenção do usuário em consultas semânticas | 5 | 2 |
| RF02 | Média | Como usuário, quero gerar relatórios em PDF baseados nos filtros aplicados | 5 | 2 |
| RF06 | Média | Como sistema, quero calcular um score ambiental para análise ASG | 5 | 3 |
| RF06 | Média | Como sistema, quero classificar o risco ambiental de imóveis | 5 | 3 |
| RF06 | Média | Como sistema, quero gerar um resumo ambiental por imóvel | 3 | 3 |
| RF06 | Média | Como sistema, quero conectar o banco PostGIS ao QGIS para visualização | 3 | 3 |
| RF06 | Média | Como sistema, quero publicar serviços WMS/WFS para consumo geoespacial | 5 | 3 |
| RF06 | Média | Como sistema, quero disponibilizar um projeto configurado no QGIS | 3 | 3 |
| RF06 | Média | Como sistema, quero otimizar consultas com índices espaciais avançados | 5 | 3 |
| RF06 | Média | Como sistema, quero implementar cache de consultas para melhorar performance | 5 | 3 |
| RF06 | Média | Como sistema, quero reduzir o tempo de resposta das APIs geoespaciais | 5 | 3 |

---

## Histórico de Sprints

## 📅 Cronograma de Evolução do Projeto

| Sprint | Período | 📄 Documentação | 🎥 Apresentação |
|--------|--------|----------------|----------------|
| Sprint 01 | 16/03 - 05/04 | [Acessar](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/Sprint-01.md) | - |
| Sprint 02 | 13/04 - 03/05 | [Acessar](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/Sprint-02.md) | - |
| Sprint 03 | 11/05 - 31/05 | [Acessar](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/Sprint-03.md) | - |

---

## ✅ Definition of Ready (DoR) e Definition of Done (DoD)

Critérios para uma tarefa estar pronta para desenvolvimento:  
[📄 Acessar DoR e DoR](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/dod-dor.md)

---

## 📂 Estrutura do Projeto

> (Diagrama aqui futuramente)

---

## 🔗 Links da API

> (Adicionar endpoints, Swagger ou documentação futuramente)

---

## 🙎 Integrantes do Grupo

<div align="center">

|          |   Nome   |  Função  |  GitHub  | LinKedin |
| :------: | :------: | :------: | :------: | :------: |
| <img src="https://avatars.githubusercontent.com/u/142221456?v=4" alt="foto de perfil" height="64px" width="64px"> | Pedro Oliveira | Product Owner | <a href="https://github.com/OliveiraPedro09"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/pedrooliv9"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/79583088?v=4"  alt="foto de perfil" height="64px" width="64px"> | Yuri Braga | Scrum Master | <a href="https://github.com/yuribragga"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/yuri-braga/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/104574671?v=4" alt="foto de perfil" height="64px" width="64px"> | Davi Maciel | Developer | <a href="https://github.com/DfMaciel"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/dfmaciel"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/61799878?v=4" alt="foto de perfil" height="64px" width="64px"> | Elisa Rachel | Developer | <a href="https://github.com/elisarachel"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/elisa-beninca-704566292/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221695?v=4" alt="foto de perfil" height="64px" width="64px"> | Joyce Silva | Developer | <a href="https://github.com/joycesilvaaa"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/joyce-silva-79a4b9287/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142128061?v=4" alt="foto de perfil" height="64px" width="64px"> | Eber Júnior | Developer | <a href="https://github.com/eberssj"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/eber-junior-b2a4a3211/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221388?v=4" alt="foto de perfil" height="64px" width="64px"> | Júlia Rosado | Developer | <a href="https://github.com/juliamariahr"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/júlia-rosado/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221848?v=4" alt="foto de perfil" height="64px" width="64px"> | Jonas Miguel | Developer | <a href="https://github.com/Jonasoliver"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/jonas-miguel-ol"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221532?v=4" alt="foto de perfil" height="64px" width="64px"> | Renato Cruz | Developer | <a href="https://github.com/Renato-Cruz-Jr"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/renato-fernandes-da-cruz-junior-798582204/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |

</div>

---

<div align="center">
  <b>Desenvolvido pela equipe Code Nine</b>
</div>
