---
title: 'Lync Server 2013: troncos SIP do site de filial'
description: 'Lync Server 2013: troncos SIP do site de ramificação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Branch site SIP trunking
ms:assetid: c4d9dfcd-8baa-41ea-9677-48b0e429429d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412974(v=OCS.15)
ms:contentKeyID: 48185350
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33e408a462c21ffa6df6e6a2aee50d7b87dca1f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435940"
---
# <a name="branch-site-sip-trunking-in-lync-server-2013"></a>Branch site SIP trunking in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-21_

Em alguns casos, talvez seja necessário implementar o entroncamento SIP distribuído em sites de filiais selecionados. Para determinar se um tronco SIP é necessário para um site de filial, examine as informações em [como implementar o entroncamento SIP no Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).

Para obter detalhes sobre as opções de topologia com suporte para a implantação de troncos SIP em sites de filiais, consulte [soluções de resiliência de site de ramificação no Lync Server 2013](lync-server-2013-branch-site-resiliency-solutions.md).

<div>

## <a name="example-branch-site-sip-trunk-requirements-analysis"></a>Análise de requisitos do tronco SIP do exemplo de local de filial

Ao decidir implantar um tronco SIP de site de filial, você precisa executar uma análise de custo específica do site. Por exemplo, uma empresa que tem um site central em Redmond, Washington e um site de filiais em Nova York, deve fazer uma análise para determinar se deve implementar um tronco SIP do site de Nova York para um provedor de serviços local.

Para determinar se um tronco SIP distribuído em Nova Iorque é uma opção com bom custo benefício, identifique quais números DID usarão o tronco SIP e analise o número de chamadas feitas de Nova Iorque para áreas diferentes de Redmond (425). Você pode ter cancelamento para o site de filial no site central. Por exemplo, o site central Redmond pode hospedar números para o site da filial de Nova York. Se o custo da implementação de um tronco SIP distribuído for menor que o custo dessas chamadas, considere a implementação de um tronco SIP no site da filial de Nova York.

</div>

<div>

## <a name="other-branch-site-sip-trunk-requirements"></a>Outros requisitos de tronco SIP do local de filial

A opção entre uma implantação de um tronco SIP em vez de um gateway tem base na diferença entre as cobranças de PSTN de longa distância de cada opção. Se você implantar um tronco SIP de site de filial, também precisará determinar os requisitos de resiliência e largura de banda. Se o link entre o site de sua filial e o site central for resistente e tiver largura de banda suficiente, você poderá implantar um tronco SIP ou um gateway. Você não precisa implantar um aparelho de ramificação sobreviventes no site da filial. Se o link entre seu site de filial e o site central não for resistente, implante um aparelho de ramificação sobreviventes ou implante um servidor de ramificação sobreviventes com um tronco de gateway ou SIP no site da filial.

</div>

</div>

<span> </span>

</div>

</div>

</div>

