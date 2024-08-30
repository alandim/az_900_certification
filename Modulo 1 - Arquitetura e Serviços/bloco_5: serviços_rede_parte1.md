## Serviços de computação do Azure

<p align="justify">A Computação do Azure é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais.</p>

### Máquinas Virtuais 
<p align="justify">No Microsoft Azure, existem diferentes opções para a computação, incluindo instâncias de contêiner, máquinas virtuais (VMs) e funções.</p>

<p align="justify">O Azure fornece o Azure Virtual Machines para criar e gerenciar VMs permitindo executar aplicativos e serviços como se estivessem em um ambiente local. As VMs do Azure oferecem alta disponibilidade, escalabilidade, desempenho e segurança.</p>

<p align="justify">As VMs podem ser personalizadas para atender às necessidades específicas dos aplicativos e suportam uma ampla variedade de sistemas operacionais e linguagens de programação.</p>

<p align="justify">As VMs fornecem IaaS (infraestrutura como serviço) na forma de um servidor virtualizado e podem ser usadas de várias maneiras. Como em um computador físico, você pode personalizar todos os programas de software em execução na VM. As VMs são uma opção ideal quando você precisa de:</p>

- Controle total sobre o SO (sistema operacional).
- Capacidade para executar um software personalizado.
- Usar configurações personalizadas de hospedagem.

<p align="justify">Uma VM do Azure oferece a flexibilidade da virtualização sem a necessidade de comprar e manter o hardware físico que a executa. No entanto, como uma oferta de IaaS, você ainda precisa configurar, atualizar e manter o software executado na VM.</p>
 
<p align="justify">As VMs são adequadas para aplicativos que exigem mais controle sobre o ambiente de execução e onde a portabilidade não é uma preocupação. As VMs são comumente usadas para hospedar aplicativos empresariais, bancos de dados e aplicativos de computação intensiva.</p>

### Funções

<p align="justify">
São uma opção de computação sem servidor, onde o código é executado em resposta a eventos, sem a necessidade de provisionar e gerenciar servidores. As funções são escaláveis, cobradas com base no uso e são adequadas para cenários em que as cargas de trabalho são intermitentes ou variáveis. O Azure fornece o Azure Functions, que permite criar e executar funções facilmente.
</p>

### Contêineres
<p align="justify">
O Azure Container Instances é um serviço de computação sem servidor do Microsoft Azure que permite executar contêineres de maneira rápida e simples, sem a necessidade de provisionar ou gerenciar máquinas virtuais subjacentes. Ele fornece um ambiente isolado e sob demanda para a execução de contêineres baseados em Docker.
</p>

<p align="justify">Os Aplicativos de Contêiner do Azure são semelhantes, em muitos aspectos, a uma instância de contêiner. Eles permitem que você comece a trabalhar imediatamente, removem a parte de gerenciamento de contêineres e são uma oferta de PaaS. Os Aplicativos de Contêiner têm benefícios extras, como a capacidade de incorporar balanceamento de carga e colocação em escala. Essas outras funções permitem que você seja mais flexível em seu design.</p>

<p align="justify">O Serviço de Kubernetes do Azure (AKS) é um serviço de orquestração de contêiner. Um serviço de orquestração gerencia o ciclo de vida dos contêineres. Quando você está implantando uma frota de contêineres, o AKS pode tornar o gerenciamento de frota mais simples e eficiente.</p>

<p align="justify">Contêineres geralmente são usados para criar soluções que utilizam uma arquitetura de microsserviço. Essa arquitetura é onde você divide as soluções em partes menores e independentes. </p>

<p align="justify">Resumindo, é melhor usar o Azure Container Instances quando você precisa de uma execução rápida e simples de contêineres isolados, especialmente em cargas de trabalho de curta duração ou tarefas pontuais. Por outro lado, o Azure Kubernetes Service é mais adequado para cargas de trabalho complexas e escaláveis, onde você precisa de recursos avançados de orquestração, gerenciamento e escalabilidade automática.
</p>