fy">
<strong style="color: gray;">Computação em nuvem (ou "cloud computing")</strong> é um modelo de entrega de serviços de TI onde os recursos, como servidores, armazenamento, bancos de dados, rede, software, e muito mais, são disponibilizados pela internet ("a nuvem") de forma rápida, e acessados sob demanda, pagando apenas pelo que usam.
</p>

<p>Os principais atributos da computação em nuvem:</p>

1. Baseado em serviço
2. Escalável/Elástico
3. Compartilhado
4. Medido por uso
5. Baseado na Internet

## Modelo de responsabilidade compartilhada

<p align="justify">O <strong style="color: gray;">modelo de responsabilidade compartilhada</strong> define que tanto o provedor de serviços em nuvem quanto o cliente compartilham a responsabilidade pela segurança e conformidade dos dados e sistemas hospedados na nuvem.
</p>

1. Você sempre será responsável por:

    * As informações e dados armazenados na nuvem
    * Dispositivos que podem se conectar à sua nuvem
    * As contas e identidades das pessoas, serviços e dispositivos em sua organização

2. O provedor de nuvem é sempre responsável por:
      * O datacenter físico
      * A rede física
      * Os hosts físicos

3. Seu modelo de serviço determinará a responsabilidade por coisas como:
    * Sistemas operacionais
    * controle de rede
    * formulários
    * identidade e infraestrutura

<p align="center">
  <img src="https://learn.microsoft.com/pt-br/training/wwl-azure/describe-cloud-compute/media/shared-responsibility-b3829bfe.svg" alt="Texto alternativo" width="2000" height="400">
</p>


## Modelos de Nuvem

<p align="justify">Os modelos de nuvem são as formas como as empresas podem utilizar a computação em nuvem para atender às suas necessidades de negócios. Os principais modelos de nuvem são: <strong style="color: gray;">pública, privada e híbrida.</strong></p>

1. **Nuvem Pública:** 

<p align="justify">As nuvens públicas são a maneira mais comum de implantação da computação em nuvem. Os recursos de nuvem (como servidores e armazenamento) pertencem a um provedor de serviço de nuvem terceirizado, são operados por ele e entregues pela Internet. Com uma nuvem pública, todo o hardware, software e outras infraestruturas de suporte são de propriedade do provedor de nuvem e gerenciadas por ele.

<p align="justify">Em uma nuvem pública, você compartilha os mesmos dispositivos de hardware, de armazenamento e de rede com outras organizações ou "locatários" da nuvem e acessa serviços e gerencia sua conta usando um navegador da Web. As implantações de nuvem pública geralmente são usadas para fornecer email baseado na Web, aplicativos de escritório online, armazenamento e ambientes de desenvolvimento e teste.

Vantagens: Redução de custos, sem manutenção, escalabilidade e alta confiabilidade.

2. **Nuvem Privada:** 

<p align="justify">Uma nuvem privada consiste em recursos de computação em nuvem usados exclusivamente por uma única empresa ou organização. A nuvem privada pode estar localizada fisicamente no datacenter local da sua organização ou pode ser hospedada por um provedor de serviços terceirizado. Mas em uma nuvem privada, os serviços e a infraestrutura são sempre mantidos na rede privada e o hardware e o software são dedicados unicamente à sua organização.

<p align="justify">Dessa forma, com a nuvem privada é mais fácil para que a organização personalize seus recursos a fim de atender a requisitos de TI específicos. As nuvens privadas geralmente são usadas por órgãos governamentais, instituições financeiras e outras organizações de grande porte com operações críticas para os negócios, que buscam melhorar o controle sobre seu ambiente.

<p align="justify">Vatangens: Maior flexibilidade, controle e escalabilidade, segurança aprimorada.

3. **Nuvem Híbrida:** 

<p align="justify">Uma nuvem híbrida é um ambiente de computação que combina um datacenter local (também chamado de nuvem privada) com uma nuvem pública, permitindo que dados e aplicativos sejam compartilhados entre eles. 

<p align="justify">Uma nuvem híbrida permite que você use os
benefícios da computação em nuvem, além de poder controlar completamente um ambiente seguro usando seu próprio equipamento
para atender aos requisitos de segurança e conformidade. 

<p align="justify">Muitas organizações adotam a abordagem de nuvem híbrida devido a exigências comerciais, por exemplo, para atender a requisitos regulatórios e de soberania de dados, aproveitar ao máximo o investimento em tecnologia local ou lidar com problemas envolvendo latência baixa.

Vantagens: Controle, flexibilidade, custo-benefício e facilidade.

## Comparação entre CapEx VS OpEx

<p align="justify"><strong style="color: gray;">CapEx</strong> realiza o gasto incial na infraestrutura física tendo um valor que é reduzido ao longo do tempo, como máquinas, equipamentos, edifícios e infraestrutura de tecnologia.</p>

