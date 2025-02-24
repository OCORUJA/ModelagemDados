# Curso NTT Data - Engenharia de Dados com Python

Bem-vindo ao repositório do projeto desenvolvido como parte do curso **NTT Data - Engenharia de Dados com Python**, ministrado pela DIO. Este projeto tem como objetivo principal a criação de um **Star Schema** no módulo de Modelagem de Dados, integrado ao Power BI, para facilitar a análise e visualização de dados.

## Descrição

O projeto consiste na construção de um modelo de dados baseado no conceito de **Star Schema**, uma abordagem amplamente utilizada em engenharia de dados para organizar informações de forma eficiente e acessível. O foco é proporcionar praticidade e clareza na manipulação e visualização dos dados dentro do contexto do curso.

## Ferramentas Utilizadas

- **MySQL Workbench**: Utilizado para a construção e modelagem do banco de dados.
  - Disponível para download em: [MySQL Workbench](https://www.mysql.com/products/workbench/)
- **Power BI**: Ferramenta para visualização e análise dos dados modelados.
- **Python**: Linguagem usada no curso para manipulação e integração de dados.

## Estrutura do Banco de Dados (Star Schema)

Abaixo estão as tabelas criadas para o modelo de dados, com seus respectivos campos e tipos:

| **Tabela**                | **Campos**                                                                 | **Descrição**                              |
|---------------------------|---------------------------------------------------------------------------|--------------------------------------------|
| `Professor`              | `idProfessor` (INT, PK), `nomeProfessor` (VARCHAR(45)), `idDepartamento` (INT) | Tabela central com dados dos professores.  |
| `FormacaoSuperior`       | `idFormacaoSuperior` (INT, PK), `tipoFormacao` (VARCHAR(45)), `nomeCurso` (VARCHAR(45)), `idProfessor` (INT) | Registra a formação acadêmica dos professores. |
| `Departamento`           | `idDepartamento` (INT, PK), `nomeDepartamento` (VARCHAR(45)), `campusDepartamento` (VARCHAR(45)), `idProfessorCoordenador` (INT) | Informações sobre os departamentos.        |
| `Disciplina`             | `idDisciplina` (INT, PK), `nomeDisciplina` (VARCHAR(45)), `idDepartamento` (INT), `idProfessor` (INT), `idCurso` (INT) | Detalhes das disciplinas oferecidas.       |
| `Curso`                  | `idCurso` (INT, PK), `nomeCurso` (VARCHAR(45)), `dataInicio` (DATE), `dataEncerramento` (DATE) | Registro dos cursos disponíveis.           |
| `PreRequisitoDisciplina` | `idPreRequisitoDisciplina` (INT, PK), `preRequisitoDisciplina` (VARCHAR(45)), `idDisciplina` (INT) | Define os pré-requisitos das disciplinas.  |

### Observações
- **PK**: Chave primária.
- A tabela `Professor` foi posicionada como fato central no diagrama do Star Schema, seguindo as boas práticas de visualização gráfica.
- As tabelas de dimensão (`FormacaoSuperior`, `Departamento`, `Disciplina`, `Curso`, `PreRequisitoDisciplina`) fornecem contexto aos dados da tabela fato.

## Arquivos Disponibilizados

- **Star_Schema_Dio.pdf**: Arquivo PDF com a visualização gráfica do modelo de banco de dados.
- **DadosCurso.mwb**: Arquivo nativo do MySQL Workbench contendo o diagrama editável do Star Schema.

Os arquivos estão disponíveis para download no seguinte endereço: [https://github.com/OCORUJA/ModelagemDados](https://github.com/OCORUJA/ModelagemDados).

## Pré-requisitos

- MySQL Workbench instalado.
- Python 3.8 ou superior (para eventuais scripts de manipulação de dados).
- Power BI Desktop (para visualização dos dados).

## Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/OCORUJA/ModelagemDados.git
2. Abra o arquivo DadosCurso.mwb no MySQL Workbench para visualizar ou editar o modelo.
3. Exporte o schema para um banco de dados MySQL ativo, se desejar testar localmente.

## Como Usar
- Abra o arquivo PDF ou MWB para explorar o modelo.
- Utilize o Power BI para conectar o banco de dados e criar visualizações baseadas no Star Schema.

## Contribuição

Contribuições são bem-vindas! Para colaborar:

1.Faça um fork deste repositório.

2.Crie uma branch para sua sugestão (git checkout -b melhoria/nova-funcionalidade).

3.Commit suas alterações (git commit -m "Adiciona melhoria no modelo").

4.Envie um pull request com uma descrição clara das mudanças propostas.

Sinta-se à vontade para contribuir com melhorias e sugestões para o projeto!

## Licença

Este projeto é de uso educacional e segue as diretrizes do curso NTT Data pela DIO.


