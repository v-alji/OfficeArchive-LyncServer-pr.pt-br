---
title: 'Lync Server 2013: configuração do banco de dados de teste'
description: 'Lync Server 2013: testando a configuração do banco de dados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing database configuration
ms:assetid: 60f7fcd2-5efe-4791-b159-b0f9bf39a41b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727307(v=OCS.15)
ms:contentKeyID: 63969606
ms.date: 07/07/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b9f88eee99c4a2d523cc84df401dcc1d7b9fe59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441036"
---
# <a name="testing-database-configuration-in-lync-server-2013"></a><span data-ttu-id="adad0-103">Testar a configuração do banco de dados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="adad0-103">Testing database configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adad0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adad0-104">

<span> </span></span></span>

<span data-ttu-id="adad0-105">_**Tópico da última modificação:** 2016-07-07_</span><span class="sxs-lookup"><span data-stu-id="adad0-105">_**Topic Last Modified:** 2016-07-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adad0-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="adad0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="adad0-107">Diário</span><span class="sxs-lookup"><span data-stu-id="adad0-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adad0-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="adad0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="adad0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="adad0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adad0-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="adad0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="adad0-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins e precisam ter privilégios de administrador no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="adad0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group, and need to have Administrator privileges on the SQL server.</span></span></p>
<p><span data-ttu-id="adad0-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet <strong>Test-CsDatabase</strong> .</span><span class="sxs-lookup"><span data-stu-id="adad0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDatabase</strong> cmdlet.</span></span> <span data-ttu-id="adad0-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="adad0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDatabase&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="adad0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="adad0-114">Description</span></span>

<span data-ttu-id="adad0-115">O cmdlet **Test-CsDatabase** verifica a conectividade de um ou mais bancos de dados do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="adad0-115">The **Test-CsDatabase** cmdlet verifies connectivity to one or more Lync Server 2013 databases.</span></span> <span data-ttu-id="adad0-116">Quando executado, o cmdlet **Test-CsDatabase** lê a topologia do Lync Server, tenta se conectar a bancos de dados relevantes e, em seguida, relata o êxito ou falha de cada tentativa.</span><span class="sxs-lookup"><span data-stu-id="adad0-116">When run, the **Test-CsDatabase** cmdlet reads the Lync Server topology, attempts to connect to relevant databases, and then reports back the success or failure of each try.</span></span> <span data-ttu-id="adad0-117">Se for possível fazer uma conexão, o cmdlet também reportará essas informações como o nome do banco de dados, as informações de versão do SQL Server e o local de todos os bancos de dados espelhados instalados.</span><span class="sxs-lookup"><span data-stu-id="adad0-117">If a connection can be made, the cmdlet will also report back such information as the database name, SQL Server version information, and the location of any installed mirror databases.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="adad0-118">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="adad0-118">Running the test</span></span>

<span data-ttu-id="adad0-119">O comando mostrado no exemplo 1 verifica a configuração do banco de dados de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="adad0-119">The command shown in Example 1 verifies the configuration of the Central Management database.</span></span>

    Test-CsDatabase -CentralManagementDatabase

<span data-ttu-id="adad0-120">O exemplo 2 verifica todos os bancos de dados do Lync Server instalados no computador atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="adad0-120">Example 2 verifies all the Lync Server databases installed on the computer atl-sql-001.litwareinc.com.</span></span>

    Test-CsDatabase -ConfiguredDatabases -SqlServerFqdn "atl-sql-001.litwareinc.com"

<span data-ttu-id="adad0-121">No exemplo 3, a verificação é realizada somente para o banco de dados de arquivamento instalado no computador atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="adad0-121">In Example 3, verification is performed only for the Archiving database installed on the computer atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="adad0-122">Observe que o parâmetro SQLINSTANCENAME está incluído para especificar a instância do SQL Server (Archinst) em que o banco de dados de arquivamento está localizado.</span><span class="sxs-lookup"><span data-stu-id="adad0-122">Note that the SqlInstanceName parameter is included to specify the SQL Server instance (Archinst) where the Archiving database is located.</span></span>

    Test-CsDatabase -DatabaseType "Archiving" -SqlServerFqdn "atl-sql-001.litwareinc.com" -SqlInstanceName "archinst"

