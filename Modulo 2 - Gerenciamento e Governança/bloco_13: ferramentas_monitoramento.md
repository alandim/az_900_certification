## 🩺 Monitoramento, suporte e integridade do Azure

<h3><strong style='color: skyblue'>1️⃣ Assistente do Azure — Azure Advisor</strong></h3>

<p align="justify">O <strong>Azure Advisor</strong> é um serviço que analisa os recursos do Azure e fornece <strong>recomendações personalizadas</strong> para ajudar a melhorar o ambiente.</p>

### 🎯 Para que serve?

O Advisor fornece recomendações em áreas como:

- 💰 **Custo** — identificar oportunidades de reduzir gastos.
- ⚡ **Desempenho** — melhorar performance.
- 🔐 **Segurança** — identificar oportunidades de melhorar a segurança.
- 🛡️ **Confiabilidade** — melhorar a disponibilidade/resiliência.
- 🏗️ **Excelência operacional** — melhorar práticas de operação.

### 🧠 Exemplo

Imagine que você possui uma VM que está sendo pouco utilizada.

O Azure Advisor pode identificar a situação e recomendar uma ação de otimização.

```text
Recursos Azure
      │
      ▼
Azure Advisor
      │
      ▼
Analisa ambiente
      │
      ▼
Recomendações
 ├── 💰 Custo
 ├── ⚡ Desempenho
 ├── 🔐 Segurança
 ├── 🛡️ Confiabilidade
 └── 🏗️ Operação
```

> **AZ-900:** Azure Advisor = **RECOMENDAÇÕES para otimizar o ambiente**.

### ⚠️ PEGADINHA

**Advisor não é Azure Monitor.**

| Serviço | Pergunta principal |
|---|---|
| **Azure Advisor** | "Como posso melhorar/otimizar meu ambiente?" |
| **Azure Monitor** | "O que está acontecendo com meu ambiente?" |
| **Service Health** | "Existe algum problema/incidente afetando meus serviços Azure?" |

---

<h3><strong style='color: skyblue'>2️⃣ Integridade do Serviço do Azure — Azure Service Health</strong></h3>

<p align="justify">O <strong>Azure Service Health</strong> fornece informações sobre a <strong>integridade dos serviços do Azure</strong> e ajuda a identificar problemas que podem afetar seus recursos.</p>

Ele reúne informações importantes sobre eventos e problemas do Azure que podem impactar seu ambiente.

### 🎯 Principais componentes

| Componente | Finalidade |
|---|---|
| **Azure Status** | Visão global da disponibilidade dos serviços Azure |
| **Service Health** | Informações personalizadas sobre eventos que podem afetar você |
| **Resource Health** | Estado de integridade de um recurso específico |

### 🟢 Azure Status

Mostra uma visão **global** do Azure.

Exemplo:

```text
Azure Status
     │
     ├── Serviço X → problema global
     ├── Serviço Y → normal
     └── Serviço Z → incidente
```

> **Palavra-chave:** visão **global**.

### 🔔 Service Health

Mostra informações relevantes para o **seu ambiente**, como:

- Incidentes de serviço.
- Manutenções planejadas.
- Avisos de saúde.
- Informações sobre impacto nos serviços.

> **Palavra-chave:** impacto **no seu ambiente**.

### 🖥️ Resource Health

Permite verificar a saúde de um **recurso específico**.

Exemplo:

```text
Minha VM
   │
   ▼
Resource Health
   │
   ├── Disponível
   ├── Indisponível
   └── Estado degradado
```

> **DECORA:**  
> **Status = Azure inteiro**  
> **Service Health = impacto nos meus serviços**  
> **Resource Health = meu recurso específico**

---

<h3><strong style='color: skyblue'>3️⃣ Azure Monitor</strong></h3>

<p align="justify">O <strong>Azure Monitor</strong> é uma plataforma de monitoramento que coleta e analisa <strong>métricas, logs e outros dados de telemetria</strong> de aplicações e recursos.</p>

A ideia central é:

```text
RECURSOS / APLICAÇÕES
          │
          ▼
     Azure Monitor
          │
     ┌────┼────┐
     ▼    ▼    ▼
  Métricas Logs Alertas
```

### 🎯 Para que serve?

- Monitorar desempenho.
- Detectar problemas.
- Analisar métricas.
- Consultar logs.
- Criar alertas.
- Identificar tendências.
- Monitorar aplicações.
- Investigar incidentes.

> **AZ-900:** Azure Monitor = **monitorar e analisar o desempenho e a operação dos recursos/aplicações**.

---

<h3><strong style='color: skyblue'>4️⃣ Azure Monitor — Métricas × Logs</strong></h3>

Essa diferença é importante.

### 📊 Métricas

São valores numéricos medidos ao longo do tempo.

Exemplos:

- CPU %
- Memória
- Latência
- Número de requisições
- Throughput

```text
VM
 │
 ├── CPU: 85%
 ├── Requests: 2.500
 └── Latência: 120 ms
```

### 📜 Logs

Contêm informações/eventos registrados pelos recursos e aplicações.

Podem ajudar a responder:

> "O que aconteceu?"

Exemplo:

```text
18:30 → Login recebido
18:31 → Erro 500
18:32 → Consulta SQL executada
18:33 → Timeout
```

> **DECORA:**  
> **Métrica = número/medição**  
> **Log = evento/informação registrada**

---

<h3><strong style='color: skyblue'>5️⃣ Log Analytics</strong></h3>

<p align="justify">O <strong>Log Analytics</strong> é uma ferramenta do Azure Monitor usada para <strong>consultar e analisar dados de logs</strong> armazenados em um <strong>Log Analytics workspace</strong>.</p>

Ele utiliza a linguagem **Kusto Query Language (KQL)** para realizar consultas.

