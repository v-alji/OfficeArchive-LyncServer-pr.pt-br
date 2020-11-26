---
title: 'Lync Server 2013: testar a configuração do nó do Inspetor'
description: 'Lync Server 2013: testando a configuração do nó do Inspetor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing watcher node configuration
ms:assetid: f9ecd85c-0ae9-4906-b786-6b002b5a77c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn751537(v=OCS.15)
ms:contentKeyID: 63969667
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1eeb141eee011d7e06f5dd49e483e026484d733
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440924"
---
# <a name="testing-watcher-node-configuration-in-lync-server-2013"></a><span data-ttu-id="910fe-103">Testando a configuração do nó do Inspetor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="910fe-103">Testing watcher node configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="910fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="910fe-104">

<span> </span></span></span>

<span data-ttu-id="910fe-105">_**Tópico da última modificação:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="910fe-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="910fe-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="910fe-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="910fe-107">Diário</span><span class="sxs-lookup"><span data-stu-id="910fe-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="910fe-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="910fe-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="910fe-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="910fe-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="910fe-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="910fe-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="910fe-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="910fe-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="910fe-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet <strong>Test-CsWatcherNodeConfiguration</strong> .</span><span class="sxs-lookup"><span data-stu-id="910fe-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWatcherNodeConfiguration</strong> cmdlet.</span></span> <span data-ttu-id="910fe-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="910fe-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot; Test-CsWatcherNodeConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="910fe-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="910fe-114">Description</span></span>

<span data-ttu-id="910fe-115">Se estiver usando o Microsoft System Center Operations Manager para monitorar o Lync Server 2013, você tem a opção de configurar "nós de Inspetor": computadores que periodicamente e automaticamente executam transações sintéticas para verificar se o Lync Server está funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="910fe-115">If you are using Microsoft System Center Operations Manager to monitor Lync Server 2013 then you have the option of setting up "watcher nodes": computers that periodically, and automatically, run synthetic transactions to verify that Lync Server is working as expected.</span></span> <span data-ttu-id="910fe-116">Os nós de Inspetor são atribuídos a pools e são gerenciados usando-se os cmdlets **CsWatcherNodeConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="910fe-116">Watcher nodes are assigned to pools, and are managed by using the **CsWatcherNodeConfiguration** cmdlets.</span></span> <span data-ttu-id="910fe-117">Observe que você não precisa instalar nós do Inspetor se estiver usando o System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="910fe-117">Note that you do not need to install watcher nodes if you are using System Center Operations Manager.</span></span> <span data-ttu-id="910fe-118">Você ainda pode monitorar o sistema sem usar nós de Inspetor.</span><span class="sxs-lookup"><span data-stu-id="910fe-118">You can still monitor your system without using watcher nodes.</span></span> <span data-ttu-id="910fe-119">A única diferença é que as transações sintéticas que você deseja executar devem ser invocadas manualmente em vez de invocadas automaticamente pelo Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="910fe-119">The only difference is that any synthetic transactions that you want to run must be invoked manually instead of automatically invoked by Operations Manager.</span></span>

<span data-ttu-id="910fe-120">O cmdlet **Test-CsWatcherNodeConfiguration** permite que você verifique se um nó do inspetor foi configurado corretamente e se foi atribuído a um pool válido do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="910fe-120">The **Test-CsWatcherNodeConfiguration** cmdlet enables you to verify that a watcher node was configured correctly and is assigned to a valid Lync Server 2013 pool.</span></span> <span data-ttu-id="910fe-121">Observe que o cmdlet **Test-CsWatcherNodeConfiguration** deve ser executado no próprio nó do Inspetor.</span><span class="sxs-lookup"><span data-stu-id="910fe-121">Note that the **Test-CsWatcherNodeConfiguration** cmdlet must be run on the watcher node itself.</span></span> <span data-ttu-id="910fe-122">O cmdlet não pode ser executado em computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="910fe-122">The cmdlet cannot be run against remote computers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="910fe-123">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="910fe-123">Running the test</span></span>

<span data-ttu-id="910fe-124">O comando a seguir verifica as definições de configuração para cada nó do inspetor que está sendo usado na organização.</span><span class="sxs-lookup"><span data-stu-id="910fe-124">The following command verifies the configuration settings for each watcher node that is being used in the organization.</span></span>

    Test-CsWatcherNodeConfiguration

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="910fe-125">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="910fe-125">Determining success or failure</span></span>

<span data-ttu-id="910fe-126">A seguinte saída de exemplo a seguir mostra um sistema com quatro servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="910fe-126">The following successful sample output shows a system with four edge servers.</span></span>

<span data-ttu-id="910fe-127">Validando o pool de destino atl-cs-001.litwareinc.com em relação à topologia.</span><span class="sxs-lookup"><span data-stu-id="910fe-127">Validating target pool atl-cs-001.litwareinc.com against topology.</span></span>

<span data-ttu-id="910fe-128">Êxito: o pool de destino atl-cs-001.litwareinc.com existe na topologia.</span><span class="sxs-lookup"><span data-stu-id="910fe-128">Success: Target pool atl-cs-001.litwareinc.com exists in topology.</span></span>

<span data-ttu-id="910fe-129">Êxito: o pool de destino atl-cs-001.litwareinc.com tem a função de registrador instalada.</span><span class="sxs-lookup"><span data-stu-id="910fe-129">Success: Target pool atl-cs-001.litwareinc.com has Registrar role installed.</span></span>

<span data-ttu-id="910fe-130">Êxito: versão do pool de destino atl-cs-001.litwareinc.com com suporte.</span><span class="sxs-lookup"><span data-stu-id="910fe-130">Success: Target pool atl-cs-001.litwareinc.com is supported version.</span></span>