<span data-ttu-id="adad0-123">O comando mostrado no exemplo 4 verifica os bancos de dados instalados no computador local.</span><span class="sxs-lookup"><span data-stu-id="adad0-123">The command shown in Example 4 verifies the databases installed on the local computer.</span></span>

    Test-CsDatabase -LocalService

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="adad0-124">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="adad0-124">Determining success or failure</span></span>

<span data-ttu-id="adad0-125">Se a conectividade do banco de dados estiver configurada corretamente, você receberá uma saída semelhante a isso, com a propriedade sucede marcada como **verdadeira**:</span><span class="sxs-lookup"><span data-stu-id="adad0-125">If database connectivity is configured correctly, you'll receive output similar to this, with the Succeed property marked as **True**:</span></span>

<span data-ttu-id="adad0-126">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="adad0-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="adad0-127">SQLINSTANCENAME: RTC</span><span class="sxs-lookup"><span data-stu-id="adad0-127">SqlInstanceName : rtc</span></span>

<span data-ttu-id="adad0-128">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="adad0-128">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="adad0-129">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="adad0-129">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="adad0-130">DatabaseName: XDS</span><span class="sxs-lookup"><span data-stu-id="adad0-130">DatabaseName : xds</span></span>

<span data-ttu-id="adad0-131">Inclusão</span><span class="sxs-lookup"><span data-stu-id="adad0-131">DataSource :</span></span>

<span data-ttu-id="adad0-132">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-132">SQLServerVersion :</span></span>

<span data-ttu-id="adad0-133">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="adad0-133">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="adad0-134">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-134">InstalledVersion :</span></span>

<span data-ttu-id="adad0-135">Êxito: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="adad0-135">Succeed : True</span></span>

<span data-ttu-id="adad0-136">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="adad0-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="adad0-137">SQLINSTANCENAME: RTC</span><span class="sxs-lookup"><span data-stu-id="adad0-137">SqlInstanceName : rtc</span></span>

<span data-ttu-id="adad0-138">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="adad0-138">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="adad0-139">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="adad0-139">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="adad0-140">DatabaseName: Lis</span><span class="sxs-lookup"><span data-stu-id="adad0-140">DatabaseName : lis</span></span>

<span data-ttu-id="adad0-141">Inclusão</span><span class="sxs-lookup"><span data-stu-id="adad0-141">DataSource :</span></span>

<span data-ttu-id="adad0-142">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-142">SQLServerVersion :</span></span>

<span data-ttu-id="adad0-143">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="adad0-143">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="adad0-144">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-144">InstalledVersion :</span></span>

<span data-ttu-id="adad0-145">Êxito: verdadeiro</span><span class="sxs-lookup"><span data-stu-id="adad0-145">Succeed : True</span></span>

<span data-ttu-id="adad0-146">Se o banco de dados estiver configurado corretamente, mas ainda estiver disponível, o campo bem-sucedido será mostrado como **falso**, e avisos adicionais e informações serão fornecidos:</span><span class="sxs-lookup"><span data-stu-id="adad0-146">If the database is configured correctly but still available, the Succeed field will be shown as **False**, and additional warnings and information will be provided:</span></span>

<span data-ttu-id="adad0-147">SqlServerFqdn: atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="adad0-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="adad0-148">SQLINSTANCENAME: RTC</span><span class="sxs-lookup"><span data-stu-id="adad0-148">SqlInstanceName : rtc</span></span>

<span data-ttu-id="adad0-149">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="adad0-149">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="adad0-150">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="adad0-150">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="adad0-151">DatabaseName: XDS</span><span class="sxs-lookup"><span data-stu-id="adad0-151">DatabaseName : xds</span></span>

<span data-ttu-id="adad0-152">Inclusão</span><span class="sxs-lookup"><span data-stu-id="adad0-152">DataSource :</span></span>

<span data-ttu-id="adad0-153">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-153">SQLServerVersion :</span></span>

<span data-ttu-id="adad0-154">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="adad0-154">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="adad0-155">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-155">InstalledVersion :</span></span>

