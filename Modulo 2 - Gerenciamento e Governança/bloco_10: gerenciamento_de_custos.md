## 💰 AZ-900 — Gerenciamento de custos do Azure

<p align="justify">O Azure oferece ferramentas para <strong>estimar, acompanhar, analisar e controlar os custos</strong> dos recursos de nuvem.</p>

---

<h3><strong style='color: skyblue'>1️⃣ Fatores que podem afetar os custos no Azure</strong></h3>

<p align="justify">O custo de um recurso no Azure não depende apenas do tipo de serviço. Diversos fatores podem alterar o preço final.</p>

### Principais fatores

- **Tipo de recurso** → VM, Storage, banco de dados etc.
- **Tamanho/capacidade** → uma VM maior custa mais que uma menor.
- **Região** → preços podem variar entre regiões.
- **Consumo** → quantidade de processamento, armazenamento, requisições etc.
- **Tempo de execução** → recursos executados por mais tempo podem gerar maior custo.
- **Transferência de dados** → determinados tipos de transferência podem gerar cobrança.
- **Modelo de compra** → Pay-as-you-go, Reservations, Spot etc.
- **Licenciamento** → algumas soluções possuem custos de licença.
- **Nível de desempenho** → tiers/performance superiores normalmente custam mais.
- **Redundância** → opções de redundância de armazenamento podem ter custos diferentes.

> **AZ-900:** O custo depende de **serviço + configuração + região + consumo + modelo de preço**.

---

<h3><strong style='color: skyblue'>2️⃣ Exemplo de fatores que alteram o preço</strong></h3>

<pre>
                 CUSTO AZURE
                      │
        ┌─────────────┼─────────────┐
        │             │             │
      Recurso       Região        Consumo
        │             │             │
       VM         Região A       CPU/RAM
        │         Região B       Storage
        │             │          Requests
        ▼             ▼
     Tamanho      Preço pode
     da VM        variar
</pre>

<p align="justify">Por exemplo, duas VMs do mesmo tipo podem apresentar custos diferentes dependendo da região, do sistema operacional/licenciamento e do modelo de compra.</p>

> **PEGADINHA:** "Azure é sempre mais barato" não é uma regra. O custo depende da configuração e do uso.

---

<h3><strong style='color: skyblue'>3️⃣ Calculadora de preços do Azure</strong></h3>

<p align="justify">A <strong>Azure Pricing Calculator</strong> permite estimar o custo de serviços do Azure antes de implantá-los.</p>

### Para que serve?

- Estimar custos.
- Comparar configurações.
- Simular diferentes quantidades de recursos.
- Avaliar diferentes regiões.
- Escolher opções de compra.
- Criar uma estimativa para uma solução.

### Exemplo

<pre>
Preciso de:
   │
   ├── 3 VMs
   ├── 1 TB Storage
   ├── Banco de dados
   └── Rede
          │
          ▼
Azure Pricing Calculator
          │
          ▼
Estimativa de custo
</pre>

<p align="justify">A calculadora permite selecionar os serviços e suas configurações para produzir uma estimativa.</p>

> **DECORA:**  
> **Pricing Calculator = ESTIMAR custos antes/depois de planejar uma solução.**

---

<h3><strong style='color: skyblue'>4️⃣ Pricing Calculator × Cost Management</strong></h3>

<p align="justify">Essa diferença é importante para a prova.</p>

| Ferramenta | Principal finalidade |
|---|---|
| **Pricing Calculator** | Estimar custos |
| **Azure Cost Management** | Analisar e controlar gastos reais |
| **Budgets** | Definir limites/alertas de orçamento |
| **Tags** | Categorizar recursos e custos |

> **PEGADINHA:** Pricing Calculator não é a ferramenta principal para analisar o gasto real da sua assinatura.

---

<h3><strong style='color: skyblue'>5️⃣ Azure Cost Management</strong></h3>

