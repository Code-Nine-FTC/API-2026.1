# API-2026.1 - VISIONA - Sistema para análises Ambientais, Sociais e de Governança (ASG) voltado a propriedades do Estado de São Paulo

## Descrição

A sociedade moderna tem aumentado cada vez mais sua preocupação com os aspectos ambientais,
sociais e de governança em especial aqueles que estão relacionados às propriedades rurais (fontes
de grande parte dos insumos alimentares do país). Esse fato é decorrente da necessidade de
construção de um futuro sustentável para as atuais e futuras gerações. Nesse sentido, a criação de
ferramentas que suportem a análise automatizada desses aspectos (ASG), baseados em dados
amplamente disponíveis, é não só justificável como também desejável por parte do governo e entes
privados que atuam nessa linha.

O desafio proposto para os alunos é o desenvolvimento de uma ferramenta que permita a execução
de análises integradas das condições ASG relacionadas às propriedades rurais do Estado de São
Paulo. Essa ferramenta deve ser capaz de efetuar algumas análises automatizadas utilizando fontes
tais como o SICAR (Sistema Nacional de Cadastro Ambiental Rural), que disponibiliza, por exemplo,
onde estão localizadas as propriedades, sua área, etc, e outros dados que indiquem possíveis
passivos ambientais, como, por exemplo, a existência de queimadas ou desmatamentos não
autorizados em uma propriedade.

Espera-se que essa ferramenta possua a capacidade de execução de análises e/ou recuperação de
dados a partir de interações textuais com o usuário (e.g., faz-se uma pergunta e retorna-se o dado
ou a análise desejada). Quanto mais intuitiva, explicativa e visual for a resposta ou análise fornecida
por essa ferramenta, maior será o seu valor e utilidade ao usuário final.

## DoD e DoR
[Acessar](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/dod-dor.md)

## Backlog do Produto
| *Rank* | *Prioridade* | *User Story*                                                                                                          | *Estimativa* | *Sprint* |
| -------- | -------------- | ----------------------------------------------------------------------------------------------------------------------- | -------------- | ---------- |
| 1        | Alta           | Como sistema, quero configurar um banco de dados geoespacial utilizando PostGIS para armazenamento de dados geográficos | 5              | 1          |
| 2        | Alta           | Como sistema, quero ingerir dados geográficos básicos dos municípios do estado de São Paulo                             | 5              | 1          |
| 3        | Alta           | Como sistema, quero padronizar sistemas de coordenadas (CRS) e geometrias para consistência dos dados                   | 3              | 1          |
| 4        | Alta           | Como sistema, quero indexar espacialmente os dados para otimizar consultas geográficas                                  | 5              | 1          |
| 5        | Alta           | Como sistema, quero importar dados de Unidades de Conservação do ICMBio                                                 | 3              | 1          |
| 6        | Alta           | Como sistema, quero importar dados de Terras Indígenas da FUNAI                                                         | 3              | 1          |
| 7        | Alta           | Como sistema, quero importar dados de queimadas do INPE                                                                 | 3              | 1          |
| 8        | Alta           | Como sistema, quero importar dados de assentamentos rurais do INCRA                                                     | 3              | 1          |
| 9        | Alta           | Como sistema, quero importar dados de territórios quilombolas da Fundação Palmares                                      | 3              | 1          |
| 10       | Alta           | Como sistema, quero integrar dados estaduais provenientes do DataGeo SP                                                 | 3              | 1          |
| 11       | Alta           | Como sistema, quero disponibilizar uma API para consulta por município                                                  | 5              | 1          |
| 12       | Alta           | Como sistema, quero disponibilizar uma API para retorno de features geográficas                                         | 5              | 1          |
| 13       | Alta           | Como sistema, quero permitir filtros por tipo de camada na API                                                          | 3              | 1          |
| 14       | Alta           | Como sistema, quero permitir consultas por bounding box (bbox) para visualização em mapas                               | 3              | 1          |
| 15       | Média          | Como sistema, quero tratar dados para exibição em gráficos analíticos                                                   | 3              | 1          |
| 16       | Média          | Como usuário, quero visualizar um dashboard interativo baseado em filtros selecionados                                  | 5              | 1          |
| 17       | Média          | Como usuário, quero gerar relatórios em PDF baseados nos filtros aplicados                                              | 5              | 1          |
| 18       | Alta           | Como usuário, quero visualizar um mapa com múltiplas camadas geográficas                                                | 5              | 2          |
| 19       | Alta           | Como usuário, quero alternar entre diferentes layers no mapa                                                            | 3              | 2          |
| 20       | Alta           | Como usuário, quero realizar zoom por município no mapa                                                                 | 3              | 2          |
| 21       | Alta           | Como sistema, quero detectar interseção entre imóveis rurais e unidades de conservação                                  | 5              | 2          |
| 22       | Alta           | Como sistema, quero detectar proximidade entre imóveis e áreas de queimadas                                             | 5              | 2          |
| 23       | Alta           | Como sistema, quero calcular áreas sobrepostas entre entidades geográficas                                              | 5              | 2          |
| 24       | Alta           | Como sistema, quero interpretar perguntas simples feitas pelo usuário                                                   | 3              | 2          |
| 25       | Alta           | Como sistema, quero mapear a intenção do usuário em consultas semânticas                                                | 5              | 2          |
| 26       | Alta           | Como sistema, quero extrair entidades geográficas (como município) das perguntas                                        | 5              | 2          |
| 27       | Alta           | Como sistema, quero converter perguntas em consultas SQL automaticamente                                                | 5              | 2          |
| 28       | Alta           | Como sistema, quero registrar a fonte de dados utilizada nas respostas                                                  | 3              | 2          |
| 29       | Alta           | Como sistema, quero registrar a consulta SQL executada para rastreabilidade                                             | 3              | 2          |
| 30       | Alta           | Como sistema, quero exibir as fontes utilizadas nas respostas ao usuário                                                | 3              | 2          |
| 31       | Alta           | Como sistema, quero manter log das perguntas realizadas pelos usuários                                                  | 3              | 2          |
| 32       | Média          | Como sistema, quero calcular um score ambiental para análise ASG                                                        | 5              | 3          |
| 33       | Média          | Como sistema, quero classificar o risco ambiental de imóveis                                                            | 5              | 3          |
| 34       | Média          | Como sistema, quero gerar um resumo ambiental por imóvel                                                                | 3              | 3          |
| 35       | Média          | Como sistema, quero conectar o banco PostGIS ao QGIS para visualização                                                  | 3              | 3          |
| 36       | Média          | Como sistema, quero publicar serviços WMS/WFS para consumo geoespacial                                                  | 5              | 3          |
| 37       | Média          | Como sistema, quero disponibilizar um projeto configurado no QGIS                                                       | 3              | 3          |
| 38       | Média          | Como sistema, quero otimizar consultas com índices espaciais avançados                                                  | 5              | 3          |
| 39       | Média          | Como sistema, quero implementar cache de consultas para melhorar performance                                            | 5              | 3          |
| 40       | Média          | Como sistema, quero reduzir o tempo de resposta das APIs geoespaciais                                                   | 5              | 3          |

