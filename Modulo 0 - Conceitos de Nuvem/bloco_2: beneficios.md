## ☁️ AZ-900 — Benefícios da computação em nuvem

<p align="justify">A nuvem oferece diversos benefícios além de simplesmente hospedar recursos. Para o AZ-900, é importante saber diferenciar principalmente <strong>alta disponibilidade, escalabilidade, confiabilidade, previsibilidade, segurança, governança e capacidade de gerenciamento</strong>.</p>

---

<h3><strong style='color: skyblue'>1️⃣ Alta disponibilidade (High Availability)</strong></h3>

<p align="justify"><strong>Alta disponibilidade</strong> significa manter aplicações e serviços disponíveis e funcionando pelo maior tempo possível, mesmo quando ocorrem falhas.</p>

<p align="justify">A nuvem pode utilizar recursos redundantes, zonas de disponibilidade e outras estratégias para reduzir o impacto de falhas.</p>

### Exemplo

<pre>
                APLICAÇÃO
                    │
          ┌─────────┴─────────┐
          │                   │
       Zona 1              Zona 2
          │                   │
       Instância           Instância
          │                   │
          └─────────┬─────────┘
                    │
              Serviço continua
                 disponível
</pre>

<p align="justify">Se uma instância ou uma zona apresentar uma falha, outra instância poderá continuar atendendo às solicitações, dependendo da arquitetura adotada.</p>

> **AZ-900:** Alta disponibilidade = manter o serviço disponível mesmo diante de falhas.

---

<h3><strong style='color: skyblue'>2️⃣ Escalabilidade (Scalability)</strong></h3>

<p align="justify"><strong>Escalabilidade</strong> é a capacidade de aumentar ou diminuir recursos para atender à demanda.</p>

### Escala vertical — Scale Up / Down

<p align="justify">Aumenta ou reduz a capacidade de um recurso existente.</p>

<pre>
VM pequena
   │
   ▼
VM maior
mais CPU / RAM
</pre>

### Escala horizontal — Scale Out / In

<p align="justify">Adiciona ou remove instâncias.</p>

<pre>
       1 VM
        │
        ▼
   ┌────┼────┐
   ▼    ▼    ▼
  VM1  VM2  VM3
</pre>

### Benefícios

- Atender picos de demanda.
- Reduzir recursos quando a demanda diminui.
- Evitar desperdício de capacidade.
- Melhorar o desempenho.
- Adaptar a infraestrutura à necessidade da aplicação.

> **PEGADINHA AZ-900:**  
> **Scale Up = aumentar o tamanho/capacidade.**  
> **Scale Out = aumentar a quantidade de instâncias.**

---

<h3><strong style='color: skyblue'>3️⃣ Alta disponibilidade × Escalabilidade</strong></h3>

| Conceito | Pergunta que responde |
|---|---|
| **Alta disponibilidade** | "O serviço continua disponível?" |
| **Escalabilidade** | "Consigo aumentar/diminuir a capacidade?" |

> **DECORA:**  
> 🟢 **Disponibilidade = continuar funcionando**  
> 🔵 **Escalabilidade = aumentar/diminuir capacidade**

---

<h3><strong style='color: skyblue'>4️⃣ Confiabilidade (Reliability)</strong></h3>

<p align="justify"><strong>Confiabilidade</strong> é a capacidade de um sistema funcionar de maneira consistente e se recuperar de falhas.</p>

<p align="justify">A nuvem oferece recursos que ajudam a criar arquiteturas resilientes, como redundância, replicação, backup e distribuição geográfica.</p>

### Exemplo

<pre>
Recurso principal
      │
      ├──────────► Cópia redundante
      │
      └──────────► Backup
</pre>

<p align="justify">Se houver uma falha, mecanismos de redundância ou recuperação podem permitir que o serviço continue ou seja restaurado.</p>

> **AZ-900:** Confiabilidade = capacidade de operar de forma consistente e lidar com falhas.

---

<h3><strong style='color: skyblue'>5️⃣ Previsibilidade (Predictability)</strong></h3>

