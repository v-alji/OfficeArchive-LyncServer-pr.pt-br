---
title: 'Lync Server 2013: Resumo de certificado-Federação de protocolo de presença e mensagens extensível (XMPP)'
description: 'Lync Server 2013: Resumo de certificados – Federação de protocolo de presença e mensagens extensível (XMPP).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: b059a34e-99df-40af-91fe-fe2aa52841f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618374(v=OCS.15)
ms:contentKeyID: 49105661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e2bb593d909c2eec6032dc89c07cc5f5b1a72db
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435296"
---
# <a name="certificate-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="40170-103">Resumo de certificados – Federação de protocolo de presença e mensagens extensíveis (XMPP) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40170-103">Certificate summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40170-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40170-104">

<span> </span></span></span>

<span data-ttu-id="40170-105">_**Tópico da última modificação:** 2012-12-23_</span><span class="sxs-lookup"><span data-stu-id="40170-105">_**Topic Last Modified:** 2012-12-23_</span></span>

<span data-ttu-id="40170-106">Os requisitos de certificado para habilitar e estabelecer comunicações com parceiros de protocolo de presença e mensagens extensível (XMPP) exigem o registro adicional de seus domínios do XMPP.</span><span class="sxs-lookup"><span data-stu-id="40170-106">Certificate requirements for enabling and establishing communications with extensible messaging and presence protocol (XMPP) partners require the additional record of your XMPP domains.</span></span> <span data-ttu-id="40170-107">O registro incluído no certificado como um nome alternativo de assunto (SAN) será o domínio que pode participar de comunicações XMPP.</span><span class="sxs-lookup"><span data-stu-id="40170-107">The record that is included on the certificate as a subject alternative name (SAN) will be the domain that can participate in XMPP communications.</span></span> <span data-ttu-id="40170-108">O domínio pode ser o domínio de nível raiz (por exemplo, contoso.com) se você quiser habilitar o XMPP para o seu domínio inteiro ou pode ser selecionado domínios filho (por exemplo, corp.contoso.com, finance.contoso.com) se você estiver habilitando XMPP para um subconjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="40170-108">The domain can be the root-level domain (for example, contoso.com) if you want to enable XMPP for your entire domain, or can be selected child domains (for example, corp.contoso.com, finance.contoso.com) if you are enabling XMPP for a subset of users.</span></span>

<div>

## <a name="certificate-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="40170-109">Resumo do certificado de mensagens extensíveis e protocolo de presença</span><span class="sxs-lookup"><span data-stu-id="40170-109">Certificate Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40170-110">Componente</span><span class="sxs-lookup"><span data-stu-id="40170-110">Component</span></span></th>
<th><span data-ttu-id="40170-111">Nome do assunto</span><span class="sxs-lookup"><span data-stu-id="40170-111">Subject name</span></span></th>
<th><span data-ttu-id="40170-112">Nomes alternativos de assunto (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="40170-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="40170-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="40170-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40170-114">Atribuir ao serviço Edge para acessar o servidor de borda ou o pool de bordas</span><span class="sxs-lookup"><span data-stu-id="40170-114">Assign to Access Edge service of Edge Server or Edge pool</span></span></p></td>
<td><p><span data-ttu-id="40170-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="40170-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="40170-116">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="40170-116">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="40170-117">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="40170-117">sip.contoso.com</span></span></p>
<p><span data-ttu-id="40170-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="40170-118">sip.fabrikam.com</span></span></p>
<p><span data-ttu-id="40170-119">contoso.com</span><span class="sxs-lookup"><span data-stu-id="40170-119">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="40170-120">As três primeiras entradas de SAN são as entradas de SAN normais para um servidor de perímetro completo.</span><span class="sxs-lookup"><span data-stu-id="40170-120">The first three SAN entries are the normal SAN entries for a full Edge Server.</span></span> <span data-ttu-id="40170-121">O contoso.com é a entrada necessária para federação com o parceiro XMPP no nível do domínio raiz.</span><span class="sxs-lookup"><span data-stu-id="40170-121">The contoso.com is the entry required for federation with the XMPP partner at the root domain level.</span></span> <span data-ttu-id="40170-122">Essa entrada permitirá que o XMPP para todos os domínios com o contoso.com sufixo seja re.</span><span class="sxs-lookup"><span data-stu-id="40170-122">This entry will allow XMPP for all domains with the suffix contoso.com.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="40170-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="40170-123">See Also</span></span>


[<span data-ttu-id="40170-124">Exemplo de configuração de XMPP no Lync Server 2013 – federação XMPP com Google Talk</span><span class="sxs-lookup"><span data-stu-id="40170-124">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="40170-125">Planejar certificados do Servidor de Borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40170-125">Plan for Edge Server certificates in Lync Server 2013</span></span>](lync-server-2013-plan-for-edge-server-certificates.md)  


[<span data-ttu-id="40170-126">Configurar certificados de Borda para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40170-126">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)  
[<span data-ttu-id="40170-127">Solicitação-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="40170-127">Request-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate)  
[<span data-ttu-id="40170-128">Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="40170-128">Set-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  
  

<span data-ttu-id="40170-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40170-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

