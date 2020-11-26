---
title: 'Lync Server 2013: Configurando os computadores do Lync Server que serão monitorados'
description: 'Lync Server 2013: Configurando os computadores do Lync Server que serão monitorados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computers that will be monitored
ms:assetid: 9f1b2b91-d5af-42ad-a27d-b0815f762ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205118(v=OCS.15)
ms:contentKeyID: 48184927
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 742bd8a67eb42472e598c45619514e9407cb29cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432552"
---
# <a name="configuring-the-lync-server-computers-that-will-be-monitored-in-lync-server-2013"></a><span data-ttu-id="15937-103">Configurando os computadores do Lync Server que serão monitorados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15937-103">Configuring the Lync Server computers that will be monitored in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15937-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15937-104">

<span> </span></span></span>

<span data-ttu-id="15937-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="15937-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="15937-106">Como o Lync Server 2013 não usa o processo de descoberta central usado no Microsoft Lync Server 2010, cada computador do Lync Server 2013 que você deseja monitorar deve ser capaz de reportar sua existência ao servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="15937-106">Because Lync Server 2013 does not use the central discovery process used in Microsoft Lync Server 2010, each Lync Server 2013 computer that you want to monitor must be able to self-report its existence to the management server.</span></span> <span data-ttu-id="15937-107">Para possibilitar isso, instale os arquivos de agente do Operations Manager em cada um dos computadores a serem monitorados.</span><span class="sxs-lookup"><span data-stu-id="15937-107">To make this possible, you must install the Operations Manager agent files on each of the computers to be monitored.</span></span> <span data-ttu-id="15937-108">Depois que os arquivos do agente tiverem sido instalados, você deve configurar o computador para atuar como um proxy do System Center.</span><span class="sxs-lookup"><span data-stu-id="15937-108">After the agent files have been installed, you must configure the computer to act as a System Center proxy.</span></span> <span data-ttu-id="15937-109">Observe que esses procedimentos devem ser executados após a instalação e a configuração do Lync Server nesses computadores.</span><span class="sxs-lookup"><span data-stu-id="15937-109">Note that these procedures should be carried out after you have installed and configured Lync Server on these computers.</span></span>

<span data-ttu-id="15937-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15937-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

