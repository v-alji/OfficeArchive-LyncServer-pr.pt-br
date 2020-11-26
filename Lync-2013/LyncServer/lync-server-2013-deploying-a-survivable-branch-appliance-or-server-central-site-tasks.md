---
title: Implantando um servidor ou aparelho de filial persistente - Tarefas do site central
description: Implantando um aparelho de ramificação ou tarefas de site central para o servidor.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server - central site tasks
ms:assetid: 0f631a36-fc2e-41cd-8a0d-f27e84f4a89e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398189(v=OCS.15)
ms:contentKeyID: 48183422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4460ea215d6fc80ee89f1ca9bc42f08ac5d14617
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430130"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013---central-site-tasks"></a><span data-ttu-id="0af23-103">Implantando um servidor ou aparelho de filial persistente com o Lync Server 2013 - Tarefas do site central</span><span class="sxs-lookup"><span data-stu-id="0af23-103">Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0af23-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0af23-104">

<span> </span></span></span>

<span data-ttu-id="0af23-105">_**Tópico da última modificação:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="0af23-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="0af23-106">Conclua as tarefas nesta seção no site central.</span><span class="sxs-lookup"><span data-stu-id="0af23-106">Complete the tasks in this section at the central site.</span></span> <span data-ttu-id="0af23-107">Se você estiver implantando um servidor de ramificação sobreviventes, pule a primeira tarefa.</span><span class="sxs-lookup"><span data-stu-id="0af23-107">If you’re deploying a Survivable Branch Server, skip the first task.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="0af23-108">Antes de executar as tarefas nesta seção, as seguintes condições devem estar em vigor:</span><span class="sxs-lookup"><span data-stu-id="0af23-108">Before you perform the tasks in this section, the following conditions must be in place:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="0af23-109">O Lync Server deve ser configurado no site central.</span><span class="sxs-lookup"><span data-stu-id="0af23-109">Lync Server must be set up at the central site.</span></span></P>
> <LI>
> <P><span data-ttu-id="0af23-110">Um técnico de instalação no site de filial deve ser adicionado ao grupo RTCUniversalSBATechnicians.</span><span class="sxs-lookup"><span data-stu-id="0af23-110">An installation technician at the branch site must be added to the RTCUniversalSBATechnicians group.</span></span></P></LI></UL><span data-ttu-id="0af23-111">Além disso, recomendamos que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0af23-111">In addition, we recommend that you do the following:</span></span>
> <UL>
> <LI>
> <P><span data-ttu-id="0af23-112">Implante um servidor DHCP em cada site de ramificação para permitir que os clientes obtenham endereços IP.</span><span class="sxs-lookup"><span data-stu-id="0af23-112">Deploy a DHCP server at each branch site to enable clients to obtain IP addresses.</span></span></P>
> <LI>
> <P><span data-ttu-id="0af23-113">Como uma alternativa para implantar um servidor DHCP em cada site de ramificação, habilite o DHCP do Lync Server no aparelho de ramificação ou servidor de ramificação sobreviventes usando o cmdlet Set-CsRegistrarConfiguration-do Shell de gerenciamento do Lync Server <STRONG>-EnableDHCPServer $true</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0af23-113">As an alternative to deploying a DHCP server at each branch site, enable Lync Server DHCP on the Survivable Branch Appliance or Survivable Branch Server by using the Lync Server Management Shell cmdlet <STRONG>Set-CsRegistrarConfiguration –EnableDHCPServer $true</STRONG>.</span></span> <span data-ttu-id="0af23-114">Para obter detalhes, consulte a seção "requisitos de hardware e software" dos <A href="lync-server-2013-branch-site-resiliency-requirements.md">requisitos de resiliência de site para o Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="0af23-114">For details, see the “Hardware and Software Requirements” section of <A href="lync-server-2013-branch-site-resiliency-requirements.md">Branch-site resiliency requirements for Lync Server 2013</A> in the Planning documentation.</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0af23-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0af23-115">In This Section</span></span>

  - [<span data-ttu-id="0af23-116">Adicionar um Aplicativo de Filial Persistente ao Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0af23-116">Add a Survivable Branch Appliance to Active Directory in Lync Server 2013</span></span>](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md)

  - [<span data-ttu-id="0af23-117">Adicionar sites de filial a sua topologia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0af23-117">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="0af23-118">Definir um Servidor ou Aparelho de Filial Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0af23-118">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="0af23-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0af23-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

