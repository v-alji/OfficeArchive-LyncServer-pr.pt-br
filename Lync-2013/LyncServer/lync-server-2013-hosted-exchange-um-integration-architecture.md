---
title: 'Lync Server 2013: Arquitetura de integração do UM do Exchange hospedado'
description: 'Lync Server 2013: arquitetura de integração do Exchange UM hospedada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange UM integration architecture
ms:assetid: 0094d5dc-1836-441c-b6e2-f88e35203a8d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398067(v=OCS.15)
ms:contentKeyID: 48183222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2399fa421b59a5ea1fd83b1a86225fc12de1f2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427604"
---
# <a name="hosted-exchange-um-integration-architecture-in-lync-server-2013"></a><span data-ttu-id="b182b-103">Arquitetura de integração do UM do Exchange hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b182b-103">Hosted Exchange UM integration architecture in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b182b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b182b-104">

<span> </span></span></span>

<span data-ttu-id="b182b-105">_**Tópico da última modificação:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="b182b-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="b182b-106">O aplicativo de roteamento ExUM do Lync Server 2013 dá suporte à integração com uma implantação do Exchange Unified Messaging (UM) local, com um provedor de serviços do Exchange hospedado por um provedor de serviços ou com uma combinação dos dois.</span><span class="sxs-lookup"><span data-stu-id="b182b-106">The Lync Server 2013 ExUM Routing application supports integration with an on-premises Exchange Unified Messaging (UM) deployment, with Exchange UM hosted by a service provider, or with a combination of the two.</span></span> <span data-ttu-id="b182b-107">O diagrama a seguir mostra todas as três possibilidades.</span><span class="sxs-lookup"><span data-stu-id="b182b-107">The following diagram shows all three possibilities.</span></span>

<span data-ttu-id="b182b-108">**Integração com uma implantação do Exchange UM local e dois provedores do Exchange hospedados**</span><span class="sxs-lookup"><span data-stu-id="b182b-108">**Integration with an on-premises Exchange UM deployment and two hosted Exchange providers**</span></span>

<span data-ttu-id="b182b-109">![Implantação do Exchange UM do Lync Server local](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "Implantação do Exchange UM do Lync Server local")</span><span class="sxs-lookup"><span data-stu-id="b182b-109">![On-premises Lync Server Exchange UM Deployment](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "On-premises Lync Server Exchange UM Deployment")</span></span>

<span data-ttu-id="b182b-110">Há suporte para os seguintes modos:</span><span class="sxs-lookup"><span data-stu-id="b182b-110">The following modes are supported:</span></span>

  - <span data-ttu-id="b182b-111">**Implantação local:** O Lync Server 2013 e o Exchange UM são implantados em servidores locais dentro da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="b182b-111">**On-premises deployment:** Lync Server 2013 and Exchange UM are both deployed on local servers within your enterprise.</span></span>

  - <span data-ttu-id="b182b-112">**Implantação em várias instalações:** O Lync Server 2013 é implantado em servidores locais na sua empresa e o Exchange UM está hospedado em um recurso do provedor de serviços online, como um Data Center online do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="b182b-112">**Cross-premises deployment:** Lync Server 2013 is deployed on local servers within your enterprise and Exchange UM is hosted in an online service provider’s facility, such as a Microsoft Exchange Online data center.</span></span>

  - <span data-ttu-id="b182b-113">**Implantação mista:** A implantação do Lync Server 2013 tem algumas caixas de correio de usuário hospedadas em servidores locais do Exchange na sua empresa e algumas caixas de correio hospedadas em um data center do serviço do Exchange.</span><span class="sxs-lookup"><span data-stu-id="b182b-113">**Mixed deployment:** Your Lync Server 2013 deployment has some user mailboxes homed on local Exchange servers within your enterprise and some mailboxes homed in a hosted Exchange service data center.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b182b-114">A implantação mista pode ser usada como uma solução de transição durante a avaliação e a migração em fases de usuários para o Exchange UM hospedada ou uma solução permanente se você optar por manter os serviços de UM dos usuários do Exchange no local depois de transferir outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="b182b-114">The mixed deployment can be used as a transitional solution during evaluation and phased migration of users to hosted Exchange UM, or a permanent solution if you opt to keep some users’ Exchange UM services on-premises after transferring others.</span></span>

    
    </div>

<div>

## <a name="shared-sip-address-space"></a><span data-ttu-id="b182b-115">Espaço de endereço SIP compartilhado</span><span class="sxs-lookup"><span data-stu-id="b182b-115">Shared SIP Address Space</span></span>

