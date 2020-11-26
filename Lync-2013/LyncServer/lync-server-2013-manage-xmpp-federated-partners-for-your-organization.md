---
title: 'Lync Server 2013: Gerenciar parceiros XMPP federados para sua organização'
description: 'Lync Server 2013: gerenciar parceiros federados XMPP para sua organização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage XMPP federated partners for your organization
ms:assetid: 48681433-725d-457f-926b-f91d95bcf082
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552450(v=OCS.15)
ms:contentKeyID: 48679561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37d6fb4104c35ffc7db9649656f7786568a48b61
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426022"
---
# <a name="manage-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="82f15-103">Gerenciar parceiros XMPP federados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82f15-103">Manage XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82f15-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82f15-104">

<span> </span></span></span>

<span data-ttu-id="82f15-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="82f15-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="82f15-106">Esta documentação é preliminar e está sujeita a alterações.</span><span class="sxs-lookup"><span data-stu-id="82f15-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="82f15-107">Os tópicos em branco são incluídos como espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="82f15-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="82f15-108">Para gerenciar o suporte para usuários de domínios federados do XMPP, você precisa fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="82f15-108">To manage support for users of XMPP federated domains, you need to do the following:</span></span>

  - <span data-ttu-id="82f15-109">Configure uma ou mais políticas de acesso externo para dar suporte a usuários de domínios federados XMPP.</span><span class="sxs-lookup"><span data-stu-id="82f15-109">Configure one or more external access policies to support users of XMPP federated domains.</span></span>

  - <span data-ttu-id="82f15-110">Configurar a política de configuração de borda de acesso para dar suporte à Federação.</span><span class="sxs-lookup"><span data-stu-id="82f15-110">Configure Access Edge Configuration policy to support federation.</span></span>

  - <span data-ttu-id="82f15-111">Criar definições de parceiros federados XMPP.</span><span class="sxs-lookup"><span data-stu-id="82f15-111">Create XMPP Federated Partners definitions.</span></span>

  - <span data-ttu-id="82f15-112">Compreenda as configurações de negociação disponíveis para a Federação do XMPP.</span><span class="sxs-lookup"><span data-stu-id="82f15-112">Understand negotiation settings available for XMPP federation.</span></span>

<span data-ttu-id="82f15-113">Para executar essas tarefas, use os procedimentos desta seção.</span><span class="sxs-lookup"><span data-stu-id="82f15-113">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="82f15-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="82f15-114">In This Section</span></span>

  - [<span data-ttu-id="82f15-115">Criar ou editar configuração do parceiro XMPP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82f15-115">Create or edit XMPP partner configuration in Lync Server 2013</span></span>](lync-server-2013-create-or-edit-xmpp-partner-configuration.md)

  - [<span data-ttu-id="82f15-116">Configurações de negociação para parceiros de XMPP federados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82f15-116">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md)

  - [<span data-ttu-id="82f15-117">Exemplo de configuração de XMPP no Lync Server 2013 – federação XMPP com Google Talk</span><span class="sxs-lookup"><span data-stu-id="82f15-117">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)

<span data-ttu-id="82f15-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82f15-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

