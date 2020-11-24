---
title: 'Lync Server 2013: telefones de área comuns'
description: 'Lync Server 2013: telefones de área comuns.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Common area phones
ms:assetid: d63bb3de-154e-4347-9251-9fa94e7d593a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994076(v=OCS.15)
ms:contentKeyID: 51803987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af8a68f875bba1d43a91e5a252259841d7a6bbda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390413"
---
# <a name="common-area-phones-in-lync-server-2013"></a><span data-ttu-id="2b5da-103">Telefones de área comuns no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b5da-103">Common area phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b5da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b5da-104">

<span> </span></span></span>

<span data-ttu-id="2b5da-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="2b5da-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="2b5da-106">Os telefones de área comuns são telefones IP que não estão associados a um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="2b5da-106">Common area phones are IP phones that are not associated with an individual user.</span></span> <span data-ttu-id="2b5da-107">Em vez de estar localizado no escritório de alguém, os telefones de área comuns geralmente estão localizados em prédio "lobbies", lanchonetes, descansos de funcionários, salas de reunião e outros locais onde um grande número de pessoas provavelmente coletará.</span><span class="sxs-lookup"><span data-stu-id="2b5da-107">Instead of being located in someone’s office, common area phones are typically located in building lobbies, cafeterias, employee lounges, meeting rooms, and other locations where a large number of people are likely to gather.</span></span> <span data-ttu-id="2b5da-108">Ao contrário de outros telefones no Lync Server, que são normalmente mantidos por meio de políticas de voz e planos de discagem que são atribuídos a usuários individuais, os telefones de área comuns não têm usuários individuais atribuídos a eles.</span><span class="sxs-lookup"><span data-stu-id="2b5da-108">Unlike other phones in Lync Server, which are typically maintained by using voice policies and dial plans that are assigned to individual users, common area phones do not have individual users assigned to them.</span></span> <span data-ttu-id="2b5da-109">Isso significa que elas devem ser gerenciadas de maneira diferente dos outros telefones.</span><span class="sxs-lookup"><span data-stu-id="2b5da-109">This means that they must be managed differently than your other phones.</span></span>

<span data-ttu-id="2b5da-110">Para gerenciar telefones de área comuns, crie objetos de contato dos serviços de domínio Active Directory para todos os telefones comuns que, como contas de usuário, podem ser atribuídos a políticas e planos de voz.</span><span class="sxs-lookup"><span data-stu-id="2b5da-110">To manage common area phones, you create Active Directory Domain Services contact objects for all your common area phones that, like user accounts, can be assigned policies and voice plans.</span></span> <span data-ttu-id="2b5da-111">Essa abordagem permite que você mantenha o controle sobre telefones comuns de área, embora esses telefones não estejam associados a um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="2b5da-111">This approach enables you to maintain control over common area phones, even though those phones are not associated with an individual user.</span></span>

<span data-ttu-id="2b5da-112">Use os tópicos desta seção para saber como criar objetos de contato para telefones celulares comuns, modificá-los e excluí-los e configurar e exibir informações de configuração sobre os telefones celulares comuns na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="2b5da-112">Use the topics in this section to learn how to create contact objects for common area phones, modify and delete them, and configure and view configuration information about the common area phones in your deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2b5da-113">Você tem três opções para telefones celulares comuns: o Aastra 6721ip Common de área comum, o telefone IP HP 4110 e o telefone de área comum de IP do CX500 Polycom.</span><span class="sxs-lookup"><span data-stu-id="2b5da-113">You have three options for common area phones: the Aastra 6721ip common area phone, the HP 4110 IP Phone, and the Polycom CX500 IP common area phone.</span></span> <span data-ttu-id="2b5da-114">O telefone de conferência IP do Polycom CX3000 é outro telefone de área comum da variante.</span><span class="sxs-lookup"><span data-stu-id="2b5da-114">The Polycom CX3000 IP conferencing phone is another variant common area phone.</span></span> <span data-ttu-id="2b5da-115">No entanto, ele deve ser usado em salas de conferência.</span><span class="sxs-lookup"><span data-stu-id="2b5da-115">However, it is intended for use in conference rooms.</span></span> <span data-ttu-id="2b5da-116">Para obter detalhes sobre telefones de área comuns, consulte a seção de telefones da área comum da <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">escolha de novos dispositivos</A>.</span><span class="sxs-lookup"><span data-stu-id="2b5da-116">For details about common area phones, see the Common Area Phones section of <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">Choosing New Devices</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2b5da-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2b5da-117">In This Section</span></span>

  - [<span data-ttu-id="2b5da-118">Exibir informações de telefone de área comum no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b5da-118">View common area phone information in Lync Server 2013</span></span>](lync-server-2013-view-common-area-phone-information.md)

  - [<span data-ttu-id="2b5da-119">Criar ou modificar um objeto de contato de telefone de área comum no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b5da-119">Create or modify a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="2b5da-120">Habilitar ou desabilitar o hot desk no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b5da-120">Enable or disable hot desking in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-hot-desking.md)

  - [<span data-ttu-id="2b5da-121">Excluir um objeto de contato de telefone de área comum no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b5da-121">Delete a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-delete-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="2b5da-122">Atribuir políticas no Lync Server 2013 a um telefone de área comum</span><span class="sxs-lookup"><span data-stu-id="2b5da-122">Assign policies in Lync Server 2013 to a common area phone</span></span>](lync-server-2013-assign-policies-to-a-common-area-phone.md)

<span data-ttu-id="2b5da-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b5da-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

