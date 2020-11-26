---
title: 'Lync Server 2013: Configurar a tabela de órbita de Estacionamento de Chamadas'
description: 'Lync Server 2013: configurar a tabela órbita do parque de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Call Park orbit table
ms:assetid: e5cc0c19-7b2c-48e7-a21d-cfb23c842f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399020(v=OCS.15)
ms:contentKeyID: 48185666
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce9fb35c2958a426888d83d075064c88ddae4bfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433630"
---
# <a name="configure-the-call-park-orbit-table-in-lync-server-2013"></a>Configurar a tabela de órbita de Estacionamento de Chamadas no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-10_

O parque de chamadas usa órbitas para chamadas de estacionamento. Para que os usuários possam estacionar e recuperar chamadas, você deve configurar a tabela órbita do parque de chamadas. Você precisa especificar os intervalos de números de ramal (órbitas) que a sua organização irá reservar para fazer chamadas de estacionamento e definir o roteamento para esses intervalos especificando qual o pool do estacionamento de chamadas manipula cada intervalo. Quando você define intervalos de órbita, a meta é ter órbitas suficientes para que qualquer uma das órbitas não seja reutilizada rapidamente, mas não muitas órbitas que você limite o número de extensões disponíveis para usuários ou outros serviços. Você pode criar várias faixas órbitas do estacionamento de chamada para cada pool do Lync Server onde o aplicativo de estacionamento de chamada é implantado. Cada faixa de opções de estacionamento de chamadas deve ter um nome globalmente exclusivo e um conjunto exclusivo de extensões.

<div>


> [!IMPORTANT]  
> Normalmente, um intervalo de órbitas engloba 100 órbitas ou menos. Cada intervalo pode ser muito maior, contanto que seja menor do que o máximo de 10.000 órbitas por intervalo e tenha menos de 50.000 órbitas por pool. Se o intervalo for muito pequeno, as órbitas serão reutilizadas mais rapidamente.



</div>

Use blocos de extensões virtuais (extensões sem um usuário ou telefone atribuído a elas) para intervalos de órbita.

<div>


> [!NOTE]  
> Não há suporte para a atribuição de números do Direct Inward Dialing (DID) como números órbitas na tabela órbita do estacionamento de chamada.



</div>

<div>

## <a name="in-this-section"></a>Nesta seção

[Criar ou modificar uma faixa de opções do parque de chamadas no Lync Server 2013](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

