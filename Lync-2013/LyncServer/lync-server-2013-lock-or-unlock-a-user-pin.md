---
title: 'Lync Server 2013: bloquear ou desbloquear um PIN de usuário'
description: 'Lync Server 2013: bloquear ou desbloquear um PIN de usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lock or unlock a user PIN
ms:assetid: 3d293a8a-e182-4547-8b06-2603c3c77329
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688028(v=OCS.15)
ms:contentKeyID: 49733618
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2cf04be333e9d17dd0a06e6eb98d314c2960c3b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426470"
---
# <a name="lock-or-unlock-a-user-pin-in-lync-server-2013"></a><span data-ttu-id="e2b67-103">Bloquear ou desbloquear um PIN de usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2b67-103">Lock or unlock a user PIN in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2b67-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2b67-104">

<span> </span></span></span>

<span data-ttu-id="e2b67-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e2b67-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e2b67-106">Você pode bloquear ou desbloquear o pino de um usuário na seção **usuários** do painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e2b67-106">You can lock or unlock a user’s PIN from the **Users** section of Lync Server 2013 Control Panel.</span></span>

<div>

## <a name="to-lock-a-users-pin-in-lync-server-control-panel"></a><span data-ttu-id="e2b67-107">Para bloquear o PIN de um usuário no painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e2b67-107">To lock a user’s PIN in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="e2b67-108">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="e2b67-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e2b67-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e2b67-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e2b67-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e2b67-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e2b67-111">Na barra de navegação esquerda, clique em **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="e2b67-112">Use um dos seguintes métodos para localizar um usuário:</span><span class="sxs-lookup"><span data-stu-id="e2b67-112">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="e2b67-113">Na caixa **Pesquisar usuários**, digite todo ou parte do nome de exibição, nome, sobrenome, nome da conta SAM, endereço SIP ou URI de linha da conta do usuário e clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-113">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="e2b67-114">Se você salvou uma consulta, clique no ícone **Abrir consulta**, use a caixa de diálogo **Abrir** para recuperar a consulta (um arquivo .usf) e clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-114">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="e2b67-115">(Opcional) Especifique o critério de pesquisa adicional para reduzir os resultados:</span><span class="sxs-lookup"><span data-stu-id="e2b67-115">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="e2b67-116">Clique em **Adicionar filtro**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-116">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="e2b67-117">Insira a propriedade do usuário digitando ou clicando na seta da lista suspensa para selecionar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e2b67-117">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="e2b67-118">Na lista suspensa **Igual a**, clique no operador (por exemplo, **Igual a** ou **Diferente de**).</span><span class="sxs-lookup"><span data-stu-id="e2b67-118">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="e2b67-119">Dependendo da propriedade de usuário selecionada, insira os critérios que você deseja usar para filtrar os resultados da pesquisa digitando-os ou clicando na seta da lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="e2b67-119">Depending on the user property you selected, enter the criteria that you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        
        <div>
        

        > [!TIP]  
        > <span data-ttu-id="e2b67-120">Para adicionar cláusulas de pesquisa adicionais à sua consulta, clique em <STRONG>Adicionar filtro</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e2b67-120">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

        
        </div>
    
    5.  <span data-ttu-id="e2b67-121">Clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-121">Click **Find**.</span></span>
    
    6.  <span data-ttu-id="e2b67-122">Clique no usuário, em **Ação** e, em seguida, em **Bloquear PIN**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-122">Click the user, click **Action**, and then click **Lock PIN**.</span></span>

</div>

<div>

