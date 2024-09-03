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

## Opções de movimentação de Arquivos

<p align="justify">AzCopy: é uma ferramenta de linha de comando que permite copiar grandes quantidades de dados para o armazenamento do Azure de forma eficiente e segura. Ele suporta transferências em massa, bem como a transferência de dados em paralelo, o que pode melhorar significativamente o desempenho. O AzCopy também suporta a sincronização de arquivos e pode ser executado em vários sistemas operacionais, incluindo Windows, Linux e macOS.</p>

<p align="justify">Azure Storage Explorer: é uma ferramenta gráfica que permite gerenciar dados no armazenamento do Azure. Ele suporta a criação e edição de contas de armazenamento, bem como a transferência de arquivos e pastas entre diferentes tipos de armazenamento. O Azure Storage Explorer também suporta a configuração de acesso seguro e a navegação em arquivos armazenados em contas de armazenamento do Azure.
</p>

<p align="justify">Azure File Sync: é uma ferramenta de sincronização de arquivos que permite sincronizar arquivos entre um servidor de arquivos local e um compartilhamento de arquivos do Azure. Ele ajuda a gerenciar o armazenamento de arquivos no local e no Azure, permitindo que os usuários acessem os arquivos de forma rápida e fácil em ambos os locais. O Azure File Sync também permite a sincronização de vários servidores de arquivos locais com um único compartilhamento de arquivos do Azure.</p>

## Opções de migração de Arquivos

<p align="justify">Azure Migrate: é uma ferramenta que ajuda a avaliar e migrar cargas de trabalho locais para o Azure. Ele oferece suporte a uma ampla variedade de sistemas operacionais, bancos de dados e aplicativos e fornece uma visão unificada do ambiente de migração. O Azure Migrate ajuda a identificar dependências de aplicativos, avaliar o desempenho e fazer recomendações de dimensionamento para a infraestrutura no Azure.</p>

<p align="justify">Azure Data Box: é um serviço de transferência de dados em massa que permite mover grandes quantidades de dados para o Azure de forma rápida, segura e eficiente. O Azure Data Box vem em diferentes formatos físicos, como o Data Box Edge, que pode ser usado como uma solução de armazenamento em cache local para cargas de trabalho de borda e IoT.</p>