# Capítulo 1: Arquitetura de Software vs Arquitetura Tradicional

## Introdução

Ao longo da história, a palavra "arquitetura" sempre esteve relacionada à arte e técnica de projetar edificações. Com o avanço da computação, o termo passou a ser usado também na engenharia de software, o que levou a comparações e até confusões entre a **arquitetura tradicional** (como a de edifícios) e a **arquitetura de software**. Este capítulo apresenta as similaridades e, principalmente, as diferenças fundamentais entre essas duas abordagens.

---

## O que é Arquitetura Tradicional?

A arquitetura tradicional diz respeito ao projeto físico de construções — casas, edifícios, pontes, entre outros. É uma disciplina que envolve:

- Estabilidade estrutural
- Materiais físicos (concreto, aço, madeira)
- Estilo e estética
- Normas urbanísticas e ambientais
- Um ambiente estático e previsível

O arquiteto tradicional é responsável por equilibrar forma, função, segurança, usabilidade e contexto físico.

---

## O que é Arquitetura de Software?

A arquitetura de software, por outro lado, lida com sistemas intangíveis, lógicos, e altamente mutáveis. Envolve decisões estruturais sobre:

- Componentes e seus relacionamentos
- Módulos, serviços, camadas e integrações
- Padrões de projeto (design patterns)
- Escalabilidade, desempenho, segurança e manutenção
- Ambiente dinâmico e evolução contínua

É a forma como organizamos e estruturamos o sistema de software para garantir que ele atenda aos requisitos de negócio e técnicos ao longo do tempo.

---

## Comparando as Duas Arquiteturas

| Aspecto                     | Arquitetura Tradicional               | Arquitetura de Software                  |
|----------------------------|----------------------------------------|------------------------------------------|
| Natureza                   | Física                                 | Lógica / Virtual                         |
| Evolução após entrega      | Muito limitada                         | Contínua e esperada                      |
| Materiais                  | Concreto, aço, madeira, etc.           | Componentes, serviços, código-fonte     |
| Ambiente de execução       | Estático (mundo físico)                | Dinâmico (infra digital, rede, nuvem)   |
| Requisitos                 | Estáveis (na maioria)                  | Voláteis e mutáveis                     |
| Testabilidade              | Maquetes, cálculos estruturais         | Testes automatizados, protótipos       |
| Temporalidade              | Longo ciclo de projeto e construção    | Ciclo iterativo e incremental           |

Apesar das diferenças, ambas compartilham preocupações com **estrutura**, **escalabilidade**, **confiabilidade** e **usabilidade**.

---

## A Metáfora que Inspira (mas não Sustenta)

A ideia de chamar um profissional de software de “arquiteto” foi inspirada pela similaridade no papel de tomar decisões estruturais importantes. No entanto, a metáfora quebra em muitos aspectos: softwares podem ser reestruturados com frequência, e seu ambiente de execução está sempre em mudança — diferente de uma ponte ou prédio que, uma vez construído, raramente muda sua fundação.

---

## Outras Dimensões a Serem Exploradas

Para diferenciar ainda melhor os níveis de organização de sistemas, vale resumir brevemente os seguintes conceitos, que serão aprofundados em capítulos futuros:

### Arquitetura de Solução (Solution Architecture)

É sobre como os sistemas se conectam. Foca em como um sistema ou conjunto de sistemas resolve um problema de negócio específico. É uma ponte entre os requisitos de negócio e a arquitetura técnica, lidando com integrações, restrições organizacionais e trade-offs.

### Design de Software

Trata da estrutura interna do sistema, considerando coesão, acoplamento, separação de responsabilidades e uso de padrões de projeto (como Strategy, Observer, etc). É onde definimos como os componentes colaboram.

### Design de Código

É o nível mais detalhado e imediato. Foca em legibilidade, clareza, nomeação, boas práticas de programação e uso adequado dos recursos da linguagem. Está diretamente ligado à manutenibilidade do sistema no dia a dia.

---

## Referências

- Bass, L., Clements, P., & Kazman, R. (2012). *Software Architecture in Practice* (3rd ed.). Addison-Wesley.
- Rozanski, N., & Woods, E. (2011). *Software Systems Architecture: Working With Stakeholders Using Viewpoints and Perspectives* (2nd ed.). Addison-Wesley.
- Kruchten, P. (1995). *Architectural Blueprints—The “4+1” View Model of Software Architecture*. IEEE Software.
- Fowler, M. (2002). *Patterns of Enterprise Application Architecture*. Addison-Wesley.
- Shaw, M., & Garlan, D. (1996). *Software Architecture: Perspectives on an Emerging Discipline*. Prentice Hall.
- IEEE 1471 (ISO/IEC/IEEE 42010): *Recommended Practice for Architectural Description of Software-Intensive Systems*.

---

