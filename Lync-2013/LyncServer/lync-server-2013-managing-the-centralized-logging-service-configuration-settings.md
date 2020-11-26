---
title: Gerenciar as configurações centralizadas de configuração do serviço de log
description: Gerenciar as configurações centralizadas de configuração do serviço de log.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Centralized Logging Service configuration settings
ms:assetid: f455c3aa-0061-413d-bdfb-a3e78f82723d
ms:mtpsurl: https://technet.microsoft.com/library/JJ721938(v=OCS.15)
ms:contentKeyID: 49733875
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e25294e096b8368aa06a11e4ad851fe5d1a84c0f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425896"
---
# <a name="managing-the-centralized-logging-service-configuration-settings-in-lync-server-2013"></a>Gerenciar as configurações centralizadas de configuração do serviço de log no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-11-01_

O serviço de log centralizado é controlado e configurado por configurações e parâmetros que são criados e usados pelo CLSController (Logging Logging Service Controller) para enviar comandos ao agente de serviço de log centralizado do computador individual (CLSAgent). O agente processa os comandos que são enviados a ele e (no caso de um comando Start) usa a configuração dos cenários, provedores, tamanho do log, duração do rastreamento e sinalizadores para começar a coletar logs de rastreamento de acordo com as informações de configuração fornecidas.

<div>


> [!IMPORTANT]
> Nem todos os cmdlets do Windows PowerShell listados para o serviço de log centralizado são destinados ao uso com implantações locais do Lync Server 2013. Embora possam parecer funcionar, os seguintes cmdlets não foram projetados para funcionar com implantações locais do Lync Server 2013: 
> <UL>
> <LI>
> <P><STRONG>Cmdlets CsClsRegion:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">set-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-CsClsRegion</A>e <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">Remove-CsClsRegion</A>.</P>
> <LI>
> <P><STRONG>Cmdlets CsClsSearchTerm:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">Get-CsClsSearchTerm</A> e <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">set-CsClsSearchTerm</A>.</P>
> <LI>
> <P><STRONG>Cmdlets CsClsSecurityGroup:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">Get-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">set-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>e <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">Remove-CsClsSecurityGroup</A>.</P></LI></UL>As configurações definidas nesses cmdlets não impedirão nem causarão qualquer comportamento adverso, mas serão projetadas para uso com o Microsoft 365 e não produzirão os resultados esperados em implantações locais. Isso não quer dizer que não há uso para esses cmdlets em implantações locais, mas sua utilização é um tópico mais avançado, que não é abordado nesta documentação.


</div>

<div>

## <a name="in-this-section"></a>Nesta seção

Os tópicos desta seção definem as opções de configuração, parâmetros e configurações para o serviço de log centralizado. Informações sobre como configurar o serviço de log centralizado, como recuperar as definições de configuração, a criação de cenários, o gerenciamento de grupos de segurança para o serviço de log centralizado, a pesquisa e outros recursos estão contidos nos tópicos a seguir.

  - [Gerenciando o computador, o site e a configuração de serviço de log centralizado global no Lync Server 2013](lync-server-2013-managing-computer-site-and-global-centralized-logging-service-configuration.md)

  - [Configurando provedores para o serviço de log centralizado no Lync Server 2013](lync-server-2013-configuring-providers-for-centralized-logging-service.md)

  - [Configurar cenários para o serviço de log centralizado no Lync Server 2013](lync-server-2013-configuring-scenarios-for-the-centralized-logging-service.md)

</div>

<div>

## <a name="see-also"></a>Confira também


[Visão geral do serviço de log centralizado no Lync Server 2013](lync-server-2013-overview-of-the-centralized-logging-service.md)  
[Cmdlets de log centralizado no Lync Server 2013](lync-server-2013-centralized-logging-cmdlets.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

