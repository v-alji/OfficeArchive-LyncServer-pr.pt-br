---
title: 'Lync Server 2013: Configurando os servidores de borda'
description: 'Lync Server 2013: Configurando servidores de borda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Edge Servers
ms:assetid: 09a22919-e36f-4122-8f0d-8d041198912d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398147(v=OCS.15)
ms:contentKeyID: 48183354
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e25c40e8d642d38b38afbab35225b2c7dda4d68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423978"
---
# <a name="setting-up-edge-servers-in-lync-server-2013"></a><span data-ttu-id="6011c-103">Configurando os servidores de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6011c-103">Setting up Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6011c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6011c-104">

<span> </span></span></span>

<span data-ttu-id="6011c-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="6011c-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="6011c-106">As principais tarefas necessárias para configurar servidores de borda são iguais para instalar um único servidor de borda ou um pool de balanceamento de carga de servidores de borda, exceto que um pool de servidores de borda com carga balanceada de hardware requer a implantação dos balanceadores de carga e outras etapas para replicar a configuração em vários servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="6011c-106">The primary tasks required to set up Edge Servers are the same for installing a single Edge Server or a load-balanced pool of Edge Servers, except that a pool of hardware load balanced Edge Servers requires deployment of the load balancers and additional steps for replicating the set up on multiple Edge Servers.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6011c-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6011c-107">In This Section</span></span>

  - [<span data-ttu-id="6011c-108">Configurar interfaces de rede para Servidores de Borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6011c-108">Set up network interfaces for Edge Servers in Lync Server 2013</span></span>](lync-server-2013-set-up-network-interfaces-for-edge-servers.md)

  - [<span data-ttu-id="6011c-109">Instalar software de pré-requisito nos Servidores de Borda para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6011c-109">Install prerequisite software on Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-prerequisite-software-on-edge-servers.md)

  - [<span data-ttu-id="6011c-110">Exportar sua topologia do Lync Server 2013 e copiá-la na mídia externa para instalação de borda</span><span class="sxs-lookup"><span data-stu-id="6011c-110">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

  - [<span data-ttu-id="6011c-111">Instalar Servidores de Borda para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6011c-111">Install Edge Servers for Lync Server 2013</span></span>](lync-server-2013-install-edge-servers.md)

  - [<span data-ttu-id="6011c-112">Configurar certificados de Borda para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6011c-112">Set up Edge certificates for Lync Server 2013</span></span>](lync-server-2013-set-up-edge-certificates.md)

  - [<span data-ttu-id="6011c-113">Iniciar Servidores de Borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6011c-113">Start Edge Servers in Lync Server 2013</span></span>](lync-server-2013-start-edge-servers.md)

  - [<span data-ttu-id="6011c-114">Configurando servidores de proxy reverso para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6011c-114">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)

<span data-ttu-id="6011c-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6011c-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