<p align="justify">O <strong>Microsoft Cost Management</strong> fornece recursos para analisar, monitorar e controlar os custos do Azure.</p>

### Permite:

- Analisar custos.
- Identificar onde o dinheiro está sendo gasto.
- Criar orçamentos.
- Configurar alertas.
- Analisar tendências.
- Identificar oportunidades de otimização.
- Dividir custos por diferentes categorias.

---

<h3><strong style='color: skyblue'>6️⃣ Cost Analysis</strong></h3>

<p align="justify"><strong>Cost Analysis</strong> permite visualizar e analisar os custos dos recursos.</p>

### Você pode analisar gastos por:

- Subscription.
- Resource Group.
- Serviço.
- Região.
- Período.
- Tags.
- Outros critérios disponíveis.

### Exemplo

<pre>
Subscription
     │
     ▼
Cost Analysis
     │
     ├── VMs ........  R$ X
     ├── Storage ....  R$ Y
     ├── Database ...  R$ Z
     └── Network ....  R$ W
</pre>

> **DECORA:** **Cost Analysis = descobrir ONDE o dinheiro está sendo gasto.**

---

<h3><strong style='color: skyblue'>7️⃣ Budgets (Orçamentos)</strong></h3>

<p align="justify">Os <strong>Budgets</strong> permitem definir um orçamento e configurar alertas quando o gasto ou a previsão de gasto atingir determinados limites.</p>

### Exemplo

<pre>
Orçamento mensal
      │
      ▼
   R$ 10.000
      │
      ├── 80% → alerta
      ├── 90% → alerta
      └── 100% → alerta
</pre>

<p align="justify">O orçamento ajuda a monitorar os gastos, mas atingir um orçamento não significa automaticamente que o Azure bloqueará os recursos.</p>

> **PEGADINHA AZ-900:** Budget = **monitoramento + alertas**, não necessariamente bloqueio automático do consumo.

---

<h3><strong style='color: skyblue'>8️⃣ Recomendações de custo</strong></h3>

<p align="justify">O Azure fornece recomendações que podem ajudar a identificar oportunidades para reduzir ou otimizar custos.</p>

### Exemplos

- Recursos subutilizados.
- VMs que podem ser redimensionadas.
- Recursos que podem ser desligados.
- Oportunidades de otimização.

> **DECORA:** **Recomendações = oportunidades de otimização.**

---

<h3><strong style='color: skyblue'>9️⃣ Tags</strong></h3>

<p align="justify"><strong>Tags</strong> são pares de <strong>nome/valor</strong> associados aos recursos para adicionar informações de identificação e organização.</p>

### Exemplo

<pre>
Recurso: VM-PROD-01

Tags:
   Ambiente = Produção
   Departamento = Financeiro
   Projeto = ERP
   CentroCusto = CC123
   Owner = Infra
</pre>

### Formato

<pre>
Nome       = Valor
Projeto    = ERP
Ambiente   = Produção
CentroCusto = 12345
</pre>

---

<h3><strong style='color: skyblue'>🔟 Para que servem as Tags?</strong></h3>

### Organização

<p align="justify">Identificar facilmente a finalidade dos recursos.</p>

### Classificação

<p align="justify">Separar recursos por ambiente, projeto, departamento ou aplicação.</p>

### Controle de custos

<p align="justify">Tags podem ser utilizadas para categorizar e analisar custos por projeto, departamento ou centro de custo.</p>

### Gerenciamento

<p align="justify">Podem ajudar a identificar responsáveis e ambientes.</p>

### Governança

<p align="justify">Podem fazer parte das estratégias de organização e governança dos recursos.</p>

> **AZ-900:** Tags ajudam a **organizar e categorizar recursos**, inclusive para análise de custos.

---

<h3><strong style='color: skyblue'>1️⃣1️⃣ Exemplo de controle de custos usando Tags</strong></h3>

