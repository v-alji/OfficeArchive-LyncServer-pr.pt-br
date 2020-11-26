---
title: 'Lync Server 2013: requisitos do aplicativo Lync da Windows Store'
description: 'Lync Server 2013: requisitos do aplicativo Lync da Windows Store.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Windows Store app requirements
ms:assetid: 5f2e0a40-8450-4f61-b6f6-913fc1906020
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ823129(v=OCS.15)
ms:contentKeyID: 50120200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17e8705a55625bcf0ad099ead1000a82c994d867
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426162"
---
# <a name="lync-windows-store-app-requirements-for-lync-server-2013"></a><span data-ttu-id="e1dea-103">Requisitos do aplicativo Lync da Windows Store para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1dea-103">Lync Windows Store app requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1dea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1dea-104">

<span> </span></span></span>

<span data-ttu-id="e1dea-105">_**Tópico da última modificação:** 2013-12-03_</span><span class="sxs-lookup"><span data-stu-id="e1dea-105">_**Topic Last Modified:** 2013-12-03_</span></span>

<span data-ttu-id="e1dea-106">As organizações com uma implantação local do Lync Server devem atender aos seguintes requisitos para dar suporte ao aplicativo Lync da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e1dea-106">Organizations with an on-premises deployment of Lync Server must meet the following requirements to support Lync Windows Store app.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e1dea-107">Para o Lync Server 2010, execute a atualização cumulativa para o Lync Server 2010: fevereiro de 2012 (disponível em <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2670352"> https://go.microsoft.com/fwlink/?linkid=3052&amp ; kbid = 2670352</A>) ou posterior em todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="e1dea-107">For Lync Server 2010, run the cumulative update for Lync Server 2010: February 2012 (available at <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2670352">https://go.microsoft.com/fwlink/?linkid=3052&amp;kbid=2670352</A>) or later on all servers.</span></span> <span data-ttu-id="e1dea-108">Para permitir que os usuários ingressem em reuniões, execute a atualização cumulativa do Lync Server 2010: outubro de 2012 (disponível em <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2737915"> https://go.microsoft.com/fwlink/?linkid=3052&amp ; kbid = 2737915</A>) nos servidores.</span><span class="sxs-lookup"><span data-stu-id="e1dea-108">To enable users to join meetings, run the cumulative update for Lync Server 2010: October 2012 (available at <A class=uri href="https://go.microsoft.com/fwlink/?linkid=3052%26kbid=2737915">https://go.microsoft.com/fwlink/?linkid=3052&amp;kbid=2737915</A>) on the servers.</span></span>



</div>

  - <span data-ttu-id="e1dea-109">Habilite a descoberta automática, o Lync Web App e os serviços de tíquete da Web no servidor.</span><span class="sxs-lookup"><span data-stu-id="e1dea-109">Enable the Autodiscover, Lync Web App, and Web Ticket services on the server.</span></span>

  - <span data-ttu-id="e1dea-110">Habilite a autenticação de certificado no servidor front-end ou no pool de front-end.</span><span class="sxs-lookup"><span data-stu-id="e1dea-110">Enable certificate authentication on the Front End Server or Front End pool.</span></span> <span data-ttu-id="e1dea-111">(O processo de registro do usuário no servidor front-end ou no pool de front-ends é geralmente chamado de registrador.) Para obter detalhes, consulte [criar configurações de registrador de configuração no Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e1dea-111">(The user registration process on the Front End Server or Front End pool is often referred to as the registrar.) For details, see [Create Registrar configuration settings in Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span></span>

  - <span data-ttu-id="e1dea-112">Publicar os registros de recursos de alias de DNS (CNAME) do serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="e1dea-112">Publish the DNS alias (CNAME) resource records for the Autodiscover service.</span></span>

  - <span data-ttu-id="e1dea-113">Não é mais necessário ter certeza de que o ponto de distribuição da lista de certificados revogados (CRL) dos certificados emitidos para o Lync Server aponta para um recurso HTTP em vez de um recurso LDAP.</span><span class="sxs-lookup"><span data-stu-id="e1dea-113">It is no longer a requirement to make sure the Certificate Revocation List (CRL) Distribution Point (CDP) for the certificates issued to Lync server points to an HTTP resource instead of an LDAP resource.</span></span> <span data-ttu-id="e1dea-114">No entanto, certifique-se de que os computadores cliente tenham as atualizações mais recentes do Windows instaladas.</span><span class="sxs-lookup"><span data-stu-id="e1dea-114">However, make sure that client computers have the latest Windows updates installed.</span></span>

  - <span data-ttu-id="e1dea-115">Configurar proxies HTTP na empresa para permitir o tráfego HTTP relacionado ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e1dea-115">Configure HTTP proxies in the enterprise to allow Lync server related HTTP traffic.</span></span>  <span data-ttu-id="e1dea-116">Adicione exceções para a descoberta automática, Lync Web App e serviços webticket, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e1dea-116">Add exceptions for the Autodiscover, Lync Web App, and WebTicket services, if necessary.</span></span>

  - <span data-ttu-id="e1dea-117">Em clientes, instale o Windows 8,1 e a versão mais recente do aplicativo Lync da Windows Store para corrigir um problema de entrada que geralmente ocorre ao usar vários domínios (por exemplo, quando o URI SIP é **UserA@domainZ.com** , mas o servidor de borda é **SIP.domainX.com**).</span><span class="sxs-lookup"><span data-stu-id="e1dea-117">On clients, install Windows 8.1 and the latest version of Lync Windows Store app to fix a sign-in issue that generally occurs when using multiple domains (for example, when the SIP URI is **userA@domainZ.com** but the Edge Server is **sip.domainX.com**).</span></span>

<span data-ttu-id="e1dea-118">Se a sua organização assinar o Lync Online ou o Microsoft 365 e você estiver usando seu próprio nome de domínio, você deve realizar algumas etapas adicionais para configurar a rede para descoberta automática dos servidores do Lync.</span><span class="sxs-lookup"><span data-stu-id="e1dea-118">If your organization subscribes to Lync Online or Microsoft 365 and you are using your own domain name, you must take some extra steps to set up your network for autodiscovery of the Lync servers.</span></span> <span data-ttu-id="e1dea-119">Os requisitos de configuração de rede são iguais para o aplicativo Lync da Windows Store e Lync em dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="e1dea-119">The network configuration requirements are the same for Lync Windows Store app and Lync on mobile devices.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="e1dea-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1dea-120">See Also</span></span>


[<span data-ttu-id="e1dea-121">Implantando o aplicativo Lync da Windows Store no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1dea-121">Deploying Lync Windows Store app in Lync Server 2013</span></span>](lync-server-2013-deploying-lync-windows-store-app.md)  
  

<span data-ttu-id="e1dea-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1dea-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
