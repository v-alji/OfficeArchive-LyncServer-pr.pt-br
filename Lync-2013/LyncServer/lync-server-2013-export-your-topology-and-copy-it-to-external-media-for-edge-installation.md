---
title: Exportar sua topologia e copiá-la na mídia externa para instalação de borda
description: Exporte a topologia e copie-a para mídia externa para instalação do Edge.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export your topology and copy it to external media for edge installation
ms:assetid: def9f416-c519-4a72-b242-7d3057d9c1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398983(v=OCS.15)
ms:contentKeyID: 48185615
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47fcee032b4c0e667455ae7f35afe8b99c2d12cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389683"
---
# <a name="export-your-lync-server-2013-topology-and-copy-it-to-external-media-for-edge-installation"></a>Exportar sua topologia do Lync Server 2013 e copiá-la na mídia externa para instalação de borda

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-08_

Depois de publicar sua topologia, o assistente de implantação do Lync Server precisa acessar os dados do repositório de gerenciamento central para iniciar o processo de implantação no servidor. Na rede interna, os dados estão disponíveis diretamente nos servidores, mas os servidores de borda que não estão no domínio interno não podem acessar os dados. Para disponibilizar os dados de configuração de topologia para uma implantação de servidor de borda, você deve exportar os dados de topologia para um arquivo e copiá-los para mídia externa (por exemplo, uma unidade USB ou um compartilhamento de rede que esteja disponível no servidor de borda) antes de executar o assistente de implantação do Lync Server no servidor de borda. Use o procedimento a seguir para disponibilizar os dados de configuração de topologia no servidor de borda que você está implantando.

<div>


> [!NOTE]
> Depois de instalar o Lync Server 2013 em um servidor de borda, você gerencia o servidor de borda usando as ferramentas administrativas da rede interna, que replica automaticamente a configuração para qualquer servidor de borda na sua implantação. A única exceção é atribuir e instalar certificados e interromper e iniciar serviços, ambos devem ser feitos no servidor de borda.



</div>

<div>

## <a name="to-make-your-topology-data-available-on-an-edge-server-by-using-lync-server-management-shell"></a>Para disponibilizar os dados de topologia em um servidor de borda usando o Shell de gerenciamento do Lync Server

1.  Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.

2.  No Shell de gerenciamento do Lync Server, execute o seguinte cmdlet:
    
        Export-CsConfiguration -FileName <ConfigurationFilePath.zip>

3.  Copie o arquivo exportado para mídia externa (por exemplo, uma unidade USB ou um compartilhamento de rede que esteja disponível no servidor de borda durante a implantação).

</div>

</div>

<span> </span>

</div>

</div>

</div>

