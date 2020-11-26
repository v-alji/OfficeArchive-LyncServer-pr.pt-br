---
title: 'Lync Server 2013: Get-CsWebServiceConfiguration para gerenciamento de catálogo de endereços'
description: 'Lync Server 2013: Get-CsWebServiceConfiguration para gerenciamento de catálogo de endereços.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsWebServiceConfiguration for Address Book management
ms:assetid: 0b223733-5224-47d1-9b47-2109e6f135c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429692(v=OCS.15)
ms:contentKeyID: 48183372
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb22d7607f9ac18cda9c8653374ae86839b033e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427940"
---
# <a name="get-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="93d11-103">Get-CsWebServiceConfiguration para gerenciamento de catálogo de endereços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93d11-103">Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93d11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93d11-104">

<span> </span></span></span>

<span data-ttu-id="93d11-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="93d11-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="93d11-106">Quem pode executar este cmdlet: por padrão, os membros dos grupos a seguir estão autorizados a executar o cmdlet Get-CsWebServiceConfiguration localmente: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="93d11-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsWebServiceConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="93d11-107">Para retornar uma lista de todas as funções de controle de acesso baseado em função (RBAC) às quais esse cmdlet foi atribuído (incluindo qualquer função RBAC personalizada que você criou), execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="93d11-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsWebServiceConfiguration"}

<span data-ttu-id="93d11-108">Get-CsWebServiceConfiguration retorna informações da configuração de serviços Web atualmente em uso em sua organização.</span><span class="sxs-lookup"><span data-stu-id="93d11-108">Get-CsWebServiceConfiguration returns information of the Web Services configuration currently in use in your organization.</span></span> <span data-ttu-id="93d11-109">De interesse para os serviços de catálogo de endereços é o status da função de expansão da lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="93d11-109">Of interest to the Address Book Services is the status of Distribution List Expansion function.</span></span> <span data-ttu-id="93d11-110">Se o atributo EnableGroupExpansion for verdadeiro, a sua organização atualmente permitirá expansão de grupo.</span><span class="sxs-lookup"><span data-stu-id="93d11-110">If the attribute EnableGroupExpansion is True, your organization currently allows group expansion.</span></span>

<span data-ttu-id="93d11-111">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="93d11-111">For example:</span></span>

    Get-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="93d11-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="93d11-112">See Also</span></span>


[<span data-ttu-id="93d11-113">Get-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="93d11-113">Get-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWebServiceConfiguration)  
  

<span data-ttu-id="93d11-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93d11-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

