# persona-playbook

Um repositório que documenta um ecossistema completo de **personas técnicas**, **modos de operação cognitiva** e **protocolos de tomada de decisão**, projetado originalmente para o **ChatGPT (Model Set Context)**, mas portável — com adaptações — para outras IAs.

Ele funciona como um **playbook operacional**, permitindo raciocínio técnico especializado em engenharia, arquitetura, segurança, SRE, DevOps, modelagem ofensiva e engenharia reversa conceitual.

---

# 📚 SUMÁRIO

* [1. Introdução](#1-introdução)

    * [1.1 O que é o repositório](#11-o-que-é-o-repositório)
    * [1.2 O prompt metodológico](#12-o-prompt-metodológico)
    * [1.3 Por que criar personas](#13-por-que-criar-personas)
    * [1.4 Por que ChatGPT e Model Set Context](#14-por-que-chatgpt-e-model-set-context)
    * [1.5 MSC vs Memória](#15-msc-vs-memória)

* [2. Personas e Flows](#2-personas-e-flows)

    * [2.1 Lista de Personas](#21-lista-de-personas)
    * [2.2 Lista de Flows](#22-lista-de-flows)
    * [2.3 Descrição breve](#23-descrição-breve)

* [3. Motivações](#3-motivações)

* [4. Benefícios](#4-benefícios)

* [5. Direitos](#5-direitos)

* [6. Portabilidade para Outras IAs (WIP)](#6-portabilidade-para-outras-ias-wip)

* [7. Estrutura do Repositório](#7-estrutura-do-repositório)

---

# 1. Introdução

## 1.1 O que é o repositório

Este repositório consolida um framework completo de **personas técnicas**, cada uma especializada em áreas como:

* backend (várias linguagens)
* arquitetura sistêmica e DDD
* DevOps / SRE / Infraestrutura
* segurança corporativa
* engenharia ofensiva conceitual
* engenharia reversa
* revisão de PR
* coordenação entre fluxos cognitivos

Ele cria um modelo de **multi-agente disciplinado**, capaz de operar como uma equipe estruturada de engenharia.

---

## 1.2 O prompt metodológico

Todas as personas seguem a mesma disciplina cognitiva central:

> Aja como um orientador intelectual rigoroso, focado em elevar meu desempenho cognitivo. Questione premissas, revele vieses, aponte inconsistências e destaque pontos cegos. Priorize precisão e clareza, diferencie fatos, inferências e hipóteses. Se faltar contexto, pare imediatamente e peça esclarecimentos. Nunca preencha lacunas quando eu puder fornecer informações. Explicite quando estiver trabalhando com hipótese. Foque em verdade, rigor técnico e crescimento intelectual.

Essa é a base de coerência do playbook.

Ele pode ser criado em: Personalização -> Instruções personalizadas

## 1.3 Por que criar personas

Sem personas, um único LLM tende a:

* misturar níveis de abstração
* assumir coisas sem perguntar
* gerar código inseguro
* confundir engenharia, arquitetura e segurança
* perder disciplina metodológica
* entregar respostas inconsistentes

As personas resolvem isso, trazendo:

* **especialização profunda**
* **papéis isolados**
* **disciplina previsível**
* **checagem cruzada**
* **decisões mais seguras e explicáveis**

---

## 1.4 Por que ChatGPT e Model Set Context

O **Model Set Context (MSC)** do ChatGPT permite:

* salvar personas persistentemente
* ativá-las com atalhos (@devnode, @security etc.)
* isolar comportamentos
* manter rigidez metodológica
* não depender da Memória tradicional do ChatGPT

É o ambiente ideal para um sistema de multi-personas.

---

## 1.5 MSC vs Memória

### **Model Set Context (MSC):**

* Guarda comportamentos, regras e personalidades.
* Não ocupa memória do usuário.
* Persistência estável.
* Ideal para prompts longos.

### **Memória do ChatGPT:**

* Apenas preferências do usuário.
* Pequena e limitada.
* Não adequada para personas.

---

# 2. Personas e Flows

## 2.1 Lista de Personas

Localizadas em `/personas`:

* [@principal](personas/principal.md)
* [@arquitetura](personas/arquitetura.md)
* [@devnode](personas/devnode.md)
* [@devruby](personas/devruby.md)
* [@devphp](personas/devphp.md)
* [@devandroid](personas/devandroid.md)
* [@infra](personas/infra.md)
* [@devops](personas/devops.md)
* [@security](personas/security.md)
* [@redteam](personas/redteam.md)
* [@reverse](personas/reverse.md)
* [@pr_quality](personas/pr_quality.md)

## 2.2 Lista de Flows

Localizadas em `/flows`:
* [Index](flows/README.md)
* [@flow_strict](flows/flow_strict.md)
* [@flow_auto](flows/flow_auto.md)
* [@flow_mix](flows/flow_mix.md)

No index temos a explicação e exemplos de como utilizar cada flow.

## 2.3 Descrição breve

### Arquitetura e Estratégia

* **@principal** — mentor estratégico, trade-offs, coordenação.
* **@arquitetura** — DDD, padrões sistêmicos, evolução arquitetural.

### Engenharia

* **@devnode** — Node.js/TS internals, performance, segurança.
* **@devruby** — Ruby/Rails, GC, metaprogramação.
* **@devphp** — PHP moderno, frameworks, performance, segurança.
* **@devandroid** — Kotlin/Compose, performance mobile, segurança.

### Infra / DevOps / SRE

* **@infra** — AWS, Kubernetes, SRE, observabilidade.
* **@devops** — CI/CD, automação, GitOps, IaC.

### Segurança e Ofensiva

* **@security** — zero-trust, IAM, MITRE, hardening.
* **@redteam** — ofensa conceitual, kill-chain.
* **@reverse** — engenharia reversa conceitual.

### Qualidade

* **@pr_quality** — revisão técnica + arquitetural + segurança.

### Orquestração

* **@flow_strict** — pipeline rígido.
* **@flow_auto** — seleção automática.
* **@flow_mix** — dinâmico.

---

# 3. Motivações

* Garantir rigor técnico e disciplinar.
* Evitar suposições e decisões precipitadas.
* Criar uma "organização virtual" de engenharia.
* Ter consistência cognitiva.
* Reduzir riscos de segurança, arquitetura e engenharia.

---

# 4. Benefícios

* Respostas mais disciplinadas e confiáveis.
* Decisões com trade-offs claros.
* Menos riscos.
* Raciocínio especializado sob demanda.
* Sistema portável entre diferentes LLMs.

---

# 5. Direitos

Este repositório usa **MIT License** (veja LICENSE).

---

# 6. Portabilidade para Outras IAs (WIP)

Documentado em:

[`core/portability_to_other_llms.md`](core/portability_to_other_llms.md)

Resumo:

* Personas são portáveis.
* Flows são parcialmente portáveis.
* MSC é exclusivo do ChatGPT.
* Outras IAs exigem adaptação.

---

# 7. Estrutura do Repositório

```
persona-playbook/
├── README.md
├── LICENSE
├── .gitignore
├── personas/
├── flows/
└── core/
```
