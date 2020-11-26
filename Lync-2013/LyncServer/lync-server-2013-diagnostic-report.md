---
title: 'Lync Server 2013: relatório de diagnóstico'
description: 'Lync Server 2013: relatório de diagnóstico.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Diagnostic Report
ms:assetid: b389dbd9-f2e8-4184-93d0-2e504796ac16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615445(v=OCS.15)
ms:contentKeyID: 48185159
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 198b836437285b464ba9172e59c9a60ed0a53b65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429301"
---
# <a name="diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="7f0f5-103">Relatório de diagnóstico no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0f5-103">Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f0f5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f0f5-104">

<span> </span></span></span>

<span data-ttu-id="7f0f5-105">_**Tópico da última modificação:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="7f0f5-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<span data-ttu-id="7f0f5-106">O Relatório de diagnóstico fornece diagnósticos e informações para a solução de problemas de uma sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-106">The Diagnostic Report provides diagnostic and troubleshooting information for a failed session.</span></span> <span data-ttu-id="7f0f5-107">Essas informações incluem a ID de diagnóstico e o cabeçalho de Diagnóstico que foram importados quando a sessão falhou.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-107">This information includes both the Diagnostic ID and the Diagnostic header that were reported when the session failed.</span></span> <span data-ttu-id="7f0f5-108">A ID de diagnóstico é um identificador exclusivo (na forma de um cabeçalho ms-diagnostics) que é anexado a uma mensagem SIP, enquanto a cabeçalho de Diagnóstico fornece uma descrição da ID de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-108">The Diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) that gets attached to a SIP message, while the Diagnostic header provides an accompanying description for the Diagnostic ID.</span></span> <span data-ttu-id="7f0f5-109">O relatório também pode conter detalhes importantes para a solução de problemas e que são conhecidos pelo componente de relatório.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-109">The report might also contain valuable troubleshooting details that are known by the reporting component.</span></span> <span data-ttu-id="7f0f5-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7f0f5-110">For example:</span></span>

  - <span data-ttu-id="7f0f5-p102">O código de motivo fornecido pelo gateway da PSTN que gerou a falha. Quando uma chamada de saída falha na rede PSTN, um código de causa ISUP (parte de usuário ISDN, em inglês) é gerado automaticamente. Por exemplo, um gateway PSTN pode enviar o código de causa 34 para indicar que nenhum circuito ou canal estava disponível para completar a chamada.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-p102">The cause code provided by the PSTN gateway that generated the failure. When an outgoing call fails on the PSTN network, an ISDN User Part (ISUP) cause code is automatically generated. For example, a PSTN gateway might send cause code 34 to indicate that no circuit or channel was available for completing the call.</span></span>

  - <span data-ttu-id="7f0f5-114">FQDN do par, porta e erros de Winsock para falhas de conectividade.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-114">Peer FQDN, port, and Winsock errors for connectivity failures.</span></span>

  - <span data-ttu-id="7f0f5-p103">Nomes pesquisados por falhas de resolução de DNS. A resolução DNS ocorre sempre que um cliente entra em contato com um servidor de nomes e solicita o endereço IP que corresponde ao nome de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-p103">Names being looked up for DNS resolution failures. DNS resolution takes place any time a client contacts a name server and requests the IP address that corresponds to specified device name.</span></span>

<div>

## <a name="accessing-the-diagnostic-report"></a><span data-ttu-id="7f0f5-117">Acessando o relatório de diagnósticos</span><span class="sxs-lookup"><span data-stu-id="7f0f5-117">Accessing the Diagnostic Report</span></span>

<span data-ttu-id="7f0f5-118">O relatório de diagnóstico pode ser acessado clicando na métrica relatório de diagnóstico (detalhe) em um [relatório de detalhes de sessão ponto a ponto no Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) ou no relatório de detalhes da conferência.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-118">The Diagnostic Report can be accessed by clicking the Diagnostic Report (Detail) metric on either the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) or the Conference Detail Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="7f0f5-119">Filtros</span><span class="sxs-lookup"><span data-stu-id="7f0f5-119">Filters</span></span>

