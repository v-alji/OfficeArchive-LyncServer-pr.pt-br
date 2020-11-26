---
title: Testando a configuração da conta Kerberos atribuída a um site
description: Testando a configuração da conta Kerberos atribuída a um site.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing configuration of the Kerberos account assigned to a site
ms:assetid: a087d77e-c59e-44f5-9caa-ccfd41be7276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743837(v=OCS.15)
ms:contentKeyID: 63969637
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0eab1618474a19753a4c6064d59aa4f8a856fceb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441064"
---
# <a name="testing-configuration-of-the-kerberos-account-assigned-to-a-site-in-lync-server-2013"></a><span data-ttu-id="4a4e1-103">Testando a configuração da conta Kerberos atribuída a um site no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a4e1-103">Testing configuration of the Kerberos account assigned to a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a4e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a4e1-104">

<span> </span></span></span>

<span data-ttu-id="4a4e1-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="4a4e1-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a4e1-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="4a4e1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="4a4e1-107">Diário</span><span class="sxs-lookup"><span data-stu-id="4a4e1-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a4e1-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="4a4e1-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="4a4e1-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a4e1-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a4e1-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="4a4e1-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="4a4e1-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="4a4e1-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsKerberosAccountAssignment cmdlet.</span></span> <span data-ttu-id="4a4e1-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="4a4e1-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsKerberosAccountAssignment&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="4a4e1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a4e1-114">Description</span></span>

<span data-ttu-id="4a4e1-115">O cmdlet Test-CsKerberosAccountAssignment permite que você verifique se uma conta Kerberos está associada a um determinado site, se essa conta está configurada corretamente e se a conta está funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-115">The Test-CsKerberosAccountAssignment cmdlet enables you to verify that a Kerberos account is associated with a given site, that this account is configured correctly, and that the account is working as expected.</span></span> <span data-ttu-id="4a4e1-116">As contas Kerberos são contas de computador que podem servir como a entidade de autenticação para todos os computadores em um site que estejam executando o IIS (servidor de informações da Internet).</span><span class="sxs-lookup"><span data-stu-id="4a4e1-116">Kerberos accounts are computer accounts that can serve as the authentication principal for all the computers in a site that are running Internet Information Server (IIS).</span></span> <span data-ttu-id="4a4e1-117">Como essas contas usam o protocolo de autenticação Kerberos, as contas são conhecidas como contas Kerberos, e o novo processo de autenticação é conhecido como autenticação da Web Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-117">Because these accounts use the Kerberos authentication protocol, the accounts are known as Kerberos accounts, and the new authentication process is known as Kerberos web authentication.</span></span> <span data-ttu-id="4a4e1-118">Isso permite que você gerencie todos os servidores IIS usando uma única conta.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-118">This enables you to manage all IIS servers by using a single account.</span></span>

<span data-ttu-id="4a4e1-119">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="4a4e1-119">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="4a4e1-120">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="4a4e1-120">Running the Test</span></span>

<span data-ttu-id="4a4e1-121">Por padrão, Test-CsKerberosAccountAssignment exibe um pouco de saída na tela.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-121">By default, Test-CsKerberosAccountAssignment displays very little output on-screen.</span></span> <span data-ttu-id="4a4e1-122">Em vez disso, as informações retornadas pelo cmdlet são gravadas em um arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-122">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="4a4e1-123">Por isso, recomendamos que você inclua o parâmetro Verbose e o parâmetro Report a qualquer momento que executar Test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-123">Because of that, we recommend that you include the Verbose parameter and the Report parameter any time that you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="4a4e1-124">O parâmetro Verbose fornecerá uma saída levemente mais detalhada na tela enquanto o cmdlet é executado.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-124">The Verbose parameter will provide slightly more detailed output on-screen while the cmdlet runs.</span></span> <span data-ttu-id="4a4e1-125">O parâmetro Report permite que você especifique um caminho de arquivo e um nome de arquivo para o arquivo HTML gerado por Test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-125">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="4a4e1-126">Se você não incluir o parâmetro do relatório, o arquivo HTML será salvo automaticamente na pasta usuários e receberá um nome semelhante a este: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-126">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="4a4e1-127">Você também deve especificar uma identidade de site ao executar Test-CsKerberosAccountAssignment.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-127">You must also specify a site Identity when you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="4a4e1-128">As contas Kerberos são atribuídas no escopo do site.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-128">Kerberos accounts are assigned at the site scope.</span></span>