<span data-ttu-id="adad0-156">Bem-sucedido: falso</span><span class="sxs-lookup"><span data-stu-id="adad0-156">Succeed : False</span></span>

<span data-ttu-id="adad0-157">SqlServerFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="adad0-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="adad0-158">SQLINSTANCENAME: RTC</span><span class="sxs-lookup"><span data-stu-id="adad0-158">SqlInstanceName : rtc</span></span>

<span data-ttu-id="adad0-159">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="adad0-159">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="adad0-160">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="adad0-160">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="adad0-161">DatabaseName: Lis</span><span class="sxs-lookup"><span data-stu-id="adad0-161">DatabaseName : lis</span></span>

<span data-ttu-id="adad0-162">Inclusão</span><span class="sxs-lookup"><span data-stu-id="adad0-162">DataSource :</span></span>

<span data-ttu-id="adad0-163">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-163">SQLServerVersion :</span></span>

<span data-ttu-id="adad0-164">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="adad0-164">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="adad0-165">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="adad0-165">InstalledVersion :</span></span>

<span data-ttu-id="adad0-166">Bem-sucedido: falso</span><span class="sxs-lookup"><span data-stu-id="adad0-166">Succeed : False</span></span>

<span data-ttu-id="adad0-167">Aviso: Test-CsDatabase encontrou erros.</span><span class="sxs-lookup"><span data-stu-id="adad0-167">WARNING: Test-CsDatabase encountered errors.</span></span> <span data-ttu-id="adad0-168">Consulte o arquivo de log para obter uma</span><span class="sxs-lookup"><span data-stu-id="adad0-168">Consult the log file for a</span></span>

<span data-ttu-id="adad0-169">análise detalhada e para garantir que todos os erros (2) e avisos (0) sejam tratados</span><span class="sxs-lookup"><span data-stu-id="adad0-169">detailed analysis, and to make sure that all errors (2) and warnings (0) are addressed</span></span>

<span data-ttu-id="adad0-170">antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="adad0-170">before continuing.</span></span>

<span data-ttu-id="adad0-171">Aviso: os resultados detalhados podem ser encontrados em</span><span class="sxs-lookup"><span data-stu-id="adad0-171">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="adad0-172">"C: \\ usuários \\ testando \\ AppData \\ local \\ \\ 2 \\ Test-CsDatabase-b18d488a-8044-4679-bbf2-</span><span class="sxs-lookup"><span data-stu-id="adad0-172">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsDatabase-b18d488a-8044-4679-bbf2-</span></span>

<span data-ttu-id="adad0-173">04d593cce8e6.html ".</span><span class="sxs-lookup"><span data-stu-id="adad0-173">04d593cce8e6.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="adad0-174">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="adad0-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="adad0-175">Aqui estão alguns motivos comuns pelos quais **Test-CsDatabase** pode falhar:</span><span class="sxs-lookup"><span data-stu-id="adad0-175">Here are some common reasons why **Test-CsDatabase** might fail:</span></span>

  - <span data-ttu-id="adad0-176">Um valor de parâmetro incorreto foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="adad0-176">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="adad0-177">Se usado, os parâmetros opcionais devem ser configurados corretamente ou o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="adad0-177">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="adad0-178">Execute o comando novamente sem os parâmetros opcionais e veja se isso é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="adad0-178">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="adad0-179">Esse comando falhará se o banco de dados estiver configurado incorretamente ou ainda não foi implantado.</span><span class="sxs-lookup"><span data-stu-id="adad0-179">This command will fail if the database is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="adad0-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="adad0-180">See Also</span></span>


[<span data-ttu-id="adad0-181">Get-CsDatabaseMirrorState</span><span class="sxs-lookup"><span data-stu-id="adad0-181">Get-CsDatabaseMirrorState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDatabaseMirrorState)  
[<span data-ttu-id="adad0-182">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="adad0-182">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="adad0-183">Get-CsUserDatabaseState</span><span class="sxs-lookup"><span data-stu-id="adad0-183">Get-CsUserDatabaseState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserDatabaseState)  
  

<span data-ttu-id="adad0-184"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adad0-184"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

