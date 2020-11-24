---
title: Conectar pool piloto aos Servidores de Borda herdados
description: Conecte o pool piloto a servidores de borda herdados.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect pilot pool to legacy Edge Servers
ms:assetid: c3b67220-5705-47f6-852e-415204f3626c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721875(v=OCS.15)
ms:contentKeyID: 49733808
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ede2256efabf561be6b3f99543437087cb5c3890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389999"
---
# <a name="connect-pilot-pool-to-legacy-edge-servers"></a>Conectar pool piloto aos Servidores de Borda herdados

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-29_

Após implantar o Lync Server 2013, você precisa configurar uma rota de Federação para seu site. Para usar a rota federada que está sendo usada pelo Lync Server 2010, o Lync Server 2013 deve ser configurado para usar essa rota.

Para habilitar o site do Lync Server 2013 para usar o diretor e o servidor de borda da implantação do Lync Server 2010, use o construtor de topologias para associar o pool de bordas herdado.

<div>

## <a name="to-associate-the-legacy-edge-pool-by-using-topology-builder"></a>Para associar o pool de bordas herdado usando o construtor de topologias

1.  Abrir o **Construtor de topologias**.

2.  Selecione seu site, que está diretamente abaixo do nó do **Lync Server** .

3.  No menu **ações** , clique em **Editar propriedades**.

4.  No painel esquerdo, selecione **roteiro de Federação**.

5.  Em **atribuição de rota de Federação do site**, selecione **habilitar Federação SIP** e, em seguida, selecione o diretor do Lync Server 2010 ou o servidor de borda do Lync Server 2010, se nenhum diretor estiver listado.
    
    ![Editar propriedades, página de roteiro de Federação](images/JJ721875.5f1d04c3-c724-426d-b27d-3fe89c6c5cfb(OCS.15).jpg "Editar propriedades, página de roteiro de Federação")  

6.  Clique em **OK** para fechar a página **Editar propriedades** .

7.  No construtor de topologias, no nó do Lync Server 2013, navegue até os pools do **servidor Standard Edition** ou do **front-end da edição Enterprise**, clique com o botão direito do mouse no pool e, em seguida, clique em **Editar propriedades**.

8.  Em **associações**, marque a caixa de seleção ao lado de **associar o pool de bordas (para componentes de mídia)**.

9.  Na lista, selecione o servidor de borda herdado.
    
    ![Caixa de diálogo Editar propriedades, selecionando a borda herdada](images/JJ721875.feae8156-540e-4804-bb0a-2b5736ec2900(OCS.15).jpg "Caixa de diálogo Editar propriedades, selecionando a borda herdada")  

10. Clique em **OK** para fechar a página **Editar propriedades** .

11. No **Construtor de topologias**, selecione o nó mais alto, **Lync Server**.

12. No menu **ação** , clique em **publicar topologia** e, em seguida, clique em **Avançar**.

13. Quando o **Assistente de publicação** for concluído, clique em **concluir**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