<span data-ttu-id="4a4e1-129">O comando a seguir executa Test-CsKerberosAccountAssignment e salva a saída em um arquivo chamado C: \\ Logs \\KerberosTest.html:</span><span class="sxs-lookup"><span data-stu-id="4a4e1-129">The following command runs Test-CsKerberosAccountAssignment and saves the output to a file that is named C:\\Logs\\KerberosTest.html:</span></span>

    Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "C:\Logs\KerberosTest.html" -Verbose

<span data-ttu-id="4a4e1-130">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="4a4e1-130">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="4a4e1-131">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="4a4e1-131">Determining Success or Failure</span></span>

<span data-ttu-id="4a4e1-132">O cmdlet Test-CsKerberosAccountAssignment não retorna uma simples indicação de sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-132">The Test-CsKerberosAccountAssignment cmdlet does not return a simple indication of success or failure.</span></span> <span data-ttu-id="4a4e1-133">Em vez disso, você deve exibir o arquivo HTML gerado usando o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-133">Instead, you must view the generated HTML file by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="4a4e1-134">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="4a4e1-134">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="4a4e1-135">Veja a seguir alguns motivos comuns para que Test-CsKerberosAccountAssignment possam falhar:</span><span class="sxs-lookup"><span data-stu-id="4a4e1-135">Here are some common reasons why Test-CsKerberosAccountAssignment might fail:</span></span>

  - <span data-ttu-id="4a4e1-136">Você pode ter especificado uma identidade de site incorreta.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-136">You might have specified an incorrect site Identity.</span></span> <span data-ttu-id="4a4e1-137">Para retornar uma lista de identidade de site válida, use este comando:</span><span class="sxs-lookup"><span data-stu-id="4a4e1-137">To return a list of valid site Identity, use this command:</span></span>
    
        Get-CsSite | Select-Identity Identity
    
    <span data-ttu-id="4a4e1-138">Uma identidade de site geralmente tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="4a4e1-138">A site Identity typically looks as follows:</span></span>
    
    <span data-ttu-id="4a4e1-139">site: Redmond</span><span class="sxs-lookup"><span data-stu-id="4a4e1-139">site:Redmond</span></span>

  - <span data-ttu-id="4a4e1-140">O site especificado pode não ter uma conta Kerberos atribuída a ele.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-140">The specified site might not have a Kerberos account assigned to it.</span></span> <span data-ttu-id="4a4e1-141">Você pode determinar se uma conta Kerberos está ou não atribuída a um site executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="4a4e1-141">You can determine whether or not a Kerberos account is assigned to a site by running a command similar to this:</span></span>
    
        Get-CsKerberosAccountAssignment -Identity "site:Redmond"

  - <span data-ttu-id="4a4e1-142">Sua conta Kerberos pode ter uma senha que não é válida.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-142">Your Kerberos account might have a password that isn't valid.</span></span> <span data-ttu-id="4a4e1-143">Se você receber a seguinte mensagem de erro no relatório, provavelmente precisará redefinir a senha da conta Kerberos:</span><span class="sxs-lookup"><span data-stu-id="4a4e1-143">If you receive the following error message in report, you'll probably have to reset the Kerberos account password:</span></span>
    
    <span data-ttu-id="4a4e1-144">InvalidKerberosConfiguration: a configuração Kerberos é inválida.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-144">InvalidKerberosConfiguration: The Kerberos configuration is invalid.</span></span>
    
    <span data-ttu-id="4a4e1-145">InvalidKerberosConfiguration: a configuração Kerberos em atl-cs001.litwareinc.com é inválida.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-145">InvalidKerberosConfiguration: The Kerberos configuration on atl-cs001.litwareinc.com is invalid.</span></span> <span data-ttu-id="4a4e1-146">A conta atribuída esperada é litwareinc \\ kerberostest.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-146">The expected assigned account is litwareinc\\kerberostest.</span></span> <span data-ttu-id="4a4e1-147">Verifique se a conta não expirou e se a senha configurada no computador corresponde à senha do Active Directory da conta.</span><span class="sxs-lookup"><span data-stu-id="4a4e1-147">Ensure that the account has not expired, and the configured password on the machine matches the Active Directory password of the account.</span></span>
    
    <span data-ttu-id="4a4e1-148">Você pode definir a senha usando o cmdlet [set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="4a4e1-148">You can set the password using the [Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="4a4e1-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a4e1-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

