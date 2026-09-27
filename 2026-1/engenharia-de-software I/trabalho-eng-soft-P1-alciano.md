# ESTUDO DE CASO

## Levantamento e Análise de Requisitos

**Curso:** Análise e Desenvolvimento de Sistemas\
**Instituição:** Centro Estadual de Educação Tecnológica Paula Souza\
**Local:** Lins-SP\
**Ano:** 2026

### Integrantes validos apenas no 1° semestre

-   Anderson Clayton Pereira de Assis
-   Anderson Porto Abrantes
-   Eduardo Matias Ferreira
-   Poliana da Silva Benedito


**Professor:** Alciano Gustavo Genovez De Oliveira

------------------------------------------------------------------------

# Sistema Web para Gestão de Pesquisas por Questionários

## 1. Apresentação

O projeto tem como objetivo proporcionar aos estudantes uma experiência
prática de desenvolvimento de software, envolvendo análise de
requisitos, modelagem de dados, desenvolvimento de aplicações web,
usabilidade, segurança da informação e geração de relatórios analíticos.

O sistema a ser desenvolvido deverá permitir a criação, aplicação e
análise de pesquisas institucionais, garantindo anonimato dos
participantes e organização das respostas por categorias de
respondentes.

## 2. Objetivo do Projeto

Desenvolver um Sistema Web para Gestão de Pesquisas por Questionários,
permitindo:

-   Cadastro e gerenciamento de pesquisas
-   Definição de categorias de participantes
-   Criação de questionários específicos por categoria
-   Aplicação da pesquisa com acesso por senha anônima
-   Coleta e armazenamento das respostas
-   Monitoramento da participação
-   Geração de relatórios estatísticos

O sistema deverá permitir a realização de pesquisas institucionais de
forma organizada, segura e anônima.

## 3. Escopo do Sistema

O sistema deverá contemplar os seguintes módulos funcionais:

### 3.1 Módulo de Cadastro de Pesquisa

Responsável pela criação e configuração das pesquisas.

**Funcionalidades mínimas:**

-   Cadastro de pesquisas
-   Definição de:
    -   título da pesquisa
    -   descrição
    -   período de aplicação (data início e fim)
    -   status (ativa/inativa)

**Cadastro de categorias de participantes**

Exemplo de categorias:

-   Alunos
-   Professores
-   Colaboradores

Cada pesquisa poderá possuir uma ou mais categorias de participantes.

### 3.2 Módulo de Questionários

Responsável pela criação das perguntas da pesquisa.

**Funcionalidades:**

-   Cadastro de questões
-   Associação das questões a uma categoria de participante
-   Cadastro de alternativas de resposta
-   Tipos de questões sugeridos:
    -   Múltipla escolha (uma resposta)
    -   Múltipla escolha (várias respostas)
    -   Escala (ex: 1 a 5)
    -   Resposta aberta (texto)

Cada categoria poderá possuir seu próprio questionário.

### 3.3 Módulo de Geração de Senhas

O sistema deverá permitir a geração de senhas de acesso anônimas.

**Características:**

-   Senhas aleatórias
-   Associadas a uma categoria de participante
-   Não devem identificar o respondente
-   Cada senha deve permitir apenas uma resposta

**Funcionalidades:**

-   Gerar lote de senhas por categoria
-   Exportar senhas (PDF ou CSV)
-   Marcar senha como utilizada

### 3.4 Módulo de Aplicação da Pesquisa (Coleta de Dados)

Interface para os participantes responderem a pesquisa.

**Fluxo de uso:**

1.  Usuário acessa o sistema.
2.  Digita a senha recebida.
3.  Sistema identifica a categoria.
4.  Exibe o questionário correspondente.
5.  Usuário responde as perguntas.
6.  Sistema grava as respostas no banco de dados.
7.  Senha é marcada como utilizada.

**Requisitos:**

-   Interface simples e responsiva
-   Validação de respostas obrigatórias
-   Impedir múltiplas respostas com a mesma senha

