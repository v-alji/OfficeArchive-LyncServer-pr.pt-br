---
title: 'Lync Server 2013: Adicionando texto personalizado a mensagens instantâneas'
description: 'Lync Server 2013: adicionar texto personalizado a mensagens instantâneas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding custom text to instant messages
ms:assetid: cabcc3ec-9d35-42ac-a403-e21b7d538c2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398847(v=OCS.15)
ms:contentKeyID: 48185458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54f5cf031da0ba4d5bd0b6dbaa7f5ebc9d0b3a6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439230"
---
# <a name="adding-custom-text-to-instant-messages-in-lync-server-2013"></a><span data-ttu-id="b6bda-103">Adicionando texto personalizado a mensagens instantâneas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6bda-103">Adding custom text to instant messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6bda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6bda-104">

<span> </span></span></span>

<span data-ttu-id="b6bda-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="b6bda-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="b6bda-106">Adicione uma declaração de isenção ou aviso ao início de cada conversa de mensagem instantânea do Lync 2013 usando os cmdlets shell do Shell de gerenciamento do Lync Server **New-CSClientPolicy** ou **set-CSClientPolicy** com o parâmetro imwarning.</span><span class="sxs-lookup"><span data-stu-id="b6bda-106">Add a disclaimer or warning to the beginning of every Lync 2013 instant messaging (IM) conversation by using the **New-CSClientPolicy** or **Set-CSClientPolicy** Lync Server Management Shell cmdlets with the IMWarning parameter.</span></span>

<span data-ttu-id="b6bda-107">O comando no exemplo a seguir adiciona um lembrete de segurança na parte superior da janela de conversa sempre que uma nova conversa de mensagem instantânea começa:</span><span class="sxs-lookup"><span data-stu-id="b6bda-107">The command in the following example adds a security reminder at the top of the Conversation window whenever a new IM conversation begins:</span></span>

    New-CsClientPolicy -Identity IMSecurityNotice -IMWarning 
    "Remember, security is everyone's responsibility. Keep it confidential."

<span data-ttu-id="b6bda-108">Use **Grant-CSClientPolicy** para atribuir esta nova política aos usuários.</span><span class="sxs-lookup"><span data-stu-id="b6bda-108">Use **Grant-CSClientPolicy** to assign this new policy to users.</span></span> <span data-ttu-id="b6bda-109">Para obter detalhes, consulte **New-CSClientPolicy** and **Grant-CSClientPolicy** na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b6bda-109">For details, see **New-CSClientPolicy** and **Grant-CSClientPolicy** in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="b6bda-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6bda-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

