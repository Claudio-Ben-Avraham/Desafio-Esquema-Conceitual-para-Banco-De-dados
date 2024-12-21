# Esquema Conceitual para Oficina Mecânica

## Contexto do Projeto

Este projeto apresenta o esquema conceitual de um sistema de controle e gerenciamento de execução de ordens de serviço (OS) em uma oficina mecânica. O sistema foi modelado com base na narrativa fornecida e visa atender às necessidades descritas para gerenciar clientes, veículos, ordens de serviço, equipes de mecânicos, serviços, e peças utilizadas.

### Recursos do Sistema
- Cadastro de clientes e veículos.
- Emissão e gerenciamento de ordens de serviço.
- Registro de serviços e peças associados a cada OS.
- Organização de mecânicos em equipes para avaliação e execução dos serviços.
- Relacionamentos estruturados para garantir integridade e clareza nos dados.

### Descrição do Sistema

1. **Clientes**:
   - Levam veículos à oficina para conserto ou revisão periódica.
   - Dados armazenados: CPF, nome, endereço e telefone.

2. **Veículos**:
   - Pertencem aos clientes e são identificados pelo modelo, marca, ano e placa.

3. **Ordens de Serviço (OS)**:
   - São emitidas para cada solicitação de conserto ou revisão.
   - Contêm número, data de emissão, valor total, status e data de conclusão.
   - Relacionam-se a um ou mais serviços e peças utilizados.

4. **Serviços**:
   - São identificados por código e nome e têm um valor de mão de obra associado com base em uma tabela de referência.

5. **Peças**:
   - Cada peça utilizada em uma OS é registrada com descrição, código e valor unitário.

6. **Mecânicos**:
   - Trabalham em equipes responsáveis por avaliar e executar os serviços da OS.
   - Dados armazenados: código, nome, endereço e especialidade.

7. **Equipes**:
   - São compostas por um ou mais mecânicos e são designadas para cada OS.

### Entidades e Relacionamentos

- **Cliente (1:N) Veículo**: Um cliente pode ter vários veículos.
- **Veículo (1:N) OS**: Um veículo pode ter várias ordens de serviço ao longo do tempo.
- **OS (N:M) Serviço**: Uma ordem de serviço pode incluir vários serviços, e um serviço pode estar em várias ordens de serviço.
- **OS (N:M) Peça**: Uma ordem de serviço pode utilizar várias peças, e uma peça pode ser utilizada em diferentes ordens de serviço.
- **Equipe (1:N) OS**: Uma equipe é designada para cada OS.
- **Equipe (N:M) Mecânico**: Uma equipe é composta por vários mecânicos, e um mecânico pode estar em várias equipes.

## Código Mermaid do Esquema Conceitual

![Banco de Dados Desafio II](https://github.com/user-attachments/assets/87fc5b89-5808-4f9c-bb1f-b25f5a0345b2)



