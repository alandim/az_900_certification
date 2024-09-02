## Serviços de computação do Azure

<p align="justify">A Computação do Azure é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais.</p>

<h3><strong style='color: skyblue'>Máquina Virtual</strong></h3>

<p align="justify">O Azure fornece o Azure Virtual Machines para criar e gerenciar VMs permitindo executar aplicativos e serviços como se estivessem em um ambiente local. As VMs do Azure oferecem alta disponibilidade, escalabilidade, desempenho e segurança. As VMs podem ser personalizadas para atender às necessidades específicas dos aplicativos e suportam uma ampla variedade de sistemas operacionais e linguagens de programação.</p>

<p align="justify">As VMs fornecem IaaS (infraestrutura como serviço) na forma de um servidor virtualizado e podem ser usadas de várias maneiras. Como em um computador físico, você pode personalizar todos os programas de software em execução na VM. As VMs são uma opção ideal quando você precisa de:</p>

- Controle total sobre o SO (sistema operacional).
- Capacidade para executar um software personalizado.
- Usar configurações personalizadas de hospedagem.

<p align="justify">Uma VM do Azure oferece a flexibilidade da virtualização sem a necessidade de comprar e manter o hardware físico que a executa. No entanto, como uma oferta de IaaS, você ainda precisa configurar, atualizar e manter o software executado na VM.</p>
 
<p align="justify">Os <u>conjuntos de dimensionamento</u> permitem que você gerencie, configure e atualize centralmente um grande número de VMs em minutos. O número de instâncias de VM pode aumentar ou diminuir automaticamente em resposta à demanda ou você pode defini-lo para uma escala com base em uma agenda definida. Os conjuntos de dimensionamento de máquinas virtuais também implantam automaticamente um balanceador de carga para garantir que seus recursos estejam sendo usados com eficiência.</p>

<p align="justify">Os <u>conjuntos de disponibilidade</u> de máquinas virtuais são outra ferramenta para ajudá-lo a criar um ambiente mais resiliente e altamente disponível. Os conjuntos de disponibilidade foram projetados para garantir que as VMs escalonem atualizações e tenham conectividade de rede e energia variadas, impedindo que você perca todas as suas VMs com uma só falha de rede ou energia.</p>

<p>A disponibilidade atinge esses objetivos agrupando VMs de duas maneiras: atualizar domínio e domínio de falha.</p>

- **Domínio de atualização:** as VMs de grupos de domínio de atualização que podem ser reinicializadas ao mesmo tempo. Essa configuração permite aplicar atualizações sabendo que apenas um agrupamento de domínio de atualização está offline por vez. Todos os computadores em uma atualização de domínio de atualização. Um grupo de atualizações que passa pelo processo de atualização recebe um tempo de 30 minutos para se recuperar antes que a manutenção no próximo domínio de atualização seja iniciada.

- **Domínio de falha:** o domínio de falha agrupa suas VMs por origem de energia comum e comutador de rede. Por padrão, um conjunto de disponibilidade divide suas VMs em até três domínios de falha. Isso ajuda a proteger contra uma falha de energia física ou de rede, tendo VMs em diferentes domínios de falha (portanto, sendo conectadas a diferentes recursos de energia e rede).

<p align="justify">As VMs são adequadas para aplicativos que exigem mais controle sobre o ambiente de execução e onde a portabilidade não é uma preocupação. As VMs são comumente usadas para hospedar aplicativos empresariais, bancos de dados e aplicativos de computação intensiva.</p>

<h3><strong style='color: skyblue'>Área de Trabalho Virtual</strong></h3>

<p align="justify">A Área de Trabalho Virtual do Azure (Azure Virtual Desktop) é um serviço de virtualização de desktops totalmente gerenciado e baseado na nuvem. Ele permite que as organizações ofereçam acesso remoto seguro e otimizado a aplicativos e desktops virtuais a partir de qualquer dispositivo e em qualquer lugar do mundo.</p>

<p align="justify">Com a Área de Trabalho Virtual do Azure, os usuários podem acessar um ambiente de trabalho completo em nuvem, incluindo o sistema operacional, aplicativos, dados e configurações pessoais. Isso permite que eles tenham uma experiência de trabalho consistente, independentemente do dispositivo que estão usando. Além disso, as organizações podem provisionar e gerenciar desktops virtuais para seus usuários de forma centralizada, reduzindo custos e simplificando o gerenciamento de TI.
</p>

<h3><strong style='color: skyblue'>Contêineres</strong></h3>

<p align="justify">É uma opção de hospedagem de aplicativos para contêineres individuais. Ele permite executar contêineres sem a necessidade de gerenciar a infraestrutura subjacente. Ele oferece suporte a vários formatos de contêiner, como Docker e Open Container Initiative (OCI), e permite dimensionar horizontalmente seus contêineres.
</p>

<p align="justify">
Os contêineres são leves e projetados para serem criados, dimensionados e interrompidos dinamicamentepermitiindo que você responda às alterações sob demanda. Com contêineres, você pode reiniciar rapidamente se houver uma falha ou de uma interrupção de hardware. 
</p>

<p align="justify">As Instâncias de Contêiner do Azure oferecem a maneira mais rápida e simples de executar um contêiner no Azure, sem a necessidade de gerenciar máquinas virtuais nem adotar serviços adicionais. Instâncias de Contêiner do Azure são uma oferta de PaaS (plataforma como serviço).</p>

<p align="justify">Os Aplicativos de Contêiner do Azure são semelhantes, em muitos aspectos, a uma instância de contêiner. Eles permitem que você comece a trabalhar imediatamente, removem a parte de gerenciamento de contêineres e são uma oferta de PaaS. Os Aplicativos de Contêiner têm benefícios extras, como a capacidade de incorporar balanceamento de carga e colocação em escala.</p>

<p align="justify">Contêineres geralmente são usados para criar soluções que utilizam uma arquitetura de microsserviço. Essa arquitetura é onde você divide as soluções em partes menores e independentes. </p>

<h3><strong style='color: skyblue'>Kubernetes</strong></h3>

<p align="justify">O Serviço de Kubernetes do Azure (AKS) é um serviço de orquestração de contêiner. Um serviço de orquestração gerencia o ciclo de vida dos contêineres. Quando você está implantando uma frota de contêineres, o AKS pode tornar o gerenciamento de frota mais simples e eficiente.</p>


<p align="justify">Resumindo, é melhor usar o Azure Container Instances quando você precisa de uma execução rápida e simples de contêineres isolados, especialmente em cargas de trabalho de curta duração ou tarefas pontuais. Por outro lado, o Azure Kubernetes Service é mais adequado para cargas de trabalho complexas e escaláveis, onde você precisa de recursos avançados de orquestração, gerenciamento e escalabilidade automática.
</p>

<h3><strong style='color: skyblue'>Funções</strong></h3>

<p align="justify">
É uma plataforma de computação sem servidor que permite executar código em resposta a eventos. Ele é projetado para hospedar pequenos trechos de código que respondem a eventos, como acionadores de mensagens, acionadores de tempo ou acionadores HTTP. 
</p>

<p align="justify">É uma boa escolha para aplicativos que exigem escalabilidade automática e execução de tarefas pequenas e específicas em resposta a eventos. É uma opção popular para a criação de microsserviços e para a execução de tarefas em lotes.</p>

<p align="justify">As funções podem ser sem estado ou com estado. Quando eles são sem estado (o padrão), eles se comportam como se fossem reiniciados sempre que respondem a um evento. Quando são com estado (chamadas de Durable Functions), um contexto é passado pela função para acompanhar a atividade anterior.</p>
