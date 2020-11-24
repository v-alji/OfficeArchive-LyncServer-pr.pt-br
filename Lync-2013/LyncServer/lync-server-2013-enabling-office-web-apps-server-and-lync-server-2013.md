---
title: 'Lync Server 2013: Habilitando a integração com servidor de Office Web Apps e Lync Server 2013'
description: 'Lync Server 2013: Habilitando o servidor do Office Web Apps e o Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Office Web Apps Server and Lync Server 2013
ms:assetid: 3370ab55-9949-4f32-b88b-5cffed6aaad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204792(v=OCS.15)
ms:contentKeyID: 48183790
ms.date: 08/19/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a1bf4e09dc29bf344b78df50595258f0663cd731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390145"
---
# <a name="configuring-integration-with-office-web-apps-server-and-lync-server-2013"></a>Configurando a integração com servidor de Office Web Apps e Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2016-08-19_

O Lync Server 2013 emprega o servidor do Office Web Apps para manipular apresentações do PowerPoint. Para obter informações sobre as vantagens dessa abordagem, consulte [visão geral de Webconferência no Lync Server 2013](lync-server-2013-web-conferencing-overview.md).

Para usar esses novos recursos, os administradores devem instalar o Office Web Apps Server e devem configurar o Lync Server 2013 para se comunicar com o servidor do Office Web Apps. Esta documentação fornece informações sobre como configurar o Lync Server 2013 para trabalhar com o servidor do Office Web Apps. O que essa documentação não fornece é uma informação sobre como instalar o próprio servidor do Office Web Apps; para obter essas informações, consulte o site de implantação do Microsoft Office Web Apps em <https://go.microsoft.com/fwlink/p/?linkid=257525> . Esse guia inclui informações completas de pré-requisito para o Office Web Apps Server; Observe que o Office Web Apps Server deve ser instalado em um computador autônomo que não esteja executando o Lync Server, o Microsoft SQL Server ou qualquer outro aplicativo de servidor. (Você não deve ter nenhuma versão do Microsoft Office instalada nesse computador.) Qualquer computador usado para executar o Office Web Apps Server também deve ter um conjunto específico de softwares instalado (incluindo .NET Framework 4,5 e Windows PowerShell 3,0); esses requisitos, juntamente com informações sobre a configuração de certificados e serviços de informações da Internet (IIS), são discutidos em detalhes no site de implantação do Microsoft Office Web Apps em <https://go.microsoft.com/fwlink/p/?linkid=257525> .

<div>


> [!NOTE]  
> A iteração mais recente do Office Web Apps Server é chamada Office Online Server, que é compatível com o Lync Server 2013. Para obter mais detalhes, consulte a <A href="https://technet.microsoft.com/library/jj219456(v=office.16).aspx">documentação do Office Online Server</A>.



</div>

Este documento aborda as seguintes áreas de tópico:

  - [Configurando o Lync Server 2013 para trabalhar com o servidor do Office Web Apps](lync-server-2013-configuring-lync-server-2013-to-work-with-office-web-apps-server.md)

  - [Publicando o servidor do Office Web Apps no Lync Server 2013 usando um servidor proxy reverso](lync-server-2013-publishing-office-web-apps-server-using-a-reverse-proxy-server.md)

  - [Validando a configuração do servidor do Office Web Apps no Lync Server 2013](lync-server-2013-validating-the-configuration-of-office-web-apps-server.md)

  - [Configurar clientes do Lync Server 2013 para uso com o servidor do Office Web Apps](lync-server-2013-configuring-clients-for-use-with-office-web-apps-server.md)

</div>

<span> </span>

</div>

</div>

</div>

