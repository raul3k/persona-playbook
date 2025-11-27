# Flows — Visão Geral

Este diretório reúne os três *modos de operação cognitiva* que definem **como** o sistema de personas deve trabalhar durante um raciocínio, exploração de ideia, modelagem ou solução técnica.

Os flows não substituem personas. Eles **orquestram o comportamento**.

Cada flow altera o nível de rigidez, validação, profundidade e colaboração entre personas.

---

# 📚 Sumário

* [1. O que são flows?](#1-o-que-são-flows)
* [2. Quando usar cada flow](#2-quando-usar-cada-flow)

    * [2.1 @flow_strict](#21-flow_strict)
    * [2.2 @flow_auto](#22-flow_auto)
    * [2.3 @flow_mix](#23-flow_mix)
* [3. Como os flows se relacionam com as personas](#3-como-os-flows-se-relacionam-com-as-personas)
* [4. Tabela comparativa](#4-tabela-comparativa)
* [5. Links para os arquivos individuais](#5-links-para-os-arquivos-individuais)

---

# 1. O que são flows?

**Flows são modos cognitivos que controlam a forma como o ChatGPT realiza raciocínio, revisão, análise e tomada de decisão.**

Enquanto as personas representam *especializações técnicas*, os flows representam *estilos de operação*.

Exemplo:

* Você pode ativar o **@flow_strict** e, depois, usar **@arquitetura** ou **@devnode**, e o flow ditará o rigor metodológico.

Os flows definem:

* rigidez metodológica
* exigência de contexto
* paralisação diante de inconsistências
* necessidade de validação antes de gerar código ou arquitetura
* como as personas interagem entre si

---

# 2. Quando usar cada flow

## 2.1 **@flow_strict**

O mais rígido, disciplinado e exigente.

Use quando:

* precisa de revisão cuidadosa
* risco técnico é alto
* arquitetura precisa estar correta antes de qualquer ação
* deseja processo semelhante a compliance ou auditoria técnica

Não recomendado para:

* brainstorming
* imaginação livre

---

## 2.2 **@flow_auto**

O flow adaptativo.

Use quando:

* quer explorar ideias livremente
* deseja que o sistema escolha automaticamente a persona adequada
* não sabe ainda qual área técnica está envolvida

Ótimo para:

* ideação
* refinamento inicial
* exploração rápida e aberta

---

## 2.3 **@flow_mix**

O modo híbrido.

Use quando:

* deseja brainstorming **com** disciplina
* quer exploração livre, mas com segurança técnica
* quer que o sistema equilibre criatividade e precisão

É o modo "consultor experiente":

* imagina possibilidades
* aponta riscos
* valida coerência
* mas não bloqueia fluxo como o strict

---

# 3. Como os flows se relacionam com as personas

Flows **não substituem** personas.
Eles servem como **camadas de controle**.

Exemplo:

* `@flow_strict` + `@devnode`: análise rigorosa de back-end
* `@flow_mix` + `@arquitetura`: brainstorming arquitetural seguro
* `@flow_auto`: delega ao sistema escolher automaticamente entre `@principal`, `@security`, `@infra`, etc.

A mecânica funciona assim:

1. O flow influencia o estilo cognitivo.
2. A persona executa o conteúdo técnico.

---

# 4. Tabela comparativa

| Flow             | Rigor       | Criatividade | Segurança | Bloqueios | Uso comum                                             |
| ---------------- | ----------- | ------------ | --------- | --------- | ----------------------------------------------------- |
| **@flow_strict** | 🔒 Máximo   | 🟡 Baixa     | 🔥 Alta   | Muitos    | Arquitetura crítica, segurança, sistemas de pagamento |
| **@flow_auto**   | 🟡 Médio    | 🔵 Alta      | 🟡 Média  | Poucos    | Exploração, ideias, investigação inicial              |
| **@flow_mix**    | 🟠 Moderado | 🔵 Alta      | 🔥 Alta   | Alguns    | Migrações, discussões, design interativo              |

---

# 5. Links para os arquivos individuais

* **[@flow_strict](flow_strict.md)** — Modo rígido e disciplinado.
* **[@flow_auto](flow_auto.md)** — Modo adaptativo automático.
* **[@flow_mix](flow_mix.md)** — Modo híbrido equilibrado.

---

Se quiser, posso gerar também:

* diagrama visual dos flows
* paginação para GitHub Pages
* exemplos de diálogo usando cada flow

---

# 6. Exemplos de Diálogo para Cada Flow

A seguir estão **exemplos reais e diretos** mostrando como cada flow influencia o comportamento cognitivo e o estilo de interação.

---

## **6.1 Exemplo — @flow_strict**

### **Você:**

@flow_strict
Preciso definir a arquitetura de um serviço de pagamento.

### **Assistente:**

Antes de avançarmos, preciso de **contexto obrigatório**:

* escopo funcional
* volume esperado
* requisitos de segurança
* integrações externas
* requisitos de latência e resiliência

Sem isso, qualquer proposta seria especulação.
Por favor, forneça essas informações.

*(O flow strict bloqueia imediatamente caso falte contexto.)*

---

## **6.2 Exemplo — @flow_auto**

### **Você:**

@flow_auto
Quero explorar uma ideia para melhorar nossa experiência de onboarding.

### **Assistente:**

Entendido. Para entender melhor sua intenção, quero explorar primeiro:

* objetivo principal (negócio ou técnico?)
* público de impacto
* métricas que você quer melhorar

Enquanto isso, estou considerando personas como @arquitetura (fluxos), @principal (estratégia) e possivelmente @devnode (viabilidade técnica), mas vou alternar conforme o tema evoluir.

*(Flow auto alterna personas automaticamente e incentiva exploração.)*

---

## **6.3 Exemplo — @flow_mix**

### **Você:**

@flow_mix
Estou pensando em migrar um módulo para outro serviço. O que acha?

### **Assistente:**

Vamos explorar rapidamente as ideias possíveis, mas com segurança e coerência arquitetural:

**Possíveis caminhos:**

1. Extração parcial (mantendo acoplamentos essenciais)
2. Extração total (com event-driven ou API)
3. Migração para um bounded context separado

**Riscos imediatos:**

* aumento da latência
* duplicação de dados
* inconsistência entre serviços

Se quiser, posso aprofundar em qualquer um dos caminhos.

*(Flow mix combina brainstorming com disciplina arquitetural.)*

---

Se quiser, posso adicionar:

* exemplos completos com personas + flows
* casos de uso reais (arquitetura, segurança, engenharia)
* diagramas mostrando a interação entre flows e personas

---

# 7. Exemplos completos usando **flows + personas**

A seguir estão exemplos práticos combinando *flows* com *personas*, simulando situações reais de engenharia, arquitetura e segurança.

---

## **7.1 Arquitetura — @flow_strict + @arquitetura**

### **Você:**

@flow_strict
@arquitetura
Preciso redesenhar o módulo de pagamentos para suportar múltiplos gateways.

### **Assistente (@flow_strict + @arquitetura):**

Antes de propor qualquer solução, preciso de **dados essenciais**:

* quais gateways serão integrados?
* os fluxos atuais de pagamento?
* limites e responsabilidades do bounded context?
* requisitos de consistência?

Sem isso, qualquer proposta arquitetural seria especulativa.
Forneça esses dados para avançarmos.

*(O strict exige contexto; a persona de arquitetura opera no macro.)*

---

## **7.2 Segurança — @flow_mix + @security**

### **Você:**

@flow_mix
@security
Quero revisar a política IAM desse serviço.

### **Assistente:**

Vamos fazer isso com equilíbrio entre fluidez e rigor.

**Primeiro, observações rápidas:**

* a role atual permite `s3:*` em múltiplos buckets → risco alto
* há permissões amplas em `iam:List*` → aumenta superfície de discovery

**Agora, para validar com precisão:**

* qual é o conjunto mínimo de operações necessárias?
* há pipelines que dependem dessa role?
* existe acesso cross-account?

Posso propor uma política restrita assim que você fornecer o escopo exato.

*(Flow mix permite brainstorming com disciplina; persona security analisa vetores reais.)*

---

## **7.3 Engenharia — @flow_auto + @devnode**

### **Você:**

@flow_auto
@devnode
Quero melhorar o desempenho da API de checkout.

### **Assistente:**

Entendido. Antes de sugerir uma otimização, quero identificar o tipo de gargalo.

Perguntas iniciais:

* o problema é **I/O** (DB, rede, cache) ou **CPU** (serialização, JSON, hashing)?
* há métricas de latência ou logs de slow queries?
* existe profiling de heap/GC?

Enquanto você responde, avalio caminhos potenciais:

* otimização de serialização
* redução de roundtrips
* caching prévio
* parallelismo controlado

*(Flow auto adapta o estilo; persona devnode aplica conhecimento profundo de Node.)*

---

# 8. Casos de uso reais

Casos reais de como flows + personas resolvem problemas complexos.

---

## **8.1 Arquitetura de microsserviços — divisão de domínio**

**Contexto:** você quer dividir um monólito.

**Flow recomendado:** @flow_strict
**Personas:** @arquitetura + @principal

**Por quê?**

* decisões de boundaries não podem ser tomadas superficialmente
* risco arquitetural alto

**Como funcionaria:**

1. strict exige contexto
2. arquitetura desenha domínios e limites
3. principal valida trade-offs e impacto organizacional

Resultado: divisão coerente e sustentável.

---

## **8.2 Revisão de PR crítica — segurança**

**Contexto:** PR adiciona OAuth + upload de arquivos.

**Flow recomendado:** @flow_mix
**Personas:** @security + @pr_quality

**Como funcionaria:**

* flow_mix permite discussão aberta mas segura
* @security revisa vetores: XSS, CSRF, SSRF, validação
* @pr_quality valida clareza, testes e arquitetura

Resultado: PR maduro e seguro sem bloquear a conversa.

---

## **8.3 Engenharia — aumento de throughput**

**Contexto:** lambda processa 10k msgs/min e precisa chegar a 30k.

**Flow recomendado:** @flow_auto
**Personas:** @devnode, @infra, @security

**Como funcionaria:**

* flow_auto ativa quem for necessário
* @infra avalia limites de filas, escalabilidade
* @devnode otimiza concorrência, I/O e hot-paths
* @security valida permissões e riscos de burst

Resultado: solução rápida, técnica e segura.

---
