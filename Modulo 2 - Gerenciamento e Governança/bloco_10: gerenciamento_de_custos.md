## Fatores que podem afetar os custos

1. Tipo de recursos: Serviços que podem aumentar ou diminuir automaticamente com base na demanda (por exemplo, autoscaling de VMs ou containers) podem afetar o custo dependendo da utilização.

2. Consumo: Quanto mais recursos (como CPUs, memória e armazenamento) forem usados, maior será o custo.

3. Manutenção: monitoramento do volume e a manutenção do ambiente podem ajudar a identificar e reduzir os custos.

4. área geográfica: O custo pode variar de acordo com a região de implantação escolhida, pois os preços podem ser diferentes em cada região.

5. Tráfego de rede: A largura de banda refere-se aos dados que entram e saem dos datacenters do Azure. Algumas transferências de dados de entrada (dados que entram em datacenters do Azure) são gratuitas. Para transferências de dados de saída (dados que saem de data centers do Azure), o preço de transferência de dados é baseado em zonas.

6. Assinatura: Alguns tipos de assinatura do Azure também incluem as concessões de uso, que afetam os custos.

## Calculadoras

<p align="justify">A calculadora de preços e a calculadora TCO (custo total de propriedade) ajudam a entender possíveis despesas do Azure. Ambas podem ser acessadas pela Internet e permitem criar uma configuração. No entanto, as duas calculadoras têm propósitos muito diferentes.</p>

<p align="justify">A calculadora de preços foi projetada para fornecer um custo estimado para provisionar recursos no Azure. Você pode obter uma estimativa para recursos individuais, criar uma solução ou usar um cenário de exemplo para ver uma estimativa dos gastos do Azure. O foco da calculadora de preços está no custo dos recursos provisionados no Azure.</p>

<p align="justify">Com a calculadora de preços, você pode estimar o custo de todos os recursos provisionados, incluindo computação, armazenamento e custos de rede associados. Você pode até mesmo considerar diferentes opções de armazenamento, como tipo de armazenamento, camada de acesso e redundância.</p>

<p align="justify">A calculadora de TCO foi projetada para ajudá-lo a comparar os custos para executar uma infraestrutura local versus uma infraestrutura de nuvem do Azure. Com a calculadora de TCO, você insere sua configuração de infraestrutura atual, incluindo servidores, bancos de dados, armazenamento e tráfego de rede de saída. Então a calculadora de TCO compara os custos previstos para seu ambiente atual com um ambiente do Azure que dá suporte aos mesmos requisitos de infraestrutura.</p>

## Funcionalidades de gerenciamento de custos do Azure

<p align="justify">O Gerenciamento de Custos (Azure Cost Management) permite verificar rapidamente os custos de recursos do Azure, criar alertas com base nos gastos com recursos e criar orçamentos que podem ser usados para automatizar o gerenciamento de recursos.</p>

<p align="justify">A análise de custo é um subconjunto de Gerenciamento de Custos que apresenta um visual rápido para os custos do Azure. Usando a análise de custo, você pode visualizar rapidamente o custo total de várias maneiras, inclusive por ciclo de cobrança, região, recurso etc.</p>

<p align="justify">Os alertas de custo fornecem um só local para verificar rapidamente todos os diferentes tipos de alerta que podem aparecer no serviço de Gerenciamento de Custos. Os três tipos de alertas que podem aparecer são:</p>

- Alertas de orçamento
- Alertas de crédito
- Alertas de cota de gastos do departamento.

<p align="justify">Você pode definir orçamentos com base em uma assinatura, grupo de recursos, tipo de serviço ou outros critérios. Ao definir um orçamento, você também define um alerta de orçamento. Quando o orçamento atinge o nível de alerta do orçamento, ele dispara um alerta de orçamento que aparece na área de alertas de custo. Se configurados, os alertas de orçamento também enviarão uma notificação por email de que um limite de alerta de orçamento foi disparado.</p>

##  Marcas do Azure (Azure Tags)

<p align="justify">As Marcas do Azure (Azure Tags) são um recurso do Microsoft Azure que permite rotular recursos para fins de gerenciamento e organização. Com as Marcas do Azure, é possível identificar facilmente recursos específicos com base em informações personalizadas, como ambiente (produção, teste, desenvolvimento), proprietário, departamento ou qualquer outro critério que seja relevante para a organização.</p>

| **Nome**       | **Valor**                                      |
|----------------|-----------------------------------------------|
| AppName        | O nome do aplicativo do qual o recurso faz parte. |
| CostCenter     | O código do centro de custo interno.            |
| Proprietário   | O nome do proprietário de negócios responsável pelo recurso. |
| Ambiente       | Um nome de ambiente, como "Prod", "Dev" ou "Test". |
| Impacto        | O grau de importância do recurso para as operações de negócios, como "Crítico", "De alto impacto" ou "De baixo impacto". |
