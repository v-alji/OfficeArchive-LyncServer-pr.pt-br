---
title: 'Lync Server 2013: Adicionando um link personalizado às mensagens de erro do Lync'
description: 'Lync Server 2013: adicionar um link personalizado para mensagens de erro do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding a custom link to Lync error messages
ms:assetid: de756088-fcc3-4e47-bde8-4fa4cc852fd1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398979(v=OCS.15)
ms:contentKeyID: 48185607
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a5d333b6f27e10e5092de23fcdf1d37fd75e75a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439279"
---
# <a name="adding-a-custom-link-to-lync-error-messages-in-lync-server-2013"></a><span data-ttu-id="9c139-103">Adicionando um link personalizado às mensagens de erro do Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c139-103">Adding a custom link to Lync error messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c139-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c139-104">

<span> </span></span></span>

<span data-ttu-id="9c139-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="9c139-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="9c139-106">Personalize mensagens de erro do Lync 2013 adicionando um link para suas próprias informações de solução de problemas ou suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="9c139-106">Customize Lync 2013 error messages by adding a link to your own troubleshooting or help desk information.</span></span> <span data-ttu-id="9c139-107">Para fazer isso, use os cmdlets shell do Shell de gerenciamento do Lync Server **New-CSClientPolicy** ou **set-CSClientPolicy** com o parâmetro CustomLinkInErrorMessages.</span><span class="sxs-lookup"><span data-stu-id="9c139-107">To do this, use the **New-CSClientPolicy** or **Set-CSClientPolicy** Lync Server Management Shell cmdlets with the CustomLinkInErrorMessages parameter.</span></span> <span data-ttu-id="9c139-108">O texto do link personalizado é "clique aqui para obter tópicos de suporte do administrador" e não pode ser personalizado.</span><span class="sxs-lookup"><span data-stu-id="9c139-108">The text of the custom link is "Click here for support topics from your administrator," and it cannot be customized.</span></span>

<span data-ttu-id="9c139-109">Por exemplo, o comando a seguir faz com que o link personalizado apareça na área de notas de rodapé de cada mensagem de erro do Lync 2013 e define o destino do link como http://contoso.com/help/LyncHelpDesk.aspx:</span><span class="sxs-lookup"><span data-stu-id="9c139-109">For example, the following command causes the custom link to appear in the footnote area of every Lync 2013 error message and sets the link destination to http://contoso.com/help/LyncHelpDesk.aspx:</span></span>

    New-CsClientPolicy -Identity LyncErrorLink -CustomLinkInErrorMessages "http://contoso/help/LyncHelpDesk.aspx"

<span data-ttu-id="9c139-110">Use **Grant-CSClientPolicy** para atribuir esta nova política aos usuários.</span><span class="sxs-lookup"><span data-stu-id="9c139-110">Use **Grant-CSClientPolicy** to assign this new policy to users.</span></span> <span data-ttu-id="9c139-111">Para obter detalhes, consulte **New-CSClientPolicy** and **Grant-CSClientPolicy** na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9c139-111">For details, see **New-CSClientPolicy** and **Grant-CSClientPolicy** in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="9c139-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c139-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

