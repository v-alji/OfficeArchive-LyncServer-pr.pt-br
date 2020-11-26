---
title: 'Lync Server 2013: configurar o banco de dados de localização'
description: 'Lync Server 2013: configurar o banco de dados de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the location database
ms:assetid: 8544be31-6958-47ef-b926-fdc80d56191c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398679(v=OCS.15)
ms:contentKeyID: 48184704
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 877c83976ca0db9abc3a9e57d4a1cf5adaa1291a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433609"
---
# <a name="configure-the-location-database-in-lync-server-2013"></a><span data-ttu-id="8c228-103">Configure the location database in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c228-103">Configure the location database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c228-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c228-104">

<span> </span></span></span>

<span data-ttu-id="8c228-105">_**Tópico da última modificação:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="8c228-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="8c228-106">Para que os clientes possam detectar automaticamente seu local na rede, primeiro configure o banco de dados de localização.</span><span class="sxs-lookup"><span data-stu-id="8c228-106">To enable clients to automatically detect their location within a network, you first need to configure the location database.</span></span> <span data-ttu-id="8c228-107">Se você não configurar um banco de dados de local e a **localização necessária** na política de localização estiver definida como **Sim** ou **isenção de responsabilidade**, o usuário será solicitado a inserir um local manualmente.</span><span class="sxs-lookup"><span data-stu-id="8c228-107">If you do not configure a location database, and **Location Required** in the location policy is set to **Yes** or **Disclaimer**, the user will be prompted to manually enter a location.</span></span>

<span data-ttu-id="8c228-108">Para configurar o banco de dados de localização, você executará as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="8c228-108">To configure the location database, you will perform the following tasks:</span></span>

1.  <span data-ttu-id="8c228-109">Preencha o banco de dados com um mapeamento de elementos de rede para os locais.</span><span class="sxs-lookup"><span data-stu-id="8c228-109">Populate the database with a mapping of network elements to locations.</span></span> <span data-ttu-id="8c228-110">Se você usar um gateway de número de identificação de localização de emergência (ELIN), precisará incluir o ELIN no \<CompanyName\> campo.</span><span class="sxs-lookup"><span data-stu-id="8c228-110">If you use an Emergency Location Identification Number (ELIN) gateway, you need to include the ELIN in the \<CompanyName\> field.</span></span>

2.  <span data-ttu-id="8c228-111">Valide os endereços em relação ao MSAG (catálogo de endereços principal) mantido pelo provedor de serviços de emergência.</span><span class="sxs-lookup"><span data-stu-id="8c228-111">Validate the addresses against the master street address guide (MSAG) that is maintained by the E9-1-1 service provider.</span></span>

3.  <span data-ttu-id="8c228-112">Publique o banco de dados atualizado.</span><span class="sxs-lookup"><span data-stu-id="8c228-112">Publish the updated database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8c228-113">Como alternativa, você pode definir um banco de dados de origem de local secundário que pode ser usado no banco de dados de localização.</span><span class="sxs-lookup"><span data-stu-id="8c228-113">Alternately, you can define a secondary location source database that can be used in placed of the location database.</span></span> <span data-ttu-id="8c228-114">Para obter detalhes, consulte <A href="lync-server-2013-configure-a-secondary-location-information-service.md">configurar um serviço de informações de localização secundário no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8c228-114">For details, see <A href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8c228-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8c228-115">In This Section</span></span>

  - [<span data-ttu-id="8c228-116">Preencher o banco de dados de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c228-116">Populate the location database in Lync Server 2013</span></span>](lync-server-2013-populate-the-location-database.md)

  - [<span data-ttu-id="8c228-117">Validar endereços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c228-117">Validate addresses in Lync Server 2013</span></span>](lync-server-2013-validate-addresses.md)

  - [<span data-ttu-id="8c228-118">Publicar o banco de dados de localização do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c228-118">Publish the location database from Lync Server 2013</span></span>](lync-server-2013-publish-the-location-database.md)

<span data-ttu-id="8c228-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c228-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

