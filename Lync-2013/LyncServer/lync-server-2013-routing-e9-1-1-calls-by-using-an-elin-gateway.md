---
title: 'Lync Server 2013: Roteamento de chamadas E9-1-1 usando um gateway ELIN'
description: 'Lync Server 2013: Routing E9-1-1 chamadas usando um gateway ELIN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Routing E9-1-1 calls by using an ELIN gateway
ms:assetid: 5a3997e3-898d-49cb-922a-4184c3373350
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204919(v=OCS.15)
ms:contentKeyID: 48184221
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9ddbdbbdf10f9eecbffecaaf8416718bbdcf224
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442290"
---
# <a name="routing-e9-1-1-calls-by-using-an-elin-gateway-in-lync-server-2013"></a><span data-ttu-id="2cfa8-103">Roteamento de chamadas E9-1-1 usando um gateway ELIN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2cfa8-103">Routing E9-1-1 calls by using an ELIN gateway in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2cfa8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2cfa8-104">

<span> </span></span></span>

<span data-ttu-id="2cfa8-105">_**Tópico da última modificação:** 2013-02-05_</span><span class="sxs-lookup"><span data-stu-id="2cfa8-105">_**Topic Last Modified:** 2013-02-05_</span></span>

<span data-ttu-id="2cfa8-106">Alguns parceiros do Programa de Interoperabilidade Aberta de Comunicações Unificadas fornecem gateways compatíveis com ELIN (número de identificação de local de emergência) qualificados, que podem servir como uma alternativa a uma conexão de tronco SIP com um provedor de serviços E9-1-1 qualificado.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-106">Some partners in the Unified Communications Open Interoperability Program provide qualified Emergency Location Identification Number (ELIN)-capable gateways, which can serve as an alternative to a SIP trunk connection to a qualified E9-1-1 service provider.</span></span> <span data-ttu-id="2cfa8-107">Os gateways ELIN dão suporte à conectividade CAMA (Contabilidade de Mensagem Automática Centralizada) ou ISDN com serviços E9-1-1 baseados em PSTN (Rede Telefônica Pública Comutada).</span><span class="sxs-lookup"><span data-stu-id="2cfa8-107">ELIN gateways support ISDN or Centralized Automatic Message Accounting (CAMA) connectivity to public switched telephone network (PSTN)-based E9-1-1 services.</span></span> <span data-ttu-id="2cfa8-108">Para obter detalhes sobre os parceiros que fornecem gateways do ELIN e links para a documentação dele, consulte [https://go.microsoft.com/fwlink/p/?LinkId=248425](https://go.microsoft.com/fwlink/p/?linkid=248425) .</span><span class="sxs-lookup"><span data-stu-id="2cfa8-108">For details about partners who provide ELIN gateways and links to their documentation, see [https://go.microsoft.com/fwlink/p/?LinkId=248425](https://go.microsoft.com/fwlink/p/?linkid=248425).</span></span>

<span data-ttu-id="2cfa8-109">Assim como as conexões de tronco SIP com provedores de serviços E9-1-1, os gateways ELIN também fornecem um meio de encaminhar uma chamada de emergência para o PSAP (Ponto de Atendimento Público Seguro) mais apropriado do chamador, mas esses gateways usam um ELIN como identificador do local.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-109">Like SIP trunk connections to E9-1-1 service providers, ELIN gateways also provide the means of routing an emergency call to the caller's most appropriate Public Safety Answering Point (PSAP), but these gateways use an ELIN as the location identifier.</span></span> <span data-ttu-id="2cfa8-110">Você define ELINs para cada local de resposta de emergência (ERL) em sua organização (para obter detalhes, consulte [Gerenciando locais para gateways Elin no Lync Server 2013](lync-server-2013-managing-locations-for-elin-gateways.md)).</span><span class="sxs-lookup"><span data-stu-id="2cfa8-110">You define ELINs for each Emergency Response Location (ERL) in your organization (for details, see [Managing locations for ELIN gateways in Lync Server 2013](lync-server-2013-managing-locations-for-elin-gateways.md)).</span></span>

