---
title: Redefinir controle de admissão de chamada
description: Redefina o controle de admissão de chamadas.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4539cda453de6249be3a9b9b61521ecf478cb70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443619"
---
# <a name="reset-call-admission-control"></a><span data-ttu-id="fb3eb-103">Redefinir controle de admissão de chamada</span><span class="sxs-lookup"><span data-stu-id="fb3eb-103">Reset call admission control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb3eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb3eb-104">

<span> </span></span></span>

<span data-ttu-id="fb3eb-105">_**Tópico da última modificação:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="fb3eb-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="fb3eb-106">Se um pool de front-end do Lync Server 2010 estiver hospedando o controle de admissão de chamadas (CAC), você deverá mover o hospedagem do CAC para um pool do Lync Server 2013 para poder remover o pool de front-ends do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-106">If a Lync Server 2010 Front End pool is hosting call admission control (CAC), you must move CAC hosting to a Lync Server 2013 pool before you can remove the Lync Server 2010 Front End pool.</span></span>

<div>

## <a name="to-reset-cac"></a><span data-ttu-id="fb3eb-107">Para redefinir o CAC</span><span class="sxs-lookup"><span data-stu-id="fb3eb-107">To reset CAC</span></span>

1.  <span data-ttu-id="fb3eb-108">Abrir o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-108">Open Topology Builder.</span></span>

2.  <span data-ttu-id="fb3eb-109">Clique com o botão direito do mouse no nó do site e, em seguida, clique em **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-109">Right-click the site node, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="fb3eb-110">Em **configuração de controle de admissão de chamada**, verifique se a opção **habilitar controle de admissão de chamadas** está selecionada.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-110">Under **Call Admission Control setting**, make sure **Enable Call Admission Control** is selected.</span></span>

4.  <span data-ttu-id="fb3eb-111">Em **pool de front-ends para executar o controle de admissão de chamadas (CAC)**, selecione o pool do Lync Server 2013 para hospedar o CAC e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-111">Under **Front End pool to run call admission control (CAC)**, select the Lync Server 2013 pool that is to host CAC, and then click **OK**.</span></span>

5.  <span data-ttu-id="fb3eb-112">Publique a topologia.</span><span class="sxs-lookup"><span data-stu-id="fb3eb-112">Publish the topology.</span></span>

<span data-ttu-id="fb3eb-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb3eb-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

