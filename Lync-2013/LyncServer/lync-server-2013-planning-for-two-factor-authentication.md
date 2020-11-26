---
title: 'Lync Server 2013: planejando a autenticação de dois fatores'
description: 'Lync Server 2013: planejando a autenticação de dois fatores.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for two-factor authentication
ms:assetid: 16f08710-8961-4659-acbf-ebb95a198fb4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308562(v=OCS.15)
ms:contentKeyID: 54973683
ms.date: 04/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a3a2cd5508f6ce9a8a389b0059a09747b9f9a09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442870"
---
# <a name="planning-for-two-factor-authentication-in-lync-server-2013"></a><span data-ttu-id="06629-103">Planejando a autenticação de dois fatores no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06629-103">Planning for two-factor authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06629-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06629-104">

<span> </span></span></span>

<span data-ttu-id="06629-105">_**Tópico da última modificação:** 2015-04-06_</span><span class="sxs-lookup"><span data-stu-id="06629-105">_**Topic Last Modified:** 2015-04-06_</span></span>

<span data-ttu-id="06629-106">Veja a seguir uma lista de considerações de implantação ao configurar um ambiente do Microsoft Lync Server 2013 para dar suporte à autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-106">The following is a list of deployment considerations when configuring a Microsoft Lync Server 2013 environment to support two-factor authentication.</span></span>

<div>

## <a name="client-support"></a><span data-ttu-id="06629-107">Suporte de Cliente</span><span class="sxs-lookup"><span data-stu-id="06629-107">Client Support</span></span>

<span data-ttu-id="06629-108">As atualizações cumulativas do Lync 2013 para o Lync Server 2013: julho de 2013 do cliente de área de trabalho e todos os clientes móveis atualmente dão suporte à autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-108">The Lync 2013 Cumulative Updates for Lync Server 2013: July 2013 desktop client and all mobile clients currently support two-factor authentication.</span></span>

</div>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="06629-109">Requisitos de topologia</span><span class="sxs-lookup"><span data-stu-id="06629-109">Topology Requirements</span></span>

<span data-ttu-id="06629-110">Os clientes são altamente incentivados a implantar a autenticação de dois fatores usando o Lync Server dedicado 2013 com atualizações cumulativas para o Lync Server 2013:2013 de julho a Edge, director e grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="06629-110">Customers are strongly encouraged to deploy two-factor authentication using dedicated Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Edge, Director, and User Pools.</span></span> <span data-ttu-id="06629-111">Para habilitar a autenticação passiva para usuários do Lync, outros métodos de autenticação devem ser desabilitados para outras funções e serviços, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="06629-111">To enable passive authentication for Lync users, other authentication methods must be disabled for other roles and services, including the following:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06629-112">Tipo de configuração</span><span class="sxs-lookup"><span data-stu-id="06629-112">Configuration Type</span></span></th>
<th><span data-ttu-id="06629-113">Tipo de serviço</span><span class="sxs-lookup"><span data-stu-id="06629-113">Service Type</span></span></th>
<th><span data-ttu-id="06629-114">Função do servidor</span><span class="sxs-lookup"><span data-stu-id="06629-114">Server Role</span></span></th>
<th><span data-ttu-id="06629-115">Tipo de autenticação a ser desabilitada</span><span class="sxs-lookup"><span data-stu-id="06629-115">Authentication Type to Disable</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06629-116">Serviço Web</span><span class="sxs-lookup"><span data-stu-id="06629-116">Web Service</span></span></p></td>
<td><p><span data-ttu-id="06629-117">WebServer</span><span class="sxs-lookup"><span data-stu-id="06629-117">WebServer</span></span></p></td>
<td><p><span data-ttu-id="06629-118">Diretor</span><span class="sxs-lookup"><span data-stu-id="06629-118">Director</span></span></p></td>
<td><p><span data-ttu-id="06629-119">Kerberos, NTLM e Certificado</span><span class="sxs-lookup"><span data-stu-id="06629-119">Kerberos, NTLM, and Certificate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06629-120">Serviço Web</span><span class="sxs-lookup"><span data-stu-id="06629-120">Web Service</span></span></p></td>
<td><p><span data-ttu-id="06629-121">WebServer</span><span class="sxs-lookup"><span data-stu-id="06629-121">WebServer</span></span></p></td>
<td><p><span data-ttu-id="06629-122">Front-End</span><span class="sxs-lookup"><span data-stu-id="06629-122">Front End</span></span></p></td>
<td><p><span data-ttu-id="06629-123">Kerberos, NTLM e Certificado</span><span class="sxs-lookup"><span data-stu-id="06629-123">Kerberos, NTLM, and Certificate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06629-124">Proxy</span><span class="sxs-lookup"><span data-stu-id="06629-124">Proxy</span></span></p></td>
<td><p><span data-ttu-id="06629-125">EdgeServer</span><span class="sxs-lookup"><span data-stu-id="06629-125">EdgeServer</span></span></p></td>
<td><p><span data-ttu-id="06629-126">Borda</span><span class="sxs-lookup"><span data-stu-id="06629-126">Edge</span></span></p></td>
<td><p><span data-ttu-id="06629-127">Kerberos e NTLM</span><span class="sxs-lookup"><span data-stu-id="06629-127">Kerberos and NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06629-128">Proxy</span><span class="sxs-lookup"><span data-stu-id="06629-128">Proxy</span></span></p></td>
<td><p><span data-ttu-id="06629-129">Registrador</span><span class="sxs-lookup"><span data-stu-id="06629-129">Registrar</span></span></p></td>
<td><p><span data-ttu-id="06629-130">Front-End</span><span class="sxs-lookup"><span data-stu-id="06629-130">Front End</span></span></p></td>
<td><p><span data-ttu-id="06629-131">Kerberos e NTLM</span><span class="sxs-lookup"><span data-stu-id="06629-131">Kerberos and NTLM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="06629-132">A menos que esses tipos de autenticação sejam desabilitados no nível de serviço, todas as outras versões do cliente do Lync não poderão entrar com êxito após a habilitação da autenticação de dois fatores na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="06629-132">Unless these authentication types are disabled at the service level, all other versions of the Lync client will be unable to sign in successfully once two-factor authentication is enabled within in your deployment.</span></span>

