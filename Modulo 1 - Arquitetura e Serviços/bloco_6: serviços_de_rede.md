## Serviços de rede do Azure

<h3><strong style='color: skyblue'>Rede Virtual (Vnet)</strong></h3>

<p align="justify">As redes virtuais e as sub-redes virtuais do Azure permitem que recursos do Azure, como VMs, aplicativos Web e bancos de dados, comuniquem-se uns com os outros, com usuários na Internet e com computadores cliente locais. São redes isoladas e personalizáveis que podem ser criadas dentro de uma assinatura do Azure, permitindo uma conectividade flexível e escalável.</p> 

<p align="justify">Uma rede virtual pode ser dividida em várias sub-redes virtuais (Subnets) para criar isolamento e segmentação de recursos. Cada sub-rede possui um intervalo de endereços IP exclusivo dentro da rede virtual.</p>

- Pontos de extremidade públicos têm um endereço IP público e podem ser acessados de qualquer lugar do mundo.
- Pontos de extremidade privados existem em uma rede virtual e têm um endereço IP privado dentro do espaço de endereço dessa rede virtual.

<p align="justify">O emparelhamento de Vnets (Virtual Networks) no Microsoft Azure permite a conexão de duas redes virtuais em uma região específica, permitindo que os recursos nas redes virtuais se comuniquem entre si como se estivessem na mesma rede física. Esse emparelhamento cria uma conexão de rede privada entre as Vnets, isolada da Internet pública.</p>

<h3><strong style='color: skyblue'>Gateway de VPN</strong></h3>

<p align="justify">O Gateway de VPN do Azure é um serviço que permite estabelecer uma conexão segura entre redes locais e a infraestrutura de rede virtual no Azure. Ele atua como um gateway de entrada e saída para o tráfego de rede entre a rede local e a rede virtual do Azure.</p>

<p align="justify">Todas as transferências de dados são criptografadas em um túnel privado à medida que atravessam a Internet. Você pode implantar apenas um gateway de VPN em cada rede virtual. Porém, você pode usar um gateway para se conectar a vários locais, incluindo outras redes virtuais ou datacenters locais.</p>

<p align="justify">Ao configurar um gateway de VPN, você deve especificar o tipo de VPN: baseada em política ou baseada em rota. A principal distinção entre esses dois tipos é como eles determinam qual tráfego precisa de criptografia.</p>

<p align="justify">Uso de um gateway de VPN baseado em rota se precisar de qualquer um dos seguintes tipos de conectividade:</p>

- Conexões entre redes virtuais
- Conexões ponto a site
- Conexões multissite
- Coexistência com um gateway do Azure ExpressRoute

<h3><strong style='color: skyblue'> ExpressRoute</strong></h3>

<p align="justify">O Express Route do Azure amplia redes locais para o Azure por meio de uma conexão privada facilitada por um provedor de conectividade. Essa conexão é chamada de Circuito do ExpressRoute. 
</p>
<p align="justify">Ele estabelece uma conexão direta através de provedores de rede selecionados, contornando a Internet pública. Essa configuração permite que as conexões do ExpressRoute ofereçam mais confiabilidade, velocidades mais rápidas, latências consistentes e maior segurança do que as conexões típicas pela Internet.</p>