### 3.5 Módulo de Gestão (Dashboard)

Interface administrativa para acompanhamento da pesquisa.

**Indicadores sugeridos:**

-   Total de senhas geradas
-   Total de respostas recebidas
-   Taxa de participação
-   Participação por categoria

### 3.6 Módulo de Relatórios

O sistema deverá permitir a geração de relatórios analíticos.

**Relatórios sugeridos:**

-   Resultado por pergunta
-   Resultado por categoria
-   Comparação entre categorias
-   Exportação de resultados (PDF, CSV)
-   Visualização em tela com gráficos

## 4. Requisitos Funcionais

O sistema deverá permitir:

-   Cadastrar pesquisas
-   Cadastrar categorias de participantes
-   Criar questionários por categoria
-   Cadastrar perguntas e alternativas
-   Gerar senhas anônimas
-   Aplicar questionários via senha
-   Registrar respostas no banco de dados
-   Impedir reutilização de senhas
-   Monitorar participação em tempo real
-   Gerar relatórios estatísticos

## 5. Requisitos Não Funcionais

O sistema deverá atender aos seguintes requisitos:

### Usabilidade

-   Interface web amigável
-   Layout responsivo

### Segurança

-   Senhas criptografadas no banco
-   Validação de acesso
-   Proteção contra múltiplas respostas

### Performance

-   Sistema capaz de suportar múltiplos acessos simultâneos

### Portabilidade

-   Funcionamento em navegadores modernos

## 6. Requisitos Tecnológicos

Utilizar tecnologias modernas de desenvolvimento web.

**Sugestão de stack:**

### Backend

-   PHP (Laravel)
-   Node.js
-   Java Spring Boot

### Frontend

-   HTML5
-   CSS3
-   Bootstrap
-   JavaScript
-   React (opcional)

### Banco de dados

-   MySQL
-   PostgreSQL

### Outras tecnologias sugeridas

-   APIs REST
-   Docker (opcional)
-   Git/GitHub para versionamento

# Requisitos Funcionais

Os requisitos funcionais descrevem o que o sistema deve fazer --- as
funcionalidades que deverão ser implementadas para atender às
necessidades dos usuários.

  -----------------------------------------------------------------------
  ID                                  Descrição
  ----------------------------------- -----------------------------------
  RF01                                Cadastrar pesquisas

  RF02                                Cadastrar categorias de
                                      participantes

  RF03                                Criar questionários por categoria

  RF04                                Cadastrar perguntas e alternativas
                                      de resposta

  RF05                                Gerar senhas anônimas por lote e
                                      por categoria

  RF06                                Exportar senhas geradas (PDF ou
                                      CSV)

  RF07                                Aplicar questionários via senha
                                      anônima

  RF08                                Registrar respostas no banco de
                                      dados

  RF09                                Impedir reutilização de senhas

  RF10                                Monitorar participação em tempo
                                      real (dashboard)

  RF11                                Gerar relatórios estatísticos por
                                      pergunta, categoria e comparativos

  RF12                                Exportar resultados em PDF e CSV
  -----------------------------------------------------------------------

# Requisitos Não Funcionais

Os requisitos não funcionais definem as qualidades e restrições do
sistema, como desempenho, segurança, usabilidade e portabilidade.

  -----------------------------------------------------------------------
  ID                      Categoria               Descrição
  ----------------------- ----------------------- -----------------------
  RNF01                   Usabilidade             Interface web amigável
                                                  e layout responsivo,
                                                  acessível em
                                                  dispositivos móveis e
                                                  desktops.

  RNF02                   Segurança               Senhas criptografadas
                                                  no banco, validação de
                                                  acesso e proteção
                                                  contra múltiplas
                                                  respostas.

  RNF03                   Performance             O sistema deve suportar
                                                  múltiplos acessos
                                                  simultâneos sem
                                                  degradação de
                                                  desempenho.

  RNF04                   Portabilidade           Funcionamento em
                                                  navegadores modernos
                                                  (Chrome, Firefox, Edge,
                                                  Safari).

  RNF05                   Anonimato               Nenhuma resposta deve
                                                  poder ser rastreada ao
                                                  respondente
                                                  individualmente.
  -----------------------------------------------------------------------

