---
title: 'Lync Server 2013: Configurar Entrada Automática de Cliente para usar o Diretor'
description: 'Lync Server 2013: configurar o Sign-In de cliente automático para usar o diretor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Automatic Client Sign-In to use the Director
ms:assetid: 85369ffc-53ae-43be-8a23-84a094faecff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398678(v=OCS.15)
ms:contentKeyID: 48184703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9c45a1a677d3a30704d8dca1771ef865cef29ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390262"
---
# <a name="configure-automatic-client-sign-in-to-use-the-director-in-lync-server-2013"></a>Configurar Entrada Automática de Cliente para usar o Diretor no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-08_

Ao implantar um aplicativo do Lync Server 2013, diretor ou um pool de diretores, recomendamos que você use o cliente automático Sign-In como prática recomendada. Para obter detalhes sobre como configurar servidores DNS para a entrada automática do cliente, confira [requisitos de DNS para entrada automática do cliente no Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) na documentação de planejamento.

Se você já tiver implantado a entrada automática do cliente, consulte as seções a seguir para configurá-lo em seu (s) director (es).

<div>

## <a name="single-director-instance"></a>Instância do diretor único

Se você já tiver o cliente automático Sign-In implantado e ele estiver apontando para um servidor front-end ou um pool de front-end, será necessário alterar o registro SRV DNS para apontar para o diretor.

</div>

<div>

## <a name="director-pool"></a>Pool de diretor

Se você já tiver o cliente automático Sign-In implantado e ele estiver apontando para um servidor front-end ou um pool de front-end, será necessário alterar o registro SRV DNS para apontar para o pool diretor.

</div>

</div>

<span> </span>

</div>

</div>

</div>

