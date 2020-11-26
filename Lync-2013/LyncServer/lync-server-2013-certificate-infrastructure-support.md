---
title: 'Lync Server 2013: Suporte à infraestrutura de certificado'
description: Suporte à infraestrutura de certificado do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure support
ms:assetid: 47aa5c95-eb60-4d4b-81d5-7fdaef1a1145
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425950(v=OCS.15)
ms:contentKeyID: 48184047
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc08719e5b1c58a4dc3c1cab07db5e9842d46d5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435401"
---
# <a name="certificate-infrastructure-support-in-lync-server-2013"></a>Suporte à infraestrutura de certificado no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-11-07_

O Lync Server 2013 requer uma infraestrutura de chave pública (PKI) para dar suporte a conexões de camada de transporte (TLS) e TLS (MTLS) mútua. Por padrão, o Lync Server 2013 está configurado para usar o TLS para conexões de cliente para servidor. O MTLS é usado para conexões entre servidores.

Os certificados MTLS devem ser emitidos por autoridades de certificação (CAs) confiáveis para o Lync Server 2013. O Lync Server dá suporte a certificados emitidos a partir das seguintes autoridades de certificação:

  - Certificados emitidos por uma CA interna:
    
      - A autoridade de certificação do sistema operacional Windows Server 2003
    
      - A autoridade de certificação do sistema operacional Windows Server 2008
    
      - A autoridade de certificação do sistema operacional Windows Server 2008 R2
    
      - A autoridade de certificação do sistema operacional Windows Server 2012
    
      - A autoridade de certificação do sistema operacional Windows Server 2012 R2

  - Certificados emitidos por uma autoridade de certificação pública

A comunicação com outros aplicativos e servidores, como o Exchange 2013, requer um certificado que seja compatível com outros aplicativos e produtos. Para o lançamento do 2013, Lync Server 2013 e outros produtos do Microsoft Server, incluindo Exchange 2013 e SharePoint Server, suporte ao protocolo de autorização aberta (OAuth) para autenticação e autorização do servidor para servidor. Para obter detalhes, consulte [Gerenciando a autenticação de servidor para servidor (OAuth) e aplicativos de parceiros no Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) na documentação de implantação ou na documentação de operações.

Para conexões de clientes que executam o sistema operacional Windows 7, sistema operacional Windows Server 2008 R2 e Microsoft Office Communicator 2007 Phone Edition, Lync Server 2013 inclui suporte para (mas não exigem) certificados assinados usando a função hash criptográfico SHA-256. Para dar suporte ao acesso externo usando SHA-256, o certificado externo é emitido por uma autoridade de certificação pública que usa SHA-256.

Para obter detalhes sobre requisitos de certificado, consulte [requisitos de infraestrutura de certificado para o Lync Server 2013](lync-server-2013-certificate-infrastructure-requirements.md) na documentação de planejamento. Para obter detalhes sobre o uso de caracteres curinga com certificados, consulte [suporte a certificados curinga no Lync Server 2013](lync-server-2013-wildcard-certificate-support.md) na documentação de suporte.

</div>

<span> </span>

</div>

</div>

</div>

