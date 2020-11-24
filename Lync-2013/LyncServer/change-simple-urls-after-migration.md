---
title: Alterar URLs simples após a migração
description: Alterar URLs simples após a migração.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change simple URLs after migration
ms:assetid: addb0dc8-8324-42b1-9a00-f4bd14fdf5c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721844(v=OCS.15)
ms:contentKeyID: 49733777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f9974106d28bcfdc64c2255337baf721a937e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389916"
---
# <a name="change-simple-urls-after-migration"></a><span data-ttu-id="f82d6-103">Alterar URLs simples após a migração</span><span class="sxs-lookup"><span data-stu-id="f82d6-103">Change simple URLs after migration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f82d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f82d6-104">

<span> </span></span></span>

<span data-ttu-id="f82d6-105">_**Tópico da última modificação:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="f82d6-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="f82d6-106">O Lync Server oferece suporte a três URLs simples:</span><span class="sxs-lookup"><span data-stu-id="f82d6-106">Lync Server supports three simple URLs:</span></span>

  - <span data-ttu-id="f82d6-107">A **reunião** é usada como a URL base para todas as conferências no site ou na organização.</span><span class="sxs-lookup"><span data-stu-id="f82d6-107">**Meet** is used as the base URL for all conferences in the site or organization.</span></span> <span data-ttu-id="f82d6-108">Com a URL simples de reunião, os links para ingressar em reuniões são fáceis de compreender e fáceis de se comunicar e distribuir.</span><span class="sxs-lookup"><span data-stu-id="f82d6-108">With the Meet simple URL, links to join meetings are easy to comprehend, and easy to communicate and distribute.</span></span>

  - <span data-ttu-id="f82d6-109">A **discagem** permite o acesso à página da Web configurações de conferência discada.</span><span class="sxs-lookup"><span data-stu-id="f82d6-109">**Dial-in** enables access to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="f82d6-110">A URL simples Dial-in é incluída em todos os convites de reunião para que os usuários que desejam discar para a reunião possam acessar o número de telefone e as informações de PIN necessárias.</span><span class="sxs-lookup"><span data-stu-id="f82d6-110">The Dial-in simple URL is included in all meeting invitations so that users who want to dial in to the meeting can access the necessary phone number and PIN information.</span></span>

  - <span data-ttu-id="f82d6-111">O **administrador** habilita o acesso rápido ao painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f82d6-111">**Admin** enables quick access to the Lync Server Control Panel.</span></span> <span data-ttu-id="f82d6-112">A URL simples de Admin é parte interna da sua organização.</span><span class="sxs-lookup"><span data-stu-id="f82d6-112">The Admin simple URL is internal to your organization.</span></span>

<span data-ttu-id="f82d6-113">Depois de migrar para o Lync Server 2013, você deve estar ciente de como a alteração afeta seus registros DNS e certificados para URLs simples.</span><span class="sxs-lookup"><span data-stu-id="f82d6-113">After migrating to Lync Server 2013, you must be aware of how the change impacts your DNS records and certificates for simple URLs.</span></span> <span data-ttu-id="f82d6-114">Se o diretor herdado do Lync Server 2010 permanecer em uso na topologia, nenhuma alteração nas suas URLs simples será necessária.</span><span class="sxs-lookup"><span data-stu-id="f82d6-114">If the legacy Lync Server 2010 Director remains in use in the topology, no changes to your simple URLs are required.</span></span> <span data-ttu-id="f82d6-115">Se o diretor do Lync Server 2010 for removido da topologia após a migração, os registros DNS de URL simples deverão ser atualizados para apontar para um dos pools do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f82d6-115">If the Lync Server 2010 Director is removed from the topology after migration, the simple URL DNS records must be updated to point to one of the Lync Server 2013 pools.</span></span> <span data-ttu-id="f82d6-116">No entanto, sempre que você alterar um nome de URL simples, será necessário executar Enable-CsComputer em cada director e servidor front-end para registrar a alteração.</span><span class="sxs-lookup"><span data-stu-id="f82d6-116">Whenever you change a simple URL name, however, you must run Enable-CsComputer on each Director and Front End Server to register the change.</span></span>

<div>

## <a name="changing-simple-urls-after-migration"></a><span data-ttu-id="f82d6-117">Alterar URLs simples após a migração</span><span class="sxs-lookup"><span data-stu-id="f82d6-117">Changing Simple URLs after Migration</span></span>

<span data-ttu-id="f82d6-118">**Para atualizar a URL de reunião simples**</span><span class="sxs-lookup"><span data-stu-id="f82d6-118">**To update the Meet simple URL**</span></span>

1.  <span data-ttu-id="f82d6-119">No construtor de topologias, clique com o botão direito do mouse no nó superior do **Lync Server** e clique em **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f82d6-119">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="f82d6-120">Selecione **URLs simples** no painel esquerdo e, abaixo de **URLs de reunião:** selecione a URL do encontro e clique em **Editar URL**.</span><span class="sxs-lookup"><span data-stu-id="f82d6-120">Select **Simple URLs** in the left pane, then below **Meeting URLs:** select the Meet URL and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="f82d6-121">Atualize a URL para o valor desejado e clique em **OK** para salvar a URL editada.</span><span class="sxs-lookup"><span data-stu-id="f82d6-121">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span>

<span data-ttu-id="f82d6-122">**Para atualizar a URL simples de administrador**</span><span class="sxs-lookup"><span data-stu-id="f82d6-122">**To update the Admin simple URL**</span></span>

1.  <span data-ttu-id="f82d6-123">No construtor de topologias, clique com o botão direito do mouse no nó superior do **Lync Server** e clique em **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f82d6-123">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="f82d6-124">Selecione **URLs simples** no painel esquerdo e, em seguida, abaixo da caixa **URL de acesso administrativo** , insira a URL simples que você deseja para acessar o painel de controle do Lync Server 2013 e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f82d6-124">Select **Simple URLs** in the left pane, then below **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="f82d6-125">Nós recomendamos que você use a URL do administrador mais simples possível.</span><span class="sxs-lookup"><span data-stu-id="f82d6-125">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="f82d6-126">A opção mais simples é <STRONG> https://admin .</STRONG> &lt; domínio &gt; .</span><span class="sxs-lookup"><span data-stu-id="f82d6-126">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f82d6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f82d6-127">See Also</span></span>


[<span data-ttu-id="f82d6-128">Planejamento de URLs simples no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f82d6-128">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="f82d6-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f82d6-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

