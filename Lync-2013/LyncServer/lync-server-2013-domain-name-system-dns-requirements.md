---
title: 'Lync Server 2013: requisitos de DNS (sistema de nomes de domínio)'
description: 'Lync Server 2013: requisitos do sistema de nome de domínio (DNS).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Domain Name System (DNS) requirements
ms:assetid: 586cf18e-0080-4eb1-aee5-56843277fdfc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398386(v=OCS.15)
ms:contentKeyID: 48184194
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f84868d4929cc410cddbb6c9ad2019a12841e80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389699"
---
# <a name="domain-name-system-dns-requirements-for-lync-server-2013"></a><span data-ttu-id="6c967-103">Requisitos do sistema de nomes de domínio (DNS) para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-103">Domain Name System (DNS) requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c967-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c967-104">

<span> </span></span></span>

<span data-ttu-id="6c967-105">_**Tópico da última modificação:** 2012-06-18_</span><span class="sxs-lookup"><span data-stu-id="6c967-105">_**Topic Last Modified:** 2012-06-18_</span></span>

<span data-ttu-id="6c967-106">Para implantar o Lync Server, você deve criar registros de sistema de nome de domínio (DNS) que permitem a descoberta de clientes e servidores e, opcionalmente, suporte para entrada automática de cliente se a sua organização quiser dar suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="6c967-106">To deploy Lync Server, you must create Domain Name System (DNS) records that enable the discovery of clients and servers, and, optionally, support for automatic client sign-in if your organization wants to support it.</span></span>

<span data-ttu-id="6c967-107">O Lync Server usa o DNS das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="6c967-107">Lync Server uses DNS in the following ways:</span></span>

  - <span data-ttu-id="6c967-108">Para descobrir servidores internos ou pools para comunicações entre servidores.</span><span class="sxs-lookup"><span data-stu-id="6c967-108">To discover internal servers or pools for server-to-server communications.</span></span>

  - <span data-ttu-id="6c967-109">Para permitir que os clientes descubram o pool de front-end ou o servidor Standard Edition usado para várias transações SIP.</span><span class="sxs-lookup"><span data-stu-id="6c967-109">To allow clients to discover the Front End pool or Standard Edition server used for various SIP transactions.</span></span>

  - <span data-ttu-id="6c967-110">Para permitir que dispositivos de comunicação unificada (UC) não estejam conectados para descobrir o pool de front-end ou o servidor Standard Edition executando o serviço Web de atualização de dispositivos, obtenha atualizações e envie logs.</span><span class="sxs-lookup"><span data-stu-id="6c967-110">To allow unified communications (UC) devices that are not logged on to discover the Front End pool or Standard Edition server running Device Update Web Service, obtain updates, and send logs.</span></span>

  - <span data-ttu-id="6c967-111">Para permitir que servidores e clientes externos se conectem a servidores de borda ou ao proxy reverso HTTP para mensagens instantâneas (IM) ou conferência.</span><span class="sxs-lookup"><span data-stu-id="6c967-111">To allow external servers and clients to connect to Edge Servers or the HTTP reverse proxy for instant messaging (IM) or conferencing.</span></span>

  - <span data-ttu-id="6c967-112">Para permitir que dispositivos de comunicação unificada externos se conectem ao serviço Web de atualização de dispositivo por meio de servidores de borda ou do proxy reverso HTTP e obtenham atualizações</span><span class="sxs-lookup"><span data-stu-id="6c967-112">To allow external UC devices to connect to Device Update Web service through Edge Servers or the HTTP reverse proxy and obtain updates.</span></span>

  - <span data-ttu-id="6c967-113">Para permitir que os clientes móveis descubram automaticamente os recursos de serviços Web sem exigir que os usuários insiram manualmente URLs nas configurações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c967-113">To allow mobile clients to automatically discover Web Services resources without requiring users to manually enter URLs in device settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6c967-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6c967-114">In This Section</span></span>

  - [<span data-ttu-id="6c967-115">Determinar requisitios de DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-115">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)

  - [<span data-ttu-id="6c967-116">Requisitos de DNS para pools front-end no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-116">DNS requirements for Front End pools in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-front-end-pools.md)

  - [<span data-ttu-id="6c967-117">Requisitos de DNS para servidores de edição padrão no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-117">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-standard-edition-servers.md)

  - [<span data-ttu-id="6c967-118">Requisitos de DNS para URLs simples no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-118">DNS requirements for simple URLs in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-simple-urls.md)

  - [<span data-ttu-id="6c967-119">Requisitos de DNS para entrada automática do cliente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-119">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)

  - [<span data-ttu-id="6c967-120">Requisitos de DNS para mobilidade com o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-120">DNS requirements for mobility with Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-mobility.md)

  - [<span data-ttu-id="6c967-121">Balanceamento de carga de DNS no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c967-121">DNS load balancing in Lync Server 2013</span></span>](lync-server-2013-dns-load-balancing.md)

<span data-ttu-id="6c967-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c967-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

