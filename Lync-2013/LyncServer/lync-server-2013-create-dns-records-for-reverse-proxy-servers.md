---
title: 'Lync Server 2013: Criar registros de DNS para servidores de proxy reverso'
description: 'Lync Server 2013: criar registros DNS para servidores de proxy reverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create DNS records for reverse proxy servers
ms:assetid: b3513339-e49b-4665-80f1-b5a1c81a0e2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429719(v=OCS.15)
ms:contentKeyID: 48185181
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef785ebbd7160274b631a2d2b6b1f1dcc866e5fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431943"
---
# <a name="create-dns-records-for-reverse-proxy-servers-in-lync-server-2013"></a><span data-ttu-id="5dbd8-103">Criar registros de DNS para servidores de proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5dbd8-103">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5dbd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5dbd8-104">

<span> </span></span></span>

<span data-ttu-id="5dbd8-105">_**Tópico da última modificação:** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="5dbd8-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="5dbd8-106">Criar registros DNS externos A que apontam para a interface pública pública do seu Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, Forefront Threat Management Gateway 2010 Server ou serviço de solicitação de aplicativo do servidor de informações da Internet, conforme descrito em [Configurar o suporte a DNS para Edge no Lync Server 2013](lync-server-2013-configure-dns-for-edge-support.md).</span><span class="sxs-lookup"><span data-stu-id="5dbd8-106">Create external DNS A records that point to the public external interface of your Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, Forefront Threat Management Gateway 2010 Server or Internet Information Server Application Request Routing, as described in [Configure DNS for edge support in Lync Server 2013](lync-server-2013-configure-dns-for-edge-support.md).</span></span> <span data-ttu-id="5dbd8-107">Você precisa de registros de DNS para os FQDNs do serviço Web externo para cada pool, o diretor (ou o pool de directors) e cada URL simples.</span><span class="sxs-lookup"><span data-stu-id="5dbd8-107">You need DNS records for the external Web Service FQDNs for each pool, the Director (or Director pool), and each simple URL.</span></span>

<span data-ttu-id="5dbd8-108">Os registros DNS mínimos para a resolução do cliente para o proxy reverso, os seguintes registros devem ser criados:</span><span class="sxs-lookup"><span data-stu-id="5dbd8-108">The minimum DNS records for client resolution to the reverse proxy, the following records must be created:</span></span>

  - <span data-ttu-id="5dbd8-109">Registro (s) do host (A) que define os serviços Web externos publicados para directors e pools de directors (por exemplo, **webdirext.contoso.com**)</span><span class="sxs-lookup"><span data-stu-id="5dbd8-109">Host (A) record(s) that define the published external web services for Directors and Director pools (for example, **webdirext.contoso.com**)</span></span>

  - <span data-ttu-id="5dbd8-110">Registros de host (A) que definem os serviços Web externos publicados para serviços Web externos hospedados em todas as funções de servidor front-end e Standard Edition (por exemplo, **webext.contoso.com**)</span><span class="sxs-lookup"><span data-stu-id="5dbd8-110">Host (A) record(s) that define the published external web services for external web services hosted on the any Front End pools and Standard Edition server roles (for example, **webext.contoso.com**)</span></span>

  - <span data-ttu-id="5dbd8-111">Registros de host (A) para URLs simples (por exemplo, **dialin.contoso.com** e **Meet.contoso.com**)</span><span class="sxs-lookup"><span data-stu-id="5dbd8-111">Host (A) records for the Simple URLs (for example, **dialin.contoso.com** and **meet.contoso.com**)</span></span>

  - <span data-ttu-id="5dbd8-112">Registro de host (A) para o registro externo de descoberta do Lync e também fornece o ponteiro para descoberta automática para todos os aplicativos Web, incluindo o Lync Web App, o Agendador e a mobilidade (por exemplo, **lyncdiscover.contoso.com**)</span><span class="sxs-lookup"><span data-stu-id="5dbd8-112">Host (A) record for the Lync Discover External record, and also provides pointer to AutoDiscover for all Web apps, including the Lync Web App, scheduler and Mobility (for example, **lyncdiscover.contoso.com**)</span></span>

  - <span data-ttu-id="5dbd8-113">Registros de host (A) para a URL do servidor dos Office Web Apps (por exemplo, **officewebapp01.contoso.com**)</span><span class="sxs-lookup"><span data-stu-id="5dbd8-113">Host (A) records for the Office Web Apps Server URL (for example **officewebapp01.contoso.com**)</span></span>

<span data-ttu-id="5dbd8-114">Para obter detalhes, consulte [Resumo DNS-proxy reverso no Lync Server 2013](lync-server-2013-dns-summary-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="5dbd8-114">For details, see [DNS summary - Reverse proxy in Lync Server 2013](lync-server-2013-dns-summary-reverse-proxy.md).</span></span>

<span data-ttu-id="5dbd8-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5dbd8-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