<span data-ttu-id="b182b-116">Para integrar o Lync Server 2013 com uma implantação do Exchange UM local, conceda a permissão do Lync Server 2013 para ler objetos dos serviços de domínio do Active Directory de UM Exchange.</span><span class="sxs-lookup"><span data-stu-id="b182b-116">To integrate Lync Server 2013 with an on-premises Exchange UM deployment, you grant Lync Server 2013 permission to read Exchange UM Active Directory Domain Services objects.</span></span> <span data-ttu-id="b182b-117">No entanto, essa abordagem não funciona para a integração com o Exchange UM hospedado, porque o Lync Server 2013 e o Exchange UM são instalados em florestas separadas sem nenhuma confiança entre elas.</span><span class="sxs-lookup"><span data-stu-id="b182b-117">This approach does not work for integration with hosted Exchange UM, however, because Lync Server 2013 and Exchange UM are installed in separate forests with no trust between them.</span></span>

<span data-ttu-id="b182b-118">Para integrar o Lync Server 2013 com o Exchange UM hospedado, você deve configurar um *espaço de endereço SIP compartilhado*.</span><span class="sxs-lookup"><span data-stu-id="b182b-118">To integrate Lync Server 2013 with hosted Exchange UM, you must configure a *shared SIP address space*.</span></span> <span data-ttu-id="b182b-119">Nesta configuração, o mesmo espaço de endereço de domínio SIP está disponível para o Lync Server 2013 e para o provedor de serviços de UM host do Exchange.</span><span class="sxs-lookup"><span data-stu-id="b182b-119">In this configuration, the same SIP domain address space is available to both Lync Server 2013 and the hosted Exchange UM service provider.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b182b-120">O uso do espaço de endereço SIP compartilhado é semelhante à abordagem usada em um ambiente do Lync Server 2013, no qual alguns usuários são hospedados na implantação local e alguns são hospedados em uma implantação hospedada (como o Lync Online).</span><span class="sxs-lookup"><span data-stu-id="b182b-120">Use of the shared SIP address space is similar to the approach used in a cross-premises Lync Server 2013 environment, in which some users are homed in the on-premises deployment and some are homed in a hosted deployment (such as Lync Online).</span></span> <span data-ttu-id="b182b-121">O domínio SIP é dividido entre eles.</span><span class="sxs-lookup"><span data-stu-id="b182b-121">The SIP domain is split between them.</span></span> <span data-ttu-id="b182b-122">Ao integrar o Lync Server 2013 com o Exchange UM hospedado, certifique-se de incluir o provedor de serviços de UM do Exchange no espaço de endereço SIP compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b182b-122">When you integrate Lync Server 2013 with hosted Exchange UM, ensure that you include the Exchange UM service provider in the shared SIP address space.</span></span>



</div>

<span data-ttu-id="b182b-123">Para configurar o espaço de endereço SIP compartilhado para integração com um provedor de serviços de UM Exchange, você precisa configurar o servidor de borda da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b182b-123">To configure the shared SIP address space for integrating with an Exchange UM service provider, you need to configure your Edge Server as follows:</span></span>

1.  <span data-ttu-id="b182b-124">Configure o servidor de borda para Federação executando o cmdlet **set-CsAccessEdgeConfiguration** para definir os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b182b-124">Configure the Edge Server for federation by running the **Set-CsAccessEdgeConfiguration** cmdlet to set the following parameters:</span></span>
    
      - <span data-ttu-id="b182b-125">**UseDnsSrvRouting** especifica se os Servidores de Borda dependerão dos registros DNS SRV ao enviar e receber solicitações de federação.</span><span class="sxs-lookup"><span data-stu-id="b182b-125">**UseDnsSrvRouting** specifies that Edge Servers will rely on DNS SRV records when sending and receiving federation requests.</span></span>
    
      - <span data-ttu-id="b182b-p105">**AllowFederatedUsers** especifica se os usuários internos têm permissão para se comunicar com usuários de domínios federados. Essa propriedade também determina se os usuários internos podem se comunicar com usuários em uma situação de divisão de domínios.</span><span class="sxs-lookup"><span data-stu-id="b182b-p105">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains. This property also determines whether internal users can communicate with users in a split domain scenario.</span></span>
    
      - <span data-ttu-id="b182b-128">**EnablePartnerDiscovery** especifica se o Lync Server 2013 usará os registros de DNS para tentar descobrir domínios de parceiros que não estão listados na lista de domínios permitidos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b182b-128">**EnablePartnerDiscovery** specifies whether Lync Server 2013 will use DNS records to try to discover partner domains that are not listed in the Active Directory allowed domains list.</span></span> <span data-ttu-id="b182b-129">Se falso, o Lync Server 2013 se federará apenas com domínios encontrados na lista de domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="b182b-129">If False, Lync Server 2013 will federate only with domains that are found on the allowed domains list.</span></span> <span data-ttu-id="b182b-130">Esse parâmetro é obrigatório caso se esteja utilizando o roteamento de serviço de DNS.</span><span class="sxs-lookup"><span data-stu-id="b182b-130">This parameter is required if you use DNS service routing.</span></span> <span data-ttu-id="b182b-131">Na maioria das implantações, o valor é definido como falso para evitar abrir a federação a todos os parceiros.</span><span class="sxs-lookup"><span data-stu-id="b182b-131">In most deployments, the value is set to false to avoid opening up federation to all partners.</span></span>

