## Serviços de armazenamento do Azure

<p align="justify">O <strong>Armazenamento do Azure</strong> fornece serviços para armazenar diferentes tipos de dados na nuvem, como arquivos, objetos, discos e dados estruturados. O Azure oferece diferentes opções de armazenamento de acordo com o tipo de dado, frequência de acesso, desempenho, disponibilidade e necessidade de redundância.</p>

---

<h3><strong style='color: skyblue'>Comparar os serviços de armazenamento do Azure</strong></h3>

<p align="justify">Os principais serviços de armazenamento do Azure são <strong>Blob Storage, Azure Files, Queue Storage e Table Storage</strong>. Cada um é destinado a um tipo diferente de necessidade.</p>

### Azure Blob Storage

<p align="justify">O <strong>Azure Blob Storage</strong> é um armazenamento de objetos otimizado para grandes quantidades de dados não estruturados.</p>

<p align="justify">É utilizado para armazenar dados como imagens, vídeos, documentos, backups, arquivos de log e outros arquivos.</p>

<p align="justify">Os dados são armazenados como <strong>blobs</strong> dentro de <strong>containers</strong>.</p>

**Exemplos:**

- Imagens e vídeos.
- Documentos.
- Backups.
- Logs.
- Arquivos de grandes dimensões.
- Dados para aplicações distribuídas.

> **AZ-900:** Blob Storage → **objetos / dados não estruturados**.

---

### Azure Files

<p align="justify">O <strong>Azure Files</strong> fornece compartilhamentos de arquivos gerenciados na nuvem que podem ser acessados por diferentes máquinas virtuais, aplicações e sistemas.</p>

<p align="justify">Os compartilhamentos podem utilizar protocolos conhecidos, como <strong>SMB</strong> e <strong>NFS</strong>, dependendo da configuração e do tipo de compartilhamento.</p>

<p align="justify">É especialmente útil quando uma aplicação precisa de um <strong>compartilhamento de arquivos</strong> semelhante a um file server tradicional.</p>

**Exemplos:**

- Compartilhamento de arquivos entre VMs.
- Migração de um file server para a nuvem.
- Aplicações que precisam acessar arquivos por meio de um compartilhamento de rede.

> **AZ-900:** Azure Files → **compartilhamento de arquivos**.

---

### Azure Queue Storage

<p align="justify">O <strong>Azure Queue Storage</strong> fornece armazenamento de mensagens para permitir comunicação assíncrona entre componentes de uma aplicação.</p>

<p align="justify">Uma aplicação pode colocar uma mensagem em uma fila e outro componente pode processá-la posteriormente.</p>

**Exemplo:**

<pre>
Aplicação A
    │
    ▼
Queue Storage
    │
    ▼
Aplicação B
</pre>

<p align="justify">Isso permite desacoplar componentes e lidar melhor com cargas de trabalho que precisam ser processadas posteriormente.</p>

> **AZ-900:** Queue Storage → **mensagens / comunicação assíncrona**.

---

### Azure Table Storage

<p align="justify">O <strong>Azure Table Storage</strong> fornece um armazenamento NoSQL para dados estruturados que podem ser organizados em entidades.</p>

<p align="justify">É uma opção para aplicações que precisam armazenar grandes quantidades de dados estruturados sem utilizar um banco de dados relacional tradicional.</p>

> **AZ-900:** Table Storage → **dados estruturados NoSQL**.

---

### Comparação rápida

| Serviço | Principal finalidade | Exemplo |
|---|---|---|
| **Blob Storage** | Objetos / dados não estruturados | Imagens, vídeos, backups |
| **Azure Files** | Compartilhamento de arquivos | File server |
| **Queue Storage** | Mensagens | Processamento assíncrono |
| **Table Storage** | Dados estruturados NoSQL | Dados de aplicações |

> **DECORA:**  
> **Blob = objetos**  
> **Files = arquivos compartilhados**  
> **Queue = mensagens**  
> **Table = dados NoSQL**

---

<h3><strong style='color: skyblue'>Descrever os níveis de armazenamento</strong></h3>

