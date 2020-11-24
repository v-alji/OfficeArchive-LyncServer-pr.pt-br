---
title: 'Lync Server 2013: planejando o controle de chamada remota'
description: 'Lync Server 2013: planejando o controle de chamada remota.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for remote call control
ms:assetid: 688a0328-1aa7-449f-b5f7-98c876112ed2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558658(v=OCS.15)
ms:contentKeyID: 48184371
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e3a089a806683098a948d235559bbcb16224bdde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390459"
---
# <a name="planning-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="c937c-103">Planejando o controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c937c-103">Planning for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c937c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c937c-104">

<span> </span></span></span>

<span data-ttu-id="c937c-105">_**Tópico da última modificação:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="c937c-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="c937c-106">No Lync Server 2013, o suporte para cenários de controle de chamada remota permite que os usuários controlem seus telefones PBX (Private Branch Exchange) usando o Lync 2013 em seus computadores desktop.</span><span class="sxs-lookup"><span data-stu-id="c937c-106">In Lync Server 2013, support for remote call control scenarios enables users to control their private branch exchange (PBX) phones by using Lync 2013 on their desktop computers.</span></span> <span data-ttu-id="c937c-107">Esta seção descreve os recursos de controle de chamada remota e os requisitos para a implantação do controle de chamada remota.</span><span class="sxs-lookup"><span data-stu-id="c937c-107">This section describes remote call control features and requirements for deploying remote call control.</span></span>

<span data-ttu-id="c937c-108">A integração entre um PBX e o Lync Server 2013 torna possível aos usuários habilitados para controle de chamada remota usar a interface do usuário do Lync 2013 para controlar chamadas em seus telefones PBX das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="c937c-108">Integration between a PBX and Lync Server 2013 makes it possible for users enabled for remote call control to use the Lync 2013 user interface (UI) to control calls on their PBX phones in the following ways:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c937c-109">Por fim, os recursos do PBX que hospedam o telefone PBX de um usuário determinam os recursos de controle de chamada remota que estarão disponíveis para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="c937c-109">Ultimately, the capabilities of the PBX that hosts a user’s PBX phone determine the remote call control features that will be available to that user.</span></span>



</div>

  - <span data-ttu-id="c937c-110">Fazer uma chamada de saída</span><span class="sxs-lookup"><span data-stu-id="c937c-110">Make an outgoing call</span></span>

  - <span data-ttu-id="c937c-111">Atender uma chamada de entrada</span><span class="sxs-lookup"><span data-stu-id="c937c-111">Answer an incoming call</span></span>

  - <span data-ttu-id="c937c-112">Atender uma chamada de entrada com uma mensagem instantânea</span><span class="sxs-lookup"><span data-stu-id="c937c-112">Answer an incoming call with an instant message</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c937c-113">Ou seja, quando o número de telefone do chamador pode ser associado a um endereço de mensagem instantânea na GAL (lista de endereços global) da sua organização, na lista de contatos do Lync do chamador ou na organização de um parceiro federado.</span><span class="sxs-lookup"><span data-stu-id="c937c-113">That is, when the caller’s phone number can be associated with an instant message address in your organization’s global address list (GAL), in the callee’s Lync Contacts list, or in a federated partner’s organization.</span></span>

    
    </div>

  - <span data-ttu-id="c937c-114">Transferir uma chamada</span><span class="sxs-lookup"><span data-stu-id="c937c-114">Transfer a call</span></span>

  - <span data-ttu-id="c937c-115">Encaminhar uma chamada de entrada</span><span class="sxs-lookup"><span data-stu-id="c937c-115">Forward an incoming call</span></span>

  - <span data-ttu-id="c937c-116">Fazer chamadas em espera</span><span class="sxs-lookup"><span data-stu-id="c937c-116">Place calls on hold</span></span>

  - <span data-ttu-id="c937c-117">Alternar entre várias chamadas simultâneas</span><span class="sxs-lookup"><span data-stu-id="c937c-117">Alternate between multiple concurrent calls</span></span>

  - <span data-ttu-id="c937c-118">Atender uma segunda chamada enquanto já estiver em uma chamada (ou seja, chamada em espera)</span><span class="sxs-lookup"><span data-stu-id="c937c-118">Answer a second call while already in a call (that is, call waiting)</span></span>

  - <span data-ttu-id="c937c-119">Discar dígitos de multifrequência (DTMF) de Tom duplo</span><span class="sxs-lookup"><span data-stu-id="c937c-119">Dial dual-tone multifrequency (DTMF) digits</span></span>

  - <span data-ttu-id="c937c-120">Na janela de conversa, digite anotações no programa de anotações do Microsoft Office OneNote</span><span class="sxs-lookup"><span data-stu-id="c937c-120">In the Conversation window, type notes in Microsoft Office OneNote note-taking program</span></span>