<p align="justify">A nuvem permite maior <strong>previsibilidade</strong> de desempenho e custos por meio de recursos de monitoramento, métricas, autoscaling, modelos de preços e gerenciamento de capacidade.</p>

### Previsibilidade de desempenho

<p align="justify">É possível monitorar recursos e ajustar a capacidade de acordo com a demanda.</p>

### Previsibilidade de custos

<p align="justify">Ferramentas de gerenciamento de custos permitem acompanhar gastos, definir orçamentos e analisar tendências.</p>

### Exemplo

<pre>
Monitoramento
     │
     ├── CPU
     ├── Memória
     ├── Tráfego
     └── Custos
             │
             ▼
      Ajustar recursos
             │
             ▼
      Maior previsibilidade
</pre>

> **DECORA:**  
> **Previsibilidade = saber/estimar melhor o comportamento e os custos do ambiente.**

---

<h3><strong style='color: skyblue'>6️⃣ Confiabilidade × Previsibilidade</strong></h3>

| Conceito | Foco |
|---|---|
| **Confiabilidade** | Sistema funciona de forma consistente e lida com falhas |
| **Previsibilidade** | Comportamento, desempenho e custos podem ser estimados/gerenciados |

> **PEGADINHA:** Confiabilidade não significa simplesmente "ter backup". Backup é um mecanismo que pode contribuir para recuperação e confiabilidade.

---

<h3><strong style='color: skyblue'>7️⃣ Segurança na nuvem</strong></h3>

<p align="justify">A nuvem oferece recursos e serviços para ajudar a proteger identidades, aplicações, redes e dados.</p>

### Exemplos

- Microsoft Entra ID → identidade e autenticação.
- Microsoft Defender for Cloud → postura de segurança e proteção de workloads.
- Network Security Groups → filtragem de tráfego.
- Azure Key Vault → gerenciamento seguro de chaves e segredos.
- Microsoft Sentinel → SIEM e análise de segurança.

<p align="justify">Além dos recursos fornecidos pelo provedor, o cliente continua tendo responsabilidades de segurança conforme o modelo de responsabilidade compartilhada.</p>

> **AZ-900:** Segurança na nuvem = recursos e controles para proteger identidade, dados, aplicações e infraestrutura.

---

<h3><strong style='color: skyblue'>8️⃣ Governança (Governance)</strong></h3>

<p align="justify"><strong>Governança</strong> é o conjunto de processos, regras e controles usados para garantir que os recursos sejam utilizados de acordo com as políticas da organização.</p>

### Exemplos no Azure

- Azure Policy.
- RBAC.
- Tags.
- Management Groups.
- Azure Blueprints — conceito histórico que pode aparecer em materiais antigos, mas não é a ferramenta principal atual.

### Exemplo

<pre>
Organização
     │
     ▼
Política
"Somente regiões aprovadas"
     │
     ▼
Azure Policy
     │
     ▼
Recursos avaliados
</pre>

<p align="justify">A governança ajuda a controlar conformidade, localização de recursos, configurações permitidas e padrões organizacionais.</p>

> **DECORA:**  
> **Segurança = proteger.**  
> **Governança = controlar e garantir conformidade.**

---

<h3><strong style='color: skyblue'>9️⃣ Segurança × Governança</strong></h3>

| Conceito | Pergunta |
|---|---|
| **Segurança** | "Como protegemos nossos recursos?" |
| **Governança** | "Como garantimos que os recursos sejam utilizados de acordo com as regras?" |

### Exemplo

**Segurança:**

> "Somente usuários autorizados podem acessar este recurso."

**Governança:**

> "Recursos desta organização só podem ser criados em regiões aprovadas."

---

<h3><strong style='color: skyblue'>🔟 Capacidade de gerenciamento (Manageability)</strong></h3>

<p align="justify"><strong>Capacidade de gerenciamento</strong> é a facilidade de administrar, monitorar, configurar e automatizar os recursos na nuvem.</p>

### Exemplos

- Azure Portal.
- Azure CLI.
- Azure PowerShell.
- Azure Resource Manager (ARM).
- Azure Monitor.
- Templates/IaC.
- Automação.
- Tags.
- Políticas.

