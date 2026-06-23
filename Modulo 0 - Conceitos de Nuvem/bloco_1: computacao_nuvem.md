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

4. **MultiCloud:** 
<p align="justify">Um quarto cenário, e cada vez mais provável, é um cenário multicloud. Em um cenário multicloud, você usa vários provedores de nuvem pública. Talvez você use recursos diferentes de provedores de nuvem diferentes. Ou talvez você tenha iniciado sua jornada na nuvem com um provedor e esteja em processo de migração para outro provedor. Independentemente disso, em um ambiente multicloud você lida com dois (ou mais) provedores de nuvem pública e gerencia recursos e segurança em ambos os ambientes.</p>


## Modelo baseado em Consumo

<p align="justify">A computação em nuvem opera em um modelo baseado no consumo. Você paga pelos recursos de TI que usa, e nada mais. Em vez de comprar e manter sua própria infraestrutura de datacenter, você aluga energia computacional e armazenamento e libera esses recursos quando terminar.</p>

<p align="justify">CapEx refere-se a gastos iniciais em infraestrutura física, como servidores, hardware de rede e espaço de datacenter. OpEx refere-se aos gastos contínuos com serviços ao longo do tempo. Como você paga por serviços em nuvem enquanto os consome, a computação em nuvem é classificada como uma despesa operacional.</p>
