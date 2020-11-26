---
title: 'Lync Server 2013: (opcional) definir conjuntos de feriados do grupo de resposta'
description: 'Lync Server 2013: (opcional) defina os conjuntos de feriados do grupo de resposta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Define Response Group holiday sets
ms:assetid: 56c37b3b-6517-49b9-86b7-ae48cc349119
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688063(v=OCS.15)
ms:contentKeyID: 49733657
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7ba735cc62efb9d5553c8bd6aad1aa9484f70f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424895"
---
# <a name="optional-define-response-group-holiday-sets-in-lync-server-2013"></a><span data-ttu-id="0b88e-103">Adicionais Definir conjuntos de feriados do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b88e-103">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b88e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b88e-104">

<span> </span></span></span>

<span data-ttu-id="0b88e-105">_**Tópico da última modificação:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="0b88e-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="0b88e-p101">As configurações de feriados definem os dias nos quais um grupo de respostas estará fechado para negócios e especificam a ação a ser tomada nesses dias. Um conjunto de feriados é a coleção de feriados que se aplicam a um grupo de respostas.</span><span class="sxs-lookup"><span data-stu-id="0b88e-p101">Holiday settings define the days that a response group is closed for business and specify the action to take on those days. A holiday set is the collection of holidays that apply to a response group.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0b88e-108">Se um fluxo de trabalho for definido como um fluxo de trabalho gerenciado, então qualquer usuário que estiver atribuído à função CsResponseGroupManager poderá definir e modificar feriados para fluxos de trabalho que eles gerenciam.</span><span class="sxs-lookup"><span data-stu-id="0b88e-108">If a workflow is defined as a Managed workflow, then any user is assigned the CsResponseGroupManager role can set and modify holidays for workflows that they manage.</span></span>



</div>

<div>

## <a name="to-create-a-holiday-set"></a><span data-ttu-id="0b88e-109">Para criar um conjunto de feriados</span><span class="sxs-lookup"><span data-stu-id="0b88e-109">To create a holiday set</span></span>

1.  <span data-ttu-id="0b88e-110">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="0b88e-110">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="0b88e-111">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="0b88e-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="0b88e-112">Para cada feriado que você deseja definir, execute:</span><span class="sxs-lookup"><span data-stu-id="0b88e-112">For each holiday you want to define, run:</span></span>
    
        $x = New-CsRgsHoliday [-Name <holiday name>] -StartDate <starting date of holiday> -EndDate <ending date of holiday>
    
    <span data-ttu-id="0b88e-113">Para criar o conjunto de feriados que contém os feriados que você definiu, execute:</span><span class="sxs-lookup"><span data-stu-id="0b88e-113">To create the holiday set that contains the holidays you defined, run:</span></span>
    
        New-CsRgsHolidaySet -Parent <service where the workflow is hosted> -Name <unique name for holiday set> -HolidayList <one or more holidays to be included in the holiday set>
    
    <span data-ttu-id="0b88e-114">O exemplo a seguir mostra um conjunto de feriados que inclui dois feriados:</span><span class="sxs-lookup"><span data-stu-id="0b88e-114">The following example shows a holiday set that includes two holidays:</span></span>
    
        $a = New-CsRgsHoliday -Name "New Year's Day" -StartDate "1/1/2013 12:00 AM" -EndDate "1/1/2013 12:00 AM" 
        $b = New-CsRgsHoliday -Name "Independence Day" -StartDate "7/4/2013 12:00 AM" -EndDate "7/5/2013 12:00 AM" 
        New-CsRgsHolidaySet -Parent "ApplicationServer:Redmond.contoso.com -Name "2013 Holidays" -HolidayList ($a, $b)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0b88e-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b88e-115">See Also</span></span>


[<span data-ttu-id="0b88e-116">Criar ou modificar um fluxo de trabalho de grupo coletivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b88e-116">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)  
[<span data-ttu-id="0b88e-117">Criar ou modificar um fluxo de trabalho interativo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b88e-117">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)  


[<span data-ttu-id="0b88e-118">New-CsRgsHoliday</span><span class="sxs-lookup"><span data-stu-id="0b88e-118">New-CsRgsHoliday</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsHoliday)  
[<span data-ttu-id="0b88e-119">New-CsRgsHolidaySet</span><span class="sxs-lookup"><span data-stu-id="0b88e-119">New-CsRgsHolidaySet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsHolidaySet)  
  

<span data-ttu-id="0b88e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b88e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

