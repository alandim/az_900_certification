## Controle de acesso e autorização no Azure

<p align="justify">O Azure possui diferentes mecanismos para controlar o acesso aos recursos. Para o AZ-900, é importante diferenciar o <strong>Microsoft Entra Conditional Access</strong>, que controla <strong>quando e em quais condições uma identidade pode acessar</strong>, do <strong>Azure RBAC</strong>, que controla <strong>quais ações uma identidade pode realizar em um recurso</strong>.</p>

---

<h3><strong style='color: skyblue'>Acesso Condicional do Microsoft Entra</strong></h3>

<p align="justify">O <strong>Microsoft Entra Conditional Access (Acesso Condicional)</strong> permite criar políticas que analisam determinadas condições durante uma tentativa de acesso e aplicam controles de acesso de acordo com essas condições.</p>

<p align="justify">Ele funciona como um mecanismo de <strong>política</strong>: dependendo do contexto da solicitação, o acesso pode ser permitido, bloqueado ou exigir controles adicionais.</p>

<pre>
Usuário
   │
   ▼
Tentativa de acesso
   │
   ├── Quem é?
   ├── De onde está acessando?
   ├── Qual dispositivo?
   ├── Qual aplicação?
   └── Qual o contexto?
          │
          ▼
   Acesso Condicional
          │
     ┌────┴────┐
     ▼         ▼
 Permitir    Bloquear
     │
     ▼
Exigir MFA / outros controles
</pre>

---

### Sinais utilizados pelo Acesso Condicional

<p align="justify">As políticas podem considerar diferentes sinais relacionados à tentativa de acesso.</p>

**Exemplos:**

- Usuário ou grupo.
- Aplicação ou recurso.
- Localização.
- Informações do dispositivo.
- Risco de entrada.
- Risco do usuário.
- Tipo de autenticação.
- Plataforma utilizada.

<p align="justify">Com base nesses sinais, uma política pode determinar o controle que deverá ser aplicado.</p>

---

### Controles de acesso

<p align="justify">Uma política de Acesso Condicional pode aplicar diferentes controles.</p>

**Exemplos:**

- Exigir MFA.
- Bloquear o acesso.
- Exigir que o dispositivo esteja em conformidade.
- Exigir autenticação apropriada.
- Conceder acesso somente quando determinadas condições forem atendidas.

**Exemplo:**

<pre>
Usuário tenta acessar aplicação
            │
            ▼
    Está fora da rede
            │
            ▼
     Acesso Condicional
            │
            ▼
       Exigir MFA
            │
            ▼
      Usuário confirma
            │
            ▼
          Acesso
</pre>

> **AZ-900:** Acesso Condicional → **avalia condições/contexto e aplica uma política de acesso**.

---

### Acesso Condicional x MFA

<p align="justify">O <strong>MFA</strong> é um método/controle de autenticação. O <strong>Acesso Condicional</strong> pode utilizar o MFA como uma das condições ou ações de uma política.</p>

<pre>
Acesso Condicional
       │
       ├── Bloquear acesso
       │
       ├── Permitir acesso
       │
       └── Exigir MFA
                │
                ▼
               MFA
</pre>

> **PEGADINHA AZ-900:** Acesso Condicional **não é sinônimo de MFA**. Uma política de Acesso Condicional pode **exigir MFA** dependendo das condições.

---

<h3><strong style='color: skyblue'>Exemplo de política de Acesso Condicional</strong></h3>

<p align="justify">Imagine uma organização que deseja exigir MFA quando funcionários acessarem uma aplicação corporativa fora de uma localização confiável.</p>

<pre>
CONDIÇÕES

Usuário: Funcionários
Aplicação: Aplicação corporativa
Localização: Fora de localização confiável

              │
              ▼

AÇÃO

Exigir MFA

              │
              ▼

Resultado:

Usuário realiza MFA
        ↓
Acesso concedido
</pre>

