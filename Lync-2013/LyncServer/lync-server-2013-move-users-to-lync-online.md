---
title: 'Lync Server 2013: mover usuários para o Lync Online'
description: 'Lync Server 2013: mover usuários para o Lync Online.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move users to Lync Online
ms:assetid: 6a523c86-2eac-4fa4-973a-4406872c9a7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204969(v=OCS.15)
ms:contentKeyID: 48184392
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 501eda3a76cec3226831c0af3631317377cd82cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425273"
---
# <a name="move-users-to-lync-online-in-lync-server-2013"></a><span data-ttu-id="5c3f1-103">Mover usuários para o Lync Online no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c3f1-103">Move users to Lync Online in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c3f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c3f1-104">

<span> </span></span></span>

<span data-ttu-id="5c3f1-105">_**Tópico da última modificação:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="5c3f1-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="5c3f1-106">Antes de começar a migrar usuários para o Lync Online, você deve fazer backup dos dados do usuário associados às contas a serem movidas.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-106">Before you start migrating users to Lync Online, you should backup the user data associated with the accounts to be moved.</span></span> <span data-ttu-id="5c3f1-107">Nem todos os dados de usuário são movidos junto com a conta.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-107">Not all user data is moved with the user account.</span></span> <span data-ttu-id="5c3f1-108">Para obter informações, consulte [requisitos de backup e restauração no Lync Server 2013: dados](lync-server-2013-backup-and-restoration-requirements-data.md).</span><span class="sxs-lookup"><span data-stu-id="5c3f1-108">For information, see [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md).</span></span>

<div>

## <a name="migrate-user-settings-to-lync-online"></a><span data-ttu-id="5c3f1-109">Migrar configurações de usuário para o Lync Online</span><span class="sxs-lookup"><span data-stu-id="5c3f1-109">Migrate User Settings to Lync Online</span></span>

<span data-ttu-id="5c3f1-110">As configurações do usuário são movidas com a conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-110">User settings are moved with the user account.</span></span> <span data-ttu-id="5c3f1-111">Algumas configurações locais não são movidas com a conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-111">Some on-premises settings are not moved with the user account.</span></span>

</div>

<div>

## <a name="moving-pilot-users-to-lync-online"></a><span data-ttu-id="5c3f1-112">Movendo usuários piloto para o Lync Online</span><span class="sxs-lookup"><span data-stu-id="5c3f1-112">Moving Pilot Users to Lync Online</span></span>

<span data-ttu-id="5c3f1-113">Antes de começar a mover usuários para o Lync Online, talvez você queira mover alguns usuários piloto para confirmar se o seu ambiente está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-113">Before you begin to move users to Lync Online, you may want to move a few pilot users to confirm that your environment is correctly configured.</span></span> <span data-ttu-id="5c3f1-114">Em seguida, você pode verificar se os recursos e serviços do Lync funcionam como esperado antes de tentar mover usuários adicionais.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-114">You can then verify that Lync features and services function as expected before attempting to move additional users.</span></span>

<span data-ttu-id="5c3f1-115">Para mover um usuário local para o seu locatário do Lync Online, execute os seguintes cmdlets no Shell de gerenciamento do Lync Server, usando as credenciais de administrador da sua organização do Microsoft 365 ou do Office 365.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-115">To move an on-premises user to your Lync Online tenant, run the following cmdlets in the Lync Server Management Shell, using the administrator credentials for your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="5c3f1-116">Substitua "username@contoso.com" pela informação do usuário que você deseja mover.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-116">Replace "username@contoso.com" with the information for the user that you want to move.</span></span>

   ```PowerShell
    $creds=Get-Credential
   ```

   ```PowerShell
    Move-CsUser -Identity username@contoso.com -Target sipfed.online.lync.com -Credential $creds -HostedMigrationOverrideUrl <URL>
   ```

<span data-ttu-id="5c3f1-117">O formato da URL especificada para o parâmetro **HostedMigrationOverrideUrl** deve ser a URL do pool em que o serviço de migração hospedada está em execução, no seguinte formato: https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-117">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format: Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc.</span></span>

<span data-ttu-id="5c3f1-118">Você pode determinar a URL do serviço de migração hospedada visualizando a URL do painel de controle do Lync Online para sua conta da organização do Microsoft 365 ou do Office 365.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-118">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>

