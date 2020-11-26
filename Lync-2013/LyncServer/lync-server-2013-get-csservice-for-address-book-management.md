---
title: 'Lync Server 2013: Get-CsService para gerenciamento de catálogo de endereços'
description: 'Lync Server 2013: Get-CsService para gerenciamento de catálogo de endereços.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsService for Address Book management
ms:assetid: 373b717d-5efa-4c36-a899-a23a5bd922b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429698(v=OCS.15)
ms:contentKeyID: 48183853
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e46173429988d87022c13fab33e3778279dd0e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427982"
---
# <a name="get-csservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="35143-103">Get-CsService para gerenciamento de catálogo de endereços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35143-103">Get-CsService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="35143-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="35143-104">

<span> </span></span></span>

<span data-ttu-id="35143-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="35143-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="35143-106">Quem pode executar este cmdlet: por padrão, os membros dos grupos a seguir estão autorizados a executar o cmdlet Get-CsService localmente: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="35143-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsService cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="35143-107">Para retornar uma lista de todas as funções de controle de acesso baseado em função (RBAC) às quais esse cmdlet foi atribuído (incluindo qualquer função RBAC personalizada que você criou), execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="35143-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsService"}

<span data-ttu-id="35143-108">Get-CsService é importante recuperar e exibir a configuração atual dos serviços Web definidos pela sua infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="35143-108">Get-CsService is valuable to retrieve and display the current configuration of your infrastructure’s defined Web Services.</span></span> <span data-ttu-id="35143-109">Ao definir o FQDN (nome de domínio totalmente qualificado) e o parâmetro WebServer (FQDN) do pool, o cmdlet retorna os serviços baseados na Web oferecidos pelo seu servidor, incluindo os URIs manipulador de catálogo de endereços e expansão de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="35143-109">By defining the pool’s fully qualified domain name (FQDN) and the parameter WebServer, the cmdlet returns the web-based services offered by your server, including the Address Book handler and distribution list expansion URIs.</span></span>

<span data-ttu-id="35143-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="35143-110">For example:</span></span>

    Get-CsService -PoolFqdn "fe01.contoso.net" -WebServer

<span data-ttu-id="35143-111">Este cmdlet retorna o seguinte:</span><span class="sxs-lookup"><span data-stu-id="35143-111">This cmdlet returns the following:</span></span>

<span data-ttu-id="35143-112">Identidade: webserver:pool01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="35143-112">Identity : WebServer:pool01.contoso.net</span></span>

<span data-ttu-id="35143-113">Filestore: filestore:dc01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="35143-113">FileStore : FileStore:dc01.contoso.net</span></span>

<span data-ttu-id="35143-114">Userserver: userserver:pool01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="35143-114">UserServer : UserServer:pool01.contoso.net</span></span>

<span data-ttu-id="35143-115">PrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="35143-115">PrimaryHttpPort : 80</span></span>

<span data-ttu-id="35143-116">PrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="35143-116">PrimaryHttpsPort : 443</span></span>

<span data-ttu-id="35143-117">ExternalHttpPort: 8080</span><span class="sxs-lookup"><span data-stu-id="35143-117">ExternalHttpPort : 8080</span></span>

<span data-ttu-id="35143-118">ExternalHttpsPort: 4443</span><span class="sxs-lookup"><span data-stu-id="35143-118">ExternalHttpsPort : 4443</span></span>

<span data-ttu-id="35143-119">PublishedPrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="35143-119">PublishedPrimaryHttpPort : 80</span></span>

<span data-ttu-id="35143-120">PublishedPrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="35143-120">PublishedPrimaryHttpsPort : 443</span></span>

<span data-ttu-id="35143-121">PublishedExternalHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="35143-121">PublishedExternalHttpPort : 80</span></span>

<span data-ttu-id="35143-122">PublishedExternalHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="35143-122">PublishedExternalHttpsPort : 443</span></span>

<span data-ttu-id="35143-123">ReachPrimaryPsomServerPort: 8060</span><span class="sxs-lookup"><span data-stu-id="35143-123">ReachPrimaryPsomServerPort : 8060</span></span>