<p align="justify"><strong style="color: gray;">OpEx</strong> se refere aos gastos operacionais refere-se a um tipo de gasto que se destina a financiar as atividades cotidianas de uma empresa, como salários, aluguéis, energia elétrica, serviços de internet, entre outros.</p>

## Modelo baseado em Consumo

<p align="justify"><strong style="color: gray;">O modelo baseado no consumo</strong>, também conhecido como "pay-as-you-go", é um modelo de cobrança em que os clientes pagam apenas pelos recursos de nuvem que usam. Em outras palavras, os clientes pagam com base no consumo de recursos, como armazenamento, processamento e transferência de dados.</p>

<p align="justify">O modelo baseado no consumo oferece uma maneira flexível e econômica de usar recursos de nuvem, o que pode ser uma opção atraente para empresas que precisam de escalabilidade ou que desejam experimentar a nuvem sem se comprometer com a compra de recursos de nuvem fixos.</p>


<h1 align="center" style="border: none;"> Bloco 2 - Benefícios da Nuvem</h1>

## Alta disponibilidade na nuvem
<p align="justify">Refere-se à capacidade de manter um serviço ou aplicativo em execução sem interrupções, mesmo em caso de falhas de hardware ou software. A alta disponibilidade ajuda a garantir que os usuários possam acessar os serviços e aplicativos quando precisarem.</p>

## Escalabilidade
<p align="justify">Refere-se à capacidade de um serviço ou aplicativo de lidar com o aumento da demanda sem comprometer seu desempenho. Isso é alcançado através da capacidade de aumentar ou diminuir rapidamente os recursos de computação.</p>

<p align="justify">A escala geralmente vem em duas variedades: vertical e horizontal. 

- A escala vertical se concentra em aumentar ou diminuir a capacidade dos recursos. 

- A escala horizontal é adição ou subtração do número de recursos.</p>
   


## Confiabilidade

<p align="justify">Resiliência é a capacidade que um sistema tem de se recuperar de falhas e continuar funcionando. Ela também é um dos pilares do Microsoft Azure Well-Architected Framework.</p>

<p align="justify">Devido ao design descentralizado, a nuvem naturalmente dá suporte a uma infraestrutura confiável e resiliente. Com um design descentralizado, a nuvem permite que você tenha recursos implantados em várias regiões do mundo. Com essa escala global, mesmo que ocorra um evento catastrófico em uma região, as outras regiões ainda estarão em funcionamento.</p>

## Previsibilidade

<p align="justify">A previsibilidade na nuvem permite que você avance com confiança. A previsibilidade pode se concentrar na previsibilidade de desempenho ou na previsibilidade de custo. Tanto a previsibilidade de desempenho quanto a de custo são bastante influenciadas pelo Microsoft Azure Well-Architected Framework.</p>

- A **previsibilidade de desempenho** se concentra em prever os recursos necessários para oferecer uma experiência positiva aos clientes. O dimensionamento automático, o balanceamento de carga e a alta disponibilidade são apenas alguns dos conceitos de nuvem que dão suporte.

- A **previsibilidade de custos** se concentra em prever o custo dos gastos com a nuvem. Com a nuvem, você pode acompanhar o uso de recursos em tempo real, monitorar os recursos para garantir a maior eficiência de uso possível e aplicar a análise de dados para encontrar padrões e tendências que ajudam a planejar melhor as implantações de recursos. 

## Segurança

<p align="justify">A maioria dos provedores de nuvem oferece proteção contra ameaças externas, como ataques de hackers, bem como proteção contra ameaças internas, como acesso não autorizado a dados.</p>

- **Segurança física:** A nuvem fornece segurança física avançada, com múltiplas camadas de proteção para seus data centers, incluindo câmeras de segurança, controles de acesso, sistemas de detecção de incêndio e outros recursos de segurança.

- **Segurança lógica:** A nuvem também oferece segurança lógica, incluindo criptografia de dados em repouso e em trânsito, detecção e prevenção de ameaças, e gerenciamento de identidades e acessos.

## Governança

<p align="justify">Os provedores de nuvem geralmente cumprem as regulamentações governamentais e da indústria. Isso significa que as empresas que lidam com dados regulamentados podem usar a nuvem sem se preocupar com a conformidade. 
</p>

## Gerenciamento

<p align="justify">A capacidade de gerenciamento se refere as boas práticas de implementação de nuvem em conformidade.</p>

- **Gerenciamento da nuvem:** diz respeito a gerenciar seus recursos de nuvem.
    - Escalar automaticamente a implantação de recursos com base na necessidade.
    - Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual.
    - Monitorar a integridade dos recursos e substituir automaticamente os recursos com falha.
    - Receber alertas automáticos com base em métricas configuradas, de modo a ficar ciente do desempenho em tempo real.
    
- **Gerenciamento na nuvem:** diz respeito à maneira de gerenciar seu ambiente de nuvem e seus recursos. 
    - Por meio de um portal da Web.
    - Usando uma interface de linha de comando.
    - Usando APIs.
    - Usando o PowerShell.