<span data-ttu-id="5c3f1-119">**Para determinar a URL do serviço de migração hospedada para sua organização**</span><span class="sxs-lookup"><span data-stu-id="5c3f1-119">**To determine the Hosted Migration Service URL for your organization**</span></span>

1.  <span data-ttu-id="5c3f1-120">Conecte-se à sua organização do Microsoft 365 ou do Office 365 como administrador.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-120">Login to your Microsoft 365 or Office 365 organization as an administrator.</span></span>

2.  <span data-ttu-id="5c3f1-121">Abra o **centro de administração do Lync**.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-121">Open the **Lync admin center**.</span></span>

3.  <span data-ttu-id="5c3f1-122">Com o **centro de administração do Lync** exibido, selecione e copie a URL na barra de endereços até **Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-122">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="5c3f1-123">Uma URL de exemplo seria parecida com esta:</span><span class="sxs-lookup"><span data-stu-id="5c3f1-123">An example URL looks similar to the following:</span></span>
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  <span data-ttu-id="5c3f1-124">Substitua **webdir** na URL por **admin**, o que resulta no seguinte:</span><span class="sxs-lookup"><span data-stu-id="5c3f1-124">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
    
    `https://admin0a.online.lync.com`

5.  <span data-ttu-id="5c3f1-125">Anexe a cadeia de caracteres a seguir à URL: **/HostedMigration/hostedmigrationservice.svc**.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-125">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
    
    <span data-ttu-id="5c3f1-126">A URL resultante, que tem o valor de **HostedMigrationOverrideUrl**, deverá ser parecida com esta:</span><span class="sxs-lookup"><span data-stu-id="5c3f1-126">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

</div>

<div>

## <a name="moving-users-to-lync-online"></a><span data-ttu-id="5c3f1-127">Mover usuários para o Lync Online</span><span class="sxs-lookup"><span data-stu-id="5c3f1-127">Moving Users to Lync Online</span></span>

<span data-ttu-id="5c3f1-128">Você pode mover vários usuários usando o cmdlet [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) com o parâmetro – Filter para selecionar os usuários com uma propriedade específica atribuída às contas de usuário, como RegistrarPool.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-128">You can move multiple users by using the [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) cmdlet with the –Filter parameter to select the users with a specific property assigned to the user accounts, such as RegistrarPool.</span></span> <span data-ttu-id="5c3f1-129">Em seguida, você pode canalizar os usuários retornados para o cmdlet [move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-129">You can then pipe the returned users to the [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) cmdlet, as shown in the following example.</span></span>

    Get-CsUser -Filter {UserProperty -eq "UserPropertyValue"} | Move-CsUser -Target sipfed.online.lync.com -Credential $creds -HostedMigrationOverrideUrl <URL>

<span data-ttu-id="5c3f1-130">Você também pode usar o parâmetro -OU para recuperar todos os usuários no OU especificado, como mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-130">You can also use the –OU parameter to retrieve all users in the specified OU, as shown in the following example.</span></span>

    Get-CsUser -OU "cn=hybridusers,cn=contoso.." | Move-CsUser -Target sipfed.online.lync.com -Credentials $creds -HostedMigrationOverrideUrl <URL>

</div>

<div>

## <a name="verify-lync-online-user-settings-and-features"></a><span data-ttu-id="5c3f1-131">Verificar as configurações e os recursos do usuário do Lync Online</span><span class="sxs-lookup"><span data-stu-id="5c3f1-131">Verify Lync Online User Settings and Features</span></span>

<span data-ttu-id="5c3f1-132">Você pode verificar que o usuário foi movido com sucesso das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="5c3f1-132">You can verify that the user was moved successfully in the following ways:</span></span>

  - <span data-ttu-id="5c3f1-133">Exiba o status do usuário no painel de controle do Lync Online.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-133">View the status of the user in the Lync Online Control Panel.</span></span> <span data-ttu-id="5c3f1-134">O indicador visual para usuários no local e online é diferente.</span><span class="sxs-lookup"><span data-stu-id="5c3f1-134">The visual indicator for on-premises users and online users is different.</span></span>

  - <span data-ttu-id="5c3f1-135">Execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3f1-135">Run the following cmdlet:</span></span>
    
        Get-CsUser -Identity

<span data-ttu-id="5c3f1-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c3f1-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

