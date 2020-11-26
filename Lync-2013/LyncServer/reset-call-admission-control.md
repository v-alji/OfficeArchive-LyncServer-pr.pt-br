---
title: Redefinir controle de admissão de chamada
description: Redefina o controle de admissão de chamadas.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4539cda453de6249be3a9b9b61521ecf478cb70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443619"
---
# <a name="reset-call-admission-control"></a>Redefinir controle de admissão de chamada

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-11_

Se um pool de front-end do Lync Server 2010 estiver hospedando o controle de admissão de chamadas (CAC), você deverá mover o hospedagem do CAC para um pool do Lync Server 2013 para poder remover o pool de front-ends do Lync Server 2010.

<div>

## <a name="to-reset-cac"></a>Para redefinir o CAC

1.  Abrir o construtor de topologias.

2.  Clique com o botão direito do mouse no nó do site e, em seguida, clique em **Editar propriedades**.

3.  Em **configuração de controle de admissão de chamada**, verifique se a opção **habilitar controle de admissão de chamadas** está selecionada.

4.  Em **pool de front-ends para executar o controle de admissão de chamadas (CAC)**, selecione o pool do Lync Server 2013 para hospedar o CAC e, em seguida, clique em **OK**.

5.  Publique a topologia.

</div>

</div>

<span> </span>

</div>

</div>

</div>

