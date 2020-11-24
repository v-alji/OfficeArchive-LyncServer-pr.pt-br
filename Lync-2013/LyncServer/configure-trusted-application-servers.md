---
title: Configurar servidores de aplicativo confiáveis
description: Configurar servidores de aplicativos confiáveis.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure trusted application servers
ms:assetid: 20c3815f-3048-4940-8c0f-cdfcd0801d5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204735(v=OCS.15)
ms:contentKeyID: 48183592
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39f439ea3e5996e0a3464540069024b70c415e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390009"
---
# <a name="configure-trusted-application-servers"></a><span data-ttu-id="25d2d-103">Configurar servidores de aplicativo confiáveis</span><span class="sxs-lookup"><span data-stu-id="25d2d-103">Configure trusted application servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25d2d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25d2d-104">

<span> </span></span></span>

<span data-ttu-id="25d2d-105">_**Tópico da última modificação:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="25d2d-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="25d2d-106">Em um ambiente misto, se você criar um novo servidor de aplicativos confiável, deverá definir o próximo pool de saltos como um pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25d2d-106">In a mixed environment, if you create a new trusted application server, you must set the next hop pool to be a Lync Server 2013 pool.</span></span> <span data-ttu-id="25d2d-107">Em um ambiente misto, o pool herdado do Lync Server 2010 e o pool do Lync Server 2013 aparecem na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="25d2d-107">In a mixed environment, both the legacy Lync Server 2010 pool and the Lync Server 2013 pool appear in the drop down list.</span></span> <span data-ttu-id="25d2d-108">Não há suporte para a seleção do pool herdado.</span><span class="sxs-lookup"><span data-stu-id="25d2d-108">Selecting the legacy pool is not supported.</span></span>

<span data-ttu-id="25d2d-109">**Selecione o Lync Server 2013 como próximo nó ao criar um servidor de aplicativos confiável**</span><span class="sxs-lookup"><span data-stu-id="25d2d-109">**Select Lync Server 2013 as next hop when creating a Trusted application server**</span></span>

1.  <span data-ttu-id="25d2d-110">Abrir o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="25d2d-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="25d2d-111">No painel esquerdo, clique com o botão direito do mouse em **servidores de aplicativos confiáveis** e clique em **novo pool de aplicativos confiáveis**.</span><span class="sxs-lookup"><span data-stu-id="25d2d-111">In the left pane, right click **Trusted application servers** and click **New Trusted Application Pool**.</span></span>

3.  <span data-ttu-id="25d2d-112">Digite o **FQDN do pool** do pool de aplicativos confiável e selecione se ele será um único servidor ou vários servidores.</span><span class="sxs-lookup"><span data-stu-id="25d2d-112">Enter the **Pool FQDN** of the trusted application pool and select whether it will be a single-server or multiple-server.</span></span>

4.  <span data-ttu-id="25d2d-113">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="25d2d-113">Click **Next**.</span></span>

5.  <span data-ttu-id="25d2d-114">Na página **selecionar o próximo salto** , na lista, selecione o pool de front-end do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25d2d-114">On the **Select the next hop** page, from the list, select the Lync Server 2013 Front End pool.</span></span>

6.  <span data-ttu-id="25d2d-115">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="25d2d-115">Click **Finish**.</span></span>

7.  <span data-ttu-id="25d2d-116">Selecione o servidor de **Lync** do nó superior e, no menu **ação** , selecione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="25d2d-116">Select the top node **Lync Server** and from the **Action** menu, select **Publish**.</span></span>
    
    <span data-ttu-id="25d2d-117">Verifique se o **pool de aplicativos confiável** foi criado com êxito e associado ao pool de front-end correto.</span><span class="sxs-lookup"><span data-stu-id="25d2d-117">Verify the **Trusted Application Pool** has been created successfully and is associated with the correct Front End pool.</span></span>

<span data-ttu-id="25d2d-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25d2d-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

