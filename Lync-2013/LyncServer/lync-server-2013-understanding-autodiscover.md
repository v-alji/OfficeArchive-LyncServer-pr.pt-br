---
title: 'Lync Server 2013: Noções básicas sobre descoberta automática'
description: 'Lync Server 2013: compreendendo a descoberta automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Autodiscover
ms:assetid: d70a15b7-750b-4e0f-9a7f-0254d6d486c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945654(v=OCS.15)
ms:contentKeyID: 51541522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 295aba4bffbe5d17070702203cfd933284cb12c0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390220"
---
# <a name="understanding-autodiscover-in-lync-server-2013"></a><span data-ttu-id="6b7f9-103">Compreendendo a descoberta automática no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b7f9-103">Understanding Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b7f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b7f9-104">

<span> </span></span></span>

<span data-ttu-id="6b7f9-105">_**Tópico da última modificação:** 2013-06-03_</span><span class="sxs-lookup"><span data-stu-id="6b7f9-105">_**Topic Last Modified:** 2013-06-03_</span></span>

<span data-ttu-id="6b7f9-106">O serviço de descoberta automática do Lync Server 2013 é um recurso que foi originalmente introduzido no Microsoft Lync Server 2010 como parte da atualização cumulativa do Lync Server 2010: novembro de 2011.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-106">The Lync Server 2013 Autodiscover Service is a feature that was originally introduced in Microsoft Lync Server 2010 as part of the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="6b7f9-107">Além de correções, esta atualização cumulativa fornece suporte para clientes do Lync Mobile e do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-107">In addition to fixes, this cumulative update delivered support for Lync Mobile and Lync 2013 clients.</span></span>

<span data-ttu-id="6b7f9-108">No Lync Server 2013, o serviço de descoberta automática é uma parte integral da operação de clientes móveis externos e externos, e a descoberta automática também é prorrogada para novos clientes, como o aplicativo Lync da Windows Store recentemente introduzido para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-108">In Lync Server 2013, the Autodiscover Service is an integral part of the operation of external and internal mobile clients, and Autodiscover is also extended to new clients, such as the recently introduced Lync Windows Store app for Windows 8.</span></span> <span data-ttu-id="6b7f9-109">A descoberta automática também é usada pelos clientes de desktop do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-109">Autodiscover is also used by the Lync 2013 desktop clients.</span></span> <span data-ttu-id="6b7f9-110">A descoberta automática é reconhecida no Lync Server pelos registros DNS (sistema de nome de domínio) obrigatórios **lyncdiscover. \<domain\>**</span><span class="sxs-lookup"><span data-stu-id="6b7f9-110">Autodiscover is recognized in Lync Server by the required domain name system (DNS) records **lyncdiscover.\<domain\>**</span></span> <span data-ttu-id="6b7f9-111">e **lyncdiscoverinternal. \<domain\>**.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-111">and **lyncdiscoverinternal.\<domain\>**.</span></span> <span data-ttu-id="6b7f9-112">Além disso, as versões mais recentes do cliente de área de trabalho Lync 2010 e Lync 2013 preferem a descoberta automática nos registros SRV do sistema de nomes de domínio (DNS), usando os registros SRV DNS somente se lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="6b7f9-112">Additionally, newer versions of the Lync 2010 and Lync 2013 desktop client prefer Autodiscover over the domain name system (DNS) SRV records, using DNS SRV records only if lyncdiscover.\<domain\></span></span> <span data-ttu-id="6b7f9-113">ou lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="6b7f9-113">or lyncdiscoverinternal.\<domain\></span></span> <span data-ttu-id="6b7f9-114">Não responde ou não é resolvido.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-114">does not respond or does not resolve.</span></span> <span data-ttu-id="6b7f9-115">O aplicativo Lync da Windows Store para Windows 8 e Lync Mobile usa o autodiscover exclusivamente e não se refere aos Registros SRV DNS tradicionais.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-115">The Lync Windows Store app for Windows 8 and Lync Mobile uses Autodiscover exclusively and will not refer to the traditional DNS SRV records.</span></span>

<span data-ttu-id="6b7f9-116">No Lync Server 2013, a descoberta automática é expandida para se comunicar com o cliente quais elementos, recursos e métodos de comunicação estão disponíveis para o cliente.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-116">In Lync Server 2013, Autodiscover is expanded to communicate to the client which elements, features, and communication methods are available to the client.</span></span> <span data-ttu-id="6b7f9-117">As informações são comunicadas por meio de uma solicitação que é enviada do cliente, e os serviços Web do Lync Server respondem com uma resposta claramente definida que nomeia o que está disponível para o cliente e como entrar em contato com esses recursos no formato do documento resposta de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-117">The information is communicated through a request that is sent from the client, and the Lync Server web services responds with a clearly defined response that names what is available to the client, and how to contact those features in the format of the Autodiscover Response document.</span></span>

