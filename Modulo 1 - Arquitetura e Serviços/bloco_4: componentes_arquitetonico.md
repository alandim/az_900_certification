## 🏗️ AZ-900 — Arquitetura e serviços do Azure
### 🌍 Regiões, zonas, datacenters e hierarquia de recursos

<h3><strong style='color: skyblue'>1️⃣ Regiões do Azure</strong></h3>

<p align="justify">Uma <strong>região do Azure</strong> é uma área geográfica do mundo que contém um ou mais datacenters conectados por uma rede de baixa latência.</p>

<p align="justify">Ao criar um recurso no Azure, normalmente você escolhe uma <strong>região</strong> onde esse recurso será hospedado.</p>

### Por que escolher uma região?

- Proximidade dos usuários → pode reduzir latência.
- Requisitos de residência/localização dos dados.
- Disponibilidade de determinados serviços.
- Requisitos de conformidade.
- Preços podem variar entre regiões.
- Estratégias de recuperação de desastre e continuidade.

> **AZ-900:** Região = localização geográfica onde os recursos do Azure são hospedados.

---

<h3><strong style='color: skyblue'>2️⃣ Pares de regiões (Region Pairs)</strong></h3>

<p align="justify">Algumas regiões do Azure são agrupadas em <strong>pares de regiões</strong>. Essas regiões ficam relativamente próximas dentro da mesma área geográfica e são usadas para ajudar em estratégias de continuidade e recuperação.</p>

<p align="justify">Os pares também ajudam a Azure a coordenar determinadas atualizações da plataforma, evitando que regiões emparelhadas sejam atualizadas simultaneamente em algumas situações.</p>

### Exemplo conceitual

<pre>
Região A ─────────────── Região B
  │                         │
  └──── Region Pair ────────┘
       ↑
       Redundância / recuperação
</pre>

> **PEGADINHA AZ-900:** Region Pair ≠ Availability Zone.

- **Region Pair** → duas regiões geográficas diferentes.
- **Availability Zone** → zonas fisicamente separadas dentro de uma mesma região.

---

<h3><strong style='color: skyblue'>3️⃣ Regiões soberanas do Azure</strong></h3>

<p align="justify">As <strong>regiões soberanas</strong> são ambientes separados das regiões públicas do Azure, destinados a atender requisitos específicos de governos e órgãos públicos.</p>

<p align="justify">Exemplos conhecidos incluem:</p>

- <strong>Azure Government</strong> → ambientes para organizações governamentais dos Estados Unidos.
- <strong>Azure China</strong> → regiões operadas separadamente na China.

<p align="justify">Esses ambientes possuem requisitos específicos de conformidade, residência de dados e operação.</p>

> **DECORA:** Regiões soberanas = ambientes separados para requisitos específicos de governo/regulamentação.

---

<h3><strong style='color: skyblue'>4️⃣ Zonas de disponibilidade (Availability Zones)</strong></h3>

<p align="justify">As <strong>Availability Zones</strong> são locais físicos distintos dentro de uma região do Azure.</p>

<p align="justify">Cada zona possui infraestrutura independente de energia, refrigeração e rede. As zonas são conectadas por uma rede de alta velocidade e baixa latência.</p>

### Exemplo

<pre>
                 REGIÃO AZURE
                      │
       ┌──────────────┼──────────────┐
       │              │              │
   Zona 1          Zona 2          Zona 3
       │              │              │
   Datacenter      Datacenter      Datacenter
   independente   independente   independente
</pre>

<p align="justify">Se uma zona apresentar uma falha, workloads distribuídos em outras zonas podem continuar funcionando.</p>

> **AZ-900:** Availability Zone = proteção contra falha de datacenter dentro de uma região.

### Region x Availability Zone

| Conceito | O que é? |
|---|---|
| **Região** | Área geográfica |
| **Availability Zone** | Local físico isolado dentro de uma região |
| **Region Pair** | Duas regiões emparelhadas |
| **Região soberana** | Ambiente separado para requisitos específicos |

