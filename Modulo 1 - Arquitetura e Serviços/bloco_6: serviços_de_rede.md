## Serviços de rede do Azure

<p align="justify">Os <strong>serviços de rede do Azure</strong> permitem conectar recursos entre si, redes locais e a Internet. Eles fornecem recursos para criar redes privadas, controlar o tráfego, estabelecer conexões híbridas e resolver nomes de domínio.</p>

<h3><strong style='color: skyblue'>Rede Virtual do Azure</strong></h3>

<p align="justify">A <strong>Rede Virtual do Azure (Azure Virtual Network – VNet)</strong> é o bloco de construção fundamental para redes privadas no Azure. Ela permite que recursos do Azure, como máquinas virtuais, se comuniquem entre si, com a Internet e com redes locais.</p>

<p align="justify">Uma rede virtual fornece isolamento e permite definir o espaço de endereçamento IP utilizado pelos recursos. Dentro de uma VNet, é possível criar uma ou mais sub-redes para organizar os recursos e controlar o tráfego de rede.</p>

> **AZ-900:** VNet = rede privada no Azure.

### Sub-redes

<p align="justify">Uma <strong>sub-rede (subnet)</strong> é um intervalo de endereços IP dentro de uma rede virtual. Uma VNet pode ser dividida em várias sub-redes para organizar os recursos e aplicar diferentes configurações de rede e segurança.</p>

<p align="justify">Por exemplo, uma aplicação pode utilizar sub-redes separadas para servidores Web, servidores de aplicação e bancos de dados.</p>

<pre>
Rede Virtual
10.0.0.0/16
      │
      ├── Sub-rede Web
      │   10.0.1.0/24
      │
      ├── Sub-rede Aplicação
      │   10.0.2.0/24
      │
      └── Sub-rede Banco de Dados
          10.0.3.0/24
</pre>

<p align="justify">Os recursos implantados nas sub-redes podem se comunicar entre si dentro da VNet, desde que não existam regras de segurança ou roteamento impedindo essa comunicação.</p>

<p align="justify">Ao planejar uma VNet, é importante escolher intervalos de endereços que não se sobreponham a outras redes virtuais ou redes locais que precisarão ser conectadas.</p>

> **AZ-900:**  
> **VNet → rede**  
> **Subnet → divisão da rede em intervalos de IP**

### Pontos de extremidade de serviço

<p align="justify">Os <strong>pontos de extremidade de serviço (Service Endpoints)</strong> permitem estender a identidade da VNet e o espaço de endereçamento privado da rede para determinados serviços do Azure.</p>

<p align="justify">Com um ponto de extremidade de serviço, o tráfego entre a VNet e o serviço do Azure permanece na rede de backbone da Microsoft. Isso permite restringir o acesso ao serviço para determinadas redes virtuais.</p>

<p align="justify">Os pontos de extremidade de serviço são utilizados, por exemplo, para controlar o acesso de uma VNet a serviços PaaS do Azure.</p>

> **AZ-900:** Service Endpoint = permite proteger o acesso a determinados serviços do Azure a partir de uma VNet.

### Pontos de extremidade privados

<p align="justify">O <strong>Azure Private Link</strong> permite acessar serviços do Azure por meio de um <strong>ponto de extremidade privado (Private Endpoint)</strong> dentro de uma VNet.</p>

<p align="justify">O ponto de extremidade privado utiliza um endereço IP privado da VNet para acessar o serviço. Dessa forma, o serviço pode ser acessado de forma privada sem precisar expô-lo à Internet pública.</p>

> **AZ-900:**  
> **Service Endpoint → estende a VNet ao serviço**  
> **Private Endpoint → fornece um IP privado para acessar o serviço**

<p align="justify">Os pontos de extremidade privados consomem endereços IP da sub-rede existente e não exigem uma sub-rede dedicada.</p>


<h3><strong style='color: skyblue'>Grupos de Segurança de Rede</strong></h3>

