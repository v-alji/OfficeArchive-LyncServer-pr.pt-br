---
title: 'Lync Server 2013: Requisitos de infraestrutura do Active Directory'
description: 'Lync Server 2013: requisitos de infraestrutura do Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory infrastructure requirements
ms:assetid: c2086f7b-662f-4179-ab99-2c0311ebd903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412955(v=OCS.15)
ms:contentKeyID: 48185318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62218605c9b3fac20743d0b6bb475515c9498f9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439412"
---
# <a name="active-directory-infrastructure-requirements-for-lync-server-2013"></a>Requisitos de infraestrutura do Active Directory para Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-11-07_

Antes de iniciar o processo de preparação dos serviços de domínio Active Directory para o Lync Server 2013, certifique-se de que a sua infraestrutura do Active Directory atenda aos seguintes pré-requisitos:

  - Todos os controladores de domínio (que incluem todos os servidores de catálogo global) na floresta em que você implanta o Lync Server executam um dos seguintes sistemas operacionais:
    
      - Sistema operacional Windows Server 2012 R2
    
      - Sistema operacional Windows Server 2012
    
      - Sistema operacional Windows Server 2008 R2
    
      - Sistema operacional Windows Server 2008
    
      - Windows Server 2008 Enterprise 32-bit
    
      - versões de 32 bits ou 64 bits do sistema operacional Windows Server 2003 R2
    
      - versões de 32 bits ou 64 bits do sistema operacional Windows Server 2003

  - Todos os domínios nos quais você implanta o Lync Server são gerados para um nível funcional de domínio do Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 ou pelo menos Windows Server 2003.

  - A floresta na qual você implanta o Lync Server é gerada para um nível funcional da floresta do Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 ou pelo menos Windows Server 2003.
    
    <div>
    

    > [!NOTE]  
    > Para alterar o nível funcional do domínio ou da floresta, consulte "elevando os níveis funcionais do domínio e da floresta" na biblioteca do TechNet em <A href="https://go.microsoft.com/fwlink/p/?linkid=263775">https://go.microsoft.com/fwlink/p/?LinkId=263775</A> .

    
    </div>

  - Um catálogo global é implantado em cada domínio onde você implanta usuários ou computadores do Lync Server.

O Lync Server 2013 dá suporte a grupos universais nos sistemas operacionais Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 e Windows Server 2003. Os membros dos grupos universais podem incluir outros grupos e contas de qualquer domínio na árvore ou floresta de domínio e podem receber permissões em qualquer domínio na árvore ou floresta de domínio. O suporte a grupos universais, combinado com delegação de administrador, simplifica o gerenciamento de uma implantação do Lync Server. Por exemplo, não é necessário adicionar um domínio a outro para permitir que um administrador os gerencie.

</div>

<span> </span>

</div>

</div>

</div>

