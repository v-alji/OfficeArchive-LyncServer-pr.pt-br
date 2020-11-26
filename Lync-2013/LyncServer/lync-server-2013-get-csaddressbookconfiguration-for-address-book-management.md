---
title: 'Lync Server 2013: Get-CsAddressBookConfiguration para gerenciamento de catálogo de endereços'
description: 'Lync Server 2013: Get-CsAddressBookConfiguration para gerenciamento de catálogo de endereços.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsAddressBookConfiguration for Address Book management
ms:assetid: bd62f916-caf3-4e10-ada4-631bbb331ef1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429721(v=OCS.15)
ms:contentKeyID: 48185264
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91b96aead7b7038464f3166691a5952b9ff850dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427975"
---
# <a name="get-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="60fe9-103">Get-CsAddressBookConfiguration para gerenciamento de catálogo de endereços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="60fe9-103">Get-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="60fe9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="60fe9-104">

<span> </span></span></span>

<span data-ttu-id="60fe9-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="60fe9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="60fe9-106">Quem pode executar este cmdlet: por padrão, os membros dos grupos a seguir estão autorizados a executar o cmdlet Get-CsAddressBookConfiguration localmente: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="60fe9-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="60fe9-107">Para retornar uma lista de todas as funções de controle de acesso baseado em função (RBAC) às quais esse cmdlet foi atribuído (incluindo qualquer função RBAC personalizada que você criou), execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="60fe9-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsAddressBookConfiguration"}

<span data-ttu-id="60fe9-108">O cmdlet Get-CsAddressBookConfiguration retorna informações sobre uma configuração que já existe.</span><span class="sxs-lookup"><span data-stu-id="60fe9-108">The cmdlet Get-CsAddressBookConfiguration returns information about a configuration that already exists.</span></span>

<span data-ttu-id="60fe9-109">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="60fe9-109">For example:</span></span>

    Get-CsAddressBookConfiguration -Identity site:Redmond

<span data-ttu-id="60fe9-110">A combinação da funcionalidade de Get-CsAddressBookConfiguration e Set-CsAddressBookConfiguration permite que o administrador defina quais configurações modificar e, em seguida, aplicar as modificações.</span><span class="sxs-lookup"><span data-stu-id="60fe9-110">Combining the functionality of Get-CsAddressBookConfiguration and Set-CsAddressBookConfiguration allows the administrator to define which configurations to modify and then apply the modifications.</span></span> <span data-ttu-id="60fe9-111">Por exemplo, isso combina:</span><span class="sxs-lookup"><span data-stu-id="60fe9-111">For example, this combined:</span></span>

    Get-CsAddressBookConfiguration -Filter site:* | Set-CsAddressBookConfiguration -RunTimeOfDay 23:00

<span data-ttu-id="60fe9-112">Retorna todas as configurações em todos os sites e aplica a RunTimeOfDay de 23:00 horas às configurações.</span><span class="sxs-lookup"><span data-stu-id="60fe9-112">Returns all configurations in all sites and applies the RunTimeOfDay of 23:00 hours to the configurations.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="60fe9-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="60fe9-113">See Also</span></span>


[<span data-ttu-id="60fe9-114">Get-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="60fe9-114">Get-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAddressBookConfiguration)  
  

<span data-ttu-id="60fe9-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="60fe9-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

