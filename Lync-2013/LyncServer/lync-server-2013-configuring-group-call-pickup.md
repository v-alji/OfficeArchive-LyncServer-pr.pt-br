---
title: 'Lync Server 2013: Configurando o recebimento de chamadas em grupo'
description: 'Lync Server 2013: Configurando o recebimento de chamadas em grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Group Call Pickup
ms:assetid: b4b0a9a0-91c6-43a5-9e2b-a086caeb3f94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945645(v=OCS.15)
ms:contentKeyID: 51541505
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff6be1ea20a98cfaf2addf32c7767940b420c5c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433028"
---
# <a name="configuring-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="456ce-103">Configurando a coleta de chamadas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="456ce-103">Configuring Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="456ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="456ce-104">

<span> </span></span></span>

<span data-ttu-id="456ce-105">_**Tópico da última modificação:** 2013-02-01_</span><span class="sxs-lookup"><span data-stu-id="456ce-105">_**Topic Last Modified:** 2013-02-01_</span></span>

<span data-ttu-id="456ce-106">Atualização cumulativa do Lync Server 2013: fevereiro de 2013 introduz o recebimento de chamadas em grupo como um novo recurso Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="456ce-106">Cumulative update for Lync Server 2013: February 2013 introduces Group Call Pickup as a new Enterprise Voice feature.</span></span> <span data-ttu-id="456ce-107">A retirada de chamadas em grupo permite que os usuários selecionem chamadas que estejam tocando para outro usuário discando um número de grupo de recebimento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="456ce-107">Group Call Pickup lets users pick up calls that are ringing for another user by dialing a call pickup group number.</span></span>

<span data-ttu-id="456ce-108">Os componentes que o recurso de retirada de chamadas em grupo usam são instalados e habilitados automaticamente no servidor front-end ou no servidor Standard Edition quando você implanta Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="456ce-108">The components that Group Call Pickup uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="456ce-109">No entanto, você deve configurar o recebimento de chamadas em grupo antes de disponibilizá-lo para os usuários.</span><span class="sxs-lookup"><span data-stu-id="456ce-109">However, you must configure Group Call Pickup before it is available to users.</span></span>

<span data-ttu-id="456ce-110">Esta seção orienta você na configuração da retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="456ce-110">This section guides you through the configuration of Group Call Pickup.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="456ce-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="456ce-111">In This Section</span></span>

[<span data-ttu-id="456ce-112">Chamadas em grupo escolha pré-requisitos de configuração e direitos de usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="456ce-112">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-group-call-pickup-configuration-prerequisites-and-user-rights.md)

[<span data-ttu-id="456ce-113">Processo de implantação para retirada de chamadas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="456ce-113">Deployment process for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-group-call-pickup.md)

[<span data-ttu-id="456ce-114">Deploy the SEFAUtil tool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="456ce-114">Deploy the SEFAUtil tool in Lync Server 2013</span></span>](lync-server-2013-deploy-the-sefautil-tool.md)

[<span data-ttu-id="456ce-115">Configurar números de grupo de recebimento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="456ce-115">Configure call pickup group numbers in Lync Server 2013</span></span>](lync-server-2013-configure-call-pickup-group-numbers.md)

[<span data-ttu-id="456ce-116">Habilitar o recebimento de chamadas em grupo para usuários no Lync Server 2013 e atribuir um número de grupo</span><span class="sxs-lookup"><span data-stu-id="456ce-116">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>](lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md)

[<span data-ttu-id="456ce-117">Comunicar as atribuições de recebimento de chamadas em grupo aos usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="456ce-117">Communicate Group Call Pickup assignments to users in Lync Server 2013</span></span>](lync-server-2013-communicate-group-call-pickup-assignment-to-users.md)

[<span data-ttu-id="456ce-118">Adicionais Verificar a implantação da retirada de chamadas em grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="456ce-118">(Optional) Verify the Group Call Pickup deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-the-group-call-pickup-deployment.md)

<span data-ttu-id="456ce-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="456ce-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

