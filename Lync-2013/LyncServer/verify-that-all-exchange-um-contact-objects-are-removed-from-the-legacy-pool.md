---
title: Verificar se todos os objetos de contato do Exchange UM são removidos do pool herdado
description: Verifique se todos os objetos de contato de UM do Exchange foram removidos do pool herdado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440133"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a>Verificar se todos os objetos de contato do Exchange UM são removidos do pool herdado

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-26_

Use a ferramenta **OCSUmUtil** ou o cmdlet **Get-CsExumContact** para verificar se objetos de contato do Exchange um foram removidos do pool herdado do Office Communications Server 2007 R2. O **OCSUmUtil** está localizado na seguinte pasta:

% Arquivos de programas% \\ Arquivos comuns \\ Lync Server 2013 \\ suporte \\OcsUMUtil.exe

O **OCSUmUtil** deve ser executado a partir de uma conta de usuário que tenha:

  - Associação no grupo RTCUniversalServerAdmins e RTCUniversalUserAdmins (que inclui direitos para ler as configurações de mensagens unificadas do Exchange Server)

  - Direitos de domínio para criar objetos de contato no contêiner de unidade organizacional (UO) especificado

Para obter detalhes sobre como usar o cmdlet **Get-CsExumContact** , consulte [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) na documentação do Shell de gerenciamento do Lync Server.

</div>

<span> </span>

</div>

</div>

</div>

