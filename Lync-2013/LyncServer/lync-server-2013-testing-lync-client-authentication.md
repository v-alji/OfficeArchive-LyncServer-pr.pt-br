---
title: 'Lync Server 2013: testando a autenticação do cliente do Lync'
description: 'Lync Server 2013: testando a autenticação do cliente do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Client authentication
ms:assetid: e22114cb-4456-4e5f-93ab-51592c4a8209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689120(v=OCS.15)
ms:contentKeyID: 63969659
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03694b7fd56d7847d8d493304b97af335d2a5b4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390036"
---
# <a name="testing-lync-client-authentication-in-lync-server-2013"></a><span data-ttu-id="a8058-103">Testando a autenticação do cliente do Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8058-103">Testing Lync Client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8058-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8058-104">

<span> </span></span></span>

<span data-ttu-id="a8058-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="a8058-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8058-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="a8058-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="a8058-107">Diário</span><span class="sxs-lookup"><span data-stu-id="a8058-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8058-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="a8058-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="a8058-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8058-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8058-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="a8058-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="a8058-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="a8058-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="a8058-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsClientAuth.</span><span class="sxs-lookup"><span data-stu-id="a8058-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="a8058-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a8058-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsClientAuth&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="a8058-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8058-114">Description</span></span>

<span data-ttu-id="a8058-115">O cmdlet Test-CsClientAuth permite que você determine se um usuário pode fazer logon no Lync Server usando um certificado de cliente, você pode executar o cmdlet Test-CsClientAuth.</span><span class="sxs-lookup"><span data-stu-id="a8058-115">The Test-CsClientAuth cmdlet enables you to determine whether a user can log on to the Lync Server by using a client certificate, you can run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="a8058-116">Depois de chamar Test-CsClientAuth, o cmdlet entrará em contato com o serviço de provisionamento de certificado e baixará uma cópia de qualquer certificado de cliente para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="a8058-116">After calling Test-CsClientAuth, the cmdlet will contact the certificate provisioning service and download a copy of any client certificates for the specified user.</span></span> <span data-ttu-id="a8058-117">Se um certificado de cliente puder ser encontrado e baixado, o Test-CsClientAuth tentará fazer logon usando esse certificado.</span><span class="sxs-lookup"><span data-stu-id="a8058-117">If a client certificate can be found and downloaded, Test-CsClientAuth will then attempt to log on by using that certificate.</span></span> <span data-ttu-id="a8058-118">Se o logon for bem-sucedido, o Test-CsClientAuth fará logoff e relatará que o teste foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a8058-118">If logon succeeds, Test-CsClientAuth will log off and report that the test succeeded.</span></span> <span data-ttu-id="a8058-119">Se não for possível localizar ou baixar um certificado, ou se o cmdlet não conseguir fazer logon usando esse certificado, Test-CsClientAuth relatará que o teste falhou.</span><span class="sxs-lookup"><span data-stu-id="a8058-119">If a certificate cannot be found or downloaded, or if the cmdlet is unable to logon using that certificate, then Test-CsClientAuth will report that the test failed.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="a8058-120">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="a8058-120">Running the test</span></span>

<span data-ttu-id="a8058-121">O cmdlet Test-CsClientAuth é executado usando a conta de qualquer usuário habilitado para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a8058-121">The Test-CsClientAuth cmdlet is run by using the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="a8058-122">Para executar essa verificação usando uma conta de usuário real, primeiro você deve criar um objeto de credenciais do Windows PowerShell que contenha o nome da conta e a senha.</span><span class="sxs-lookup"><span data-stu-id="a8058-122">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="a8058-123">Em seguida, você deve incluir esse objeto de credenciais e o endereço SIP atribuído à conta quando o sistema chamar Test-CsClientAuth:</span><span class="sxs-lookup"><span data-stu-id="a8058-123">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsClientAuth:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="a8058-124">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) .</span><span class="sxs-lookup"><span data-stu-id="a8058-124">For more information, see the Help documentation for the [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="a8058-125">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="a8058-125">Determining success or failure</span></span>

<span data-ttu-id="a8058-126">Se o usuário especificado puder fazer logon no Lync Server usando um certificado de cliente, você receberá uma saída semelhante a isso, com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="a8058-126">If the specified user can log on to Lync Server by using a client certificate, you will receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="a8058-127">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a8058-127">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a8058-128">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="a8058-128">Result : Success</span></span>

<span data-ttu-id="a8058-129">Latência: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="a8058-129">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="a8058-130">Erros</span><span class="sxs-lookup"><span data-stu-id="a8058-130">Error :</span></span>

<span data-ttu-id="a8058-131">Correto</span><span class="sxs-lookup"><span data-stu-id="a8058-131">Diagnosis :</span></span>

<span data-ttu-id="a8058-132">Se o usuário especificado não puder fazer logon, o resultado será mostrado como uma falha e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="a8058-132">If the specified user can not log on, the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="a8058-133">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a8058-133">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a8058-134">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="a8058-134">Result : Failure</span></span>

