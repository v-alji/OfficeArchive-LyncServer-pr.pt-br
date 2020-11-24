---
title: 'Lync Server 2013: Iniciando o Lync a partir de outro aplicativo'
description: 'Lync Server 2013: Iniciando o Lync a partir de outro aplicativo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Starting Lync from another application
ms:assetid: 573b30b1-6590-4b24-8e96-a41be57cb0ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398376(v=OCS.15)
ms:contentKeyID: 48184184
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd64b8b9f335638b54a0bf6473b5d159c97a0e7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389766"
---
# <a name="starting-lync-from-another-application"></a><span data-ttu-id="87573-103">Iniciando o Lync a partir de outro aplicativo</span><span class="sxs-lookup"><span data-stu-id="87573-103">Starting Lync from another application</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87573-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87573-104">

<span> </span></span></span>

<span data-ttu-id="87573-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="87573-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="87573-106">Você pode usar parâmetros de linha de comando para iniciar rapidamente o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="87573-106">You can use command-line parameters to quick-start Lync 2013.</span></span> <span data-ttu-id="87573-107">Por exemplo, se um usuário clicar em um número de telefone em outro aplicativo, o aplicativo poderá iniciar uma instância do Lync 2013 e iniciar uma chamada para esse número.</span><span class="sxs-lookup"><span data-stu-id="87573-107">For example, if a user clicks a phone number in another application, the application can start an instance of Lync 2013 and initiate a call to that number.</span></span>

<span data-ttu-id="87573-108">O Lync 2013 também pode reconhecer uma lista delimitada por ponto-e-vírgula de nomes de contatos para conferência multiparte.</span><span class="sxs-lookup"><span data-stu-id="87573-108">Lync 2013 can also recognize a semicolon-delimited list of contact names for multiparty conferencing.</span></span>

<span data-ttu-id="87573-109">Se o Lync 2013 estiver configurado para entrar automaticamente quando iniciado, iniciar o Lync 2013 com parâmetros de linha de comando abrirá a janela principal do Lync.</span><span class="sxs-lookup"><span data-stu-id="87573-109">If Lync 2013 is configured to automatically sign in when started, then starting Lync 2013 with command-line parameters will open the Lync main window.</span></span> <span data-ttu-id="87573-110">Se o Lync não estiver configurado para entrar automaticamente quando iniciado, a janela de entrada será aberta.</span><span class="sxs-lookup"><span data-stu-id="87573-110">If Lync is not configured to automatically sign in when started, the sign-in window opens.</span></span>

<span data-ttu-id="87573-111">A tabela a seguir mostra os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87573-111">The following table shows the available parameters.</span></span>