<span data-ttu-id="6b7f9-118">A melhor maneira de entender o documento de resposta de descoberta automática, incluindo como os serviços Web comunicam os recursos aos clientes por meio deste documento, é Dissect e definir cada linha em uma resposta típica do documento de resposta de descoberta automática do Lync Web Service.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-118">The best way to understand the Autodiscover response document, including how the web services communicate features to clients through this document, is to dissect and define each line in a typical response from the Lync web service Autodiscover response document.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="6b7f9-119">Nos detalhes a seguir, o usuário já foi autenticado no servidor primário respondendo a uma solicitação de autenticação.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-119">In the details that follow, the user has already authenticated to the home server by responding to an authentication request.</span></span>



</div>

<div class="">


> [!NOTE]  
> <span data-ttu-id="6b7f9-120">O serviço Web de descoberta automática do Lync é definido nos <STRONG>protocolos do Microsoft Office</STRONG> na seção <STRONG>especificações abertas</STRONG> da biblioteca do <STRONG>Microsoft Developer Network</STRONG> (MSDN).</span><span class="sxs-lookup"><span data-stu-id="6b7f9-120">The Lync Autodiscover Web Service is defined in the <STRONG>Microsoft Office Protocols</STRONG> in the <STRONG>Open Specifications</STRONG> section of the <STRONG>Microsoft Developer Network</STRONG> (MSDN) library.</span></span> <span data-ttu-id="6b7f9-121">Para obter detalhes, consulte o documento de especificação completa, "protocolo de serviço Web de descoberta automática do Lync" em: <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A> .</span><span class="sxs-lookup"><span data-stu-id="6b7f9-121">For details, see the full specification document, "Lync Autodiscover Web Service Protocol," at: <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A>.</span></span> <span data-ttu-id="6b7f9-122">Para obter detalhes sobre autenticação, consulte "protocolo de serviço Web de autenticação OC" em <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A> .</span><span class="sxs-lookup"><span data-stu-id="6b7f9-122">For details about authentication, see "OC Authentication Web Service Protocol" at <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A>.</span></span>



</div>

<div>

## <a name="the-lync-server-web-service-autodiscover-response"></a><span data-ttu-id="6b7f9-123">A resposta de descoberta automática do serviço Web do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6b7f9-123">The Lync Server Web Service Autodiscover Response</span></span>

<span data-ttu-id="6b7f9-124">A resposta retornada quando a solicitação de descoberta automática é enviada é a mesma para um cliente interno ou externo.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-124">The response returned when the Autodiscover request is sent is the same for an internal or an external client.</span></span> <span data-ttu-id="6b7f9-125">Alguns parâmetros que reconhecem a localização podem mudar.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-125">Some parameters that are location–aware may change.</span></span> <span data-ttu-id="6b7f9-126">Se uma solicitação de cliente for recebida, mas o pool real for diferente daquele que foi contatado, o pool inicial do usuário será definido para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-126">If a client request is received, but the actual pool is other than the one that has been contacted, the user’s home pool will be set for that user.</span></span> <span data-ttu-id="6b7f9-127">Um colega cuja conta de usuário está em um pool diferente, mas conectar-se ao mesmo escritório, seria uma resposta um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-127">A colleague whose user account is on a different pool, but logging in from the same office, would get a slightly different response.</span></span> <span data-ttu-id="6b7f9-128">A resposta indica o servidor front-end correto ou o pool de front-end para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-128">The response indicates the correct Front End Server or Front End pool for that user.</span></span>

<span data-ttu-id="6b7f9-129">Um exemplo de um documento de resposta de descoberta automática:</span><span class="sxs-lookup"><span data-stu-id="6b7f9-129">An example of an Autodiscover Response document:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">
       <User>
          <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>
          <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>
          <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>
          <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>
          <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>
          <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>
          <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>
          <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>
          <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>
          <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>
          <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>
          <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>
          <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>
       </User>
    </AutodiscoverResponse>

<div>

