---
title: 'Lync Server 2013: Status de replicação do repositório de gerenciamento central'
description: 'Lync Server 2013: status de replicação do repositório de gerenciamento central.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central management store replication status
ms:assetid: f514f88d-986b-4e45-b79b-e04a7616c1fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720926(v=OCS.15)
ms:contentKeyID: 63969663
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f1f9008a966040cf34ac0499c023f9dbe53a541
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435457"
---
# <a name="central-management-store-replication-status-in-lync-server-2013"></a>Status de replicação do repositório de gerenciamento central no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2015-01-26_

Quando um administrador faz uma alteração de algum tipo para o Lync Server (por exemplo, quando um administrador cria uma nova política de voz ou altera as configurações de configuração do servidor do catálogo de endereços), essa alteração é registrada no repositório de gerenciamento central. Em seguida, a alteração deve ser duplicada em todos os computadores que estão executando os serviços ou funções de servidor do Lync Server.

Para replicar dados, o Replicador Mestre (executado no Servidor de Gerenciamento Central) cria um instantâneo dos dados de configuração alterados. Uma cópia desse instantâneo é enviada para cada computador que esteja executando serviços do Lync Server ou funções de servidor. Nesses computadores, um agente de replicação recebe o instantâneo e carrega os dados alterados. Em seguida, o agente envia uma mensagem ao Replicador Mestre informando o status recente da replicação.

O cmdlet Get-CsManagementStoreReplicationStatus permite que você verifique o status de replicação de qualquer (ou todos) dos computadores do Lync Server em sua organização.

Quem pode executar este cmdlet? Por padrão, os membros destes grupos estão autorizados a executar o cmdlet Get-CsManagementStoreReplicationStatus localmente: RTCUniversalUserAdmins, RTCUniversalServerAdmins.

Para retornar uma lista de todas as funções RBAC às quais esse cmdlet foi atribuído (incluindo qualquer função RBAC personalizada que você tenha criado), execute o seguinte comando no prompt do Windows PowerShell:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsManagementStoreReplicationStatus"}

<div>

## <a name="see-also"></a>Confira também


[Get-CsManagementStoreReplicationStatus](https://docs.microsoft.com/powershell/module/skype/Get-CsManagementStoreReplicationStatus)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

