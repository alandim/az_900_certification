## Segurança no Azure

<p align="justify">O Azure utiliza diferentes conceitos e serviços para proteger identidades, dados, aplicações e infraestrutura. Para o AZ-900, três conceitos importantes são <strong>Confiança Zero (Zero Trust)</strong>, <strong>Defesa em Profundidade (Defense in Depth)</strong> e <strong>Microsoft Defender for Cloud</strong>.</p>

---

<h3><strong style='color: skyblue'>Confiança Zero (Zero Trust)</strong></h3>

<p align="justify">O modelo de <strong>Confiança Zero (Zero Trust)</strong> parte do princípio de que nenhuma identidade, dispositivo ou rede deve ser considerada confiável automaticamente.</p>

<p align="justify">Em vez de confiar implicitamente em algo porque está dentro da rede corporativa, cada solicitação deve ser <strong>verificada e autorizada</strong> antes que o acesso seja concedido.</p>

> **AZ-900:** Zero Trust → **"Nunca confie, sempre verifique."**

---

### Princípios da Confiança Zero

#### 1. Verificar explicitamente

<p align="justify">As decisões de acesso devem considerar todos os sinais disponíveis, como identidade, localização, dispositivo, aplicação e risco.</p>

**Exemplo:**

<pre>
Usuário
   │
   ├── Identidade
   ├── Dispositivo
   ├── Localização
   ├── Aplicação
   └── Risco
        │
        ▼
   Verificação
        │
        ▼
   Decisão de acesso
</pre>

---

#### 2. Usar acesso com privilégio mínimo

<p align="justify">Os usuários e sistemas devem receber somente as permissões necessárias para realizar suas atividades.</p>

<p align="justify">Isso reduz o impacto caso uma identidade ou recurso seja comprometido.</p>

**Exemplo:**

- Um usuário que precisa apenas consultar uma VM recebe **Reader**.
- Um administrador que precisa alterar recursos pode receber **Contributor**.
- Não é necessário conceder **Owner** quando as permissões adicionais não são necessárias.

> **Privilégio mínimo → somente o acesso necessário.**

---

#### 3. Presumir violação

<p align="justify">O modelo considera que uma violação pode ocorrer e, por isso, os recursos devem ser protegidos mesmo quando outra camada de segurança já existe.</p>

<p align="justify">Isso envolve reduzir o impacto de um possível comprometimento por meio de segmentação, monitoramento, controles de acesso e outras medidas.</p>

> **Presumir violação → agir como se um comprometimento pudesse acontecer.**

---

### Os três princípios

<pre>
ZERO TRUST
│
├── Verificar explicitamente
│   └── Validar identidade, dispositivo, contexto etc.
│
├── Privilégio mínimo
│   └── Conceder apenas o acesso necessário
│
└── Presumir violação
    └── Limitar impacto de um possível comprometimento
</pre>

> **DECORA:**  
> **Verificar explicitamente**  
> **Privilégio mínimo**  
> **Presumir violação**

---

<h3><strong style='color: skyblue'>Confiança Zero x Segurança de rede tradicional</strong></h3>

<p align="justify">Em um modelo tradicional, uma organização pode confiar mais nos recursos que estão dentro da rede corporativa. No modelo Zero Trust, estar dentro da rede <strong>não significa que o acesso será automaticamente confiável</strong>.</p>

<pre>
MODELO TRADICIONAL

Internet
   │
   ▼
Firewall
   │
   ▼
Rede interna
   │
   └── Maior confiança


ZERO TRUST

Usuário / Dispositivo
        │
        ▼
   Verificação
        │
        ▼
   Autorização
        │
        ▼
Recurso específico
</pre>

> **AZ-900:** Zero Trust não significa simplesmente "bloquear tudo". Significa **verificar e autorizar explicitamente**.

---

<h3><strong style='color: skyblue'>Defesa em Profundidade (Defense in Depth)</strong></h3>

