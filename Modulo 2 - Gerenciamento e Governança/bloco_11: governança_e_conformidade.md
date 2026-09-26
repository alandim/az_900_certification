## 🔐 Governança e conformidade no Azure

<h3><strong style='color: skyblue'>1️⃣ Microsoft Purview</strong></h3>

<p align="justify">O <strong>Microsoft Purview</strong> ajuda as organizações a <strong>descobrir, catalogar, classificar e governar dados</strong>. Ele fornece visibilidade sobre onde os dados estão, que tipo de dados existem e como eles são utilizados.</p>

### 🎯 Para que serve?

- Descobrir e catalogar dados em diferentes fontes.
- Classificar dados conforme seu tipo e sensibilidade.
- Identificar informações sensíveis.
- Criar uma visão do patrimônio de dados da organização.
- Ajudar na governança e conformidade dos dados.
- Rastrear a origem e movimentação dos dados (**data lineage**).

> **AZ-900:** Purview está relacionado principalmente a **dados, governança, descoberta, classificação e conformidade**.

### 🧠 Exemplo

Imagine uma empresa com dados espalhados em:

- Azure SQL
- Storage Account
- bancos de dados locais
- Microsoft 365
- outras fontes

O Purview ajuda a responder:

> **"Onde estão nossos dados? Que tipo de dados temos? Existem dados sensíveis? De onde esses dados vieram?"**

### ⚠️ PEGADINHA AZ-900

**Purview ≠ Azure Policy**

| Serviço | Foco |
|---|---|
| **Microsoft Purview** | Governança e descoberta/classificação de **dados** |
| **Azure Policy** | Aplicar **regras e padrões** aos recursos |
| **Resource Locks** | Impedir **alterações ou exclusões** |

> **DECORA:**  
> **Purview → Dados**  
> **Policy → Regras**  
> **Locks → Proteção contra alterações/exclusões**

---

<h3><strong style='color: skyblue'>2️⃣ Azure Policy</strong></h3>

<p align="justify">O <strong>Azure Policy</strong> permite criar e aplicar <strong>regras</strong> para garantir que os recursos do Azure estejam em conformidade com determinados padrões.</p>

### 🎯 Para que serve?

- Impor padrões organizacionais.
- Garantir conformidade.
- Avaliar recursos existentes e novos.
- Impedir determinadas configurações.
- Auditar configurações.
- Corrigir automaticamente determinadas configurações, quando a política permitir.

### 🧠 Exemplos

Uma organização pode criar uma Policy dizendo:

- ❌ Não permitir recursos fora da região `Brazil South`.
- ❌ Não permitir Storage Accounts sem determinado tipo de configuração.
- ❌ Exigir uma determinada tag.
- ❌ Permitir somente determinados tipos de máquinas virtuais.
- 🔎 Auditar recursos que não estejam em conformidade.

### ⚙️ Efeitos comuns de uma Policy

| Efeito | O que faz |
|---|---|
| **Audit** | Apenas identifica recursos fora da regra |
| **Deny** | Impede a criação/alteração que viole a regra |
| **Modify** | Pode alterar/adicionar configurações |
| **DeployIfNotExists** | Pode implantar uma configuração quando ela estiver ausente |

> **AZ-900:** Se a questão falar em **"garantir que todos os recursos sigam determinada regra/padrão"**, pense em **Azure Policy**.

### ⚠️ PEGADINHA

**Azure Policy não é o mesmo que Resource Lock.**

Exemplo:

- Policy: **"Não permita criar recursos nessa região."**
- Lock: **"Mesmo que alguém tenha permissão, não deixe excluir este recurso."**

---

<h3><strong style='color: skyblue'>3️⃣ Resource Locks — Bloqueios de recursos</strong></h3>

<p align="justify">Os <strong>Resource Locks</strong> protegem recursos do Azure contra <strong>exclusão acidental ou alterações indesejadas</strong>.</p>

Existem dois tipos principais:

### 🔒 ReadOnly

Impede alterações no recurso.

- Permite leitura.
- Impede modificações.
- Também pode impedir determinadas operações que exigiriam alteração.

### 🗑️ CanNotDelete

Impede a exclusão do recurso.

- O recurso continua podendo ser utilizado e alterado.
- ❌ Não pode ser excluído enquanto o bloqueio existir.

| Lock | Ler | Alterar | Excluir |
|---|:---:|:---:|:---:|
| **CanNotDelete** | ✅ | ✅ | ❌ |
| **ReadOnly** | ✅ | ❌ | ❌ |

> **AZ-900:** Resource Lock protege contra **alteração/exclusão**, independentemente de quem tenha a intenção de realizar a operação.

### 🧠 Exemplo

Você possui uma Storage Account crítica:

```text
Storage Account
      │
      └── 🔒 CanNotDelete
              │
              └── Evita exclusão acidental
```

Mesmo que alguém tente excluir o recurso, o bloqueio impede a operação enquanto estiver aplicado.

---

<h3><strong style='color: skyblue'>4️⃣ Comparação para a prova</strong></h3>

| Recurso | Finalidade principal | Palavra-chave |
|---|---|---|
| **Microsoft Purview** | Descobrir, catalogar, classificar e governar dados | 🗃️ **Dados** |
| **Azure Policy** | Definir e aplicar regras de conformidade | 📏 **Regras** |
| **Resource Locks** | Evitar alterações/exclusões | 🔒 **Proteção** |

### 🧩 MAPA MENTAL

<pre>
                    GOVERNANÇA AZURE
                          │
          ┌───────────────┼────────────────┐
          │               │                │
      PURVIEW          POLICY             LOCKS
          │               │                │
        DADOS           REGRAS          PROTEÇÃO
          │               │                │
    ┌─────┴─────┐    ┌────┴────┐     ┌────┴────┐
    │           │    │         │     │         │
 Catalogar  Classificar Audit  Deny  ReadOnly  CanNotDelete
    │           │    │         │     │         │
    └──────┬────┘    └────┬────┘     └────┬────┘
           │               │               │
       Governança      Conformidade    Evitar ações
        de dados       e padrões       indesejadas
</pre>

### 🔥 DECORAÇÃO FINAL

> **PURVIEW → "Que dados temos e como são governados?"**

> **POLICY → "Quais regras os recursos devem seguir?"**

> **LOCK → "Não deixe alguém alterar/excluir este recurso."**

### 🎯 PEGADINHAS AZ-900

- **Classificação de dados sensíveis → Purview**
- **Catálogo de dados → Purview**
- **Data lineage → Purview**
- **Exigir uma tag em recursos → Azure Policy**
- **Impedir criação de recurso fora de determinada região → Azure Policy**
- **Auditar recursos fora de um padrão → Azure Policy**
- **Impedir exclusão de um recurso → Resource Lock**
- **Impedir alterações em um recurso → ReadOnly Lock**
- **Proteger recurso crítico contra exclusão acidental → `CanNotDelete`**

> 🧠 **Regra de 3 segundos:**  
> **DADOS = Purview | REGRAS = Policy | BLOQUEAR = Locks**
