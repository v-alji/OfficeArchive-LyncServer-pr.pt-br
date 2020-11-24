---
title: Configurar servidores de aplicativo confiáveis
description: Configurar servidores de aplicativos confiáveis.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure trusted application servers
ms:assetid: 20c3815f-3048-4940-8c0f-cdfcd0801d5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204735(v=OCS.15)
ms:contentKeyID: 48183592
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39f439ea3e5996e0a3464540069024b70c415e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390009"
---
# <a name="configure-trusted-application-servers"></a>Configurar servidores de aplicativo confiáveis

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-11_

Em um ambiente misto, se você criar um novo servidor de aplicativos confiável, deverá definir o próximo pool de saltos como um pool do Lync Server 2013. Em um ambiente misto, o pool herdado do Lync Server 2010 e o pool do Lync Server 2013 aparecem na lista suspensa. Não há suporte para a seleção do pool herdado.

**Selecione o Lync Server 2013 como próximo nó ao criar um servidor de aplicativos confiável**

1.  Abrir o construtor de topologias.

2.  No painel esquerdo, clique com o botão direito do mouse em **servidores de aplicativos confiáveis** e clique em **novo pool de aplicativos confiáveis**.

3.  Digite o **FQDN do pool** do pool de aplicativos confiável e selecione se ele será um único servidor ou vários servidores.

4.  Click **Next**.

5.  Na página **selecionar o próximo salto** , na lista, selecione o pool de front-end do Lync Server 2013.

6.  Clique em **Concluir**.

7.  Selecione o servidor de **Lync** do nó superior e, no menu **ação** , selecione **publicar**.
    
    Verifique se o **pool de aplicativos confiável** foi criado com êxito e associado ao pool de front-end correto.

</div>

<span> </span>

</div>

</div>

</div>