<span data-ttu-id="c937c-121">Além disso, quando um usuário está habilitado para controle de chamada remota, o Lync 2013 fornece ao usuário as seguintes informações de chamada:</span><span class="sxs-lookup"><span data-stu-id="c937c-121">Additionally, when a user is enabled for remote call control, Lync 2013 provides the user with the following call information:</span></span>

  - <span data-ttu-id="c937c-122">Identificação de um chamador por nome quando o número de telefone do chamador existe na lista de contatos de um cliente de colaboração e mensagens do Microsoft Office Outlook habilitado para controle de chamada remota, lista de contatos do Lync ou GAL da sua organização.</span><span class="sxs-lookup"><span data-stu-id="c937c-122">Identification of a caller by name when the caller’s phone number exists in the Contacts list of a remote call control-enabled user’s Microsoft Office Outlook messaging and collaboration client, Lync Contacts list, or your organization’s GAL.</span></span>

  - <span data-ttu-id="c937c-123">Chamadas de entrada e saída passadas, que são salvas na pasta Histórico de conversas no Outlook.</span><span class="sxs-lookup"><span data-stu-id="c937c-123">Past incoming and outgoing calls, which are saved in the Conversation History folder in Outlook.</span></span>

  - <span data-ttu-id="c937c-124">Notificações de chamada perdida, que são enviadas para a pasta caixa de entrada do Outlook do usuário, mas são geradas apenas se o Lync estiver sendo executado quando a chamada de entrada for recebida.</span><span class="sxs-lookup"><span data-stu-id="c937c-124">Missed call notifications, which are sent to the user’s Outlook Inbox folder, but are generated only if Lync is running when the incoming call is received.</span></span>

<div>

## <a name="remote-call-control-and-enterprise-voice"></a><span data-ttu-id="c937c-125">Controle de chamada remota e Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="c937c-125">Remote Call Control and Enterprise Voice</span></span>

<span data-ttu-id="c937c-126">Embora os recursos de controle de chamada remota sejam separados das funcionalidades do Enterprise Voice e os usuários não podem ser habilitados para ambos, o Enterprise Voice fornece um subconjunto de recursos que também estão disponíveis para os usuários que estão habilitados para controle de chamada remota.</span><span class="sxs-lookup"><span data-stu-id="c937c-126">Although remote call control features are separate from Enterprise Voice features and users cannot be enabled for both, Enterprise Voice provides a subset of features that are also available to users who are enabled for remote call control.</span></span> <span data-ttu-id="c937c-127">Se o Enterprise Voice for implantado, os usuários habilitados para controle de chamada remota poderão usar o Lync para acessar os seguintes recursos da Enterprise Voice:</span><span class="sxs-lookup"><span data-stu-id="c937c-127">If Enterprise Voice is deployed, users who are enabled for remote call control can use Lync to access the following Enterprise Voice features:</span></span>

  - <span data-ttu-id="c937c-128">Fazer e receber chamadas de áudio para outro cliente do Lync</span><span class="sxs-lookup"><span data-stu-id="c937c-128">Make and receive audio calls to another Lync client</span></span>

  - <span data-ttu-id="c937c-129">Ingressar na parte de áudio de uma conferência criada por um usuário habilitado para o Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="c937c-129">Join the audio portion of a conference created by a user who is enabled for Enterprise Voice</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c937c-130">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c937c-130">In This Section</span></span>

  - [<span data-ttu-id="c937c-131">Tarefas de implantação de controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c937c-131">Deployment tasks for remote call control in Lync Server 2013</span></span>](lync-server-2013-deployment-tasks-for-remote-call-control.md)

<span data-ttu-id="c937c-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c937c-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

