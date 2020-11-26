---
title: Migrar a federação XMPP
description: Migrando a Federação do XMPP.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating XMPP federation
ms:assetid: b8d2b4b9-d0ed-4b48-820a-2c257fbdd2fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721861(v=OCS.15)
ms:contentKeyID: 49733794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e63c9f6fd3f1c1d45de77c27417987505678f74b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440357"
---
# <a name="migrating-xmpp-federation"></a><span data-ttu-id="372c1-103">Migrar a federação XMPP</span><span class="sxs-lookup"><span data-stu-id="372c1-103">Migrating XMPP federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="372c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="372c1-104">

<span> </span></span></span>

<span data-ttu-id="372c1-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="372c1-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="372c1-106">As versões anteriores do Lync Server e do Office Communications Server forneciam um gateway de protocolo de presença e mensagens (XMPP) extensível que poderia ser implantado como uma função de servidor separada para permitir a Federação com implantações do XMPP.</span><span class="sxs-lookup"><span data-stu-id="372c1-106">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="372c1-107">No Lync Server 2013, a funcionalidade XMPP pode ser implantada como um recurso.</span><span class="sxs-lookup"><span data-stu-id="372c1-107">In Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="372c1-108">A funcionalidade XMPP é instalada em duas partes: como um proxy do XMPP que é executado no servidor de borda do Lync Server 2013 e o Gateway XMPP executado no servidor front-end do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="372c1-108">XMPP functionality is installed in two parts: as an XMPP proxy that runs on the Lync Server 2013 Edge Server, and the XMPP Gateway that runs on the Lync Server 2013 Front End Server.</span></span>

<span data-ttu-id="372c1-109">De uma perspectiva de migração, uma conta de usuário do Lync Server pode ser movida para um pool do Lync Server 2013 e continuar a usar o gateway herdado XMPP.</span><span class="sxs-lookup"><span data-stu-id="372c1-109">From a migration perspective, a Lync Server user account can be moved to a Lync Server 2013 pool and continue to use the legacy XMPP gateway.</span></span> <span data-ttu-id="372c1-110">Isso só é possível quando o parceiro federado XMPP não está configurado no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="372c1-110">This is possible only when the XMPP federated partner is not configured in Lync Server 2013.</span></span>

<span data-ttu-id="372c1-111">Em resumo, se o Lync Server 2010 tiver sido implantado com o gateway do Office Communications Server 2007 R2 XMPP e a Federação do XMPP tiver sido habilitada para usuários herdados do Lync Server 2010, para migrar a Federação do XMPP para o Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="372c1-111">In summary, if Lync Server 2010 has been deployed with the Office Communications Server 2007 R2 XMPP Gateway and XMPP federation has been enabled for legacy Lync Server 2010 users, to migrate the XMPP federation to Lync Server 2013:</span></span>

1.  <span data-ttu-id="372c1-112">Implantar um pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="372c1-112">Deploy a Lync Server 2013 pool.</span></span>

2.  <span data-ttu-id="372c1-113">Implantar um servidor de borda do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="372c1-113">Deploy a Lync Server 2013 Edge server.</span></span>

3.  <span data-ttu-id="372c1-114">Mover todos os usuários para o pool do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="372c1-114">Move all users to the Lync Server 2013 pool</span></span>

4.  <span data-ttu-id="372c1-115">Criar políticas e certificados de acesso XMPP para o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="372c1-115">Create XMPP access policies and certificates for the Edge Server.</span></span>

5.  <span data-ttu-id="372c1-116">Habilite a Federação do XMPP no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="372c1-116">Enable XMPP federation in Lync Server 2013.</span></span> 

6.  <span data-ttu-id="372c1-117">Atualize as entradas de DNS para apontar para o gateway do Lync Server 2013 XMPP.</span><span class="sxs-lookup"><span data-stu-id="372c1-117">Update the DNS entries to point to the Lync Server 2013 XMPP Gateway.</span></span>

<span data-ttu-id="372c1-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="372c1-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