# Atores

Os atores representam os perfis de usuários que interagem com o sistema.

  -----------------------------------------------------------------------
  Ator                                Descrição
  ----------------------------------- -----------------------------------
  Administrador                       Responsável por criar e gerenciar
                                      pesquisas, categorias,
                                      questionários, senhas e relatórios.
                                      Tem acesso total ao sistema.

  Participante                        Usuário que recebe uma senha
                                      anônima e responde ao questionário
                                      correspondente à sua categoria. Não
                                      possui conta no sistema.

  Secretaria                          Responsável por aprovar pesquisas
                                      antes de sua aplicação e analisar
                                      relatórios para subsidiar decisões
                                      institucionais.

  Analista de Dados                   Responsável por analisar os
                                      resultados das pesquisas, gerar
                                      insights e exportar dados para uso
                                      externo.

  Suporte Técnico                     Responsável pela manutenção do
                                      sistema, resolução de erros e
                                      garantia de continuidade
                                      operacional.

  Auditor                             Responsável por auditar os dados
                                      coletados, verificar a segurança do
                                      sistema e garantir conformidade com
                                      normas.
  -----------------------------------------------------------------------

# User Stories

As User Stories descrevem as funcionalidades do sistema do ponto de
vista do usuário, no formato: **Ator --- Ação --- Resultado esperado**.

  -----------------------------------------------------------------------
  Ator                    Ação do Usuário         Resultado Esperado
  ----------------------- ----------------------- -----------------------
  Administrador           Cadastrar uma nova      O sistema registra a
                          pesquisa                pesquisa com título,
                                                  descrição, período e
                                                  status.

  Administrador           Cadastrar categorias de O sistema associa as
                          participantes           categorias (ex: Alunos,
                                                  Professores) à
                                                  pesquisa.

  Administrador           Criar questionário por  O sistema vincula as
                          categoria               perguntas à categoria
                                                  selecionada.

  Administrador           Gerar lote de senhas    O sistema gera senhas
                          anônimas por categoria  aleatórias associadas à
                                                  categoria, sem
                                                  identificar o
                                                  respondente.

  Administrador           Gerar relatório de      O sistema exibe
                          resultados              gráficos e permite
                                                  exportação em PDF ou
                                                  CSV.

  Participante            Acessar a pesquisa com  O sistema identifica a
                          a senha recebida        categoria do
                                                  participante e exibe o
                                                  questionário
                                                  correspondente.

  Participante            Responder o             O sistema valida as
                          questionário            respostas obrigatórias
                                                  e grava as respostas no
                                                  banco de dados.

  Secretaria              Aprovar pesquisas antes O sistema libera a
                          da aplicação            pesquisa para aplicação
                                                  após aprovação.

  Secretaria              Analisar relatórios     O sistema fornece dados
                          institucionais          consolidados para apoio
                                                  à tomada de decisão.

  Analista de Dados       Analisar resultados     O sistema exibe
                          detalhados              gráficos detalhados por
                                                  categoria e pergunta.

  Analista de Dados       Gerar insights e        O sistema permite
                          exportar dados          exportação dos dados
                                                  para análises externas.

  Suporte Técnico         Manter o sistema em     O sistema continua
                          operação                funcionando
                                                  corretamente após
                                                  manutenção.

  Suporte Técnico         Resolver erros e falhas As falhas são
                                                  corrigidas e o sistema
                                                  retorna à normalidade.

  Auditor                 Auditar os dados        O sistema garante
                          coletados               integridade e
                                                  rastreabilidade dos
                                                  dados.

  Auditor                 Verificar segurança e   A conformidade com
                          conformidade            normas de segurança é
                                                  validada.
  -----------------------------------------------------------------------
