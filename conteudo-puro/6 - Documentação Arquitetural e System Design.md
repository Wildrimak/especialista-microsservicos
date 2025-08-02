# Capítulo 6: Documentação Arquitetural e System Design

## Importância da Documentação Arquitetural

A documentação arquitetural é essencial para garantir a clareza, rastreabilidade e justificativa das decisões tomadas ao longo do ciclo de vida de um sistema. Documentar não é apenas um ato burocrático, mas uma forma de preservar o raciocínio técnico e estratégico da equipe de arquitetura.

### Por que documentar?

* **Explica o porquê das decisões**: não apenas o que foi decidido, mas as motivações por trás das escolhas arquiteturais.
* **Estrutura, evolução e objetivos técnicos**: permite rastrear como a arquitetura se desenvolveu e os objetivos que guiavam cada etapa.
* **Evita problemas futuros**: a ausência de histórico pode levar à repetição de erros ou ao abandono de decisões eficazes por falta de contexto.

## Tipos de Documentação Arquitetural

### Design Docs

Os *Design Docs* são documentos escritos **antes da implementação**, com o objetivo de discutir e registrar ideias, avaliar alternativas e estabelecer uma base sólida para as decisões que virão.

#### Características gerais:

* Criado para análise e revisão coletiva.
* Registro formal das decisões arquiteturais.
* Ajuda a alinhar as partes interessadas.

#### Estrutura típica:

* **Contexto e o problema a ser resolvido**
* **Requisitos funcionais e não funcionais** (objetivos)
* **Arquitetura proposta**
* **Alternativas consideradas** e seus **trade-offs**
* **Riscos e desafios identificados**
* **Plano de implementação**
* **Diagramas arquiteturais**

#### Recursos úteis:

* Templates públicos e exemplos estão disponíveis em: [https://designdocs.dev/library](https://designdocs.dev/library)

### ADRs (Architecture Decision Records)

Os *ADRs* são pequenos documentos que registram decisões arquiteturais **já adotadas**, explicando o raciocínio por trás de cada uma.

#### Objetivos:

* Registrar mudanças relevantes: escolha de frameworks, configuração de serviços, padrões etc.
* Preservar o histórico para futuros times ou manutenções.
* Devem ser versionados junto com o código-fonte.

#### Estrutura típica:

* **Título**
* **Contexto**
* **Decisão**
* **Principais razões**
* **Alternativas consideradas**
* **Impacto**
* **Status da decisão** (proposta, aceita, rejeitada, etc.)

## System Design

O *System Design* é o processo de projetar a arquitetura de um sistema considerando seus requisitos e restrições. É um passo essencial na transição da análise do problema para a criação de uma solução técnica concreta.

### Etapas principais:

* Compreender o problema a ser resolvido.
* Levantar os requisitos funcionais e não funcionais.
* Propor uma arquitetura que atenda aos objetivos do sistema.
* Criar os diagramas e artefatos técnicos necessários.

### Exemplos práticos:

* O site [bytebytego.com](https://bytebytego.com) reúne estudos de caso e documentos públicos sobre arquitetura de sistemas em larga escala.

## System Design Interview

As entrevistas técnicas de *System Design* são comuns para cargos de engenheiro de software e arquiteto de sistemas. Nelas, o candidato é desafiado a projetar uma solução arquitetural para um problema realista em tempo limitado.

### Como funciona:

* O entrevistador apresenta um problema de alto nível.
* O candidato deve propor uma arquitetura escalável, segura e robusta.
* É avaliada a capacidade de comunicação, raciocínio lógico, visão sistêmica e conhecimento técnico.

### Exemplos comuns de desafios:

* Projetar um sistema de encurtamento de URLs (tipo Bit.ly)
* Projetar uma arquitetura semelhante ao WhatsApp
* Projetar uma solução como o Netflix

Esses desafios ajudam a simular situações reais enfrentadas por arquitetos e engenheiros em empresas de tecnologia.

---

## Referências

* Richards, Mark; Ford, Neal. *Fundamentals of Software Architecture: An Engineering Approach*. O'Reilly Media, 2020.
* designdocs.dev — Templates e exemplos de Design Docs: [https://designdocs.dev/library](https://designdocs.dev/library)
* bytebytego.com — Estudo de casos reais de system design: [https://bytebytego.com](https://bytebytego.com)
* ThoughtWorks. *Architecture Decision Records (ADRs)*: [https://www.thoughtworks.com/en-us/radar/techniques/lightweight-architecture-decision-records](https://www.thoughtworks.com/en-us/radar/techniques/lightweight-architecture-decision-records)
* Microsoft Docs. *Documenting software architecture*: [https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/documentation](https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/documentation)
* Brown, Simon. *The C4 Model for Visualising Software Architecture*: [https://c4model.com](https://c4model.com)
