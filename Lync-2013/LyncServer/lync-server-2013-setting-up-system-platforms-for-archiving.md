---
title: 'Lync Server 2013: Configurando plataformas do sistema para arquivamento'
description: 'Lync Server 2013: configurar plataformas do sistema para arquivamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up system platforms for Archiving
ms:assetid: 2df40fdf-0e32-46d4-9fb2-1ce1d7bfa328
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204768(v=OCS.15)
ms:contentKeyID: 48183716
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f210083451ae8fcb87c53e52b5512de6f1f18d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441673"
---
# <a name="setting-up-system-platforms-for-archiving-in-lync-server-2013"></a>Configurando plataformas do sistema para arquivamento no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-09_

Antes de iniciar a implantação do arquivamento, você deve instalar o sistema operacional necessário e qualquer outro software de pré-requisito em hardware que atenda aos requisitos do sistema:

  - **Plataforma do Lync Server 2013**   As implantações do Lync Server 2013 não têm servidores de arquivamento. Em vez disso, os agentes de coleta de dados unificados são executados em servidores de front-end e servidores Standard Edition para capturar dados para arquivamento, portanto, não é preciso ter uma plataforma de sistema separada para hospedar o arquivamento.

  - **Plataforma de armazenamento de dados**   No Lync Server 2013, você pode armazenar dados usando um dos seguintes procedimentos:
    
      - **Integração com o Microsoft Exchange**   Se você deseja armazenar dados de arquivamento do Lync Server 2013 usando a implantação do Exchange 2013, em vez de ou além de configurar um banco de dados separado para armazenamento de dados de arquivamento, a implantação do Exchange deve estar executando o Exchange 2013. Para obter detalhes sobre a configuração de plataformas do sistema para o Exchange 2013, consulte a documentação do produto Exchange.
    
      - **SQL Server**   Se você quiser usar um banco de dados separado do SQL Server para armazenamento de dados de arquivamento, em vez de usar a integração do Microsoft Exchange, você deve configurar a plataforma do sistema para o banco de dados antes da implantação do arquivamento. Os requisitos da plataforma do sistema específico dependem se você usa o Microsoft SQL Server 2008 R2 ou o Microsoft SQL Server 2012 para o banco de dados de arquivamento. Para obter detalhes sobre a configuração de plataformas do sistema para esses bancos de dados, consulte a documentação do Microsoft SQL Server 2008 R2 e do Microsoft SQL Server 2012.

  - **Plataforma de servidor de arquivos**   O Lync Server 2013 armazena arquivos de arquivamento do Lync Server no mesmo local que você especifica para armazenamento de arquivos quando você configura seus servidores front-end ou servidores Standard Edition. Você não pode especificar um local separado para arquivar o armazenamento de arquivos, portanto, nenhuma plataforma de sistema separada é necessária para arquivar o armazenamento de arquivos. Se você usa a integração do Microsoft Exchange, o Exchange 2013 os arquivos das comunicações arquivadas do Lync são armazenados nos servidores Exchange 2013 para usuários hospedados nesses servidores Exchange.

</div>

<span> </span>

</div>

</div>

</div>

