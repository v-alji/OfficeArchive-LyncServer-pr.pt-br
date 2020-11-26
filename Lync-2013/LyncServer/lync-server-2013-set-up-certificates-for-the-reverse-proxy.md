---
title: 'Lync Server 2013: Configurar certificados para o proxy reverso'
description: 'Lync Server 2013: configurar certificados para o proxy reverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the reverse proxy
ms:assetid: c03a08ec-a67b-4f11-b0d7-6677461beaaa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412938(v=OCS.15)
ms:contentKeyID: 48185291
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4b84241775bb3594840b68551048c01ff5faba2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441743"
---
# <a name="set-up-certificates-for-the-reverse-proxy-in-lync-server-2013"></a>Configurar certificados para o proxy reverso no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-08_

Cada servidor proxy reverso exige um certificado de servidor Web para ser usado pelo serviço de escuta. O certificado do servidor Web deve ser emitido por uma autoridade de certificação pública (CA).

Para obter detalhes sobre esse e outros requisitos de certificado, consulte [requisitos de certificado para acesso de usuários externos no Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).

<div>

## <a name="to-set-up-a-web-services-certificate-for-the-reverse-proxy"></a>Para configurar um certificado de serviços Web para o proxy reverso

  - Você já deve ter configurado seu proxy reverso, incluindo a configuração do certificado de serviços Web. Se você não fez isso antes de iniciar a implantação de seus servidores de borda, use os procedimentos [para configurar servidores proxy inversos para o Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) para criar uma solicitação e instalar o certificado de serviços Web e, em seguida, criar cada regra de publicação da Web e configurá-la para usar o certificado.

</div>

</div>

<span> </span>

</div>

</div>

</div>

