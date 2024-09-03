## Serviços de armazenamento do Azure

<p align="justify">Os serviços de armazenamento do Azure são uma coleção de soluções de armazenamento altamente escaláveis e duráveis oferecidos pela Microsoft. Eles permitem que você armazene, gerencie e proteja dados em uma variedade de formatos, como objetos, arquivos, discos e tabelas. </p>

<p align="justify"> Dos principais serviços de armazenamento do Azure incluem:</p>

1. O ***armazenamento de contêiner (blob)*** é otimizado para armazenar grandes quantidades de dados não estruturados, como dados binários ou de texto.
2. O ***armazenamento em disco*** fornece discos para máquinas virtuais, aplicativos e outros serviços acessarem e usarem.

3. Os ***Arquivos do Azure*** configuram compartilhamentos de arquivos de rede altamente disponíveis que podem ser acessados usando o protocolo padrão SMB (Bloco de Mensagens do Servidor).

4. As ***Filas do Azure*** são um armazenamento de mensagens para um sistema de mensagens confiável entre componentes do aplicativo.

5. As ***Tabelas do Azure*** são a opção de tabela NoSQL para dados estruturados e não relacionais.

<p align="justify">Uma conta de armazenamento fornece um namespace exclusivo para os dados do Armazenamento do Azure que podem ser acessados de qualquer lugar do mundo por HTTP ou HTTPS. Os dados nesta conta são seguros, altamente disponíveis, duráveis e maciçamente escalonáveis.</p>

## Camadas de armazenamento

<p align="justify">O Armazenamento do Azure oferece diferentes camadas de acesso para seu armazenamento de blobs, ajudando você a armazenar dados de objeto da maneira mais econômica. As camadas de acesso disponíveis incluem:</p>

- Camada de acesso quente (Hot Tier): otimizada para armazenar dados que são acessados com frequência (por exemplo, imagens de seu site).

- Camada de acesso esporádico: otimizada para dados acessados com menos frequência e armazenados por pelo menos 30 dias (por exemplo, faturas de seus clientes).

- Camada de acesso frio (Cool Tier): otimizada para armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 90 dias.

- Camada de acesso aos arquivos: adequada para dados acessados raramente e armazenados por pelo menos 180 dias, com requisitos de latência flexíveis (por exemplo, backups de longo prazo).

## Opções de Redundância

<p align="justify">As opções de redundância de armazenamento do Microsoft Azure são utilizadas para fornecer alta disponibilidade e resiliência aos dados armazenados no Azure. Existem cinco opções de redundância de armazenamento:</p>