<h1 align="center" style="border: none;"> Bloco 3 - Tipos de Serviços</h1>

<p align="justify">Existem três modelos principais de serviço em nuvem: Software como Serviço (SaaS), Plataforma como Serviço (PaaS) e Infraestrutura como Serviço (IaaS).</p>

## Infraestrutura como Serviço (IaaS)

<p align="justify">A infraestrutura como serviço (IaaS) é um modelo de computação em nuvem que fornece aos usuários recursos de computação, armazenamento e rede em um ambiente virtualizado, permitindo que as empresas criem e gerencie sua própria infraestrutura de TI sem precisar investir em hardware físico. O Azure oferece vários serviços IaaS, como o Azure Virtual Machines, Azure Virtual Network e Azure Storage.</p>

<p align="justify">Vantagens da IaaS incluem a redução de custos, a escalabilidade, a flexibilidade e a agilidade na implementação de recursos de TI. Com a IaaS, as empresas podem provisionar recursos de TI conforme necessário e pagar apenas pelos recursos utilizados.</p>

<p align="justify">Os cenários comuns para a IaaS incluem a hospedagem de aplicativos, a hospedagem de sites, o armazenamento de dados, o backup e a recuperação de desastres, a execução de cargas de trabalho de alto desempenho e a execução de testes de software.</p>

- Hospedagem de aplicativos personalizados: se você precisa hospedar um aplicativo personalizado e quer ter controle total sobre a configuração e gerenciamento da infraestrutura subjacente, o IaaS pode ser a opção mais adequada.

- Armazenamento em nuvem: o IaaS pode ser utilizado para armazenar dados e arquivos de grande porte em um ambiente de nuvem escalável.


## Plataforma como Serviço (PaaS)

<p align="justify">É um modelo de computação em nuvem que fornece aos desenvolvedores um ambiente de execução para a criação, teste e implantação de aplicativos sem que seja necessário gerenciar a infraestrutura subjacente. Na PaaS, o provedor de nuvem gerencia as máquinas virtuais, redes, armazenamento e outros recursos, permitindo que os desenvolvedores se concentrem na construção do aplicativo.</p>

 <p align="justify">Em um cenário de PaaS, você não precisa se preocupar com o licenciamento nem com a aplicação de patch em sistemas operacionais e bancos de dados.</p>

<p align="justify">O PaaS é adequado para fornecer um ambiente de desenvolvimento completo sem a preocupação de manter toda a infraestrutura de desenvolvimento.</p>

- Desenvolvimento e implantação de aplicativos: o PaaS é uma opção adequada para equipes de desenvolvimento que desejam criar e implantar aplicativos com mais rapidez e facilidade, sem se preocupar com a configuração e gerenciamento da infraestrutura subjacente.

- Análise de dados: o PaaS pode ser usado para análise de dados em grande escala, permitindo que as empresas processem grandes quantidades de dados com facilidade e eficiência.

- IoT (Internet das Coisas): o PaaS pode ser utilizado para gerenciar e processar dados de dispositivos IoT em larga escala.


## Software como Serviço (SaaS) 

<p align="justify">É um modelo de entrega de software no qual um provedor de serviços hospeda aplicativos na nuvem e os disponibiliza aos usuários finais pela Internet. Em outras palavras, os usuários não precisam instalar, configurar ou gerenciar o software em seus próprios dispositivos; em vez disso, eles acessam a aplicação através de um navegador da web ou aplicativo cliente.</p>

- Aplicativos de produtividade: se você precisa de aplicativos comuns, como processadores de texto, planilhas e ferramentas de colaboração, o SaaS pode ser a opção mais adequada. 

<h1 align="center" style="border: none;"> Bloco 4 - Principais Componentes Arquitetônicos</h1>

## Tópico 1 - Regiões

<p align="justify">Cada região do Azure é um conjunto de data centers que estão estrategicamente localizados em diferentes partes do mundo. Essas regiões são conectadas por uma rede de alta velocidade, permitindo que os serviços e recursos do Azure sejam disponibilizados globalmente.</p>

Vantagens:

- Latência reduzida: Ao escolher uma região próxima aos seus usuários ou recursos, você pode reduzir a latência de rede e melhorar o desempenho dos aplicativos e serviços hospedados no Azure.

- Conformidade com regulamentações locais: As regiões do Azure são projetadas para atender a requisitos de conformidade específicos em diferentes países e regiões, permitindo que você mantenha seus dados e aplicativos em conformidade com as leis e regulamentos locais.

- Redundância e resiliência: Ao implantar seus recursos em regiões do Azure separadas geograficamente, você pode obter maior redundância e resiliência, garantindo a disponibilidade contínua de seus aplicativos e dados, mesmo em caso de falhas em uma região específica.

- Escalabilidade global: O Azure oferece a capacidade de dimensionar globalmente seus aplicativos e serviços, aproveitando várias regiões do Azure para atender a demandas de tráfego e carga de trabalho em diferentes partes do mundo.

