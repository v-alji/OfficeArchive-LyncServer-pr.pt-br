---
title: Práticas recomendadas do Servidor de Chat Persistente
description: Práticas recomendadas do servidor de chat persistente.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server best practices
ms:assetid: dc18e7f7-599b-4d32-abf7-cd9e691426a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398970(v=OCS.15)
ms:contentKeyID: 48185612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c575c0afa0366e88748eadfcf4c04fccb20b375
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438782"
---
# <a name="persistent-chat-server-best-practices"></a><span data-ttu-id="0795a-103">Práticas recomendadas do Servidor de Chat Persistente</span><span class="sxs-lookup"><span data-stu-id="0795a-103">Persistent Chat Server best practices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0795a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0795a-104">

<span> </span></span></span>

<span data-ttu-id="0795a-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="0795a-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="0795a-106">À medida que você cria suas categorias e salas de chat persistentes e cria seu escopo e associação, as dicas a seguir podem ajudar no seu planejamento:</span><span class="sxs-lookup"><span data-stu-id="0795a-106">As you create your categories and Persistent Chat rooms and design your scoping and membership, the following tips can help your planning:</span></span>

  - <span data-ttu-id="0795a-107">Se a sua empresa não exigir uma parede ética, não restrinja o escopo na sua árvore de categoria.</span><span class="sxs-lookup"><span data-stu-id="0795a-107">If your company does not require an ethical wall, do not narrow the scope in your category tree.</span></span> <span data-ttu-id="0795a-108">Coloque todos os usuários no escopo de uma categoria e crie todas as salas de chat nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="0795a-108">Put all your users in the scope of one category, and create all chat rooms in that category.</span></span> <span data-ttu-id="0795a-109">Em seguida, use somente listas de associação para conceder ou restringir o acesso a cada sala de chat.</span><span class="sxs-lookup"><span data-stu-id="0795a-109">Subsequently, use only membership lists to grant or restrict access to each chat room.</span></span>

  - <span data-ttu-id="0795a-110">Na maioria dos casos, você deve permitir que os usuários criem novas salas de chat para que as discussões sobre novos tópicos possam ser iniciadas a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="0795a-110">In most cases, you should enable users to create new chat rooms so that discussions about new topics can be started any time.</span></span> <span data-ttu-id="0795a-111">Faça isso fazendo com que a lista de **criadores** seja a mesma que a lista **AllowedMembers** .</span><span class="sxs-lookup"><span data-stu-id="0795a-111">Do this by making the **Creators** list the same as the **AllowedMembers** list.</span></span> <span data-ttu-id="0795a-112">No entanto, se você quiser permitir que apenas uma equipe de suporte central ou usuários designados criem salas, torne a lista de **criadores** como o subconjunto apropriado.</span><span class="sxs-lookup"><span data-stu-id="0795a-112">However, if you want to allow only a central support team or designated users to create rooms, then make the **Creators** list as the appropriate subset.</span></span>

  - <span data-ttu-id="0795a-113">Dê a cada sala de chat um resumo completo de nome e descrição que descreva onde cabe em sua organização.</span><span class="sxs-lookup"><span data-stu-id="0795a-113">Give each chat room a complete name and description summary that describes where it fits in with your organization.</span></span> <span data-ttu-id="0795a-114">Como os usuários não conseguem ver o nome da categoria quando usam a sala de chat, você não pode depender do nome da categoria para ajudar os usuários a determinar o fórum de discussão desejado para a sala de chat.</span><span class="sxs-lookup"><span data-stu-id="0795a-114">Because users cannot see the category name when they use the chat room, you cannot rely on the category name to help users determine the intended discussion forum for the chat room.</span></span>

  - <span data-ttu-id="0795a-115">Talvez você queira ter um fluxo de trabalho de criação de sala personalizado se tiver determinadas convenções de nomenclatura ou outros controles ou validações de acesso a implementar.</span><span class="sxs-lookup"><span data-stu-id="0795a-115">You may want to have a custom room creation workflow if you have certain naming conventions or other access controls or validations to implement.</span></span> <span data-ttu-id="0795a-116">A configuração de chat persistente permite que você personalize o **RoomManagementUrl** para algo que você hospeda.</span><span class="sxs-lookup"><span data-stu-id="0795a-116">The Persistent Chat configuration enables you to customize the **RoomManagementUrl** to something that you host.</span></span> <span data-ttu-id="0795a-117">Por exemplo, quando os usuários clicam em **criar uma sala** em seus clientes Lync, eles podem ser redirecionados para sua solução personalizada.</span><span class="sxs-lookup"><span data-stu-id="0795a-117">For example, when users click **Create a room** in their Lync client, they can be redirected to your custom solution.</span></span>

  - <span data-ttu-id="0795a-118">Crie uma variedade de suplementos que ajudam a aprimorar a experiência de salas de chat, trazendo outros dados comerciais para salas de chat.</span><span class="sxs-lookup"><span data-stu-id="0795a-118">Create a variety of add-ins that help to enhance the experience of chat rooms by bringing in other business data into chat rooms.</span></span> <span data-ttu-id="0795a-119">Os administradores devem registrar os suplementos que desejam permitir no sistema.</span><span class="sxs-lookup"><span data-stu-id="0795a-119">Administrators must register the add-ins that they want to allow in the system.</span></span> <span data-ttu-id="0795a-120">Os criadores e os criadores da sala de chat podem escolher na lista de suplementos permitidos para aqueles que são mais relevantes para suas respectivas salas.</span><span class="sxs-lookup"><span data-stu-id="0795a-120">Chat room managers and creators can choose from the list of allowed add-ins for the ones most relevant to their respective rooms.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="0795a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0795a-121">See Also</span></span>


[<span data-ttu-id="0795a-122">Gerenciando categotias, salas e suplementos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0795a-122">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>](lync-server-2013-managing-categories-rooms-and-add-ins.md)  
  

<span data-ttu-id="0795a-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0795a-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

