## Serviços de armazenamento do Azure

<p align="justify">Os serviços de armazenamento do Azure são uma coleção de soluções de armazenamento altamente escaláveis e duráveis oferecidos pela Microsoft. Eles permitem que você armazene, gerencie e proteja dados em uma variedade de formatos, como objetos, arquivos, discos e tabelas. </p>

<p align="justify"> Dos principais serviços de armazenamento do Azure incluem:</p>

1. O ***armazenamento de contêiner (blob)*** é otimizado para armazenar grandes quantidades de dados não estruturados, como dados binários ou de texto - "https://storage-account-name.blob.core.windows.net".
2. O ***armazenamento em disco*** fornece discos para máquinas virtuais, aplicativos e outros serviços acessarem e usarem - "https://storage-account-name.dfs.core.windows.net".

3. Os ***Arquivos do Azure*** configuram compartilhamentos de arquivos de rede altamente disponíveis que podem ser acessados usando o protocolo padrão SMB (Bloco de Mensagens do Servidor) - "https://storage-account-name.file.core.windows.net".

4. As ***Filas do Azure*** são um armazenamento de mensagens para um sistema de mensagens confiável entre componentes do aplicativo - "https://storage-account-name.queue.core.windows.net".

5. As ***Tabelas do Azure*** são a opção de tabela NoSQL para dados estruturados e não relacionais - "https://storage-account-name.table.core.windows.net".

<p align="justify">Uma conta de armazenamento fornece um namespace exclusivo para os dados do Armazenamento do Azure que podem ser acessados de qualquer lugar do mundo por HTTP ou HTTPS. Os dados nesta conta são seguros, altamente disponíveis, duráveis e maciçamente escalonáveis.</p>

## Camadas de armazenamento

<p align="justify">O Armazenamento do Azure oferece diferentes camadas de acesso para seu armazenamento de blobs, ajudando você a armazenar dados de objeto da maneira mais econômica. As camadas de acesso disponíveis incluem:</p>

- Camada de acesso quente (Hot Tier): otimizada para armazenar dados que são acessados com frequência (por exemplo, imagens de seu site).

- Camada de acesso esporádico: otimizada para dados acessados com menos frequência e armazenados por pelo menos 30 dias (por exemplo, faturas de seus clientes).

- Camada de acesso frio (Cool Tier): otimizada para armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 90 dias.

- Camada de acesso aos arquivos: adequada para dados acessados raramente e armazenados por pelo menos 180 dias, com requisitos de latência flexíveis (por exemplo, backups de longo prazo).

## Opções de Redundância

<p align="justify">As opções de redundância de armazenamento do Microsoft Azure são utilizadas para fornecer alta disponibilidade e resiliência aos dados armazenados no Azure. Existem seis opções de redundância de armazenamento:</p>

| Configuração               | Implantação                       | Durabilidade                                            |
|----------------------------|-----------------------------------|---------------------------------------------------------|
| LRS (Locally Redundant Storage) | Dentro de um único datacenter       | Alta durabilidade (99,999999999% - 11 9's) dentro do datacenter local |
| ZRS (Zone-Redundant Storage)    | Em múltiplas zonas dentro de uma região | Alta durabilidade (99,9999999999% - 12 9's) com replicação entre zonas  |
| GRS (Geo-Redundant Storage)     | Em múltiplas regiões (Primária e Secundária) | Muito alta durabilidade (99,99999999999999% - 16 9's) com replicação geográfica |
| RA-GRS (Read-Access Geo-Redundant Storage) | Em múltiplas regiões (Primária e Secundária) com acesso de leitura à região secundária | Mesma durabilidade que GRS, com a vantagem adicional de leitura na réplica secundária |
| GZRS (Geo-Zone-Redundant Storage) | Múltiplas zonas em uma região primária e replicação para uma região secundária | Altíssima durabilidade (99,99999999999999% - 16 9's), combinando zona e replicação geográfica |
| RA-GZRS (Read-Access Geo-Zone-Redundant Storage) | Múltiplas zonas em uma região primária e replicação para uma região secundária com acesso de leitura | Mesma durabilidade que GZRS, com a vantagem adicional de leitura na réplica secundária |