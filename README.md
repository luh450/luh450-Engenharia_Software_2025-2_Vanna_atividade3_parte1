# Etapa 1 – Diagnóstico e Auditoria  


## O Cenário Atual do Ciclo de Vida do Software

**Repositório analisado:** https://github.com/vanna-ai/vanna  


## Integrantes
Josias Ribeiro de Freitas Júnior - 202200025644

Natalia Silva Santos - 202400018206

Luzia dos Santos Souza Neta - 201700017537

Anthony Amoz Santos Aragao - 202100011207


---

## 1. Objetivo da Etapa

Realizar uma investigação no repositório original com o objetivo de compreender como o ciclo de vida do software é gerenciado atualmente, com foco em práticas de **Integração Contínua (CI)** e **Entrega Contínua (CD)**, identificando automações existentes, evidências técnicas, fluxo de trabalho atual, riscos e gargalos.


## 2. Investigação de Ferramentas de CI/CD

### 2.1 Ferramentas Identificadas

O projeto utiliza GitHub Actions como ferramenta de CI/CD.

A evidência pode ser confirmada pela aba **Actions** do repositório, onde estão listados diversos workflows ativos, incluindo:

- *Basic Integration Tests*
- *Copilot code review*
- *Upload Python Package*

Esses workflows indicam a presença de automação para:
- Execução de testes de integração
- Apoio à revisão de código
- Empacotamento e publicação de pacotes Python


## 3. Evidências Técnicas

### 3.1 Arquivos de Configuração

O repositório contém a pasta:
`.github/workflows/`


Esse diretório é o padrão do GitHub Actions para armazenar arquivos de configuração no formato `.yml`, que definem:
- Gatilhos de execução (push, pull request, releases)
- Etapas de build, teste e publicação
- Dependências e ambientes de execução

Esses arquivos constituem a principal evidência da adoção de CI/CD no projeto.



### 3.2 Histórico de Pull Requests

O projeto apresenta:
- Grande volume de Pull Requests abertas e fechadas
- Uso recorrente de PRs como mecanismo principal de integração de código

A análise do histórico de PRs indica:
- Uso consistente de revisão de código
- Execução automática de checks de CI associados às PRs
- Integração de mudanças baseada em validações automatizadas



## 4. Mapeamento do Fluxo Atual

### 4.1 Fluxo de Desenvolvimento Identificado

1. O desenvolvedor cria uma branch ou fork
2. Alterações são submetidas via Pull Request
3. GitHub Actions é acionado automaticamente
4. Workflows executam testes e verificações
5. Após aprovação e sucesso dos checks, o código é integrado à branch principal


### 4.2 Integração Contínua (CI)

- Presente e funcional
- Automatiza testes e validações
- Reduz riscos de integração de código defeituoso



### 4.3 Entrega Contínua (CD)

- Não há evidência clara de pipelines completos de deploy automatizado
- A automação parece focada principalmente em:
  - Testes
  - Revisão de código
  - Publicação de pacotes

Isso sugere que o processo de entrega final (deploy em ambientes produtivos ou similares) pode:
- Não estar automatizado
- Estar parcialmente automatizado
- Ou ocorrer fora do escopo público do repositório



## 5. Riscos e Gargalos Identificados

### 5.1 Riscos

- Dependência de processos manuais para deploy ou publicação final
- Possível ausência de validações automáticas adicionais (ex: segurança, qualidade de código)
- Risco de inconsistência entre ambientes caso o deploy não seja automatizado



### 5.2 Gargalos Manuais

- Necessidade de intervenção humana para etapas finais do ciclo
- Maior tempo de entrega de novas versões
- Potencial erro humano em processos repetitivos


## 6. Conclusão 

O projeto **vanna-ai/vanna** apresenta um nível maduro de **Integração Contínua**, com uso efetivo de GitHub Actions, testes automatizados e integração via Pull Requests.

Entretanto, a **Entrega Contínua (CD)** não é claramente identificável como totalmente automatizada, representando uma oportunidade de melhoria para reduzir riscos, gargalos e aumentar a eficiência do ciclo de vida do software.

Esta análise estabelece uma base sólida para as próximas etapas de evolução e otimização do pipeline CI/CD do projeto.


