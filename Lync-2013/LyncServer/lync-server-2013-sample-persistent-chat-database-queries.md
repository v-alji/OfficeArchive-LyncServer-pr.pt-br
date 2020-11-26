---
title: 'Lync Server 2013: Amostragem de consultas de banco de dados de Chat Persistente'
description: 'Lync Server 2013: exemplo de consultas de banco de dados de chat persistentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Sample Persistent Chat database queries
ms:assetid: 545b1a93-9758-4344-98cc-aa0e559d494f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558649(v=OCS.15)
ms:contentKeyID: 48184133
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e1cb49e944dbbd3e22c1b944b4c8495c6ff9b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442164"
---
# <a name="sample-persistent-chat-database-queries-for-lync-server-2013"></a><span data-ttu-id="2a659-103">Amostragem de consultas de banco de dados de Chat Persistente para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a659-103">Sample Persistent Chat database queries for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a659-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a659-104">

<span> </span></span></span>

<span data-ttu-id="2a659-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="2a659-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="2a659-106">Esta seção contém exemplos de consultas para o banco de dados de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="2a659-106">This section contains sample queries for the Persistent Chat database.</span></span>

<span data-ttu-id="2a659-107">Use o exemplo a seguir para obter uma lista de suas salas de chat persistente mais ativas após uma determinada data.</span><span class="sxs-lookup"><span data-stu-id="2a659-107">Use the following example to get a list of your most active Persistent Chat rooms after a certain date.</span></span>

    SELECT nodeName as ChatRoom, COUNT(*) as ChatMessages
      FROM tblChat, tblNode
      WHERE channelId = nodeID AND dbo.fnTicksToDate(chatDate) > '1/1/2011'
      GROUP BY nodeName
      ORDER BY ChatMessages DESC

<span data-ttu-id="2a659-108">Use o exemplo a seguir para obter uma lista dos seus usuários ativos após uma determinada data.</span><span class="sxs-lookup"><span data-stu-id="2a659-108">Use the following example to get a list of your most active users after a certain date.</span></span>

    SELECT prinName as Name, count(*) as ChatMessages
      FROM tblChat, tblPrincipal
      WHERE prinID = userId AND dbo.fnTicksToDate(chatDate) > '1/1/2011'
      GROUP BY prinName
      ORDER BY ChatMessages DESC

<span data-ttu-id="2a659-109">Use o exemplo a seguir para obter uma lista de todos os participantes que já enviaram uma mensagem com "Olá mundo".</span><span class="sxs-lookup"><span data-stu-id="2a659-109">Use the following example to get a list of everyone who ever sent a message with "Hello World" in it.</span></span>

    SELECT nodeName as ChatRoom, prinName as Name, content as Message
      FROM tblChat, tblNode, tblPrincipal
      WHERE channelId = nodeID AND userId = prinID AND content like '%Hello World%'

<span data-ttu-id="2a659-110">Use o exemplo a seguir para obter uma lista de associações de grupo para uma determinada entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="2a659-110">Use the following example to get a list of group memberships for a certain principal.</span></span>

    SELECT prinName as Name    
      FROM tblPrincipalAffiliations as pa, tblPrincipal
      where principalID = 7 and affiliationID = prinID

<span data-ttu-id="2a659-111">Use o exemplo a seguir para obter uma lista de cada sala de chat que um usuário, Jane Dow, é membro direto de.</span><span class="sxs-lookup"><span data-stu-id="2a659-111">Use the following example to get a list of every chat room that a user, Jane Dow, is a direct member of.</span></span>

    SELECT DISTINCT nodeName as ChatRoom, prinName as Name          
      FROM tblPrincipalRole, tblPrincipal, tblNode
      WHERE  prinRoleNodeID = nodeID AND prinRolePrinID = prinID AND prinName = 'Jane Dow'

<span data-ttu-id="2a659-112">Use o exemplo a seguir para obter uma lista de convites que um usuário recebeu.</span><span class="sxs-lookup"><span data-stu-id="2a659-112">Use the following example to get a list of invitations that a user has received.</span></span>

    SELECT prinName
          ,nodeName
          ,invID   
          ,createdOn
      FROM tblPrincipalInvites as inv, tblPrincipal as p, tblNode as n
      where inv.prinID = 5 AND inv.prinID = p.prinID and inv.nodeID = n.nodeID
      ORDER BY invID DESC

<span data-ttu-id="2a659-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a659-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

