## Controle de Acesso baseado em Função (RBAC) do Azure

<p align="justify">O Azure fornece funções internas que descrevem regras de acesso comuns para os recursos de nuvem. Você também pode definir suas funções. Cada função tem um conjunto associado de permissões de acesso relacionadas a essa função. Quando você atribui indivíduos ou grupos a uma ou mais funções, eles recebem todas as permissões de acesso relacionadas.</p>

<p align="justify">Portanto, se você contratar um novo engenheiro e adicioná-lo ao grupo do RBAC do Azure para engenheiros, ele obterá automaticamente o mesmo acesso que os outros engenheiros do mesmo grupo do RBAC do Azure. Da mesma forma, se você adicionar outros recursos e apontar o RBAC do Azure para eles, todos nesse grupo do RBAC do Azure vão ter as permissões nos novos recursos, bem como nos recursos existentes.</p>

## Modelo de Confiança Zero

<p align="justify">O conceito de Zero Trust é uma abordagem de segurança cibernética que se baseia na premissa de que as organizações não devem confiar automaticamente em nenhum usuário, dispositivo ou rede, mesmo que já tenham acesso legítimo. Em vez disso, todas as solicitações de acesso devem ser verificadas e autenticadas antes de serem autorizadas. Isso significa que, em vez de confiar na segurança perimetral para proteger os recursos, como era comum no passado, o Zero Trust exige que as organizações criem um ambiente de segurança em camadas, onde cada solicitação de acesso é verificada e validada.</p>

## Defesa em Profundidade

<p align="justify">O objetivo da defesa em profundidade é proteger as informações e impedir que elas sejam roubadas por pessoas que não estejam autorizadas a acessá-las.
Uma estratégia de defesa em profundidade usa uma série de mecanismos para reduzir o avanço de um ataque que busca obter acesso não autorizado aos dados.</p>

<p align="left">
  <img src="https://learn.microsoft.com/pt-br/training/wwl-azure/describe-azure-identity-access-security/media/defense-depth-486afc12.png" width="300" height="200">
</p>

<p align="justify">Cada camada fornece proteção, de modo que se uma camada for violada, uma camada seguinte já estará em vigor para impedir a exposição adicional. Essa abordagem elimina a dependência de qualquer camada única de proteção. Ela desacelera um ataque e fornece informações de alerta sobre as quais as equipes de segurança podem agir, automática ou manualmente.</p>

- A camada de segurança física é a primeira linha de defesa para proteger o hardware de computação no datacenter.

- A camada de identidade e acesso controla o acesso à infraestrutura e ao controle de alterações.

- A camada de perímetro usa a proteção contra DDoS (ataque de negação de serviço distribuído) para filtrar ataques em grande escala antes que eles possam causar uma negação de serviço para os usuários.

- A camada de rede limita a comunicação entre recursos por meio de controles de acesso e segmentação.

- A camada de computação protege o acesso a máquinas virtuais.

- A camada de aplicativo ajuda a garantir que os aplicativos estejam seguros e livres de vulnerabilidades de segurança.

- A camada de dados controla o acesso aos dados corporativos e do cliente que você precisa proteger.

## Microsoft Defender para Nuvem

<p align="justify">O Defender para Nuvem é uma ferramenta de monitoramento para gerenciamento da postura de segurança e proteção contra ameaças. Ele monitora os seus ambientes de nuvem, locais, híbridos e de várias nuvens para fornecer diretrizes e notificações com o objetivo de fortalecer sua postura de segurança.</p>

<p align="justify">O Defender para Nuvem fornece as ferramentas necessárias para proteger seus recursos, acompanhar sua postura de segurança, proteger contra ataques cibernéticos e simplificar o gerenciamento de segurança. A implantação do Defender para Nuvem é fácil e já está integrada nativamente ao Azure.</p>