## 📅 Cronograma de Evolução do Projeto

| Sprint | Período | 📄 Documentação | 🎥 Apresentação |
|--------|--------|----------------|----------------|
| Sprint 01 | 16/03 - 05/04 | [Acessar](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/Sprint-01.md) | - |
| Sprint 02 | 13/04 - 03/05 | [Acessar](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/Sprint-02.md) | - |
| Sprint 03 | 11/05 - 31/05 | [Acessar](https://github.com/Code-Nine-FTC/API-2026.1/blob/main/docs/Sprint-03.md) | - |

## (Tabela descritiva das Sprints com as colunas: Periodo Sprint, link p/ doc, link p/ youtube)

## 🧰 Tecnologias Utilizadas

### ⚙️ Backend / Serviços
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Alembic-000000?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/GeoServer-2C7FB8?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/WMS/WFS-4CAF50?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge"/>
</p>

---

### 🗄️ Banco de Dados
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/pgvector-000000?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/PostGIS-336791?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white"/>
</p>

---

### 🎨 Frontend
<p>
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
</p>


## Estrutura do Projeto

## Links para Docs API

## Equipe

<div align="center">

|          |   Nome   |  Função  |  GitHub  | LinKedin |
| :------: | :------: | :------: | :------: | :------: |
| <img src="https://avatars.githubusercontent.com/u/142221456?v=4" alt="foto de perfil" height="64px" width="64px"> | Pedro Oliveira | Product Owner | <a href="https://github.com/OliveiraPedro09"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/pedrooliv9"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/79583088?v=4"  alt="foto de perfil" height="64px" width="64px"> | Yuri Braga | Scrum Master | <a href="https://github.com/yuribragga"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/yuri-braga/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/104574671?v=4" alt="foto de perfil" height="64px" width="64px"> | Davi Maciel | Developer | <a href="https://github.com/DfMaciel"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/dfmaciel"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142128061?v=4" alt="foto de perfil" height="64px" width="64px"> | Eber Júnior | Developer | <a href="https://github.com/eberssj"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/eber-junior-b2a4a3211/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/61799878?v=4" alt="foto de perfil" height="64px" width="64px"> | Elisa Rachel | Developer | <a href="https://github.com/elisarachel"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/elisa-beninca-704566292/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221848?v=4" alt="foto de perfil" height="64px" width="64px"> | Jonas Miguel | Developer | <a href="https://github.com/Jonasoliver"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/jonas-miguel-ol"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221695?v=4" alt="foto de perfil" height="64px" width="64px"> | Joyce Silva | Developer | <a href="https://github.com/joycesilvaaa"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/joyce-silva-79a4b9287/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221388?v=4" alt="foto de perfil" height="64px" width="64px"> | Júlia Rosado | Developer | <a href="https://github.com/juliamariahr"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/júlia-rosado/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |
| <img src="https://avatars.githubusercontent.com/u/142221532?v=4" alt="foto de perfil" height="64px" width="64px"> | Renato Cruz | Developer | <a href="https://github.com/Renato-Cruz-Jr"><img src="https://img.shields.io/badge/GitHub-13196a?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/renato-fernandes-da-cruz-junior-798582204/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a> |


</div>
