---
title: 'Lync Server 2013: opções de bypass de mídia global'
description: 'Lync Server 2013: opções de bypass de mídia global.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Global media bypass options
ms:assetid: 1bd35f90-8587-48a1-b0c2-095a4053fc77
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398255(v=OCS.15)
ms:contentKeyID: 48183551
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e69a776c13171d74666a202108fa4b5c72e224d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427905"
---
# <a name="global-media-bypass-options-in-lync-server-2013"></a><span data-ttu-id="39643-103">Opções de bypass de mídia global no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39643-103">Global media bypass options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39643-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39643-104">

<span> </span></span></span>

<span data-ttu-id="39643-105">_**Tópico da última modificação:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="39643-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39643-106">Este tópico pressupõe que você já configurou a bypass de mídia para qualquer tronco para um par (um gateway PSTN (rede telefônica pública comutada), um PBX IP ou um controlador de borda de sessão (SBC) em um provedor de serviços de telefonia pela Internet, para um site ou serviço específico para o qual você deseja que a mídia ignore o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="39643-106">This topic assumes that you have already configured media bypass for any trunks to a peer (a public switched telephone network (PSTN) gateway, an IP-PBX, or a Session Border Controller (SBC) at an Internet Telephony Service Provider) for a specific site or service for which you want media to bypass the Mediation Server.</span></span>



</div>

<span data-ttu-id="39643-p101">Além de habilitar o bypass de mídia para conexões individuais de tronco associadas a um par, você deve também habilitá-lo globalmente. As configurações globais de bypass de mídia podem tanto especificar que o bypass de mídia sempre recebe tentativas de chamadas para o PSTN ou que o bypass de mídia é implantado usando o mapeamento de subredes para sites de rede e regiões de rede - similar ao que é feito pelo controle de admissão de chamada, outro recurso de voz avançado. Quando o bypass de mídia e o controle de admissão de chamadas estão ativados a região de rede, o site de rede e as informações da subrede especificadas pelo controle de admissão de chamada são usados automaticamente ao determinar se usam ou não o bypass de mídia. Isso significa que você não pode especificar se o bypass de mídia sempre recebe tentativas de chamada para o PSTN quando o controle de admissão de chamada está ativado.</span><span class="sxs-lookup"><span data-stu-id="39643-p101">In addition to enabling media bypass for individual trunk connections associated with a peer, you must also enable media bypass globally. Global media bypass settings can either specify that media bypass is always attempted for calls to the PSTN, or that media bypass is employed by using the mapping of subnets to network sites and network regions—similar to what is done by call admission control, another advanced voice feature. When media bypass and call admission control are both enabled, then the network region, network site, and subnet information that is specified for call admission control is automatically used when determining whether to employ media bypass. This means that you cannot specify that media bypass is always attempted for calls to the PSTN when call admission control is enabled.</span></span>

<span data-ttu-id="39643-111">Este tópico descreve como usar o painel de controle do Lync Server e o Shell de gerenciamento do Lync Server juntos para definir configurações de bypass de mídia global.</span><span class="sxs-lookup"><span data-stu-id="39643-111">This topic describes how to use Lync Server Control Panel and Lync Server Management Shell together to configure global media bypass settings.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39643-112">Ao usar estas etapas para configurar o bypass de mídia, pressupõe-se que você possui uma boa conectividade entre os clientes e o par do Servidor de Mediação (por exemplo, um gateway PSTN, um IP-PBX ou um SBC em um provedor de tronco SIP).</span><span class="sxs-lookup"><span data-stu-id="39643-112">When you use these steps to configure media bypass, the assumption is that you have good connectivity between clients and the Mediation Server peer (for example, a PSTN gateway, an IP-PBX, or an SBC at a SIP trunking provider).</span></span> <span data-ttu-id="39643-113">Se houver qualquer limitação de largura de banda no link, o bypass de mídia não poderá ser aplicado na chamada.</span><span class="sxs-lookup"><span data-stu-id="39643-113">If there are any bandwidth limitations on the link, media bypass cannot be applied to the call.</span></span> <span data-ttu-id="39643-114">O bypass de mídia não interopera com todos os gateways PSTN, IP-PBX e SBC.</span><span class="sxs-lookup"><span data-stu-id="39643-114">Media bypass will not interoperate with every PSTN gateway, IP-PBX, and SBC.</span></span> <span data-ttu-id="39643-115">A Microsoft testou um conjunto de gateways PSTN e SBCs com os parceiros certificados e realizou alguns testes com IP-PBXs da Cisco.</span><span class="sxs-lookup"><span data-stu-id="39643-115">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="39643-116">O bypass de mídia só tem suporte com produtos e versões listados no programa de interoperabilidade aberta da comunicação unificada – Lync Server em <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A> .</span><span class="sxs-lookup"><span data-stu-id="39643-116">Media bypass is supported only with products and versions listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A>.</span></span>



</div>

<div>

## <a name="next-steps-choose-global-media-bypass-settings"></a><span data-ttu-id="39643-117">Próximas etapas: escolher configurações de bypass de mídia global</span><span class="sxs-lookup"><span data-stu-id="39643-117">Next Steps: Choose Global Media Bypass Settings</span></span>

<span data-ttu-id="39643-118">Depois de habilitar a opção ignorar mídia em qualquer conexão de tronco a um par de sites ou serviços específicos, use o seguinte conteúdo para:</span><span class="sxs-lookup"><span data-stu-id="39643-118">After you have enabled media bypass on any trunk connections to a peer for specific sites or services, use the following content to either:</span></span>

  - <span data-ttu-id="39643-119">Habilite o bypass de mídia sempre, conforme descrito em [Configurar o bypass de mídia no Lync Server 2013 para sempre ignorar o servidor de mediação](lync-server-2013-configure-media-bypass-to-always-bypass-the-mediation-server.md).</span><span class="sxs-lookup"><span data-stu-id="39643-119">Enable media bypass always, as described in [Configure media bypass in Lync Server 2013 to always bypass the Mediation Server](lync-server-2013-configure-media-bypass-to-always-bypass-the-mediation-server.md).</span></span>

  - <span data-ttu-id="39643-120">Ou configure o bypass de mídia para usar as informações do site e da região, conforme descrito em [configurar as configurações globais do bypass de mídia no Lync Server 2013 para usar as informações do site e da região](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md).</span><span class="sxs-lookup"><span data-stu-id="39643-120">Or, configure media bypass to use site and region information, as described in [Configure media bypass global settings in Lync Server 2013 to use site and region information](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="39643-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="39643-121">See Also</span></span>


[<span data-ttu-id="39643-122">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39643-122">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="39643-123">Associar uma subrede a um site de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39643-123">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)  


[<span data-ttu-id="39643-124">Configurar bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39643-124">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)  
[<span data-ttu-id="39643-125">Bypass de mídia e Servidor de Mediação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39643-125">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)  
  

<span data-ttu-id="39643-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39643-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

