---
title: 'Lync Server 2013: Reverter usuários migrados'
description: 'Lync Server 2013: reverter usuários migrados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Roll back migrated users
ms:assetid: bfabaf0b-9a42-4057-b729-a7ab9eee8c72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205224(v=OCS.15)
ms:contentKeyID: 48185286
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c5993bfd530c84307d3ee5be627b3ed33814be73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442338"
---
# <a name="roll-back-migrated-users-in-lync-server-2013"></a><span data-ttu-id="b6421-103">Reverter usuários migrados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6421-103">Roll back migrated users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6421-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6421-104">

<span> </span></span></span>

<span data-ttu-id="b6421-105">_**Tópico da última modificação:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="b6421-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="b6421-106">Se você precisar reverter o recurso de repositório de contatos unificado, reverta os contatos apenas se mover o usuário de volta para o Exchange 2010 ou o Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b6421-106">If you need to roll back the unified contact store feature, roll back the contacts only if you move the user back to Exchange 2010 or Lync Server 2010.</span></span> <span data-ttu-id="b6421-107">Para reverter, desabilite a política do usuário e execute o cmdlet **Invoke-CsUcsRollback**.</span><span class="sxs-lookup"><span data-stu-id="b6421-107">To roll back, disable the policy for the user, and then run the **Invoke-CsUcsRollback** cmdlet.</span></span> <span data-ttu-id="b6421-108">Apenas executar o **Invoke-CsUcsRollback** não é suficiente para garantir uma reversão permanente, porque a migração do repositório de contato unificado será iniciada novamente se a política não estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b6421-108">Just running **Invoke-CsUcsRollback** alone is not enough to ensure permanent rollback, because unified contact store migration will be initiated again if the policy is not disabled.</span></span> <span data-ttu-id="b6421-109">Por exemplo, se um usuário for revertido porque o Exchange 2013 é revertido para o Exchange 2010, e a caixa de correio do usuário é movida para o Exchange 2013, a migração do repositório de contatos unificado será iniciada novamente sete dias após a reversão, desde que o repositório de contatos unificado ainda esteja habilitado para o usuário na política de serviços de usuário.</span><span class="sxs-lookup"><span data-stu-id="b6421-109">For example, if a user is rolled back because Exchange 2013 is rolled back to Exchange 2010, and then the user’s mailbox is moved to Exchange 2013, the unified contact store migration will be initiated again seven days after the rollback, as long as unified contact store is still enabled for the user in the user services policy.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b6421-110">O cmdlet <STRONG>move-CsUser</STRONG> retorna automaticamente a loja de contatos do usuário do Exchange 2013 para o Lync Server 2013 nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="b6421-110">The <STRONG>Move-CsUser</STRONG> cmdlet automatically rolls back the user's contact store from Exchange 2013 to Lync Server 2013 in the following situations:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="b6421-111">Quando os usuários forem movidos do Lync Server 2013 para o Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b6421-111">When users are moved from Lync Server 2013 to Lync Server 2010.</span></span></P>
> <LI>
> <P><span data-ttu-id="b6421-112">Quando os usuários são migrados de forma cruzada, como quando um usuário é movido do Lync Online para o Lync Server 2013 local ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="b6421-112">When users are migrated cross premises, such as when a user is moved from Lync Online to Lync Server 2013 on-premises, or vice versa.</span></span></P></LI></UL>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b6421-p102">Importar os dados do repositório de contato unificado de um banco de dados de backup pode fazer com que os dados do repositório de contato unificado e os dados do usuário sejam corrompidos se o modo do repositório de contato unificado mudar entre a exportação e a importação. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b6421-p102">Importing unified contact store data from a backup database can cause unified contact store data and user data to become corrupted if the unified contact store mode changed between the export and the import. For example:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="b6421-115">Se você exportar listas de contatos antes de os contatos dos usuários serem migrados para o Exchange 2013 e depois, após a migração, importar os mesmos dados, os dados do repositório de contatos unificado e as listas de contatos serão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="b6421-115">If you export contact lists before the users' contacts are migrated to Exchange 2013 and then, after the migration, import the same data, the unified contact store data and contact lists will be corrupted.</span></span></P>
> <LI>
> <P><span data-ttu-id="b6421-116">Se você exportar UserData depois de migrar os usuários para o Exchange 2013, reverta a migração e, por algum motivo, importar os dados após a migração, os dados do repositório de contatos unificado e as listas de contatos serão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="b6421-116">If you export userdata after you migrate users to Exchange 2013, roll back the migration, and then for some reason you import the data from after the migration, the unified contact store data and contact lists will be corrupted.</span></span></P></LI></UL>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b6421-117">Antes de mover uma caixa de correio do Exchange do Exchange 2013 para o Exchange 2010, o administrador do Exchange deve certificar-se de que o administrador do Lync Server primeiro reverteu os contatos do usuário do servidor do Lync do Exchange 2013 para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b6421-117">Before you move an Exchange mailbox from Exchange 2013 to Exchange 2010, the Exchange administrator must make sure that the Lync Server administrator has first rolled back the Lync Server user contacts from Exchange 2013 to Lync Server.</span></span> <span data-ttu-id="b6421-118">Para reverter contatos do repositório de contatos unificados para o Lync Server, consulte procedimento "para reverter contatos do repositório de contatos unificados do Exchange 2013 para o Lync Server 2013", posteriormente nesta seção.</span><span class="sxs-lookup"><span data-stu-id="b6421-118">To roll back unified contact store contacts to Lync Server, see procedure "To roll back unified contact store contacts from Exchange 2013 to Lync Server 2013," later in this section.</span></span>



