---
title: 'Lync Server 2013: projetando o tronco SIP para E9-1-1'
description: 'Lync Server 2013: projetando o tronco SIP para E9-1-1.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Designing the SIP trunk for E9-1-1
ms:assetid: 4f93b974-b460-45c7-a4a8-6f38e34840f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398323(v=OCS.15)
ms:contentKeyID: 48184096
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ced3c92cb14739367c4e54da933a536cb66deb08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429535"
---
# <a name="designing-the-sip-trunk-for-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="dcd63-103">Criando o tronco SIP para E9-1-1 no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dcd63-103">Designing the SIP trunk for E9-1-1 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dcd63-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dcd63-104">

<span> </span></span></span>

<span data-ttu-id="dcd63-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="dcd63-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="dcd63-106">O Lync Server usa troncos SIP para conectar uma chamada de emergência ao provedor de serviços E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="dcd63-106">Lync Server uses SIP trunks to connect an emergency call to the E9-1-1 service provider.</span></span> <span data-ttu-id="dcd63-107">Você pode configurar os troncos SIP do serviço de emergência para E9-1-1 em um local central, em vários locais centrais ou em cada filial.</span><span class="sxs-lookup"><span data-stu-id="dcd63-107">You can set up emergency service SIP trunks for E9-1-1 at one central site, at multiple central sites, or at each branch site.</span></span> <span data-ttu-id="dcd63-108">No entanto, se o link da WAN entre o local do chamador e o local que hospeda o tronco SIP do serviço de emergência não estiver disponível, uma chamada colocada por um usuário no site desconectado precisará de um registro de uso de telefone especial na política de voz do usuário que roteará a chamada ao ECRC por meio do gateway da PSTN (Rede Telefônica Pública Comutada) local.</span><span class="sxs-lookup"><span data-stu-id="dcd63-108">However, if the WAN link between the caller’s site and the site that hosts the emergency service SIP trunk is unavailable, then a call placed by a user at the disconnected site will need a special phone usage record in the user’s voice policy that will route the call to the ECRC through the local public switched telephone network (PSTN) gateway.</span></span> <span data-ttu-id="dcd63-109">O mesmo é verdadeiro se os limites de chamadas simultâneas do serviço de controle de admissão chamada estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="dcd63-109">The same is true if call admission control concurrent call limits are in effect.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dcd63-110">Há duas maneiras de implementar um tronco SIP em um ambiente do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="dcd63-110">There are two ways to implement a SIP trunk in a Lync Server environment:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="dcd63-111">Use servidores de mediação multihomed que usam as interfaces roteadas de forma externa para se comunicar com o provedor de tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="dcd63-111">Use multihomed Mediation Servers that use their outward-facing publicly-routed interfaces to communicate with the SIP trunk provider.</span></span></P>
> <LI>
> <P><span data-ttu-id="dcd63-112">Use um SBC (controlador de borda de sessão local) para fornecer um ponto de demarcabilidade seguro entre os servidores de mediação e os serviços do provedor de tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="dcd63-112">Use an on-premises Session Border Controller (SBC) to provide a secure demarcation point between the Mediation Servers and the SIP trunk provider’s services.</span></span></P></LI></UL><span data-ttu-id="dcd63-113">Se você escolher o último método, certifique-se de que a marca e o modelo do SBC escolhidos foram certificados e oferecem suporte à transmissão de dados de localização PIDF-LO (objeto Local de formato de dados de informação de presença) como parte de seu SIP INVITE.</span><span class="sxs-lookup"><span data-stu-id="dcd63-113">If you choose the latter method, be sure that the SBC make and model that you choose has been certified and supports passing Presence Information Data Format Location Object (PIDF-LO) location data as part of its SIP INVITE.</span></span> <span data-ttu-id="dcd63-114">Caso contrário, as chamadas chegarão ao provedor de serviços de emergência retirado das suas informações de localização.</span><span class="sxs-lookup"><span data-stu-id="dcd63-114">Otherwise, the calls will arrive at the emergency services service provider stripped of their location information.</span></span> <span data-ttu-id="dcd63-115">Para obter detalhes sobre o SBCs certificado, consulte "infraestrutura qualificada para o Microsoft Lync" em <A href="https://go.microsoft.com/fwlink/p/?linkid=248425">https://go.microsoft.com/fwlink/p/?LinkId=248425</A> .</span><span class="sxs-lookup"><span data-stu-id="dcd63-115">For details about certified SBCs, see "Infrastructure Qualified for Microsoft Lync" at <A href="https://go.microsoft.com/fwlink/p/?linkid=248425">https://go.microsoft.com/fwlink/p/?LinkId=248425</A>.</span></span><BR><span data-ttu-id="dcd63-116">Os provedores de serviços E9-1-1 fornecem acesso a um par de SBCs para redundância.</span><span class="sxs-lookup"><span data-stu-id="dcd63-116">E9-1-1 service providers supply you with access to a pair of SBCs for redundancy.</span></span> <span data-ttu-id="dcd63-117">Você precisa tomar várias decisões em relação à topologia do servidor de mediação e à configuração de encaminhamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="dcd63-117">You need to make several decisions regarding the Mediation Server topology and call routing configuration.</span></span> <span data-ttu-id="dcd63-118">Você tratará os SBCs como pares iguais e utilizará o roteamento em rodízio para chamadas entre eles ou designará um SBC como primário e outro secundário?</span><span class="sxs-lookup"><span data-stu-id="dcd63-118">Will you treat both SBCs as equal peers and use round-robin routing for calls between them, or will you designate one SBC as primary and the other as secondary?</span></span>



</div>

