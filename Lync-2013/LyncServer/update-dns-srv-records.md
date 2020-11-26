---
title: Atualizar registros de DNS SRV
description: Atualize os registros SRV DNS.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Update DNS SRV records
ms:assetid: 9542b91a-108c-4980-89ec-634905cbbf26
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688139(v=OCS.15)
ms:contentKeyID: 49733739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24161074e8f3bcf7e296a957588eeb59d5f2ad1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446546"
---
# <a name="update-dns-srv-records"></a><span data-ttu-id="258c4-103">Atualizar registros de DNS SRV</span><span class="sxs-lookup"><span data-stu-id="258c4-103">Update DNS SRV records</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="258c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="258c4-104">

<span> </span></span></span>

<span data-ttu-id="258c4-105">_**Tópico da última modificação:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="258c4-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="258c4-106">Para concluir esse procedimento com êxito, você deve estar conectado ao servidor ou ao domínio como membro do grupo Domain admins ou de um membro do grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="258c4-106">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="258c4-107">Este tópico descreve como atualizar os registros DNS (sistema de nomes de domínio) após a migração para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="258c4-107">This topic describes how to update the Domain Name System (DNS) records after migrating to Lync Server 2013.</span></span> <span data-ttu-id="258c4-108">Depois que todos os usuários tiverem sido movidos para o Lync Server 2013, mas antes de o pool ou diretor herdado do Lync Server 2010 ser encerrado, você deve atualizar os registros SRV DNS no seu DNS interno para cada domínio SIP.</span><span class="sxs-lookup"><span data-stu-id="258c4-108">After all users have been moved to Lync Server 2013, but before the legacy Lync Server 2010 pool or Director is decommissioned, you must update the DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="258c4-109">Este procedimento pressupõe que o seu DNS interno tem zonas para seus domínios de usuário SIP.</span><span class="sxs-lookup"><span data-stu-id="258c4-109">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<span data-ttu-id="258c4-110">**Para configurar um registro SRV DNS**</span><span class="sxs-lookup"><span data-stu-id="258c4-110">**To configure a DNS SRV record**</span></span>

1.  <span data-ttu-id="258c4-111">No servidor DNS, clique em **Iniciar**, clique em **Ferramentas administrativas** e, em seguida, clique em **DNS**.</span><span class="sxs-lookup"><span data-stu-id="258c4-111">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="258c4-112">Na árvore de console do seu domínio SIP, expanda **zonas de pesquisa direta**, expanda o domínio SIP no qual o Lync Server 2013 está instalado e navegue até a configuração **\_ TCP** .</span><span class="sxs-lookup"><span data-stu-id="258c4-112">In the console tree for your SIP domain, expand **Forward Lookup Zones**, expand the SIP domain in which Lync Server 2013 is installed, and navigate to the **\_tcp** setting.</span></span>

3.  <span data-ttu-id="258c4-113">No painel direito, clique com o botão direito do mouse em **\_ sipinternaltls** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="258c4-113">In the right pane, right click **\_sipinternaltls** and select **Properties**.</span></span>

4.  <span data-ttu-id="258c4-114">Em **host oferecendo esse serviço**, atualize o FQDN do host para apontar para o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="258c4-114">In **Host offering this service**, update the host FQDN to point to the Lync Server 2013 pool.</span></span>

5.  <span data-ttu-id="258c4-115">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="258c4-115">Click **OK**.</span></span>

<span data-ttu-id="258c4-116">**Para verificar se o FQDN do servidor de front-end ou do servidor Standard Edition pode ser resolvido**</span><span class="sxs-lookup"><span data-stu-id="258c4-116">**To verify that the FQDN of the Front End pool or Standard Edition server can be resolved**</span></span>

1.  <span data-ttu-id="258c4-117">Faça logon em um computador cliente no domínio.</span><span class="sxs-lookup"><span data-stu-id="258c4-117">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="258c4-118">Clique em  **Iniciar** e em  **Executar**.</span><span class="sxs-lookup"><span data-stu-id="258c4-118">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="258c4-119">Na caixa **abrir** , digite **cmd** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="258c4-119">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="258c4-120">No prompt de comando, digite **nslookup** \<FQDN of the Front End pool\> ou \<FQDN of the Standard Edition server\> , em seguida, pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="258c4-120">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="258c4-121">Verifique se você recebe uma resposta que é resolvida para o endereço IP apropriado para o FQDN.</span><span class="sxs-lookup"><span data-stu-id="258c4-121">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="258c4-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="258c4-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