</div>

<div>

## <a name="lync-service-discovery"></a><span data-ttu-id="06629-133">Descoberta de serviço do Lync</span><span class="sxs-lookup"><span data-stu-id="06629-133">Lync Service Discovery</span></span>

<span data-ttu-id="06629-134">Os registros DNS usados por clientes internos e/ou externos para descobrir serviços do Lync devem ser configurados para resolver para um Lync Server que não está habilitado para autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-134">DNS records used by internal and/or external clients to discover Lync services should be configured to resolve to a Lync server that is not enabled for two-factor authentication.</span></span> <span data-ttu-id="06629-135">Com essa configuração, os usuários de pools do Lync que não estão habilitados para autenticação de dois fatores não serão necessários para inserir um PIN para autenticação, enquanto os usuários de pools do Lync habilitados para a autenticação de dois fatores serão solicitados a digitar o PIN para autenticação.</span><span class="sxs-lookup"><span data-stu-id="06629-135">With this configuration, users from Lync Pools that are not enabled for two-factor authentication will not be required to enter a PIN to authenticate, while users from Lync Pools that are enabled for two-factor authentication will be required to enter their PIN to authenticate.</span></span>

</div>

<div>

## <a name="exchange-authentication"></a><span data-ttu-id="06629-136">Autenticação do Exchange</span><span class="sxs-lookup"><span data-stu-id="06629-136">Exchange Authentication</span></span>

<span data-ttu-id="06629-137">Os clientes que implantaram a autenticação de dois fatores para o Microsoft Exchange podem descobrir que determinados recursos no cliente do Lync não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="06629-137">Customers who have deployed two-factor authentication for Microsoft Exchange may find that certain features in the Lync client are unavailable.</span></span> <span data-ttu-id="06629-138">Isso, no momento, é design, pois o cliente do Lync não dá suporte à autenticação de dois fatores para recursos que dependem da integração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="06629-138">This is currently by design, as the Lync client does not support two-factor authentication for features that are dependent on Exchange integration.</span></span>

</div>

<div>

## <a name="lync-contacts"></a><span data-ttu-id="06629-139">Contatos do Lync</span><span class="sxs-lookup"><span data-stu-id="06629-139">Lync Contacts</span></span>

<span data-ttu-id="06629-140">Os usuários do Lync que estiverem configurados para aproveitar o recurso de repositório de contatos unificado verão que seus contatos não estarão mais disponíveis depois de entrar com a autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-140">Lync users who are configured to leverage the Unified Contact Store feature will find that their contacts are no longer available after signing in with two-factor authentication.</span></span>

<span data-ttu-id="06629-141">Você deve usar o cmdlet **Invoke-CsUcsRollback** para remover os contatos do usuário existentes do repositório de contatos unificado e armazená-los no Lync Server 2013 antes de habilitar a autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-141">You should use the **Invoke-CsUcsRollback** cmdlet to remove existing user contacts from the Unified Contact Store and store them in Lync Server 2013 before enabling two-factor authentication.</span></span>

</div>

<div>

## <a name="skill-search"></a><span data-ttu-id="06629-142">Pesquisa de Habilidades</span><span class="sxs-lookup"><span data-stu-id="06629-142">Skill Search</span></span>

