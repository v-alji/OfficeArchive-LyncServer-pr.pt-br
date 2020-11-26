---
title: 'Lync Server 2013: Concedendo permissões de unidade organizacional'
description: 'Lync Server 2013: concedendo permissões de unidade organizacional.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting organizational unit permissions
ms:assetid: 95ee5ffa-39b1-4d80-87a2-27bb364f7396
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398763(v=OCS.15)
ms:contentKeyID: 48184849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47ad862241e409190620afa7dbf4fa73adf339de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427891"
---
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a><span data-ttu-id="4c750-103">Concedendo permissões de unidade organizacional no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c750-103">Granting organizational unit permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c750-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c750-104">

<span> </span></span></span>

<span data-ttu-id="4c750-105">_**Tópico da última modificação:** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="4c750-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="4c750-106">Você pode usar o cmdlet **Grant-CsOuPermission** para conceder permissões a objetos em unidades organizacionais (UOs) especificadas para que os membros dos grupos universais do RTC criados pela preparação da floresta possam acessá-los sem serem membros do grupo Domain admins.</span><span class="sxs-lookup"><span data-stu-id="4c750-106">You can use the **Grant-CsOuPermission** cmdlet to grant permissions to objects in specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access them without being members of the Domain Admins group.</span></span> <span data-ttu-id="4c750-107">As permissões adicionadas à UO especificada são as mesmas permissões que o cmdlet **Enable-CsAdDomain** adiciona aos recipientes computadores e usuários durante a preparação do domínio.</span><span class="sxs-lookup"><span data-stu-id="4c750-107">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users containers during domain preparation.</span></span>

<span data-ttu-id="4c750-108">Use o cmdlet **Test-CsOuPermission** para verificar as permissões configuradas usando o cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="4c750-108">Use the **Test-CsOuPermission** cmdlet to verify the permissions you set up by using the **Grant-CsOuPermission** cmdlet.</span></span>

<span data-ttu-id="4c750-109">Você pode usar o cmdlet **REVOKE-CsOuPermission** para remover permissões concedidas usando o cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="4c750-109">You can use the **Revoke-CsOuPermission** cmdlet to remove permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-ou-permissions"></a><span data-ttu-id="4c750-110">Para conceder permissões de OU</span><span class="sxs-lookup"><span data-stu-id="4c750-110">To grant OU permissions</span></span>

1.  <span data-ttu-id="4c750-111">Faça logon em um computador que esteja executando o Lync Server 2013 no domínio em que você deseja conceder permissões de OU.</span><span class="sxs-lookup"><span data-stu-id="4c750-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant OU permissions.</span></span> <span data-ttu-id="4c750-112">Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.</span><span class="sxs-lookup"><span data-stu-id="4c750-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="4c750-113">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="4c750-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="4c750-114">Execute:</span><span class="sxs-lookup"><span data-stu-id="4c750-114">Run:</span></span>
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="4c750-115">Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="4c750-115">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-ou-permissions"></a><span data-ttu-id="4c750-116">Para verificar permissões de OU</span><span class="sxs-lookup"><span data-stu-id="4c750-116">To verify OU permissions</span></span>

1.  <span data-ttu-id="4c750-117">Faça logon em um computador que esteja executando o Lync Server 2013 no domínio em que você deseja verificar as permissões de OU que você concedeu usando o cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="4c750-117">Log on to a computer running Lync Server 2013 in the domain where you want to verify OU permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="4c750-118">Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.</span><span class="sxs-lookup"><span data-stu-id="4c750-118">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="4c750-119">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="4c750-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="4c750-120">Execute:</span><span class="sxs-lookup"><span data-stu-id="4c750-120">Run:</span></span>
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="4c750-121">Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="4c750-121">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-ou-permissions"></a><span data-ttu-id="4c750-122">Para revogar permissões de OU</span><span class="sxs-lookup"><span data-stu-id="4c750-122">To revoke OU permissions</span></span>

1.  <span data-ttu-id="4c750-123">Faça logon em um computador que esteja executando o Lync Server 2013 no domínio em que você deseja revogar permissões de OU que foram concedidas pelo cmdlet **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="4c750-123">Log on to a computer running Lync Server 2013 in the domain where you want to revoke OU permissions that were granted by the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="4c750-124">Use uma conta que seja membro do grupo Domain admins ou do grupo Administradores de empresa se a UO estiver em um domínio filho diferente.</span><span class="sxs-lookup"><span data-stu-id="4c750-124">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="4c750-125">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="4c750-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="4c750-126">Execute:</span><span class="sxs-lookup"><span data-stu-id="4c750-126">Run:</span></span>
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="4c750-127">Se você não especificar o parâmetro Domain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="4c750-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="4c750-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c750-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