<span data-ttu-id="2cfa8-111">Ao usar um gateway ELIN para chamadas de emergência, use a mesma infraestrutura do Lync Server E9-1 que você usaria para uma conexão de tronco SIP.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-111">When you use an ELIN gateway for emergency calls, you use the same Lync Server E9-1-1 infrastructure that you would use for a SIP trunk connection.</span></span> <span data-ttu-id="2cfa8-112">Ou seja, o banco de dados do serviço de informações de localização fornece o local para o cliente do Lync Server, e a política de localização habilita o recurso e define o roteamento.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-112">That is, the Location Information service database provides the location to the Lync Server client, and the location policy enables the feature and defines the routing.</span></span> <span data-ttu-id="2cfa8-113">No entanto, com um gateway ELIN, você precisa adicionar o ELINs ao banco de dados do serviço de informações de localização e ter sua operadora PSTN carregá-los para o banco de dados de identificação automática de local (ALI).</span><span class="sxs-lookup"><span data-stu-id="2cfa8-113">With an ELIN gateway, however, you need to add the ELINs to the Location Information service database and have your PSTN carrier upload them to the Automatic Location Identification (ALI) database.</span></span>

<span data-ttu-id="2cfa8-114">Quando um cliente do Lync obtém seu local do serviço de informações de localização, o local inclui o ELIN.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-114">When a Lync client obtains its location from the Location Information service, the location includes the ELIN.</span></span> <span data-ttu-id="2cfa8-115">Durante uma chamada de emergência, o ELIN é incluído no local enviado para o gateway ELIN.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-115">During an emergency call, the ELIN is included with the location sent to the ELIN gateway.</span></span> <span data-ttu-id="2cfa8-116">O gateway ELIN identifica a chamada como uma chamada de emergência e troca o número do chamador pelo ELIN.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-116">The ELIN gateway identifies the call as an emergency call and swaps the calling party's number with the ELIN.</span></span> <span data-ttu-id="2cfa8-117">Em seguida, o gateway de ELIN encaminha a chamada para a PSTN com o ELIN como número chamador.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-117">The ELIN gateway then routes the call to the PSTN with the ELIN as the calling number.</span></span> <span data-ttu-id="2cfa8-118">O provedor de E9-1-1 da PSTN pesquisa o ELIN no banco de dados ALI, que é um banco de dados complementar ao banco de dados MSAG (Catálogo de Endereços Principal).</span><span class="sxs-lookup"><span data-stu-id="2cfa8-118">The PSTN E9-1-1 provider looks up the ELIN in the ALI database, which is a companion database to the Master Street Address Guide (MSAG) database.</span></span> <span data-ttu-id="2cfa8-119">A PSTN então envia a chamada para o PSAP mais apropriado com base na pesquisa do ALI, e o PSAP envia as equipes de emergência para o local do chamador com base na pesquisa do ALI.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-119">The PSTN then sends the call to the most appropriate PSAP based on the ALI lookup, and the PSAP sends first responders to the caller's location based on the ALI lookup.</span></span> <span data-ttu-id="2cfa8-120">O número chamador é armazenado em cache no gateway ELIN por um tempo predefinido para retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-120">The calling number is cached on the ELIN gateway for a predefined amount of time for callbacks.</span></span> <span data-ttu-id="2cfa8-121">Durante um retorno de chamada, o PSAP chega ao gateway ELIN, que troca o ELIN pelo número DID (discagem direta interna) do chamador.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-121">During a callback, the PSAP reaches the ELIN gateway, which swaps the ELIN for the caller's direct inward dialing (DID) number.</span></span>

<span data-ttu-id="2cfa8-122">Os gateways ELIN oferecem suporte a chamadas de emergência somente de dentro da rede da sua organização.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-122">ELIN gateways support emergency calls only from within your organization's network.</span></span> <span data-ttu-id="2cfa8-123">Eles não oferecem suporte a chamadas de emergência realizadas fora da sua rede.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-123">They do not support emergency calls made from outside your network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2cfa8-124">Para obter detalhes sobre como usar uma conexão de tronco SIP para chamadas de emergência, consulte <A href="lync-server-2013-routing-e9-1-1-calls-by-using-a-sip-trunk.md">Roteamento E9-1-1 usando um tronco SIP no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-124">For details about using a SIP trunk connection for emergency calls, see <A href="lync-server-2013-routing-e9-1-1-calls-by-using-a-sip-trunk.md">Routing E9-1-1 calls by using a SIP trunk in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="2cfa8-125">O diagrama a seguir mostra como uma chamada de emergência é roteada do Lync Server para o PSAP quando você usa um gateway ELIN.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-125">The following diagram shows how an emergency call is routed from Lync Server to the PSAP when you use an ELIN gateway.</span></span>

