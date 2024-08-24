* A certificação fornece uma visão geral do panorama da nuvem e da Azure, sendo um bom ponto de partida para especializações e desenvolvimento profissional;

* É necessário obter 700 pontos em um total de 1000 para passar no exame;

* O número de questões pode variar entre 35 e 50, com diferentes tipos de questões, como múltipla escolha, múltipla resposta, arrastar e soltar, sim e não;

* A duração do exame é de 45 minutos, mas o tempo de assento pode ser de 60 a 65 minutos;

* Os tópicos a serem abordados são sobre os fundamentos da computação em nuvem, os benefícios dos serviços em nuvem, os serviços principais da Azure, identidade, segurança, governança, precificação, ferramentas de gerenciamento e recursos da Azure;

<h1 align="center" style="border: none;"> Bloco 1 - Conceitos da Nuvem</h1>

## Definição

<p align="justify">
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



<h1 align="center" style="border: none;"> Bloco 4 - Principais Componentes Arquitetônicos</h1>

## Tópico 1 - Regiões

<p align="justify">Cada região do Azure é um conjunto de data centers que estão estrategicamente localizados em diferentes partes do mundo. Essas regiões são conectadas por uma rede de alta velocidade, permitindo que os serviços e recursos do Azure sejam disponibilizados globalmente.</p>

Vantagens:

- Latência reduzida: Ao escolher uma região próxima aos seus usuários ou recursos, você pode reduzir a latência de rede e melhorar o desempenho dos aplicativos e serviços hospedados no Azure.

- Conformidade com regulamentações locais: As regiões do Azure são projetadas para atender a requisitos de conformidade específicos em diferentes países e regiões, permitindo que você mantenha seus dados e aplicativos em conformidade com as leis e regulamentos locais.

- Redundância e resiliência: Ao implantar seus recursos em regiões do Azure separadas geograficamente, você pode obter maior redundância e resiliência, garantindo a disponibilidade contínua de seus aplicativos e dados, mesmo em caso de falhas em uma região específica.

- Escalabilidade global: O Azure oferece a capacidade de dimensionar globalmente seus aplicativos e serviços, aproveitando várias regiões do Azure para atender a demandas de tráfego e carga de trabalho em diferentes partes do mundo.


## Pares de Regiões

<p align="justify">Os pares de regiões do Azure são um conceito que se refere à associação de duas regiões do Azure, dentro da mesma área geográfica, em uma configuração de emparelhamento. Os datacenters dentro de um par de regiões são separados por centenas de quilômetros, o que ajuda a garantir a continuidade do negócio e a resiliência do aplicativo. Se ocorrer uma interrupção em uma região, o Azure pode redirecionar o tráfego para a outra região do par.</p>
<p align="justify">Cada região do par é designada como primária ou secundária. As regiões primárias são geralmente a primeira escolha para implantação de recursos, enquanto as regiões secundárias são usadas como backups em caso de falhas nas regiões primárias.
</p>
<p align="justify">A vantagem de utilizar pares de regiões do Azure é a capacidade de fornecer alta disponibilidade e resiliência para seus aplicativos e dados.</p>

## Regiões Soberanas

<p align="justify">As Regiões Soberanas do Azure são regiões geográficas isoladas que são designadas para oferecer serviços de nuvem exclusivos para entidades governamentais e organizações que precisam cumprir requisitos de soberania, conformidade e resiliência de dados específicos de um país ou região. Essas regiões são projetadas para fornecer controle e proteção adicionais aos dados sensíveis e críticos do governo ou de organizações com requisitos de conformidade rigorosos.</p>

## Tópico 2 - Descrever zonas de disponibilidade

<p align="justify">Zonas de disponibilidade são datacenters separados fisicamente dentro de uma região do Azure. Cada zona de disponibilidade é composta de um ou mais datacenters equipados com energia, resfriamento e rede independentes. Uma zona de disponibilidade é configurada para ser um limite de isolamento. Se uma zona ficar inativa, as outras continuarão funcionando. Zonas de disponibilidade são conectadas por meio de redes de fibra óptica privadas de alta velocidade.</p>

<p align="justify">Pode usar as zonas de disponibilidade para executar aplicativos críticos e incorporar alta disponibilidade à arquitetura do aplicativo, colocalizando seus recursos de computação, armazenamento, rede e dados em uma zona de disponibilidade e replicando em outras zonas de disponibilidade.</p>

<p align="justify">As zonas de disponibilidade são destinadas, principalmente, a VMs, discos gerenciados, balanceadores de carga e bancos de dados SQL. Os serviços do Azure que dão suporte às zonas de disponibilidade enquadram-se em três categorias:</p>

