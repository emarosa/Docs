# SOA-Monolith
### Introduction 

This is a practical academic exercise to incentive the study of DevOps and Software Architecture.

### Objectives
* Understanding motivations to break a monolith
* Using a scientific approach to detail architectural changes
* Promoting the adoption of tests during development step
* Promoting the knowledge of Deployment Pipeline
* Sharing tactics to support deployability, availability and scalability

### Steps 
- [x] 1. Decompose SOA-Monolith (this repository) in **PEDIDO service** and **CLIENTE service**, and documenting the Architectural Design Decisions;
- [x] 2. Write the verification of **Cliente** during recording of a new **Pedido**;
- [x] 3. Write automated tests (Unit Tests);
- [x] 4. Pass tests trough pipeline (https://circleci.com/ or Jenkins) using docker;
- [x] 5. Deploy Services on Google Cloud or Amazon AWS;
6. Monitor the the record of new **pedidos** with Elastic Search;
- [x] 7. Replicate PEDIDO service (>2 instances) and support availability of ecosystem;

### Teacher acceptance tests

* Step 1.a: The presentation of 2 repositories with the source code of microservices components;
* Step 1.b: The Technical Documentation of architectural decisions;
* Step 2: The presentation of the verification at runtime;
* Step 3: The presentation of source code of Unit Tests;
* Step 4 & 5: Execution of pipeline until deployment;
* Step 6: Show kibana monitoring the recording of new **pedidos**
* Step 7: "simulate" a **PEDIDO service** (>2 instances) problem and the automated execution of the selfhealing; 

# Escolhas de arquitetura

## SOA-Monolith
    Utilizando o paper 9 como base para definição de arquitetura,o padrão utilizado inicialmente foi o 
    "MP1-Enable the Continuous Integration", pois o contexto era o mesmo do contexto recomendado a este padrão (aplicação rodando atualmente de forma monolitica, e houve a decisão de mudar para microserviços),logo, a aplicação foi decomposta em dois serviçoes distintos, e foi habilitado o continuous integration.
    Após essa fase ,
    Nossa primeira ação foi dividir a aplicação em dois serviços, 
    detalhados abaixo
    

###  PEDIDO service 
    Pedidos service - rodando na porta 8081, nesse serviço encontram-se as rotas destinadas as logicas de pedidos
    
###  CLIENTE service
    Cliente service - rodando na porta 8080, nesse serviço encontram-se as rotas destinadas as logicas de pedidos