<p align="justify">A política não precisa simplesmente dizer "todos devem usar MFA". Ela pode aplicar o requisito de acordo com o <strong>contexto da tentativa de acesso</strong>.</p>

---

<h3><strong style='color: skyblue'>Azure RBAC</strong></h3>

<p align="justify">O <strong>Azure RBAC (Role-Based Access Control)</strong> é o sistema de autorização utilizado para controlar o que uma identidade pode fazer nos recursos do Azure.</p>

<p align="justify">Em vez de conceder permissões individualmente para cada ação, o Azure RBAC utiliza <strong>funções (roles)</strong> que possuem conjuntos de permissões.</p>

<p align="justify">Uma identidade recebe uma função em determinado <strong>escopo</strong>.</p>

<pre>
Identidade
    │
    ▼
Função (Role)
    │
    ▼
Permissões
    │
    ▼
Escopo
    │
    ▼
Recurso Azure
</pre>

---

### Componentes do Azure RBAC

<p align="justify">Uma atribuição de função do Azure RBAC envolve principalmente três elementos:</p>

### 1. Security Principal

<p align="justify">É a identidade que recebe a permissão.</p>

**Pode ser:**

- Usuário.
- Grupo.
- Service principal.
- Managed identity.

### 2. Role Definition

<p align="justify">Define quais ações podem ser realizadas.</p>

**Exemplos:**

- Ler recursos.
- Criar recursos.
- Alterar recursos.
- Excluir recursos.

### 3. Scope

<p align="justify">Define <strong>onde</strong> a permissão se aplica.</p>

**Possíveis escopos:**

- Management group.
- Subscription.
- Resource group.
- Recurso individual.

<pre>
Management Group
       │
       ▼
Subscription
       │
       ▼
Resource Group
       │
       ▼
Resource
</pre>

> **AZ-900:** RBAC = **quem + qual função + em qual escopo**.

---

<h3><strong style='color: skyblue'>Funções comuns do Azure RBAC</strong></h3>

### Owner

<p align="justify">A função <strong>Owner</strong> possui acesso amplo aos recursos dentro do escopo e também pode gerenciar atribuições de acesso.</p>

> **Owner → pode gerenciar recursos + acesso.**

---

### Contributor

<p align="justify">A função <strong>Contributor</strong> pode criar e gerenciar recursos, mas não pode gerenciar atribuições de acesso do Azure RBAC.</p>

> **Contributor → gerencia recursos, mas não concede acesso via RBAC.**

---

### Reader

<p align="justify">A função <strong>Reader</strong> permite visualizar recursos, mas não permite fazer alterações.</p>

> **Reader → somente leitura.**

---

### Comparação

| Função | Visualizar | Gerenciar recursos | Gerenciar acesso |
|---|:---:|:---:|:---:|
| **Reader** | ✓ | ✗ | ✗ |
| **Contributor** | ✓ | ✓ | ✗ |
| **Owner** | ✓ | ✓ | ✓ |

> **PEGADINHA AZ-900:**  
> **Contributor ≠ Owner**.  
> Contributor pode gerenciar recursos, mas **não pode gerenciar atribuições de acesso**.

---

<h3><strong style='color: skyblue'>Escopo do Azure RBAC</strong></h3>

<p align="justify">As permissões podem ser atribuídas em diferentes níveis. Uma permissão atribuída em um escopo superior pode ser herdada por escopos inferiores.</p>

<pre>
Management Group
       │
       └── Subscription
              │
              └── Resource Group
                     │
                     ├── VM
                     ├── Storage Account
                     └── Database
</pre>

<p align="justify">Por exemplo, uma função atribuída no nível da <strong>Subscription</strong> pode fornecer acesso aos recursos existentes dentro dessa assinatura, conforme a função e o escopo da atribuição.</p>

> **AZ-900:** Quanto mais alto o escopo, maior pode ser o conjunto de recursos afetados pela atribuição.