<p align="justify">O <strong>Grupo de Segurança de Rede (Network Security Group – NSG)</strong> permite filtrar o tráfego de entrada e saída de recursos do Azure.</p>

<p align="justify">As regras do NSG podem permitir ou negar tráfego com base em informações como endereço IP de origem, endereço IP de destino, porta e protocolo.</p>

<p align="justify">Um NSG pode ser associado a uma sub-rede ou a uma interface de rede (NIC), permitindo controlar quais conexões podem acessar os recursos.</p>

> **AZ-900:** NSG = filtrar tráfego de entrada e saída.


<h3><strong style='color: skyblue'>Gateway de VPN</strong></h3>

<p align="justify">O <strong>Gateway de VPN (VPN Gateway)</strong> permite estabelecer conexões criptografadas entre redes utilizando a Internet. Ele pode ser usado para conectar redes locais ao Azure ou conectar redes virtuais entre si.</p>

<p align="justify">O Gateway de VPN é implantado em uma VNet e permite estabelecer diferentes tipos de conexão.</p>

### VPN Site a Site

<p align="justify">Uma <strong>VPN Site a Site (S2S)</strong> conecta uma rede local a uma rede virtual do Azure por meio de um túnel VPN criptografado.</p>

<pre>
Rede local
    │
    │ Túnel VPN criptografado
    │
    ▼
VPN Gateway
    │
    ▼
Azure VNet
</pre>

<p align="justify">Esse tipo de conexão é adequado quando uma organização deseja conectar toda a sua rede local ao Azure.</p>

> **AZ-900:** Site-to-Site = rede local ↔ Azure.

### VPN Ponto a Site

<p align="justify">Uma <strong>VPN Ponto a Site (P2S)</strong> permite que um computador ou usuário individual se conecte a uma VNet do Azure por meio de uma conexão VPN.</p>

<p align="justify">É adequada para cenários em que usuários individuais precisam acessar recursos da rede virtual, como em situações de trabalho remoto.</p>

> **AZ-900:** Point-to-Site = usuário/computador individual ↔ Azure.

### VPN VNet a VNet

<p align="justify">A <strong>VPN VNet a VNet</strong> permite conectar duas redes virtuais do Azure por meio de uma conexão VPN.</p>

<pre>
VNet 1
  │
  │ VPN
  │
  ▼
VNet 2
</pre>

<p align="justify">Essa opção pode ser utilizada para permitir comunicação entre recursos localizados em redes virtuais diferentes.</p>

> **AZ-900:** VNet-to-VNet = VNet ↔ VNet.


<h3><strong style='color: skyblue'>ExpressRoute</strong></h3>

<p align="justify">O <strong>Azure ExpressRoute</strong> permite estender uma rede local para a infraestrutura da Microsoft por meio de uma conexão <strong>privada</strong> fornecida por um parceiro de conectividade.</p>

<p align="justify">Diferentemente de uma VPN, o tráfego do ExpressRoute não passa pela Internet pública.</p>

<pre>
Rede local
    │
    │ Conexão privada
    │
    ▼
ExpressRoute
    │
    ▼
Microsoft / Azure
</pre>

<p align="justify">O ExpressRoute pode ser utilizado para conectar redes locais aos serviços da Microsoft, incluindo o Azure.</p>

### Quando usar o ExpressRoute?

<p align="justify">O ExpressRoute é adequado quando uma organização precisa de uma conexão privada entre seu ambiente local e a Microsoft, especialmente quando há requisitos de conectividade mais previsíveis e quando não se deseja utilizar a Internet pública para o tráfego.</p>

> **AZ-900:**  
> **VPN → conexão criptografada pela Internet**  
> **ExpressRoute → conexão privada que não passa pela Internet pública**

### VPN Gateway × ExpressRoute