<p align="justify">A <strong>Defesa em Profundidade</strong> é uma estratégia de segurança que utiliza <strong>múltiplas camadas de proteção</strong>.</p>

<p align="justify">O objetivo é evitar que a falha ou violação de uma única camada permita que um invasor comprometa todo o ambiente.</p>

<pre>
┌──────────────────────────────┐
│ Segurança física             │
├──────────────────────────────┤
│ Identidade e acesso          │
├──────────────────────────────┤
│ Perímetro / rede             │
├──────────────────────────────┤
│ Rede                          │
├──────────────────────────────┤
│ Computação                    │
├──────────────────────────────┤
│ Aplicações                    │
├──────────────────────────────┤
│ Dados                         │
└──────────────────────────────┘
</pre>

<p align="justify">Cada camada fornece uma barreira adicional de proteção.</p>

---

### Camadas da Defesa em Profundidade

#### Segurança física

<p align="justify">Protege instalações, datacenters, servidores e equipamentos físicos contra acesso não autorizado ou danos.</p>

**Exemplos:**

- Controle de acesso físico.
- Câmeras.
- Portas de segurança.
- Proteção dos datacenters.

---

#### Identidade e acesso

<p align="justify">Controla quem pode acessar sistemas e recursos.</p>

**Exemplos:**

- Microsoft Entra ID.
- MFA.
- RBAC.
- Acesso Condicional.

---

#### Perímetro

<p align="justify">Protege a fronteira entre a rede e o ambiente externo.</p>

**Exemplos:**

- Azure DDoS Protection.
- Azure Firewall.

---

#### Rede

<p align="justify">Controla a comunicação entre redes e recursos.</p>

**Exemplos:**

- Network Security Groups (NSG).
- Segmentação de rede.
- Azure Firewall.

---

#### Computação

<p align="justify">Protege servidores e máquinas virtuais.</p>

**Exemplos:**

- Atualizações de segurança.
- Antimalware.
- Controle de acesso às VMs.

---

#### Aplicações

<p align="justify">Protege o software e as aplicações contra vulnerabilidades e ataques.</p>

**Exemplos:**

- Validação de entrada.
- Secure coding.
- Web Application Firewall (WAF).

---

#### Dados

<p align="justify">Protege as informações armazenadas e processadas.</p>

**Exemplos:**

- Criptografia.
- Controle de acesso.
- Backups.
- Proteção contra perda de dados.

---

### Objetivo da Defesa em Profundidade

<p align="justify">O objetivo não é simplesmente adicionar ferramentas de segurança. A ideia é criar <strong>camadas independentes de proteção</strong> para reduzir o impacto de uma falha ou ataque.</p>

**Exemplo:**

<pre>
Atacante
   │
   ▼
Camada 1 → Firewall
   │
   ▼
Camada 2 → NSG
   │
   ▼
Camada 3 → Identidade + MFA
   │
   ▼
Camada 4 → RBAC
   │
   ▼
Camada 5 → Proteção dos dados
</pre>

<p align="justify">Mesmo que uma camada seja comprometida, as demais continuam fornecendo proteção.</p>

> **AZ-900:** Defesa em Profundidade → **múltiplas camadas de segurança**.

---

<h3><strong style='color: skyblue'>Confiança Zero x Defesa em Profundidade</strong></h3>

| Conceito | Ideia principal |
|---|---|
| **Zero Trust** | Não confiar implicitamente; verificar sempre |
| **Defesa em Profundidade** | Utilizar várias camadas de proteção |

> **DECORA:**  
> **Zero Trust = modelo de confiança**  
> **Defense in Depth = modelo de camadas**

---

<h3><strong style='color: skyblue'>Microsoft Defender for Cloud</strong></h3>

<p align="justify">O <strong>Microsoft Defender for Cloud</strong> é uma plataforma de segurança que ajuda a proteger recursos e workloads em ambientes de nuvem e híbridos.</p>

<p align="justify">Ele fornece recursos para <strong>avaliar a postura de segurança, identificar riscos, detectar ameaças e fornecer recomendações de segurança</strong>.</p>

