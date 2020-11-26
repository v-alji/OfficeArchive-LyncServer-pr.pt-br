---
title: Verificar se todos os objetos de contato do Exchange UM são removidos do pool herdado
description: Verifique se todos os objetos de contato de UM do Exchange foram removidos do pool herdado.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440133"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a><span data-ttu-id="3274e-103">Verificar se todos os objetos de contato do Exchange UM são removidos do pool herdado</span><span class="sxs-lookup"><span data-stu-id="3274e-103">Verify that all Exchange UM Contact objects are removed from the legacy pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3274e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3274e-104">

<span> </span></span></span>

<span data-ttu-id="3274e-105">_**Tópico da última modificação:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="3274e-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="3274e-106">Use a ferramenta **OCSUmUtil** ou o cmdlet **Get-CsExumContact** para verificar se objetos de contato do Exchange um foram removidos do pool herdado do Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3274e-106">Use either the **OCSUmUtil** tool or the **Get-CsExumContact** cmdlet to verify that Exchange UM contact objects have been removed from the legacy Office Communications Server 2007 R2 pool.</span></span> <span data-ttu-id="3274e-107">O **OCSUmUtil** está localizado na seguinte pasta:</span><span class="sxs-lookup"><span data-stu-id="3274e-107">**OCSUmUtil** is located in the following folder:</span></span>

<span data-ttu-id="3274e-108">% Arquivos de programas% \\ Arquivos comuns \\ Lync Server 2013 \\ suporte \\OcsUMUtil.exe</span><span class="sxs-lookup"><span data-stu-id="3274e-108">%Program Files%\\Common Files\\Lync Server 2013\\Support\\OcsUMUtil.exe</span></span>

<span data-ttu-id="3274e-109">O **OCSUmUtil** deve ser executado a partir de uma conta de usuário que tenha:</span><span class="sxs-lookup"><span data-stu-id="3274e-109">**OCSUmUtil** must be run from a user account that has:</span></span>

  - <span data-ttu-id="3274e-110">Associação no grupo RTCUniversalServerAdmins e RTCUniversalUserAdmins (que inclui direitos para ler as configurações de mensagens unificadas do Exchange Server)</span><span class="sxs-lookup"><span data-stu-id="3274e-110">Membership in the RTCUniversalServerAdmins and RTCUniversalUserAdmins group (which includes rights to read Exchange Server Unified Messaging settings)</span></span>

  - <span data-ttu-id="3274e-111">Direitos de domínio para criar objetos de contato no contêiner de unidade organizacional (UO) especificado</span><span class="sxs-lookup"><span data-stu-id="3274e-111">Domain rights to create contact objects in the specified organizational unit (OU) container</span></span>

<span data-ttu-id="3274e-112">Para obter detalhes sobre como usar o cmdlet **Get-CsExumContact** , consulte [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3274e-112">For details about using the **Get-CsExumContact** cmdlet, see [Get-CsExUmContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="3274e-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3274e-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

