---
title: 'Lync Server 2013: configurar um aplicativo SNMP'
description: 'Lync Server 2013: configurar um aplicativo SNMP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure an SNMP application
ms:assetid: c4b4a736-3b2e-45b9-a965-19d22161ad57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412972(v=OCS.15)
ms:contentKeyID: 48185346
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7374b61ad85d7ddcb40ef1db535e17f86dea58f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434106"
---
# <a name="configure-an-snmp-application-in-lync-server-2013"></a><span data-ttu-id="2c2ed-103">Configurar um aplicativo SNMP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c2ed-103">Configure an SNMP application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c2ed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c2ed-104">

<span> </span></span></span>

<span data-ttu-id="2c2ed-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="2c2ed-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="2c2ed-106">O Lync Server 2013 inclui uma interface de serviço Web padrão que você pode usar para conectar o serviço de informações de localização a aplicativos de protocolo de gerenciamento de rede simples (SNMP) que correspondem a endereços MAC com informações de porta e switch.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-106">Lync Server 2013 includes a standard web service interface that you can use to connect the Location Information service to Simple Network Management Protocol (SNMP) applications that match MAC addresses with port and switch information.</span></span>

<span data-ttu-id="2c2ed-107">Se um aplicativo SNMP estiver instalado e o serviço de informações de localização não conseguir encontrar uma correspondência no banco de dados de localização, o serviço de informações de localização consultará automaticamente o aplicativo usando o endereço MAC fornecido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-107">If an SNMP application is installed and the Location Information service fails to find a match in the location database, the Location Information service automatically queries the application by using the MAC address provided by the client.</span></span> <span data-ttu-id="2c2ed-108">Em seguida, o serviço de informações de localização usa a porta e as informações de troca retornadas pelo aplicativo SNMP para consultar o banco de dados de localização novamente.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-108">The Location Information service then uses the port and switch information returned by the SNMP application to query the location database again.</span></span>

<span data-ttu-id="2c2ed-109">Para obter detalhes, consulte [set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration).</span><span class="sxs-lookup"><span data-stu-id="2c2ed-109">For details, see [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2c2ed-110">Os endereços MAC não estão disponíveis em computadores que executam o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-110">MAC addresses are not available on computers running Windows 8.</span></span>



</div>

<div>

## <a name="to-configure-the-snmp-application-url"></a><span data-ttu-id="2c2ed-111">Para configurar a URL do aplicativo SNMP</span><span class="sxs-lookup"><span data-stu-id="2c2ed-111">To configure the SNMP application URL</span></span>

1.  <span data-ttu-id="2c2ed-112">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="2c2ed-113">Execute o seguinte cmdlet para configurar a URL do aplicativo SNMP.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-113">Run the following cmdlet to configure the URL for the SNMP application.</span></span>
    
        Set-CsWebServiceConfiguration -MACResolverUrl "<SNMP application url>" 

<span data-ttu-id="2c2ed-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c2ed-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

