---
title: 'Lync Server 2013: Test-CsAddressBookService para gerenciamento de catálogo de endereços'
description: 'Lync Server 2013: Test-CsAddressBookService para gerenciamento de catálogo de endereços.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookService for Address Book management
ms:assetid: b88cea74-41fd-4c0e-9284-7135bff27a27
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429720(v=OCS.15)
ms:contentKeyID: 48185206
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 345886c68c814534fcbfd4debfd3be8562fae5a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444277"
---
# <a name="test-csaddressbookservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="53b98-103">Test-CsAddressBookService para gerenciamento de catálogo de endereços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53b98-103">Test-CsAddressBookService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="53b98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="53b98-104">

<span> </span></span></span>

<span data-ttu-id="53b98-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="53b98-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="53b98-106">Quem pode executar este cmdlet: por padrão, os membros dos grupos a seguir estão autorizados a executar o cmdlet Test-CsAddressBookService: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="53b98-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookService cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="53b98-107">Para retornar uma lista de todas as funções de controle de acesso baseado em função (RBAC) às quais esse cmdlet foi atribuído (incluindo qualquer função RBAC personalizada que você criou), execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="53b98-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

<span data-ttu-id="53b98-108">O Lync Server 2013 contém vários cmdlets que iniciam comandos sintéticos para confirmar se uma função específica ou um recurso está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="53b98-108">Lync Server 2013 contains a number of cmdlets that initiate synthetic commands to confirm that a specific function or feature is working properly.</span></span> <span data-ttu-id="53b98-109">Test-CsAddressBookService confirma que um usuário definido pode se conectar e solicitar os arquivos locais do serviço Web de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="53b98-109">Test-CsAddressBookService confirms that a defined user can connect and request the local files from the Address Book Web service.</span></span>

<span data-ttu-id="53b98-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="53b98-110">For example:</span></span>

    Test-CsAddressBookService -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a><span data-ttu-id="53b98-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="53b98-111">See Also</span></span>


[<span data-ttu-id="53b98-112">Test-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="53b98-112">Test-CsAddressBookService</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService)  
  

<span data-ttu-id="53b98-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="53b98-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