</div>

<span data-ttu-id="b6421-119">O seguinte procedimento descreve como reverter contatos do usuário.</span><span class="sxs-lookup"><span data-stu-id="b6421-119">The following procedure describes how to roll back user contacts.</span></span> <span data-ttu-id="b6421-120">Se você usar o cmdlet **move-CsUser** para mover os usuários entre o lync Server 2013 e o lync Server 2010, poderá ignorar essas etapas porque o cmdlet **move-CsUser** é revertido automaticamente unifed o repositório de contatos quando ele move os usuários do Lync Server 2013 para o Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="b6421-120">If you use the **Move-CsUser** cmdlet to move users between Lync Server 2013 and Lync Server 2010, you can skip these steps because the **Move-CsUser** cmdlet automatically rolls back unifed contact store when it moves users from Lync Server 2013 to Lync Server 2010.</span></span> <span data-ttu-id="b6421-121">**Move-CsUser** não desabilita a política de repositório de contatos unificado, portanto, a migração para o repositório de contatos unificado será recorrente se o usuário for movido de volta para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b6421-121">**Move-CsUser** does not disable unified contact store policy, so the migration to unified contact store will recur if the user is moved back to Lync Server 2013.</span></span>

<div>

## <a name="to-roll-back-user-contacts-from-lync-server-2013-to-lync-server-2010"></a><span data-ttu-id="b6421-122">Para reverter contatos do usuário do Lync Server 2013 para o Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="b6421-122">To roll back user contacts from Lync Server 2013 to Lync Server 2010</span></span>

1.  <span data-ttu-id="b6421-123">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b6421-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="b6421-124">Desabilite o repositório de contatos unificado para que os usuários sejam revertidos para que eles não sejam migrados novamente após a reversão.</span><span class="sxs-lookup"><span data-stu-id="b6421-124">Disable unified contact store for the users to be rolled back so that they will not be remigrated after rollback.</span></span> <span data-ttu-id="b6421-125">(Execute esta etapa somente se desejar garantir que os usuários não serão remigrados no futuro.) Para desabilitar o repositório de contatos unificado para usuários individuais, na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="b6421-125">(Perform this step only if you want to make sure that users will not remigrate in the future.) To disable unified contact store for individual users, at the command line, type:</span></span>
    
        Set-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $False
    
    <span data-ttu-id="b6421-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b6421-126">For example:</span></span>
    
        Set-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $False

