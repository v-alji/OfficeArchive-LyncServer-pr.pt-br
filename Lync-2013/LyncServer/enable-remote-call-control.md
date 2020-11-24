---
title: Habilitar o controle de chamada remota
description: Habilite o controle de chamada remota.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Enable remote call control
ms:assetid: 0b91d418-e6ed-4556-97af-e8523e01f249
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204664(v=OCS.15)
ms:contentKeyID: 48183380
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8009ffc927ad3f7a4f83ad3505100f3a9d4e82d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389983"
---
# <a name="enable-remote-call-control"></a><span data-ttu-id="c9d3f-103">Habilitar o controle de chamada remota</span><span class="sxs-lookup"><span data-stu-id="c9d3f-103">Enable remote call control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c9d3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c9d3f-104">

<span> </span></span></span>

<span data-ttu-id="c9d3f-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="c9d3f-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="c9d3f-106">O controle de chamada remota permite que os usuários controlem seus telefones PBX (Private Branch Exchange) da área de trabalho usando o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-106">Remote call control enables users to control their desktop private branch exchange (PBX) phones by using Lync Server 2013.</span></span> <span data-ttu-id="c9d3f-107">Se você tiver implantado o controle de chamada remota em seu ambiente herdado e quiser migrar o Lync Server 2013, será necessário executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c9d3f-107">If you deployed remote call control in your legacy environment and want to migrate it Lync Server 2013, you need to perform the following tasks:</span></span>

1.  <span data-ttu-id="c9d3f-108">Instale um gateway SIP/CSTA e configure-o para se comunicar com o seu PBX.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-108">Install a SIP/CSTA gateway and configure it to communicate with your PBX.</span></span> <span data-ttu-id="c9d3f-109">Você precisa fazer esta etapa ao implantar o pool piloto do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-109">You need to do this step when you deploy your Lync Server 2013 pilot pool.</span></span>