<span data-ttu-id="a8058-135">Latência: 00:00:03.3645259</span><span class="sxs-lookup"><span data-stu-id="a8058-135">Latency : 00:00:03.3645259</span></span>

<span data-ttu-id="a8058-136">Erro: não foi possível baixar um certificado de CS para o usuário fornecido.</span><span class="sxs-lookup"><span data-stu-id="a8058-136">Error : Could not download a CS Certificate for the given user.</span></span> <span data-ttu-id="a8058-137">Verifique se</span><span class="sxs-lookup"><span data-stu-id="a8058-137">Check if</span></span>

<span data-ttu-id="a8058-138">as credenciais e o URI fornecidos estão corretos.</span><span class="sxs-lookup"><span data-stu-id="a8058-138">provided uri and credentials are correct.</span></span>

<span data-ttu-id="a8058-139">Correto</span><span class="sxs-lookup"><span data-stu-id="a8058-139">Diagnosis :</span></span>

<span data-ttu-id="a8058-140">Por exemplo, a saída anterior informa que o teste falhou porque um certificado de cliente válido não pôde ser localizado para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="a8058-140">For example, the previous output states that the test failed because a valid client certificate couldn't be located for the specified user.</span></span> <span data-ttu-id="a8058-141">Você pode retornar uma lista dos certificados de cliente emitidos para um usuário executando um comando da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a8058-141">You can return a list of the client certificates issued to a user by running a command as follows:</span></span>

    Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="a8058-142">Se Test-CsClientAuth falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="a8058-142">If Test-CsClientAuth fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential -Verbose

<span data-ttu-id="a8058-143">Quando o parâmetro Verbose estiver incluído, Test-CsClientAuth retornará uma conta passo a passo de cada ação que tentou verificar quando verificou a capacidade do usuário especificado para fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a8058-143">When the Verbose parameter is included, Test-CsClientAuth will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="a8058-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a8058-144">For example:</span></span>

<span data-ttu-id="a8058-145">Tentando baixar um certificado de CS para o usuário: kenmyer@litwareinc.com Endpoint: STEpid</span><span class="sxs-lookup"><span data-stu-id="a8058-145">Trying to download a CS certificate for User : kenmyer@litwareinc.com endpoint : STEpid</span></span>

<span data-ttu-id="a8058-146">URL do serviço Web: https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="a8058-146">Web Service url : https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span></span>

<span data-ttu-id="a8058-147">Não foi possível baixar um certificado de CS do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="a8058-147">Could not download a CS certificate from web service.</span></span>

<span data-ttu-id="a8058-148">SELECIONAR</span><span class="sxs-lookup"><span data-stu-id="a8058-148">CHECK:</span></span>

<span data-ttu-id="a8058-149">\- A URL do serviço Web é válida e os serviços Web são funcionais</span><span class="sxs-lookup"><span data-stu-id="a8058-149">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="a8058-150">\-Se estiver usando \\ \\ o pino PhoneNo para autenticar, certifique-se de que correspondam ao URI do usuário</span><span class="sxs-lookup"><span data-stu-id="a8058-150">\- If using PhoneNo\\\\Pin to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="a8058-151">\- Se estiver usando a \\ autenticação Kerberos NTLM, certifique-se de que você forneceu credenciais válidas</span><span class="sxs-lookup"><span data-stu-id="a8058-151">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="a8058-152">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="a8058-152">Reasons why the test might have failed</span></span>

<span data-ttu-id="a8058-153">Veja a seguir alguns motivos comuns para que Test-CsClientAuth possam falhar:</span><span class="sxs-lookup"><span data-stu-id="a8058-153">Here are some common reasons why Test-CsClientAuth might fail:</span></span>

  - <span data-ttu-id="a8058-154">Você especificou uma conta de usuário que não era válida.</span><span class="sxs-lookup"><span data-stu-id="a8058-154">You specified a user account that was not valid.</span></span> <span data-ttu-id="a8058-155">Você pode verificar se existe uma conta de usuário executando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="a8058-155">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="a8058-156">A conta de usuário é válida, mas a conta não está habilitada no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a8058-156">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="a8058-157">Para verificar se uma conta de usuário está habilitada para o Lync Server, execute um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8058-157">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="a8058-158">Se a propriedade Enabled estiver definida como false, isso significa que o usuário não está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a8058-158">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="a8058-159">O usuário de teste pode não ter um certificado de cliente válido.</span><span class="sxs-lookup"><span data-stu-id="a8058-159">The test user might not have a valid client certificate.</span></span> <span data-ttu-id="a8058-160">Você pode retornar informações sobre os certificados de cliente atribuídos a um usuário usando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="a8058-160">You can return information about the client certificates assigned to a user by using a command similar to this:</span></span>
    
        Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="a8058-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8058-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

