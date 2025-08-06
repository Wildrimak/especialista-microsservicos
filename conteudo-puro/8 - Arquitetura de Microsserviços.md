# Capítulo 8: Arquitetura de Microsserviços

## Introdução

A arquitetura de microsserviços é uma abordagem de design de sistemas que ganhou ampla adoção nos últimos anos, mas que não possui uma definição definitiva e universal. Autores e especialistas propõem interpretações distintas com base em suas experiências, contextos e necessidades de mercado. No entanto, há alguns princípios fundamentais que costumam ser aceitos amplamente e que vamos explorar neste capítulo.

## Microsserviços não são sobre ferramentas

Uma das ideias equivocadas mais comuns é associar microsserviços à escolha de uma linguagem específica, framework ou ferramenta. Na verdade, microsserviços são sobre **modelagem organizacional e arquitetural**, e não sobre tecnologia em si. Trata-se de uma abordagem para dividir um sistema em módulos menores, independentes e autônomos, cada um focado em uma área específica de negócio.

## Isolamento de estado: cada microsserviço gerencia seus dados

Um dos pilares dos microsserviços é a autonomia completa de cada serviço, o que inclui o gerenciamento de seu próprio estado e dados. Isso significa que:

* **Cada microsserviço tem seu próprio banco de dados**, ou outro mecanismo de armazenamento, de forma que não compartilha diretamente os dados com outros serviços.
* Segue-se o padrão conhecido como **Database per Service Pattern**, que reforça o encapsulamento dos dados dentro dos limites do serviço.
* Mudanças internas em um serviço não devem afetar outros serviços, mantendo **contratos bem definidos** para comunicação externa, geralmente via APIs ou eventos.

### Evitando acoplamento através do banco de dados

Compartilhar um banco de dados entre microsserviços pode parecer tentador, especialmente para reaproveitar dados ou facilitar queries complexas. No entanto, isso gera **forte acoplamento** e quebra os princípios de autonomia. O banco de dados deve ser considerado um **detalhe interno** do serviço, não uma dependência compartilhada.

> "Quando dois serviços compartilham um banco de dados, qualquer mudança no esquema afeta todos os consumidores, mesmo que indiretamente. Isso fere a independência dos microsserviços." — Sam Newman, *Building Microservices*

### Casos especiais: quando o compartilhamento é aceitável

Embora o uso de um banco de dados compartilhado seja geralmente considerado um **anti-padrão** ("Shared Database Anti-Pattern"), há situações específicas onde ele pode ser adotado de forma consciente e temporária:

* Quando os **dados são altamente relacionados** e sua separação causaria impacto de performance ou complexidade excessiva.
* Para **operações de leitura intensiva**, como dashboards analíticos ou relatórios agregados.
* Em contextos onde a **latência de comunicação entre microsserviços é um gargalo crítico**.
* Em sistemas legados, como uma etapa de transição para microsserviços, evitando uma refatoração abrupta e arriscada.
* Quando a **análise dos trade-offs** mostra que os benefícios do compartilhamento superam os riscos no curto prazo.

> O importante é que essa escolha seja **consciente**, **temporária** e que os riscos sejam documentados e monitorados.

## Baixo acoplamento e alta coesão

Outro pilar da arquitetura de microsserviços é o **baixo acoplamento** entre os serviços. Cada serviço deve poder evoluir, escalar ou ser reimplantado de forma independente dos demais. Para isso:

* A comunicação entre serviços deve ocorrer por **interfaces bem definidas** (como REST, gRPC, eventos, etc.).
* Os serviços devem ter **alta coesão**, ou seja, todas as funcionalidades dentro de um serviço devem estar fortemente relacionadas ao seu contexto de negócio.
* Mudanças no banco de dados ou na lógica interna de um serviço **não devem impactar consumidores externos**.

---

## Referências

* Newman, Sam. *Building Microservices*. O'Reilly Media, 2015.
* Richards, Mark. *Software Architecture Patterns*. O'Reilly Media, 2015.
* Evans, Eric. *Domain-Driven Design: Tackling Complexity in the Heart of Software*. Addison-Wesley, 2003.
* Microsoft. [Microservices architecture style](https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/microservices)
* ThoughtWorks. [Technology Radar - Microservices](https://www.thoughtworks.com/en-us/radar/techniques/microservices)
* Fowler, Martin. [Microservices](https://martinfowler.com/articles/microservices.html)
