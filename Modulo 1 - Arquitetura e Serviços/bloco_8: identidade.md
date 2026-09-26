## Serviços de identidade do Azure

<p align="justify">O <strong>Microsoft Entra ID</strong> é o serviço de gerenciamento de identidades e acesso baseado em nuvem da Microsoft. Ele permite controlar quem pode acessar recursos, aplicações e serviços, além de fornecer recursos de autenticação e autorização.</p>

<p align="justify">Para o AZ-900, é importante diferenciar o <strong>Microsoft Entra ID</strong> do <strong>Microsoft Entra Domain Services</strong>, entender os principais métodos de autenticação e saber como funcionam as identidades externas.</p>

---

<h3><strong style='color: skyblue'>Microsoft Entra ID</strong></h3>

<p align="justify">O <strong>Microsoft Entra ID</strong>, anteriormente chamado de <strong>Azure Active Directory (Azure AD)</strong>, é o serviço de gerenciamento de identidades e acesso da Microsoft baseado em nuvem.</p>

<p align="justify">Ele permite gerenciar <strong>usuários, grupos, dispositivos, aplicações e acesso aos recursos</strong>.</p>

<p align="justify">O Entra ID é utilizado para autenticar usuários e controlar o acesso a aplicações e serviços, tanto da Microsoft quanto de terceiros.</p>

**Exemplos de uso:**

- Login no portal do Azure.
- Acesso ao Microsoft 365.
- Autenticação em aplicações corporativas.
- Controle de acesso baseado em identidade.
- SSO entre aplicações.
- MFA.
- Gerenciamento de usuários e grupos.

> **AZ-900:** Microsoft Entra ID → **identidade + autenticação + acesso na nuvem**.

---

### Microsoft Entra ID x Active Directory Domain Services

<p align="justify">O <strong>Microsoft Entra ID</strong> não é simplesmente uma versão em nuvem do Active Directory Domain Services tradicional.</p>

<p align="justify">O Active Directory Domain Services (AD DS) utiliza conceitos tradicionais de domínio, como <strong>controladores de domínio, LDAP, Kerberos, NTLM e Group Policy</strong>.</p>

<p align="justify">O Entra ID é baseado em identidade e autenticação para aplicações e serviços modernos de nuvem.</p>

| Característica | Microsoft Entra ID | Active Directory Domain Services |
|---|---|---|
| Ambiente principal | Nuvem | Tradicional/on-premises |
| Identidade | Usuários, grupos, dispositivos e aplicações | Usuários, computadores e recursos de domínio |
| LDAP tradicional | Não é o modelo principal | Sim |
| Kerberos/NTLM tradicional | Não é o modelo principal | Sim |
| Group Policy | Não | Sim |
| SSO para aplicações de nuvem | Sim | Não é sua função principal |

> **PEGADINHA AZ-900:** Entra ID **não é um controlador de domínio tradicional hospedado no Azure**.

---

<h3><strong style='color: skyblue'>Microsoft Entra Domain Services</strong></h3>

<p align="justify">O <strong>Microsoft Entra Domain Services</strong> fornece serviços de domínio gerenciados no Azure para aplicações que dependem de protocolos e recursos tradicionais de domínio.</p>

<p align="justify">Ele permite utilizar recursos como <strong>LDAP, Kerberos, NTLM e Group Policy</strong> sem que você precise implantar e administrar seus próprios controladores de domínio.</p>

<p align="justify">O serviço é útil principalmente quando uma aplicação antiga ou uma VM precisa de funcionalidades tradicionais de domínio.</p>

**Exemplo:**

<pre>
Aplicação legada
      │
      │ LDAP / Kerberos / NTLM
      ▼
Microsoft Entra Domain Services
      │
      ▼
Microsoft Entra ID
</pre>

<p align="justify">O Domain Services é sincronizado com o Microsoft Entra ID, mas não transforma o Entra ID em um domínio AD DS tradicional.</p>

> **AZ-900:** Entra Domain Services → **AD tradicional como serviço gerenciado**.

---

### Entra ID x Entra Domain Services

| Serviço | Principal finalidade |
|---|---|
| **Microsoft Entra ID** | Identidade e acesso para aplicações e serviços modernos |
| **Microsoft Entra Domain Services** | Suporte a aplicações que precisam de recursos tradicionais de domínio |

> **DECORA:**
>
> **Entra ID → identidade na nuvem**  
> **Entra Domain Services → domínio tradicional gerenciado**

---