| Característica | VPN Gateway | ExpressRoute |
|---|---|---|
| Conexão | VPN | Conexão privada |
| Internet pública | Utilizada | Não utilizada |
| Criptografia | Túnel VPN criptografado | Conexão privada |
| Site a Site | ✅ | ✅ |
| Principal conceito | Conectividade VPN | Conectividade privada |

> **Dica de prova:** se a questão enfatizar **"não passa pela Internet pública"**, pense em **ExpressRoute**.


<h3><strong style='color: skyblue'>DNS do Azure</strong></h3>

<p align="justify">O <strong>DNS do Azure</strong> fornece serviços de hospedagem e resolução de nomes DNS utilizando a infraestrutura do Azure.</p>

<p align="justify">O DNS é responsável por traduzir nomes de domínio, como <code>www.exemplo.com</code>, em endereços IP que podem ser utilizados para localizar recursos na rede.</p>

### DNS Público do Azure

<p align="justify">O <strong>DNS Público do Azure</strong> permite hospedar domínios DNS no Azure e gerenciar seus registros DNS.</p>

<p align="justify">Os registros DNS podem ser gerenciados utilizando o portal do Azure, APIs, ferramentas e outros mecanismos de gerenciamento.</p>

> **AZ-900:** DNS Público = hospedar e gerenciar domínios DNS públicos.

### DNS Privado do Azure

<p align="justify">O <strong>DNS Privado do Azure</strong> fornece resolução de nomes para redes virtuais do Azure sem a necessidade de implantar uma solução DNS personalizada.</p>

<p align="justify">Ele permite criar zonas DNS privadas que podem ser utilizadas pelos recursos dentro das redes virtuais.</p>

> **AZ-900:** DNS Privado = resolução de nomes em redes privadas.


<h3><strong style='color: skyblue'>Acesso básico à rede para um recurso do Azure</strong></h3>

<p align="justify">Para permitir que um recurso, como uma máquina virtual, tenha conectividade de rede, é necessário configurar os componentes básicos de rede associados ao recurso.</p>

<p align="justify">Uma máquina virtual, por exemplo, utiliza uma <strong>interface de rede (NIC)</strong> para se conectar a uma sub-rede de uma VNet.</p>

<pre>
                    Rede Virtual
                   10.0.0.0/16
                        │
                  Sub-rede
                  10.0.1.0/24
                        │
                       NIC
                        │
                        ▼
                       VM
</pre>

### Componentes básicos

- **VNet:** fornece a rede privada.
- **Sub-rede:** define o intervalo de endereços IP utilizado pelo recurso.
- **NIC:** conecta a VM à rede virtual.
- **IP privado:** permite comunicação dentro da rede.
- **IP público:** permite conectividade pela Internet quando necessário.
- **NSG:** controla o tráfego de entrada e saída.

<p align="justify">Durante a criação de uma VM, é possível selecionar ou criar uma VNet, uma sub-rede, uma interface de rede e, quando necessário, um endereço IP público e um NSG.</p>

### Exemplo de acesso básico

<p align="justify">Para permitir que uma VM seja acessada por RDP ou SSH, é necessário permitir a porta correspondente nas regras de segurança e fornecer uma forma de alcançar a VM, como um endereço IP público.</p>

<p align="justify">Entretanto, expor diretamente a VM à Internet nem sempre é a opção mais adequada. O <strong>Azure Bastion</strong>, por exemplo, permite acesso administrativo às VMs por meio do portal do Azure, utilizando o endereço IP privado da VM.</p>

> **AZ-900:**  
> **NIC → conecta a VM à VNet**  
> **IP → identifica o recurso na rede**  
> **NSG → controla o tráfego**


## 🧠 Resumo dos serviços de rede

