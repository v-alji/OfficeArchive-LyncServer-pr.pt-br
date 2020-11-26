---
title: 'Lync Server 2013: Concedendo permissões de configuração'
description: 'Lync Server 2013: concedendo permissões de instalação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting setup permissions
ms:assetid: 15982bfe-6844-44f6-815a-72dcaf0e4d21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398225(v=OCS.15)
ms:contentKeyID: 48183491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5523494219d07907caeefc1bd139c41856effa54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427892"
---
# <a name="granting-setup-permissions-in-lync-server-2013"></a><span data-ttu-id="c36e4-103">Concedendo permissões de configuração no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c36e4-103">Granting setup permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c36e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c36e4-104">

<span> </span></span></span>

<span data-ttu-id="c36e4-105">_**Tópico da última modificação:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="c36e4-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="c36e4-106">Você pode usar o cmdlet **Grant-CsSetupPermission** para adicionar permissões de leitura, gravação, ReadSPN e WriteSPN ao grupo RTCUniversalServerAdmins para uma unidade organizacional (ou) especificada do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c36e4-106">You can use the **Grant-CsSetupPermission** cmdlet to add Read, Write, ReadSPN, and WriteSPN permissions to the RTCUniversalServerAdmins group for a specified Active Directory organizational unit (OU).</span></span> <span data-ttu-id="c36e4-107">Em seguida, os membros do grupo RTCUniversalServerAdmins nessa UO podem instalar servidores que executam o Lync Server 2013 no domínio especificado sem serem membros do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="c36e4-107">Then members of the RTCUniversalServerAdmins group in that OU can install servers running Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="c36e4-108">Use o cmdlet **Test-CsSetupPermission** para verificar as permissões configuradas usando o cmdlet **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="c36e4-108">Use the **Test-CsSetupPermission** cmdlet to verify the permissions you set up by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<span data-ttu-id="c36e4-109">Você pode usar o cmdlet **REVOKE-CsSetupPermission** para remover permissões concedidas usando o cmdlet **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="c36e4-109">You can use the **Revoke-CsSetupPermission** cmdlet to remove permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-setup-permissions"></a><span data-ttu-id="c36e4-110">Para conceder permissões de configuração</span><span class="sxs-lookup"><span data-stu-id="c36e4-110">To grant setup permissions</span></span>

1.  <span data-ttu-id="c36e4-111">Faça logon em um computador que esteja executando o Lync Server 2013 no domínio onde você deseja conceder permissões de configuração.</span><span class="sxs-lookup"><span data-stu-id="c36e4-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant setup permissions.</span></span> <span data-ttu-id="c36e4-112">Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.</span><span class="sxs-lookup"><span data-stu-id="c36e4-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="c36e4-113">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="c36e4-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c36e4-114">Execute:</span><span class="sxs-lookup"><span data-stu-id="c36e4-114">Run:</span></span>
    
        Grant-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="c36e4-115">Você pode especificar o parâmetro ComputerOu como relativo ao contexto de nomenclatura padrão do domínio especificado (por exemplo, CN = computadores).</span><span class="sxs-lookup"><span data-stu-id="c36e4-115">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="c36e4-116">Você também pode especificar esse parâmetro como o nome diferenciado (DN) completo da OU (por exemplo, "CN = computadores, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="c36e4-116">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="c36e4-117">Nesse caso, você deve especificar um DN de OU consistente com o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="c36e4-117">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="c36e4-118">Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="c36e4-118">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-setup-permissions"></a><span data-ttu-id="c36e4-119">Para verificar as permissões de configuração</span><span class="sxs-lookup"><span data-stu-id="c36e4-119">To verify setup permissions</span></span>

1.  <span data-ttu-id="c36e4-120">Faça logon em um computador que esteja executando o Lync Server 2013 no domínio em que você deseja verificar as permissões de configuração concedidas usando o cmdlet **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="c36e4-120">Log on to a computer running Lync Server 2013 in the domain where you want to verify setup permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="c36e4-121">Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.</span><span class="sxs-lookup"><span data-stu-id="c36e4-121">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="c36e4-122">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="c36e4-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c36e4-123">Execute:</span><span class="sxs-lookup"><span data-stu-id="c36e4-123">Run:</span></span>
    
        Test-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="c36e4-124">Você pode especificar o parâmetro ComputerOu como relativo ao contexto de nomenclatura padrão do domínio especificado (por exemplo, CN = computadores).</span><span class="sxs-lookup"><span data-stu-id="c36e4-124">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="c36e4-125">Você também pode especificar esse parâmetro como o nome diferenciado (DN) completo da OU (por exemplo, "CN = computadores, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="c36e4-125">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="c36e4-126">Nesse caso, você deve especificar um DN de OU consistente com o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="c36e4-126">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="c36e4-127">Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="c36e4-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-setup-permissions"></a><span data-ttu-id="c36e4-128">Para revogar permissões de configuração</span><span class="sxs-lookup"><span data-stu-id="c36e4-128">To revoke setup permissions</span></span>

1.  <span data-ttu-id="c36e4-129">Faça logon em um computador que esteja executando o Lync Server 2013 no domínio onde você deseja revogar as permissões de configuração que foram concedidas pelo cmdlet **Grant-CsSetupPermission** .</span><span class="sxs-lookup"><span data-stu-id="c36e4-129">Log on to a computer running Lync Server 2013 in the domain where you want to revoke setup permissions that were granted by the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="c36e4-130">Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.</span><span class="sxs-lookup"><span data-stu-id="c36e4-130">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="c36e4-131">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="c36e4-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c36e4-132">Execute:</span><span class="sxs-lookup"><span data-stu-id="c36e4-132">Run:</span></span>
    
        Revoke-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="c36e4-133">Você pode especificar o parâmetro ComputerOu como relativo ao contexto de nomenclatura padrão do domínio especificado (por exemplo, CN = computadores).</span><span class="sxs-lookup"><span data-stu-id="c36e4-133">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="c36e4-134">Você também pode especificar esse parâmetro como o nome diferenciado (DN) completo da OU (por exemplo, "CN = computadores, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="c36e4-134">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="c36e4-135">Nesse caso, você deve especificar um DN de OU consistente com o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="c36e4-135">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="c36e4-136">Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="c36e4-136">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="c36e4-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c36e4-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

