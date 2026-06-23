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
<p>O modelo de responsabilidade compartilhada está fortemente ligado aos tipos de serviço em nuvem: infraestrutura como serviço (IaaS), plataforma como serviço (PaaS) e software como serviço (SaaS).</p>
<p>O diagrama a seguir destaca como o Modelo de Responsabilidade Compartilhada informa quem é responsável pelo que, dependendo do tipo de serviço na nuvem.</p>
<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-compute/media/shared-responsibility-model.png" alt="Texto alternativo" width="1000" height="500">
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

## Modelos de Nuvem

<p align="justify">Os modelos de nuvem são as formas como as empresas podem utilizar a computação em nuvem para atender às suas necessidades de negócios. Os principais modelos de nuvem são: <strong style="color: gray;">pública, privada e híbrida.</strong></p>
<p align="center">
  <img src="https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-compute/media/cloud-deployment-models.png" alt="Texto alternativo" width="1000" height="500">
</p>

1. **Nuvem Pública:** 

<p align="justify">As nuvens públicas são a maneira mais comum de implantação da computação em nuvem. Os recursos de nuvem (como servidores e armazenamento) pertencem a um provedor de serviço de nuvem terceirizado, são operados por ele e entregues pela Internet. Com uma nuvem pública, todo o hardware, software e outras infraestruturas de suporte são de propriedade do provedor de nuvem e gerenciadas por ele.

<p align="justify">Em uma nuvem pública, você compartilha os mesmos dispositivos de hardware, de armazenamento e de rede com outras organizações ou "locatários" da nuvem e acessa serviços e gerencia sua conta usando um navegador da Web. As implantações de nuvem pública geralmente são usadas para fornecer email baseado na Web, aplicativos de escritório online, armazenamento e ambientes de desenvolvimento e teste.

Vantagens: Redução de custos, sem manutenção, escalabilidade e alta confiabilidade.

2. **Nuvem Privada:** 

<p align="justify">Uma nuvem privada consiste em recursos de computação em nuvem usados exclusivamente por uma única empresa ou organização. A nuvem privada pode estar localizada fisicamente no datacenter local da sua organização ou pode ser hospedada por um provedor de serviços terceirizado. Mas em uma nuvem privada, os serviços e a infraestrutura são sempre mantidos na rede privada e o hardware e o software são dedicados unicamente à sua organização.

<p align="justify">Dessa forma, com a nuvem privada é mais fácil para que a organização personalize seus recursos a fim de atender a requisitos de TI específicos. As nuvens privadas geralmente são usadas por órgãos governamentais, instituições financeiras e outras organizações de grande porte com operações críticas para os negócios, que buscam melhorar o controle sobre seu ambiente.

<p align="justify">Vantagens: Maior flexibilidade, controle e escalabilidade, segurança aprimorada.

3. **Nuvem Híbrida:** 

<p align="justify">Uma nuvem híbrida é um ambiente de computação que combina um datacenter local (também chamado de nuvem privada) com uma nuvem pública, permitindo que dados e aplicativos sejam compartilhados entre eles. 

<p align="justify">Uma nuvem híbrida permite que você use os
benefícios da computação em nuvem, além de poder controlar completamente um ambiente seguro usando seu próprio equipamento
para atender aos requisitos de segurança e conformidade. 

<p align="justify">Muitas organizações adotam a abordagem de nuvem híbrida devido a exigências comerciais, por exemplo, para atender a requisitos regulatórios e de soberania de dados, aproveitar ao máximo o investimento em tecnologia local ou lidar com problemas envolvendo latência baixa.

Vantagens: Controle, flexibilidade, custo-benefício e facilidade.

4. **MultiCloud** 
<p>Um quarto cenário, e cada vez mais provável, é um cenário multicloud. Em um cenário multicloud, você usa vários provedores de nuvem pública. Talvez você use recursos diferentes de provedores de nuvem diferentes. Ou talvez você tenha iniciado sua jornada na nuvem com um provedor e esteja em processo de migração para outro provedor. Independentemente disso, em um ambiente multicloud você lida com dois (ou mais) provedores de nuvem pública e gerencia recursos e segurança em ambos os ambientes.</p>

## Comparação entre CapEx VS OpEx

<p align="justify"><strong style="color: gray;">CapEx</strong> realiza o gasto incial na infraestrutura física tendo um valor que é reduzido ao longo do tempo, como máquinas, equipamentos, edifícios e infraestrutura de tecnologia.</p>

<p align="justify"><strong style="color: gray;">OpEx</strong> se refere aos gastos operacionais refere-se a um tipo de gasto que se destina a financiar as atividades cotidianas de uma empresa, como salários, aluguéis, energia elétrica, serviços de internet, entre outros.</p>

## Modelo baseado em Consumo

<p align="justify"><strong style="color: gray;">O modelo baseado no consumo</strong>, também conhecido como "pay-as-you-go", é um modelo de cobrança em que os clientes pagam apenas pelos recursos de nuvem que usam. Em outras palavras, os clientes pagam com base no consumo de recursos, como armazenamento, processamento e transferência de dados.</p>

<p align="justify">O modelo baseado no consumo oferece uma maneira flexível e econômica de usar recursos de nuvem, o que pode ser uma opção atraente para empresas que precisam de escalabilidade ou que desejam experimentar a nuvem sem se comprometer com a compra de recursos de nuvem fixos.</p>
