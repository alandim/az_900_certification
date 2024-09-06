## Portal do Azure

<p align="justify">O Portal do Azure é uma interface gráfica baseada na web que permite gerenciar e monitorar recursos do Azure. Ele fornece uma visão geral de todos os serviços do Azure usados, permitindo que os usuários gerenciem os recursos, monitorem o uso e configurem as opções do serviço. O portal do Azure é altamente personalizável e pode ser usado para gerenciar qualquer serviço do Azure, independentemente de qual modelo de implantação (clássico ou Resource Manager) foi usado.</p>

## Azure Cloud Shell

<p align="justify">O Azure Cloud Shell é uma ferramenta de shell baseada em navegador que permite criar, configurar e gerenciar recursos do Azure usando um shell. O Azure Cloud Shell dá suporte ao Azure PowerShell e à CLI (Interface de Linha de Comando) do Azure, que é um shell bash.</p>

<p align="justify">Azure PowerShell é um módulo do PowerShell que permite aos usuários gerenciar recursos do Azure usando comandos do PowerShell. Ele oferece uma maneira poderosa e flexível de gerenciar recursos do Azure usando scripts e automatizar tarefas.</p>

<p align="justify">A CLI do Azure é funcionalmente equivalente ao Azure PowerShell, sendo a principal diferença a sintaxe dos comandos. Enquanto o Azure PowerShell usa comandos do PowerShell, a CLI do Azure usa comandos Bash.</p>

## Azure Arc 

<p align="justify">O Azure Arc é um serviço da Microsoft Azure que permite aos usuários gerenciar seus recursos em nuvem, no local e em ambientes multicloud, como Amazon Web Services (AWS) e Google Cloud Platform (GCP), usando uma única plataforma. O Azure Arc fornece uma única interface para gerenciar recursos em várias plataformas de nuvem, fornecendo visibilidade e controle unificados de todos os recursos.</p>

## Azure Resource Manager

<p align="justify">O ARM (Azure Resource Manager) é o serviço de implantação e gerenciamento do Azure. Ele fornece uma camada de gerenciamento que lhe permite criar, atualizar e excluir recursos em sua conta do Azure. Sempre que você faz qualquer coisa com seus recursos do Azure, o ARM está envolvido.</p>

<p align="justify">Quando um usuário envia uma solicitação de ferramentas, APIs ou SDKs do Azure, o ARM recebe a solicitação. O ARM se autentica e autoriza a solicitação. Então, o ARM envia a solicitação para o serviço do Azure, que executa a ação solicitada. Você vê resultados e recursos consistentes em todas as diferentes ferramentas porque todas as solicitações são tratadas por meio da mesma API.</p>

## Infraestrutura como código

<p align="justify">A infraestrutura como código é um conceito em que você gerencia sua infraestrutura como linhas de código. Em um nível introdutório, é como usar o Azure Cloud Shell, Azure PowerShell ou a CLI do Azure para gerenciar e configurar seus recursos. À medida que você fica mais confortável na nuvem, você pode usar a infraestrutura como conceito de código para gerenciar implantações inteiras usando modelos e configurações repetíveis. Os modelos do ARM e o Bicep são dois exemplos de como usar a infraestrutura como código com o Azure Resource Manager para manter seu ambiente.</p>

## Modelos de ARM

<p align="justify">Ao usar os modelos do ARM, você pode descrever os recursos que deseja usar em um formato JSON declarativo. Com um modelo do ARM, o código de implantação é verificado antes da execução de qualquer código. Isso garante que os recursos serão criados e conectados corretamente. Em seguida, o modelo orquestra a criação desses recursos em paralelo. Ou seja, se você precisar de 50 instâncias do mesmo recurso, todas as 50 instâncias serão criadas ao mesmo tempo.</p>

<p align="justify">O Bicep é uma linguagem que usa sintaxe declarativa para implantar recursos do Azure. Um arquivo Bicep define a infraestrutura e a configuração. Em seguida, o ARM implanta esse ambiente com base no arquivo Bicep. Embora semelhante a um modelo do ARM, que é escrito em JSON, os arquivos Bicep tendem a usar um estilo mais simples e conciso.</p>