<p align="justify">O Azure Blob Storage possui diferentes <strong>níveis de acesso (Access Tiers)</strong>. A escolha depende principalmente da frequência com que os dados são acessados e do custo que você está disposto a assumir para armazenamento e acesso.</p>

### Hot

<p align="justify">O nível <strong>Hot</strong> é destinado a dados acessados com frequência.</p>

- Maior custo de armazenamento.
- Menor custo de acesso em comparação aos níveis menos frequentes.
- Indicado para dados usados frequentemente.

**Exemplos:**

- Dados ativos de aplicações.
- Arquivos acessados frequentemente.
- Dados que precisam estar disponíveis para acesso recorrente.

> **Hot = acesso frequente.**

---

### Cool

<p align="justify">O nível <strong>Cool</strong> é destinado a dados acessados com pouca frequência, mas que ainda precisam estar disponíveis rapidamente quando forem necessários.</p>

- Menor custo de armazenamento que Hot.
- Custo de acesso maior que Hot.
- Indicado para dados acessados ocasionalmente.

**Exemplos:**

- Backups acessados ocasionalmente.
- Dados que precisam permanecer disponíveis, mas não são utilizados frequentemente.

> **Cool = acesso pouco frequente.**

---

### Cold

<p align="justify">O nível <strong>Cold</strong> é destinado a dados que são acessados com pouca frequência e precisam permanecer armazenados por períodos mais longos.</p>

- Custo de armazenamento menor que Cool.
- Custo de acesso maior.
- Indicado para dados raramente acessados.

> **Cold = acesso muito pouco frequente.**

---

### Archive

<p align="justify">O nível <strong>Archive</strong> é destinado a dados que raramente são acessados e que podem permanecer offline por um período antes de serem recuperados.</p>

- Menor custo de armazenamento.
- Maior custo de acesso.
- Os dados precisam ser reidratados antes de serem acessados.
- Indicado para arquivamento de longo prazo.

**Exemplos:**

- Arquivos históricos.
- Dados que precisam ser mantidos por requisitos de retenção.
- Backups antigos.
- Dados que raramente serão acessados.

> **AZ-900:** Archive = **menor custo de armazenamento + dados raramente acessados + recuperação não imediata**.

---

### Comparação dos níveis

| Nível | Frequência de acesso | Custo de armazenamento | Custo de acesso |
|---|---|---:|---:|
| **Hot** | Alta | Maior | Menor |
| **Cool** | Baixa | Menor | Maior |
| **Cold** | Muito baixa | Ainda menor | Ainda maior |
| **Archive** | Raríssima | Menor | Maior |

<pre>
Frequência de acesso

ALTA ───────────────────────────────► BAIXA

HOT → COOL → COLD → ARCHIVE

Armazenamento:
MAIOR ──────────────────────────────► MENOR

Acesso:
MENOR ──────────────────────────────► MAIOR
</pre>

> **PEGADINHA AZ-900:** Não escolha Archive simplesmente porque é "mais barato". Ele é adequado quando os dados são **raramente acessados** e podem tolerar o processo de recuperação.

---

<h3><strong style='color: skyblue'>Descrever as opções de redundância</strong></h3>

<p align="justify">A redundância do Azure Storage determina como os dados são replicados para aumentar a <strong>durabilidade e disponibilidade</strong>.</p>

### LRS — Locally Redundant Storage

<p align="justify">O <strong>LRS</strong> mantém várias cópias dos dados dentro de um único <strong>datacenter</strong>.</p>

- Proteção contra falhas de hardware dentro do datacenter.
- Menor custo entre as principais opções de redundância.
- Não protege contra a perda completa do datacenter.

> **LRS = várias cópias em um único datacenter.**

---

### ZRS — Zone-Redundant Storage

<p align="justify">O <strong>ZRS</strong> replica os dados de forma síncrona entre múltiplas <strong>zonas de disponibilidade</strong> dentro de uma região.</p>

- Protege contra falha de uma zona de disponibilidade.
- Os dados permanecem dentro da região.
- Maior resiliência que LRS contra falhas de uma zona.

