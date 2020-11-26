---
title: 'Lync Server 2013: Configurando o suporte para descoberta automática'
description: 'Lync Server 2013: Configurando o suporte para descoberta automática.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Autodiscover
ms:assetid: 3a266456-69a0-4539-ba99-d388b83799a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945622(v=OCS.15)
ms:contentKeyID: 51541463
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23991f2f9467035f4ba461ff1b6a84fa8ed1a11d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432608"
---
# <a name="configuring-support-for-autodiscover-in-lync-server-2013"></a>Configurando o suporte para descoberta automática no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-01-21_

O **serviço de descoberta automática** de serviços Web do Lync Server apareceu pela primeira vez na atualização cumulativa do lync Server 2010: de novembro de 2011. Esta atualização foi acompanhada pela versão inicial dos clientes móveis do Lync. O serviço de descoberta automática expôs os serviços de mobilidade, conhecidos como o serviço MCX.

O serviço de descoberta automática age como um local único para que todos os clientes solicitem informações sobre quais serviços e recursos estão disponíveis, e como entrar em contato com o sevices – seja por um nome de domínio totalmente qualificado ou uma referência do localizador de recursos uniforme da Web. A descoberta automática expõe diversos recursos, e cada cliente fará solicitações com base nos recursos que o cliente pode usar. Por exemplo, um cliente do Lync da área de trabalho do 2013 usará o autodiscvoer para determinar os serviços Web externos, mas não usará os serviços de mobilidade (MCX). Para definir e habilitar corretamente seus clientes para usar os recursos disponíveis para eles, os cenários que permitem que um cliente encontre e use entradas de descoberta automática devem ser definidos. Para usar o autodoscover, sua implantação requer que um proxy reverso publique os serviços Web do Lync Server, que os registros DNS são configurados para resolver consultas DNS para o serviço de descoberta automática do Lync Server e serviços Web do Lync Server e se os serviços de certificado estão configurados corretamente para o seu cenário específico.

<div>


> [!TIP]  
> Para obter detalhes técnicos sobre o que os elementos da solicitação/resposta do autodiscover fazem, consulte <A href="lync-server-2013-understanding-autodiscover.md">compreendendo a descoberta automática no Lync Server 2013</A>.



</div>

As seguintes informações e tabelas definem, por cenário, quais configurações (se houver) que você precisa implementar para fornecer o uso completo e efetivo do serviço de descoberta automática. As informações nos tópicos a seguir são específicas do Microsoft Lync Server 2013. Se você estiver procurando orientação sobre como planejar a mobilidade do Lync Server 2010, consulte [https://go.microsoft.com/fwlink/?LinkId=275113](https://go.microsoft.com/fwlink/?linkid=275113) . Para implantar o Mobility para o Lync Server 2010, consulte [https://go.microsoft.com/fwlink/?LinkId=275114](https://go.microsoft.com/fwlink/?linkid=275114)

<div>

## <a name="in-this-section"></a>Nesta seção

  - [Configurando o DNS para descoberta automática no Lync Server 2013](lync-server-2013-configuring-dns-for-autodiscover.md)

  - [Configurando certificados para descoberta automática no Lync Server 2013](lync-server-2013-configuring-certificates-for-autodiscover.md)

  - [Configurando um proxy inverso para descoberta automática no Lync Server 2013](lync-server-2013-configuring-a-reverse-proxy-for-autodiscover.md)

  - [Configurando a descoberta automática no Lync Server 2013 para implantações híbridas](lync-server-2013-configuring-autodiscover-for-hybrid-deployments.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

