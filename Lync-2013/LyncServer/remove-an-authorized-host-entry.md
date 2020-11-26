---
title: Remover uma entrada de host autorizado
description: Remover uma entrada de host autorizado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove an authorized host entry
ms:assetid: 56a04140-347e-4eef-bede-0e858534f71e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204902(v=OCS.15)
ms:contentKeyID: 48184177
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95aa8df1745ad3108654fcb9b441b5919d42ec40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443255"
---
# <a name="remove-an-authorized-host-entry"></a><span data-ttu-id="3d55b-103">Remover uma entrada de host autorizado</span><span class="sxs-lookup"><span data-stu-id="3d55b-103">Remove an authorized host entry</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3d55b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3d55b-104">

<span> </span></span></span>

<span data-ttu-id="3d55b-105">_**Tópico da última modificação:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="3d55b-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="3d55b-106">Este tópico descreve como remover uma entrada de host autorizado herdada (conhecida como uma *entrada de aplicativo confiável* no Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="3d55b-106">This topic describes how to remove a legacy authorized host entry (known as a *trusted application entry* in Lync Server 2013).</span></span> <span data-ttu-id="3d55b-107">Você deve remover entradas de host autorizadas existentes para quaisquer gateways SIP/CSTA na sua implantação do Office Communications Server 2007 R2 ao migrar o controle de chamada remota para uma implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3d55b-107">You must remove existing authorized host entries for any SIP/CSTA gateways in your Office Communications Server 2007 R2 deployment when you migrate remote call control to a Lync Server 2013 deployment.</span></span> <span data-ttu-id="3d55b-108">Você deve usar as ferramentas administrativas incluídas no Office Communications Server 2007 R2 para remover as entradas de host autorizadas existentes.</span><span class="sxs-lookup"><span data-stu-id="3d55b-108">You must use the administrative tools included with Office Communications Server 2007 R2 to remove the existing authorized host entries.</span></span>

<div>

## <a name="to-remove-an-authorized-host-entry-in-an-office-communications-server-2007-r2-deployment"></a><span data-ttu-id="3d55b-109">Para remover uma entrada de host autorizado em uma implantação do Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="3d55b-109">To remove an authorized host entry in an Office Communications Server 2007 R2 deployment</span></span>

1.  <span data-ttu-id="3d55b-110">Abra o console administrativo do Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3d55b-110">Open the Office Communications Server 2007 R2 administrative console.</span></span>

2.  <span data-ttu-id="3d55b-111">Expanda a árvore e clique com o botão direito do mouse no pool em que o host autorizado foi criado.</span><span class="sxs-lookup"><span data-stu-id="3d55b-111">Expand the tree and right-click the pool where the authorized host was created.</span></span>

3.  <span data-ttu-id="3d55b-112">Clique em **Propriedades** e, em seguida, clique em **Propriedades de front-end**.</span><span class="sxs-lookup"><span data-stu-id="3d55b-112">Click **Properties**, and then click **Front End Properties**.</span></span>

4.  <span data-ttu-id="3d55b-113">Clique na guia **autorização do host** .</span><span class="sxs-lookup"><span data-stu-id="3d55b-113">Click the **Host Authorization** tab.</span></span>

5.  <span data-ttu-id="3d55b-114">Selecione um servidor e, em seguida, clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="3d55b-114">Select a server, and then click **Remove**.</span></span>

6.  <span data-ttu-id="3d55b-115">Em **Propriedades**, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d55b-115">In **Properties**, click **OK**.</span></span>

<span data-ttu-id="3d55b-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3d55b-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