<h3><strong style='color: skyblue'>Autenticação</strong></h3>

<p align="justify"><strong>Autenticação</strong> é o processo utilizado para verificar a identidade de uma pessoa ou entidade.</p>

<p align="justify">Depois da autenticação, o Azure pode utilizar mecanismos de <strong>autorização</strong> para determinar quais recursos a identidade pode acessar.</p>

<pre>
Usuário
   │
   │ Quem é você?
   ▼
Autenticação
   │
   ▼
Identidade confirmada
   │
   │ O que você pode acessar?
   ▼
Autorização
</pre>

> **AZ-900:** Autenticação = **verificar quem você é**.  
> Autorização = **determinar o que você pode acessar**.

---

<h3><strong style='color: skyblue'>SSO — Single Sign-On</strong></h3>

<p align="justify">O <strong>SSO (Single Sign-On)</strong>, ou logon único, permite que o usuário se autentique uma vez e utilize essa autenticação para acessar várias aplicações sem precisar inserir novamente suas credenciais em cada aplicação.</p>

**Exemplo:**

<pre>
Usuário
   │
   ▼
Login no Microsoft Entra ID
   │
   ├──► Microsoft 365
   ├──► Azure Portal
   ├──► Aplicação A
   └──► Aplicação B
</pre>

<p align="justify">O principal benefício do SSO é reduzir a quantidade de vezes que o usuário precisa realizar login.</p>

> **AZ-900:** SSO → **uma autenticação para acessar várias aplicações**.

---

<h3><strong style='color: skyblue'>MFA — Autenticação Multifator</strong></h3>

<p align="justify">A <strong>MFA (Multifactor Authentication)</strong> adiciona uma ou mais formas adicionais de verificação à autenticação.</p>

<p align="justify">A ideia é exigir fatores de autenticação diferentes para aumentar a segurança da conta.</p>

### Principais fatores

**Algo que você sabe**

- Senha.
- PIN.

**Algo que você possui**

- Celular.
- Aplicativo autenticador.
- Chave de segurança.

**Algo que você é**

- Impressão digital.
- Reconhecimento facial.

**Exemplo:**

<pre>
Senha
  +
Microsoft Authenticator
  ↓
Acesso
</pre>

<p align="justify">Mesmo que alguém descubra a senha, ainda poderá ser necessário fornecer o segundo fator.</p>

> **AZ-900:** MFA → **mais de um fator para autenticar**.

---

<h3><strong style='color: skyblue'>Acesso sem senha</strong></h3>

<p align="justify">A autenticação <strong>sem senha (passwordless)</strong> permite autenticar o usuário sem depender de uma senha tradicional.</p>

<p align="justify">O Microsoft Entra ID oferece diferentes métodos de autenticação sem senha, incluindo recursos como <strong>Microsoft Authenticator, Windows Hello for Business e chaves de segurança FIDO2</strong>.</p>

### Exemplos

**Microsoft Authenticator**

<p align="justify">O usuário pode aprovar uma solicitação de autenticação no aplicativo autenticador.</p>

**Windows Hello for Business**

<p align="justify">Permite autenticação utilizando mecanismos como PIN ou biometria associados ao dispositivo.</p>

**FIDO2**

<p align="justify">Utiliza chaves de segurança compatíveis com o padrão FIDO2 para autenticação.</p>

> **AZ-900:** Passwordless → **autenticação sem senha tradicional**.

---

<h3><strong style='color: skyblue'>SSO x MFA x Passwordless</strong></h3>

| Recurso | O que resolve? | Ideia principal |
|---|---|---|
| **SSO** | Reduz múltiplos logins | Uma autenticação → várias aplicações |
| **MFA** | Aumenta a segurança da autenticação | Dois ou mais fatores |
| **Passwordless** | Elimina a dependência da senha | Autenticação sem senha |

> **PEGADINHA:** SSO, MFA e passwordless **não são a mesma coisa**.  
> **SSO** trata principalmente da experiência de login.  
> **MFA** adiciona fatores de autenticação.  
> **Passwordless** elimina a necessidade de uma senha tradicional.

---

<h3><strong style='color: skyblue'>Identidades externas no Azure</strong></h3>

<p align="justify">As <strong>identidades externas</strong> permitem que pessoas que não pertencem diretamente à organização utilizem recursos e aplicações controlados pelo Microsoft Entra ID.</p>

<p align="justify">Isso é útil para cenários envolvendo <strong>clientes, parceiros, fornecedores, convidados e usuários externos</strong>.</p>

