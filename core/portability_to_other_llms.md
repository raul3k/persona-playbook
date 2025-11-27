# Portabilidade para Outras IAs (WIP)

Este documento explica como portar o *persona-playbook* para outras IAs generativas além do ChatGPT. Ele descreve limitações, adaptações necessárias e estratégias para emular o comportamento do **Model Set Context (MSC)** em plataformas que não possuem esse recurso.

Atualmente, as IAs principais consideradas são:

* **Claude (Anthropic)**
* **Gemini (Google)**
* **Grok (xAI)**
* **Llama / Meta AI (via interfaces como Perplexity, Poe, ou servidores próprios)**
* **Mistral (Mixtral) e modelos open-source em geral**

---

# 1. Conceito central da portabilidade

O *persona-playbook* foi criado para operar com:

* personas persistentes
* protocolos rígidos
* modos de operação
* prompts longos
* disciplina metodológica

Como **apenas o ChatGPT possui MSC**, a portabilidade requer estratégias específicas.

Ao portar para outras IAs, é necessário:

1. **Recriar manualmente as personas** em abas separadas.
2. **Estabelecer contexto no início de cada conversa.**
3. **Usar mensagens fixas de inicialização (preface prompts).**
4. **Controlar o fluxo cognitivo manualmente.**

---

# 2. Portando para Claude

Claude é excelente para:

* longos contextos
* disciplina lógica
* precisão textual

### O que funciona bem:

* prompts longos
* instruções rígidas
* personas isoladas
* explicações profundas

### O que não existe em Claude:

* Model Set Context
* atalhos persistentes (@persona)
* memória de comportamentos

### Como portar:

1. Criar um arquivo local com cada prompt de persona.
2. Abrir uma nova conversa.
3. Colar o prompt integral da persona.
4. Salvar essa conversa nos "Projects" do Claude (recurso novo).
5. Repetir para cada persona.

### Observação:

Claude tende a ser **mais literal**.
É ideal reduzir redundâncias e reforçar regras como: *pare se faltar contexto*.

---

# 3. Portando para Gemini

Gemini possui um estilo:

* mais livre
* mais interpretativo
* mais inclinado a preencher lacunas

### O que funciona:

* prompts diretos e curtos
* instruções claras de restrição cognitiva
* modo de análise profunda (Gemini 2.0)

### O que não existe:

* MSC
* modos persistentes
* controle fino de comportamento

### Como portar:

1. Encapsular cada persona em um bloco curto.
2. Reduzir instruções redundantes.
3. Repetir o prompt inteiro no início de cada sessão.

### Observação:

Para Gemini, é recomendado usar *personas mais enxutas*, pois ele perde contexto com mais facilidade.

---

# 4. Portando para Grok

Grok possui:

* estilo opinativo
* tendência a improvisar
* menor rigidez metodológica

### O que funciona:

* personas diretas
* instruções de estilo

### O que não funciona bem:

* disciplina rígida
* protocolos longos
* prompts muito extensos

### Como portar:

1. Reduzir a persona ao essencial.
2. Evitar listas excessivas.
3. Reforçar regras como: *não preencha lacunas*.

---

# 5. Portando para Llama / Meta AI (Perplexity, Poe, local)

Modelos open-source variam muito.

### O que funciona:

* prompts médios
* regras diretas
* estilos simples

### O que não funciona:

* disciplina complexa
* longos protocolos
* multi-agentes simultâneos

### Como portar:

1. Criar arquivos locais com cada persona.
2. Em sessões locais, colar a persona a cada reinício.
3. Para servidores locais (Ollama, LM Studio), salvar o prompt como *template*.

---

# 6. Portando para Mistral / Mixtral e outras open-source

### O que funciona:

* prompts compactos
* personas simples

### O que não funciona:

* prompts longos demais
* estruturas multi-agente complexas

### Como portar:

* manter cada persona pequena
* reforçar regras básicas somente

---

# 7. Como emular o MSC manualmente

Para qualquer IA sem MSC, o processo é:

### **7.1 Criar um arquivo local por persona**

`personas/devnode.txt`, `personas/security.txt`, etc.

### **7.2 Criar "salas" ou conversas fixas**

Uma aba para cada persona.

### **7.3 Fixar um prompt inicial curto** que será colado toda vez.

### **7.4 Usar comandos prefixados**:

* `#devnode:`
* `#security:`
* `#infra:`

### **7.5 Controlar manualmente os flows**

Sem MSC, o fluxo cognitivo não é automático.

---

# 8. Requisitos mínimos por IA

| IA                | Suporta prompts longos | Suporta disciplina rígida | Ideal para multisistema |
| ----------------- | ---------------------- | ------------------------- | ----------------------- |
| **ChatGPT (MSC)** | ✔️✔️✔️                 | ✔️✔️                      | ✔️ Melhor opção         |
| **Claude**        | ✔️✔️                   | ✔️                        | ✔️ (com Projects)       |
| **Gemini**        | ✔️                     | ⚠️                        | ⚠️                      |
| **Grok**          | ⚠️                     | ⚠️                        | ❌                       |
| **Llama / Meta**  | ✔️                     | ⚠️                        | ⚠️                      |
| **Mistral**       | ✔️                     | ⚠️                        | ❌                       |

---

# 9. Estratégia recomendada

### **Melhor experiência completa:**

**ChatGPT (MSC)**

### **Melhor alternativa geral:**

**Claude**, usando Projects

### **Melhor open-source:**

**Llama 3** rodando localmente

### **Pior para disciplina rígida:**

**Grok**

---

# 10. Status

Este documento é **WIP** e será expandido com:

* templates para cada IA
* scripts auxiliares
* automações
* guias de comparação técnica
