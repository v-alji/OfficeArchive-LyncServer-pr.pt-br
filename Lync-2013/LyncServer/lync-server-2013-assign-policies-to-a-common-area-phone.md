---
title: 'Lync Server 2013: atribuir políticas a um telefone comum de área'
description: 'Lync Server 2013: atribuir políticas a um telefone comum de área.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign policies to a common area phone
ms:assetid: f0554fd1-b237-49b3-9eb4-26f4b91f5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994082(v=OCS.15)
ms:contentKeyID: 51803993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe437ec87ba30eff834239db2b4815adb2d5718c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438313"
---
# <a name="assign-policies-in-lync-server-2013-to-a-common-area-phone"></a><span data-ttu-id="5cefe-103">Atribuir políticas no Lync Server 2013 a um telefone de área comum</span><span class="sxs-lookup"><span data-stu-id="5cefe-103">Assign policies in Lync Server 2013 to a common area phone</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5cefe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5cefe-104">

<span> </span></span></span>

<span data-ttu-id="5cefe-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="5cefe-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="5cefe-106">Depois de criar sua política para telefones celulares comuns (para obter detalhes, consulte [criar uma política de voz e configurar registros de uso PSTN no Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), você pode atribuir a política a um telefone comum usando o Windows PowerShell e o cmdlet **Grant-cs** apropriado.</span><span class="sxs-lookup"><span data-stu-id="5cefe-106">After you create your policy for common area phones (for details, see [Create a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), you can assign the policy to a common area phone by using Windows PowerShell and the appropriate **Grant-Cs** cmdlet.</span></span> <span data-ttu-id="5cefe-107">Esses cmdlets podem ser executados no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cefe-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="5cefe-108">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="5cefe-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="assigning-a-policy-to-a-single-common-area-phone"></a><span data-ttu-id="5cefe-109">Atribuir uma política a um único telefone de área comum</span><span class="sxs-lookup"><span data-stu-id="5cefe-109">Assigning a Policy to a Single Common Area Phone</span></span>

  - <span data-ttu-id="5cefe-110">O comando a seguir atribui a política de voz por usuário RedmondVoice para o telefone de área comum que tem a identidade prédio 14 lobby.</span><span class="sxs-lookup"><span data-stu-id="5cefe-110">The following command assigns the per-user voice policy RedmondVoice to the common area phone that has the Identity Building 14 Lobby.</span></span>
    
        Grant-CsVoicePolicy -Identity "Building 14 Lobby" -PolicyName "RedmondVoicePolicy"

</div>

<div>

## <a name="assigning-a-policy-to-multiple-common-area-phones"></a><span data-ttu-id="5cefe-111">Atribuir uma política a vários telefones comuns de área</span><span class="sxs-lookup"><span data-stu-id="5cefe-111">Assigning a Policy to Multiple Common Area Phones</span></span>

  - <span data-ttu-id="5cefe-112">Neste exemplo, a política de voz por usuário RedmondVoice é atribuída a todos os telefones de área comuns configurados para uso na organização.</span><span class="sxs-lookup"><span data-stu-id="5cefe-112">In this example, the per-user voice policy RedmondVoice is assigned to all the common area phones configured for use in the organization.</span></span>
    
        Get-CsCommonAreaPhone | Grant-CsVoicePolicy  -PolicyName "RedmondVoicePolicy"

</div>

<span data-ttu-id="5cefe-113">Para obter detalhes, consulte os tópicos da ajuda para o [Grant-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy).</span><span class="sxs-lookup"><span data-stu-id="5cefe-113">For details, see the Help topics for the [Grant-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5cefe-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cefe-114">See Also</span></span>


[<span data-ttu-id="5cefe-115">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="5cefe-115">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="5cefe-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5cefe-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

