## Serviços de diretório do Azure

<p align="justify">Os serviços de diretório no Microsoft Azure fornecem gerenciamento de identidade e acesso para aplicativos em nuvem e locais, permitindo que as empresas gerenciem usuários e grupos de maneira centralizada. Existem dois principais serviços de diretório disponíveis no Azure:</p>

<h3><strong style='color: skyblue'>Microsoft Entra ID</strong></h3>

<p align="justify">Microsoft Entra ID (anteriormente conhecido como Azure Active Directory): Serve para autenticação e gerenciamento de identidades em aplicações e recursos na nuvem e on-premises. Ele oferece suporte a SSO (Single Sign-On), multifator de autenticação (MFA), e gerenciamento de acesso baseado em funções (RBAC), além de proteger contra ameaças com capacidades de segurança avançadas.</p>

<p align="justify">Um dos métodos de conexão entre o Microsoft Entra ID e seu AD local é o uso do Microsoft Entra Connect. O Microsoft Entra Connect sincroniza as identidades do usuário entre o Active Directory local e o Microsoft Entra ID. O Microsoft Entra Connect sincroniza alterações entre os dois sistemas de identidade, de forma que você possa usar recursos como o SSO, a autenticação multifator e a redefinição de senha por autoatendimento em ambos.</p>

<h3><strong style='color: skyblue'>Microsoft Entra Domain Services</strong></h3>

<p align="justify">Microsoft Entra Domain Services: Serve para fornecer serviços de domínio gerenciado, como ingresso no domínio, política de grupo, protocolo de acesso leve a diretórios (LDAP) e autenticação Kerberos/NTLM. Assim como o Microsoft Entra ID permite que você use serviços de diretório sem precisar manter uma infraestrutura que os sustente, com o Microsoft Entra Domain Services você obtém o benefício dos serviços de domínio sem precisar implantar, gerenciar ou aplicar patches nos controladores de domínio (DCs) na nuvem.
</p>

<p align="justify">Um domínio gerenciado é configurado para executar uma sincronização unidirecional do Microsoft Entra ID para o Microsoft Entra Domain Services. É possível criar recursos diretamente no domínio gerenciado, mas eles não são sincronizados com o Microsoft Entra ID. Em um ambiente híbrido com um ambiente local do AD DS, o Microsoft Entra Connect sincroniza as informações de identidade com o Microsoft Entra ID, que, por sua vez, é sincronizado com o domínio gerenciado.</p>

<p align="center">
  <img src="https://learn.microsoft.com/pt-br/training/wwl-azure/describe-azure-identity-access-security/media/azure-active-directory-sync-topology-7359f2b8.png" width="2000" height="400">
</p>

## Métodos de Autenticação no Azure

<p align="justify">Os métodos de autenticação no Azure são formas de validar a identidade do usuário e permitir o acesso a recursos no ambiente do Azure. </p>

<p align="justify">O SSO (logon único) permite que um usuário entre uma vez e use essa credencial para acessar vários recursos e aplicativos de provedores diferentes. Para que o SSO funcione, os diferentes aplicativos e provedores devem confiar no autenticador inicial.</p>

<p align="justify">A autenticação multifator é o processo de solicitar a um usuário uma forma (ou um fator) adicional de identificação durante o processo de entrada. A MFA ajuda a proteger contra uma exposição de senha em situações em que a senha tenha sido comprometida, mas o segundo fator não.</p>

<p align="justify">A autenticação multifator fornece segurança adicional para as identidades, exigindo dois ou mais elementos para a autenticação completa. Esses elementos se enquadram em três categorias:</p>

- Algo que o usuário saiba– essa pode ser uma pergunta de desafio.
- Algo que o usuário tenha – pode ser um código enviado para o telefone celular do usuário.
- Algo que o usuário seja – normalmente é algum tipo de propriedade biométrica, como a leitura de impressão digital ou reconhecimento facial.

<p align="justify">A autenticação sem senha é um método de autenticação que elimina a necessidade de senhas. Em vez disso, ele usa uma combinação de outras formas de autenticação, como autenticação baseada em certificado ou biometria. Isso melhora a segurança e simplifica a experiência do usuário, pois eles não precisam lembrar de senhas complexas. O Microsoft Entra ID oferece suporte à autenticação sem senha por meio de recursos como o Passwordless authentication.
</p>

## Identidades Externas no Azure

<p align="justify">As identidades externas no Azure referem-se à capacidade de gerenciar e autenticar usuários que não fazem parte da organização interna. Isso inclui parceiros de negócios (B2B) e clientes (B2C), permitindo-lhes acessar recursos e serviços da empresa de maneira segura e controlada.</p>

<p align="justify">Para o B2B Microsoft Entra External ID permite que empresas convidem e colaborem com usuários externos, como parceiros, fornecedores e outros terceiros. Os usuários externos podem usar suas próprias credenciais para acessar os recursos da empresa, sem a necessidade de criar uma nova identidade dentro do Azure AD da organização.</p>

<p align="justify">Azure AD B2C é um serviço de gerenciamento de identidade para consumidores. Ele permite que empresas criem soluções personalizadas de autenticação para seus clientes, permitindo que eles usem suas contas de redes sociais ou criem novas contas usando um sistema de gerenciamento de identidade seguro.
</p>