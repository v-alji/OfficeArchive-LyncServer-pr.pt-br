---
title: 'Lync Server 2013: Gerenciando chamadas para números não atribuídos'
description: 'Lync Server 2013: Gerenciando chamadas para números não atribuídos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing calls to unassigned numbers
ms:assetid: a45a7546-5ee6-4c1e-ab13-20a71a058f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688167(v=OCS.15)
ms:contentKeyID: 49733772
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a91c1ec30ea1e942fa3ea27fbcd369572884a52a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390096"
---
# <a name="managing-calls-to-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="80560-103">Gerenciando chamadas para números não atribuídos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80560-103">Managing calls to unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80560-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80560-104">

<span> </span></span></span>

<span data-ttu-id="80560-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="80560-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="80560-106">O Lync Server permite que você configure a manipulação de chamadas telefônicas de entrada quando o número discado é válido para a sua organização, mas não é atribuído a um usuário ou telefone.</span><span class="sxs-lookup"><span data-stu-id="80560-106">Lync Server lets you configure the handling of incoming phone calls when the dialed number is valid for your organization, but is not assigned to a user or phone.</span></span> <span data-ttu-id="80560-107">Você pode usar o aplicativo de anúncio para transferir essas chamadas para um destino predeterminado (número de telefone, URI de SIP ou caixa postal) ou executar um anúncio de áudio ou ambos.</span><span class="sxs-lookup"><span data-stu-id="80560-107">You can use the Announcement application to transfer these calls to a predetermined destination (phone number, SIP URI, or voice mail), or play an audio announcement, or both.</span></span> <span data-ttu-id="80560-108">Você também pode transferir essas chamadas para um número de telefone de atendedor automático do Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="80560-108">You can also transfer these calls to an Exchange UM Auto Attendant phone number.</span></span> <span data-ttu-id="80560-109">A manipulação de chamadas para números não atribuídos de uma dessas maneiras ajuda você a evitar as situações em que um chamador disca sem erros e ouve um tom ocupado, ou o cliente SIP recebe uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="80560-109">Handling calls to unassigned numbers in one of these ways helps you avoid the situations in which a caller misdials and then hears a busy tone, or the SIP client receives an error message.</span></span>

<span data-ttu-id="80560-110">Esta seção descreve como gerenciar intervalos de números não atribuídos para manipular chamadas para números de telefone não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="80560-110">This section describes how to manage unassigned number ranges to handle calls to unassigned phone numbers.</span></span> <span data-ttu-id="80560-111">A seção também descreve como gerenciar anúncios durante a recuperação de desastres se desejar essa funcionalidade durante uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="80560-111">The section also describes how to manage Announcements during disaster recovery if you want this functionality during an outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="80560-112">Usar a manipulação de número não atribuído durante uma interrupção é opcional.</span><span class="sxs-lookup"><span data-stu-id="80560-112">Using unassigned number handling during an outage is optional.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="80560-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="80560-113">In This Section</span></span>

  - [<span data-ttu-id="80560-114">Criar um anúncio no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80560-114">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="80560-115">Configurar números de telefone não atribuídos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80560-115">Configure unassigned phone numbers in Lync Server 2013</span></span>](lync-server-2013-configure-unassigned-phone-numbers.md)

  - [<span data-ttu-id="80560-116">Gerenciar comunicados durante recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80560-116">Manage announcements during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-announcements-during-disaster-recovery.md)

<span data-ttu-id="80560-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80560-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

