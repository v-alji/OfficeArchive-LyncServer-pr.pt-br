---
title: 'Lync Server 2013: Suporte à infraestrutura de DNS'
description: 'Lync Server 2013: suporte à infraestrutura de DNS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Domain Name System (DNS) infrastructure support
ms:assetid: 37777c16-94ce-436d-b517-bcf53a564513
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425850(v=OCS.15)
ms:contentKeyID: 48183878
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea65907eba13367fd92e546d62994d10907bf89
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429074"
---
# <a name="dns-infrastructure-support-in-lync-server-2013"></a>Suporte à infraestrutura de DNS no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-03-08_

O Lync Server 2013 requer o sistema de nomes de domínio (DNS) e o usa das seguintes maneiras:

  - Para descobrir servidores internos ou pools para comunicações entre servidores.

  - Para permitir que os clientes descubram o pool de front-end ou o servidor Standard Edition usado para várias transações SIP.

  - Associar as URLs simples para conferências com os servidores que hospedam essas conferências.

  - Para permitir que servidores e clientes externos se conectem a servidores de borda ou ao proxy reverso HTTP para mensagens instantâneas (IM) ou conferência.

  - Para habilitar dispositivos de comunicação unificada (UC) que não estão conectados para descobrir o pool de front-end ou o servidor Standard Edition executando o serviço Web de atualização de dispositivos, obtenha atualizações e envie logs.

  - Para permitir que os clientes móveis descubram automaticamente os recursos de serviços Web sem exigir que os usuários insiram manualmente URLs nas configurações do dispositivo.

  - Para o balanceamento de carga de DNS.

<div>


> [!NOTE]  
> O Lync Server 2013 não é compatível com nomes de domínio internacionalizados (IDNs).



</div>

<div>


> [!IMPORTANT]  
> O nome especificado deve ser idêntico ao nome do computador configurado no servidor. Por padrão, o nome do computador de um computador que não tiver ingressado em um domínio deverá ser um nome curto, não um nome de domínio totalmente qualificado (FQDN). O Construtor de Topologias usa FQDNs, não nomes curtos. Portanto, você deverá configurar um sufixo DNS no nome do computador a ser implantado no Servidor de Borda que não ingressou no domínio. <STRONG>Use apenas caracteres padrão</STRONG> (incluindo A–Z, a–z, 0–9 e hifens) ao atribuir FQDNs de seus Lync Servers, Servidores de Borda e pools. Não use caracteres Unicode ou sublinhados. Normalmente, caracteres não padrão no FQDN não são suportados por DNS externo e CAs públicas (ou seja, quando o FQDN deve ser atribuído ao SN no certificado).



</div>

</div>

<span> </span>

</div>

</div>

</div>

