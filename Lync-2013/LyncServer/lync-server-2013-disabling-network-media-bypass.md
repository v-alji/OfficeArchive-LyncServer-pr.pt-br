---
title: 'Lync Server 2013: desativando o bypass de mídia de rede'
description: 'Lync Server 2013: desativando o bypass de mídia de rede.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling network media bypass
ms:assetid: 936d2678-d712-4589-b172-b5793013652f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688141(v=OCS.15)
ms:contentKeyID: 49733741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1472711417218aa87936a3ccabe1bb465dd07c20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429095"
---
# <a name="disabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="91449-103">Desativando o bypass de mídia de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91449-103">Disabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91449-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91449-104">

<span> </span></span></span>

<span data-ttu-id="91449-105">_**Tópico da última modificação:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="91449-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="91449-106">As configurações de bypass de mídia se aplicam globalmente em uma implantação do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="91449-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="91449-107">O bypass de mídia permite que as chamadas ignorem o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="91449-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="91449-108">Para obter detalhes sobre quando usar o bypass de mídia, consulte [planejando a bypass de mídia no Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) na seção planejamento. Você pode desativar o bypass de mídia no painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91449-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.You can disable media bypass from the Lync Server Control Panel.</span></span> <span data-ttu-id="91449-109">Para obter detalhes sobre como habilitar e configurar o bypass de mídias média, consulte [habilitando o bypass de mídia de rede no Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span><span class="sxs-lookup"><span data-stu-id="91449-109">For details on enabling and configuring medial bypass, see [Enabling network media bypass in Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span></span>

<div>

## <a name="to-disable-media-bypass"></a><span data-ttu-id="91449-110">Para desativar o bypass de mídia</span><span class="sxs-lookup"><span data-stu-id="91449-110">To disable media bypass</span></span>

1.  <span data-ttu-id="91449-111">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="91449-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="91449-112">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91449-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="91449-113">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="91449-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="91449-114">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **global**.</span><span class="sxs-lookup"><span data-stu-id="91449-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="91449-115">Na página **global** , clique em configuração **global** .</span><span class="sxs-lookup"><span data-stu-id="91449-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="91449-116">Sempre existe apenas uma configuração, e ela é sempre chamada de global.</span><span class="sxs-lookup"><span data-stu-id="91449-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="91449-117">No menu **Editar** , clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="91449-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="91449-118">Na página **Editar configuração global** , desmarque a caixa de seleção **habilitar bypass de mídia** .</span><span class="sxs-lookup"><span data-stu-id="91449-118">On the **Edit Global Setting** page, clear the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="91449-119">Clique em **confirmar** para salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="91449-119">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="91449-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="91449-120">See Also</span></span>


[<span data-ttu-id="91449-121">Habilitando o bypass de mídia de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91449-121">Enabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-network-media-bypass.md)  
  

<span data-ttu-id="91449-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91449-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