<span data-ttu-id="06629-143">Os clientes que tiverem configurado o recurso de pesquisa de habilidades no ambiente do Lync perceberão que esse recurso não funciona quando o Lync estiver habilitado para autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-143">Customers who have configured the Skill Search feature in their Lync environment will find that this feature does not work when Lync is enabled for two-factor authentication.</span></span> <span data-ttu-id="06629-144">Isso ocorre devido ao projeto, já que o Microsoft SharePoint não é compatível com a autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-144">This is by design, as Microsoft SharePoint does not currently support two-factor authentication.</span></span>

</div>

<div>

## <a name="lync-credentials"></a><span data-ttu-id="06629-145">Credenciais do Lync</span><span class="sxs-lookup"><span data-stu-id="06629-145">Lync Credentials</span></span>

<span data-ttu-id="06629-146">Há várias considerações de implantação envolvendo as credenciais do Lync salvas, que podem afetar os usuários configurados para usar a autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-146">There are a number of deployment considerations involving saved Lync credentials which may impact users who are configured to use two-factor authentication.</span></span>

<div>

## <a name="deleting-saved-credentials"></a><span data-ttu-id="06629-147">Exclusão de Credenciais Salvas</span><span class="sxs-lookup"><span data-stu-id="06629-147">Deleting Saved Credentials</span></span>

<span data-ttu-id="06629-148">Os usuários de cliente de desktop devem usar a opção **excluir minhas informações de entrada** no cliente do Lync e excluir a pasta de perfil SIP de% LocalAppData% \\ Microsoft \\ Office \\ 15,0 \\ Lync antes de tentar se conectar pela primeira vez usando a autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-148">Desktop client users should use the **Delete my sign-in info** option in the Lync client and delete their SIP profile folder from %localappdata%\\Microsoft\\Office\\15.0\\Lync before attempting to sign for the first time using two-factor authentication.</span></span>

</div>

<div>

## <a name="disablentcredentials"></a><span data-ttu-id="06629-149">DisableNTCredentials</span><span class="sxs-lookup"><span data-stu-id="06629-149">DisableNTCredentials</span></span>

<span data-ttu-id="06629-150">Com o método de autenticação Kerberos ou NTLM, as credenciais do Windows do usuário são usadas automaticamente para fins de autenticação.</span><span class="sxs-lookup"><span data-stu-id="06629-150">With the Kerberos or NTLM authentication method, the user’s Windows credentials are used automatically for authentication.</span></span> <span data-ttu-id="06629-151">Em uma implantação típica do Lync Server 2013 na qual Kerberos e/ou NTLM está habilitado para autenticação, os usuários não devem inserir suas credenciais toda vez que entrarem.</span><span class="sxs-lookup"><span data-stu-id="06629-151">In a typical Lync Server 2013 deployment where Kerberos and/or NTLM is enabled for authentication, users should not have to enter their credentials every time that they sign in.</span></span>

<span data-ttu-id="06629-152">Se as credenciais dos usuários forem inadvertidamente solicitadas antes de ser necessário informar o PIN, a chave de registro **DisableNTCredentials** pode estar configurada por engano nos computadores clientes, possivelmente através de uma Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="06629-152">If users are unintentionally prompted for credentials before they are prompted to enter their PIN, the **DisableNTCredentials** registry key may be unintentionally configured on client computers, possibly through Group Policy.</span></span>

<span data-ttu-id="06629-153">Para impedir o prompt adicional de credenciais, crie a seguinte entrada do registro na estação de trabalho local ou use o modelo administrativo do Lync para aplicar a todos os usuários de um determinado pool usando a política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="06629-153">To prevent the additional prompt for credentials, create the following registry entry on the local workstation or use the Lync administrative template to apply to all users for a given pool using Group Policy:</span></span>

<span data-ttu-id="06629-154">HKEY \_ local \_ Machine \\ software \\ policies \\ Microsoft \\ Office \\ 15,0 \\ Lync</span><span class="sxs-lookup"><span data-stu-id="06629-154">HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Office\\15.0\\Lync</span></span>

<span data-ttu-id="06629-155">REG \_ DWORD: DisableNTCredentials</span><span class="sxs-lookup"><span data-stu-id="06629-155">REG\_DWORD: DisableNTCredentials</span></span>

<span data-ttu-id="06629-156">Value: 0x0</span><span class="sxs-lookup"><span data-stu-id="06629-156">Value: 0x0</span></span>

</div>

<div>

## <a name="savepassword"></a><span data-ttu-id="06629-157">SavePassword</span><span class="sxs-lookup"><span data-stu-id="06629-157">SavePassword</span></span>