2.  <span data-ttu-id="c9d3f-110">Depois de Mesclar sua topologia e migrar suas políticas e configurações, configure o Lync Server 2013 para direcionar as solicitações de CSTA para o gateway SIP/CSTA.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-110">After you merge your topology and migrate your policies and settings, configure Lync Server 2013 to route CSTA requests to the SIP/CSTA gateway.</span></span> <span data-ttu-id="c9d3f-111">Esta etapa é uma etapa manual que segue a migração automatizada.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-111">This step is a manual step that follows the automated migration.</span></span> <span data-ttu-id="c9d3f-112">Para configurar o roteamento de solicitações de CSTA, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c9d3f-112">To configure routing for CSTA requests, do the following:</span></span>
    
      - <span data-ttu-id="c9d3f-113">Remova as entradas de host autorizadas herdadas (conhecidas como *entradas de servidor confiáveis* no Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="c9d3f-113">Remove legacy authorized host entries (known as *trusted server entries* in Lync Server 2013).</span></span> <span data-ttu-id="c9d3f-114">Se você estiver migrando usuários da implantação herdada, certifique-se de remover todas as entradas de host autorizadas existentes que você criou para o gateway SIP/CSTA antes de configurar novas entradas de aplicativo confiável no pool piloto do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-114">If you are migrating users from your legacy deployment, ensure that you remove all existing authorized host entries that you created for the SIP/CSTA gateway before you configure new trusted application entries on the Lync Server 2013 pilot pool.</span></span> <span data-ttu-id="c9d3f-115">Para obter detalhes sobre como remover entradas de host autorizadas herdadas, consulte [remover uma entrada de host autorizado](remove-an-authorized-host-entry.md).</span><span class="sxs-lookup"><span data-stu-id="c9d3f-115">For details about how to remove legacy authorized host entries, see [Remove an authorized host entry](remove-an-authorized-host-entry.md).</span></span>
    
      - <span data-ttu-id="c9d3f-116">Configurar uma rota estática para o controle de chamada remota.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-116">Configure a static route for remote call control.</span></span> <span data-ttu-id="c9d3f-117">Você pode configurar uma rota estática para pools individuais para os quais você deseja dar suporte para controle de chamada remota, ou pode configurar uma rota estática global para que cada pool que não esteja configurado com uma rota estática em nível de pool use a rota estática global.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-117">You can configure a static route for individual pools that you want to support remote call control, or you can configure a global static route so that each pool that is not configured with a pool-level static route uses the global static route.</span></span> <span data-ttu-id="c9d3f-118">Para obter detalhes sobre como configurar a rota estática, consulte [Configurar uma rota estática para o controle de chamada remota no Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-118">For details about how to configure the static route, see [Configure a static route for remote call control in Lync Server 2013](lync-server-2013-configure-a-static-route-for-remote-call-control.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="c9d3f-119">Configure uma entrada de aplicativo confiável para controle de chamada remota em cada pool para o qual você deseja dar suporte ao controle de chamada remota.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-119">Configure a trusted application entry for remote call control on each pool for which you want to support remote call control.</span></span> <span data-ttu-id="c9d3f-120">Para obter detalhes sobre como configurar uma entrada de aplicativo confiável, consulte [Configurar uma entrada de aplicativo confiável para o controle de chamada remota no Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-120">For details about how to configure a trusted application entry, see [Configure a trusted application entry for remote call control in Lync Server 2013](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md) in the Deployment documentation.</span></span>

3.  <span data-ttu-id="c9d3f-121">Se você implantou um gateway SIP/CSTA que usa o protocolo de controle de transmissão (TCP) para se conectar ao Lync Server 2013, defina o endereço IP do gateway no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-121">If you deployed a SIP/CSTA gateway that uses Transmission Control Protocol (TCP) to connect to Lync Server 2013, define the IP address of the gateway in Topology Builder.</span></span> <span data-ttu-id="c9d3f-122">Para obter detalhes sobre como definir o endereço IP, consulte [definir um endereço IP de gateway SIP/CSTA no Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-122">For details about defining the IP address, see [Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) in the Deployment documentation.</span></span>

4.  <span data-ttu-id="c9d3f-123">Configurar os usuários do Lync 2013 para controle de chamada remota habilitando o controle de chamada remota e atribuindo um URI (Uniform Resource Identifier) do servidor de linha e um URI de linha.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-123">Configure Lync 2013 users for remote call control by enabling remote call control and assigning a line server Uniform Resource Identifier (URI) and a line URI.</span></span> <span data-ttu-id="c9d3f-124">Quando você migra os usuários da sua implantação herdada para o Lync Server 2013, as configurações do controle de chamada remota são migradas juntamente com as outras configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-124">When you migrate users from your legacy deployment to Lync Server 2013, the remote call control settings are migrated along with the other user settings.</span></span>

5.  <span data-ttu-id="c9d3f-125">Se você tiver personalizado regras de normalização de número de telefone do catálogo de endereços em sua implantação herdada, será necessário executar algumas tarefas manuais após a conclusão da migração automatizada de políticas e configurações para migrar as regras de normalização personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-125">If you customized Address Book phone number normalization rules in your legacy deployment, you need to perform some manual tasks after the automated migration of policies and settings is complete to migrate the customized normalization rules.</span></span> <span data-ttu-id="c9d3f-126">Se você não tiver personalizado as regras de normalização, o catálogo de endereços será migrado juntamente com o restante da sua topologia.</span><span class="sxs-lookup"><span data-stu-id="c9d3f-126">If you did not customize normalization rules, Address Book is migrated along with the rest of your topology.</span></span> <span data-ttu-id="c9d3f-127">Para obter detalhes sobre a migração manual das regras de normalização personalizada, consulte [migrar catálogo de endereços](migrate-address-book.md).</span><span class="sxs-lookup"><span data-stu-id="c9d3f-127">For details about manually migrating customized normalization rules, see [Migrate Address Book](migrate-address-book.md).</span></span>

<span data-ttu-id="c9d3f-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c9d3f-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

