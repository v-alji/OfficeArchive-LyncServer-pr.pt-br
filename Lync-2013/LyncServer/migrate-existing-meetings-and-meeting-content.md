---
title: Migrar reuniões existentes e conteúdo de reunião
description: Migrar reuniões existentes e o conteúdo da reunião.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443801"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a>Migrar reuniões existentes e conteúdo de reunião

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-22_

Quando uma conta de usuário é movida do Lync Server 2010 para um servidor do Lync Server 2013, as seguintes informações são movidas com essa conta de usuário:

  - **Reuniões já programadas pelo usuário**. Isso inclui a movimentação dos diretórios de conferências e dos dados de conferência.

  - **PIN (número de identificação pessoal) do usuário**. O PIN atual do usuário continua a funcionar até que ele expire ou que o usuário solicitou um novo PIN.

As seguintes informações da conta de usuário não se movem para o novo servidor.

  - **Conteúdo da reunião**. Para mover o conteúdo compartilhado durante uma reunião, por exemplo, PowerPoint, quadro de comunicações, anexos ou dados de votação, use o parâmetro **-MoveConferenceData** como parte do cmdlet **move-CsUser** .

</div>

<span> </span>

</div>

</div>

</div>