### 🧠 Fluxo

```text
Recursos / Aplicações
        │
        ▼
      Logs
        │
        ▼
Log Analytics Workspace
        │
        ▼
   Log Analytics
        │
        ▼
       KQL
        │
        ▼
   Análise / Investigação
```

### 🎯 Exemplo conceitual

Você quer descobrir:

> "Quais erros ocorreram nas últimas 24 horas?"

O Log Analytics permite consultar os logs usando KQL.

> **AZ-900:** Log Analytics = **consultar/analisar logs**.

### ⚠️ PEGADINHA

**Log Analytics não é o mesmo que Azure Monitor.**

```text
Azure Monitor
     │
     ├── Métricas
     ├── Logs
     ├── Alertas
     └── Application Insights
              │
              ▼
       Monitoramento de aplicações

Log Analytics
     │
     └── Consulta/análise de logs
         usando KQL
```

---

<h3><strong style='color: skyblue'>6️⃣ Alertas do Azure Monitor</strong></h3>

<p align="justify">Os <strong>Azure Monitor Alerts</strong> permitem configurar condições para que o Azure <strong>detecte situações importantes e gere notificações ou ações</strong>.</p>

### 🧠 Exemplo

Você pode criar um alerta:

```text
CPU > 90%
   │
   ▼
Azure Monitor
   │
   ▼
Condição satisfeita
   │
   ▼
🔔 ALERTA
   │
   ▼
Notificação / ação
```

Podem ser usados para monitorar:

- Métricas.
- Logs.
- Atividade.
- Disponibilidade.
- Condições específicas dos recursos.

> **AZ-900:** Alertas = **reagir quando uma condição definida for atingida**.

### ⚠️ Diferença importante

```text
Azure Monitor
     │
     ├── COLETA dados
     ├── ANALISA dados
     └── DETECTA condições
                │
                ▼
             ALERTA
                │
                ▼
       Notificação / ação
```

---

<h3><strong style='color: skyblue'>7️⃣ Application Insights</strong></h3>

<p align="justify">O <strong>Azure Monitor Application Insights</strong> é um recurso do Azure Monitor voltado para <strong>monitoramento de aplicações</strong>.</p>

Ele ajuda desenvolvedores e equipes de operações a entender como uma aplicação está funcionando e identificar problemas.

### 🎯 Pode ajudar a monitorar:

- Disponibilidade da aplicação.
- Requisições.
- Tempo de resposta.
- Erros e exceções.
- Dependências.
- Desempenho.
- Comportamento da aplicação.

### 🧠 Exemplo

Uma API está apresentando lentidão.

```text
Usuário
   │
   ▼
Aplicação
   │
   ├── Requisição → 2s
   ├── Banco      → 1,7s
   └── API        → 2s
          │
          ▼
 Application Insights
          │
          ▼
 Identifica gargalo
```

> **AZ-900:** Application Insights = **monitoramento de aplicações e sua performance/telemetria**.

---

<h3><strong style='color: skyblue'>8️⃣ Como tudo se relaciona?</strong></h3>

<pre>
                    AZURE
                      │
       ┌──────────────┴──────────────┐
       │                             │
   SERVICE HEALTH                AZURE MONITOR
       │                             │
       │                  ┌──────────┼───────────┐
       │                  │          │           │
   Saúde do Azure       Métricas    Logs      Alertas
       │                             │
       │                             ▼
       │                       Log Analytics
       │                             │
       │                            KQL
       │
       └── Incidentes
       └── Manutenções
       └── Avisos
       └── Impactos

                           AZURE MONITOR
                                │
                                ▼
                       APPLICATION INSIGHTS
                                │
                                ▼
                       Aplicações / APIs
                       ├── Requests
                       ├── Errors
                       ├── Performance
                       └── Dependencies


                    AZURE ADVISOR
                         │
                         ▼
                   RECOMENDAÇÕES
                   ├── Custo
                   ├── Segurança
                   ├── Performance
                   ├── Confiabilidade
                   └── Operação
</pre>

<h3><strong style='color: skyblue'>🔥 DECORAÇÃO FINAL</strong></h3>

> **Advisor → "Como posso melhorar meu ambiente?"**

> **Service Health → "Existe algum problema/manutenção do Azure que afeta meus serviços?"**

> **Resource Health → "Qual é o estado deste recurso específico?"**

> **Azure Monitor → "O que está acontecendo no meu ambiente?"**

> **Log Analytics → "Quero consultar/analisar os logs."**

> **Monitor Alerts → "Avise-me quando uma condição acontecer."**

> **Application Insights → "Como minha aplicação está funcionando?"**

### 🎯 PEGADINHAS AZ-900

- **Recomendação para reduzir custos → Azure Advisor**
- **Recomendação para melhorar segurança → Azure Advisor**
- **Incidente/manutenção do Azure que pode afetar seu ambiente → Service Health**
- **Visão global da disponibilidade do Azure → Azure Status**
- **Saúde de uma VM/recurso específico → Resource Health**
- **Monitoramento de métricas e logs → Azure Monitor**
- **Consulta de logs usando KQL → Log Analytics**
- **CPU ultrapassou determinado limite e você quer ser avisado → Azure Monitor Alert**
- **Monitorar requisições, erros e desempenho de uma aplicação → Application Insights**

> 🧠 **REGRA DE 7 SEGUNDOS:**
>
> **ADVISOR = RECOMENDA**  
> **SERVICE HEALTH = INCIDENTES/MANUTENÇÃO**  
> **RESOURCE HEALTH = RECURSO**  
> **MONITOR = MONITORA**  
> **LOG ANALYTICS = LOGS + KQL**  
> **ALERT = AVISA**  
> **APPLICATION INSIGHTS = APLICAÇÃO**
