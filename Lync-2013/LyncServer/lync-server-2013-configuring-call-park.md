---
title: 'Lync Server 2013: Configurando Estacionamento de Chamadas'
description: 'Lync Server 2013: Configurando o estacionamento de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Call Park
ms:assetid: e4c5da53-7f6c-4535-bc9b-9da2026caec8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399014(v=OCS.15)
ms:contentKeyID: 48185732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2708f26fae5706afc31aa195b9fdb82536247b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433245"
---
# <a name="configuring-call-park-in-lync-server-2013"></a><span data-ttu-id="784ff-103">Configurando Estacionamento de Chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-103">Configuring Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="784ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="784ff-104">

<span> </span></span></span>

<span data-ttu-id="784ff-105">_**Tópico da última modificação:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="784ff-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="784ff-106">O estacionamento de chamadas permite que um usuário de voz empresarial Coloque uma chamada em espera de um telefone e, em seguida, recupere a chamada mais tarde, discando um número interno (conhecido como um parque de chamadas *órbita*) de qualquer telefone.</span><span class="sxs-lookup"><span data-stu-id="784ff-106">Call Park enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later by dialing an internal number (known as a Call Park *orbit*) from any telephone.</span></span>

<span data-ttu-id="784ff-107">Os componentes que chamam o parque usa são instalados e habilitados automaticamente no servidor front-end ou no servidor Standard Edition ao implantar o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="784ff-107">The components that Call Park uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="784ff-108">No entanto, você deve configurar o parque da chamada antes de disponibilizá-lo para os usuários.</span><span class="sxs-lookup"><span data-stu-id="784ff-108">However, you must configure Call Park before it is available to users.</span></span>

<span data-ttu-id="784ff-109">Esta seção orienta você na configuração do parque de chamadas.</span><span class="sxs-lookup"><span data-stu-id="784ff-109">This section guides you through the configuration of Call Park.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="784ff-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="784ff-110">In This Section</span></span>

  - [<span data-ttu-id="784ff-111">Pré-requisitos de Estacionamento de Chamadas e direitos de usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-111">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-call-park-configuration-prerequisites-and-user-rights.md)

  - [<span data-ttu-id="784ff-112">Processo de implantação para estacionamento de chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-112">Deployment process for Call Park in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-call-park.md)

  - [<span data-ttu-id="784ff-113">Configurar a tabela de órbita de Estacionamento de Chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-113">Configure the Call Park orbit table in Lync Server 2013</span></span>](lync-server-2013-configure-the-call-park-orbit-table.md)

  - [<span data-ttu-id="784ff-114">Configurar as definições do estacionamento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-114">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="784ff-115">Personalizar a chamada de música do parque em espera no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-115">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="784ff-116">Habilitar o estacionamento de chamadas para usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-116">Enable Call Park for users in Lync Server 2013</span></span>](lync-server-2013-enable-call-park-for-users.md)

  - [<span data-ttu-id="784ff-117">Verificar as regras de normalização para o parque de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-117">Verify normalization rules for Call Park in Lync Server 2013</span></span>](lync-server-2013-verify-normalization-rules-for-call-park.md)

  - [<span data-ttu-id="784ff-118">Adicionais Verificar a implantação do estacionamento de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="784ff-118">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-call-park-deployment.md)

<span data-ttu-id="784ff-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="784ff-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

