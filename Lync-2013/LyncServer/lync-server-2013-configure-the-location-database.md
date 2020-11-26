---
title: 'Lync Server 2013: configurar o banco de dados de localização'
description: 'Lync Server 2013: configurar o banco de dados de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the location database
ms:assetid: 8544be31-6958-47ef-b926-fdc80d56191c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398679(v=OCS.15)
ms:contentKeyID: 48184704
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 877c83976ca0db9abc3a9e57d4a1cf5adaa1291a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433609"
---
# <a name="configure-the-location-database-in-lync-server-2013"></a>Configure the location database in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-17_

Para que os clientes possam detectar automaticamente seu local na rede, primeiro configure o banco de dados de localização. Se você não configurar um banco de dados de local e a **localização necessária** na política de localização estiver definida como **Sim** ou **isenção de responsabilidade**, o usuário será solicitado a inserir um local manualmente.

Para configurar o banco de dados de localização, você executará as seguintes tarefas:

1.  Preencha o banco de dados com um mapeamento de elementos de rede para os locais. Se você usar um gateway de número de identificação de localização de emergência (ELIN), precisará incluir o ELIN no \<CompanyName\> campo.

2.  Valide os endereços em relação ao MSAG (catálogo de endereços principal) mantido pelo provedor de serviços de emergência.

3.  Publique o banco de dados atualizado.

<div>


> [!NOTE]  
> Como alternativa, você pode definir um banco de dados de origem de local secundário que pode ser usado no banco de dados de localização. Para obter detalhes, consulte <A href="lync-server-2013-configure-a-secondary-location-information-service.md">configurar um serviço de informações de localização secundário no Lync Server 2013</A>.



</div>

<div>

## <a name="in-this-section"></a>Nesta seção

  - [Preencher o banco de dados de localização no Lync Server 2013](lync-server-2013-populate-the-location-database.md)

  - [Validar endereços no Lync Server 2013](lync-server-2013-validate-addresses.md)

  - [Publicar o banco de dados de localização do Lync Server 2013](lync-server-2013-publish-the-location-database.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

