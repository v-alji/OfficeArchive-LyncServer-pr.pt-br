---
title: 'Lync Server 2013: Configurar número de acesso da conferência discada'
description: 'Lync Server 2013: configurar números de acesso de conferência discada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing access numbers
ms:assetid: d8a18030-f318-43dd-834d-70e5014b5e8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398952(v=OCS.15)
ms:contentKeyID: 48185623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0edb3492c243b36b69c4b48df8c22adc4ece7999
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390366"
---
# <a name="configure-dial-in-conferencing-access-numbers-in-lync-server-2013"></a><span data-ttu-id="9ea85-103">Configurar número de acesso da conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9ea85-103">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9ea85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9ea85-104">

<span> </span></span></span>

<span data-ttu-id="9ea85-105">_**Tópico da última modificação:** 2011-07-17_</span><span class="sxs-lookup"><span data-stu-id="9ea85-105">_**Topic Last Modified:** 2011-07-17_</span></span>

<span data-ttu-id="9ea85-106">Ao implantar uma conferência discada, você precisa configurar números de telefone que os usuários poderão discar da PSTN para participar da parte de áudio das conferências.</span><span class="sxs-lookup"><span data-stu-id="9ea85-106">When you deploy dial-in conferencing, you need to set up phone numbers that users can dial from the public switched telephone network (PSTN) to join the audio portion of conferences.</span></span> <span data-ttu-id="9ea85-107">Esses números de acesso de discagem aparecem nos convites de reunião e na página Configurações de Conferência Discada.</span><span class="sxs-lookup"><span data-stu-id="9ea85-107">These dial-in access numbers appear in meeting invitations and on the Dial-in Conferencing Settings webpage.</span></span>

<span data-ttu-id="9ea85-108">Antes de criar números de acesso discado, primeiro você precisa planejar as regiões de conferência discada e, em seguida, configurar os planos de discagem nas regiões.</span><span class="sxs-lookup"><span data-stu-id="9ea85-108">Before you can create dial-in access numbers, you must first plan your dial-in conferencing regions and then configure dial plans with the regions.</span></span> <span data-ttu-id="9ea85-109">Para obter detalhes sobre regiões, consulte [requisitos de conferência discada no Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="9ea85-109">For details about regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span> <span data-ttu-id="9ea85-110">Para obter detalhes sobre como configurar planos de discagem para conferência discada, consulte [configurar planos de discagem para conferência discada no Lync Server 2013](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-110">For details about configuring dial plans for dial-in conferencing, see [Configure dial plans for dial-in conferencing in Lync Server 2013](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9ea85-111">Você não pode usar um novo número de acesso discada até que a duplicação dos serviços de domínio Active Directory (AD &nbsp; DS) desse número de acesso seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9ea85-111">You cannot use a new dial-in access number until Active Directory Domain Services (AD&nbsp;DS) replication of that access number is complete.</span></span> <span data-ttu-id="9ea85-112">A replicação pode demorar algumas horas para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="9ea85-112">Replication can take several hours to complete.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="9ea85-113">Após a criação dos números de acesso discado, é possível modificar o nome de exibição dos objetos de contato do Active Directory de modo que os usuários possam identificar com mais facilidade o número de acesso correto.</span><span class="sxs-lookup"><span data-stu-id="9ea85-113">After you create dial-in access numbers, you can modify the display name for the Active Directory contact objects so that users can more easily identify the correct access number.</span></span> <span data-ttu-id="9ea85-114">Use o cmdlet <STRONG>set-CsDialInConferencingAccessNumber</STRONG> para modificar o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="9ea85-114">Use the <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> cmdlet to modify the display name.</span></span> <span data-ttu-id="9ea85-115">Não modifique os objetos do Active Directory manualmente.</span><span class="sxs-lookup"><span data-stu-id="9ea85-115">You should not modify Active Directory objects manually.</span></span> <span data-ttu-id="9ea85-116">Para obter detalhes sobre como modificar um número de acesso, consulte documentação do Shell de gerenciamento do Lync Server para o cmdlet <STRONG>set-CsDialInConferencingAccessNumber</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="9ea85-116">For details about modifying an access number, see Lync Server Management Shell documentation for the <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> cmdlet.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9ea85-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9ea85-117">In This Section</span></span>

[<span data-ttu-id="9ea85-118">Criar ou modificar um número de acesso de conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9ea85-118">Create or modify a dial-in conferencing access number in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-dial-in-conferencing-access-number.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9ea85-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ea85-119">See Also</span></span>


[<span data-ttu-id="9ea85-120">Requisitos de conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9ea85-120">Dial-in conferencing requirements in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-requirements.md)  


[<span data-ttu-id="9ea85-121">Configurar planos de discagem para conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9ea85-121">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)  
  

<span data-ttu-id="9ea85-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9ea85-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