2.  <span data-ttu-id="b182b-132">Replique o repositório de gerenciamento central para o servidor de borda e verifique a replicação.</span><span class="sxs-lookup"><span data-stu-id="b182b-132">Replicate the Central Management store to the Edge Server and verify the replication.</span></span> <span data-ttu-id="b182b-133">Para obter detalhes, consulte [exportar sua topologia do Lync Server 2013 e copiá-la para mídia externa para instalação do Edge](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="b182b-133">For details, see [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) in the Deployment documentation.</span></span>

3.  <span data-ttu-id="b182b-134">Configure um *provedor de hospedagem* no servidor de borda executando o cmdlet **New-CsHostingProvider** para definir os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b182b-134">Configure a *hosting provider* on the Edge Server by running the **New-CsHostingProvider** cmdlet to set the following parameters:</span></span>
    
      - <span data-ttu-id="b182b-135">**Identity** especifica um identificador de valor de cadeia de caracteres exclusivo para o provedor de hospedagem que você está criando, por exemplo, **Hosted Exchange um**.</span><span class="sxs-lookup"><span data-stu-id="b182b-135">**Identity** specifies a unique string value identifier for the hosting provider that you are creating, for example, **Hosted Exchange UM**.</span></span>
    
      - <span data-ttu-id="b182b-136">**Habilitado** indica se a conexão de rede entre seu domínio e o provedor de hospedagem está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b182b-136">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="b182b-137">Deve ser definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="b182b-137">Must be set to **True**.</span></span>
    
      - <span data-ttu-id="b182b-138">**EnabledSharedAddressSpace** indica se o provedor de hospedagem será usado em um cenário de espaço de endereçamento SIP compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b182b-138">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="b182b-139">Deve ser definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="b182b-139">Must be set to **True**.</span></span>
    
      - <span data-ttu-id="b182b-140">**HostsOCSUsers** indica se o provedor de hospedagem é usado para hospedar contas do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b182b-140">**HostsOCSUsers** indicates whether the hosting provider is used to host Lync Server 2013 accounts.</span></span> <span data-ttu-id="b182b-141">Deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="b182b-141">Must be set to **False**.</span></span>
    
      - <span data-ttu-id="b182b-142">**ProxyFQDN** especifica o nome de domínio totalmente qualificado (FQDN) do servidor proxy usado pelo provedor de hospedagem, por exemplo, **ProxyServer.fabrikam.com**.</span><span class="sxs-lookup"><span data-stu-id="b182b-142">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider, for example, **proxyserver.fabrikam.com**.</span></span> <span data-ttu-id="b182b-143">Entre em contato com seu provedor de hospedagem para obter essas informações.</span><span class="sxs-lookup"><span data-stu-id="b182b-143">Contact your hosting provider for this information.</span></span> <span data-ttu-id="b182b-144">Esse valor não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="b182b-144">This value cannot be modified.</span></span> <span data-ttu-id="b182b-145">Se o provedor de hospedagem alterar seu servidor proxy, será preciso excluir e recriar a entrada para esse provedor.</span><span class="sxs-lookup"><span data-stu-id="b182b-145">If the hosting provider changes its proxy server, you will need to delete and then recreate the entry for that provider.</span></span>
    
      - <span data-ttu-id="b182b-146">**IsLocal** indica se o servidor proxy usado pelo provedor de hospedagem está contido na sua topologia do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b182b-146">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server 2013 topology.</span></span> <span data-ttu-id="b182b-147">Deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="b182b-147">Must be set to **False**.</span></span>

<span data-ttu-id="b182b-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b182b-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