> **PEGADINHA:** Zonas de disponibilidade não são regiões diferentes.

---

<h3><strong style='color: skyblue'>5️⃣ Datacenters do Azure</strong></h3>

<p align="justify">Um <strong>datacenter</strong> é uma instalação física que contém servidores, armazenamento, redes, energia, refrigeração e outros componentes necessários para executar os serviços de nuvem.</p>

<p align="justify">Os datacenters do Azure são agrupados fisicamente para formar regiões e, quando aplicável, Availability Zones.</p>

### Hierarquia simplificada

<pre>
MUNDO
  │
  └── Região do Azure
         │
         ├── Availability Zone 1
         │      └── Datacenter(s)
         │
         ├── Availability Zone 2
         │      └── Datacenter(s)
         │
         └── Availability Zone 3
                └── Datacenter(s)
</pre>

> **DECORA:** Datacenter = infraestrutura física.  
> **Zona = isolamento físico dentro da região.**  
> **Região = localização geográfica.**

---

<h3><strong style='color: skyblue'>6️⃣ Recursos do Azure</strong></h3>

<p align="justify">Um <strong>recurso</strong> é uma instância de um serviço do Azure que você cria e gerencia.</p>

### Exemplos

- Máquina virtual
- Conta de armazenamento
- Banco de dados
- Rede virtual
- Interface de rede
- IP público
- App Service
- Key Vault

<p align="justify">Cada recurso possui propriedades, configurações e permissões próprias.</p>

> **AZ-900:** Recurso = algo que você cria/usa no Azure.

---

<h3><strong style='color: skyblue'>7️⃣ Grupos de recursos (Resource Groups)</strong></h3>

<p align="justify">Um <strong>Resource Group</strong> é um contêiner lógico utilizado para organizar e gerenciar recursos do Azure.</p>

### Exemplo

<pre>
Resource Group: RG-SISTEMA-VENDAS
        │
        ├── VM
        ├── Storage Account
        ├── Network Interface
        ├── Public IP
        └── Key Vault
</pre>

<p align="justify">Os recursos dentro de um grupo geralmente pertencem à mesma solução ou ciclo de vida.</p>

### Características importantes

- Um recurso pertence a <strong>um único Resource Group</strong>.
- Um Resource Group pertence a <strong>uma única assinatura</strong>.
- Recursos de regiões diferentes podem, em muitos casos, estar no mesmo Resource Group.
- O Resource Group possui uma região para seus metadados.
- É possível aplicar RBAC, políticas e tags no nível do Resource Group.

> **PEGADINHA:** Resource Group não é um datacenter e não limita necessariamente todos os recursos à mesma região.

---

<h3><strong style='color: skyblue'>8️⃣ Assinaturas (Subscriptions)</strong></h3>

<p align="justify">Uma <strong>Subscription</strong> é uma unidade lógica e administrativa dentro do Azure que fornece um limite para gerenciamento, cobrança e controle de acesso.</p>

### Uma assinatura pode conter:

<pre>
Subscription
    │
    ├── Resource Group A
    │      ├── VM
    │      └── Storage
    │
    ├── Resource Group B
    │      ├── VNet
    │      └── Database
    │
    └── Resource Group C
           └── App Service
</pre>

### Para que serve uma assinatura?

- Gerenciamento de recursos.
- Cobrança.
- Controle de acesso.
- Limites e quotas.
- Separação de ambientes/projetos.

<p align="justify">Uma organização pode ter várias assinaturas para separar, por exemplo, ambientes, departamentos ou projetos.</p>

> **DECORA:** Subscription = limite de cobrança + gerenciamento + acesso.

---

<h3><strong style='color: skyblue'>9️⃣ Grupos de gerenciamento (Management Groups)</strong></h3>

<p align="justify">Os <strong>Management Groups</strong> permitem organizar e gerenciar várias assinaturas em uma estrutura hierárquica.</p>

<p align="justify">Eles são especialmente úteis para aplicar políticas e controles de governança em várias assinaturas.</p>

### Exemplo

