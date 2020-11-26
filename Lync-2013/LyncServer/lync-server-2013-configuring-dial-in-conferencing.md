---
title: 'Lync Server 2013: Configurando conferência discada'
description: 'Lync Server 2013: Configurando conferência discada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring dial-in conferencing
ms:assetid: 79a98c5d-a0a8-4729-828d-b9166842432c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398600(v=OCS.15)
ms:contentKeyID: 48184587
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9c3353caa1344b717b0f64c271149f078f194e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433203"
---
# <a name="configuring-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="14396-103">Configurando conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-103">Configuring dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14396-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14396-104">

<span> </span></span></span>

<span data-ttu-id="14396-105">_**Tópico da última modificação:** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="14396-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="14396-106">Esta seção orienta você na configuração da conferência discada do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="14396-106">This section guides you through the configuration of Lync Server 2013 dial-in conferencing.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="14396-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="14396-107">In This Section</span></span>

  - [<span data-ttu-id="14396-108">Pré-requisitos e permissões de configuração de conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-108">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-configuration-prerequisites-and-permissions.md)

  - [<span data-ttu-id="14396-109">Lista de verificação de implantação para conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-109">Deployment checklist for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-dial-in-conferencing.md)

  - [<span data-ttu-id="14396-110">Configurar planos de discagem para conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-110">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)

  - [<span data-ttu-id="14396-111">Verifique se os planos de discagem do Lync Server 2013 atribuiram regiões</span><span class="sxs-lookup"><span data-stu-id="14396-111">Make sure dial plans Lync Server 2013 have assigned regions</span></span>](lync-server-2013-make-sure-dial-plans-have-assigned-regions.md)

  - [<span data-ttu-id="14396-112">(Opcional) Verificar configurações de política de PIN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-112">(Optional) Verify PIN policy settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-pin-policy-settings.md)

  - [<span data-ttu-id="14396-113">Configurar política de conferência para discagem no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-113">Configure conferencing policy for dial-in in Lync Server 2013</span></span>](lync-server-2013-configure-conferencing-policy-for-dial-in.md)

  - [<span data-ttu-id="14396-114">Configurar número de acesso da conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-114">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>](lync-server-2013-configure-dial-in-conferencing-access-numbers.md)

  - [<span data-ttu-id="14396-115">(Opcional) Verificar configurações de conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-115">(Optional) Verify dial-in conferencing settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing-settings.md)

  - [<span data-ttu-id="14396-116">(Opcional) Modificar mapeamento principal de comandos DTMF no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-116">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</span></span>](lync-server-2013-optional-modify-key-mapping-for-dtmf-commands.md)

  - [<span data-ttu-id="14396-117">(Opcional) Habilitar e desabilitar comunicados de ingresso e saída de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-117">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>](lync-server-2013-optional-enable-and-disable-conference-join-and-leave-announcements.md)

  - [<span data-ttu-id="14396-118">(Opcional) Verificar conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-118">(Optional) Verify dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing.md)

  - [<span data-ttu-id="14396-119">Implantar suplemento Online Meeting para Lync 2013</span><span class="sxs-lookup"><span data-stu-id="14396-119">Deploy the Online Meeting Add-in for Lync 2013</span></span>](lync-server-2013-deploy-the-online-meeting-add-in-for-lync-2013.md)

  - [<span data-ttu-id="14396-120">Definir configurações de conta do usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-120">Configure user account settings in Lync Server 2013</span></span>](lync-server-2013-configure-user-account-settings.md)

  - [<span data-ttu-id="14396-121">(Recommended) Create Conference Directories</span><span class="sxs-lookup"><span data-stu-id="14396-121">(Recommended) Create Conference Directories</span></span>](recommended-create-conference-directories.md)

  - [<span data-ttu-id="14396-122">(Opcional) Dar as boas-vindas aos usuários na conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-122">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-welcome-users-to-dial-in-conferencing.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="14396-123">Seções Relacionadas</span><span class="sxs-lookup"><span data-stu-id="14396-123">Related Sections</span></span>

[<span data-ttu-id="14396-124">Implantando o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14396-124">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)

<span data-ttu-id="14396-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14396-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