<p align="justify">O Microsoft Entra ID possui recursos para colaboração com usuários externos, permitindo controlar o acesso sem necessariamente criar uma identidade interna tradicional para cada pessoa.</p>

---

### Microsoft Entra B2B

<p align="justify">O <strong>Microsoft Entra B2B (Business-to-Business)</strong> permite colaborar com usuários externos, como parceiros e fornecedores.</p>

<p align="justify">O usuário externo pode utilizar sua própria identidade para acessar recursos aos quais recebeu permissão.</p>

**Exemplo:**

<pre>
Empresa A
   │
   │ compartilha recurso
   ▼
Usuário externo da Empresa B
   │
   ▼
Microsoft Entra ID
   │
   ▼
Recurso autorizado
</pre>

<p align="justify">Esse modelo é utilizado principalmente para <strong>colaboração entre organizações</strong>.</p>

> **AZ-900:** B2B → **usuários externos / parceiros / convidados**.

---

### Microsoft Entra B2C

<p align="justify">O <strong>Microsoft Entra External ID</strong> fornece recursos para cenários de identidades externas, incluindo aplicações voltadas para consumidores.</p>

<p align="justify">Em materiais mais antigos da Microsoft, você pode encontrar a nomenclatura <strong>Azure AD B2C</strong>. A Microsoft passou a utilizar a família <strong>Microsoft Entra External ID</strong> para os recursos de identidade externa voltados a clientes.</p>

<p align="justify">O cenário típico é uma aplicação que precisa permitir que <strong>clientes</strong> criem ou utilizem uma identidade para acessar a aplicação.</p>

> **AZ-900:** Identidade externa para clientes → **External ID / cenário B2C**.

---

<h3><strong style='color: skyblue'>B2B x B2C</strong></h3>

| Cenário | Usuário | Objetivo |
|---|---|---|
| **B2B** | Parceiro, fornecedor ou convidado | Colaboração entre organizações |
| **B2C / External ID** | Cliente ou consumidor | Acesso de clientes a uma aplicação |

> **DECORA:**  
> **B2B → Business → empresas/parceiros**  
> **B2C → Consumer → clientes**

---

<h3><strong style='color: skyblue'>Mapa mental — Identidade no Azure</strong></h3>

<pre>
AZURE IDENTITY
│
├── Microsoft Entra ID
│   ├── Usuários
│   ├── Grupos
│   ├── Dispositivos
│   ├── Aplicações
│   ├── Autenticação
│   └── Autorização
│
├── Entra Domain Services
│   ├── LDAP
│   ├── Kerberos
│   ├── NTLM
│   └── Group Policy
│
├── Autenticação
│   ├── SSO
│   │   └── Uma autenticação → várias aplicações
│   │
│   ├── MFA
│   │   └── Dois ou mais fatores
│   │
│   └── Passwordless
│       └── Sem senha tradicional
│
└── Identidades externas
    ├── B2B
    │   └── Parceiros / convidados
    │
    └── External ID / B2C
        └── Clientes / consumidores
</pre>

---

<h3><strong style='color: skyblue'>Resumo para a prova AZ-900</strong></h3>

| Se a questão falar sobre... | Pense em... |
|---|---|
| Gerenciamento de identidades na nuvem | **Microsoft Entra ID** |
| Usuários, grupos e acesso a aplicações | **Microsoft Entra ID** |
| LDAP e Kerberos gerenciados no Azure | **Entra Domain Services** |
| Aplicação legada que precisa de domínio tradicional | **Entra Domain Services** |
| Uma autenticação para várias aplicações | **SSO** |
| Mais de um fator de autenticação | **MFA** |
| Autenticação sem senha | **Passwordless** |
| Microsoft Authenticator | **Passwordless / autenticação** |
| Windows Hello for Business | **Passwordless** |
| FIDO2 | **Passwordless** |
| Parceiro ou fornecedor externo | **B2B** |
| Usuário convidado externo | **B2B** |
| Cliente de uma aplicação | **External ID / B2C** |

> **🔥 DECORAÇÃO FINAL AZ-900**
>
> **Entra ID → identidade e acesso na nuvem**
>
> **Entra Domain Services → LDAP / Kerberos / NTLM / Group Policy**
>
> **SSO → uma vez, várias aplicações**
>
> **MFA → vários fatores**
>
> **Passwordless → sem senha**
>
> **B2B → parceiro/convidado**
>
> **B2C / External ID → cliente/consumidor**
