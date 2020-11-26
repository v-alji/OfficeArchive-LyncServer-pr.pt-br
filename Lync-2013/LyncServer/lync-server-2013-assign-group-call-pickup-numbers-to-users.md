---
title: 'Lync Server 2013: atribuir números de recebimento de chamadas em grupo aos usuários'
description: 'Lync Server 2013: atribuir números de recebimento de chamadas em grupo aos usuários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign Group Call Pickup numbers to users
ms:assetid: b8e79275-8e7e-4799-b908-f34f61df22f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945647(v=OCS.15)
ms:contentKeyID: 51541508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d550b4556af427e11e99ffb26fb2a6c34d019490
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438341"
---
# <a name="assign-group-call-pickup-numbers-to-users-in-lync-server-2013"></a><span data-ttu-id="1e6ce-103">Atribuir números de recebimento de chamadas em grupo aos usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e6ce-103">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1e6ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1e6ce-104">

<span> </span></span></span>

<span data-ttu-id="1e6ce-105">_**Tópico da última modificação:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="1e6ce-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="1e6ce-106">Depois de adicionar números de grupo de recebimento de chamada em grupo à tabela órbita do parque de chamadas, você pode atribuir os grupos aos usuários.</span><span class="sxs-lookup"><span data-stu-id="1e6ce-106">After you add Group Call Pickup group numbers to the call park orbit table, you can assign the groups to users.</span></span> <span data-ttu-id="1e6ce-107">Use a ferramenta de kit de recursos de extensão do recurso de extensão secundária (SEFAUtil) para atribuir grupos de separação de chamadas a usuários.</span><span class="sxs-lookup"><span data-stu-id="1e6ce-107">Use the secondary extension feature activation (SEFAUtil ) resource kit tool to assign call pickup groups to users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1e6ce-108">Em uma implantação híbrida, não atribua um grupo de recebimento de chamadas em grupo aos usuários que estiverem em casa online.</span><span class="sxs-lookup"><span data-stu-id="1e6ce-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="1e6ce-109">Os usuários que estiverem hospedados online não poderão participar da retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="1e6ce-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="1e6ce-110">Isso significa que suas chamadas não podem ser atendidas por outros usuários, e eles não podem responder chamadas no lugar de outros usuários.</span><span class="sxs-lookup"><span data-stu-id="1e6ce-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-call-pickup-group-to-a-user"></a><span data-ttu-id="1e6ce-111">Para atribuir um grupo de recebimento de chamadas em grupo a um usuário</span><span class="sxs-lookup"><span data-stu-id="1e6ce-111">To assign a Group Call Pickup group to a user</span></span>

1.  <span data-ttu-id="1e6ce-112">Realize logon no computador em que você instalou a ferramenta SEFAUtil com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="1e6ce-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="1e6ce-113">Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="1e6ce-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="1e6ce-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1e6ce-114">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1e6ce-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e6ce-115">See Also</span></span>


[<span data-ttu-id="1e6ce-116">Habilitar a retirada de chamadas em grupo para usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e6ce-116">Enable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-group-call-pickup-for-users.md)  
[<span data-ttu-id="1e6ce-117">Desabilitar a retirada de chamadas em grupo para usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e6ce-117">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="1e6ce-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1e6ce-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