> **ZRS = várias zonas dentro da mesma região.**

---

### GRS — Geo-Redundant Storage

<p align="justify">O <strong>GRS</strong> mantém os dados em uma região primária e replica os dados para uma <strong>região secundária</strong> geograficamente distante.</p>

- Protege contra uma falha que afete a região primária.
- A replicação para a região secundária é assíncrona.
- A região secundária normalmente não é usada para acesso de leitura até que seja habilitada a configuração apropriada.

> **GRS = região primária + região secundária.**

---

### GZRS — Geo-Zone-Redundant Storage

<p align="justify">O <strong>GZRS</strong> combina redundância entre zonas na região primária com replicação geográfica para uma região secundária.</p>

<pre>
Região Primária
 ├── Zona 1
 ├── Zona 2
 └── Zona 3
        │
        │ replicação geográfica
        ▼
Região Secundária
</pre>

<p align="justify">Ele combina proteção contra falhas de zona com proteção contra falhas regionais.</p>

> **GZRS = ZRS + replicação geográfica.**

---

### RA-GRS e RA-GZRS

<p align="justify">As opções <strong>RA-GRS</strong> e <strong>RA-GZRS</strong> permitem acesso de leitura aos dados replicados na região secundária.</p>

- **RA-GRS** = Read-Access Geo-Redundant Storage.
- **RA-GZRS** = Read-Access Geo-Zone-Redundant Storage.

> **RA = Read Access.**

---

### Comparação de redundância

| Opção | Onde ficam as cópias? | Proteção principal |
|---|---|---|
| **LRS** | Um datacenter | Falhas locais de hardware |
| **ZRS** | Múltiplas zonas na mesma região | Falha de uma zona |
| **GRS** | Região primária + secundária | Falha regional |
| **GZRS** | Múltiplas zonas + região secundária | Falha de zona + região |
| **RA-GRS** | GRS + leitura secundária | GRS + acesso de leitura |
| **RA-GZRS** | GZRS + leitura secundária | GZRS + acesso de leitura |

> **DECORA:**
>
> **LRS → Local**  
> **ZRS → Zones**  
> **GRS → Geo**  
> **GZRS → Geo + Zones**  
> **RA → Read Access**

---

<h3><strong style='color: skyblue'>Descrever as opções de conta de armazenamento</strong></h3>

<p align="justify">Uma <strong>conta de armazenamento do Azure</strong> fornece um namespace exclusivo para armazenar dados no Azure Storage.</p>

<p align="justify">A conta pode fornecer acesso a diferentes serviços de armazenamento, como Blob Storage, Azure Files, Queue Storage e Table Storage, dependendo do tipo de conta e dos recursos utilizados.</p>

### StorageV2 — General-purpose v2

<p align="justify">A conta <strong>General-purpose v2</strong> é a opção de uso geral recomendada para a maioria dos cenários modernos do Azure Storage.</p>

<p align="justify">Ela oferece suporte aos principais serviços de armazenamento e aos recursos modernos do Azure Storage.</p>

> **AZ-900:** General-purpose v2 = conta de armazenamento de uso geral.

---

### Premium Block Blob

<p align="justify">As contas <strong>Premium Block Blob</strong> são destinadas a cenários que exigem alto desempenho para armazenamento de blobs em blocos.</p>

> **Premium Block Blob → alto desempenho para Block Blobs.**

---

### Premium File Shares

<p align="justify">As contas <strong>Premium File Shares</strong> são destinadas a compartilhamentos de arquivos que precisam de alto desempenho.</p>

> **Premium File Shares → Azure Files com alto desempenho.**

---

### Premium Page Blobs

<p align="justify">As contas <strong>Premium Page Blob</strong> são destinadas a Page Blobs e cenários específicos de armazenamento baseado em páginas.</p>

> **Page Blob → páginas.**

---

### Tipos de blobs

<p align="justify">O Blob Storage possui diferentes tipos de blobs, cada um destinado a uma finalidade específica.</p>

