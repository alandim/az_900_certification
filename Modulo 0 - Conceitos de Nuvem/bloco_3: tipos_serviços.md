## ☁️ Modelos de serviço de nuvem

<p align="justify">Os principais modelos de serviço de nuvem são <strong>IaaS (Infraestrutura como Serviço)</strong>, <strong>PaaS (Plataforma como Serviço)</strong> e <strong>SaaS (Software como Serviço)</strong>.</p>

<p align="justify">A principal diferença entre eles está no <strong>nível de responsabilidade e controle</strong> que fica com o cliente e com o provedor de nuvem.</p>

<pre>
MAIOR CONTROLE DO CLIENTE
        │
        ▼
      IaaS
        │
      PaaS
        │
      SaaS
        │
        ▼
MAIOR GERENCIAMENTO DO PROVEDOR
</pre>

> **AZ-900:** Quanto mais você sobe de **IaaS → PaaS → SaaS**, menos infraestrutura você precisa gerenciar.

---

<h3><strong style='color: skyblue'>1️⃣ IaaS — Infraestrutura como Serviço</strong></h3>

<p align="justify">A <strong>IaaS (Infrastructure as a Service)</strong> fornece recursos básicos de infraestrutura de TI pela nuvem, como <strong>máquinas virtuais, armazenamento e redes</strong>.</p>

<p align="justify">O provedor gerencia a infraestrutura física, enquanto o cliente possui maior controle sobre o ambiente virtual, incluindo o sistema operacional, aplicações e dados.</p>

### O provedor gerencia:

- Datacenters.
- Hardware físico.
- Rede física.
- Armazenamento físico.
- Virtualização.

### O cliente gerencia:

- Sistema operacional.
- Aplicações.
- Dados.
- Configurações do ambiente.
- Controle do software instalado.

<pre>
┌─────────────────────────────┐
│ Aplicação       → CLIENTE   │
│ Dados           → CLIENTE   │
│ Sistema Operacional → CLIENTE│
├─────────────────────────────┤
│ Virtualização   → AZURE     │
│ Hardware        → AZURE     │
│ Rede física     → AZURE     │
│ Datacenter      → AZURE     │
└─────────────────────────────┘
</pre>

### Exemplos no Azure

- Azure Virtual Machines.
- Discos gerenciados.
- Redes virtuais.
- IPs e componentes de rede.

> **AZ-900:** IaaS = **mais controle + mais responsabilidade**.

---

<h3><strong style='color: skyblue'>Quando usar IaaS?</strong></h3>

<p align="justify">IaaS é apropriado quando você precisa de <strong>maior controle sobre o sistema operacional e o ambiente de execução</strong>.</p>

### Casos de uso

- Migrar uma aplicação existente de um datacenter para a nuvem.
- Executar uma aplicação que exige configuração específica do sistema operacional.
- Hospedar aplicações legadas.
- Executar softwares personalizados.
- Criar ambientes de desenvolvimento e teste com controle sobre as VMs.
- Quando é necessário instalar softwares específicos no servidor.

### Exemplo

<p align="justify">Uma empresa possui uma aplicação antiga que precisa de uma versão específica do Windows Server e de determinados componentes instalados no sistema operacional.</p>

<p align="justify">Nesse caso, uma <strong>VM do Azure</strong> pode fornecer o nível de controle necessário.</p>

> **Pense em IaaS:**  
> **"Quero controlar o servidor."**

---

<h3><strong style='color: skyblue'>2️⃣ PaaS — Plataforma como Serviço</strong></h3>

<p align="justify">A <strong>PaaS (Platform as a Service)</strong> fornece uma plataforma gerenciada para desenvolver, executar e hospedar aplicações sem que o cliente precise administrar a infraestrutura subjacente.</p>

<p align="justify">O provedor gerencia componentes como <strong>hardware, rede, virtualização e sistema operacional</strong>, permitindo que o cliente se concentre principalmente na aplicação e nos dados.</p>

<pre>
┌─────────────────────────────┐
│ Aplicação       → CLIENTE   │
│ Dados           → CLIENTE   │
├─────────────────────────────┤
│ Runtime         → AZURE     │
│ Sistema Operacional → AZURE │
│ Virtualização   → AZURE     │
│ Hardware        → AZURE     │
│ Rede            → AZURE     │
│ Datacenter      → AZURE     │
└─────────────────────────────┘
</pre>

### Exemplos no Azure

