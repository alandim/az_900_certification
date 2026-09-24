## Serviços de computação do Azure

<p align="justify">A <strong>Computação do Azure</strong> fornece recursos de computação sob demanda, como processadores, memória, armazenamento, rede e sistemas operacionais. Esses recursos podem ser utilizados para executar aplicações, serviços e cargas de trabalho na nuvem.</p>

<h3><strong style='color: skyblue'>Máquinas Virtuais</strong></h3>

<p align="justify">O <strong>Azure Virtual Machines (VMs)</strong> permite criar e gerenciar máquinas virtuais na nuvem, possibilitando executar aplicações e serviços como se estivessem em um ambiente local.</p>

<p align="justify">As VMs são uma oferta de <strong>IaaS (Infraestrutura como Serviço)</strong> e fornecem um servidor virtualizado sobre o qual você possui um alto nível de controle. É possível escolher o sistema operacional, instalar softwares e configurar o ambiente de acordo com as necessidades da aplicação.</p>

<p align="justify">As VMs são uma boa opção quando você precisa de:</p>

- Controle sobre o sistema operacional.
- Capacidade de instalar e executar softwares personalizados.
- Configurações específicas de hardware e software.
- Migração de aplicações existentes para a nuvem sem grandes alterações.

<p align="justify">Uma VM oferece a flexibilidade da virtualização sem a necessidade de comprar ou manter o hardware físico. No entanto, como é uma oferta de IaaS, o cliente continua responsável pelo sistema operacional e pelo software executado na VM, incluindo configuração, atualizações e manutenção.</p>

### Conjuntos de Dimensionamento de Máquinas Virtuais

<p align="justify">Os <strong>Conjuntos de Dimensionamento de Máquinas Virtuais (Virtual Machine Scale Sets – VMSS)</strong> permitem criar e gerenciar um grupo de VMs idênticas de maneira centralizada.</p>

<p align="justify">O número de instâncias pode aumentar ou diminuir automaticamente de acordo com a demanda ou seguir uma programação definida. Isso permite que a capacidade computacional seja ajustada conforme a necessidade da aplicação.</p>

<p align="justify">Os conjuntos de dimensionamento também podem trabalhar com balanceamento de carga, distribuindo o tráfego entre as instâncias disponíveis.</p>

> **AZ-900:** VMSS = várias VMs + gerenciamento centralizado + escalabilidade.

### Conjuntos de Disponibilidade

<p align="justify">Os <strong>Conjuntos de Disponibilidade (Availability Sets)</strong> ajudam a aumentar a disponibilidade e a resiliência das VMs, distribuindo-as entre diferentes domínios de falha e de atualização.</p>

<p align="justify">O objetivo é evitar que todas as VMs de uma aplicação sejam afetadas simultaneamente por uma falha física ou por uma manutenção planejada.</p>

#### Domínio de atualização

<p align="justify">Um <strong>domínio de atualização</strong> agrupa VMs que podem ser reiniciadas juntas durante uma manutenção planejada. As atualizações são aplicadas a um domínio por vez, mantendo os demais domínios disponíveis.</p>

#### Domínio de falha

<p align="justify">Um <strong>domínio de falha</strong> agrupa VMs que compartilham componentes físicos, como uma fonte de energia ou um switch de rede. Distribuir as VMs entre diferentes domínios de falha ajuda a reduzir o impacto de uma falha física.</p>

> **AZ-900:**  
> **Domínio de atualização → manutenção planejada**  
> **Domínio de falha → falha física**

<p align="justify">As VMs são especialmente adequadas para aplicações que exigem maior controle sobre o ambiente de execução, como aplicações empresariais, bancos de dados e cargas de trabalho que dependem de configurações específicas do sistema operacional.</p>


<h3><strong style='color: skyblue'>Área de Trabalho Virtual do Azure</strong></h3>

<p align="justify">A <strong>Área de Trabalho Virtual do Azure (Azure Virtual Desktop – AVD)</strong> é um serviço de virtualização de desktops e aplicativos executado no Azure.</p>

<p align="justify">Ele permite que os usuários acessem desktops e aplicativos Windows remotamente, utilizando diferentes dispositivos e locais.</p>

<p align="justify">Com o Azure Virtual Desktop, as organizações podem fornecer ambientes de trabalho virtuais de forma centralizada, permitindo que sistemas operacionais, aplicativos e dados sejam disponibilizados aos usuários sem depender exclusivamente do computador local.</p>

<p align="justify">O serviço é especialmente útil para cenários de trabalho remoto, trabalho híbrido, acesso centralizado a aplicativos e disponibilização de desktops para diferentes grupos de usuários.</p>

> **AZ-900:** AVD = desktops e aplicativos Windows virtualizados na nuvem.


<h3><strong style='color: skyblue'>Contêineres</strong></h3>

<p align="justify">Os <strong>contêineres</strong> fornecem um ambiente isolado para executar aplicações e suas dependências. Diferentemente das máquinas virtuais, os contêineres compartilham o sistema operacional do host, tornando-os geralmente mais leves e rápidos para iniciar.</p>

