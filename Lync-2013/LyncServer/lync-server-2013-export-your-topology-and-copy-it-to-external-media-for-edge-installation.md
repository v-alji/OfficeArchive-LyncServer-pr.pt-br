---
title: Exportar sua topologia e copiá-la na mídia externa para instalação de borda
description: Exporte a topologia e copie-a para mídia externa para instalação do Edge.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export your topology and copy it to external media for edge installation
ms:assetid: def9f416-c519-4a72-b242-7d3057d9c1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398983(v=OCS.15)
ms:contentKeyID: 48185615
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47fcee032b4c0e667455ae7f35afe8b99c2d12cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389683"
---
# <a name="export-your-lync-server-2013-topology-and-copy-it-to-external-media-for-edge-installation"></a><span data-ttu-id="1509b-103">Exportar sua topologia do Lync Server 2013 e copiá-la na mídia externa para instalação de borda</span><span class="sxs-lookup"><span data-stu-id="1509b-103">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1509b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1509b-104">

<span> </span></span></span>

<span data-ttu-id="1509b-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="1509b-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="1509b-106">Depois de publicar sua topologia, o assistente de implantação do Lync Server precisa acessar os dados do repositório de gerenciamento central para iniciar o processo de implantação no servidor.</span><span class="sxs-lookup"><span data-stu-id="1509b-106">After you publish your topology, the Lync Server Deployment Wizard needs access to the Central Management store data in order to start the deployment process on the server.</span></span> <span data-ttu-id="1509b-107">Na rede interna, os dados estão disponíveis diretamente nos servidores, mas os servidores de borda que não estão no domínio interno não podem acessar os dados.</span><span class="sxs-lookup"><span data-stu-id="1509b-107">In the internal network, the data is available directly from the servers, but Edge Servers that are not in the internal domain cannot access the data.</span></span> <span data-ttu-id="1509b-108">Para disponibilizar os dados de configuração de topologia para uma implantação de servidor de borda, você deve exportar os dados de topologia para um arquivo e copiá-los para mídia externa (por exemplo, uma unidade USB ou um compartilhamento de rede que esteja disponível no servidor de borda) antes de executar o assistente de implantação do Lync Server no servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="1509b-108">To make the topology configuration data available for an Edge Server deployment, you must export the topology data to a file and copy it to external media (for example, a USB drive or a network share that is available from the Edge Server) before you run the Lync Server Deployment Wizard on the Edge Server.</span></span> <span data-ttu-id="1509b-109">Use o procedimento a seguir para disponibilizar os dados de configuração de topologia no servidor de borda que você está implantando.</span><span class="sxs-lookup"><span data-stu-id="1509b-109">Use the following procedure to make your topology configuration data available on the Edge Server that you are deploying.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="1509b-110">Depois de instalar o Lync Server 2013 em um servidor de borda, você gerencia o servidor de borda usando as ferramentas administrativas da rede interna, que replica automaticamente a configuração para qualquer servidor de borda na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="1509b-110">After you install Lync Server 2013 on an Edge Server, you manage the Edge Server using the administrative tools in the internal network, which automatically replicate configuration to any Edge Servers in your deployment.</span></span> <span data-ttu-id="1509b-111">A única exceção é atribuir e instalar certificados e interromper e iniciar serviços, ambos devem ser feitos no servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="1509b-111">The only exception is assigning and installing certificates and stopping and starting services, both of which must be done on the Edge Server.</span></span>



</div>

<div>

## <a name="to-make-your-topology-data-available-on-an-edge-server-by-using-lync-server-management-shell"></a><span data-ttu-id="1509b-112">Para disponibilizar os dados de topologia em um servidor de borda usando o Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="1509b-112">To make your topology data available on an Edge Server by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="1509b-113">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="1509b-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1509b-114">No Shell de gerenciamento do Lync Server, execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1509b-114">In the Lync Server Management Shell, run the following cmdlet:</span></span>
    
        Export-CsConfiguration -FileName <ConfigurationFilePath.zip>

3.  <span data-ttu-id="1509b-115">Copie o arquivo exportado para mídia externa (por exemplo, uma unidade USB ou um compartilhamento de rede que esteja disponível no servidor de borda durante a implantação).</span><span class="sxs-lookup"><span data-stu-id="1509b-115">Copy the exported file to external media (for example, a USB drive or a network share that is available from the Edge Server during deployment).</span></span>

<span data-ttu-id="1509b-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1509b-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

