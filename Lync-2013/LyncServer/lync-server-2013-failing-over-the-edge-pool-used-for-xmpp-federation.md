---
title: 'Lync Server 2013: Failover do pool de Borda usado para federação de XMPP'
description: 'Lync Server 2013: falha sobre o pool de bordas usado para Federação do XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for XMPP federation
ms:assetid: 587e7829-a26b-46f8-8aad-b78a7b325b55
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688065(v=OCS.15)
ms:contentKeyID: 49733659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccdfe119258b4d09ddedefb22d0272d72003bf04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428248"
---
# <a name="failing-over-the-edge-pool-used-for-xmpp-federation-in-lync-server-2013"></a>Failover do pool de Borda usado para federação de XMPP no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-19_

Em sua organização, há um pool de bordas designado como o pool a ser usado para a Federação do XMPP. Se esse pool ficar inativo, você deve fazer failover da Federação do XMPP para usar um pool de bordas diferente antes que o XMPP federado possa funcionar novamente.

Ao instalar primeiro os pools de borda e habilitar a Federação do XMPP, você pode simplificar o processo de recuperação de desastres Configurando os registros SRV DNS externos para todos os seus pools de bordas para a Federação do XMPP, em vez de apenas um. Cada um desses registros SRV deve ter um conjunto de prioridades diferente. Todo o tráfego de Federação do XMPP passa pelo pool com o registro SRV com a prioridade mais alta. Para obter mais informações sobre como habilitar e configurar a Federação do XMPP, consulte [Configurando a Federação do XMPP no Lync Server 2013](lync-server-2013-setting-up-xmpp-federation.md).

No procedimento a seguir, EdgePool1 é o pool que hospeda originalmente a Federação do XMPP, e EdgePool2 é o pool que agora hospeda XMPP Federação.

<div>

## <a name="failing-over-the-edge-pool-used-for-xmpp-federation"></a>Falha sobre o pool de bordas usado para a Federação do XMPP

1.  Se você ainda não tiver outro pool de bordas implantado (além do que está indisponível no momento), implante esse pool. Para obter detalhes, consulte [implantando o acesso de usuários externos no Lync Server 2013](lync-server-2013-deploying-external-user-access.md).

2.  Em cada servidor de borda no novo pool de bordas que agora hospeda a Federação do XMPP (EdgePool2), execute o seguinte cmdlet:
    
        Stop-CsWindowsService

3.  Execute o cmdlet a seguir para redirecionar a rota de Federação do XMPP para EdgePool2:
    
        Set-CsSite Site2 -XmppExternalFederationRoute EdgeServer2.contoso.com
    
    Neste exemplo, site2 é o site que contém o pool de borda que agora hospeda a rota de Federação do XMPP, e EdgeServer2.contoso.com é o FQDN de um servidor de borda nesse pool.

4.  No servidor DNS externo, altere o registro DNS a para a Federação XMPP para apontar para EdgeServer2.contoso.com.

5.  Se você ainda não tiver um registro SRV DNS para a Federação do XMPP, que é resolvido para o pool de borda que agora hospedará a Federação do XMPP, você deve adicioná-lo, como no exemplo a seguir. Esse registro SRV deve ter um valor de porta 5269.
    
        _xmpp-server._tcp.contoso.com

6.  Verifique se o pool de bordas que agora hospeda a Federação do XMPP tem a porta 5269 aberta externamente.

7.  Inicie os serviços em todos os servidores de borda do pool de borda que agora hospedarão a Federação do XMPP:
    
        Start-CsWindowsService

</div>

</div>

<span> </span>

</div>

</div>

</div>