<span data-ttu-id="2cfa8-126">**Encaminhar chamadas de E9-1-1 com um gateway ELIN**</span><span class="sxs-lookup"><span data-stu-id="2cfa8-126">**Routing E9-1-1 calls with an ELIN gateway**</span></span>

<span data-ttu-id="2cfa8-127">![ea68f88a-0fc4-43d4-9660-79a7e8936df1](images/JJ204919.ea68f88a-0fc4-43d4-9660-79a7e8936df1(OCS.15).jpg "ea68f88a-0fc4-43d4-9660-79a7e8936df1")</span><span class="sxs-lookup"><span data-stu-id="2cfa8-127">![ea68f88a-0fc4-43d4-9660-79a7e8936df1](images/JJ204919.ea68f88a-0fc4-43d4-9660-79a7e8936df1(OCS.15).jpg "ea68f88a-0fc4-43d4-9660-79a7e8936df1")</span></span>

1.  <span data-ttu-id="2cfa8-128">Um convite SIP que contém o local, o número de retorno de chamada do chamador e a URL de notificação (opcional) e o número de retorno de chamada de conferência é roteado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-128">A SIP INVITE containing the location, the caller's callback number, and the (optional) Notification URL and conference callback number is routed to Lync Server.</span></span>

2.  <span data-ttu-id="2cfa8-129">O Lync Server corresponde ao número de emergência e roteia a chamada (com base no valor de **uso de PSTN** definido na política de localização aplicável) para um servidor de mediação e de lá para um gateway Elin.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-129">Lync Server matches the emergency number and then routes the call (based on the **PSTN Usage** value defined in the applicable location policy) to a Mediation Server, and from there to an ELIN gateway.</span></span>

3.  <span data-ttu-id="2cfa8-130">O gateway ELIN encaminha a chamada para o PSTN por meio de um tronco CAMA ou ISDN.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-130">The ELIN gateway routes the call over an ISDN or CAMA trunk to the PSTN.</span></span>

4.  <span data-ttu-id="2cfa8-p106">O PSTN identifica a chamada como uma chamada de emergência e a encaminha para um roteador E9-1-1 seletivo na rede. O roteador E9-1-1 seletivo pesquisa o número do chamador no banco de dados ALI para obter o local geográfico. O roteador E9-1-1 seletivo envia a chamada para o PSAP mais apropriado com base nas informações de local que foram recuperadas do banco de dados ALI. </span><span class="sxs-lookup"><span data-stu-id="2cfa8-p106">The PSTN identifies the call as an emergency call and routes it to an E9-1-1 selective router in the network. The E9-1-1 selective router looks up the caller's number in the ALI database to obtain the geographical location. The E9-1-1 selective router sends the call to the most appropriate PSAP based on the location information that was retrieved from the ALI database.</span></span>

5.  <span data-ttu-id="2cfa8-134">Se você configurou a política de localização para notificações, um ou mais gerentes de segurança da sua organização receberão uma mensagem de chat especial de notificação de emergência do Lync.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-134">If you configured the location policy for notifications, one or more of your organization’s security officers are sent a special Lync emergency notification instant message.</span></span> <span data-ttu-id="2cfa8-135">Essa mensagem sempre aparecerá na(s) tela(s) dos funcionários de segurança e contém o nome, o número de telefone, a hora e o local do chamador, permitindo que a equipe de segurança atenda rapidamente ao chamador de emergência usando uma mensagem instantânea ou voz.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-135">This message always pops up on the security officers’ screen(s) and contains the caller’s name, phone number, time, and location, enabling security personnel to quickly respond to the emergency caller by using an instant message or voice.</span></span>

6.  <span data-ttu-id="2cfa8-p108">Se a chamada for interrompida prematuramente, o PSAP usará o ELIN para contatar diretamente o chamador. O gateway ELIN trocará o ELIN pelo DID do chamador.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-p108">If the call is broken prematurely, the PSAP uses the ELIN to contact the caller directly. The ELIN gateway swaps the ELIN for the caller's DID.</span></span>

<span data-ttu-id="2cfa8-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2cfa8-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