<span data-ttu-id="35143-124">ReachExternalPsomServerPort: 8061</span><span class="sxs-lookup"><span data-stu-id="35143-124">ReachExternalPsomServerPort : 8061</span></span>

<span data-ttu-id="35143-125">AppSharingPortStart: 49152</span><span class="sxs-lookup"><span data-stu-id="35143-125">AppSharingPortStart : 49152</span></span>

<span data-ttu-id="35143-126">AppSharingPortCount: 16383</span><span class="sxs-lookup"><span data-stu-id="35143-126">AppSharingPortCount : 16383</span></span>

<span data-ttu-id="35143-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="35143-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span></span>

<span data-ttu-id="35143-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span><span class="sxs-lookup"><span data-stu-id="35143-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span></span>

<span data-ttu-id="35143-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span><span class="sxs-lookup"><span data-stu-id="35143-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span></span>

<span data-ttu-id="35143-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="35143-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span></span>

<span data-ttu-id="35143-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="35143-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span></span>

<span data-ttu-id="35143-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="35143-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="35143-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="35143-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="35143-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span><span class="sxs-lookup"><span data-stu-id="35143-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span></span>

<span data-ttu-id="35143-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span><span class="sxs-lookup"><span data-stu-id="35143-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span></span>

<span data-ttu-id="35143-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="35143-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="35143-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="35143-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span></span>

<span data-ttu-id="35143-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="35143-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span></span>

<span data-ttu-id="35143-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span><span class="sxs-lookup"><span data-stu-id="35143-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span></span>

<span data-ttu-id="35143-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span><span class="sxs-lookup"><span data-stu-id="35143-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span></span>

<span data-ttu-id="35143-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="35143-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="35143-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="35143-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="35143-143">MeetExternalUri : https://csweb.contoso.com/Meet</span><span class="sxs-lookup"><span data-stu-id="35143-143">MeetExternalUri : https://csweb.contoso.com/Meet</span></span>

<span data-ttu-id="35143-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span><span class="sxs-lookup"><span data-stu-id="35143-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span></span>

<span data-ttu-id="35143-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span><span class="sxs-lookup"><span data-stu-id="35143-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span></span>

<span data-ttu-id="35143-146">ReachExternalUri : https://csweb.contoso.com/Reach</span><span class="sxs-lookup"><span data-stu-id="35143-146">ReachExternalUri : https://csweb.contoso.com/Reach</span></span>

<span data-ttu-id="35143-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span><span class="sxs-lookup"><span data-stu-id="35143-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span></span>

<span data-ttu-id="35143-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="35143-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="35143-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="35143-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="35143-150">ExternalFqdn: csweb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="35143-150">ExternalFqdn : csweb.contoso.com</span></span>

<span data-ttu-id="35143-151">InternalFqdn: internalweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="35143-151">InternalFqdn : internalweb.contoso.net</span></span>

<span data-ttu-id="35143-152">DependentServiceList: {registrar:pool01. contoso. net, ConferencingServer:pool01. contoso. net}</span><span class="sxs-lookup"><span data-stu-id="35143-152">DependentServiceList : {Registrar:pool01.contoso.net, ConferencingServer:pool01.contoso.net}</span></span>

<span data-ttu-id="35143-153">ServiceId: 1-WebServices-1</span><span class="sxs-lookup"><span data-stu-id="35143-153">ServiceId : 1-WebServices-1</span></span>

<span data-ttu-id="35143-154">SiteId: site: Redmond</span><span class="sxs-lookup"><span data-stu-id="35143-154">SiteId : Site:Redmond</span></span>

<span data-ttu-id="35143-155">PoolFqdn: pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="35143-155">PoolFqdn : pool01.contoso.net</span></span>

<span data-ttu-id="35143-156">Versão: 5</span><span class="sxs-lookup"><span data-stu-id="35143-156">Version : 5</span></span>

<span data-ttu-id="35143-157">Função: WebServer</span><span class="sxs-lookup"><span data-stu-id="35143-157">Role : WebServer</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="35143-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="35143-158">See Also</span></span>


[<span data-ttu-id="35143-159">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="35143-159">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="35143-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="35143-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