<span data-ttu-id="dcd63-119">Para obter detalhes sobre a implantação de um tronco SIP no Lync Server, consulte [como implementar o entroncamento SIP no Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="dcd63-119">For details about deploying a SIP trunk in Lync Server, see [How do I implement SIP trunking in Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span></span> <span data-ttu-id="dcd63-120">As seguintes perguntas ajudaram você a implantar troncos SIP para E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="dcd63-120">The following questions will help you decide how to deploy the SIP trunks for E9-1-1.</span></span>

  - <span data-ttu-id="dcd63-121">**Você deve implantar o tronco SIP em uma conexão de concessão dedicada ou uma conexão compartilhada com a Internet?**</span><span class="sxs-lookup"><span data-stu-id="dcd63-121">**Should you deploy the SIP trunk over a dedicated leased or a shared internet connection?**</span></span>  
    <span data-ttu-id="dcd63-p105">É importante que as chamadas de emergência sejam sempre conectadas. Uma linha dedicada fornece uma conexão que não será garantida por outro tráfego na rede e permite que você implemente a QoS (Qualidade de Serviço). Lembre-se de que, se você estiver se conectando a provedores de serviços de emergência por meio da Internet pública, será preciso garantir a confidencialidade das chamadas de emergência e a criptografia IPSec será necessária.</span><span class="sxs-lookup"><span data-stu-id="dcd63-p105">It is important that emergency calls always connect. A dedicated line provides a connection that will not be preempted by other traffic on the network, and gives you the ability to implement Quality of Service (QoS). Remember that if you are connecting to emergency services service providers over the public Internet and you need to guarantee the confidentiality of emergency calls, IPSec encryption is required.</span></span>

<!-- end list -->

  - <span data-ttu-id="dcd63-125">**A implantação do E9-1-1 foi desenvolvida para tolerância a desastres?**</span><span class="sxs-lookup"><span data-stu-id="dcd63-125">**Is your E9-1-1 deployment designed for disaster tolerance?**</span></span>  
    <span data-ttu-id="dcd63-126">Como esta é uma solução de emergência, a resiliência é importante.</span><span class="sxs-lookup"><span data-stu-id="dcd63-126">Because this is an emergency solution, resiliency is important.</span></span> <span data-ttu-id="dcd63-127">Implante seus servidores de mediadores primário e secundário e troncos SIP em locais tolerantes a desastres.</span><span class="sxs-lookup"><span data-stu-id="dcd63-127">Deploy your primary and secondary Mediation Servers and SIP trunks in disaster tolerant locations.</span></span> <span data-ttu-id="dcd63-128">É uma boa ideia implantar o servidor de mediação primário mais próximo dos usuários aos quais ele oferece suporte e direcionar as chamadas de failover por meio do servidor de mediação secundário (localizado em uma localização geográfica diferente).</span><span class="sxs-lookup"><span data-stu-id="dcd63-128">It is a good idea to deploy your primary Mediation Server closest to the users that it is supporting, and route failover calls through the secondary Mediation Server (located in a different geographic location).</span></span>

<!-- end list -->

  - <span data-ttu-id="dcd63-129">**Você deve implantar um tronco SIP separado para cada filial?**</span><span class="sxs-lookup"><span data-stu-id="dcd63-129">**Should you deploy a separate SIP trunk for each branch office?**</span></span>  
    <span data-ttu-id="dcd63-130">O Lync Server oferece várias estratégias para lidar com a resiliência de voz em filiais, incluindo: redes de dados resistentes, implantação de um tronco SIP em cada filial ou envio de chamadas para o gateway local durante paralisações.</span><span class="sxs-lookup"><span data-stu-id="dcd63-130">Lync Server provides several strategies for handling voice resiliency in branch offices, including: having resilient data networks, deploying a SIP trunk at each branch, or pushing calls out to the local gateway during outages.</span></span> <span data-ttu-id="dcd63-131">Para obter detalhes, consulte [entroncamento do site de filial SIP no Lync Server 2013](lync-server-2013-branch-site-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="dcd63-131">For details, see [Branch site SIP trunking in Lync Server 2013](lync-server-2013-branch-site-sip-trunking.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="dcd63-132">**O CAC (serviço de controle de admissão de chamada) está habilitado?**</span><span class="sxs-lookup"><span data-stu-id="dcd63-132">**Is call admission control (CAC) enabled?**</span></span>  
    <span data-ttu-id="dcd63-133">O Lync Server não manipula as chamadas de emergência de maneira diferente de uma chamada comum.</span><span class="sxs-lookup"><span data-stu-id="dcd63-133">Lync Server does not handle emergency calls any differently than an ordinary call.</span></span> <span data-ttu-id="dcd63-134">Por essa razão, o gerenciamento de largura de banda ou o CAC (serviço de controle de admissão de chamada) pode ter um impacto negativo em uma configuração de E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="dcd63-134">For this reason, bandwidth management, or call admission control (CAC), can have a negative impact on an E9-1-1 configuration.</span></span> <span data-ttu-id="dcd63-135">As chamadas de emergência serão bloqueadas ou roteadas para o gateway PSTN local se um CAC estiver habilitado e for excedido o limite configurado em um link no qual as chamadas de emergência estão sendo roteadas.</span><span class="sxs-lookup"><span data-stu-id="dcd63-135">Emergency calls will be blocked or routed to the local PSTN gateway if a CAC is enabled and the configured limit is exceeded on a link where emergency calls are being routed.</span></span> <span data-ttu-id="dcd63-136">Como acima, tais chamadas não terão dados de localização e devem ser direcionadas manualmente para o ECRC.</span><span class="sxs-lookup"><span data-stu-id="dcd63-136">As indicated earlier in this topic, such calls will not have location data and must be manually routed to the ECRC.</span></span>

<span data-ttu-id="dcd63-137"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dcd63-137"></div>

<span> </span>

</div>

</div>

</span></span></div>

