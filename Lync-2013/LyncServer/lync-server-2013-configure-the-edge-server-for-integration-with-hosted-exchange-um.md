---
title: Configurar Servidor de Borda para integração com o Exchange UM hospedado
description: Configure o Servidor de Borda para integração com a UM do Exchange hospedada.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Edge Server for integration with hosted Exchange UM
ms:assetid: ede3f2f9-f412-418e-a705-8d8ec98176c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399075(v=OCS.15)
ms:contentKeyID: 48185745
ms.date: 01/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1a2eb55df172e6df0bacef0c468a235cb00c3f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433644"
---
# <a name="configure-the-edge-server-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="6718a-103">Configurar Servidor de Borda para integração com o Exchange UM hospedado</span><span class="sxs-lookup"><span data-stu-id="6718a-103">Configure the Edge Server for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6718a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6718a-104">

<span> </span></span></span>

<span data-ttu-id="6718a-105">_**Tópico Última Modificação:** 2015-01-23_</span><span class="sxs-lookup"><span data-stu-id="6718a-105">_**Topic Last Modified:** 2015-01-23_</span></span>

<span data-ttu-id="6718a-106">Para fornecer aos usuários do Lync Server 2013 recursos de caixa postal na UM (Unificação de Mensagens do Exchange) hospedada, execute as seguintes tarefas de configuração no Servidor de Borda:</span><span class="sxs-lookup"><span data-stu-id="6718a-106">To provide your Lync Server 2013 users with voice mail capabilities on hosted Exchange Unified Messaging (UM), you must perform the following configuration tasks on the Edge Server:</span></span>

  - <span data-ttu-id="6718a-107">Configure o Servidor de Borda para federação.</span><span class="sxs-lookup"><span data-stu-id="6718a-107">Configure the Edge Server for federation.</span></span>

  - <span data-ttu-id="6718a-108">Replicar dados do Armazenamento de Gerenciamento Central para o Servidor de Borda e verificar a replicação.</span><span class="sxs-lookup"><span data-stu-id="6718a-108">Replicate Central Management store data to the Edge Server and verify the replication.</span></span>

  - <span data-ttu-id="6718a-109">Crie um provedor de hospedagem no Servidor de Borda.</span><span class="sxs-lookup"><span data-stu-id="6718a-109">Create a hosting provider on the Edge Server.</span></span>

<span data-ttu-id="6718a-110">Para obter detalhes, consulte a documentação do Shell de Gerenciamento do Lync Server para os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6718a-110">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="6718a-111">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6718a-111">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span></span>

  - <span data-ttu-id="6718a-112">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6718a-112">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="6718a-113">É necessário criar um registro DNS SRV para o serviço Exchange de hospedagem antes de você executar essas etapas.</span><span class="sxs-lookup"><span data-stu-id="6718a-113">You must create an external DNS SRV record for the hosting Exchange service before you perform these steps.</span></span> <span data-ttu-id="6718a-114">Para obter detalhes, <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">consulte Create a DNS SRV record for integration with hosted Exchange UM</A>.</span><span class="sxs-lookup"><span data-stu-id="6718a-114">For details, see <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">Create a DNS SRV record for integration with hosted Exchange UM</A>.</span></span>



</div>

<div>

## <a name="to-configure-the-edge-server-for-federation"></a><span data-ttu-id="6718a-115">Para configurar o Servidor de Borda para federação</span><span class="sxs-lookup"><span data-stu-id="6718a-115">To configure the Edge Server for federation</span></span>