### <a name="lync-2013-command-line-parameters"></a><span data-ttu-id="87573-112">Parâmetros Command-Line do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="87573-112">Lync 2013 Command-Line Parameters</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87573-113">Prorroga</span><span class="sxs-lookup"><span data-stu-id="87573-113">Extension</span></span></th>
<th><span data-ttu-id="87573-114">Formato dos dados</span><span class="sxs-lookup"><span data-stu-id="87573-114">Format of Data</span></span></th>
<th><span data-ttu-id="87573-115">Action</span><span class="sxs-lookup"><span data-stu-id="87573-115">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87573-116">telefone</span><span class="sxs-lookup"><span data-stu-id="87573-116">tel:</span></span></p></td>
<td><p><span data-ttu-id="87573-117">URI do Tel</span><span class="sxs-lookup"><span data-stu-id="87573-117">tel URI</span></span></p></td>
<td><p><span data-ttu-id="87573-118">Abre a janela de conversa para uma chamada de áudio, mas não disca o número especificado.</span><span class="sxs-lookup"><span data-stu-id="87573-118">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87573-119">callto</span><span class="sxs-lookup"><span data-stu-id="87573-119">callto:</span></span></p></td>
<td><p><span data-ttu-id="87573-120">Tel:, SIP: ou URI de Tel digitado</span><span class="sxs-lookup"><span data-stu-id="87573-120">tel:, sip:, or typeable tel URI</span></span></p></td>
<td><p><span data-ttu-id="87573-121">Abre a janela de conversa para uma chamada de áudio, mas não disca o número especificado.</span><span class="sxs-lookup"><span data-stu-id="87573-121">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87573-122">SPI</span><span class="sxs-lookup"><span data-stu-id="87573-122">sip:</span></span></p></td>
<td><p><span data-ttu-id="87573-123">URI do SIP</span><span class="sxs-lookup"><span data-stu-id="87573-123">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="87573-124">Abre a janela de conversa com o URI (Uniform Resource Identifier) SIP especificado na lista de participantes.</span><span class="sxs-lookup"><span data-stu-id="87573-124">Opens the Conversation window with the specified SIP Uniform Resource Identifier (URI) in the participant list.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87573-125">SIPS</span><span class="sxs-lookup"><span data-stu-id="87573-125">Sips:</span></span></p></td>
<td><p><span data-ttu-id="87573-126">URI do SIP</span><span class="sxs-lookup"><span data-stu-id="87573-126">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="87573-127">Se o Lync 2013 estiver configurado para usar o protocolo TLS (Transport Layer Security), funciona exatamente como SIP:.</span><span class="sxs-lookup"><span data-stu-id="87573-127">If Lync 2013 is configured to use the Transport Layer Security (TLS) protocol, functions exactly like sip:.</span></span> <span data-ttu-id="87573-128">Se o TLS não estiver sendo usado, exibe uma caixa de diálogo informando ao usuário que um nível mais alto de segurança é necessário.</span><span class="sxs-lookup"><span data-stu-id="87573-128">If TLS is not being used, displays a dialog box informing the user that a higher level of security is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87573-129">Conferência</span><span class="sxs-lookup"><span data-stu-id="87573-129">conf:</span></span></p></td>
<td><p><span data-ttu-id="87573-130">URI SIP da conferência para ingressar</span><span class="sxs-lookup"><span data-stu-id="87573-130">SIP URI of conference to join</span></span></p></td>
<td><p><span data-ttu-id="87573-131">Se URI for Self, instancia o foco e mostra o modo de exibição somente de lista.</span><span class="sxs-lookup"><span data-stu-id="87573-131">If URI is self, instantiates the focus and brings up roster-only view.</span></span> <span data-ttu-id="87573-132">Caso contrário, exibe o modo de exibição de lista, mas não envia convite.</span><span class="sxs-lookup"><span data-stu-id="87573-132">Otherwise, brings up roster view but does not send INVITE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87573-133">comunicar</span><span class="sxs-lookup"><span data-stu-id="87573-133">im:</span></span></p></td>
<td><p><span data-ttu-id="87573-134">URI do SIP</span><span class="sxs-lookup"><span data-stu-id="87573-134">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="87573-135">Exibe uma janela de conversa somente de mensagens instantâneas (IM) com o URI SIP.</span><span class="sxs-lookup"><span data-stu-id="87573-135">Displays an instant messaging (IM)-only Conversation window with the SIP URI.</span></span> <span data-ttu-id="87573-136">Aceita vários URIs SIP especificados dentro dos colchetes angulares ( &lt; &gt; ) sem qualquer separador.</span><span class="sxs-lookup"><span data-stu-id="87573-136">Accepts multiple SIP URIs specified inside angle brackets (&lt;&gt;) without any separator.</span></span></p>
<pre><code>im:&lt;sip:user1@host&gt;&lt;sip:user2@host&gt;</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87573-137">A tabela a seguir fornece exemplos desses parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="87573-137">The following table provides examples of these command-line parameters.</span></span>

### <a name="command-line-parameter-examples"></a><span data-ttu-id="87573-138">Exemplos de parâmetros Command-Line</span><span class="sxs-lookup"><span data-stu-id="87573-138">Command-Line Parameter Examples</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87573-139">Instância</span><span class="sxs-lookup"><span data-stu-id="87573-139">Instance</span></span></th>
<th><span data-ttu-id="87573-140">Resultados</span><span class="sxs-lookup"><span data-stu-id="87573-140">Results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87573-141">Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="87573-141">Tel:+14255550101</span></span></p></td>
<td><p><span data-ttu-id="87573-142">Abre um modo de exibição somente telefone com + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="87573-142">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87573-143">Callto: Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="87573-143">Callto:tel:+ 14255550101</span></span></p></td>
<td><p><span data-ttu-id="87573-144">Abre um modo de exibição somente telefone com + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="87573-144">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87573-145">Callto:sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="87573-145">Callto:sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="87573-146">Abre uma exibição somente de telefone com o kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="87573-146">Opens a phone-only view with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87573-147">sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="87573-147">sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="87573-148">Abre uma janela de conversa com o kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="87573-148">Opens a Conversation window with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87573-149">conf: SIP:https://meet.contoso.com/kazuto/7322994</span><span class="sxs-lookup"><span data-stu-id="87573-149">conf:sip:https://meet.contoso.com/kazuto/7322994</span></span></p></td>
<td><p><span data-ttu-id="87573-150">Abre uma janela de conversa e exibe as opções de ingresso no áudio da reunião.</span><span class="sxs-lookup"><span data-stu-id="87573-150">Opens a Conversation window and displays meeting audio join options.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="87573-151">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87573-151">


</div>

<span> </span>

</div>

</div>

</span></span></div>

