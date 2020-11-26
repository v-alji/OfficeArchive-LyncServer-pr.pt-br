---
title: 'Lync Server 2013: habilitar o recebimento de chamadas em grupo para usuários e atribuir um número de grupo'
description: 'Lync Server 2013: habilitar o recebimento de chamadas em grupo para usuários e atribuir um número de grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Group Call Pickup for users and assign a group number
ms:assetid: c33bb6c2-d43b-4fb6-a0fa-6d82a7b09abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945650(v=OCS.15)
ms:contentKeyID: 51541517
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a03fcb20bfd88842dc8b29100b9ece595bf76254
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428920"
---
# <a name="enable-group-call-pickup-for-users-in-lync-server-2013-and-assign-a-group-number"></a><span data-ttu-id="9a663-103">Habilitar o recebimento de chamadas em grupo para usuários no Lync Server 2013 e atribuir um número de grupo</span><span class="sxs-lookup"><span data-stu-id="9a663-103">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a663-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a663-104">

<span> </span></span></span>

<span data-ttu-id="9a663-105">_**Tópico da última modificação:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="9a663-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="9a663-106">Depois de adicionar números de grupo de recebimento de chamada à tabela órbita do parque de chamadas, você atribui os números de grupo aos usuários e habilita o recebimento de chamadas em grupo para eles.</span><span class="sxs-lookup"><span data-stu-id="9a663-106">After you add call pickup group numbers to the call park orbit table, you assign the group numbers to users and enable Group Call Pickup for them.</span></span> <span data-ttu-id="9a663-107">Use a ferramenta de kit de recursos de extensão do recurso de extensão secundária (SEFAUtil) para atribuir números de grupo e habilitar a retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="9a663-107">Use the secondary extension feature activation (SEFAUtil) resource kit tool to assign group numbers and enable Group Call Pickup.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9a663-108">Em uma implantação híbrida, não atribua um grupo de recebimento de chamadas em grupo aos usuários que estiverem em casa online.</span><span class="sxs-lookup"><span data-stu-id="9a663-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="9a663-109">Os usuários que estiverem hospedados online não poderão participar da retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="9a663-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="9a663-110">Isso significa que suas chamadas não podem ser atendidas por outros usuários, e eles não podem responder chamadas no lugar de outros usuários.</span><span class="sxs-lookup"><span data-stu-id="9a663-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-number-and-enable-group-call-pickup-for-a-user"></a><span data-ttu-id="9a663-111">Para atribuir um número de grupo e habilitar a retirada de chamadas em grupo para um usuário</span><span class="sxs-lookup"><span data-stu-id="9a663-111">To assign a group number and enable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="9a663-112">Realize logon no computador em que você instalou a ferramenta SEFAUtil com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="9a663-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="9a663-113">Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="9a663-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="9a663-114">Por exemplo, para atribuir o número de grupo 199 a um usuário:</span><span class="sxs-lookup"><span data-stu-id="9a663-114">For example, to assign group number 199 to a user:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199 

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9a663-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a663-115">See Also</span></span>


[<span data-ttu-id="9a663-116">Desabilitar a retirada de chamadas em grupo para usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a663-116">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="9a663-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a663-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

