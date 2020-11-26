---
title: 'Lync Server 2013: Certifique-se de que os planos de discagem têm opções atribuídas'
description: 'Lync Server 2013: Certifique-se de que os planos de discagem tenham regiões atribuídas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Make sure dial plans have assigned regions
ms:assetid: 3da3a907-0dbf-4440-b12f-370f94dd4c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425903(v=OCS.15)
ms:contentKeyID: 48183937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c055eda221bc03de449631ba38483165a8621773
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426148"
---
# <a name="make-sure-dial-plans-lync-server-2013-have-assigned-regions"></a><span data-ttu-id="25e0e-103">Verifique se os planos de discagem do Lync Server 2013 atribuiram regiões</span><span class="sxs-lookup"><span data-stu-id="25e0e-103">Make sure dial plans Lync Server 2013 have assigned regions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25e0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25e0e-104">

<span> </span></span></span>

<span data-ttu-id="25e0e-105">_**Tópico da última modificação:** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="25e0e-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="25e0e-106">Os planos de discagem que são usados para conferência discada precisam ter uma **região de conferência discada** especificada para associar números de acesso à conferência discada com o plano de discagem apropriado.</span><span class="sxs-lookup"><span data-stu-id="25e0e-106">Dial plans that are used for dial-in conferencing need to have a **Dial-in conferencing region** specified to associate dial-in conferencing access numbers with the appropriate dial plan.</span></span> <span data-ttu-id="25e0e-107">Ao configurar um plano de discagem, você especifica a região de conferência discada que se aplica ao plano de discagem.</span><span class="sxs-lookup"><span data-stu-id="25e0e-107">When you set up a dial plan, you specify the dial-in conferencing region that applies to that dial plan.</span></span> <span data-ttu-id="25e0e-108">Em seguida, ao criar o número de acesso de discagem, selecione as regiões que associam o número de acesso com os planos de discagem apropriados.</span><span class="sxs-lookup"><span data-stu-id="25e0e-108">Then, when you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="25e0e-109">Como é importante especificar uma região para todos os planos de discagem, recomendamos que você use este procedimento para verificar se todos os planos de discagem têm regiões.</span><span class="sxs-lookup"><span data-stu-id="25e0e-109">Because it important to specify a region for all dial plans, we recommend that you use this procedure to verify that all dial plans have regions.</span></span> <span data-ttu-id="25e0e-110">Esta etapa é opcional.</span><span class="sxs-lookup"><span data-stu-id="25e0e-110">This step is optional.</span></span>

<span data-ttu-id="25e0e-111">Use o cmdlet **Get-CsDialPlan** para verificar se a região está definida para todos os planos de discagem de conferência discada.</span><span class="sxs-lookup"><span data-stu-id="25e0e-111">Use the **Get-CsDialPlan** cmdlet to verify whether the region is set for all dial-in conferencing dial plans.</span></span> <span data-ttu-id="25e0e-112">Se a região não existir nos planos de discagem, você poderá usar o cmdlet **Set-CsDialPlan** para defini-la.</span><span class="sxs-lookup"><span data-stu-id="25e0e-112">If the region is missing from dial plans, you can use the **Set-CsDialPlan** cmdlet to set the region.</span></span> <span data-ttu-id="25e0e-113">Você também pode usar o painel de controle do Lync Server para atualizar a região em planos de discagem existentes.</span><span class="sxs-lookup"><span data-stu-id="25e0e-113">You can also use Lync Server Control Panel to update the region in existing dial plans.</span></span> <span data-ttu-id="25e0e-114">Para obter detalhes sobre como usar o painel de controle do Lync Server, consulte [modificar um plano de discagem no Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="25e0e-114">For details about using Lync Server Control Panel, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

<div>

## <a name="to-verify-whether-dial-plans-have-the-region-property-set"></a><span data-ttu-id="25e0e-115">Para verificar se os planos de discagem têm a propriedade de região definida</span><span class="sxs-lookup"><span data-stu-id="25e0e-115">To verify whether dial plans have the region property set</span></span>

1.  <span data-ttu-id="25e0e-116">Efetue logon no computador como membro do grupo RTCUniversalServerAdmins ou como membro da função **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** ou **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="25e0e-116">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="25e0e-117">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="25e0e-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="25e0e-118">Execute o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="25e0e-118">Run the following at the command prompt:</span></span>
    
        Get-CsDialPlan [-Identity <Identifier of the dial plans to be retrieved>]
    
    <span data-ttu-id="25e0e-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="25e0e-119">For example:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="25e0e-120">Neste exemplo, todos os planos de discagem configurados para sua organização são retornados.</span><span class="sxs-lookup"><span data-stu-id="25e0e-120">In this example, all the dial plans configured for your organization are returned.</span></span>

4.  <span data-ttu-id="25e0e-121">Revise os planos de discagem retornados para identificar todos que estão faltando na região da conferência discada.</span><span class="sxs-lookup"><span data-stu-id="25e0e-121">Review the returned dial plans to identify any that are missing the dial-in conferencing region.</span></span> <span data-ttu-id="25e0e-122">Para obter detalhes, consulte a documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="25e0e-122">For details, see the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-set-the-region-property-for-a-dial-plan"></a><span data-ttu-id="25e0e-123">Para definir a propriedade de região de um plano de discagem</span><span class="sxs-lookup"><span data-stu-id="25e0e-123">To set the region property for a dial plan</span></span>

1.  <span data-ttu-id="25e0e-124">Efetue logon no computador como membro do grupo RTCUniversalServerAdmins ou como membro da função **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** ou **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="25e0e-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="25e0e-125">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="25e0e-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="25e0e-126">Para todos os planos de discagem que não têm a região de conferência discada, execute:</span><span class="sxs-lookup"><span data-stu-id="25e0e-126">For any dial plans that are missing the dial-in conferencing region, run:</span></span>
    
        Set-CsDialPlan [-Identity <Identity of the dial plan to be modified>] -DialinConferencingRegion "<new region>"
    
    <span data-ttu-id="25e0e-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="25e0e-127">For example:</span></span>
    
        Set-CsDialPlan -Identity Redmond -DialinConferencingRegion "US West Coast"
    
    <span data-ttu-id="25e0e-128">Neste exemplo, o plano de discagem com Identidade de Redmond é modificado para definir a propriedade DialinConferencingRegion como "Costa Leste dos EUA".</span><span class="sxs-lookup"><span data-stu-id="25e0e-128">In this example, the dial plan with the Identity of Redmond is modified to set the DialinConferencingRegion property to "US West Coast".</span></span> <span data-ttu-id="25e0e-129">Para obter detalhes, consulte a documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="25e0e-129">For details, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="25e0e-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25e0e-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

