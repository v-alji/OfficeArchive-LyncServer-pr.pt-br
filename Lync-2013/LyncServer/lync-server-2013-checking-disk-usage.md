---
title: 'Lync Server 2013: verificando o uso do disco'
description: 'Lync Server 2013: verificando o uso do disco.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking disk usage
ms:assetid: 0f0cb9bf-3f11-43ff-be10-5c8e1b5c4f08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720908(v=OCS.15)
ms:contentKeyID: 63969578
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7eddde772d156f0a416dab381efe1ab33ee202f9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434988"
---
# <a name="checking-disk-usage-in-lync-server-2013"></a>Verificando o uso do disco no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2014-04-30_

Unidades de discos rígidos são um componente importante da implantação do Lync Server 2013. Sem um volume de disco livre suficiente, nem o sistema operacional nem os bancos de dados do Lync Server 2013 podem funcionar corretamente. Você deve monitorar as estatísticas de banco de dados de back-end do Lync Server 2013 diariamente para ajudar a garantir que os servidores não fiquem sem espaço em disco e para se preparar para adicionar recursos de armazenamento conforme necessário.

Além de verificar o espaço em discos que hospedam o sistema operacional, arquivos de programas, banco de dados e logs de transações (Lync Server 2013 back-end), você também deve monitorar o uso do sistema de arquivos que inclui espaço em disco para os compartilhamentos de arquivos que contêm os dados importantes a seguir:

  - Conteúdo da reunião

  - Metadados de conteúdo da reunião

  - Registros de conformidade para reuniões

  - Arquivos de dados de aplicativo (usados internamente pelo componente de servidor de aplicativos)

  - Serviço Web e pastas de conformidade do servidor de chat em grupo (para armazenar arquivos carregados no serviço Web de chat de grupo)

  - Arquivos XML de conformidade de chat em grupo (que contêm registros de conformidade de chat em grupo)

  - Atualizar arquivos (para o serviço de atualização de dispositivo)

  - Arquivos do catálogo de endereços

O Lync Server 2013 precisa do espaço do disco rígido para armazenar seus bancos de dados e logs de transação, além de arquivos em compartilhamento de arquivos listados anteriormente.

Você deve monitorar o espaço em disco regularmente para ajudar a garantir que a implantação do Lync Server 2013 não seja afetada de forma adversa devido a recursos de armazenamento insuficientes.

Comparar e manter as informações estatísticas sobre o espaço disponível em disco em cada volume do Lync Server 2013 e o crescimento esperado dos arquivos de log de transação e bancos de dados. Isso ajuda a planejar a capacidade e a adicionar armazenamento quando os recursos de armazenamento são necessários.

Para acomodar as situações de solução de problemas e recuperação de desastres, recomendamos que o espaço disponível no volume seja igual ou superior a 110% do tamanho do banco de dados.

Você pode verificar o espaço livre em disco usando os seguintes métodos:

1.  **Gerenciador de operações do System Center**   O System Center Operations Manager pode ser usado para avisar os administradores quando o espaço do volume é restringido.

2.  **Executar um script**   Monitore o espaço em disco executando um script que envia uma mensagem para você se o espaço disponível no disco rígido ficar abaixo de 20%. Você pode encontrar um exemplo de script no Microsoft Script Center no TechNet, examine: [https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard%20disk%20alert\&f%5B0%5D.Value=hard%20disk%20alert\&f%5B0%5D.Type=SearchText\&ac=5](https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard+disk+alert%26f%5b0%5d.value=hard+disk+alert%26f%5b0%5d.type=searchtext%26ac=5)

3.  **Explorador do Windows**   Use o Windows Explorer para verificar o espaço em disco em volumes que armazenam logs e bancos de dados do Lync Server 2013.

</div>

<span> </span>

</div>

</div>

</div>