3.  <span data-ttu-id="b6421-127">Antes de mover um usuário do Lync Server 2013 para o Lync Server 2010, reverta a lista de amigos dos usuários especificados no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b6421-127">Before moving a user from Lync Server 2013 to Lync Server 2010, roll back the Buddy List for the specified users on Lync Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b6421-128">Se essa etapa for omitida, a lista de amigos será perdida.</span><span class="sxs-lookup"><span data-stu-id="b6421-128">If this step is omitted, the Buddy List will be lost.</span></span>

    
    </div>

4.  <span data-ttu-id="b6421-129">Reverter os usuários especificados.</span><span class="sxs-lookup"><span data-stu-id="b6421-129">Roll back the specified users.</span></span> <span data-ttu-id="b6421-130">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="b6421-130">At the command line, type:</span></span>
    
        Invoke-CsUcsRollback -Identity "<user display name>"
    
    <span data-ttu-id="b6421-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b6421-131">For example:</span></span>
    
        Invoke-CsUcsRollback -Identity "Ken Myer"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b6421-132">Não recomendamos usar a opção – Force para forçar a reversão.</span><span class="sxs-lookup"><span data-stu-id="b6421-132">We do not recommend using the –Force option to force the rollback.</span></span> <span data-ttu-id="b6421-133">Se você usar essa opção, os contatos dos usuários serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="b6421-133">If you use this option, the users' contacts will be lost.</span></span>

    
    </div>

</div>

<div>

## <a name="to-roll-back-unified-contact-store-contacts-from-exchange-2013-to-lync-server-2013"></a><span data-ttu-id="b6421-134">Para reverter os contatos do repositório de contatos unificado do Exchange 2013 para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6421-134">To roll back unified contact store contacts from Exchange 2013 to Lync Server 2013</span></span>

1.  <span data-ttu-id="b6421-135">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b6421-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="b6421-136">Desabilite o repositório de contatos unificado para que os usuários sejam revertidos para que eles não sejam migrados novamente após a reversão.</span><span class="sxs-lookup"><span data-stu-id="b6421-136">Disable unified contact store for the users to be rolled back so that they will not be remigrated after rollback.</span></span> <span data-ttu-id="b6421-137">Para desabilitar o repositório de contatos unificado para usuários individuais, na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="b6421-137">To disable unified contact store for individual users, at the command line, type:</span></span>
    
        Set-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $False
    
    <span data-ttu-id="b6421-138">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b6421-138">For example:</span></span>
    
        Set-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $False

3.  <span data-ttu-id="b6421-139">Reverter os usuários especificados.</span><span class="sxs-lookup"><span data-stu-id="b6421-139">Roll back the specified users.</span></span> <span data-ttu-id="b6421-140">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="b6421-140">At the command line, type:</span></span>
    
        Invoke-CsUcsRollback -Identity "<user display name>"
    
    <span data-ttu-id="b6421-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b6421-141">For example:</span></span>
    
        Invoke-CsUcsRollback -Identity "Ken Myer"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b6421-142">Primeiro, você deve reverter o usuário do Lync Server e, em seguida, mover a caixa de correio do Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="b6421-142">You must first roll back the Lync Server user, and then move the Exchange 2013 mailbox.</span></span> <span data-ttu-id="b6421-143">O administrador do Exchange está bloqueado para reverter o Exchange até que a reversão do Lync Server seja concluída.</span><span class="sxs-lookup"><span data-stu-id="b6421-143">The Exchange administrator is blocked from rolling back Exchange until the Lync Server rollback is complete.</span></span> <span data-ttu-id="b6421-144">Não recomendamos usar a opção – Force para forçar a reversão.</span><span class="sxs-lookup"><span data-stu-id="b6421-144">We do not recommend using the –Force option to force the rollback.</span></span> <span data-ttu-id="b6421-145">Se você usar essa opção, os contatos dos usuários serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="b6421-145">If you use this option, the users' contacts will be lost.</span></span>

    
    </div>

4.  <span data-ttu-id="b6421-146">Depois de reverter o usuário para o Lync Server, o administrador do Exchange pode reverter o usuário do Exchange do Exchange 2013 para o Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="b6421-146">After you roll back the user to Lync Server, the Exchange administrator can roll back the Exchange user from Exchange 2013 to Exchange 2010.</span></span>

<span data-ttu-id="b6421-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6421-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

