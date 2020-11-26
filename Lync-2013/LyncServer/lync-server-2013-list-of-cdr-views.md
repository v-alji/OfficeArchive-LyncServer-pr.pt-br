---
title: 'Lync Server 2013: lista de modos de exibição de CDR'
description: 'Lync Server 2013: lista de modos de exibição de CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of CDR views
ms:assetid: 2f72aead-d1da-4185-b75c-f6c31d76a6b3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688009(v=OCS.15)
ms:contentKeyID: 49733598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f1c29560851c0e4466dbf4316bf0b1335906d4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426589"
---
# <a name="list-of-cdr-views-in-lync-server-2013"></a><span data-ttu-id="0978b-103">Lista de modos de exibição CDR no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0978b-103">List of CDR views in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0978b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0978b-104">

<span> </span></span></span>

<span data-ttu-id="0978b-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="0978b-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="0978b-106">Os modos de exibição fornecem uma maneira fácil de acessar informações sobre os cenários mais comuns usados para retornar dados do banco de dados CDR.</span><span class="sxs-lookup"><span data-stu-id="0978b-106">Views provide an easy way to access information about the most common scenarios used for returning data from the CDR database.</span></span> <span data-ttu-id="0978b-107">É recomendável que você use modos de exibição para criar relatórios personalizados em vez de usar as tabelas de banco de dados CDR reais; Isso porque os modos de exibição de banco de dados são mais prováveis de manter a compatibilidade com versões anteriores do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0978b-107">It is recommended that you use views for building custom reports instead of using the actual CDR database tables ; that’s because the database views are more likely to maintain backwards compatibility with future releases of Lync Server.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0978b-108">Nome do modo de exibição</span><span class="sxs-lookup"><span data-stu-id="0978b-108">View Name</span></span></th>
<th><span data-ttu-id="0978b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0978b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0978b-110"><a href="lync-server-2013-clientversions-view.md">Exibição ClientVersions no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-110"><a href="lync-server-2013-clientversions-view.md">ClientVersions view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-111">Retorna informações sobre o software/dispositivos cliente usados em uma sessão de comunicação.</span><span class="sxs-lookup"><span data-stu-id="0978b-111">Returns information about the client software/devices used in a communication session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-112"><a href="lync-server-2013-conferencemessagecount-view.md">Exibição ConferenceMessageCount no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-112"><a href="lync-server-2013-conferencemessagecount-view.md">ConferenceMessageCount view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-113">Retorna informações sobre o número de mensagens enviadas pelos usuários em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="0978b-113">Returns information about the number of messages sent by users in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0978b-114"><a href="lync-server-2013-conferences-view.md">Modo de exibição conferências no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-114"><a href="lync-server-2013-conferences-view.md">Conferences view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-115">Retorna informações de conferência, incluindo a hora de início, a hora de término e o organizador de conferências.</span><span class="sxs-lookup"><span data-stu-id="0978b-115">Returns conference information, including start time, end time, and conference organizer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-116"><a href="lync-server-2013-conferencesessiondetails-view.md">Exibição ConferenceSessionDetails no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-116"><a href="lync-server-2013-conferencesessiondetails-view.md">ConferenceSessionDetails view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-117">Retorna detalhes de sessão para todas as sessões de conferência, incluindo hora de início e término, IDs de usuário, códigos de resposta e IDs de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0978b-117">Returns session details for all conferencing sessions, including start and end time, user IDs, response codes, and diagnostic IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0978b-118"><a href="lync-server-2013-conferenceuris-view.md">Exibição ConferenceUris no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-118"><a href="lync-server-2013-conferenceuris-view.md">ConferenceUris view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-119">Retorna informações sobre URIs de conferência usados em uma conferência</span><span class="sxs-lookup"><span data-stu-id="0978b-119">Returns information about conference URIs used in a conference</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-120"><a href="lync-server-2013-errorreport-view.md">Exibição ErrorReport no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-120"><a href="lync-server-2013-errorreport-view.md">ErrorReport view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-121">Retorna informações sobre erros ocorridos durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="0978b-121">Returns information about errors that occurred during a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0978b-122"><a href="lync-server-2013-filetransfers-view.md">Modo de exibição de transferência de fileviews no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-122"><a href="lync-server-2013-filetransfers-view.md">FileTransfers view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-123">Retorna informações sobre as sessões de transferência de arquivos, incluindo o nome do arquivo e se a transferência foi aceita, rejeitada ou cancelada.</span><span class="sxs-lookup"><span data-stu-id="0978b-123">Returns information about file transfer sessions, including the file name and whether the transfer was accepted, rejected, or cancelled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-124"><a href="lync-server-2013-focusjoinsandleaves-view.md">Exibição FocusJoinsAndLeaves no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-124"><a href="lync-server-2013-focusjoinsandleaves-view.md">FocusJoinsAndLeaves view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-125">Retorna informações sobre atividades de ingressar em conferência e licença.</span><span class="sxs-lookup"><span data-stu-id="0978b-125">Returns information about conference join and leave activities.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0978b-126"><a href="lync-server-2013-mcujoinsandleaves-view.md">Exibição McuJoinsAndLeaves no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-126"><a href="lync-server-2013-mcujoinsandleaves-view.md">McuJoinsAndLeaves view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-127">Retorna informações combinadas sobre atividades de ingressar em conferência e licença (cada junção de conferência está emparelhada com a saída de conferência correspondente).</span><span class="sxs-lookup"><span data-stu-id="0978b-127">Returns combined information about conference join and leave activities (each conference join is paired with the corresponding conference leave).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-128"><a href="lync-server-2013-mcus-view.md">Exibição MCUs no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-128"><a href="lync-server-2013-mcus-view.md">Mcus view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-129">Retorna informações sobre servidores de conferência.</span><span class="sxs-lookup"><span data-stu-id="0978b-129">Returns information about Conferencing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0978b-130"><a href="lync-server-2013-media-view.md">Modo de exibição de mídia no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-130"><a href="lync-server-2013-media-view.md">Media view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-131">Retorna informações sobre os tipos de mídia usados em sessões de comunicação ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="0978b-131">Returns information about the types of media used in peer-to-peer communication sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-132"><a href="lync-server-2013-progressreport-view.md">Exibição ProgressReport no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-132"><a href="lync-server-2013-progressreport-view.md">ProgressReport view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-133">Retorna informações sobre sessões concluídas.</span><span class="sxs-lookup"><span data-stu-id="0978b-133">Returns information about completed sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0978b-134"><a href="lync-server-2013-registration-view.md">Modo de exibição de registro no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-134"><a href="lync-server-2013-registration-view.md">Registration view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-135">Retorna informações sobre registros com o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0978b-135">Returns information about registrations with Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-136"><a href="lync-server-2013-sessiondetails-view.md">Exibição SessionDetails no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-136"><a href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-137">Retorna informações sobre sessões ponto a ponto, incluindo VoIP-VoIP chamadas telefônicas, sessões de mensagens instantâneas de duas partes ou outras sessões de comunicação ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="0978b-137">Returns information about peer-to-peer sessions, including VoIP-VoIP phone calls, two-party IM sessions, or other peer-to-peer communication sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0978b-138"><a href="lync-server-2013-user-view.md">Modo de exibição de usuário no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-138"><a href="lync-server-2013-user-view.md">User view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-139">Retorna informações sobre os usuários que participaram de sessões de comunicação.</span><span class="sxs-lookup"><span data-stu-id="0978b-139">Returns information about the users who have participated in communication sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0978b-140"><a href="lync-server-2013-voipdetails-view.md">Exibição VoIPDetails no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0978b-140"><a href="lync-server-2013-voipdetails-view.md">VoIPDetails view in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="0978b-141">Retorna informações sobre sessões ponto a ponto que envolvem pelo menos um usuário VoIP (voz sobre e/s).</span><span class="sxs-lookup"><span data-stu-id="0978b-141">Returns information for peer-to-peer sessions involving at least one VoIP (Voice over IO) user.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0978b-142">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0978b-142">


</div>

<span> </span>

</div>

</div>

</span></span></div>

