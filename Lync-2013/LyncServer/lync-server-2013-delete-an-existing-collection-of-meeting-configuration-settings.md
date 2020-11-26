---
title: Excluir uma coleção existente de definições de configuração de reunião
description: Excluir uma coleção existente de definições de configuração de reunião.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of meeting configuration settings
ms:assetid: 92ff8a91-05c5-4047-a533-5dff12f22299
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688136(v=OCS.15)
ms:contentKeyID: 49733736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc0985023a1459130c7d589327535436145a0ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430529"
---
# <a name="delete-an-existing-collection-of-meeting-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="7bd5f-103">Excluir uma coleção existente de definições de configuração de reunião no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7bd5f-103">Delete an existing collection of meeting configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7bd5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7bd5f-104">

<span> </span></span></span>

<span data-ttu-id="7bd5f-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="7bd5f-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="7bd5f-106">Você pode excluir uma configuração de site ou de usuário.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-106">You can delete a site or user configuration.</span></span> <span data-ttu-id="7bd5f-107">A configuração global não pode ser removida.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="7bd5f-108">Se você excluir a configuração global, ela automaticamente retorna para os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-108">If you delete the global configuration, it is automatically reset to the default values.</span></span>

<div>

## <a name="to-delete-a-site-or-user-meeting-configuration"></a><span data-ttu-id="7bd5f-109">Para excluir uma configuração de reunião de site ou de usuário</span><span class="sxs-lookup"><span data-stu-id="7bd5f-109">To delete a site or user meeting configuration</span></span>

1.  <span data-ttu-id="7bd5f-110">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7bd5f-111">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7bd5f-112">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7bd5f-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7bd5f-113">Na barra de navegação à esquerda, clique em **conferência** e em **configuração de reunião**.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-113">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="7bd5f-114">Na lista de configuração de reunião, clique na configuração de site ou pool que deseja excluir, clique em **Editar** e em **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-114">In the list of meeting configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-meeting-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="7bd5f-115">Como remover as configurações de reunião usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7bd5f-115">Removing Meeting Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="7bd5f-116">As configurações de reunião podem ser excluídas usando o Windows PowerShell e o cmdlet Remove-CsMeetingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-116">Meeting settings can be deleted by using Windows PowerShell and the Remove-CsMeetingConfiguration cmdlet.</span></span> <span data-ttu-id="7bd5f-117">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-117">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="7bd5f-118">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="7bd5f-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-meeting-configuration-settings"></a><span data-ttu-id="7bd5f-119">Para remover uma coleção especificada de definições de configuração de reunião</span><span class="sxs-lookup"><span data-stu-id="7bd5f-119">To remove a specified collection of meeting configuration settings</span></span>

  - <span data-ttu-id="7bd5f-120">Este comando remove as definições de configuração de reunião aplicadas ao site Redmond:</span><span class="sxs-lookup"><span data-stu-id="7bd5f-120">This command removes the meeting configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsMeetingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="7bd5f-121">Para remover todas as definições de configuração de reunião aplicadas ao escopo do site</span><span class="sxs-lookup"><span data-stu-id="7bd5f-121">To remove all the meeting configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="7bd5f-122">Esse comando Remove todas as definições de configuração de reunião aplicadas ao escopo do site:</span><span class="sxs-lookup"><span data-stu-id="7bd5f-122">This command removes all the meeting configuration settings applied to the site scope:</span></span>
    
        Get-CsMeetingConfiguration -Filter "site:*" | Remove-CsMeetingConfiguration

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-that-admit-anonymous-users-by-default"></a><span data-ttu-id="7bd5f-123">Para remover todas as configurações de reunião que admitem usuários anônimos por padrão</span><span class="sxs-lookup"><span data-stu-id="7bd5f-123">To remove all the meeting configuration settings that admit anonymous users by default</span></span>

  - <span data-ttu-id="7bd5f-124">E isso remove todas as configurações que permitem que os usuários anônimos sejam admitidos por padrão:</span><span class="sxs-lookup"><span data-stu-id="7bd5f-124">And this one removes all the settings that allow anonymous users to be admitted by default:</span></span>
    
        Get-CsMeetingConfiguration | Where-Object {$_.AdmitAnonymousUsersByDefault -eq $True} | Remove-CsMeetingConfiguration

</div>

<span data-ttu-id="7bd5f-125">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="7bd5f-125">For more information, see the help topic for the [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="7bd5f-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7bd5f-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