- Azure App Service.
- Azure Functions.
- Azure Container Apps.
- Serviços gerenciados de banco de dados.

> **AZ-900:** PaaS = **foco na aplicação sem administrar a infraestrutura**.

---

<h3><strong style='color: skyblue'>Quando usar PaaS?</strong></h3>

<p align="justify">PaaS é apropriado quando você quer <strong>desenvolver e executar uma aplicação sem precisar gerenciar servidores e sistemas operacionais</strong>.</p>

### Casos de uso

- Desenvolvimento de aplicações Web.
- Hospedagem de APIs.
- Desenvolvimento rápido de aplicações.
- Aplicações que precisam de escalabilidade.
- APIs e back-ends.
- Aplicações modernas que não precisam de controle do sistema operacional.

### Exemplo

<p align="justify">Uma equipe desenvolve uma API em Python e quer hospedá-la sem precisar configurar uma VM, instalar o sistema operacional, aplicar patches ou administrar o servidor.</p>

<p align="justify">Uma solução PaaS pode fornecer o ambiente necessário para executar a aplicação.</p>

> **Pense em PaaS:**  
> **"Quero desenvolver a aplicação, não administrar o servidor."**

---

<h3><strong style='color: skyblue'>3️⃣ SaaS — Software como Serviço</strong></h3>

<p align="justify">O <strong>SaaS (Software as a Service)</strong> fornece uma aplicação completa pela Internet.</p>

<p align="justify">Nesse modelo, o provedor gerencia praticamente toda a infraestrutura e a própria aplicação. O usuário normalmente precisa apenas utilizar o software e configurar as opções disponibilizadas.</p>

<pre>
┌─────────────────────────────┐
│ Aplicação       → AZURE     │
│ Dados           → AZURE*    │
│ Runtime         → AZURE     │
│ SO              → AZURE     │
│ Virtualização   → AZURE     │
│ Hardware        → AZURE     │
│ Rede            → AZURE     │
│ Datacenter      → AZURE     │
└─────────────────────────────┘

* O cliente continua responsável pelos
dados e configurações que utiliza no serviço.
</pre>

### Exemplos de SaaS

- Microsoft 365.
- Microsoft Teams.
- Outlook na Web.
- Microsoft Dynamics 365.

> **AZ-900:** SaaS = **software pronto para utilização**.

---

<h3><strong style='color: skyblue'>Quando usar SaaS?</strong></h3>

<p align="justify">SaaS é apropriado quando você precisa utilizar uma aplicação pronta sem se preocupar com a infraestrutura ou com o desenvolvimento e manutenção do software.</p>

### Casos de uso

- E-mail corporativo.
- Ferramentas de colaboração.
- Videoconferência.
- CRM.
- Aplicações de produtividade.
- Sistemas empresariais prontos.

### Exemplo

<p align="justify">Uma empresa precisa de uma plataforma de e-mail corporativo. Em vez de criar e administrar seus próprios servidores de e-mail, pode utilizar uma solução SaaS como o Microsoft 365.</p>

> **Pense em SaaS:**  
> **"Quero usar o software pronto."**

---

<h3><strong style='color: skyblue'>4️⃣ Comparação IaaS x PaaS x SaaS</strong></h3>

| Característica | IaaS | PaaS | SaaS |
|---|:---:|:---:|:---:|
| Hardware | Azure | Azure | Azure |
| Rede física | Azure | Azure | Azure |
| Virtualização | Azure | Azure | Azure |
| Sistema operacional | **Cliente** | Azure | Azure |
| Runtime | **Cliente** | Azure | Azure |
| Aplicação | **Cliente** | **Cliente** | Azure |
| Dados | **Cliente** | **Cliente** | Cliente* |
| Controle do cliente | 🔵 Alto | 🟡 Médio | 🟢 Baixo |
| Gerenciamento pelo cliente | 🔵 Alto | 🟡 Médio | 🟢 Baixo |

<p align="justify">Essa divisão representa o modelo tradicional de responsabilidade compartilhada. Na prática, os limites exatos podem variar de acordo com o serviço específico. :contentReference[oaicite:1]{index=1}</p>

---

<h3><strong style='color: skyblue'>5️⃣ Escada de responsabilidade</strong></h3>