<span data-ttu-id="7f0f5-p104">Nenhum. Não é possível filtrar o Relatório de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-p104">None. You cannot filter the Diagnostic Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="7f0f5-122">Métricas</span><span class="sxs-lookup"><span data-stu-id="7f0f5-122">Metrics</span></span>

<span data-ttu-id="7f0f5-123">A tabela a seguir lista as informações fornecidas no Relatório de Diagnóstico para cada sessão.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-123">The following table lists the information provided in the Diagnostic Report for each session.</span></span>

### <a name="diagnostic-report-metrics"></a><span data-ttu-id="7f0f5-124">Métricas do Relatório de Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="7f0f5-124">Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f0f5-125">Nome</span><span class="sxs-lookup"><span data-stu-id="7f0f5-125">Name</span></span></th>
<th><span data-ttu-id="7f0f5-126">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="7f0f5-126">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="7f0f5-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f0f5-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f0f5-128"><strong>Hora do relatório</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-128"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-129">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-129">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-130">Data e hora do registro do relatório.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-130">Date and time that the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f0f5-131"><strong>Código da resposta</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-131"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-132">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-132">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-133">Código da resposta SIP enviado quando a sessão falhou.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-133">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f0f5-134"><strong>Tipo de solicitação</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-134"><strong>Request type</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-135">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-135">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-p105">Tipo de solicitação SIP que falhou. Por exemplo, CONVIDAR, ATÉ LOGO ou SERVIÇO.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-p105">SIP request type that failed. For example, INVITE, BYE, or SERVICE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f0f5-138"><strong>Origem</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-138"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-139">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-139">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-140">Origem do erro.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-140">Source of the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f0f5-141"><strong>URI do usuário de origem</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-141"><strong>From user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-142">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-142">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-143">Endereço SIP do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-143">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f0f5-144"><strong>Representante do usuário de origem</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-144"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-145">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-145">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-146">Software usado pelo ponto de extremidade do usuário que iniciou a sessão.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-146">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f0f5-147"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-147"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-148">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-148">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-149">Identificador exclusivo (na forma de um cabeçalho de diagnóstico-ms) anexado a uma mensagem SIP que fornece informações úteis sobre os erros de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-149">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f0f5-150"><strong>Tipo de conteúdo</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-150"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-151">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-151">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-p106">Tipo de conteúdo de mídia que falhou. Por exemplo, um tipo de conteúdo comum é Application/sdp. SDP (Protocolo de descrição de sessão) é um protocolo padrão de Internet usado para anúncios de sessão, convites de sessão e outras formas de início de sessão multimídia.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-p106">Type of media content that failed. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f0f5-155"><strong>Aplicativo</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-155"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-156">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-156">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-157">Aplicativo envolvido no erro.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-157">Application involved in the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f0f5-158"><strong>URI do usuário de destino</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-158"><strong>To user URI</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-159">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-159">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-160">Endereço SIP do usuário convidado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-160">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f0f5-161">Hora de ingresso de conferência (ms)</span><span class="sxs-lookup"><span data-stu-id="7f0f5-161">Conference join times (ms)</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-162">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-162">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-163">Tempo (em milissegundos) que o usuário precisou para ingressar na conferência.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-163">Amount of time (in milliseconds) it took for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f0f5-164"><strong>Cabeçalho do diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="7f0f5-164"><strong>Diagnostic header</strong></span></span></p></td>
<td><p><span data-ttu-id="7f0f5-165">Não</span><span class="sxs-lookup"><span data-stu-id="7f0f5-165">No</span></span></p></td>
<td><p><span data-ttu-id="7f0f5-166">Descrição do ID de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7f0f5-166">Diagnostic ID description.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7f0f5-167">Uma lista de erros de diagnóstico pode ser encontrada na [página de cabeçalho MS-Diagnostics](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx).</span><span class="sxs-lookup"><span data-stu-id="7f0f5-167">A list of diagnostic errors can be found on the [Ms-Diagnostics Header page](https://msdn.microsoft.com/library/gg132446\(v=office.12\).aspx).</span></span>

<span data-ttu-id="7f0f5-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f0f5-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