## <a name="autodiscover-response-document-details"></a><span data-ttu-id="6b7f9-130">Detalhes do documento de resposta de descoberta automática</span><span class="sxs-lookup"><span data-stu-id="6b7f9-130">Autodiscover Response Document Details</span></span>

<span data-ttu-id="6b7f9-131">O documento resposta de descoberta automática pode estar em um dos dois formatos.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-131">The Autodiscover Response document can be in one of two formats.</span></span> <span data-ttu-id="6b7f9-132">O formato padrão é uma JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="6b7f9-132">The default format is a JavaScript Object Notation (JSON).</span></span> <span data-ttu-id="6b7f9-133">O outro formato é o documento Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="6b7f9-133">The other format is extensible markup language (XML) document.</span></span> <span data-ttu-id="6b7f9-134">O XML é usado para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-134">The XML is used for this example.</span></span> <span data-ttu-id="6b7f9-135">A solicitação e a resposta são previsíveis porque o documento tem um esquema definido que determina o formato.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-135">The request and response are predictable because the document has a defined schema that determines the format.</span></span> <span data-ttu-id="6b7f9-136">A linha no documento que descreve o esquema usado é a primeira linha na solicitação ou resposta:</span><span class="sxs-lookup"><span data-stu-id="6b7f9-136">The line in the document that describes the schema used is the first line in the request or response:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">

<span data-ttu-id="6b7f9-137">A definição de **AccessLocation = "externo"** indica que a solicitação foi feita de um usuário externo.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-137">The definition of **AccessLocation=”External”** indicates that the request was made from an external user.</span></span>

    <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>

&nbsp;

    <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>

<span data-ttu-id="6b7f9-138">SipServerInternalAccess e SipServerExternalAccess não são usados no momento.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-138">SipServerInternalAccess and SipServerExternalAccess are currently not used.</span></span> <span data-ttu-id="6b7f9-139">Essas entradas são reservadas para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-139">These entries are reserved for future use.</span></span>

    <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>

&nbsp;

    <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>

<span data-ttu-id="6b7f9-140">SipClientInternalAccess e SipClientExternalAccess descrevem o nome de domínio totalmente qualificado e a porta que um cliente interno ou externo usará para acessar o servidor SIP definido.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-140">SipClientInternalAccess and SipClientExternalAccess describe the fully qualified domain name and port that an internal or external client will use to access the defined SIP Server.</span></span> <span data-ttu-id="6b7f9-141">O cliente de área de trabalho do Lync e o aplicativo Lync da Windows Store usam essas entradas com base em sua localização (interna ou externa) para localizar o diretor ou servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-141">The Lync desktop client and the Lync Windows Store app use these entries, based on their location (internal or external) to find the Director or Front End Server.</span></span>

    <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>

&nbsp;

    <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>

<span data-ttu-id="6b7f9-142">As `Autodiscover` referências contêm os pontos de entrada de serviço para o serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-142">The `Autodiscover` references contain the service entry points for the Autodiscover service.</span></span> <span data-ttu-id="6b7f9-143">O atributo token contém o nome do serviço e o href é uma URL que define para o cliente onde o serviço pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-143">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="6b7f9-144">Os clientes em uma rede externa usam o `External/Autodiscover` .</span><span class="sxs-lookup"><span data-stu-id="6b7f9-144">Clients on an external network use the `External/Autodiscover`.</span></span> <span data-ttu-id="6b7f9-145">O serviço descoberta automática é instalado como parte do processo de implantação.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-145">The Autodiscover service is installed as part of the deployment process.</span></span> <span data-ttu-id="6b7f9-146">`Internal/Autodiscover` Não está sendo usado no momento e está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-146">`Internal/Autodiscover` is not currently used, and is reserved for future use.</span></span>

    <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>

&nbsp;

    <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>

<span data-ttu-id="6b7f9-147">As `AuthBroker` referências contêm os pontos de entrada de serviço para o serviço de agente de autenticação interno e externo, nesse caso, SIP. svc.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-147">The `AuthBroker` references contain the service entry points for the internal and the external authentication broker service, in this case, sip.svc.</span></span> <span data-ttu-id="6b7f9-148">O atributo token contém o nome do serviço e o href é uma URL que define para o cliente onde o serviço pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-148">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="6b7f9-149">Clientes na rede interna com uso `Internal/AuthBroker` .</span><span class="sxs-lookup"><span data-stu-id="6b7f9-149">Clients on the internal network with use `Internal/AuthBroker`.</span></span> <span data-ttu-id="6b7f9-150">Os clientes em uma rede externa usam o `External/AuthBroker` .</span><span class="sxs-lookup"><span data-stu-id="6b7f9-150">Clients on an external network use the `External/AuthBroker`.</span></span> <span data-ttu-id="6b7f9-151">O serviço AuthBroker é instalado como parte do processo de implantação de seus serviços Web internos de implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-151">The AuthBroker service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>