<pre>
                 MAIS CONTROLE
                      ▲
                      │
              ┌──────────────┐
              │     IaaS     │
              │              │
              │ Mais controle│
              │ Mais trabalho│
              └──────────────┘
                      │
              ┌──────────────┐
              │     PaaS     │
              │              │
              │ Menos gestão │
              │ de infra      │
              └──────────────┘
                      │
              ┌──────────────┐
              │     SaaS     │
              │              │
              │ Software     │
              │ pronto       │
              └──────────────┘
                      │
                      ▼
               MENOS CONTROLE
</pre>

> **Quanto mais controle → mais responsabilidade.**  
> **Quanto menos infraestrutura você gerencia → mais o provedor gerencia.**

---

<h3><strong style='color: skyblue'>6️⃣ Exemplo prático: aplicação Web</strong></h3>

<p align="justify">Imagine que você tenha uma aplicação Web e queira colocá-la no Azure.</p>

### IaaS

<pre>
Você
 │
 ├── Cria VM
 ├── Configura SO
 ├── Instala runtime
 ├── Instala aplicação
 └── Mantém servidor
</pre>

**Escolha IaaS quando:** você precisa controlar o servidor e o sistema operacional.

---

### PaaS

<pre>
Você
 │
 ├── Desenvolve aplicação
 └── Faz deploy
          │
          ▼
       Azure
       ├── SO
       ├── Runtime
       ├── Infraestrutura
       └── Escalabilidade
</pre>

**Escolha PaaS quando:** você quer focar no desenvolvimento da aplicação.

---

### SaaS

<pre>
Você
 │
 └── Utiliza aplicação pronta
          │
          ▼
       Azure / Provedor
       └── Gerencia o restante
</pre>

**Escolha SaaS quando:** você só precisa utilizar uma aplicação pronta.

---

<h3><strong style='color: skyblue'>7️⃣ Como identificar na prova</strong></h3>

| A questão falar sobre... | Pense em... |
|---|---|
| Máquina virtual | **IaaS** |
| Controle do sistema operacional | **IaaS** |
| Aplicação legada | **IaaS** |
| Configuração personalizada do servidor | **IaaS** |
| Desenvolvimento de aplicações | **PaaS** |
| Hospedar uma aplicação Web sem administrar servidor | **PaaS** |
| API sem gerenciar infraestrutura | **PaaS** |
| Aplicação pronta | **SaaS** |
| E-mail como serviço | **SaaS** |
| CRM pronto | **SaaS** |
| Microsoft 365 | **SaaS** |

---

<h3><strong style='color: skyblue'>8️⃣ IaaS x PaaS x SaaS — regra rápida</strong></h3>

<pre>
"QUERO CONTROLAR O SERVIDOR"
              │
              ▼
             IaaS
              
"QUERO DESENVOLVER A APLICAÇÃO"
              │
              ▼
             PaaS

"QUERO USAR A APLICAÇÃO PRONTA"
              │
              ▼
             SaaS
</pre>

---

<h3><strong style='color: skyblue'>🧠 Mapa mental</strong></h3>

<pre>
MODELOS DE SERVIÇO
│
├── IaaS
│   ├── Infraestrutura
│   ├── VM
│   ├── Storage
│   ├── Rede
│   ├── Mais controle
│   ├── Mais responsabilidade
│   └── Aplicações legadas / customizadas
│
├── PaaS
│   ├── Plataforma gerenciada
│   ├── Desenvolvimento
│   ├── Web Apps
│   ├── APIs
│   ├── Menos gestão de infraestrutura
│   └── Foco na aplicação
│
└── SaaS
    ├── Software pronto
    ├── Microsoft 365
    ├── E-mail
    ├── CRM
    ├── Pouca gestão
    └── Foco na utilização
</pre>

---

<h3><strong style='color: skyblue'>🎯 Resumo para a prova AZ-900</strong></h3>

| Modelo | O que você recebe | Principal característica | Caso de uso |
|---|---|---|---|
| **IaaS** | Infraestrutura | Controle do SO e ambiente | VM / aplicação legada |
| **PaaS** | Plataforma | Foco no desenvolvimento | Web App / API |
| **SaaS** | Software pronto | Foco na utilização | Microsoft 365 / CRM |

> **🔥 DECORAÇÃO FINAL AZ-900**
>
> **IaaS → Infraestrutura → EU gerencio mais**
>
> **PaaS → Plataforma → EU desenvolvo**
>
> **SaaS → Software → EU utilizo**
>
> **IaaS = mais controle**
>
> **PaaS = equilíbrio entre controle e gerenciamento**
>
> **SaaS = menos gerenciamento**
