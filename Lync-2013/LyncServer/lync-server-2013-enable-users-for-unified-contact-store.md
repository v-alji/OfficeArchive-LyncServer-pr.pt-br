---
title: 'Lync Server 2013: Habilitar usuários para repositório unificado de contatos'
description: 'Lync Server 2013: habilitar usuários para repositório de contatos unificado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for unified contact store
ms:assetid: 7b46a01f-beb5-4a33-adb0-35f0502b168d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205024(v=OCS.15)
ms:contentKeyID: 48184599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2249249d314e13d840b276e46f1fe38ad271664a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428815"
---
# <a name="enable-users-for-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="cf0d3-103">Habilitar usuários para repositório unificado de contatos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf0d3-103">Enable users for unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf0d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf0d3-104">

<span> </span></span></span>

<span data-ttu-id="cf0d3-105">_**Tópico da última modificação:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="cf0d3-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="cf0d3-106">Quando você implanta o Lync Server 2013 e publica a topologia, o repositório de contatos unificado é habilitado para todos os usuários por padrão.</span><span class="sxs-lookup"><span data-stu-id="cf0d3-106">When you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="cf0d3-107">Você não precisa executar nenhuma ação adicional para habilitar o repositório de contatos unificado após a implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf0d3-107">You do not need to take any additional action to enable unified contact store after you deploy Lync Server 2013.</span></span> <span data-ttu-id="cf0d3-108">Contudo, você pode usar o cmdlet **Set-CsUserServicesPolicy** para definir quais usuários têm o repositório unificado de contatos disponível.</span><span class="sxs-lookup"><span data-stu-id="cf0d3-108">However, you can use the **Set-CsUserServicesPolicy** cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="cf0d3-109">Você pode habilitar esse recurso globalmente, por local, por locatário ou por indivíduos ou grupos de indivíduos.</span><span class="sxs-lookup"><span data-stu-id="cf0d3-109">You can enable this feature globally, by site, by tenant, or by individuals or groups of individuals.</span></span>

<div>

## <a name="to-enable-users-for-unified-contact-store"></a><span data-ttu-id="cf0d3-110">Para permitir o repositório unificado de contatos</span><span class="sxs-lookup"><span data-stu-id="cf0d3-110">To enable users for unified contact store</span></span>

1.  <span data-ttu-id="cf0d3-111">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="cf0d3-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="cf0d3-112">Execute qualquer uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-112">Do any of the following:</span></span>
    
      - <span data-ttu-id="cf0d3-113">Para habilitar o repositório de contatos unificado globalmente para todos os usuários do Lync Server, na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-113">To enable unified contact store globally for all Lync Server users, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Identity global -UcsAllowed $True
    
      - <span data-ttu-id="cf0d3-114">Para habilitar o repositório de contatos unificado para os usuários em um site específico, digite o seguinte na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-114">To enable unified contact store for the users at a specific site, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity site:<site name> -UcsAllowed $True
        
        <span data-ttu-id="cf0d3-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-115">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity site:Redmond -UcsAllowed $True
    
      - <span data-ttu-id="cf0d3-116">Para habilitar o repositório de contatos unificado por locatário, na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-116">To enable unified contact store by tenant, at the command line, type:</span></span>
        
            Set-CsUserServicesPolicy -Tenant <tenantId> -UcsAllowed $True
        
        <span data-ttu-id="cf0d3-117">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-117">For example:</span></span>
        
            Set-CsUserServicesPolicy -Tenant "38aad667-af54-4397-aaa7-e94c79ec2308" -UcsAllowed $True
    
      - <span data-ttu-id="cf0d3-118">Para habilitar o repositório de contatos unificado para usuários específicos, na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-118">To enable unified contact store for specific users, at the command line, type:</span></span>
        
            New-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "<user display name>" -PolicyName <"policy name">
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="cf0d3-119">Você também pode alterar o URI do SIP ou o usuário remoto em vez do nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="cf0d3-119">You can also use user alias or SIP URI instead of the user display name.</span></span>

        
        </div>
        
        <span data-ttu-id="cf0d3-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="cf0d3-120">For example:</span></span>
        
            New-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $True
            Grant-CsUserServicesPolicy -Identity "Ken Myer" -PolicyName "UCS Enabled Users"
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="cf0d3-p102">No exemplo anterior, o primeiro comando cria uma nova política por usuário chamada <EM>Usuários do UCS Permitidos</EM>, com o sinalizador AcsAllowed definido como True. O segundo comando atribui a política ao usuário com o nome Ken Myer, o que significa que Ken Myer está habilitado para o repositório unificado de contatos.</span><span class="sxs-lookup"><span data-stu-id="cf0d3-p102">In the preceding example, the first command creates a new per-user policy named <EM>UCS Enabled Users</EM> with the UcsAllowed flag set to True. The second command assigns the policy to the user with the display name Ken Myer, which means that Ken Myer is now enabled for unified contact store.</span></span>

        
        <span data-ttu-id="cf0d3-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf0d3-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

