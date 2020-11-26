---
title: Remover um pool Front-End ou um servidor Standard Edition
description: Remova o pool de front-end ou o servidor Standard Edition.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440273"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a>Remover um pool Front-End ou um servidor Standard Edition

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-04_

Este tópico fornece orientações sobre o processo de remoção de um pool de front-end ou um servidor front-end Standard Edition. Quando você remove um pool de front-end, Remove cada servidor front-end que pertence ao pool como parte do processo de remoção de pool. Quando você remove um servidor front-end padrão da edição, deve remover a definição do SQL Store do construtor de topologias.

<div>

## <a name="to-remove-a-front-end-server-pool"></a>Para remover um pool de servidores front-end

1.  Abrir o construtor de topologias.

2.  Navegue até o nó do Lync Server 2010.

3.  Expanda **pools de front-end do Enterprise Edition**, expanda o pool de front-ends, clique com o botão direito do mouse no pool de front-ends que você deseja remover e clique em **excluir**.

4.  Publique a topologia, verifique o status da replicação e execute o assistente de implantação do Lync Server conforme necessário.

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a>Para remover um servidor front-end padrão da edição

1.  Abrir o construtor de topologias.

2.  Navegue até o nó do Lync Server 2010.

3.  Expanda **servidores front-end padrão da edição**, clique com o botão direito do mouse no servidor front-end que você deseja remover e, em seguida, clique em **excluir**.

4.  Expanda **repositórios SQL**, clique com o botão direito do mouse no banco de dados do SQL Server associado ao servidor front-end Standard Edition e clique em **excluir**.
    
    <div>
    

    > [!IMPORTANT]  
    > Você deve remover a definição dos bancos de dados do SQL Server posicionado do servidor front-end da Standard Edition.

    
    </div>

5.  Publique a topologia, verifique o status da replicação e execute o assistente de implantação do Lync Server conforme necessário.

</div>

</div>

<span> </span>

</div>

</div>

</div>

