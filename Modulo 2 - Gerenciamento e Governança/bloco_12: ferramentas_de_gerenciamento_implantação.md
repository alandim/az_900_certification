## 🛠️ Ferramentas de gerenciamento e infraestrutura do Azure

<h3><strong style='color: skyblue'>1️⃣ Portal do Azure</strong></h3>

<p align="justify">O <strong>Azure Portal</strong> é uma interface gráfica baseada na Web usada para <strong>criar, configurar, gerenciar, monitorar e excluir recursos do Azure</strong>.</p>

### 🎯 O que posso fazer pelo Portal?

- Criar máquinas virtuais.
- Criar Storage Accounts.
- Configurar redes.
- Gerenciar Resource Groups.
- Visualizar métricas e alertas.
- Gerenciar usuários e permissões.
- Configurar recursos sem utilizar comandos.

> **AZ-900:** Portal do Azure = **interface gráfica (GUI)** para administrar recursos Azure.

### 🧠 Decora

```text
AZURE PORTAL
     │
     ├── Interface gráfica
     ├── Criar recursos
     ├── Configurar recursos
     ├── Monitorar recursos
     └── Gerenciar ambiente
```

---

<h3><strong style='color: skyblue'>2️⃣ Azure Cloud Shell</strong></h3>

<p align="justify">O <strong>Azure Cloud Shell</strong> é um ambiente de linha de comando hospedado pela Microsoft, acessível pelo navegador, que permite executar comandos para administrar recursos do Azure.</p>

Ele pode ser acessado diretamente pelo Portal do Azure.

Possui dois principais ambientes:

- **Bash**
- **PowerShell**

### 🎯 Vantagem

Você não precisa instalar localmente todas as ferramentas necessárias para começar a executar comandos.

```text
Navegador
   │
   ▼
Azure Portal
   │
   ▼
Cloud Shell
   │
   ├── Bash
   └── PowerShell
```

> **AZ-900:** Cloud Shell = **terminal hospedado no Azure e acessível pelo navegador**.

---

<h3><strong style='color: skyblue'>3️⃣ Azure CLI</strong></h3>

<p align="justify">A <strong>Azure CLI</strong> é uma ferramenta de linha de comando usada para criar e gerenciar recursos do Azure por meio de comandos.</p>

É multiplataforma e pode ser executada em:

- Windows
- Linux
- macOS
- Cloud Shell

### 🧠 Exemplo

```bash
az group list
```

O comando `az` é característico da Azure CLI.

> **DECORA:**  
> **Azure CLI → comandos `az` → multiplataforma**

---

<h3><strong style='color: skyblue'>4️⃣ Azure PowerShell</strong></h3>

<p align="justify">O <strong>Azure PowerShell</strong> é um conjunto de módulos do PowerShell que permite administrar recursos do Azure usando comandos/cmdlets do PowerShell.</p>

### 🧠 Exemplo

```powershell
Get-AzResource
```

Os comandos normalmente começam com:

```text
Get-Az...
New-Az...
Set-Az...
Remove-Az...
```

### ⚔️ CLI × PowerShell

| Ferramenta | Característica |
|---|---|
| **Azure CLI** | Comandos `az` |
| **Azure PowerShell** | Cmdlets `Az` |
| **Cloud Shell** | Ambiente de execução no navegador |
| **Portal** | Interface gráfica |

> **PEGADINHA:** Cloud Shell **não é concorrente** da CLI/PowerShell. Ele é um **ambiente** onde você pode utilizar Bash/Azure CLI ou PowerShell.

---

<h3><strong style='color: skyblue'>5️⃣ Azure Arc</strong></h3>

<p align="justify">O <strong>Azure Arc</strong> permite estender os recursos de gerenciamento do Azure para recursos que estão <strong>fora do Azure</strong>.</p>

Isso inclui ambientes:

- On-premises
- Outras nuvens
- Ambientes híbridos
- Servidores físicos
- Máquinas virtuais
- Clusters Kubernetes

### 🧠 Ideia principal

```text
                    AZURE
                      │
              Azure Arc
                      │
        ┌─────────────┼─────────────┐
        │             │             │
    On-premises   AWS/Outra      Kubernetes
      Server        Cloud          Cluster
```

Você pode usar recursos de gerenciamento e governança do Azure para recursos que não estão hospedados diretamente no Azure.

> **AZ-900:** Azure Arc = **gerenciar recursos fora do Azure como parte do ambiente Azure**.

### ⚠️ PEGADINHA

Azure Arc **não significa simplesmente "mover o servidor para o Azure"**.

A ideia principal é **estender o gerenciamento e os serviços do Azure para ambientes híbridos e multicloud**.

---

<h3><strong style='color: skyblue'>6️⃣ Infraestrutura como Código — IaC</strong></h3>

<p align="justify"><strong>Infrastructure as Code (IaC)</strong> é a prática de definir a infraestrutura por meio de <strong>código ou arquivos de configuração</strong>, em vez de configurar tudo manualmente.</p>

### ❌ Sem IaC

```text
Portal
  ↓
Criar recurso
  ↓
Configurar
  ↓
Repetir manualmente
  ↓
Outro ambiente
```

Problemas:

- Mais trabalho manual.
- Maior possibilidade de erro.
- Difícil reproduzir exatamente o mesmo ambiente.
- Mais difícil controlar alterações.

### ✅ Com IaC

```text
Código / Template
       ↓
Automação
       ↓
Infraestrutura
       ↓
Ambiente reproduzível
```

### 🎯 Benefícios

