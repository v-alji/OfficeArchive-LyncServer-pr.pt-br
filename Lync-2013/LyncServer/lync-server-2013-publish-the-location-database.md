---
title: 'Lync Server 2013: publicar o banco de dados de localização'
description: 'Lync Server 2013: publicar o banco de dados de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26892429c7bf5fd9cbfebd0d7ac62482767a541e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390074"
---
# <a name="publish-the-location-database-from-lync-server-2013"></a><span data-ttu-id="c82f7-103">Publicar o banco de dados de localização do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c82f7-103">Publish the location database from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c82f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c82f7-104">

<span> </span></span></span>

<span data-ttu-id="c82f7-105">_**Tópico da última modificação:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="c82f7-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="c82f7-106">Os novos locais adicionados ao banco de dados de local não serão disponibilizados para o cliente até que sejam publicados.</span><span class="sxs-lookup"><span data-stu-id="c82f7-106">The new locations that you added to the location database will not be made available to the client until they have been published.</span></span>

<span data-ttu-id="c82f7-107">Para obter detalhes, consulte a documentação do Shell de gerenciamento do Lync Server para o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c82f7-107">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="c82f7-108">**Publish-CsLisConfiguration**</span><span class="sxs-lookup"><span data-stu-id="c82f7-108">**Publish-CsLisConfiguration**</span></span>

<span data-ttu-id="c82f7-109">Se você usar gateways ELIN, também é necessário carregar os ELINs para o banco de dados ALI da transportadora PSTN.</span><span class="sxs-lookup"><span data-stu-id="c82f7-109">If you use Emergency Location Identification Number (ELIN) gateways, you also need to upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span> <span data-ttu-id="c82f7-110">Sua transportadora PSTN pode exigir que você use um formato específico para os registros ELIN.</span><span class="sxs-lookup"><span data-stu-id="c82f7-110">Your PSTN carrier may require you to use a specific format for the ELIN records.</span></span> <span data-ttu-id="c82f7-111">Entre em contato com sua transportadora PSTN para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c82f7-111">Contact your PSTN carrier for details.</span></span> <span data-ttu-id="c82f7-112">Você pode exportar os registros do banco de dados do serviço de informações de localização e formatá-los conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="c82f7-112">You can export the records from the Location Information service database and format them as required.</span></span>

<div>

## <a name="to-publish-the-location-database"></a><span data-ttu-id="c82f7-113">Para publicar o banco de dados local</span><span class="sxs-lookup"><span data-stu-id="c82f7-113">To publish the location database</span></span>

  - <span data-ttu-id="c82f7-114">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="c82f7-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

  - <span data-ttu-id="c82f7-115">Execute o seguinte cmdlet para publicar o banco de dados local.</span><span class="sxs-lookup"><span data-stu-id="c82f7-115">Run the following cmdlet to publish the location database.</span></span>
    
        Publish-CsLisConfiguration

<span data-ttu-id="c82f7-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c82f7-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