<span data-ttu-id="06629-158">Quando um usuário entrar no Lync pela primeira vez, o usuário será solicitado a salvar sua senha.</span><span class="sxs-lookup"><span data-stu-id="06629-158">When a user signs in to Lync for the first time, the user is prompted to save his or her password.</span></span> <span data-ttu-id="06629-159">Em caso positivo, o certificado de cliente do usuário fica armazenado no armazenamento de certificado pessoal e as credenciais do Windows do usuário ficam armazenadas no Gerenciador de Credenciais do computador local.</span><span class="sxs-lookup"><span data-stu-id="06629-159">If selected, this option allows the user’s client certificate to be stored in the personal certificate store and the user’s Windows credentials to be stored in the Credential Manager of the local computer.</span></span>

<span data-ttu-id="06629-160">A configuração do registro **SavePassword** deve ser desabilitada quando o Lync estiver configurado para dar suporte à autenticação de dois fatores.</span><span class="sxs-lookup"><span data-stu-id="06629-160">The **SavePassword** registry setting should be disabled when Lync is configured to support two-factor authentication.</span></span> <span data-ttu-id="06629-161">Para impedir que os usuários salvem suas senhas, altere a seguinte entrada do registro na estação de trabalho local ou use o modelo administrativo do Lync para aplicar a todos os usuários de um determinado pool usando a política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="06629-161">To prevent users from saving their passwords, change the following registry entry on the local workstation or use the Lync administrative template to apply to all users for a given pool using Group Policy:</span></span>

<span data-ttu-id="06629-162">HKEY \_ \_ software user \\ atual \\ Microsoft \\ Office \\ 15,0 \\ Lync</span><span class="sxs-lookup"><span data-stu-id="06629-162">HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync</span></span>

<span data-ttu-id="06629-163">REG \_ DWORD: SavePassword</span><span class="sxs-lookup"><span data-stu-id="06629-163">REG\_DWORD: SavePassword</span></span>

<span data-ttu-id="06629-164">Value: 0x0</span><span class="sxs-lookup"><span data-stu-id="06629-164">Value: 0x0</span></span>

</div>

</div>

<div>

## <a name="ad-fs-20-token-replay"></a><span data-ttu-id="06629-165">AD FS 2.0 Token Replay</span><span class="sxs-lookup"><span data-stu-id="06629-165">AD FS 2.0 Token Replay</span></span>

<span data-ttu-id="06629-p108">O AD FS 2.0 oferece um recurso chamado detecção de repetição de token, pelo qual é possível detectar várias solicitações de token que usam o mesmo token a fim de descartá-las. Quanto este recurso está habilitado, a detecção de repetição de token protege a integridade das solicitações de autenticação tanto no perfil passivo do WS-Federation quanto no perfil de SAML WebSSO, certificando-se de que o mesmo token nunca é usado mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="06629-p108">AD FS 2.0 provides a feature referred to as token replay detection, by which multiple token requests using the same token can be detected and then discarded. When this feature is enabled, token replay detection protects the integrity of authentication requests in both the WS-Federation passive profile and the SAML WebSSO profile by making sure that the same token is never used more than once.</span></span>

<span data-ttu-id="06629-168">Esse recurso deve ser habilitado em situações em que há grandes preocupações com a segurança, como quando se usa quiosques.</span><span class="sxs-lookup"><span data-stu-id="06629-168">This feature should be enabled in situations where security is a very high concern such as when using kiosks.</span></span> <span data-ttu-id="06629-169">Para obter mais informações sobre a detecção de repetição de token, consulte práticas recomendadas para o planejamento seguro e a implantação do AD FS 2,0 em [https://go.microsoft.com/fwlink/p/?LinkId=309215](https://go.microsoft.com/fwlink/p/?linkid=309215) .</span><span class="sxs-lookup"><span data-stu-id="06629-169">For more information about token replay detection, see Best Practices for Secure Planning and Deployment of AD FS 2.0 at [https://go.microsoft.com/fwlink/p/?LinkId=309215](https://go.microsoft.com/fwlink/p/?linkid=309215).</span></span>

</div>

<div>

## <a name="external-user-access"></a><span data-ttu-id="06629-170">Acesso de usuários externos</span><span class="sxs-lookup"><span data-stu-id="06629-170">External User Access</span></span>

<span data-ttu-id="06629-171">A configuração de um proxy do AD FS ou do proxy reverso para dar suporte à autenticação de dois fatores do Lync de redes externas não é abordada nestes tópicos.</span><span class="sxs-lookup"><span data-stu-id="06629-171">Configuring an AD FS Proxy or Reverse Proxy to support Lync two-factor authentication from external networks is not covered in these topics.</span></span>

<span data-ttu-id="06629-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06629-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