- Automação.
- Consistência.
- Repetibilidade.
- Versionamento.
- Menos configuração manual.
- Facilita criação de ambientes idênticos.

> **AZ-900:** IaC = **definir infraestrutura através de código/configuração para automatizar e reproduzir ambientes**.

---

<h3><strong style='color: skyblue'>7️⃣ ARM — Azure Resource Manager</strong></h3>

<p align="justify">O <strong>Azure Resource Manager (ARM)</strong> é a camada de gerenciamento do Azure responsável por fornecer uma forma consistente de <strong>criar, atualizar, organizar, controlar e excluir recursos</strong>.</p>

Ele fica entre as ferramentas utilizadas pelo administrador e os recursos do Azure.

```text
Portal
Azure CLI
PowerShell
Templates
    │
    ▼
┌─────────────────────┐
│ Azure Resource      │
│ Manager (ARM)       │
└─────────────────────┘
    │
    ▼
Recursos Azure
```

### 🎯 O ARM permite:

- Criar recursos.
- Atualizar recursos.
- Excluir recursos.
- Organizar recursos em Resource Groups.
- Aplicar controle de acesso (RBAC).
- Aplicar tags.
- Trabalhar com templates.
- Gerenciar recursos de forma consistente.

> **DECORA:**  
> **ARM = camada de gerenciamento dos recursos Azure.**

---

<h3><strong style='color: skyblue'>8️⃣ Modelos do ARM — ARM Templates</strong></h3>

<p align="justify">Os <strong>ARM Templates</strong> são arquivos JSON que descrevem a infraestrutura e os recursos que devem ser implantados no Azure.</p>

Eles são uma forma de implementar **Infrastructure as Code (IaC)**.

### 🧠 Exemplo conceitual

Em vez de fazer manualmente:

```text
Criar Resource Group
        ↓
Criar Storage Account
        ↓
Configurar propriedades
        ↓
Criar rede
        ↓
Configurar permissões
```

Você pode definir a infraestrutura em um template:

```text
ARM Template
     │
     ▼
ARM
     │
     ▼
Implantação dos recursos
```

### 🎯 Benefícios

- Implantação repetível.
- Infraestrutura padronizada.
- Automação.
- Versionamento do código.
- Menos erros manuais.
- Facilita replicar ambientes.

> **AZ-900:** ARM Template = **arquivo JSON que descreve os recursos/configurações desejados para uma implantação Azure**.

---

<h3><strong style='color: skyblue'>9️⃣ ARM × ARM Template × IaC</strong></h3>

Essa diferença pode aparecer bastante em questões conceituais:

| Conceito | O que é? |
|---|---|
| **IaC** | Conceito/prática de definir infraestrutura através de código |
| **ARM** | Camada de gerenciamento e implantação de recursos do Azure |
| **ARM Template** | Template JSON usado para definir infraestrutura Azure |
| **Portal** | Interface gráfica para administrar Azure |
| **Azure CLI** | Ferramenta de linha de comando |
| **Azure PowerShell** | Ferramenta baseada em PowerShell |
| **Cloud Shell** | Ambiente de terminal hospedado no Azure |
| **Azure Arc** | Gerenciamento de recursos fora do Azure |

---

<h3><strong style='color: skyblue'>🔟 Mapa mental para a prova</strong></h3>

<pre>
             GERENCIAMENTO DO AZURE
                       │
       ┌───────────────┼────────────────┐
       │               │                │
     GUI             CLI             POWERHELL
       │               │                │
    Portal          Azure CLI       Azure PowerShell
                       │
                       │
                 Cloud Shell
                  /          \
               Bash       PowerShell
                       │
                       ▼
                      ARM
                       │
          ┌────────────┼────────────┐
          │            │            │
       Recursos     RBAC         Templates
                                    │
                                    ▼
                               ARM Template
                                    │
                                    ▼
                                   IaC
                                    │
                             Infraestrutura
                              automatizada
                                   
              ─────────────────────────
                       │
                       ▼
                   Azure Arc
                       │
          Recursos FORA do Azure
          ├── On-premises
          ├── Outras nuvens
          └── Kubernetes
</pre>

<h3><strong style='color: skyblue'>🔥 DECORAÇÃO FINAL</strong></h3>

> **Portal → GUI**

> **Cloud Shell → terminal no navegador**

> **Azure CLI → comandos `az`**

> **Azure PowerShell → cmdlets `Az`**

> **Azure Arc → gerenciar recursos fora do Azure**

> **IaC → infraestrutura definida por código**

> **ARM → gerenciamento dos recursos Azure**

> **ARM Template → JSON que descreve a infraestrutura**

### 🎯 PEGADINHAS AZ-900

- Quer **interface gráfica**? → **Portal**
- Quer **terminal no navegador**? → **Cloud Shell**
- Viu comando `az`? → **Azure CLI**
- Viu `Get-AzResource`? → **Azure PowerShell**
- Recursos estão **on-premises ou em outra nuvem**, mas você quer gerenciá-los pelo Azure? → **Azure Arc**
- Quer **automatizar e reproduzir infraestrutura**? → **IaC**
- Quer saber qual é a **camada de gerenciamento** dos recursos? → **ARM**
- Quer um **arquivo JSON que define recursos para implantação**? → **ARM Template**

> 🧠 **REGRA DE 5 SEGUNDOS:**  
> **PORTAL = GUI | CLI = `az` | POWERSHELL = `Az` | ARC = FORA DO AZURE | IaC = CÓDIGO | ARM = GERENCIAMENTO | TEMPLATE = JSON**
