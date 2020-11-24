---
title: 'Lync Server 2013: Implantando repositório unificado de contatos'
description: 'Lync Server 2013: Implantando repositório de contatos unificado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying unified contact store
ms:assetid: 68959d58-ac8a-45de-afcd-b9de2c36799c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204963(v=OCS.15)
ms:contentKeyID: 48184373
ms.date: 06/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 056792d2e4ea66699b276d0d571e83c8a0256483
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389785"
---
# <a name="deploying-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="c4918-103">Implantando repositório unificado de contatos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4918-103">Deploying unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4918-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4918-104">

<span> </span></span></span>

<span data-ttu-id="c4918-105">_**Tópico da última modificação:** 2016-06-06_</span><span class="sxs-lookup"><span data-stu-id="c4918-105">_**Topic Last Modified:** 2016-06-06_</span></span>

<span data-ttu-id="c4918-106">Habilitar o repositório de contatos unificado no Lync Server 2013 não requer nenhuma configuração de topologia.</span><span class="sxs-lookup"><span data-stu-id="c4918-106">Enabling unified contact store in Lync Server 2013 does not require any topology settings.</span></span> <span data-ttu-id="c4918-107">Habilitar o repositório de contatos unificado para usuários requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c4918-107">Enabling unified contact store for users requires the following:</span></span>

  - <span data-ttu-id="c4918-108">Que a política do repositório unificado de contatos esteja habilitada (ela é habilitada por padrão).</span><span class="sxs-lookup"><span data-stu-id="c4918-108">Unified contact store policy is enabled (default is enabled).</span></span>

  - <span data-ttu-id="c4918-109">Os usuários fazem logon com o Lync 2013 pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="c4918-109">Users log in with Lync 2013 at least once.</span></span>

<span data-ttu-id="c4918-110">Após a migração dos contatos de um usuário, o que acontece automaticamente quando um usuário faz logon com o Lync 2013, o usuário pode acessar e gerenciar seus contatos do Lync do Lync 2013, Outlook 2013 ou Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="c4918-110">After a user’s contacts have been migrated, which happens automatically when a user logs in with Lync 2013, the user can access and manage their Lync contacts from Lync 2013, Outlook 2013, or Outlook Web Access.</span></span> <span data-ttu-id="c4918-111">O usuário não precisa estar conectado ao Lync para gerenciar seus contatos do Outlook ou do Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="c4918-111">The user does not have to be logged in to Lync to manage their contacts from Outlook or Outlook Web Access.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c4918-112">Se um usuário fizer logon do Lync 2010 após a migração, os contatos e os grupos estarão disponíveis e atualizados, mas o usuário não poderá gerenciar (ou seja, adicionar, excluir, mover, marcar, remover ou modificar) esses contatos.</span><span class="sxs-lookup"><span data-stu-id="c4918-112">If a user logs in from Lync 2010 after migration, contacts and groups are available and up-to-date, but the user cannot manage (that is, add, delete, move, tag, untag, or modify) those contacts.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c4918-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c4918-113">In This Section</span></span>

  - [<span data-ttu-id="c4918-114">Habilitar usuários para repositório unificado de contatos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4918-114">Enable users for unified contact store in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-unified-contact-store.md)

  - [<span data-ttu-id="c4918-115">Migrar usuários para o repositório unificado de contatos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4918-115">Migrate users to unified contact store in Lync Server 2013</span></span>](lync-server-2013-migrate-users-to-unified-contact-store.md)

  - [<span data-ttu-id="c4918-116">Reverter usuários migrados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4918-116">Roll back migrated users in Lync Server 2013</span></span>](lync-server-2013-roll-back-migrated-users.md)

<span data-ttu-id="c4918-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4918-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