### Gerenciamento centralizado

<pre>
                  AZURE
                    │
       ┌────────────┼────────────┐
       │            │            │
    Portal         CLI       PowerShell
       │            │            │
       └────────────┼────────────┘
                    │
                    ▼
               Recursos
</pre>

<p align="justify">Em vez de administrar cada servidor individualmente, é possível utilizar ferramentas centralizadas para gerenciar grandes quantidades de recursos.</p>

> **AZ-900:** Gerenciabilidade = facilidade para administrar, monitorar e automatizar recursos.

---

<h3><strong style='color: skyblue'>1️⃣1️⃣ Benefícios da capacidade de gerenciamento</strong></h3>

### Monitoramento

<p align="justify">Acompanhar métricas, logs, desempenho e disponibilidade.</p>

### Automação

<p align="justify">Executar tarefas automaticamente, reduzindo trabalho manual.</p>

### Gerenciamento centralizado

<p align="justify">Administrar recursos por ferramentas como Azure Portal, CLI e PowerShell.</p>

### Infraestrutura como código

<p align="justify">Definir infraestrutura por meio de arquivos/templates, tornando a implantação mais consistente e repetível.</p>

### Tags

<p align="justify">Adicionar informações aos recursos para organização, identificação, custos e gerenciamento.</p>

---

<h3><strong style='color: skyblue'>1️⃣2️⃣ Resumo dos benefícios</strong></h3>

| Benefício | O que significa |
|---|---|
| **Alta disponibilidade** | Serviço continua disponível apesar de falhas |
| **Escalabilidade** | Aumentar ou diminuir capacidade conforme demanda |
| **Confiabilidade** | Operação consistente e capacidade de lidar com falhas |
| **Previsibilidade** | Melhor capacidade de estimar/controlar desempenho e custos |
| **Segurança** | Proteção de identidades, dados, aplicações e recursos |
| **Governança** | Regras, políticas e conformidade |
| **Gerenciabilidade** | Administrar, monitorar e automatizar recursos |

---

<h3><strong style='color: skyblue'>🧠 Mapa mental</strong></h3>

<pre>
                 BENEFÍCIOS DA NUVEM
                         │
       ┌─────────────────┼─────────────────┐
       │                 │                 │
  DISPONIBILIDADE    CONFIABILIDADE     SEGURANÇA
       │                 │                 │
       ├── Alta          ├── Resiliência   ├── Identidade
       ├── Redundância   ├── Recuperação   ├── Dados
       └── Zonas         └── Redundância   └── Rede
       │
       ▼
  ESCALABILIDADE
       │
       ├── Scale Up
       └── Scale Out

       │
       ▼
  PREVISIBILIDADE
       │
       ├── Desempenho
       └── Custos

       │
       ▼
  GOVERNANÇA
       │
       ├── Políticas
       ├── Conformidade
       └── Controle

       │
       ▼
  GERENCIABILIDADE
       │
       ├── Portal
       ├── CLI
       ├── PowerShell
       ├── Monitoramento
       └── Automação
</pre>

<h3><strong style='color: skyblue'>🎯 DECORAÇÃO FINAL AZ-900</strong></h3>

<pre>
ALTA DISPONIBILIDADE
→ continuar funcionando

ESCALABILIDADE
→ aumentar/diminuir capacidade

CONFIABILIDADE
→ funcionar de forma consistente + lidar com falhas

PREVISIBILIDADE
→ estimar/controlar desempenho e custos

SEGURANÇA
→ proteger

GOVERNANÇA
→ estabelecer regras + conformidade

GERENCIABILIDADE
→ administrar + monitorar + automatizar
</pre>

> **🔥 PEGADINHA CLÁSSICA:**  
> **Disponibilidade ≠ Escalabilidade ≠ Confiabilidade.**
>
> **Disponibilidade** → serviço está disponível?  
> **Escalabilidade** → consigo ajustar a capacidade?  
> **Confiabilidade** → o sistema consegue operar consistentemente e lidar com falhas?