| Tipo | Uso principal |
|---|---|
| **Block Blob** | Arquivos e dados gerais |
| **Append Blob** | Dados adicionados ao final, como logs |
| **Page Blob** | Dados organizados em páginas; usado, por exemplo, para discos VHD |

> **AZ-900:**  
> **Block Blob → arquivos gerais**  
> **Append Blob → anexar dados, como logs**  
> **Page Blob → páginas / VHD**

---

<h3><strong style='color: skyblue'>Identificar opções para mover arquivos</strong></h3>

<p align="justify">O Azure oferece diferentes ferramentas para copiar, sincronizar ou transferir arquivos entre ambientes locais e o Azure.</p>

### AzCopy

<p align="justify">O <strong>AzCopy</strong> é uma ferramenta de linha de comando otimizada para copiar dados de e para o Azure Storage.</p>

<p align="justify">É especialmente útil para transferências de grande volume e automação por scripts.</p>

**Exemplo conceitual:**

<pre>
Servidor local
      │
      │ AzCopy
      ▼
Azure Storage
</pre>

> **AZ-900:** AzCopy → **linha de comando para copiar dados**.

---

### Azure Storage Explorer

<p align="justify">O <strong>Azure Storage Explorer</strong> é uma aplicação gráfica que permite visualizar e gerenciar recursos de armazenamento do Azure.</p>

<p align="justify">Ele pode ser utilizado para trabalhar com blobs, arquivos, filas e tabelas por meio de uma interface gráfica.</p>

> **AZ-900:** Storage Explorer → **interface gráfica para gerenciar Storage**.

---

### Azure File Sync

<p align="justify">O <strong>Azure File Sync</strong> permite sincronizar um Windows Server local com um compartilhamento do <strong>Azure Files</strong>.</p>

<p align="justify">Ele possibilita manter arquivos disponíveis localmente enquanto utiliza o Azure Files como armazenamento centralizado.</p>

<pre>
Windows Server local
        │
        │ Azure File Sync
        ▼
    Azure Files
</pre>

<p align="justify">O recurso <strong>Cloud Tiering</strong> pode manter localmente apenas os arquivos acessados com maior frequência, enquanto arquivos menos acessados podem permanecer no Azure.</p>

> **AZ-900:** Azure File Sync → **sincronização entre Windows Server e Azure Files**.

---

### Comparação das ferramentas

| Ferramenta | Característica principal |
|---|---|
| **AzCopy** | Linha de comando para transferência |
| **Storage Explorer** | Interface gráfica para gerenciar Storage |
| **Azure File Sync** | Sincroniza Windows Server com Azure Files |

> **PEGADINHA:** Azure File Sync não é simplesmente uma ferramenta de "copiar arquivos". Seu objetivo principal é **sincronizar um servidor de arquivos com Azure Files**.

---

<h3><strong style='color: skyblue'>Descrever as opções de migração</strong></h3>

<p align="justify">O Azure oferece diferentes ferramentas para migrar servidores, aplicações e grandes volumes de dados para a nuvem.</p>

### Azure Migrate

<p align="justify">O <strong>Azure Migrate</strong> é um serviço utilizado para <strong>avaliar e migrar workloads</strong> para o Azure.</p>

<p align="justify">Ele pode ajudar a descobrir e avaliar ambientes existentes e planejar a migração de servidores, máquinas virtuais, bancos de dados e aplicações.</p>

<pre>
Ambiente local
      │
      │ Azure Migrate
      ▼
Avaliação
      │
      ▼
Planejamento
      │
      ▼
Migração para Azure
</pre>

> **AZ-900:** Azure Migrate → **avaliar e migrar workloads para o Azure**.

---

### Azure Data Box

<p align="justify">O <strong>Azure Data Box</strong> é utilizado para transferir grandes volumes de dados para o Azure utilizando um <strong>dispositivo físico</strong>.</p>

<p align="justify">Ele é especialmente útil quando transferir os dados pela rede seria muito demorado, difícil ou inviável.</p>