---

### Principais finalidades

#### Postura de segurança

<p align="justify">O Defender for Cloud ajuda a identificar configurações e práticas que podem representar riscos de segurança.</p>

<p align="justify">Ele fornece recomendações que ajudam a melhorar a postura de segurança do ambiente.</p>

**Exemplos:**

- Identificar recursos com configurações inseguras.
- Identificar recomendações de segurança.
- Avaliar a postura geral do ambiente.

---

#### Proteção contra ameaças

<p align="justify">O Defender for Cloud também fornece recursos de proteção e detecção de ameaças para workloads.</p>

<p align="justify">Dependendo dos recursos habilitados, ele pode monitorar diferentes tipos de workloads, incluindo máquinas virtuais, containers, bancos de dados e outros recursos.</p>

---

#### Recomendações de segurança

<p align="justify">O serviço apresenta recomendações que podem ajudar a corrigir problemas identificados.</p>

**Exemplo conceitual:**

<pre>
Recurso Azure
     │
     ▼
Defender for Cloud
     │
     ├── Avalia configuração
     ├── Identifica risco
     ├── Gera recomendação
     └── Ajuda na proteção
</pre>

> **AZ-900:** Defender for Cloud → **postura de segurança + proteção contra ameaças**.

---

<h3><strong style='color: skyblue'>Defender for Cloud x Microsoft Defender XDR</strong></h3>

<p align="justify">Para o AZ-900, não é necessário confundir o <strong>Defender for Cloud</strong> com outras soluções da família Microsoft Defender.</p>

<p align="justify">O Defender for Cloud tem foco na <strong>segurança de recursos e workloads de nuvem e ambientes híbridos</strong>, incluindo postura de segurança e proteção contra ameaças.</p>

| Serviço | Foco |
|---|---|
| **Defender for Cloud** | Segurança de recursos e workloads de nuvem/híbridos |
| **Microsoft Defender XDR** | Detecção e resposta coordenadas em diferentes domínios de segurança |

---

<h3><strong style='color: skyblue'>Mapa mental — Segurança do Azure</strong></h3>

<pre>
SEGURANÇA AZURE
│
├── ZERO TRUST
│   │
│   ├── Verificar explicitamente
│   ├── Privilégio mínimo
│   └── Presumir violação
│
├── DEFESA EM PROFUNDIDADE
│   │
│   ├── Segurança física
│   ├── Identidade e acesso
│   ├── Perímetro
│   ├── Rede
│   ├── Computação
│   ├── Aplicações
│   └── Dados
│
└── DEFENDER FOR CLOUD
    │
    ├── Postura de segurança
    ├── Recomendações
    ├── Avaliação de riscos
    └── Proteção / detecção de ameaças
</pre>

---

<h3><strong style='color: skyblue'>Resumo para a prova AZ-900</strong></h3>

| Se a questão falar sobre... | Pense em... |
|---|---|
| Nunca confiar automaticamente | **Zero Trust** |
| Verificar cada solicitação | **Zero Trust** |
| Privilégio mínimo | **Zero Trust** |
| Presumir violação | **Zero Trust** |
| Várias camadas de proteção | **Defesa em Profundidade** |
| Segurança física + rede + identidade + dados | **Defesa em Profundidade** |
| Avaliar postura de segurança | **Defender for Cloud** |
| Recomendações de segurança | **Defender for Cloud** |
| Detectar ameaças em workloads | **Defender for Cloud** |
| Proteger recursos de nuvem e ambientes híbridos | **Defender for Cloud** |

> **🔥 DECORAÇÃO FINAL AZ-900**
>
> **ZERO TRUST → nunca confie, sempre verifique**
>
> **3 princípios → verificar explicitamente + privilégio mínimo + presumir violação**
>
> **DEFESA EM PROFUNDIDADE → várias camadas de segurança**
>
> **DEFENDER FOR CLOUD → postura de segurança + recomendações + proteção contra ameaças**