<pre>
Management Group
       │
       ├── Subscription A
       │
       ├── Subscription B
       │
       └── Subscription C
</pre>

<p align="justify">Uma política aplicada em um Management Group pode ser herdada pelas assinaturas e recursos abaixo dele, dependendo da configuração.</p>

> **AZ-900:** Management Group = agrupa e governa várias subscriptions.

---

<h3><strong style='color: skyblue'>🔟 Hierarquia do Azure</strong></h3>

<p align="justify">A hierarquia administrativa do Azure é fundamental para entender onde políticas, permissões e recursos podem ser aplicados.</p>

### Estrutura

<pre>
Tenant / Microsoft Entra ID
          │
          ▼
  Management Group
          │
          ├───────────────┐
          ▼               ▼
   Subscription A   Subscription B
          │               │
          ▼               ▼
   Resource Group    Resource Group
          │               │
          ▼               ▼
       Resources        Resources
</pre>

### Hierarquia principal para memorizar

<pre>
Management Group
       ↓
Subscription
       ↓
Resource Group
       ↓
Resource
</pre>

> **DECORA AZ-900:**  
> **Management Group → Subscription → Resource Group → Resource**

---

<h3><strong style='color: skyblue'>1️⃣1️⃣ Como diferenciar tudo na prova</strong></h3>

| Conceito | Pense em... | Função principal |
|---|---|---|
| **Região** | 🌍 Localização | Onde os recursos são hospedados |
| **Region Pair** | 🔗 Regiões | Continuidade/recuperação |
| **Availability Zone** | 🏢 Zona física | Resiliência dentro da região |
| **Datacenter** | 🖥️ Infraestrutura física | Servidores e infraestrutura |
| **Resource** | ⚙️ Serviço | Instância de um serviço |
| **Resource Group** | 📦 Pasta | Agrupar recursos |
| **Subscription** | 💳 Conta administrativa | Cobrança + gerenciamento |
| **Management Group** | 🗂️ Pasta de subscriptions | Governança em escala |

---

<h3><strong style='color: skyblue'>🧠 Mapa mental para decorar</strong></h3>

<pre>
                    AZURE
                      │
        ┌─────────────┴─────────────┐
        │                           │
   INFRAESTRUTURA               HIERARQUIA
        │                           │
        ├── Região                  ├── Management Group
        │     │                     │
        │     ├── Zone 1            ├── Subscription
        │     ├── Zone 2            │
        │     └── Zone 3            ├── Resource Group
        │                           │
        └── Datacenters             └── Resource
                      
REGIÃO
  └── localização geográfica

AVAILABILITY ZONE
  └── isolamento físico dentro da região

REGION PAIR
  └── região ↔ região

RESOURCE
  └── serviço/instância

RESOURCE GROUP
  └── agrupa recursos

SUBSCRIPTION
  └── cobrança + gerenciamento

MANAGEMENT GROUP
  └── agrupa subscriptions
</pre>

<h3><strong style='color: skyblue'>🎯 Resumo para a prova</strong></h3>

| Se a questão falar de... | Resposta provável |
|---|---|
| Localização geográfica | **Region** |
| Datacenters isolados dentro de uma região | **Availability Zones** |
| Continuidade entre regiões | **Region Pairs** |
| Infraestrutura física | **Datacenter** |
| Instância de um serviço | **Resource** |
| Agrupar recursos de uma solução | **Resource Group** |
| Cobrança e limite administrativo | **Subscription** |
| Governança de várias subscriptions | **Management Group** |
| Estrutura administrativa | **Management Group → Subscription → Resource Group → Resource** |

> **🔥 DECORAÇÃO FINAL:**  
> 🌍 **Região** = onde  
> 🏢 **Zona** = isolamento físico  
> 🖥️ **Datacenter** = infraestrutura física  
> ⚙️ **Recurso** = o que você cria  
> 📦 **Resource Group** = agrupa recursos  
> 💳 **Subscription** = cobrança/limite administrativo  
> 🗂️ **Management Group** = agrupa subscriptions  
> 🔗 **Region Pair** = duas regiões para resiliência
