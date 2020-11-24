---
title: Alterar as rotas de voz para usar o novo servidor de mediação do Lync Server 2013
description: Altere as rotas de voz para usar o novo servidor de mediação do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change voice routes to use the new Lync Server 2013 Mediation Server
ms:assetid: acd487b3-377c-46bf-9f71-fe6152002664
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205162(v=OCS.15)
ms:contentKeyID: 48185069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef58ba61512b5de31a74b79e554dbb3f94b67d99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389917"
---
# <a name="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server"></a>Alterar as rotas de voz para usar o novo servidor de mediação do Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-28_

Esse procedimento altera as rotas de voz para usar o servidor de mediação do Lync Server 2013, em vez do servidor de mediação do Office Communications Server 2007 R2 herdado.

<div>

## <a name="to-change-the-voice-routes-to-use-the-new-mediation-server"></a>Para alterar as rotas de voz para usar o novo servidor de mediação

1.  Painel de Controle do Lync Server 2013

2.  No painel esquerdo, selecione **Roteamento de voz** e **encaminhar**.

3.  Clique em **novo** para criar uma nova rota de voz.

4.  Preencha os seguintes campos:
    
      - **Nome**: digite um nome descritivo da rota de voz. Para este documento, vamos usar o **W15PSTNRoute**.
    
      - **Descrição**: digite uma breve descrição da rota de voz.

5.  Ignore todas as seções restantes até alcançar os **gateways associados**. Clique em **Adicionar**. Selecione o novo gateway padrão e clique em **OK**.

6.  Em **usos de PSTN associados**, clique em **selecionar**.

7.  Na página **selecionar registro de uso de PSTN** , selecione um nome de registro e clique em **OK**.

8.  Na página **nova rota de voz** , clique em **OK** para criar a **rota de voz**.

9.  Na página **Roteamento de voz** , selecione **roteiro**.

10. Mova a rota recém-criada para a parte superior da lista e selecione **confirmar**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

