---
title: 'Lync Server 2013: Guia de configuração para conectividade Lync-Skype'
description: 'Lync Server 2013: guia de provisionamento para Lync-Skype conectividade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Provisioning guide for Lync-Skype connectivity
ms:assetid: 69adda9b-5b72-4538-9be6-079b2f462e09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440173(v=OCS.15)
ms:contentKeyID: 57793363
ms.date: 11/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9859a7a621ba4329fe0436fe50a0d9de1d0ae1ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436738"
---
# <a name="provisioning-guide-for-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="59f20-103">Guia de configuração para conectividade Lync-Skype no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="59f20-103">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="59f20-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="59f20-104">

<span> </span></span></span>

<span data-ttu-id="59f20-105">_**Tópico da última modificação:** 2014-11-26_</span><span class="sxs-lookup"><span data-stu-id="59f20-105">_**Topic Last Modified:** 2014-11-26_</span></span>

<span data-ttu-id="59f20-106">O Lync Server 2013 suporta conectividade com o Skype.</span><span class="sxs-lookup"><span data-stu-id="59f20-106">Lync Server 2013 supports connectivity with Skype.</span></span> <span data-ttu-id="59f20-107">Essa conectividade permite que os usuários do seu Lync 2013 adicionem os contatos do Skype usando a conta da Microsoft de usuário do Skype (MSA).</span><span class="sxs-lookup"><span data-stu-id="59f20-107">This connectivity enables your Lync 2013 users to add Skype contacts by using the Skype user’s Microsoft Account (MSA).</span></span> <span data-ttu-id="59f20-108">Os clientes do Skype podem adicionar os usuários do Lync à sua lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="59f20-108">Skype clients can also add Lync users to their contact list.</span></span> <span data-ttu-id="59f20-109">Com base em políticas definidas administrativamente no Lync Server, usuários do Lync e do Skype poderão se comunicar por mensagem instantânea, ver a presença de cada um e iniciar chamadas de áudio e de vídeo.</span><span class="sxs-lookup"><span data-stu-id="59f20-109">Based on policies administratively set in Lync Server, Lync and Skype users will be able to communicate using instant messaging, see each other’s presence, and initiate audio and video calls.</span></span> <span data-ttu-id="59f20-110">Lync-Skype conectividade também é um recurso do Lync Online e pode ser habilitado para clientes do Lync Online a partir do centro de administração do Lync no centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="59f20-110">Lync-Skype connectivity is also a feature of Lync Online, and can be enabled for Lync Online customers from the Lync Administration Center within the Microsoft 365 admin center.</span></span>

<div>

> [!IMPORTANT]  
> <span data-ttu-id="59f20-p102">Se o Servidor Lync já está configurado para conectar com o Windows Messenger usando Conectividade Pública de Mensagem Instantânea (PIC), sua implantação já está configurada para a conectividade Lync-Skype. A única mudança que você pode querer considerar é renomear sua entrada existente no Messenger PIC como do Skype. Para mais detalhes, consulte Configurar o provedor do Skype PIC definindo para Lync mais adiante, neste guia.</span><span class="sxs-lookup"><span data-stu-id="59f20-p102">If Lync Server is already configured to connect with Windows Messenger by using Public Instant Messaging Connectivity (PIC), your deployment is already configured for Lync-Skype connectivity. The only change you may want to consider is to rename your existing Messenger PIC entry as Skype. For details, see Configure the Skype PIC provider setting for Lync later in this guide.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="59f20-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="59f20-114">In This Section</span></span>

  - [<span data-ttu-id="59f20-115">Observação sobre a conectividade do Lync-Skype no Lync Server 2013 para clientes do Lync Online</span><span class="sxs-lookup"><span data-stu-id="59f20-115">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>](lync-server-2013-note-about-lync-skype-connectivity-for-lync-on.md)

  - [<span data-ttu-id="59f20-116">Acessando o site de configuração de conectividade a redes públicas de mensagens instantâneas do Lync Server a partir do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="59f20-116">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>](lync-server-2013-accessing-the-lync-server-public-im-connectivity-provisioning-site.md)

  - [<span data-ttu-id="59f20-117">Habilitando conectividade Lync-Skype no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="59f20-117">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-enabling-lync-skype-connectivity.md)

  - [<span data-ttu-id="59f20-118">Usando a conectividade Lync-Skype no Lync Server 2013 como usuário final</span><span class="sxs-lookup"><span data-stu-id="59f20-118">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

  - [<span data-ttu-id="59f20-119">Perguntas Frequentes: Configurando Lync Server 2013 para conectividade com Skype</span><span class="sxs-lookup"><span data-stu-id="59f20-119">Frequently Asked Questions: Provisioning Lync Server 2013 for Skype connectivity</span></span>](lync-server-2013-frequently-asked-questions-provisioning-lync-server-for-skype-connectivity.md)

<span data-ttu-id="59f20-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="59f20-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

