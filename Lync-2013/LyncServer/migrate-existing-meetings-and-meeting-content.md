---
title: Migrar reuniões existentes e conteúdo de reunião
description: Migrar reuniões existentes e o conteúdo da reunião.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443801"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a><span data-ttu-id="9f396-103">Migrar reuniões existentes e conteúdo de reunião</span><span class="sxs-lookup"><span data-stu-id="9f396-103">Migrate existing meetings and meeting content</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f396-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f396-104">

<span> </span></span></span>

<span data-ttu-id="9f396-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="9f396-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="9f396-106">Quando uma conta de usuário é movida do Lync Server 2010 para um servidor do Lync Server 2013, as seguintes informações são movidas com essa conta de usuário:</span><span class="sxs-lookup"><span data-stu-id="9f396-106">When a user account is moved from Lync Server 2010 to a Lync Server 2013 server, the following information is moved with that user account:</span></span>

  - <span data-ttu-id="9f396-107">**Reuniões já programadas pelo usuário**.</span><span class="sxs-lookup"><span data-stu-id="9f396-107">**Meetings already scheduled by the user**.</span></span> <span data-ttu-id="9f396-108">Isso inclui a movimentação dos diretórios de conferências e dos dados de conferência.</span><span class="sxs-lookup"><span data-stu-id="9f396-108">This includes moving the conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="9f396-109">**PIN (número de identificação pessoal) do usuário**.</span><span class="sxs-lookup"><span data-stu-id="9f396-109">**User’s personal identification number (PIN)**.</span></span> <span data-ttu-id="9f396-110">O PIN atual do usuário continua a funcionar até que ele expire ou que o usuário solicitou um novo PIN.</span><span class="sxs-lookup"><span data-stu-id="9f396-110">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="9f396-111">As seguintes informações da conta de usuário não se movem para o novo servidor.</span><span class="sxs-lookup"><span data-stu-id="9f396-111">The following user account information does not move to the new server.</span></span>

  - <span data-ttu-id="9f396-112">**Conteúdo da reunião**.</span><span class="sxs-lookup"><span data-stu-id="9f396-112">**Meeting content**.</span></span> <span data-ttu-id="9f396-113">Para mover o conteúdo compartilhado durante uma reunião, por exemplo, PowerPoint, quadro de comunicações, anexos ou dados de votação, use o parâmetro **-MoveConferenceData** como parte do cmdlet **move-CsUser** .</span><span class="sxs-lookup"><span data-stu-id="9f396-113">In order to move the content shared during a meeting, for example PowerPoint, Whiteboard, attachments or poll data, use the **-MoveConferenceData** parameter as part of the **Move-CsUser** cmdlet.</span></span>

<span data-ttu-id="9f396-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f396-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

