## Regiões

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

## Descrever zonas de disponibilidade

<p align="justify">Zonas de disponibilidade são datacenters separados fisicamente dentro de uma região do Azure. Cada zona de disponibilidade é composta de um ou mais datacenters equipados com energia, resfriamento e rede independentes. Uma zona de disponibilidade é configurada para ser um limite de isolamento. Se uma zona ficar inativa, as outras continuarão funcionando. Zonas de disponibilidade são conectadas por meio de redes de fibra óptica privadas de alta velocidade.</p>

<p align="justify">Pode usar as zonas de disponibilidade para executar aplicativos críticos e incorporar alta disponibilidade à arquitetura do aplicativo, colocalizando seus recursos de computação, armazenamento, rede e dados em uma zona de disponibilidade e replicando em outras zonas de disponibilidade.</p>

<p align="justify">As zonas de disponibilidade são destinadas, principalmente, a VMs, discos gerenciados, balanceadores de carga e bancos de dados SQL. Os serviços do Azure que dão suporte às zonas de disponibilidade enquadram-se em três categorias:</p>

- **Serviços em zonas:** você fixa o recurso a uma zona específica (por exemplo, VMs, discos gerenciados, endereços IP).

- **Serviços com redundância de zona:** a plataforma replica automaticamente entre zonas (por exemplo, armazenamento com redundância de zona, Banco de Dados SQL).

- **Serviços não regionais:** os serviços estão sempre disponíveis em geografias do Azure e são resilientes a interrupções em toda a zona, bem como a interrupções em toda a região.

## Descrever os datacenters do Azure

<p align="justify">Os datacenters do Azure são instalações físicas em todo o mundo que são projetadas para hospedar servidores, armazenamento, redes e outros componentes de infraestrutura de nuvem do Azure. Cada datacenter do Azure é composto por milhares de servidores, roteadores, switches e outros equipamentos de rede, e é gerenciado por uma equipe de técnicos especializados em datacenters.</p>

## Descrever os recursos e grupos de recursos do Azure


- **Recursos do Azure:** são os componentes de infraestrutura que constituem os serviços do Azure. Isso pode incluir, por exemplo, máquinas virtuais, bancos de dados, armazenamento, redes, entre outros. Cada recurso do Azure é identificado por um nome exclusivo e uma ID de recurso.

- **Grupos de recursos do Azure:** são containers lógicos que permitem gerenciar todos os recursos relacionados a um determinado aplicativo, solução ou ambiente. É possível adicionar, modificar ou excluir recursos dentro de um grupo de recursos sem afetar os outros grupos de recursos. Os grupos de recursos também permitem que você gerencie permissões e acesso para usuários e grupos específicos.

<p align="justify">Os grupos de recursos no Azure proporcionam uma maneira eficiente de organizar e gerenciar seus recursos de forma estruturada. Eles permitem que você agrupe recursos com base em aplicativos, ambientes, soluções ou departamentos, facilitando o gerenciamento e a administração.</p>

<p align="justify">Com um gerenciamento centralizado, você pode provisionar, monitorar, configurar e desativar vários recursos a partir de um único local. Além disso, os grupos de recursos oferecem controle de acesso granular, permitindo que você defina permissões específicas para usuários e grupos, restringindo o acesso apenas aos recursos necessários.</p>

<p align="justify">Essa abordagem também simplifica o faturamento, permitindo que todos os recursos associados a um aplicativo ou solução sejam agrupados em um único item de faturamento, facilitando o gerenciamento de custos e a visualização das despesas.</p>

## Descrever assinaturas

<p align="justify">Uma assinatura do Azure é uma conta que fornece acesso aos serviços e recursos do Azure. Ao criar uma assinatura do Azure, você pode provisionar e gerenciar recursos do Azure, como máquinas virtuais, bancos de dados, armazenamento, redes, entre outros. Uma assinatura do Azure também permite que você gerencie permissões e acesso para usuários e grupos específicos.
</p>
<p align="justify">As assinaturas do Azure permitem que você gerencie e <u>controle os custos</u> dos serviços do Azure, incluindo monitoramento e faturamento em tempo real, além de permitir que você gerencie vários recursos do Azure em um único local, incluindo provisionamento, monitoramento, configuração e desativação.</p>

<p align="justify">Permitem que você aumente ou diminua o uso dos serviços do Azure com base nas necessidades do seu negócio, experimente e teste novos serviços e recursos do Azure antes de decidir se deseja implementá-los em escala.</p>

## Descrever grupos de gerenciamento (Management Group)

<p align="justify">A hierarquia de grupos de recursos, assinaturas e grupos de gerenciamento do Azure é um modelo de organização e gerenciamento de recursos de nuvem do Azure em diferentes níveis de abstração e escopo. Essa hierarquia é composta por grupos de gerenciamento, assinaturas e grupos de recursos.</p>

<p align="justify">Os grupos de gerenciamento são uma hierarquia de objetos que ajudam a gerenciar o acesso, a conformidade e a governança em grande escala no Azure. Eles permitem que você gerencie várias assinaturas do Azure como uma única entidade e aplique políticas e controles em toda a sua organização. Os grupos de gerenciamento do Azure permitem que você organize recursos do Azure em uma estrutura hierárquica com vários níveis, semelhante a uma árvore.</p>