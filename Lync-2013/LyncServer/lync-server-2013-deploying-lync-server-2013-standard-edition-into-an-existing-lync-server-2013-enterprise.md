---
title: 'Lync Server 2013: Implantando o Lync Server 2013 Standard Edition em um Lync Server 2013 Enterprise existente'
description: 'Lync Server 2013: implantação do Lync Server 2013 Standard Edition em um Lync Server 2013 Enterprise existente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise
ms:assetid: 05ea128d-6c94-49b3-b28b-477367196425
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398112(v=OCS.15)
ms:contentKeyID: 48183297
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b233d4e782e716904fca0a2a146b2459e906aa57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429948"
---
# <a name="deploying-lync-server-2013-standard-edition-into-an-existing-lync-server-2013-enterprise"></a>Implantando o Lync Server 2013 Standard Edition em um Lync Server 2013 Enterprise existente

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-01_

A implantação de um servidor Standard Edition em uma implantação existente do Enterprise Edition é semelhante à implantação de funções de servidor adicionais. Um servidor padrão da edição pode ser implantado em outro site, permitindo que os usuários nesse site sejam hospedados no servidor do Standard Edition, em vez do pool de front-end em uma rede de longa distância (WAN). Os procedimentos para instalar o novo site e os servidores nesse site já estão definidos em outras seções da documentação sobre a [implantação do Lync Server 2013](lync-server-2013-deploying-lync-server.md) .

<div id="sectionSection0" class="section">

**Para definir um novo site**

1.  Iniciar o construtor de topologias: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Construtor de topologias do Lync Server**.

2.  Na árvore de console, clique com o botão direito do mouse no **Lync Server 2013** e, em seguida, clique em **novo site central**.

3.  Na página **identificar o site** , forneça um nome para o site e, opcionalmente, insira uma descrição.

4.  Siga os procedimentos para definir o restante da topologia do site. Para obter detalhes, consulte [definindo e configurando a topologia no Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).

5.  Publicar a topologia atualizada. Para obter detalhes, consulte [publicar a topologia no Lync Server 2013](lync-server-2013-publish-the-topology.md).

6.  Configurar e instalar um servidor Standard Edition.
    
    <div>
    

    > [!Caution]  
    > Se você implantou um ambiente com apenas um servidor Standard Edition, você começou a usar o processo de instalação do assistente de implantação do Lync Server usando o link <STRONG>preparar primeiro padrão do servidor</STRONG> para instalar os arquivos de banco de dados iniciais para o novo servidor Standard Edition. <STRONG>Não siga esse</STRONG> processo ao instalar um servidor Standard Edition em uma implantação existente do Lync Server 2013.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