<pre>
                    AZURE
                      │
             ┌────────┴────────┐
             │                 │
         Projeto ERP       Projeto CRM
             │                 │
          Recursos          Recursos
             │                 │
       Tag: Projeto=ERP   Tag: Projeto=CRM
             │                 │
             └────────┬────────┘
                      │
                      ▼
                Cost Analysis
                      │
                      ▼
              Analisar custos
              por projeto
</pre>

<p align="justify">Isso permite analisar quanto os recursos associados a determinadas categorias estão custando.</p>

---

<h3><strong style='color: skyblue'>1️⃣2️⃣ Hierarquia de gerenciamento de custos</strong></h3>

<pre>
                   AZURE
                     │
                     ▼
                Subscription
                     │
                     ▼
              Cost Management
                     │
          ┌──────────┼──────────┐
          │          │          │
     Cost Analysis Budgets  Recomendações
          │          │          │
          │          │          │
       "Quanto?"  "Quanto     "Como
                   posso       otimizar?"
                   gastar?"
</pre>

---

<h3><strong style='color: skyblue'>1️⃣3️⃣ Pricing Calculator × Cost Management × Tags</strong></h3>

| Recurso | Pergunta que responde |
|---|---|
| **Pricing Calculator** | 💰 "Quanto pode custar?" |
| **Cost Analysis** | 📊 "Quanto estou gastando?" |
| **Budgets** | 🚨 "Quando devo ser alertado?" |
| **Recommendations** | 🔧 "Onde posso otimizar?" |
| **Tags** | 🏷️ "A qual projeto/departamento pertence esse custo?" |

> **🔥 DECORAÇÃO:**  
> **Calculator → ESTIMA**  
> **Cost Analysis → ANALISA**  
> **Budget → ALERTA**  
> **Recommendations → OTIMIZA**  
> **Tags → ORGANIZA**

---

<h3><strong style='color: skyblue'>🧠 Mapa mental</strong></h3>

<pre>
                    GERENCIAMENTO DE CUSTOS
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
     FATORES              ESTIMATIVA            CONTROLE
        │                     │                     │
        ├── Região       Pricing Calculator    Cost Management
        ├── Recurso                              │
        ├── Tamanho                              ├── Cost Analysis
        ├── Consumo                              ├── Budgets
        ├── Tempo                                └── Recommendations
        ├── Licença
        └── Redundância
                              │
                              ▼
                           TAGS
                              │
                    ├── Projeto
                    ├── Ambiente
                    ├── Departamento
                    ├── Centro de custo
                    └── Responsável
</pre>

<h3><strong style='color: skyblue'>🎯 Resumo para a prova AZ-900</strong></h3>

| Se a questão falar sobre... | Pense em... |
|---|---|
| Estimar custo de uma solução | **Pricing Calculator** |
| Ver gastos atuais | **Cost Analysis** |
| Criar limite de orçamento | **Budgets** |
| Receber alerta de gasto | **Budgets** |
| Encontrar oportunidades de economia | **Cost Management / Recommendations** |
| Categorizar recursos | **Tags** |
| Analisar custo por projeto | **Tags + Cost Analysis** |
| Região influenciando preço | **Fator de custo** |
| Tamanho da VM influenciando preço | **Fator de custo** |
| Quantidade de recursos influenciando preço | **Fator de custo** |

> **🔥 PEGADINHAS FINAIS**
>
> **Pricing Calculator ≠ Cost Analysis**  
> Calculator estima; Cost Analysis analisa gastos.
>
> **Budget ≠ bloqueio de recursos**  
> Budget serve principalmente para monitoramento e alertas.
>
> **Tag ≠ ferramenta de cobrança**  
> Tags ajudam a categorizar e analisar custos; não são uma forma de cobrança.
>
> **Custo não depende apenas do serviço**  
> Região, configuração, capacidade, consumo, tempo, transferência de dados, redundância e modelo de compra também podem afetar o preço.
