---
title: 'Lync Server 2013: exibir informações sobre troncos SIP individuais'
description: 'Lync Server 2013: exibir informações sobre troncos SIP individuais.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View information about individual SIP trunks
ms:assetid: adfacb74-7ea5-4c53-934e-ba7ec59879eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721847(v=OCS.15)
ms:contentKeyID: 49733780
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55c2f9fb1df4e916615cf7f95f95ae167d7216ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446301"
---
# <a name="view-information-about-individual-sip-trunks-in-lync-server-2013"></a><span data-ttu-id="7c5e1-103">Exibir informações sobre troncos SIP individuais no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c5e1-103">View information about individual SIP trunks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c5e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c5e1-104">

<span> </span></span></span>

<span data-ttu-id="7c5e1-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="7c5e1-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="7c5e1-106">Os troncos SIP são usados para conectar a rede de telefone IP do Lync Server 2013 com a rede telefônica comutada pública.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-106">SIP trunks are used to connect Lync Server 2013 Voice over IP phone network with the Public Switched Telephone Network.</span></span> <span data-ttu-id="7c5e1-107">Na versão anterior do produto, os troncos foram usados para rotear chamadas de saída de um Servidor de Mediação para um gateway PSTN e cada gateway estava limitado a um único tronco.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-107">In previous version of the product, trunks were used to route outbound calls from a Mediation Server to a PSTN gateway and each gateway was limited to a single trunk.</span></span> <span data-ttu-id="7c5e1-108">Como resultado, um gateway PSTN e um tronco SIP eram essencialmente idênticos.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-108">As a result, a PSTN gateway and a SIP trunk were essentially identical.</span></span> <span data-ttu-id="7c5e1-109">Para os administradores, isso significava que seria possível exibir informações sobre um tronco SIP individual simplesmente exibindo informações sobre o gateway PSTN associado.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-109">For administrators, that meant they could view information about an individual SIP trunk simply by viewing information about the associated PSTN gateway.</span></span>

<span data-ttu-id="7c5e1-110">No Lync Server 2013, no entanto, vários troncos agora podem ser atribuídos a um único gateway PSTN; Isso significa que os gateways e troncos não são mais um e iguais.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-110">In Lync Server 2013, however, multiple trunks can now be assigned to a single PSTN gateway; this means that gateways and trunks are no longer one and the same.</span></span> <span data-ttu-id="7c5e1-111">Por outro lado, isso significa que os administradores devem usar o novo cmdlet [Get-CsTrunk](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk) para exibir informações sobre um tronco SIP individual.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-111">In turn, that means that administrators must use the new [Get-CsTrunk](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunk) cmdlet in order to view information about an individual SIP trunk.</span></span>

<span data-ttu-id="7c5e1-112">O cmdlet Get-CsTrunk pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-112">The Get-CsTrunk cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="7c5e1-113">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="7c5e1-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-information-for-all-your-sip-trunks"></a><span data-ttu-id="7c5e1-114">Para visualizar as informações de todos os seus troncos SIP</span><span class="sxs-lookup"><span data-stu-id="7c5e1-114">To view information for all your SIP trunks</span></span>

  - <span data-ttu-id="7c5e1-115">O seguinte comando retorna informações sobre todos os troncos SIP usados em sua organização:</span><span class="sxs-lookup"><span data-stu-id="7c5e1-115">The following command returns information about all the SIP trunks in use in your organization:</span></span>
    
        Get-CsTrunk

</div>

<div>

## <a name="to-view-information-for-a-specific-sip-trunk"></a><span data-ttu-id="7c5e1-116">Para visualizar as informações de um tronco SIP específico</span><span class="sxs-lookup"><span data-stu-id="7c5e1-116">To view information for a specific SIP trunk</span></span>

  - <span data-ttu-id="7c5e1-117">Este comando retorna informações somente para o tronco SIP com a Identidade PstnGateway:192.168.0.240:</span><span class="sxs-lookup"><span data-stu-id="7c5e1-117">This command returns information only for the SIP trunk with the Identity PstnGateway:192.168.0.240:</span></span>
    
        Get-CsTrunk -Identity "PstnGateway:192.168.0.240"

</div>

<div>

## <a name="viewing-information-for-all-the-sip-trunks-assigned-to-a-pool"></a><span data-ttu-id="7c5e1-118">Exibir informações de todos os troncos SIP atribuídos a um pool</span><span class="sxs-lookup"><span data-stu-id="7c5e1-118">Viewing Information for All the SIP Trunks Assigned to a Pool</span></span>

  - <span data-ttu-id="7c5e1-119">Neste exemplo, as informações são retornadas para todos os troncos SIP atribuídos ao pool atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="7c5e1-119">In this example, information is returned for all the SIP trunks assigned to the pool atl-cs-001.litwareinc.com:</span></span>
    
        Get-CsTrunk -PoolFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="7c5e1-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c5e1-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