<span data-ttu-id="910fe-131">Êxito: o número da porta para o pool de destino do 5061 atl-cs-001.litwareinc.com está correto.</span><span class="sxs-lookup"><span data-stu-id="910fe-131">Success: Port number for 5061 Target pool atl-cs-001.litwareinc.com is correct.</span></span>

<span data-ttu-id="910fe-132">A verificação de pools ausentes na configuração do nó do Inspetor é iniciada.</span><span class="sxs-lookup"><span data-stu-id="910fe-132">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="910fe-133">Se for detectado algum erro, ele será impresso.</span><span class="sxs-lookup"><span data-stu-id="910fe-133">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="910fe-134">A verificação de pools ausentes na configuração do nó do inspetor está concluída.</span><span class="sxs-lookup"><span data-stu-id="910fe-134">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="910fe-135">A verificação de chaves do registro do nó do Inspetor criadas pela instalação do nó do Inspetor é iniciada.</span><span class="sxs-lookup"><span data-stu-id="910fe-135">Checking for watcher node registry keys created by watcher node installation, is started.</span></span> <span data-ttu-id="910fe-136">Se for detectado algum erro, ele será impresso.</span><span class="sxs-lookup"><span data-stu-id="910fe-136">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="910fe-137">A verificação das chaves do registro do nó do Inspetor criadas pela instalação do nó do inspetor está concluída.</span><span class="sxs-lookup"><span data-stu-id="910fe-137">Checking for watcher node registry keys created by watcher node installation, is finished.</span></span> <span data-ttu-id="910fe-138">O tipo de autenticação detectado é Negotiate.</span><span class="sxs-lookup"><span data-stu-id="910fe-138">Detected authentication type is Negotiate.</span></span>

<span data-ttu-id="910fe-139">Existência validada com êxito da Credential SIP do usuário de teste: user1@ atl-cs-001.litwareinc.com no repositório de gerenciamento de credenciais.</span><span class="sxs-lookup"><span data-stu-id="910fe-139">Successfully validated existence of test user’s credential sip:user1@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="910fe-140">Existência validada com êxito da Credential SIP do usuário de teste: user2@ atl-cs-001.litwareinc.com no repositório de gerenciamento de credenciais.</span><span class="sxs-lookup"><span data-stu-id="910fe-140">Successfully validated existence of test user’s credential sip:user2@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="910fe-141">A verificação de pools ausentes na configuração do nó do Inspetor é iniciada.</span><span class="sxs-lookup"><span data-stu-id="910fe-141">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="910fe-142">Se for detectado algum erro, ele será impresso.</span><span class="sxs-lookup"><span data-stu-id="910fe-142">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="910fe-143">Aviso: o pool atl-cs-001.litwareinc.com tem registrador</span><span class="sxs-lookup"><span data-stu-id="910fe-143">WARNING: Pool atl-cs-001.litwareinc.com has Registrar</span></span>

<span data-ttu-id="910fe-144">função instalada, mas não há usuários de teste configurados para ele.</span><span class="sxs-lookup"><span data-stu-id="910fe-144">role installed, but there are no test users configured for it.</span></span>

<span data-ttu-id="910fe-145">A verificação de pools ausentes na configuração do nó do inspetor está concluída.</span><span class="sxs-lookup"><span data-stu-id="910fe-145">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="910fe-146">Verificar as chaves do registro do nó do Inspetor criadas pela instalação do nó do Inspetor é</span><span class="sxs-lookup"><span data-stu-id="910fe-146">Checking for watcher node registry keys created by watcher node installation, is</span></span>

<span data-ttu-id="910fe-147">vindo.</span><span class="sxs-lookup"><span data-stu-id="910fe-147">started.</span></span> <span data-ttu-id="910fe-148">Se for detectado algum erro, ele será impresso.</span><span class="sxs-lookup"><span data-stu-id="910fe-148">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="910fe-149">Test-CsWatcherNodeConfiguration: não é possível encontrar a chave do registro de integridade no</span><span class="sxs-lookup"><span data-stu-id="910fe-149">Test-CsWatcherNodeConfiguration : Cannot find Health registry key in</span></span>

<span data-ttu-id="910fe-150">Software \\ \\ de comunicação em tempo real da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="910fe-150">Software\\Microsoft\\Real-Time Communications.</span></span> <span data-ttu-id="910fe-151">Verifique se o nó inspetor. msi está</span><span class="sxs-lookup"><span data-stu-id="910fe-151">Make sure watcher node .msi is</span></span>

<span data-ttu-id="910fe-152">instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="910fe-152">installed properly.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="910fe-153">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="910fe-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="910fe-154">Aqui estão alguns motivos comuns pelos quais **Test-CsWatcherNodeConfiguration** pode falhar:</span><span class="sxs-lookup"><span data-stu-id="910fe-154">Here are some common reasons why **Test-CsWatcherNodeConfiguration** might fail:</span></span>

  - <span data-ttu-id="910fe-155">O nó do inspetor não está instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="910fe-155">Watcher node is not correctly installed.</span></span>

  - <span data-ttu-id="910fe-156">Nenhum usuário de teste está configurado.</span><span class="sxs-lookup"><span data-stu-id="910fe-156">No test users are configured.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="910fe-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="910fe-157">See Also</span></span>


[<span data-ttu-id="910fe-158">Get-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="910fe-158">Get-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWatcherNodeConfiguration)  
[<span data-ttu-id="910fe-159">New-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="910fe-159">New-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWatcherNodeConfiguration)  
[<span data-ttu-id="910fe-160">Remove-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="910fe-160">Remove-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWatcherNodeConfiguration)  
[<span data-ttu-id="910fe-161">Set-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="910fe-161">Set-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWatcherNodeConfiguration)  
  

<span data-ttu-id="910fe-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="910fe-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

