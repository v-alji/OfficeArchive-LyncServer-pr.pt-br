---
title: 'Lync Server 2013: Set-CsWebServiceConfiguration para gerenciamento de catálogo de endereços'
description: 'Lync Server 2013: Set-CsWebServiceConfiguration para gerenciamento de catálogo de endereços.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set-CsWebServiceConfiguration for Address Book management
ms:assetid: 79d0edf5-23f3-4845-a7b7-e11b5a928bab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429709(v=OCS.15)
ms:contentKeyID: 48184572
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37dcd7676829c5a91e05667fa0ae0d74dc6f7dc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423992"
---
# <a name="set-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="a4b68-103">Set-CsWebServiceConfiguration para gerenciamento de catálogo de endereços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4b68-103">Set-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4b68-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4b68-104">

<span> </span></span></span>

<span data-ttu-id="a4b68-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a4b68-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a4b68-106">Quem pode executar este cmdlet: por padrão, os membros dos grupos a seguir estão autorizados a executar o cmdlet Set-CsWebServiceConfiguration localmente: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="a4b68-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="a4b68-107">Para retornar uma lista de todas as funções de controle de acesso baseado em função (RBAC) às quais esse cmdlet foi atribuído (incluindo qualquer função RBAC personalizada que você criou), execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a4b68-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsWebServiceConfiguration"}

<span data-ttu-id="a4b68-108">O cmdlet Set-CsWebServiceConfiguration permite que o administrador Redefina um atributo existente na configuração dos serviços Web.</span><span class="sxs-lookup"><span data-stu-id="a4b68-108">The Set-CsWebServiceConfiguration cmdlet allows the administrator to redefine an existing attribute in the configuration of the Web Services.</span></span>

<span data-ttu-id="a4b68-109">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a4b68-109">For example:</span></span>

    Set-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $True

<div>

## <a name="see-also"></a><span data-ttu-id="a4b68-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4b68-110">See Also</span></span>


[<span data-ttu-id="a4b68-111">Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4b68-111">Set-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)  
  

<span data-ttu-id="a4b68-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4b68-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

