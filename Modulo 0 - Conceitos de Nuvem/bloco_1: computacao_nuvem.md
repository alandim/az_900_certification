## ☁️ AZ-900 — Conceitos de nuvem, modelos e preços

<h3><strong style='color: skyblue'>1️⃣ O que é computação em nuvem?</strong></h3>

<p align="justify"><strong>Computação em nuvem</strong> é a entrega de recursos de computação pela Internet, sob demanda, como servidores, armazenamento, bancos de dados, redes, aplicações e outros serviços.</p>

<p align="justify">Em vez de uma organização precisar comprar e manter toda a infraestrutura física, ela pode utilizar recursos fornecidos por um provedor de nuvem, como o Azure.</p>

### Exemplos de recursos na nuvem

- Máquinas virtuais.
- Armazenamento.
- Bancos de dados.
- Redes.
- Aplicações.
- Serviços de IA.
- Serviços de segurança.

> **AZ-900:** Nuvem = recursos de TI disponibilizados pela Internet, sob demanda.

### Características fundamentais

- Recursos sob demanda.
- Acesso pela rede/Internet.
- Escalabilidade.
- Elasticidade.
- Modelo baseado em consumo.
- Redução da necessidade de infraestrutura física própria.

---

<h3><strong style='color: skyblue'>2️⃣ Modelo de responsabilidade compartilhada</strong></h3>

<p align="justify">No modelo de <strong>responsabilidade compartilhada</strong>, a segurança e o gerenciamento do ambiente são divididos entre o provedor de nuvem e o cliente.</p>

<p align="justify">O Azure é responsável pela infraestrutura física e por determinados componentes do serviço. O cliente continua responsável por aspectos que dependem do serviço utilizado e de sua própria configuração.</p>

### Regra geral

<pre>
             RESPONSABILIDADE
                    │
       ┌────────────┴────────────┐
       │                         │
     AZURE                    CLIENTE
       │                         │
 Infraestrutura             Dados
 Datacenter                  Identidades
 Hardware                    Configurações
 Rede física                 Acesso
 Virtualização               Aplicações*
</pre>

<p align="justify">Quanto mais gerenciado for o serviço, maior será a parcela de gerenciamento realizada pelo provedor.</p>

### IaaS × PaaS × SaaS

<pre>
IaaS
│
├── Azure → hardware / datacenter / virtualização
└── Cliente → SO / aplicações / dados

PaaS
│
├── Azure → infraestrutura + SO + runtime
└── Cliente → aplicação + dados/configuração

SaaS
│
├── Azure/provedor → infraestrutura + aplicação
└── Cliente → dados + acesso + configurações
</pre>

> **PEGADINHA:** "Está na nuvem" não significa que o provedor é responsável por tudo.

> **DECORA:** **Responsabilidade compartilhada = depende do serviço.**

---

<h3><strong style='color: skyblue'>3️⃣ Modelos de implantação de nuvem</strong></h3>

<p align="justify">Os principais modelos de implantação são <strong>nuvem pública, nuvem privada e nuvem híbrida</strong>.</p>

---

<h3><strong style='color: skyblue'>4️⃣ Nuvem pública (Public Cloud)</strong></h3>

<p align="justify">Na <strong>nuvem pública</strong>, os recursos são fornecidos por um provedor de nuvem e utilizados por diferentes clientes.</p>

<p align="justify">A infraestrutura física pertence e é administrada pelo provedor.</p>

### Exemplo

<pre>
                Azure
                  │
       ┌──────────┼──────────┐
       │          │          │
    Cliente A  Cliente B  Cliente C
</pre>

### Características

- Infraestrutura do provedor.
- Recursos acessados pela rede.
- Não é necessário possuir datacenter próprio.
- Alta escalabilidade.
- Modelo de pagamento baseado em consumo é comum.

### Casos de uso

- Aplicações Web.
- Startups.
- Desenvolvimento e testes.
- Aplicações que precisam escalar rapidamente.
- Organizações que não querem manter infraestrutura física própria.

> **DECORA:** **Pública = infraestrutura do provedor.**

---

<h3><strong style='color: skyblue'>5️⃣ Nuvem privada (Private Cloud)</strong></h3>