1.  <span data-ttu-id="6718a-116">Inicie o Shell de Gerenciamento do Lync Server: clique em **Iniciar,** em Todos os **Programas,** em **Microsoft Lync Server 2013** e em Shell de Gerenciamento do **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="6718a-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="6718a-p102">Execute o cmdlet Set-CsAccessEdgeConfiguration para configurar o servidor para federação. Por exemplo, execute:</span><span class="sxs-lookup"><span data-stu-id="6718a-p102">Run the Set-CsAccessEdgeConfiguration cmdlet to configure the server for federation. For example, run:</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -AllowFederatedUsers 1 -EnablePartnerDiscovery 0
    
    <span data-ttu-id="6718a-119">O exemplo anterior define os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="6718a-119">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="6718a-120">**UseDnsSrvRouting** especifica se os Servidores de Borda dependerão dos registros DNS SRV ao enviar e receber solicitações de federação.</span><span class="sxs-lookup"><span data-stu-id="6718a-120">**UseDnsSrvRouting** specifies that Edge Servers will rely on DNS SRV records when sending and receiving federation requests.</span></span>
    
      - <span data-ttu-id="6718a-p103">**AllowFederatedUsers** especifica se os usuários internos têm permissão para se comunicar com usuários de domínios federados. Essa propriedade também determina se os usuários internos podem se comunicar com usuários em uma situação de divisão de domínios.</span><span class="sxs-lookup"><span data-stu-id="6718a-p103">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains. This property also determines whether internal users can communicate with users in a split domain scenario.</span></span>
    
      - <span data-ttu-id="6718a-123">**EnablePartnerDiscovery** especifica se o Lync Server usará registros DNS para tentar descobrir domínios de parceiros não listados na lista de domínios permitidos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6718a-123">**EnablePartnerDiscovery** specifies whether Lync Server will use DNS records to try to discover partner domains not listed in the Active Directory allowed domains list.</span></span> <span data-ttu-id="6718a-124">Se False, o Lync Server 2013 só federará com domínios encontrados na lista de domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="6718a-124">If False, Lync Server 2013 will only federate with domains found on the allowed domains list.</span></span> <span data-ttu-id="6718a-125">Esse parâmetro é obrigatório caso se esteja utilizando o roteamento de serviço de DNS.</span><span class="sxs-lookup"><span data-stu-id="6718a-125">This parameter is required if you use DNS service routing.</span></span> <span data-ttu-id="6718a-126">Na maioria das implantações, o valor é definido como falso para evitar abrir a federação a todos os parceiros.</span><span class="sxs-lookup"><span data-stu-id="6718a-126">In most deployments, the value is set to false to avoid opening up federation to all partners.</span></span>

</div>

<div>

## <a name="to-replicate-data-to-the-edge-server-and-verify-the-replication"></a><span data-ttu-id="6718a-127">Para replicar os dados para o Servidor de Borda e verificar a replicação</span><span class="sxs-lookup"><span data-stu-id="6718a-127">To replicate data to the Edge Server and verify the replication</span></span>

  - <span data-ttu-id="6718a-128">Verifique se a replicação para o Servidor de Borda está completa.</span><span class="sxs-lookup"><span data-stu-id="6718a-128">Verify that the replication to the Edge Server is complete.</span></span> <span data-ttu-id="6718a-129">Para o procedimento, consulte [Verify connectivity between internal servers and Edge Servers in Lync Server 2013](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md).</span><span class="sxs-lookup"><span data-stu-id="6718a-129">For the procedure, see [Verify connectivity between internal servers and Edge Servers in Lync Server 2013](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md).</span></span>

</div>

<div>

## <a name="to-create-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="6718a-130">Para criar um provedor de hospedagem no Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="6718a-130">To create a hosting provider on the Edge Server</span></span>

