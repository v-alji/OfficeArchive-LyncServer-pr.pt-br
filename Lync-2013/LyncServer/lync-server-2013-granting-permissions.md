---
title: 'Lync Server 2013: Concedendo permissões'
description: 'Lync Server 2013: concedendo permissões.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting permissions
ms:assetid: d1c9ea66-bd07-480e-99a0-011108f97e42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398901(v=OCS.15)
ms:contentKeyID: 48185446
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4bdb2b1ef39b85caa89c7597f455e6e4fc08e44e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390300"
---
# <a name="granting-permissions-in-lync-server-2013"></a><span data-ttu-id="e72e8-103">Concedendo permissões no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e72e8-103">Granting permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e72e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e72e8-104">

<span> </span></span></span>

<span data-ttu-id="e72e8-105">_**Tópico da última modificação:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="e72e8-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="e72e8-106">Para a instalação, você pode conceder permissões ao grupo universal RTCUniversalServerAdmins para uma unidade organizacional (OU) específica do Active Directory, permitindo que os membros do grupo RTCUniversalServerAdmins dessa UO instalem o Lync Server 2013 no domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="e72e8-106">For setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain.</span></span> <span data-ttu-id="e72e8-107">Quando você concede permissões para uma OU, são concedidas as seguintes permissões:</span><span class="sxs-lookup"><span data-stu-id="e72e8-107">When you grant permissions for an OU, the following permissions are granted:</span></span>

  - <span data-ttu-id="e72e8-108">Ler</span><span class="sxs-lookup"><span data-stu-id="e72e8-108">Read</span></span>

  - <span data-ttu-id="e72e8-109">Gravação</span><span class="sxs-lookup"><span data-stu-id="e72e8-109">Write</span></span>

  - <span data-ttu-id="e72e8-110">ReadSPN</span><span class="sxs-lookup"><span data-stu-id="e72e8-110">ReadSPN</span></span>

  - <span data-ttu-id="e72e8-111">WriteSPN</span><span class="sxs-lookup"><span data-stu-id="e72e8-111">WriteSPN</span></span>

<span data-ttu-id="e72e8-112">Para administração, você pode adicionar permissões a UOs especificadas para que os membros dos grupos universais do RTC criados pela preparação da floresta possam acessar as UOs sem precisar ser membros do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="e72e8-112">For administration, you can add permissions to specified OUs so that members of the RTC universal groups created by forest preparation can access the OUs without needing to be members of the Domain Admins group.</span></span> <span data-ttu-id="e72e8-113">As permissões adicionadas à UO especificada são as mesmas permissões que o cmdlet **Enable-CsAdDomain** adiciona aos recipientes da ou computadores e usuários.</span><span class="sxs-lookup"><span data-stu-id="e72e8-113">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users OU containers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e72e8-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e72e8-114">In This Section</span></span>

  - [<span data-ttu-id="e72e8-115">Concedendo permissões de configuração no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e72e8-115">Granting setup permissions in Lync Server 2013</span></span>](lync-server-2013-granting-setup-permissions.md)

  - [<span data-ttu-id="e72e8-116">Concedendo permissões de unidade organizacional no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e72e8-116">Granting organizational unit permissions in Lync Server 2013</span></span>](lync-server-2013-granting-organizational-unit-permissions.md)

<span data-ttu-id="e72e8-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e72e8-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

