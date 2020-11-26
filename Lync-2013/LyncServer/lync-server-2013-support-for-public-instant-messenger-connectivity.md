---
title: Suporte do Lync Server 2013 para conectividade de mensagem instantânea pública
description: Suporte do Lync Server 2013 para conectividade de mensagem instantânea pública.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for public instant messenger connectivity
ms:assetid: 9c6eb500-647b-4ccd-a00e-2b8dd7c44a76
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn458579(v=OCS.15)
ms:contentKeyID: 59170234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d4a58d71eb23012da960cf4505f1a55fd08df32c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441498"
---
# <a name="support-for-public-instant-messenger-connectivity-in-lync-server-2013"></a><span data-ttu-id="7ad10-103">Suporte para conectividade de mensagem instantânea pública no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ad10-103">Support for public instant messenger connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ad10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ad10-104">

<span> </span></span></span>

<span data-ttu-id="7ad10-105">_**Tópico da última modificação:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="7ad10-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<div>

## <a name="support-for-public-instant-messenger-connectivity"></a><span data-ttu-id="7ad10-106">Suporte para conectividade de mensagem instantânea pública</span><span class="sxs-lookup"><span data-stu-id="7ad10-106">Support for Public Instant Messenger Connectivity</span></span>

<span data-ttu-id="7ad10-107">Este artigo fornece informações sobre o suporte para a PIC (conectividade pública de IM).</span><span class="sxs-lookup"><span data-stu-id="7ad10-107">This article provides information about support for Public IM Connectivity (PIC).</span></span> <span data-ttu-id="7ad10-108">A PIC é um recurso do Microsoft Lync que permite que as organizações habilitem seus usuários do Lync para se conectar com usuários de determinados serviços de mensagens instantâneas (IM) públicas por meio de seus clientes e identidades do Lync.</span><span class="sxs-lookup"><span data-stu-id="7ad10-108">PIC is a feature of Microsoft Lync that allows organizations to enable their Lync users to connect with users of certain public instant messaging (IM) services through their Lync clients and identities.</span></span>