1.  <span data-ttu-id="6718a-131">Inicie o Shell de Gerenciamento do Lync Server: clique em **Iniciar,** em Todos os **Programas,** em **Microsoft Lync Server 2013** e em Shell de Gerenciamento do **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="6718a-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="6718a-132">Execute o cmdlet **New-CsHostingProvider** para configurar o provedor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="6718a-132">Run the **New-CsHostingProvider** cmdlet to configure the hosting provider.</span></span> <span data-ttu-id="6718a-133">Por exemplo, execute:</span><span class="sxs-lookup"><span data-stu-id="6718a-133">For example, run:</span></span>
    
        New-CsHostingProvider -Identity Fabrikam.com -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFQDN "proxyserver.fabrikam.com" -IsLocal $False -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="6718a-134">O exemplo anterior define os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="6718a-134">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="6718a-p107">**Identidade** especifica um identificador exclusivo de valor de cadeia de caracteres para o provedor de hospedagem que você está criando, neste exemplo, **Fabrikam.com**. Observe que o comando falhará se um provedor existente já tiver sido configurado com essa identidade.</span><span class="sxs-lookup"><span data-stu-id="6718a-p107">**Identity** specifies a unique string value identifier for the hosting provider you are creating, in this example, **Fabrikam.com**. Note that the command will fail if an existing provider has already been configured with that Identity.</span></span>
    
      - <span data-ttu-id="6718a-p108">**Habilitado** indica se a conexão de rede entre seu domínio e o provedor de hospedagem está habilitado. As mensagens não podem ser trocadas entre as duas organizações até que esse valor seja definido como **Verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="6718a-p108">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled. Messages cannot be exchanged between the two organizations until this value is set to **True**.</span></span>
    
      - <span data-ttu-id="6718a-139">**EnabledSharedAddressSpace** indica se o provedor de hospedagem está sendo usado em um cenário de espaço de endereço SIP compartilhado (domínio dividido).</span><span class="sxs-lookup"><span data-stu-id="6718a-139">**EnabledSharedAddressSpace** indicates whether the hosting provider is being used in a shared SIP address space (split domain) scenario.</span></span>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="6718a-140">Antes de definir <CODE>EnableSharedAddressSpace</CODE> como True, tente resolver o registro SRV de Federação internamente.</span><span class="sxs-lookup"><span data-stu-id="6718a-140">Before you set <CODE>EnableSharedAddressSpace</CODE> to True, try to resolve the Federation SRV record internally.</span></span> <span data-ttu-id="6718a-141">Se esse registro não puder ser resolvido internamente, você precisará criar os registros, _sipfederationtls._tcp. &lt; domain &gt; e _sip._tls. &lt; domínio &gt; no DNS interno.</span><span class="sxs-lookup"><span data-stu-id="6718a-141">If this record cannot be resolved internally, then you need to create the records, _sipfederationtls._tcp.&lt;domain&gt; and _sip._tls.&lt;domain&gt; in the internal DNS.</span></span> <span data-ttu-id="6718a-142">Esses registros devem apontar para o endereço IP externo da Interface de Acesso do Servidor de Borda.</span><span class="sxs-lookup"><span data-stu-id="6718a-142">These records should point to the external IP address of the Access Interface of the Edge Server.</span></span>

        
        </div>
    
      - <span data-ttu-id="6718a-143">**HostsOCSUsers** indica se o provedor de hospedagem é usado para hospedar contas do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6718a-143">**HostsOCSUsers** indicates whether the hosting provider is used to host Lync Server 2013 accounts.</span></span> <span data-ttu-id="6718a-144">Se estiver definido como **Falso**, o provedor hospedará outros tipos de conta, como contas do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="6718a-144">If **False**, the provider hosts other account types, such as Microsoft Exchange accounts.</span></span>
    
      - <span data-ttu-id="6718a-p111">**ProxyFQDN** especifica o FQDN (nome de domínio totalmente qualificado) para o servidor proxy usado pelo provedor de hospedagem, neste exemplo, **proxyserver.fabrikam.com**. Esse valor não pode ser modificado. Se o provedor de hospedagem alterar o seu servidor proxy, será necessário excluir e recriar a entrada desse provedor.</span><span class="sxs-lookup"><span data-stu-id="6718a-p111">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider, in this example, **proxyserver.fabrikam.com**. This value cannot be modified. If the hosting provider changes its proxy server you will need to delete and then recreate the entry for that provider.</span></span>
    
      - <span data-ttu-id="6718a-148">**IsLocal** indica se o servidor proxy usado pelo provedor de hospedagem está contido na topologia do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6718a-148">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server 2013 topology.</span></span>
    
      - <span data-ttu-id="6718a-149">**VerficationLevel** indica o nível de verificação permitido para mensagens enviadas para e do provedor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="6718a-149">**VerficationLevel** indicates the allowed verification level for messages sent to and from the hosted provider.</span></span> <span data-ttu-id="6718a-150">Especifique **UseSourceVerification**, que depende do nível de verificação incluído nas mensagens enviadas do provedor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="6718a-150">Specify **UseSourceVerification**, which relies on the verification level included in messages sent from the hosting provider.</span></span> <span data-ttu-id="6718a-151">Se este nível não for especificado, a mensagem será rejeitada como sendo não-verificável.</span><span class="sxs-lookup"><span data-stu-id="6718a-151">If this level is not specified, then the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6718a-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="6718a-152">See Also</span></span>


[<span data-ttu-id="6718a-153">Exportar sua topologia do Lync Server 2013 e copiá-la na mídia externa para instalação de borda</span><span class="sxs-lookup"><span data-stu-id="6718a-153">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)  


[<span data-ttu-id="6718a-154">Verificar conectividade entre servidores internos e Servidores de Borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6718a-154">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)  


<span data-ttu-id="6718a-155">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6718a-155">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span></span>  
  

<span data-ttu-id="6718a-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6718a-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