<pre>
Ambiente local
      │
      │ Dados
      ▼
Azure Data Box
      │
      │ envio físico
      ▼
Microsoft Azure
</pre>

<p align="justify">A ideia principal é utilizar um dispositivo físico para transportar os dados até o Azure, reduzindo a dependência de uma transferência de grande volume pela Internet.</p>

> **AZ-900:** Data Box → **grandes volumes de dados + dispositivo físico**.

---

### Azure Data Box vs Azure Migrate

| Serviço | Principal finalidade |
|---|---|
| **Azure Migrate** | Migrar servidores, aplicações e workloads |
| **Azure Data Box** | Transferir grandes volumes de dados usando dispositivo físico |

> **DECORA:**  
> **Migrate → workloads**  
> **Data Box → dados em dispositivo físico**

---

<h3><strong style='color: skyblue'>Mapa mental — Azure Storage</strong></h3>

<pre>
AZURE STORAGE
│
├── Serviços
│   ├── Blob
│   │   └── Objetos / arquivos
│   │
│   ├── Files
│   │   └── Compartilhamento de arquivos
│   │
│   ├── Queue
│   │   └── Mensagens
│   │
│   └── Table
│       └── NoSQL
│
├── Access Tiers
│   ├── Hot
│   │   └── Acesso frequente
│   ├── Cool
│   │   └── Acesso pouco frequente
│   ├── Cold
│   │   └── Acesso muito pouco frequente
│   └── Archive
│       └── Raríssimo / offline
│
├── Redundância
│   ├── LRS
│   │   └── Local
│   ├── ZRS
│   │   └── Zonas
│   ├── GRS
│   │   └── Geográfica
│   └── GZRS
│       └── Geo + Zonas
│
├── Ferramentas
│   ├── AzCopy
│   │   └── Linha de comando
│   ├── Storage Explorer
│   │   └── Interface gráfica
│   └── Azure File Sync
│       └── Windows Server ↔ Azure Files
│
└── Migração
    ├── Azure Migrate
    │   └── Workloads
    └── Azure Data Box
        └── Dados em dispositivo físico
</pre>

---

<h3><strong style='color: skyblue'>Resumo para a prova AZ-900</strong></h3>

| Se a questão falar sobre... | Pense em... |
|---|---|
| Armazenar objetos, imagens ou vídeos | **Blob Storage** |
| Compartilhamento de arquivos | **Azure Files** |
| Mensagens entre componentes | **Queue Storage** |
| NoSQL estruturado | **Table Storage** |
| Dados acessados frequentemente | **Hot** |
| Dados acessados ocasionalmente | **Cool** |
| Dados raramente acessados | **Cold** |
| Arquivamento de longo prazo | **Archive** |
| Cópias em um datacenter | **LRS** |
| Cópias em zonas | **ZRS** |
| Cópias em regiões diferentes | **GRS** |
| Geo + zonas | **GZRS** |
| Acesso de leitura à região secundária | **RA-GRS / RA-GZRS** |
| Copiar via linha de comando | **AzCopy** |
| Gerenciar Storage por interface gráfica | **Storage Explorer** |
| Sincronizar Windows Server com Azure Files | **Azure File Sync** |
| Avaliar/migrar servidores e workloads | **Azure Migrate** |
| Transferir grande volume de dados fisicamente | **Azure Data Box** |

> **🔥 DECORAÇÃO FINAL AZ-900**
>
> **BLOB → objeto**  
> **FILES → compartilhamento**  
> **QUEUE → mensagem**  
> **TABLE → NoSQL**
>
> **HOT → frequente**  
> **COOL → pouco frequente**  
> **COLD → muito pouco frequente**  
> **ARCHIVE → raríssimo**
>
> **LRS → local**  
> **ZRS → zonas**  
> **GRS → geográfico**  
> **GZRS → geográfico + zonas**
>
> **AzCopy → copiar**  
> **Storage Explorer → gerenciar**  
> **File Sync → sincronizar**  
> **Azure Migrate → migrar workloads**  
> **Data Box → transportar dados fisicamente**
