# Sistema de Auditoria de EPIs com IA e PostgreSQL

## Sobre o Projeto

Este projeto automatiza a auditoria de Equipamentos de Proteção Individual (EPIs) por meio da utilização de Inteligência Artificial para extração de informações de documentos PDF e consultas SQL para validação de conformidade.

O processo compara os EPIs entregues aos colaboradores com os EPIs obrigatórios para cada função, identificando automaticamente possíveis não conformidades.

## Tecnologias Utilizadas

- ChatGPT / IA Generativa
- PostgreSQL
- SQL

## Fluxo da Solução

1. Recebimento dos formulários de entrega de EPI em PDF.
2. Extração das informações utilizando IA.
3. Carga das informações em tabelas PostgreSQL.
4. Relacionamento entre colaboradores, funções e EPIs obrigatórios.
5. Criação de views para identificação de EPIs não entregues.

## Estrutura de Dados

### Funcionários
Armazena os funcionários, suas respectivas funções, código da unidade, nome do setor de trabalho, epi correspondente a função e data de entrega do epi. 

### Funções
Contém o código da unidade, código do ghe(grupos homogêneos de exposição), nome do setor de trabalho e função do funcionário.

### EPIs Obrigatórios
Contém o código da unidade, código do ghe(grupos homogêneos de exposição) e epis.

### EPIs Entregues
Registra os equipamentos efetivamente recebidos pelos colaboradores.

### EPIs Faltantes
Registra os equipamentos faltantes dos colaboradores.

## Resultado

A solução permite identificar automaticamente quais colaboradores não receberam todos os EPIs obrigatórios para suas funções, reduzindo o trabalho manual de auditoria e aumentando a confiabilidade do processo.

## Autor

Felipe Salgueiro dos Prazeres