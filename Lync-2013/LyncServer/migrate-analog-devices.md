---
title: Migrar dispositivos analógicos
description: Migrar dispositivos analógicos.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63f7f92142fb6a3ced37cded1a223038ec1876d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443829"
---
# <a name="migrate-analog-devices"></a><span data-ttu-id="f2c11-103">Migrar dispositivos analógicos</span><span class="sxs-lookup"><span data-stu-id="f2c11-103">Migrate analog devices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2c11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2c11-104">

<span> </span></span></span>

<span data-ttu-id="f2c11-105">_**Tópico da última modificação:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="f2c11-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="f2c11-106">O Lync Server oferece suporte a dispositivos analógicos.</span><span class="sxs-lookup"><span data-stu-id="f2c11-106">Lync Server provides support for analog devices.</span></span> <span data-ttu-id="f2c11-107">Especificamente, os dispositivos analógicos suportados são telefones de áudio analógicos e máquinas de fax analógicas.</span><span class="sxs-lookup"><span data-stu-id="f2c11-107">Specifically, the supported analog devices are analog audio phones and analog fax machines.</span></span> <span data-ttu-id="f2c11-108">Você pode configurar os gateways qualificados para dar suporte ao uso de dispositivos analógicos em seu ambiente do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f2c11-108">You can configure the qualified gateways to support the use of analog devices in your Lync Server environment.</span></span> <span data-ttu-id="f2c11-109">Depois de migrar do Lync Server 2010 para o Lync Server 2013, você também deve migrar os objetos de contato associados aos dispositivos analógicos.</span><span class="sxs-lookup"><span data-stu-id="f2c11-109">After you migrate from Lync Server 2010 to Lync Server 2013, you must also migrate the contact objects associated with the analog devices.</span></span> <span data-ttu-id="f2c11-110">Use o Shell de gerenciamento do Lync Server para recuperar primeiro todos os objetos de contato associados aos dispositivos analógicos do Lync Server 2010 e mova esses objetos para o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2c11-110">Use Lync Server Management Shell to first retrieve all contact objects associated with the Lync Server 2010 analog devices, and then move those objects to the Lync Server 2013 pool.</span></span>

<div>

## <a name="to-migrate-analog-devices"></a><span data-ttu-id="f2c11-111">Para migrar dispositivos analógicos</span><span class="sxs-lookup"><span data-stu-id="f2c11-111">To migrate analog devices</span></span>

1.  <span data-ttu-id="f2c11-112">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="f2c11-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="f2c11-113">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="f2c11-113">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  <span data-ttu-id="f2c11-114">Verifique se todos os objetos de contato foram movidos para o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2c11-114">Verify that all contact objects have been moved to the Lync Server 2013 pool.</span></span> <span data-ttu-id="f2c11-115">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="f2c11-115">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  <span data-ttu-id="f2c11-116">Verifique se todos os objetos de contato agora estão associados ao pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2c11-116">Verify that all the contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="f2c11-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2c11-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

