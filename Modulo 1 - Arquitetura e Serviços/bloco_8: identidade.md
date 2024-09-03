## Serviços de diretório

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
