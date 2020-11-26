---
title: Excluir uma coleção existente de definições de configuração do Lync Phone Edition
description: Exclua uma coleção existente das configurações do Lync Phone Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of Lync Phone Edition configuration settings
ms:assetid: 1bfc427d-4dcd-4199-b25f-8d5cfec2164f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687984(v=OCS.15)
ms:contentKeyID: 49733574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5137590a37b8bbb47f7445d20639157953597ca6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430550"
---
# <a name="delete-an-existing-collection-of-lync-phone-edition-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="15578-103">Excluir uma coleção existente de definições de configuração do Lync Phone Edition no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15578-103">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15578-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15578-104">

<span> </span></span></span>

<span data-ttu-id="15578-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="15578-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="15578-106">Se você não quiser mais usar um conjunto de configurações para dispositivos que executam o Lync Phone Edition, exclua-o.</span><span class="sxs-lookup"><span data-stu-id="15578-106">If you no longer want to use a collection of settings for devices running Lync Phone Edition, delete it.</span></span> <span data-ttu-id="15578-107">Se você excluir uma coleção de um site, as configurações globais serão aplicadas aos telefones desse site.</span><span class="sxs-lookup"><span data-stu-id="15578-107">If you delete a collection for a site, the global settings will apply to the phones in that site.</span></span> <span data-ttu-id="15578-108">Não é possível excluir a coleção global.</span><span class="sxs-lookup"><span data-stu-id="15578-108">You cannot delete the global collection.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="15578-109">Em vez de excluir uma coleção, talvez você queira apenas alterar algumas das configurações.</span><span class="sxs-lookup"><span data-stu-id="15578-109">Instead of deleting a collection, you might just want to change some of the settings.</span></span> <span data-ttu-id="15578-110">Para obter detalhes sobre como fazer isso, consulte <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">criar ou modificar um conjunto de configurações do Lync Phone Edition no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="15578-110">For details about how to do so, see <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-delete-a-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="15578-111">Para excluir uma coleção de definições de configuração do Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="15578-111">To delete a collection of Lync Phone Edition configuration settings</span></span>

1.  <span data-ttu-id="15578-112">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="15578-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="15578-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="15578-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="15578-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="15578-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="15578-115">Na barra de navegação à esquerda, clique em **clientes** e, em seguida, clique no botão de navegação **configuração de dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="15578-115">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="15578-116">Na página **configuração de dispositivo** , clique na coleção que você deseja excluir, clique no menu **Editar** e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="15578-116">On the **Device Configuration** page, click the collection you want to delete, click the **Edit** menu, and then click **Delete**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="15578-117">Se você excluir a coleção global, as configurações apenas reverterão para as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="15578-117">If you delete the global collection, the settings just revert to the default settings.</span></span> <span data-ttu-id="15578-118">A coleção não desaparece.</span><span class="sxs-lookup"><span data-stu-id="15578-118">The collection does not go away.</span></span>

    
    </div>

5.  <span data-ttu-id="15578-119">Na caixa de confirmação, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="15578-119">In the confirmation box, click **OK**.</span></span>

</div>

<div>

## <a name="removing-lync-phone-edition-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="15578-120">Como remover as configurações de configuração do Lync Phone Edition usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="15578-120">Removing Lync Phone Edition Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="15578-121">Você pode excluir as configurações de configuração do Lync Phone Edition usando o Windows PowerShell e o cmdlet **Remove-CsUCConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="15578-121">You can delete Lync Phone Edition configuration settings by using Windows PowerShell and the **Remove-CsUCConfiguration** cmdlet.</span></span> <span data-ttu-id="15578-122">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15578-122">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="15578-123">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="15578-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="15578-124">Para remover uma coleção especificada de definições de configuração do Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="15578-124">To remove a specified collection of Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="15578-125">Esse comando exclui as definições de configuração de telefone UC aplicadas ao site Redmond:</span><span class="sxs-lookup"><span data-stu-id="15578-125">This command deletes the UC phone configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsUCPhoneConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="15578-126">Para remover todas as configurações de configuração do Lync Phone Edition aplicadas ao escopo do site</span><span class="sxs-lookup"><span data-stu-id="15578-126">To remove all of the Lync Phone Edition configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="15578-127">Esse comando Remove todas as definições de configuração de telefone UC aplicadas ao escopo do serviço:</span><span class="sxs-lookup"><span data-stu-id="15578-127">This command removes all the UC phone configuration settings applied to the service scope:</span></span>
    
        Get-CsUCPhoneConfiguration -Filter "site:*" | Remove-CsUCPhoneConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-where-phone-locking-is-disabled"></a><span data-ttu-id="15578-128">Para remover todas as configurações de configuração do Lync Phone Edition em que o bloqueio de telefone está desabilitado</span><span class="sxs-lookup"><span data-stu-id="15578-128">To remove all of the Lync Phone Edition configuration settings where phone locking is disabled</span></span>

  - <span data-ttu-id="15578-129">Esse comando exclui qualquer conjunto de configurações de configuração de telefone UC em que o bloqueio de telefone foi desabilitado:</span><span class="sxs-lookup"><span data-stu-id="15578-129">This command deletes any collection of UC phone configuration settings where phone locking has been disabled:</span></span>
    
        Get-CsUCPhoneConfiguration | Where-Object {$_.EnforcePhoneLock -eq $False} | Remove-CsUCPhoneConfiguration

</div>

<span data-ttu-id="15578-130">Para obter detalhes, consulte [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15)).</span><span class="sxs-lookup"><span data-stu-id="15578-130">For details, see [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15)).</span></span>

<span data-ttu-id="15578-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15578-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

