---
title: 'Lync Server 2013: Interoperabilidade do Cliente no Lync 2013'
description: 'Lync Server 2013: interoperabilidade do cliente no Lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client interoperability in Lync 2013
ms:assetid: 0f126571-91a2-45d5-855c-1e4ddb45fc04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204672(v=OCS.15)
ms:contentKeyID: 48183417
ms.date: 03/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea6e90d9479f03dd6d946787e70a2b3cc078699
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434918"
---
# <a name="client-interoperability-in-lync-2013"></a><span data-ttu-id="4f51b-103">Interoperabilidade do Cliente no Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-103">Client interoperability in Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f51b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f51b-104">

<span> </span></span></span>

<span data-ttu-id="4f51b-105">_**Tópico da última modificação:** 2016-03-04_</span><span class="sxs-lookup"><span data-stu-id="4f51b-105">_**Topic Last Modified:** 2016-03-04_</span></span>

<span data-ttu-id="4f51b-106">Este tópico discute a capacidade dos clientes do Microsoft Lync Server 2013 de coexistência e interação com clientes de versões anteriores do Lync Server e do Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="4f51b-106">This topic discusses the ability of Microsoft Lync Server 2013 clients to coexist and interact with clients from earlier versions of Lync Server and Office Communications Server.</span></span>

<div>

## <a name="server-and-client-compatibility"></a><span data-ttu-id="4f51b-107">Compatibilidade do servidor e do cliente</span><span class="sxs-lookup"><span data-stu-id="4f51b-107">Server and Client Compatibility</span></span>