<p align="justify">Eles são projetados para serem criados, iniciados, interrompidos e dimensionados rapidamente, sendo adequados para aplicações modernas e arquiteturas baseadas em microsserviços.</p>

<p align="justify">Uma arquitetura de <strong>microsserviços</strong> divide uma aplicação em pequenos serviços independentes, que podem ser desenvolvidos, implantados e dimensionados separadamente.</p>


### Instâncias de Contêiner do Azure

<p align="justify">As <strong>Instâncias de Contêiner do Azure (Azure Container Instances – ACI)</strong> fornecem uma maneira rápida e simples de executar contêineres no Azure sem a necessidade de gerenciar máquinas virtuais ou uma infraestrutura de orquestração.</p>

<p align="justify">O ACI é uma oferta de <strong>PaaS (Plataforma como Serviço)</strong> e é adequado principalmente para executar contêineres individuais de maneira rápida e simples.</p>

> **AZ-900:** ACI = executar contêiner rapidamente, sem gerenciar VMs.


### Aplicativos de Contêiner do Azure

<p align="justify">Os <strong>Aplicativos de Contêiner do Azure (Azure Container Apps)</strong> permitem executar aplicações baseadas em contêiner sem a necessidade de gerenciar diretamente a infraestrutura subjacente.</p>

<p align="justify">Além da execução dos contêineres, o serviço oferece recursos como dimensionamento automático, balanceamento de carga e suporte a aplicações baseadas em microsserviços.</p>

<p align="justify">Assim como o ACI, o Azure Container Apps é uma oferta de <strong>PaaS</strong>, porém é direcionado a aplicações em contêiner que precisam de recursos adicionais de hospedagem e escalabilidade.</p>

> **AZ-900:** Container Apps = aplicações em contêiner + escalabilidade + menos gerenciamento de infraestrutura.


<h3><strong style='color: skyblue'>Kubernetes</strong></h3>

<p align="justify">O <strong>Azure Kubernetes Service (AKS)</strong> é um serviço de orquestração de contêineres baseado em Kubernetes.</p>

<p align="justify">Um orquestrador de contêineres automatiza e gerencia o ciclo de vida de contêineres, incluindo implantação, escalabilidade, disponibilidade e gerenciamento de workloads.</p>

<p align="justify">O AKS é especialmente útil quando uma organização precisa gerenciar uma grande quantidade de contêineres ou aplicações distribuídas e necessita de recursos avançados de orquestração.</p>

### Comparação

| Serviço | Principal objetivo |
|---|---|
| **Azure Container Instances (ACI)** | Executar contêineres de forma simples e rápida |
| **Azure Container Apps** | Executar aplicações em contêiner com escalabilidade e menos gerenciamento |
| **Azure Kubernetes Service (AKS)** | Orquestrar e gerenciar contêineres em escala |

> **AZ-900:**  
> **ACI → contêiner simples**  
> **Container Apps → aplicação em contêiner**  
> **AKS → orquestração**


<h3><strong style='color: skyblue'>Funções</strong></h3>

<p align="justify">O <strong>Azure Functions</strong> é um serviço de computação <strong>serverless</strong> e orientado a eventos, que permite executar pequenos trechos de código em resposta a eventos sem a necessidade de gerenciar a infraestrutura.</p>

<p align="justify">Uma função pode ser acionada por diferentes tipos de eventos, como:</p>

- Requisições HTTP.
- Temporizadores.
- Mensagens.
- Eventos gerados por outros serviços do Azure.

<p align="justify">O Azure Functions é adequado para aplicações que precisam executar tarefas específicas em resposta a eventos e que podem se beneficiar da escalabilidade automática.</p>

<p align="justify">As funções podem ser <strong>sem estado</strong> ou <strong>com estado</strong>. Nas funções sem estado, cada execução é independente. Com <strong>Durable Functions</strong>, é possível manter informações sobre o estado e coordenar execuções de funções em fluxos de trabalho mais complexos.</p>

> **AZ-900:** Functions = código + evento + serverless.


## Serviços de Aplicativo do Azure

<h3><strong style='color: skyblue'>Serviço de Aplicativo</strong></h3>

<p align="justify">O <strong>Serviço de Aplicativo do Azure (Azure App Service)</strong> é uma plataforma <strong>PaaS</strong> totalmente gerenciada para criar, implantar, hospedar e dimensionar aplicações.</p>

<p align="justify">O serviço permite que você se concentre no desenvolvimento e na execução da aplicação, enquanto o Azure gerencia a infraestrutura subjacente.</p>

<p align="justify">O Azure App Service é um serviço baseado em HTTP utilizado principalmente para hospedar:</p>

- Aplicações Web.
- APIs REST.
- Back-ends de aplicações móveis.

<p align="justify">O serviço oferece suporte a diversas linguagens e frameworks, incluindo .NET, Java, Node.js, PHP, Python e Ruby, além de ambientes Windows e Linux.</p>

<p align="justify">Entre os recursos disponíveis estão escalabilidade, integração com sistemas de implantação, autenticação e autorização, domínios personalizados e certificados.</p>

> **AZ-900:** App Service = hospedar Web Apps e APIs sem gerenciar diretamente a infraestrutura.