| Serviço | Principal objetivo |
|---|---|
| **Azure VNet** | Criar uma rede privada no Azure |
| **Subnet** | Dividir uma VNet em segmentos de endereçamento |
| **Service Endpoint** | Restringir acesso a determinados serviços do Azure a partir de uma VNet |
| **Private Endpoint** | Acessar serviços por meio de um IP privado |
| **NSG** | Filtrar tráfego de entrada e saída |
| **VPN Gateway** | Conectar redes por VPN criptografada |
| **Site-to-Site VPN** | Rede local ↔ Azure |
| **Point-to-Site VPN** | Usuário/computador ↔ Azure |
| **VNet-to-VNet VPN** | VNet ↔ VNet |
| **ExpressRoute** | Conexão privada com a Microsoft |
| **Azure Public DNS** | Hospedar zonas DNS públicas |
| **Azure Private DNS** | Resolver nomes em redes privadas |
| **NIC** | Conectar uma VM à rede |
| **IP público** | Permitir conectividade pública |
| **IP privado** | Comunicação dentro da rede privada |
| **Azure Bastion** | Acesso administrativo às VMs sem expor diretamente o IP público da VM |


## 🧠 Mapa mental para AZ-900

<pre>
                  AZURE NETWORK
                       │
       ┌───────────────┼────────────────┐
       │               │                │
      VNet          CONECTIVIDADE      DNS
       │               │                │
   ┌───┼───┐       ┌───┴────┐       ┌──┴────┐
   │   │   │       │        │       │       │
Subnet NSG Endpoint VPN   Express   Public  Private
                    Gateway  Route    DNS     DNS
                       │
              ┌────────┼────────┐
              │        │        │
             S2S      P2S    VNet-VNet


              ACESSO A RECURSOS
                     │
              ┌──────┼──────┐
              │      │      │
             NIC    IP     NSG
              │      │      │
              └──────┴──────┘
                     │
                    VM
</pre>


## 🎯 O que decorar para a prova

| Se a questão falar... | Pense em... |
|---|---|
| Rede privada no Azure | **VNet** |
| Divisão da VNet | **Subnet** |
| Filtrar tráfego | **NSG** |
| Serviço Azure acessível pela VNet | **Service Endpoint** |
| IP privado para serviço PaaS | **Private Endpoint / Private Link** |
| Rede local ↔ Azure pela Internet | **Site-to-Site VPN** |
| Usuário individual ↔ Azure | **Point-to-Site VPN** |
| VNet ↔ VNet usando VPN | **VNet-to-VNet** |
| Conexão privada que não usa Internet pública | **ExpressRoute** |
| Hospedar DNS público | **Azure Public DNS** |
| DNS para rede privada | **Azure Private DNS** |
| Conectar VM à VNet | **NIC** |
| Acesso público a um recurso | **Public IP** |
| Acesso administrativo a VM sem expor IP público | **Azure Bastion** |


## ⚠️ Diferenças importantes para o AZ-900

### Service Endpoint × Private Endpoint

<pre>
Service Endpoint

VNet ─────────────────► Serviço Azure
          backbone
        da Microsoft


Private Endpoint

VNet ───► IP PRIVADO ───► Serviço Azure
</pre>

<p align="justify"><strong>Service Endpoint:</strong> permite proteger o acesso a determinados serviços do Azure a partir de uma VNet.</p>

<p align="justify"><strong>Private Endpoint:</strong> cria uma interface de rede com um endereço IP privado dentro da VNet para acessar o serviço de forma privada.</p>


### VPN × ExpressRoute

<pre>
VPN

Azure ◄──── Internet + túnel criptografado ────► On-premises


ExpressRoute

Azure ◄────────── conexão privada ─────────────► On-premises
</pre>

> **VPN → utiliza a Internet + túnel VPN**
>
> **ExpressRoute → conexão privada, sem utilizar a Internet pública**


### VNet × Subnet × NSG

<pre>
VNet
 │
 ├── Subnet A
 │     └── VM
 │
 └── Subnet B
       └── VM

NSG
 ↓
Controla quais conexões
podem entrar/sair
</pre>

<p align="justify">A <strong>VNet</strong> é a rede, a <strong>sub-rede</strong> é uma divisão dessa rede e o <strong>NSG</strong> controla o tráfego de entrada e saída.</p>