<span data-ttu-id="7ad10-109">Os usuários finais se beneficiam da capacidade de se conectar com clientes, parceiros e fornecedores em termos de seus termos.</span><span class="sxs-lookup"><span data-stu-id="7ad10-109">End-users benefit from being able to connect with customers, partners, and vendors on their terms.</span></span> <span data-ttu-id="7ad10-110">Ele se beneficia do suporte a um único cliente de comunicação em tempo real, mantendo os recursos de controle, conformidade e arquivamento do Lync.</span><span class="sxs-lookup"><span data-stu-id="7ad10-110">IT benefits from supporting a single real-time communications client while maintaining the control, compliance, and archiving features of Lync.</span></span> <span data-ttu-id="7ad10-111">A conectividade Lync-Skype, [publicamente disponível em maio de 2013](https://blogs.technet.com/b/lync/archive/2013/05/23/lync-skype-connectivity-available-today.aspx), depende do herdado que o Lync/Office Communications Server (OCS)/Live Communications Server (LCs) primeiro estabeleceu com a PIC em conexão com o MSN/Windows Live, AOL e Yahoo.</span><span class="sxs-lookup"><span data-stu-id="7ad10-111">Lync-Skype connectivity, [publicly available in May 2013](https://blogs.technet.com/b/lync/archive/2013/05/23/lync-skype-connectivity-available-today.aspx), relies on the legacy that Lync/Office Communications Server (OCS)/Live Communications Server (LCS) first established with PIC in connecting to MSN/Windows Live, AOL, and Yahoo.</span></span>  <span data-ttu-id="7ad10-112">Para obter mais informações sobre a conectividade do Lync-Skype, consulte a [conectividade do Lync com o Skype](https://office.microsoft.com/lync/lync-skype-connectivity-fx103789635.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ad10-112">For more information on Lync-Skype connectivity, see the [Lync-Skype connectivity](https://office.microsoft.com/lync/lync-skype-connectivity-fx103789635.aspx).</span></span> <span data-ttu-id="7ad10-113">A Federação com o Windows Live, o AOL e o Yahoo são cada um deles em um caminho até o fim da vida útil.</span><span class="sxs-lookup"><span data-stu-id="7ad10-113">Federation with Windows Live, AOL, and Yahoo are each on a path towards end-of-life.</span></span> <span data-ttu-id="7ad10-114">Esta página documenta o status de cada serviço.</span><span class="sxs-lookup"><span data-stu-id="7ad10-114">This page documents the status of each service.</span></span>

<span data-ttu-id="7ad10-115">Para usar a PIC, os clientes precisam ativar o serviço para cada provedor de serviço de mensagens de chat públicas.</span><span class="sxs-lookup"><span data-stu-id="7ad10-115">To use PIC, customers have been required to activate the service for each public IM service provider.</span></span> <span data-ttu-id="7ad10-116">Os requisitos e os detalhes de como fazer isso dependem do provedor de serviços de mensagens instantâneas e do programa de licenciamento subjacente do cliente.</span><span class="sxs-lookup"><span data-stu-id="7ad10-116">The requirements and details for how to do this are dependent upon the IM service provider and the customer's underlying licensing program.</span></span>

<div>

## <a name="windows-live-messenger"></a><span data-ttu-id="7ad10-117">Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7ad10-117">Windows Live Messenger</span></span>

<span data-ttu-id="7ad10-118">A Microsoft colocou o Windows Live Messenger e o Skype juntos.</span><span class="sxs-lookup"><span data-stu-id="7ad10-118">Microsoft brought Windows Live Messenger and Skype together.</span></span> <span data-ttu-id="7ad10-119">Em abril de 2013, os usuários do Messenger migraram para o Skype quando entrarem.</span><span class="sxs-lookup"><span data-stu-id="7ad10-119">In April 2013, Messenger users were migrated to Skype upon sign-in.</span></span> <span data-ttu-id="7ad10-120">Os clientes do Lync que confiam na Federação com o Messenger continuarão a ser capazes de se comunicar com seus contatos do Messenger, mesmo depois que esses contatos forem atualizados para o Skype.</span><span class="sxs-lookup"><span data-stu-id="7ad10-120">Lync customers who rely on federation with Messenger will continue to be able to communicate with their Messenger contacts, even after those contacts update to Skype.</span></span> <span data-ttu-id="7ad10-121">Não há nada que os administradores do Lync ou os usuários finais do Lync precisem fazer para manter a continuidade do serviço, e o gerenciamento dessa funcionalidade no Lync permanece o mesmo que para comunicações com o Messenger.</span><span class="sxs-lookup"><span data-stu-id="7ad10-121">There is nothing that Lync administrators or Lync end-users need to do to maintain continuity of service, and management of this capability within Lync remains the same as it has been for communications with Messenger.</span></span> 

<span data-ttu-id="7ad10-122">Quando os usuários do Messenger se conectarem ao Skype usando suas contas da Microsoft (ou seja, as mesmas credenciais usadas para o Messenger) todos os seus contatos do Messenger-incluindo contatos federados do Lync-siga-os no Skype.</span><span class="sxs-lookup"><span data-stu-id="7ad10-122">When Messenger users sign into Skype using their Microsoft accounts (i.e., the same credentials used for Messenger) all of their Messenger contacts - including federated Lync contacts - follow them into Skype.</span></span> <span data-ttu-id="7ad10-123">O compartilhamento de presença e mensagens instantâneas entre o Skype e o Lync para estes contatos está disponível.</span><span class="sxs-lookup"><span data-stu-id="7ad10-123">Presence sharing and instant messaging between Skype and Lync for these contacts is available.</span></span> 

<span data-ttu-id="7ad10-124">Conectividade Lync-Skype-adição de contato, compartilhamento de presença, mensagens instantâneas e chamadas de áudio entre o Lync e usuários do Skype – agora está disponível para todos os clientes do Lync.</span><span class="sxs-lookup"><span data-stu-id="7ad10-124">Lync-Skype connectivity - contact adding, presence sharing, instant messaging, and audio calling between Lync and Skype users - is also now available to all Lync customers.</span></span>

</div>

<div>

## <a name="yahoo-and-aol-instant-messenger"></a><span data-ttu-id="7ad10-125">Instant\!</span><span class="sxs-lookup"><span data-stu-id="7ad10-125">Yahoo\!</span></span> <span data-ttu-id="7ad10-126">e mensagem instantânea do AOL</span><span class="sxs-lookup"><span data-stu-id="7ad10-126">and AOL Instant Messenger</span></span>

<span data-ttu-id="7ad10-127">Federação com o Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="7ad10-127">Federation with Yahoo\!</span></span> <span data-ttu-id="7ad10-128">e a AOL estão em um caminho para o fim da vida para os clientes do Lync (e do Office Communications Server).</span><span class="sxs-lookup"><span data-stu-id="7ad10-128">and AOL are both on a path toward end-of-life for customers of Lync (and Office Communications Server).</span></span> <span data-ttu-id="7ad10-129">A capacidade da Microsoft de fornecer a cada um desses serviços tem o suporte contingente no Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="7ad10-129">Microsoft’s ability to provide each of these services has been contingent upon support from Yahoo\!</span></span> <span data-ttu-id="7ad10-130">e a AOL, e os acordos subjacentes deles estão prestes a ser enrolados.</span><span class="sxs-lookup"><span data-stu-id="7ad10-130">and AOL, and the underlying agreements of these are winding down.</span></span> <span data-ttu-id="7ad10-131">Para o Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="7ad10-131">For both Yahoo\!</span></span> <span data-ttu-id="7ad10-132">e AOL, o serviço continuará até de junho de 2014.</span><span class="sxs-lookup"><span data-stu-id="7ad10-132">and AOL, service will continue through June 2014.</span></span>

  - <span data-ttu-id="7ad10-133">O **Yahoo** -Service continuará até junho de 2014, e os clientes continuarão precisando ser licenciados com a licença de assinatura de usuário da conectividade de im pública do Microsoft Lync ("pic USL").</span><span class="sxs-lookup"><span data-stu-id="7ad10-133">**Yahoo** - Service will continue through June 2014, and customers continue to need to be licensed with the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”).</span></span>  <span data-ttu-id="7ad10-134">A partir de 1º de setembro de 2012, a PIC USL, não está mais disponível para compra de contratos novos ou renovadores.</span><span class="sxs-lookup"><span data-stu-id="7ad10-134">As of September 1st, 2012, the PIC USL, is no longer available for purchase for new or renewing agreements.</span></span>  <span data-ttu-id="7ad10-135">Os clientes com licenças compradas antes desta data poderão continuar a federar-se com o Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="7ad10-135">Customers with licenses purchased prior to this date will be able to continue to federate with Yahoo\!</span></span> <span data-ttu-id="7ad10-136">até o anterior da data de encerramento do serviço ou o prazo de expiração da licença.</span><span class="sxs-lookup"><span data-stu-id="7ad10-136">until the earlier of the service shut down date or their license expiration.</span></span> <span data-ttu-id="7ad10-137">Leia [o comunicado](https://blogs.technet.com/b/lync/archive/2012/11/26/lync-and-yahoo-federation-end-of-life.aspx) no blog da equipe do Lync.</span><span class="sxs-lookup"><span data-stu-id="7ad10-137">Read [the announcement](https://blogs.technet.com/b/lync/archive/2012/11/26/lync-and-yahoo-federation-end-of-life.aspx) on the Lync Team Blog.</span></span> <span data-ttu-id="7ad10-138">Os clientes que têm licenças de PIC em contratos que vão até 30 de junho de 2014 receberão um crédito em proporção ao valor dos pagamentos que abrangem o período de 30 de junho de 2014.</span><span class="sxs-lookup"><span data-stu-id="7ad10-138">Customers who have PIC licenses on agreements that extend past June 30, 2014 will receive a credit in proportion to the amount of the payments covering the time period following June 30, 2014.</span></span>

  - <span data-ttu-id="7ad10-139">A **AOL** – em 30 de junho de 2014, o serviço de conectividade de IM ("pic") do Lync não estará mais disponível.</span><span class="sxs-lookup"><span data-stu-id="7ad10-139">**AOL** - On June 30, 2014, Lync's IM connectivity ("PIC") service will no longer be available.</span></span> <span data-ttu-id="7ad10-140">Para limitar a interrupção do cliente quando o serviço terminar, descontinuamos o provisionamento de domínios adicionais do cliente.</span><span class="sxs-lookup"><span data-stu-id="7ad10-140">In order to limit customer disruption when the service ends, we have discontinued the provisioning of additional customer domains.</span></span> <span data-ttu-id="7ad10-141">Até 30 de junho de 2014, os clientes não precisam fazer nada para continuar a dar suporte às comunicações federadas com o AIM.</span><span class="sxs-lookup"><span data-stu-id="7ad10-141">Until June 30, 2014, customers do not need to do anything to continue to support federated communications with AIM.</span></span> <span data-ttu-id="7ad10-142">Além dessa data (ou para clientes que queiram provisionar domínios adicionais nesse meio tempo), um serviço substituto está disponível diretamente na AOL.</span><span class="sxs-lookup"><span data-stu-id="7ad10-142">Beyond this date (or for customers that would like to provision additional domains in the meantime), a substitute service is available directly from AOL.</span></span> <span data-ttu-id="7ad10-143">Para obter mais informações sobre o novo serviço da AOL, consulte [estabelecendo Federação direta com AIM](http://aimenterprise.aol.com/pic.php)  (abre a nova página no AOL.com).</span><span class="sxs-lookup"><span data-stu-id="7ad10-143">For more information on AOL's new service, see [Establishing Direct Federation with AIM](http://aimenterprise.aol.com/pic.php)  (opens new page on AOL.com).</span></span>  

</div>

<div>

## <a name="public-im-provider-summary"></a><span data-ttu-id="7ad10-144">Resumo do provedor de mensagens de chat públicas</span><span class="sxs-lookup"><span data-stu-id="7ad10-144">Public IM Provider Summary</span></span>

<span data-ttu-id="7ad10-145">A tabela a seguir fornece um resumo dos provedores de serviços públicos de mensagens instantâneas, recursos de Federação com o Lync e requisitos de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="7ad10-145">The following table provides a summary of the Public IM service providers, federation capabilities with Lync, and licensing requirements.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ad10-146">Provedor de serviço público de mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="7ad10-146">Public IM Service Provider</span></span></th>
<th><span data-ttu-id="7ad10-147">Recursos federados</span><span class="sxs-lookup"><span data-stu-id="7ad10-147">Federated Capabilities</span></span></th>
<th><span data-ttu-id="7ad10-148">Requisitos de licenciamento</span><span class="sxs-lookup"><span data-stu-id="7ad10-148">Licensing Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ad10-149">Skype</span><span class="sxs-lookup"><span data-stu-id="7ad10-149">Skype</span></span></p></td>
<td><p><span data-ttu-id="7ad10-150">Mensagens instantâneas, presença, áudio</span><span class="sxs-lookup"><span data-stu-id="7ad10-150">IM, Presence, Audio</span></span></p></td>
<td><p><span data-ttu-id="7ad10-151">Licenças de acesso para cliente do Lync Server, plano do Lync Online 1/2/3</span><span class="sxs-lookup"><span data-stu-id="7ad10-151">Lync Server Client Access Licenses, Lync Online Plan 1/2/3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ad10-152">Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="7ad10-152">Windows Live Messenger</span></span></p></td>
<td><p><span data-ttu-id="7ad10-153">Mensagens instantâneas, presença, áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="7ad10-153">IM, Presence, Audio/Video</span></span></p></td>
<td><p><span data-ttu-id="7ad10-154">Licenças de acesso para cliente do Lync Server (com suporte desde que o WLM esteja no mercado)</span><span class="sxs-lookup"><span data-stu-id="7ad10-154">Lync Server Client Access Licenses (supported as long as WLM is in market)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ad10-155">AOL</span><span class="sxs-lookup"><span data-stu-id="7ad10-155">AOL</span></span></p></td>
<td><p><span data-ttu-id="7ad10-156">Mensagens instantâneas, presença</span><span class="sxs-lookup"><span data-stu-id="7ad10-156">IM, Presence</span></span></p></td>
<td><p><span data-ttu-id="7ad10-157">Licenças de acesso para cliente do Lync Server; compatível até junho de 2014 para clientes atuais.</span><span class="sxs-lookup"><span data-stu-id="7ad10-157">Lync Server Client Access Licenses; supported through June 2014 for existing customers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ad10-158">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="7ad10-158">Yahoo!</span></span></p></td>
<td><p><span data-ttu-id="7ad10-159">Mensagens instantâneas, presença</span><span class="sxs-lookup"><span data-stu-id="7ad10-159">IM, Presence</span></span></p></td>
<td><p><span data-ttu-id="7ad10-160">Requer licença de assinatura de usuário de conectividade de mensagem pública adicional do Microsoft Lync ("PIC USL"), além de licenças de acesso para cliente do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7ad10-160">Requires additional Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) in addition to Lync Server Client Access Licences.</span></span> <span data-ttu-id="7ad10-161">A partir da lista de preços de setembro de 2012, o PIC USL não está mais disponível para compra.</span><span class="sxs-lookup"><span data-stu-id="7ad10-161">As of the September 2012 Price List, the PIC USL is no longer available for purchase.</span></span> <span data-ttu-id="7ad10-162">Os clientes com licenças ativas podem continuar a federar-se com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="7ad10-162">Customers with active licenses are able to continue to federate with Yahoo!</span></span> <span data-ttu-id="7ad10-163">Messenger até a data de encerramento do serviço em 30 de junho de 2014.</span><span class="sxs-lookup"><span data-stu-id="7ad10-163">Messenger until the service shut down date on June 30, 2014.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7ad10-164">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ad10-164">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

