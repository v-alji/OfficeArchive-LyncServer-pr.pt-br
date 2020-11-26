---
title: 'Lync Server 2013: (opcional) verificar a implantação do estacionamento de chamadas'
description: 'Lync Server 2013: (opcional) Verifique a implantação do estacionamento de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Call Park deployment
ms:assetid: fcfe0962-1a9c-4cbd-847c-fed40e3b1480
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413076(v=OCS.15)
ms:contentKeyID: 48185952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 772392a3a791ed57c3220d80e9bd510d8803debb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424860"
---
# <a name="optional-verify-call-park-deployment-in-lync-server-2013"></a><span data-ttu-id="5509d-103">Adicionais Verificar a implantação do estacionamento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5509d-103">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5509d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5509d-104">

<span> </span></span></span>

<span data-ttu-id="5509d-105">_**Tópico da última modificação:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="5509d-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="5509d-106">Depois de instalar e configurar o parque de chamadas, você precisa verificar a configuração para garantir que o estacionamento e a recuperação de chamadas funcionarão como esperado.</span><span class="sxs-lookup"><span data-stu-id="5509d-106">After you install and configure Call Park, you need to verify the configuration to make sure that parking and retrieving calls works as expected.</span></span> <span data-ttu-id="5509d-107">No mínimo, verifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5509d-107">At minimum, verify the following:</span></span>

  - <span data-ttu-id="5509d-108">Ligue para um usuário que tenha o estacionamento de chamadas habilitado e tenha o usuário que estaciona a chamada.</span><span class="sxs-lookup"><span data-stu-id="5509d-108">Call a user who has Call Park enabled and have the user park the call.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5509d-109">Se você ativou o estacionamento de chamadas na política de voz antes de realizar esse teste, o usuário que está estacionando a chamada precisa sair do Lync Server e, em seguida, entrar novamente para poder ver a opção parque de chamadas na lista de chamadas de transferência.</span><span class="sxs-lookup"><span data-stu-id="5509d-109">If you enabled Call Park in voice policy just before performing this test, the user who is parking the call needs to sign out of Lync Server, and then sign back in, to be able to see the Call Park option in the transfer call list.</span></span>

    
    </div>

  - <span data-ttu-id="5509d-110">Disque o número de órbita para recuperar a chamada.</span><span class="sxs-lookup"><span data-stu-id="5509d-110">Dial the orbit number to retrieve the call.</span></span>

  - <span data-ttu-id="5509d-p102">Estacione outra chamada, permita que o tempo da chamada estacionada esgote e não pegue o retorno de chamada. Verifique se a chamada que atingiu o tempo limite será corretamente roteada para o destino de fallback especificado para **OnTimeoutURI**.</span><span class="sxs-lookup"><span data-stu-id="5509d-p102">Park another call, let the parked call time out, and do not pick up the ringback. Verify that the timed-out call is correctly routed to the fallback destination that is specified for **OnTimeoutURI**.</span></span>

<span data-ttu-id="5509d-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5509d-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