&nbsp;

    <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>

<span data-ttu-id="6b7f9-152">O `WebScheduler` token referencia as URLs para o cliente acessar o agendamento baseado na Web para conferências do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-152">The `WebScheduler` token references the URLs for client access to the web-based scheduling for Lync Server conferences.</span></span> <span data-ttu-id="6b7f9-153">Atualmente, apenas o `External/WebScheduler` é usado.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-153">Currently, only the `External/WebScheduler` is used.</span></span> <span data-ttu-id="6b7f9-154">O webscheduler é instalado como parte do processo de implantação de seus serviços Web internos de implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-154">The WebScheduler is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>

&nbsp;

    <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>

<span data-ttu-id="6b7f9-155">`Internal/Mcx` e `External/Mcx` são as localizações dos serviços de mobilidade, introduzidas na atualização cumulativa do Lync Server 2010:2011 de novembro.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-155">`Internal/Mcx` and `External/Mcx` are the locations of the Mobility services, introduced in Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="6b7f9-156">Essas referências continuarão sendo usadas pelo Lync 2010 Mobile em todos os dispositivos compatíveis.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-156">These references will continue to be used by Lync 2010 Mobile on all supported devices.</span></span> <span data-ttu-id="6b7f9-157">O serviço MCX é instalado como parte do processo de implantação de seus serviços Web internos de implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-157">The Mcx service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>

&nbsp;

    <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

&nbsp;

    <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

<span data-ttu-id="6b7f9-158">**Internal/Ucwa**, **external/Ucwa** e **Ucwa** fornecem um meio para os clientes acessarem a interface de programação de aplicativo Web de comunicação unificada (API Ucwa ou simplesmente Ucwa).</span><span class="sxs-lookup"><span data-stu-id="6b7f9-158">**Internal/Ucwa**, **External/Ucwa** and **Ucwa** provide a means for clients to access the Unified Communications Web Application Programming Interface (UCWA API, or simply UCWA).</span></span> <span data-ttu-id="6b7f9-159">`Internal/Ucwa` e `External/Ucwa` diretórios virtuais são pontos de acesso reservados para futuros aprimoramentos de recursos e não são usados.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-159">`Internal/Ucwa` and `External/Ucwa` virtual directories are access points reserved for future feature enhancement, and are not used.</span></span> <span data-ttu-id="6b7f9-160">O `Ucwa` diretório virtual é usado para o Microsoft Lync Mobile (introduzido com o Lync Server 2013) em todos os dispositivos com suporte.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-160">The `Ucwa` virtual directory is used for Microsoft Lync Mobile (introduced with Lync Server 2013) on all supported devices.</span></span> <span data-ttu-id="6b7f9-161">O serviço UCWA é instalado como parte do processo de implantação de seus serviços Web internos de implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-161">The UCWA service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

<span data-ttu-id="6b7f9-162">`Internal/XFrame`, **External/Xframe** e **Xframe** fornecem acesso para aplicativos de servidor baseados em UCWA.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-162">`Internal/XFrame`, **External/XFrame** and **XFrame** provide access for UCWA-based server applications.</span></span> <span data-ttu-id="6b7f9-163">O XFrame é instalado como parte do processo de implantação de seus serviços Web internos de implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-163">XFrame is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>

<span data-ttu-id="6b7f9-164">O `Self` token se refere a informações específicas do cliente (tipo de resposta do usuário) que está realizando a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-164">The `Self` token refers to information specific to the client (user response type) that is making the request.</span></span> <span data-ttu-id="6b7f9-165">O cliente que fez essa solicitação era externo e esta referência de descoberta automática é para a parte do usuário do serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="6b7f9-165">The client that made this request was external, and this Autodiscover reference is to the user portion of the Autodiscover service.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6b7f9-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b7f9-166">See Also</span></span>


[<span data-ttu-id="6b7f9-167">Requisitos do sistema para componentes de acesso de usuário externo para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b7f9-167">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)  
[<span data-ttu-id="6b7f9-168">Planejando a descoberta automática no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b7f9-168">Planning for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-planning-for-autodiscover.md)  
  

<span data-ttu-id="6b7f9-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b7f9-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