<p align="justify">A <strong>nuvem privada</strong> é um ambiente de nuvem dedicado a uma única organização.</p>

<p align="justify">Pode estar localizada no próprio datacenter da organização ou ser hospedada por um terceiro.</p>

### Exemplo

<pre>
             ORGANIZAÇÃO
                  │
        ┌─────────┴─────────┐
        │   Nuvem Privada   │
        │                   │
        │ Recursos dedicados│
        └───────────────────┘
</pre>

### Características

- Ambiente dedicado.
- Maior controle sobre a infraestrutura.
- Pode atender requisitos específicos de segurança ou conformidade.
- Normalmente exige mais gerenciamento do que uma nuvem pública.

### Casos de uso

- Requisitos específicos de conformidade.
- Necessidade de controle dedicado.
- Aplicações que não podem ou não devem utilizar uma nuvem pública.
- Organizações que já possuem infraestrutura de datacenter.

> **DECORA:** **Privada = dedicada a uma organização.**

---

<h3><strong style='color: skyblue'>6️⃣ Nuvem híbrida (Hybrid Cloud)</strong></h3>

<p align="justify">A <strong>nuvem híbrida</strong> combina ambientes de nuvem pública e privada/on-premises, permitindo que eles trabalhem de forma integrada.</p>

### Exemplo

<pre>
       DATACENTER / PRIVADA
                │
                │ conexão
                │
                ▼
          AZURE / PÚBLICA
                │
                ▼
          Aplicações
</pre>

### Casos de uso

- Manter sistemas legados on-premises e utilizar Azure para novos sistemas.
- Expandir capacidade para a nuvem.
- Manter determinados dados localmente.
- Utilizar serviços de nuvem sem migrar tudo de uma vez.
- Cenários de migração gradual.

> **DECORA:** **Híbrida = pública + privada/on-premises trabalhando juntas.**

---

<h3><strong style='color: skyblue'>7️⃣ Comparação dos modelos de nuvem</strong></h3>

| Modelo | Infraestrutura | Controle | Caso de uso |
|---|---|---|---|
| **Pública** | Provedor | Menor controle físico | Aplicações escaláveis |
| **Privada** | Dedicada | Maior controle | Requisitos específicos |
| **Híbrida** | Pública + privada | Integra os dois ambientes | Migração e integração |

### Como identificar na prova

> "A empresa quer utilizar infraestrutura compartilhada de um provedor."  
> → **Nuvem pública**

> "A empresa precisa de um ambiente dedicado exclusivamente a ela."  
> → **Nuvem privada**

> "A empresa quer manter parte da infraestrutura local e utilizar Azure para outra parte."  
> → **Nuvem híbrida**

---

<h3><strong style='color: skyblue'>8️⃣ Modelo baseado em consumo (Consumption-Based Model)</strong></h3>

<p align="justify">No <strong>modelo baseado em consumo</strong>, o cliente paga pelos recursos que utiliza, em vez de necessariamente comprar toda a infraestrutura antecipadamente.</p>

### Modelo tradicional

<pre>
Comprar servidores
      ↓
Investimento inicial alto
      ↓
Infraestrutura própria
      ↓
Pagar mesmo se estiver subutilizada
</pre>

### Nuvem / consumo

<pre>
Usar recurso
     ↓
Medir consumo
     ↓
Pagar pelo uso
     ↓
Aumentar ou reduzir conforme necessidade
</pre>

### Benefícios

- Menor investimento inicial.
- Custos associados ao uso.
- Flexibilidade.
- Possibilidade de aumentar ou diminuir recursos.
- Evita comprar capacidade muito superior à necessidade.

> **DECORA:** **Consumption-based = paga pelo que usa.**

---

<h3><strong style='color: skyblue'>9️⃣ CapEx × OpEx</strong></h3>

<p align="justify">Essa diferença é importante para o AZ-900.</p>

### CapEx — Capital Expenditure

<p align="justify">Gasto de capital para adquirir ativos físicos.</p>

**Exemplos:**

- Comprar servidores.
- Comprar equipamentos de rede.
- Construir/ampliar datacenter.

<pre>
CAPEX
↓
Comprar infraestrutura
↓
Grande investimento inicial
