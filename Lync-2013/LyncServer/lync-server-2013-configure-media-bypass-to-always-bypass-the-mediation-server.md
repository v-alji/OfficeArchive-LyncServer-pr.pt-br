---
title: 'Lync Server 2013: configurar o bypass de mídia para sempre ignorar o servidor de mediação'
description: 'Lync Server 2013: configurar o bypass de mídia para sempre ignorar o servidor de mediação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media bypass to always bypass the Mediation Server
ms:assetid: 370c4f54-e520-4d77-96a3-84c5e84a9996
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425846(v=OCS.15)
ms:contentKeyID: 48183819
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b4981c7b12700d2f0bbf0bf05c8a51623bb8ba9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433910"
---
# <a name="configure-media-bypass-in-lync-server-2013-to-always-bypass-the-mediation-server"></a><span data-ttu-id="2fe8a-103">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span><span class="sxs-lookup"><span data-stu-id="2fe8a-103">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2fe8a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2fe8a-104">

<span> </span></span></span>

<span data-ttu-id="2fe8a-105">_**Tópico da última modificação:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="2fe8a-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2fe8a-106">Este tópico pressupõe que você já configurou a bypass de mídia para qualquer conexão de tronco a um par (um gateway PSTN (rede telefônica pública comutada), um PBX IP ou um controlador de borda de sessão (SBC) em um provedor de serviços de telefonia pela Internet (ITSP)) para um site ou serviço específico para o qual você deseja que a mídia ignore o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-106">This topic assumes that you have already configured media bypass for any trunk connections to a peer (a public switched telephone network (PSTN) gateway, an IP-PBX, or a Session Border Controller (SBC) at an Internet Telephony Service Provider (ITSP)) for a specific site or service for which you want media to bypass the Mediation Server.</span></span><BR><span data-ttu-id="2fe8a-107">Você não pode configurar mídia para sempre ignorar o servidor de mediação enquanto também habilita o controle de admissão de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-107">You cannot configure media to always bypass the Mediation Server while also enabling call admission control.</span></span> <span data-ttu-id="2fe8a-108">Essas configurações são incompatíveis e, portanto, são configurações mutuamente excludentes na interface do usuário do painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-108">These settings are incompatible and are therefore mutually exclusive settings in the Lync Server Control Panel user interface.</span></span>



</div>

<span data-ttu-id="2fe8a-109">Além de habilitar a bypass de mídia para conexões de tronco individuais associadas a um par para o servidor de mediação, você também deve definir configurações globais para bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-109">In addition to enabling media bypass for individual trunk connections associated with a peer to the Mediation Server, you must also configure global settings for media bypass.</span></span> <span data-ttu-id="2fe8a-110">Se você usar as etapas deste tópico para definir configurações globais para bypass de mídia, pressupõe-se que você tenha uma boa conectividade entre pontos de extremidade do Lync e qualquer ponto para o qual você configurou a mídia ignorada na conexão do tronco.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-110">If you use the steps in this topic to configure global settings for media bypass, the assumption is that you have good connectivity between Lync endpoints and any peer for which you configured media bypass on the trunk connection.</span></span>

<span data-ttu-id="2fe8a-111">Se você não tiver uma boa conectividade entre os pontos de extremidade do Lync Server e todos os pares do servidor de mediação cujas respectivas conexões de tronco foram habilitadas para bypass de mídia, você deve configurar as definições de bypass de mídia global para usar as informações de site e região ao empregar o bypass de mídia.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-111">If you do not have good connectivity between Lync Server endpoints and all peers to the Mediation Server whose respective trunk connections have been enabled for media bypass, you must configure global media bypass settings to use site and region information when employing media bypass.</span></span> <span data-ttu-id="2fe8a-112">Isso permite que você tenha mais controle ao determinar quando a mídia ignora o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-112">This allows for more control in determining when media bypasses the Mediation Server.</span></span> <span data-ttu-id="2fe8a-113">Para fazer isso, use as etapas em [Configurar o bypass de mídia para configurações globais no Lync server 2013 para usar as informações de site e região](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md) e [associar uma sub-rede a um site de rede no Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-113">To do this, use the steps in [Configure media bypass global settings in Lync Server 2013 to use site and region information](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md) and [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md) instead.</span></span>

<div>

## <a name="to-enable-media-bypass-globally-to-always-bypass-the-mediation-server"></a><span data-ttu-id="2fe8a-114">Para habilitar o desvio de mídia globalmente para que sempre ignore o servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="2fe8a-114">To Enable Media Bypass Globally to Always Bypass the Mediation Server</span></span>

1.  <span data-ttu-id="2fe8a-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2fe8a-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2fe8a-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="2fe8a-117">Na barra de navegação esquerda, clique em **Configuração de rede**.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-117">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="2fe8a-118">Clique duas vezes na configuração **Global** na lista.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-118">Double-click the **Global** configuration in the list.</span></span>

4.  <span data-ttu-id="2fe8a-119">Na página **Editar Configuração Global**, marque a caixa de seleção **Ativar desvio de mídia**.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-119">On the **Edit Global Setting** page, select the **Enable media bypass** check box.</span></span>

5.  <span data-ttu-id="2fe8a-120">Clique em **Sempre desviar**.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-120">Click **Always bypass**.</span></span>

6.  <span data-ttu-id="2fe8a-121">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="2fe8a-121">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2fe8a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fe8a-122">See Also</span></span>


[<span data-ttu-id="2fe8a-123">Configurar bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fe8a-123">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)  
[<span data-ttu-id="2fe8a-124">Opções de bypass de mídia global no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fe8a-124">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
[<span data-ttu-id="2fe8a-125">Bypass de mídia e Servidor de Mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fe8a-125">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)  


[<span data-ttu-id="2fe8a-126">Planejamento de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2fe8a-126">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="2fe8a-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2fe8a-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