<span data-ttu-id="4f51b-108">A tabela a seguir mostra as combinações de versões de servidor e versões de cliente com suporte.</span><span class="sxs-lookup"><span data-stu-id="4f51b-108">The following table shows the supported combinations of client versions and server versions.</span></span> <span data-ttu-id="4f51b-109">Esta tabela indica se há suporte para entrada quando o cliente tenta se conectar ao servidor indicado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-109">This table indicates whether sign-in is supported when the client attempts to connect to the server indicated.</span></span> <span data-ttu-id="4f51b-110">O Lync Server 2013 dá suporte à versão anterior do cliente.</span><span class="sxs-lookup"><span data-stu-id="4f51b-110">Lync Server 2013 supports the previous client version.</span></span> <span data-ttu-id="4f51b-111">Além disso, ao contrário das versões anteriores, o Lync Server 2010 oferece suporte aos novos clientes do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-111">Also, unlike previous releases, Lync Server 2010 supports the new Lync 2013 clients.</span></span> <span data-ttu-id="4f51b-112">Isso permite que as organizações que estão fazendo a atualização do Lync Server 2010 para distribuir novos clientes independentemente das atualizações do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4f51b-112">This allows organizations who are upgrading from Lync Server 2010 to roll out new clients independent of Lync Server upgrades.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f51b-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="4f51b-113">Client</span></span></th>
<th><span data-ttu-id="4f51b-114">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-114">Lync Server 2013</span></span></th>
<th><span data-ttu-id="4f51b-115">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-115">Lync Server 2010</span></span></th>
<th><span data-ttu-id="4f51b-116">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4f51b-116">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-117">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-117">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="4f51b-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-118">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-119">Supported5</span><span class="sxs-lookup"><span data-stu-id="4f51b-119">Supported5</span></span></p></td>
<td><p><span data-ttu-id="4f51b-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-120">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-121">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="4f51b-121">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="4f51b-122">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-122">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-123">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-123">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-124">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-124">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-125">Lync Web App 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-125">Lync Web App 2013</span></span></p></td>
<td><p><span data-ttu-id="4f51b-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-126">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-127">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-127">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-128">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-128">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-129">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-129">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4f51b-130">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-130">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-131">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-132">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-132">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-133">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="4f51b-133">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="4f51b-134">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-134">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-135">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-135">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-136">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-136">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-137">Chat de Grupo do Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-137">Lync 2010 Group Chat</span></span></p></td>
<td><p><span data-ttu-id="4f51b-138">Supported1</span><span class="sxs-lookup"><span data-stu-id="4f51b-138">Supported1</span></span></p></td>
<td><p><span data-ttu-id="4f51b-139">Supported2</span><span class="sxs-lookup"><span data-stu-id="4f51b-139">Supported2</span></span></p></td>
<td><p><span data-ttu-id="4f51b-140">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="4f51b-140">Not Applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-141">Lync Web App 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-141">Lync Web App 2010</span></span></p></td>
<td><p><span data-ttu-id="4f51b-142">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-142">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-143">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-143">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-144">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-144">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-145">Lync 2010 Attendee</span><span class="sxs-lookup"><span data-stu-id="4f51b-145">Lync 2010 Attendee</span></span></p></td>
<td><p><span data-ttu-id="4f51b-146">Não Supported3</span><span class="sxs-lookup"><span data-stu-id="4f51b-146">Not Supported3</span></span></p></td>
<td><p><span data-ttu-id="4f51b-147">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-147">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-148">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-148">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-149">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4f51b-149">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="4f51b-150">Interoperable4</span><span class="sxs-lookup"><span data-stu-id="4f51b-150">Interoperable4</span></span></p></td>
<td><p><span data-ttu-id="4f51b-151">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-151">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-152">Compatível</span><span class="sxs-lookup"><span data-stu-id="4f51b-152">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-153">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="4f51b-153">Microsoft Office Communications Server 2007 R2 Attendant</span></span></p></td>
<td><p><span data-ttu-id="4f51b-154">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-154">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-155">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-155">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-156">Compatível</span><span class="sxs-lookup"><span data-stu-id="4f51b-156">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-157">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="4f51b-157">Office Communicator 2007</span></span></p></td>
<td><p><span data-ttu-id="4f51b-158">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-158">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-159">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-159">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-160">Compatível</span><span class="sxs-lookup"><span data-stu-id="4f51b-160">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-161">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="4f51b-161">Office Live Meeting 2007</span></span></p></td>
<td><p><span data-ttu-id="4f51b-162">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-162">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-163">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-163">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-164">Compatível</span><span class="sxs-lookup"><span data-stu-id="4f51b-164">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-165">Aplicativo Lync Windows Store</span><span class="sxs-lookup"><span data-stu-id="4f51b-165">Lync Windows Store app</span></span></p></td>
<td><p><span data-ttu-id="4f51b-166">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-166">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-167">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-167">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-168">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-168">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f51b-169">1Para obter detalhes, confira [migrar do Lync Server 2010, chat em grupo ou Office Communications Server 2007 R2 Grupo chat para o Lync server 2013, servidor de chat persistente](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="4f51b-169">1For details, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="4f51b-170">2In Microsoft Lync Server 2010, a funcionalidade do chat em grupo estava disponível com o servidor de chat em grupo, um aplicativo confiável de terceiros para o Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="4f51b-170">2In Microsoft Lync Server 2010, group chat functionality was available with Group Chat Server, a third-party trusted application for Lync Server 2010.</span></span> <span data-ttu-id="4f51b-171">Os clientes do Lync 2013 não são compatíveis com o Lync Server 2010, o chat em grupo.</span><span class="sxs-lookup"><span data-stu-id="4f51b-171">Lync 2013 clients are not compatible with Lync Server 2010, Group Chat.</span></span>

<span data-ttu-id="4f51b-172">o 3Lync Web App 2013 agora oferece uma experiência completa na reunião, incluindo áudio e vídeo do computador, e é considerado como substituto para o participante do Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="4f51b-172">3Lync Web App 2013 now provides a full in-meeting experience, including computer audio and video, and is considered the replacement for Lync 2010 Attendee.</span></span> <span data-ttu-id="4f51b-173">O Lync 2010 se conectará ao Lync Server 2013 somente quando você estiver usando um navegador sem suporte (Internet Explorer 6 ou Internet Explorer 7) e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4f51b-173">Lync 2010 Attendee will connect to Lync Server 2013 only when you are using an unsupported browser (Internet Explorer 6 or Internet Explorer 7) and Windows XP.</span></span>

<span data-ttu-id="4f51b-174">os recursos de presença e de mensagem instantânea do 4The no Office Communicator 2007 R2 são compatíveis com o Lync Server 2013, mas os recursos de conferência não são.</span><span class="sxs-lookup"><span data-stu-id="4f51b-174">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="4f51b-175">Durante a migração do Office Communications Server 2007 R2, o Office Communicator 2007 R2 é adequado para presença e interoperabilidade de mensagens instantâneas, mas os usuários devem usar o Lync Web App 2013 para ingressar em reuniões do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-175">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

<span data-ttu-id="4f51b-176">5 para obter limitações, consulte "recurso de conferência de suporte para clientes do Lync 2013 no Lync Server 2010 reuniões" mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="4f51b-176">5 For limitations, see "Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings" later in this topic.</span></span>

</div>

<div>

## <a name="interoperability-among-clients"></a><span data-ttu-id="4f51b-177">Interoperabilidade entre clientes</span><span class="sxs-lookup"><span data-stu-id="4f51b-177">Interoperability among Clients</span></span>

<span data-ttu-id="4f51b-178">Com o lançamento do Lync Server 2013, várias versões de cliente podem interagir perfeitamente em cenários ponto a ponto e conferência.</span><span class="sxs-lookup"><span data-stu-id="4f51b-178">With the Lync Server 2013 release, various client versions can interact seamlessly in both peer-to-peer and conferencing scenarios.</span></span> <span data-ttu-id="4f51b-179">Esta seção discute a disponibilidade de recursos quando os usuários interagem com outros usuários que usam versões diferentes de clientes e servidores.</span><span class="sxs-lookup"><span data-stu-id="4f51b-179">This section discusses feature availability when users interact with other users who are using different versions of clients and servers.</span></span>

<div>

## <a name="peer-to-peer-feature-support"></a><span data-ttu-id="4f51b-180">Suporte a recursos ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="4f51b-180">Peer-to-Peer Feature Support</span></span>

<span data-ttu-id="4f51b-181">Os recursos ponto a ponto são suportados para os usuários que são hospedados em diferentes versões do servidor e quem está usando versões diferentes do cliente.</span><span class="sxs-lookup"><span data-stu-id="4f51b-181">Peer-to-peer features are supported for users who are homed on different versions of the server and who are using different client versions.</span></span> <span data-ttu-id="4f51b-182">A experiência do usuário final e os recursos disponíveis são consistentes com os recursos do cliente do usuário e a versão do servidor ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-182">The end-user experience and available features are consistent with the capabilities of the user’s client and the version of the server the user is signed in to.</span></span> <span data-ttu-id="4f51b-183">Em outras palavras:</span><span class="sxs-lookup"><span data-stu-id="4f51b-183">In other words:</span></span>

  - <span data-ttu-id="4f51b-184">Se um usuário estiver conectado ao Lync Server 2013 com um cliente mais antigo, o usuário terá a mesma experiência para a qual ele é usado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-184">If a user is signed in to Lync Server 2013 with an older client, the user will have the same experience he or she is used to.</span></span> <span data-ttu-id="4f51b-185">Nenhum dos novos recursos introduzidos no Lync Server 2013 estará disponível até que o cliente do usuário seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-185">None of the new features introduced in Lync Server 2013 will be available until the user’s client is upgraded.</span></span> <span data-ttu-id="4f51b-186">Exemplos incluem modo de exibição de galeria de vídeos, vídeo em HD, compartilhamento do PowerPoint atualizado e a opção de ativar o áudio e o vídeo dos participantes após a entrada da reunião.</span><span class="sxs-lookup"><span data-stu-id="4f51b-186">Examples include video gallery view, HD video, updated PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="4f51b-187">Os novos recursos estão descritos nos [novos recursos de conferência do Lync server 2013](lync-server-2013-new-conferencing-features.md) e novidades [para clientes do Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="4f51b-187">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

  - <span data-ttu-id="4f51b-188">Se um usuário estiver conectado ao Lync Server 2010 com um cliente do Lync 2013, todos os novos recursos não suportados pelo Lync Server 2010 ficarão indisponíveis até que o usuário seja movido para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-188">If a user is signed in to Lync Server 2010 with a Lync 2013 client, any new features not supported by Lync Server 2010 will be unavailable until the user is moved to Lync Server 2013.</span></span>

<span data-ttu-id="4f51b-189">A tabela a seguir compara a disponibilidade de recursos em sessões ponto a ponto nas quais o cliente está conectado ao Lync Server 2013 ou ao Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="4f51b-189">The following table compares feature availability in peer-to-peer sessions where the client is signed in to either Lync Server 2013 or Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4f51b-190">O Lync Web App e o Lync 2010 participantes são somente clientes de reunião e não estão incluídos nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="4f51b-190">Lync Web App and Lync 2010 Attendee are meeting-only clients and aren’t included in this table.</span></span>



</div>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f51b-191">Cliente</span><span class="sxs-lookup"><span data-stu-id="4f51b-191">Client</span></span></th>
<th><span data-ttu-id="4f51b-192">Mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="4f51b-192">Instant Messaging</span></span></th>
<th><span data-ttu-id="4f51b-193">Presença</span><span class="sxs-lookup"><span data-stu-id="4f51b-193">Presence</span></span></th>
<th><span data-ttu-id="4f51b-194">Voz</span><span class="sxs-lookup"><span data-stu-id="4f51b-194">Voice</span></span></th>
<th><span data-ttu-id="4f51b-195">Vídeo</span><span class="sxs-lookup"><span data-stu-id="4f51b-195">Video</span></span></th>
<th><span data-ttu-id="4f51b-196">Compartilhamento de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="4f51b-196">Application Sharing</span></span></th>
<th><span data-ttu-id="4f51b-197">Transferência de arquivos</span><span class="sxs-lookup"><span data-stu-id="4f51b-197">File Transfer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-198">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-198">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="4f51b-199">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-199">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-200">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-201">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-201">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-202">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-202">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-203">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-203">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-204">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-205">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="4f51b-205">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="4f51b-206">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-207">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-207">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-208">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-209">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-210">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-211">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-211">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-212">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-212">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4f51b-213">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-213">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-214">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-215">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-216">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-217">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-218">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-219">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="4f51b-219">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="4f51b-220">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-220">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-221">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-222">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-222">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-223">Lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="4f51b-223">Lync 2010 Mobile</span></span></p></td>
<td><p><span data-ttu-id="4f51b-224">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-225">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-225">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-226">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="4f51b-226">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="4f51b-227">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-228">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-229">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-229">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-230">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4f51b-230">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="4f51b-231">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-232">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-232">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-233">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-233">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-234">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-235">Sim1</span><span class="sxs-lookup"><span data-stu-id="4f51b-235">Yes1</span></span></p></td>
<td><p><span data-ttu-id="4f51b-236">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-236">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-237">MENSAGEM de chat pública (AOL, Yahoo!)</span><span class="sxs-lookup"><span data-stu-id="4f51b-237">Public IM (AOL, Yahoo!)</span></span></p></td>
<td><p><span data-ttu-id="4f51b-238">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-239">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-239">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-240">MENSAGEM de chat pública (MSN, Windows Live Messenger)</span><span class="sxs-lookup"><span data-stu-id="4f51b-240">Public IM (MSN, Windows Live Messenger)</span></span></p></td>
<td><p><span data-ttu-id="4f51b-241">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-241">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-242">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-243">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-243">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-244">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-244">Yes</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="4f51b-245">A partir de 1º de setembro de 2012, a licença de assinatura de usuário da conectividade de mensagem de chat pública do Microsoft Lync (PIC USL) não está mais disponível para a compra de contratos novos ou de renovação.</span><span class="sxs-lookup"><span data-stu-id="4f51b-245">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="4f51b-246">Os clientes com licenças ativas poderão continuar a federar-se com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="4f51b-246">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="4f51b-247">Messenger até a data de desligamento do serviço.</span><span class="sxs-lookup"><span data-stu-id="4f51b-247">Messenger until the service shutdown date.</span></span> <span data-ttu-id="4f51b-248">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="4f51b-248">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="4f51b-249">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-249">has been announced.</span></span> <span data-ttu-id="4f51b-250">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="4f51b-250">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>..</span></span></P>
> <LI>
> <P><span data-ttu-id="4f51b-251">O PIC USL é uma licença de assinatura por usuário e por mês necessária para o Lync Server ou o Office Communications Server se federar com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="4f51b-251">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="4f51b-252">Spam.</span><span class="sxs-lookup"><span data-stu-id="4f51b-252">Messenger.</span></span> <span data-ttu-id="4f51b-253">O recurso da Microsoft para fornecer esse serviço tem o apoio acordado do Yahoo!, o contrato subjacente para o qual não será renovado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-253">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="4f51b-254">Mais do que nunca, o Lync é uma ferramenta poderosa para a conexão entre organizações e pessoas ao redor do mundo.</span><span class="sxs-lookup"><span data-stu-id="4f51b-254">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="4f51b-255">A Federação com o Windows Live Messenger não requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync.</span><span class="sxs-lookup"><span data-stu-id="4f51b-255">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="4f51b-256">A Federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync atinjam centenas de milhões de pessoas por meio de mensagens instantâneas e de voz.</span><span class="sxs-lookup"><span data-stu-id="4f51b-256">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="4f51b-257">1 no Office Communicator 2007 R2, somente o compartilhamento de área de trabalho (e não o compartilhamento de programas) está disponível.</span><span class="sxs-lookup"><span data-stu-id="4f51b-257">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4f51b-258">O compartilhamento de área de trabalho entre o Office Communicator 2007 R2 e o Skype for Business 2015 não pode ser iniciado a partir do cliente mais recente quando a interface do usuário do cliente do Skype for Business 2015 é imposta.</span><span class="sxs-lookup"><span data-stu-id="4f51b-258">Desktop sharing between Office Communicator 2007 R2 and Skype for Business 2015 cannot be initiated from the newer client when the Skype for Business 2015 client user interface is enforced.</span></span>



</div>

</div>

<div>

## <a name="conferencing-feature-support-for-lync-2013-clients-in-lync-server-2010-meetings"></a><span data-ttu-id="4f51b-259">Suporte do recurso de conferência para clientes do Lync 2013 no Lync Server 2010 reuniões</span><span class="sxs-lookup"><span data-stu-id="4f51b-259">Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings</span></span>

<span data-ttu-id="4f51b-260">Quando os usuários ingressam em reuniões do Lync Server 2010 com um cliente Lync 2013, eles têm acesso aos recursos do cliente Lync 2013 com as seguintes exceções:</span><span class="sxs-lookup"><span data-stu-id="4f51b-260">When users join Lync Server 2010 meetings with a Lync 2013 client, they have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="4f51b-261">Nas opções de gerenciamento de **participantes** , que podem ser acessadas apontando para o ícone pessoas na janela da reunião, a opção **nenhuma mensagem instantânea de reunião** não funciona.</span><span class="sxs-lookup"><span data-stu-id="4f51b-261">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="4f51b-262">O modo de exibição de galeria não funciona em videoconferências.</span><span class="sxs-lookup"><span data-stu-id="4f51b-262">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="4f51b-263">O usuário vê apenas o alto-falante ativo em vez de todos os alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="4f51b-263">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="4f51b-264">Na lista de opções **escolher um layout** , o **modo de exibição Galeria** não está disponível</span><span class="sxs-lookup"><span data-stu-id="4f51b-264">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="4f51b-265">A lista de participantes é exibida por padrão em videoconferências.</span><span class="sxs-lookup"><span data-stu-id="4f51b-265">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="4f51b-266">Ao clicar com o botão direito do mouse em um usuário na lista de participantes, o botão **bloquear as opções de gerenciamento de participantes do vídeo** e **fixar em Galeria** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="4f51b-266">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

<div>

## <a name="conferencing-feature-support-in-lync-server-2013-meetings"></a><span data-ttu-id="4f51b-267">Suporte do recurso de conferência nas reuniões do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-267">Conferencing Feature Support in Lync Server 2013 Meetings</span></span>

<span data-ttu-id="4f51b-268">O Lync Server 2013 oferece novos recursos de conferência que se tornam disponíveis para os usuários após suas contas serem movidos para o Lync Server 2013 e que entram com o cliente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-268">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="4f51b-269">Os exemplos incluem modo de exibição de galeria de vídeo, vídeo em alta definição, compartilhamento de PowerPoint e opção para desativar o áudio e o vídeo dos participantes após a entrada da reunião.</span><span class="sxs-lookup"><span data-stu-id="4f51b-269">Examples include video gallery view, HD video, PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="4f51b-270">Os novos recursos estão descritos nos [novos recursos de conferência do Lync server 2013](lync-server-2013-new-conferencing-features.md) e novidades [para clientes do Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="4f51b-270">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="4f51b-271">Em reuniões do Lync Server 2013, determinados recursos de conferência têm suporte para os usuários que são hospedados em diferentes versões do servidor e quem usa diferentes clientes e versões do cliente.</span><span class="sxs-lookup"><span data-stu-id="4f51b-271">In Lync Server 2013 meetings, certain conferencing features are supported for users who are homed on different versions of the server and who are using different clients and client versions.</span></span> <span data-ttu-id="4f51b-272">Quando os clientes ingressam em uma reunião do Lync Server 2013, os usuários têm acesso aos recursos e funcionalidades mostrados nessa tabela.</span><span class="sxs-lookup"><span data-stu-id="4f51b-272">When clients join a Lync Server 2013 meeting, users have access to the features and capabilities shown in this table.</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f51b-273">Cliente</span><span class="sxs-lookup"><span data-stu-id="4f51b-273">Client</span></span></th>
<th><span data-ttu-id="4f51b-274">Mensagem instantânea ponto a ponto</span><span class="sxs-lookup"><span data-stu-id="4f51b-274">Peer-to-peer IM</span></span></th>
<th><span data-ttu-id="4f51b-275">Voz</span><span class="sxs-lookup"><span data-stu-id="4f51b-275">Voice</span></span></th>
<th><span data-ttu-id="4f51b-276">Vídeo</span><span class="sxs-lookup"><span data-stu-id="4f51b-276">Video</span></span></th>
<th><span data-ttu-id="4f51b-277">Compartilhamento de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="4f51b-277">Application Sharing</span></span></th>
<th><span data-ttu-id="4f51b-278">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="4f51b-278">PowerPoint</span></span></th>
<th><span data-ttu-id="4f51b-279">Transferência de arquivos</span><span class="sxs-lookup"><span data-stu-id="4f51b-279">File Transfer</span></span></th>
<th><span data-ttu-id="4f51b-280">Quadro de comunicações</span><span class="sxs-lookup"><span data-stu-id="4f51b-280">Whiteboard</span></span></th>
<th><span data-ttu-id="4f51b-281">Poll</span><span class="sxs-lookup"><span data-stu-id="4f51b-281">Polling</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-282">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-282">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="4f51b-283">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-283">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-284">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-285">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-285">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-286">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-286">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-287">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-287">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-288">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-289">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-289">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-290">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-290">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-291">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="4f51b-291">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="4f51b-292">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-293">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-293">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-294">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-294">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-295">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-295">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-296">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-297">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-297">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-298">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-298">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-299">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-299">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-300">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="4f51b-300">Lync Web App</span></span></p></td>
<td><p><span data-ttu-id="4f51b-301">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-301">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-302">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-302">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-303">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-303">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-304">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-305">Sim2</span><span class="sxs-lookup"><span data-stu-id="4f51b-305">Yes2</span></span></p></td>
<td><p><span data-ttu-id="4f51b-306">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-306">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-307">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-307">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-308">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-308">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-309">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-309">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4f51b-310">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-311">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-311">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-312">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-312">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-313">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-314">Sim3</span><span class="sxs-lookup"><span data-stu-id="4f51b-314">Yes3</span></span></p></td>
<td><p><span data-ttu-id="4f51b-315">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-315">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-316">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-316">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f51b-317">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-317">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-318">Office Communicator 2007 R2 4</span><span class="sxs-lookup"><span data-stu-id="4f51b-318">Office Communicator 2007 R2 4</span></span></p></td>
<td><p><span data-ttu-id="4f51b-319">Sim</span><span class="sxs-lookup"><span data-stu-id="4f51b-319">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f51b-320">1 no Office Communicator 2007 R2, somente o compartilhamento de área de trabalho (e não o compartilhamento de programas) está disponível.</span><span class="sxs-lookup"><span data-stu-id="4f51b-320">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<span data-ttu-id="4f51b-321">2 o Lync Server 2013 usa um mecanismo atualizado para carregar arquivos do PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="4f51b-321">2 Lync Server 2013 uses an updated mechanism for uploading PowerPoint files.</span></span> <span data-ttu-id="4f51b-322">Os usuários do Lync Web App que ingressarem em uma reunião originalmente agendada no Lync Server 2010 podem exibir e navegar em apresentações do PowerPoint, mas não podem carregar arquivos do PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="4f51b-322">Lync Web App users who join a meeting that was originally scheduled on Lync Server 2010 can view and navigate PowerPoint presentations, but cannot upload PowerPoint files.</span></span>

<span data-ttu-id="4f51b-323">3 se a reunião tiver sido agendada nos slides do Lync Server 2013 e do PowerPoint foram carregadas por um cliente do Lync 2013, os usuários do Lync 2010 terão acesso somente para exibição aos slides.</span><span class="sxs-lookup"><span data-stu-id="4f51b-323">3 If the meeting was scheduled on Lync Server 2013 and PowerPoint slides were uploaded by a Lync 2013 client, Lync 2010 users have view-only access to the slides.</span></span> <span data-ttu-id="4f51b-324">Por outro lado, se os slides do PowerPoint foram carregados por um usuário do Lync 2010, os usuários do Lync Server 2013 poderão exibir e nos slides e, se o Office Web Apps estiver configurado, acessar novos recursos, como exibição de resolução mais alta, animações, transições de slides e vídeo incorporado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-324">Conversely, if the PowerPoint slides were uploaded by a Lync 2010 user, Lync Server 2013 users will be able to view and slides and, if Office Web Apps Server is configured, access new capabilities such as higher resolution display, animations, slide transitions, and embedded video.</span></span> <span data-ttu-id="4f51b-325">Para obter mais informações, consulte [Configurando a integração com o servidor do Office Web Apps e o Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="4f51b-325">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="4f51b-326">os recursos de presença e de mensagem instantânea do 4The no Office Communicator 2007 R2 são compatíveis com o Lync Server 2013, mas os recursos de conferência não são.</span><span class="sxs-lookup"><span data-stu-id="4f51b-326">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="4f51b-327">Durante a migração do Office Communications Server 2007 R2, o Office Communicator 2007 R2 é adequado para presença e interoperabilidade de mensagens instantâneas, mas os usuários devem usar o Lync Web App 2013 para ingressar em reuniões do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-327">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

</div>

</div>

<div>

## <a name="scheduling-add-in-support"></a><span data-ttu-id="4f51b-328">Agendando o suporte ao suplemento</span><span class="sxs-lookup"><span data-stu-id="4f51b-328">Scheduling Add-in Support</span></span>

<span data-ttu-id="4f51b-329">O suporte do servidor para os vários suplementos de agendamento é consistente com a compatibilidade de versão do servidor e do cliente.</span><span class="sxs-lookup"><span data-stu-id="4f51b-329">Server support for the various scheduling add-ins is consistent with server and client version compatibility.</span></span> <span data-ttu-id="4f51b-330">Em geral, os seguintes suplementos de agendamento são suportados no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-330">In general, the following scheduling add-ins are supported on Lync Server 2013.</span></span> <span data-ttu-id="4f51b-331">No entanto, as versões anteriores dos suplementos não fornecem novos recursos de suplemento do Lync 2013, como a opção de ativar o áudio e o vídeo dos participantes após a entrada da reunião.</span><span class="sxs-lookup"><span data-stu-id="4f51b-331">However, previous versions of add-ins do not provide new Lync 2013 add-in features, such as the option to mute all attendee audio and video upon meeting entry.</span></span>

  - <span data-ttu-id="4f51b-332">**Suplemento de reunião online para o Lync 2013**   Oferece os mesmos recursos que o suplemento de reunião online do Lync 2010, com a adição de controles de desativação de participantes, que permitem que os organizadores da reunião agendem conferências com áudio e vídeo de participantes com mudo ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="4f51b-332">**Online Meeting Add-in for Lync 2013**   Provides the same features as the Online Meeting Add-in for Lync 2010, with the addition of attendee mute controls, which allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span> <span data-ttu-id="4f51b-333">Os administradores também podem personalizar os convites para reunião da organização adicionando um logotipo personalizado, uma URL de suporte, uma URL de isenção de responsabilidade legal ou texto de rodapé personalizado.</span><span class="sxs-lookup"><span data-stu-id="4f51b-333">Administrators can also customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span>

  - <span data-ttu-id="4f51b-334">**Suplemento de reunião online para o Lync 2010**   Fornece agendamento para reuniões do Lync e remove a funcionalidade de agendar conferências do Office Live Meeting.</span><span class="sxs-lookup"><span data-stu-id="4f51b-334">**Online Meeting Add-in for Lync 2010**   Provides scheduling for Lync meetings and removes the capability to schedule Office Live Meeting conferences.</span></span>

  - <span data-ttu-id="4f51b-335">**Suplemento de conferência do Office Communicator 2007 R2**   Fornece agendamento para conferências do Office Live Meeting e do Office Communicator 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="4f51b-335">**Office Communicator 2007 R2 Conferencing Add-in**   Provides scheduling for both Office Live Meeting conferences and Office Communicator 2007 R2 conferences.</span></span> 

<div>


> [!NOTE]  
> <span data-ttu-id="4f51b-336">Não é possível agendar conferências do Live Meeting no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-336">Live Meeting conferences cannot be scheduled on Lync Server 2013.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f51b-337">Cliente de agendamento</span><span class="sxs-lookup"><span data-stu-id="4f51b-337">Scheduling Client</span></span></th>
<th><span data-ttu-id="4f51b-338">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-338">Lync Server 2013</span></span></th>
<th><span data-ttu-id="4f51b-339">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-339">Lync Server 2010</span></span></th>
<th><span data-ttu-id="4f51b-340">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4f51b-340">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-341">Suplemento de reunião online do Lync 2013 (pode ser usado com o Office 2013, o Outlook 2010 e o Outlook 2007)</span><span class="sxs-lookup"><span data-stu-id="4f51b-341">Online Meeting Add-in for Lync 2013 (can be used with Office 2013, Outlook 2010, and Outlook 2007)</span></span></p></td>
<td><p><span data-ttu-id="4f51b-342">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-342">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-343">Com suporte (novos recursos de suplemento não disponíveis)</span><span class="sxs-lookup"><span data-stu-id="4f51b-343">Supported (new add-in features not available)</span></span></p></td>
<td><p><span data-ttu-id="4f51b-344">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-344">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-345">Agendador da Web do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-345">Lync 2013 Web Scheduler</span></span></p></td>
<td><p><span data-ttu-id="4f51b-346">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-346">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-347">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-347">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-348">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-348">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f51b-349">Suplemento de Reunião Online para Lync 2010</span><span class="sxs-lookup"><span data-stu-id="4f51b-349">Online Meeting Add-in for Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="4f51b-350">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-350">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-351">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-351">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-352">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-352">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f51b-353">Suplemento de conferência do Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="4f51b-353">Office Communicator 2007 R2 Conferencing Add-in</span></span></p></td>
<td><p><span data-ttu-id="4f51b-354">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4f51b-354">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-355">Compatível </span><span class="sxs-lookup"><span data-stu-id="4f51b-355">Supported</span></span></p></td>
<td><p><span data-ttu-id="4f51b-356">Compatível</span><span class="sxs-lookup"><span data-stu-id="4f51b-356">Supported</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="support-for-joining-meetings"></a><span data-ttu-id="4f51b-357">Suporte para ingressar em reuniões</span><span class="sxs-lookup"><span data-stu-id="4f51b-357">Support for Joining Meetings</span></span>

<span data-ttu-id="4f51b-358">Todos os clientes aos quais o Lync Server 2013 dá suporte têm permissão para ingressar em reuniões do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="4f51b-358">All of the clients that Lync Server 2013 supports are allowed to join Lync 2013 meetings.</span></span> <span data-ttu-id="4f51b-359">Como o Lync Web App é um componente da Web do servidor, em casos em que o Lync Web App é usado para ingressar em uma reunião do Lync Server 2013, a versão mais recente do Lync Web App é sempre usada.</span><span class="sxs-lookup"><span data-stu-id="4f51b-359">Because Lync Web App is a web component of the server, in cases where Lync Web App is used to join a Lync Server 2013 meeting, the newer version of Lync Web App is always used.</span></span>

<span data-ttu-id="4f51b-360">Os clientes do Lync 2013 podem ingressar em reuniões hospedadas no Lync 2010 e no Office Communications Server 2007 R2 com funcionalidade reduzida.</span><span class="sxs-lookup"><span data-stu-id="4f51b-360">Lync 2013 clients can join meetings hosted on Lync 2010 and Office Communications Server 2007 R2 with scaled-down functionality.</span></span> <span data-ttu-id="4f51b-361">Os recursos na reunião são limitados pela versão do servidor na qual a reunião está hospedada.</span><span class="sxs-lookup"><span data-stu-id="4f51b-361">In-meeting features are limited by the version of the server on which the meeting is hosted.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4f51b-362">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f51b-362">See Also</span></span>


[<span data-ttu-id="4f51b-363">Requisitos do aplicativo Lync da Windows Store para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-363">Lync Windows Store app requirements for Lync Server 2013</span></span>](lync-server-2013-lync-windows-store-app-requirements.md)  
[<span data-ttu-id="4f51b-364">Novos recursos de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-364">New conferencing features in Lync Server 2013</span></span>](lync-server-2013-new-conferencing-features.md)  
[<span data-ttu-id="4f51b-365">Novidades para clientes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f51b-365">What's new for clients in Lync Server 2013</span></span>](lync-server-2013-what-s-new-for-clients.md)  
  

<span data-ttu-id="4f51b-366"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f51b-366"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

