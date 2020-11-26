---
title: 'Lync Server 2013: testar a ativação do serviço e as permissões do grupo'
description: 'Lync Server 2013: testar a ativação do serviço e as permissões do grupo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing service activation and group permissions
ms:assetid: 2c59e603-ba85-40ba-91a7-51c6fd39472e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743833(v=OCS.15)
ms:contentKeyID: 63969594
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116cf939f3110616ce395eb14c7945890bdb89b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440980"
---
# <a name="testing-service-activation-and-group-permissions-in-lync-server-2013"></a><span data-ttu-id="36240-103">Testar a ativação do serviço e as permissões de grupo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36240-103">Testing service activation and group permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36240-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36240-104">

<span> </span></span></span>

<span data-ttu-id="36240-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="36240-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36240-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="36240-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="36240-107">Diário</span><span class="sxs-lookup"><span data-stu-id="36240-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36240-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="36240-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="36240-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="36240-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36240-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="36240-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="36240-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="36240-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="36240-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="36240-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTopology cmdlet.</span></span> <span data-ttu-id="36240-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="36240-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTopology&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="36240-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="36240-114">Description</span></span>

<span data-ttu-id="36240-115">O cmdlet Test-CsTopology permite que você verifique se o Lync Server 2013 está funcionando corretamente em um escopo global.</span><span class="sxs-lookup"><span data-stu-id="36240-115">The Test-CsTopology cmdlet enables you to verify that Lync Server 2013 is functioning correctly at a global scope.</span></span> <span data-ttu-id="36240-116">Por padrão, o cmdlet verifica toda a infraestrutura do Lync Server, verificando se os serviços necessários estão em execução e se as permissões apropriadas são definidas para esses serviços e para os grupos de segurança universal criados quando você instala o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="36240-116">By default, the cmdlet checks your whole Lync Server infrastructure, verifying that the required services are running and that the appropriate permissions are set for these services and for the universal security groups that are created when you install Lync Server.</span></span>

<span data-ttu-id="36240-117">Além de verificar a validade da instalação do Lync Server, Test-CsTopology também permite verificar a validade de um serviço específico.</span><span class="sxs-lookup"><span data-stu-id="36240-117">In addition to verifying the validity of the Lync Server installation, Test-CsTopology also lets you check the validity of a specific service.</span></span> <span data-ttu-id="36240-118">Por exemplo, esse comando verifica o estado do servidor de conferência A/V no pool atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="36240-118">For example, this command checks the state of the A/V Conferencing Server on the pool atl-cs-001.litwareinc.com:</span></span>

    Test-CsTopology -Service "ConferencingServer:atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="36240-119">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="36240-119">Running the test</span></span>

<span data-ttu-id="36240-120">Por padrão, Test-CsTopology exibe um pouco de saída na tela.</span><span class="sxs-lookup"><span data-stu-id="36240-120">By default, Test-CsTopology displays very little output on-screen.</span></span> <span data-ttu-id="36240-121">Em vez disso, as informações retornadas pelo cmdlet são gravadas em um arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="36240-121">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="36240-122">O parâmetro Report permite que você especifique um caminho de arquivo e um nome de arquivo para o arquivo HTML gerado por Test-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="36240-122">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsTopology.</span></span> <span data-ttu-id="36240-123">Se você não incluir o parâmetro do relatório, o arquivo HTML será salvo automaticamente na pasta usuários e receberá um nome semelhante a este: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="36240-123">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="36240-124">O comando de exemplo a seguir é executado Test-CsTopology e salva a saída em um arquivo chamado C: \\ Logs \\ComputerTest.html:</span><span class="sxs-lookup"><span data-stu-id="36240-124">The following sample command runs Test-CsTopology and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsTopology -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="36240-125">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) .</span><span class="sxs-lookup"><span data-stu-id="36240-125">For more information, see the Help documentation for the [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="36240-126">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="36240-126">Determining success or failure</span></span>

<span data-ttu-id="36240-127">Ao contrário da maioria dos cmdlets de teste, Test-CsTopology não relata sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="36240-127">Unlike most of the test cmdlets, Test-CsTopology does report back Success or Failure.</span></span> <span data-ttu-id="36240-128">Em parte, isso se deve ao grande número de verificações de verificação que o cmdlet deve fazer sempre que for executado.</span><span class="sxs-lookup"><span data-stu-id="36240-128">In part, that’s due to the large number of verification checks that the cmdlet must make every time that it runs.</span></span> <span data-ttu-id="36240-129">Em vez disso, os dados são salvos em um relatório HTML que pode ser visualizado usando o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="36240-129">Instead, data is saved to an HTML report that can then be viewed by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="36240-130">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="36240-130">Reasons why the test might have failed</span></span>

<span data-ttu-id="36240-131">Veja a seguir alguns motivos comuns para que Test-CsTopology possam falhar:</span><span class="sxs-lookup"><span data-stu-id="36240-131">Here are some common reasons why Test-CsTopology might fail:</span></span>

  - <span data-ttu-id="36240-132">A replicação pode não estar atualizada no computador de teste.</span><span class="sxs-lookup"><span data-stu-id="36240-132">Replication might not be up-to-date on the test computer.</span></span> <span data-ttu-id="36240-133">Você pode verificar o status de replicação atual para um computador executando o cmdlet Get-CsManagementStoreReplicationStatus:</span><span class="sxs-lookup"><span data-stu-id="36240-133">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="36240-134">Se o status de replicação não for atualizado, você pode forçar manualmente a ocorrência da replicação usando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="36240-134">If the replication status is not up-to-date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="36240-135">A topologia pode ter que ser ativada.</span><span class="sxs-lookup"><span data-stu-id="36240-135">The topology might have to be enabled.</span></span> <span data-ttu-id="36240-136">Se você alterar a topologia do Lync Server (alterações que podem afetar o computador local), será necessário habilitar a nova topologia.</span><span class="sxs-lookup"><span data-stu-id="36240-136">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="36240-137">Você pode habilitar a topologia a qualquer momento executando este comando:</span><span class="sxs-lookup"><span data-stu-id="36240-137">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="36240-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36240-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