- **Serviços em zonas:** você fixa o recurso a uma zona específica (por exemplo, VMs, discos gerenciados, endereços IP).

- **Serviços com redundância de zona:** a plataforma replica automaticamente entre zonas (por exemplo, armazenamento com redundância de zona, Banco de Dados SQL).

- **Serviços não regionais:** os serviços estão sempre disponíveis em geografias do Azure e são resilientes a interrupções em toda a zona, bem como a interrupções em toda a região.

## Tópico 3 - Descrever os datacenters do Azure

<p align="justify">Os datacenters do Azure são instalações físicas em todo o mundo que são projetadas para hospedar servidores, armazenamento, redes e outros componentes de infraestrutura de nuvem do Azure. Cada datacenter do Azure é composto por milhares de servidores, roteadores, switches e outros equipamentos de rede, e é gerenciado por uma equipe de técnicos especializados em datacenters.</p>

## Tópico 4 - Descrever os recursos e grupos de recursos do Azure


- **Recursos do Azure:** são os componentes de infraestrutura que constituem os serviços do Azure. Isso pode incluir, por exemplo, máquinas virtuais, bancos de dados, armazenamento, redes, entre outros. Cada recurso do Azure é identificado por um nome exclusivo e uma ID de recurso.

- **Grupos de recursos do Azure:** são containers lógicos que permitem gerenciar todos os recursos relacionados a um determinado aplicativo, solução ou ambiente. É possível adicionar, modificar ou excluir recursos dentro de um grupo de recursos sem afetar os outros grupos de recursos. Os grupos de recursos também permitem que você gerencie permissões e acesso para usuários e grupos específicos.

<p align="justify">Os grupos de recursos no Azure proporcionam uma maneira eficiente de organizar e gerenciar seus recursos de forma estruturada. Eles permitem que você agrupe recursos com base em aplicativos, ambientes, soluções ou departamentos, facilitando o gerenciamento e a administração.</p>

<p align="justify">Com um gerenciamento centralizado, você pode provisionar, monitorar, configurar e desativar vários recursos a partir de um único local. Além disso, os grupos de recursos oferecem controle de acesso granular, permitindo que você defina permissões específicas para usuários e grupos, restringindo o acesso apenas aos recursos necessários.</p>

<p align="justify">Essa abordagem também simplifica o faturamento, permitindo que todos os recursos associados a um aplicativo ou solução sejam agrupados em um único item de faturamento, facilitando o gerenciamento de custos e a visualização das despesas.</p>

## Tópico 5 - Descrever assinaturas

<p align="justify">Uma assinatura do Azure é uma conta que fornece acesso aos serviços e recursos do Azure. Ao criar uma assinatura do Azure, você pode provisionar e gerenciar recursos do Azure, como máquinas virtuais, bancos de dados, armazenamento, redes, entre outros. Uma assinatura do Azure também permite que você gerencie permissões e acesso para usuários e grupos específicos.
</p>
<p align="justify">As assinaturas do Azure permitem que você gerencie e <u>controle os custos</u> dos serviços do Azure, incluindo monitoramento e faturamento em tempo real, além de permitir que você gerencie vários recursos do Azure em um único local, incluindo provisionamento, monitoramento, configuração e desativação.</p>

<p align="justify">Permitem que você aumente ou diminua o uso dos serviços do Azure com base nas necessidades do seu negócio, experimente e teste novos serviços e recursos do Azure antes de decidir se deseja implementá-los em escala.</p>

## Tópico 6 - Descrever grupos de gerenciamento (Management Group)

<p align="justify">A hierarquia de grupos de recursos, assinaturas e grupos de gerenciamento do Azure é um modelo de organização e gerenciamento de recursos de nuvem do Azure em diferentes níveis de abstração e escopo. Essa hierarquia é composta por grupos de gerenciamento, assinaturas e grupos de recursos.</p>

<p align="justify">Os grupos de gerenciamento são uma hierarquia de objetos que ajudam a gerenciar o acesso, a conformidade e a governança em grande escala no Azure. Eles permitem que você gerencie várias assinaturas do Azure como uma única entidade e aplique políticas e controles em toda a sua organização. Os grupos de gerenciamento do Azure permitem que você organize recursos do Azure em uma estrutura hierárquica com vários níveis, semelhante a uma árvore.</p>

<p align="justify"></p>
<p align="justify"></p>
<p align="justify"></p>
<p align="justify"></p>
<p align="justify"></p>
<p align="justify"></p>