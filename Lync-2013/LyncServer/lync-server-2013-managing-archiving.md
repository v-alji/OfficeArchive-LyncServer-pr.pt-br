---
title: 'Lync Server 2013: Gerenciando Arquivamento'
description: 'Lync Server 2013: Gerenciando o arquivamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013 Archiving
ms:assetid: 48c6cc8c-c2c1-4534-9a8a-fd5eb738076a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520990(v=OCS.15)
ms:contentKeyID: 48184003
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c7010645f36a7144ea508447d2c628bc8feacb0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425973"
---
# <a name="managing-lync-server-2013-archiving"></a><span data-ttu-id="7977f-103">Gerenciando Arquivamento do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7977f-103">Managing Lync Server 2013 Archiving</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7977f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7977f-104">

<span> </span></span></span>

<span data-ttu-id="7977f-105">_**Tópico da última modificação:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="7977f-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="7977f-106">Ao implantar o arquivamento para a sua organização, você especifica a configuração inicial durante a implantação.</span><span class="sxs-lookup"><span data-stu-id="7977f-106">When you deploy Archiving for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="7977f-107">No entanto, pode haver ocasiões em que você queira alterar a forma de implementar o suporte ao arquivamento para o gerenciamento cotidiano ou atender aos novos requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="7977f-107">However, there may be times when you want to change how you implement archiving support for day-to-day management or to meet new requirements in your organization.</span></span> <span data-ttu-id="7977f-108">Por exemplo, talvez seja necessário configurar o suporte para arquivamento de forma diferente para um site, um pool ou usuários específicos dentro da sua organização.</span><span class="sxs-lookup"><span data-stu-id="7977f-108">For example, you may need to set up archiving support differently for a specific site, pool, or users within your organization.</span></span> <span data-ttu-id="7977f-109">Para os usuários hospedados no Lync Server 2013, você faz isso é criar e personalizar políticas e configurações de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="7977f-109">For users homed on Lync Server 2013, you do this be creating and customizing archiving policies and configurations.</span></span> <span data-ttu-id="7977f-110">Se você usa a integração do Microsoft Exchange, você também deve configurar as configurações do Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="7977f-110">If you use Microsoft Exchange integration, you must also configure Exchange 2013 settings.</span></span> <span data-ttu-id="7977f-111">Esta seção fornece informações e procedimentos para permitir que você faça alterações em sua implantação de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="7977f-111">This section provides information and procedures to enable you to make changes to your Archiving deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7977f-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7977f-112">In This Section</span></span>

  - [<span data-ttu-id="7977f-113">Como o arquivamento funciona no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7977f-113">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)

  - [<span data-ttu-id="7977f-114">Gerenciar o arquivamento de comunicações internas e externas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7977f-114">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)

  - [<span data-ttu-id="7977f-115">Gerenciando opções de configuração de arquivamento no Lync Server 2013 para sua organização, sites e pools</span><span class="sxs-lookup"><span data-stu-id="7977f-115">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)

  - [<span data-ttu-id="7977f-116">Alterar as opções de banco de dados de arquivamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7977f-116">Changing Archiving database options in Lync Server 2013</span></span>](lync-server-2013-changing-archiving-database-options.md)

  - [<span data-ttu-id="7977f-117">Exportando dados arquivados do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7977f-117">Exporting archived data from Lync Server 2013</span></span>](lync-server-2013-exporting-archived-data.md)

<span data-ttu-id="7977f-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7977f-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