## <a name="to-unlock-a-users-pin-in-lync-server-control-panel"></a><span data-ttu-id="e2b67-123">Para desbloquear o PIN de um usuário no painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e2b67-123">To unlock a user’s PIN in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="e2b67-124">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="e2b67-124">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e2b67-125">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e2b67-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e2b67-126">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e2b67-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e2b67-127">Na barra de navegação esquerda, clique em **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-127">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="e2b67-128">Use um dos seguintes métodos para localizar um usuário:</span><span class="sxs-lookup"><span data-stu-id="e2b67-128">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="e2b67-129">Na caixa **Pesquisar usuários**, digite todo ou parte do nome de exibição, nome, sobrenome, nome da conta SAM, endereço SIP ou URI de linha da conta do usuário e clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-129">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="e2b67-130">Se você salvou uma consulta, clique no ícone **Abrir consulta**, use a caixa de diálogo **Abrir** para recuperar a consulta (um arquivo .usf) e clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-130">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="e2b67-131">(Opcional) Especifique o critério de pesquisa adicional para reduzir os resultados:</span><span class="sxs-lookup"><span data-stu-id="e2b67-131">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="e2b67-132">Clique em **Adicionar filtro**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-132">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="e2b67-133">Insira a propriedade do usuário digitando ou clicando na seta da lista suspensa para selecionar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e2b67-133">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="e2b67-134">Na lista suspensa **Igual a**, clique no operador (por exemplo, **Igual a** ou **Diferente de**).</span><span class="sxs-lookup"><span data-stu-id="e2b67-134">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="e2b67-135">Dependendo da propriedade de usuário selecionada, insira os critérios que você deseja usar para filtrar os resultados da pesquisa digitando-os ou clicando na seta da lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="e2b67-135">Depending on the user property you selected, enter the criteria that you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        
        <div>
        

        > [!TIP]  
        > <span data-ttu-id="e2b67-136">Para adicionar cláusulas de pesquisa adicionais à sua consulta, clique em <STRONG>Adicionar filtro</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e2b67-136">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

        
        </div>
    
    5.  <span data-ttu-id="e2b67-137">Clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-137">Click **Find**.</span></span>
    
    6.  <span data-ttu-id="e2b67-138">Clique no usuário, clique em **Ação** e, então, clique em **Desbloquear PIN**.</span><span class="sxs-lookup"><span data-stu-id="e2b67-138">Click the user, click **Action**, and then click **Unlock PIN**.</span></span>

</div>

<div>

## <a name="locking-and-unlocking-user-pins-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e2b67-139">Bloqueando e desbloqueando PINs de usuários usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2b67-139">Locking and Unlocking User PINs by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e2b67-140">Você pode bloquear e desbloquear PINs de usuários usando o Windows PowerShell e os cmdlets Lock-CsClientPin e Unlock-CsClientPin.</span><span class="sxs-lookup"><span data-stu-id="e2b67-140">You can lock and unlock user PINs by using Windows PowerShell and the Lock-CsClientPin and Unlock-CsClientPin cmdlets.</span></span> <span data-ttu-id="e2b67-141">Você pode executar esses cmdlets a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2b67-141">You can run these cmdlets either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e2b67-142">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="e2b67-142">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-lock-a-user-pin"></a><span data-ttu-id="e2b67-143">Para bloquear um PIN de usuário</span><span class="sxs-lookup"><span data-stu-id="e2b67-143">To lock a user PIN</span></span>

  - <span data-ttu-id="e2b67-p104">Para bloquear o PIN de um usuário, utilize o cmdlet Lock-CsClientPin. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e2b67-p104">To lock a user’s PIN, use the Lock-CsClientPin cmdlet. For example:</span></span>
    
        Lock-CsClientPin -Identity "Ken Myer"

</div>

<div>

## <a name="to-unlock-a-user-pin"></a><span data-ttu-id="e2b67-146">Para desbloquear um PIN de usuário</span><span class="sxs-lookup"><span data-stu-id="e2b67-146">To unlock a user PIN</span></span>

  - <span data-ttu-id="e2b67-p105">Para desbloquear o PIN de um usuário, utilize o cmdlet Unlock-CsClientPin. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e2b67-p105">To unlock a user’s PIN, use the Unlock-CsClientPin cmdlet. For example:</span></span>
    
        Unlock-CsClientPin -Identity "Ken Myer"

</div>

<span data-ttu-id="e2b67-149">Para obter mais informações, consulte o tópico da ajuda para os cmdlets [Lock-CsClientPin](https://docs.microsoft.com/powershell/module/skype/Lock-CsClientPin) e [Unlock-CsClientPin](https://docs.microsoft.com/powershell/module/skype/Unlock-CsClientPin) .</span><span class="sxs-lookup"><span data-stu-id="e2b67-149">For more information, see the help topic for the [Lock-CsClientPin](https://docs.microsoft.com/powershell/module/skype/Lock-CsClientPin) and [Unlock-CsClientPin](https://docs.microsoft.com/powershell/module/skype/Unlock-CsClientPin) cmdlets.</span></span>

<span data-ttu-id="e2b67-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2b67-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

