# DOCUMENTO DE ARQUITETURA DE SOFTWARE - HELPY

## Sumário
- [DOCUMENTO DE ARQUITETURA DE SOFTWARE - HELPY](#documento-de-arquitetura-de-software---helpy)
  - [Sumário](#sumário)
  - [Introdução](#introdução)
  - [Finalidade](#finalidade)
  - [Escopo](#escopo)
  - [Requisitos e Restrições da Arquitetura](#requisitos-e-restrições-da-arquitetura)
  - [Visão de Casos de Uso](#visão-de-casos-de-uso)
  - [Visão Lógica](#visão-lógica)
    - [Visão Geral](#visão-geral)
    - [Pacotes de Design Significativos do Ponto de Vista da Arquitetura](#pacotes-de-design-significativos-do-ponto-de-vista-da-arquitetura)
  - [Visão de Implantação](#visão-de-implantação)
  - [Visão da implementação](#visão-da-implementação)
  - [Volume e Desempenho](#volume-e-desempenho)
  - [Qualidade](#qualidade)

## Introdução

O presente documento tem como objetivo descrever o documento de arquitetura do projeto Helpy. Este sistema tem como finalidade o aumento do índice de doações de alimentos na Ceilândia, mediante a realização de campanhas que podem ser compartilhadas nas redes sociais.O app oferece uma plataforma digital que busca integrar famílias e voluntários de forma eficiente em eventos beneficentes.

## Finalidade

Este documento oferece uma visão geral arquitetural abrangente do sistema, usando diversas visões arquiteturais para representar diferentes aspectos do sistema. O objetivo deste documento é capturar e comunicar as decisões arquiteturais significativas que foram tomadas em relação ao sistema. O documento irá adotar uma estrutura baseada na visão “4+1” de modelo de arquitetura, conforme (Kruchten, 1994).

![Use Case!](img/visao-4x1.png "Visões 4+1 da arquitetura de software (Kruchten, 1994)")

O público-alvo específico do documento são os membros da equipe que desenvolvem o projeto, pois há a possibilidade de que com este documento, uma visão arquitetural e abrangente do sistema seja obtida, além de auxiliar no entendimento do sistema por novos membros da equipe
futuramente.

## Escopo

O Helpy é um aplicativo mobile para Android (6.0.1 ou mais) e IOS (10 ou mais) que tem como objetivo promover eventos de arrecadação e doação de mantimentos para famílias de baixa renda da Ceilândia. Neste documento, os envolvidos no projeto podem captar aspectos arquiteturais do sistema que são necessários para o desenvolvimento de uma solução que atenda às necessidades dos usuários finais. Além de auxiliar no entendimento do sistema por novos membros da equipe.

## Requisitos e Restrições da Arquitetura

 | Requisito           | Solução                               |
 | ------------------- | ------------------------------------- |
 | Linguagem           | React Native.                         |
 | Plataforma          | Apache HTTP Server.                   |
 | Segurança           | Criptografia de dados dos clientes.   |
 | Persistência        | Banco de dados relacional MYSQL v8.0. |
 | Internacionalização | Não se aplica                         |
  
## Visão de Casos de Uso

![Use Case!](/usercase/UseCaseHelpy.png "Diagrama de Casos de Uso do Sistema")

## Visão Lógica

### Visão Geral

![Use Case!](/img/visao-geral.png "Visão Geral")

### Pacotes de Design Significativos do Ponto de Vista da Arquitetura

![Use Case!](/img/diagrama-de-pacotes.png "Diagrama de pacotes")

## Visão de Implantação

![Use Case!](/img/diagrama-de-implantacao.png "Diagrama de pacotes")

## Visão da implementação

![Use Case!](/img/diagrama-de-implementacao.png "Diagrama de pacotes")

## Volume e Desempenho

Tempo de resposta: O Helpy deverá retornar o resultado no tempo médio de 2 segundos
podendo chegar no máximo 5 segundos para concluir uma requisição.
Capacidade: A plataforma deve manter ao menos 500 pessoas simultâneas não podendo
perder desempenho em telas de carregamento ou de seções.

## Qualidade

| Item            | Descrição                                                                                                                                                         | Solução                                                                                                                                                                                                          |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Escalabilidade  | A possibilidade de expandir (muito) o seu número de clientes, usuários e/ou faturamento de forma acelerada, sem precisar aumentar seus custos na mesma proporção. | Não se aplica                                                                                                                                                                                                    |
| Confiabilidade  | É a probabilidade de o software não causar uma falha num sistema durante um determinado período de tempo sob condições especificadas.                             | A utilização de maneiras de receber o feedback do usuário onde seriam relatados possíveis ocorrências de bugs ou lentidão do sistema, afim de proporcionar um melhor funcionamento da plataforma para o usuário  |
| Disponibilidade | Esta é uma medida de quão disponível o sistema estaria para uso, isto é, quão disponível o sistema estaria para efetuar um serviço solicitado por algum usuário.  | A plataforma estará sempre online, buscando também atender 99% das solicitações dos usuários, salvo quando houver alguma manutenção no sistema.                                                                  |
| Portabilidade   | A facilidade na qual o software pode ser transferido de um sistema computacional ou ambiente para outro.                                                          | A plataforma terá portabilidade para sistemas mobile como por exemplo Android e IOS.                                                                                                                             |
| Segurança       | a segurança de que acessos não autorizados ao sistema e dados associados não serão permitidos.                                                                    | O sistema contará com criptografia de todos os dados do usuário, assim também a realização de manutenções pelo menos a cada 3 meses lançando assim patchs de segurança, afim de manter a integridade do sistema. |
  