---

<h3><strong style='color: skyblue'>RBAC x Acesso Condicional</strong></h3>

<p align="justify">Os dois mecanismos tratam de controle de acesso, mas atuam em problemas diferentes.</p>

| Recurso | Pergunta principal |
|---|---|
| **Acesso Condicional** | Em quais condições o acesso pode acontecer? |
| **Azure RBAC** | O que essa identidade pode fazer no recurso? |

**Exemplo:**

<pre>
Usuário tenta acessar Azure
          │
          ▼
Acesso Condicional
"Precisa fazer MFA?"
          │
          ▼
Autenticação / MFA
          │
          ▼
Azure RBAC
"Qual permissão esse usuário possui?"
          │
          ▼
Reader / Contributor / Owner
          │
          ▼
Ação permitida ou negada
</pre>

> **DECORA:**
>
> **Conditional Access → condições de acesso**
>
> **RBAC → permissões sobre recursos**

---

<h3><strong style='color: skyblue'>RBAC x Microsoft Entra ID</strong></h3>

<p align="justify">O <strong>Microsoft Entra ID</strong> gerencia identidades e autenticação, enquanto o <strong>Azure RBAC</strong> fornece autorização granular para recursos do Azure.</p>

<pre>
Microsoft Entra ID
       │
       ├── Quem é o usuário?
       ├── Autenticação
       └── Identidade
              │
              ▼
          Azure RBAC
              │
              ├── O que pode fazer?
              └── Em qual recurso?
</pre>

> **AZ-900:**  
> **Entra ID → identidade/autenticação**  
> **RBAC → autorização/permissões**

---

<h3><strong style='color: skyblue'>Mapa mental</strong></h3>

<pre>
CONTROLE DE ACESSO AZURE
│
├── Microsoft Entra
│   │
│   ├── Identidade
│   ├── Autenticação
│   │
│   └── Acesso Condicional
│       ├── Usuário
│       ├── Aplicação
│       ├── Localização
│       ├── Dispositivo
│       ├── Risco
│       │
│       └── Controles
│           ├── Permitir
│           ├── Bloquear
│           └── Exigir MFA
│
└── Azure RBAC
    │
    ├── Quem?
    │   └── Usuário / Grupo / Service Principal / Managed Identity
    │
    ├── O quê?
    │   └── Role
    │
    └── Onde?
        ├── Management Group
        ├── Subscription
        ├── Resource Group
        └── Resource
</pre>

---

<h3><strong style='color: skyblue'>Resumo para a prova AZ-900</strong></h3>

| Se a questão falar sobre... | Pense em... |
|---|---|
| Condições para permitir ou bloquear acesso | **Conditional Access** |
| Exigir MFA dependendo do contexto | **Conditional Access** |
| Localização do usuário | **Conditional Access** |
| Estado do dispositivo | **Conditional Access** |
| Risco de login | **Conditional Access** |
| Controlar o que um usuário pode fazer | **Azure RBAC** |
| Permissões sobre recursos Azure | **Azure RBAC** |
| Somente visualizar recursos | **Reader** |
| Criar e gerenciar recursos, sem gerenciar acesso | **Contributor** |
| Gerenciar recursos e atribuições de acesso | **Owner** |
| Aplicar permissão a uma Subscription | **RBAC Scope** |
| Aplicar permissão a um Resource Group | **RBAC Scope** |
| Aplicar permissão a um recurso específico | **RBAC Scope** |

> **🔥 DECORAÇÃO FINAL AZ-900**
>
> **Conditional Access → "EM QUAIS CONDIÇÕES entra?"**
>
> **RBAC → "O QUE pode fazer?"**
>
> **Reader → vê**
>
> **Contributor → modifica**
>
> **Owner → modifica + gerencia acesso**
>
> **Entra ID → quem é**
>
> **Conditional Access → em quais condições entra**
>
> **RBAC → o que pode fazer**
