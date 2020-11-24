---
title: 'Lync Server 2013: testando o logon no Lync Phone Edition'
description: 'Lync Server 2013: testando o logon no Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Phone Edition login
ms:assetid: 1ccde6bf-9a2d-4fcf-b81f-1bc9fee2cfbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690128(v=OCS.15)
ms:contentKeyID: 63969583
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d21d65676c4f5e0f867c7d9556cdea50419be69b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390035"
---
# <a name="testing-lync-phone-edition-login-in-lync-server-2013"></a><span data-ttu-id="a2e80-103">Testando o login do Lync Phone Edition no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2e80-103">Testing Lync Phone Edition login in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2e80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2e80-104">

<span> </span></span></span>

<span data-ttu-id="a2e80-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="a2e80-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2e80-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="a2e80-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="a2e80-107">Diário</span><span class="sxs-lookup"><span data-stu-id="a2e80-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2e80-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="a2e80-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="a2e80-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a2e80-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2e80-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="a2e80-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="a2e80-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="a2e80-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="a2e80-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsPhoneBootstrap.</span><span class="sxs-lookup"><span data-stu-id="a2e80-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPhoneBootstrap cmdlet.</span></span> <span data-ttu-id="a2e80-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a2e80-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPhoneBootstrap&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="a2e80-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2e80-114">Description</span></span>

<span data-ttu-id="a2e80-115">O cmdlet Test-CsPhoneBootstrap permite que os administradores verifiquem se um determinado usuário — usando o número de telefone e o PIN atribuído a ele ou dele — pode fazer logon no sistema a partir de um dispositivo compatível com o Lync 2013 Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="a2e80-115">The Test-CsPhoneBootstrap cmdlet enables administrators to verify that a given user—using the phone number and PIN assigned to him or her—can log on to the system from a Lync 2013 Phone Edition-compatible device.</span></span> <span data-ttu-id="a2e80-116">(Nenhum dispositivo é realmente necessário para executar o teste.)</span><span class="sxs-lookup"><span data-stu-id="a2e80-116">(No device is actually needed to run the test.)</span></span>

<span data-ttu-id="a2e80-117">Para que o Test-CsPhoneBootstrap faça sua verificação, o pool de registrador que hospeda a conta de usuário que está sendo testada deve ser detectável usando DHCP.</span><span class="sxs-lookup"><span data-stu-id="a2e80-117">In order for Test-CsPhoneBootstrap to make its check, the Registrar pool that hosts the user account being tested must be discoverable using DHCP.</span></span> <span data-ttu-id="a2e80-118">Para determinar se um registrador é detectável dessa maneira, use o cmdlet Get-CsRegistrarConfiguration e verifique o valor da propriedade EnableDHCPServer.</span><span class="sxs-lookup"><span data-stu-id="a2e80-118">To determine whether a Registrar is discoverable in this manner, use the cmdlet Get-CsRegistrarConfiguration and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="a2e80-119">Se essa propriedade for definida como false, você deverá usar Set-CsRegistrarConfiguration para definir o valor da propriedade como true e torná-lo detectável usando DHCP.</span><span class="sxs-lookup"><span data-stu-id="a2e80-119">If this property is set to False, you must use Set-CsRegistrarConfiguration to set the property value to True and make the Registrar discoverable using DHCP.</span></span> <span data-ttu-id="a2e80-120">Isso também pode ser feito usando o servidor DHCP corporativo e configurando as opções específicas do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a2e80-120">This can also be done by using Enterprise DHCP Server and configuring the Lync Server-specific options.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="a2e80-121">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="a2e80-121">Running the test</span></span>

<span data-ttu-id="a2e80-122">Para executar o cmdlet Test-CsPhoneBootstrap, você deve, no mínimo, fornecer o número de telefone e o PIN (número de identificação pessoal) do cliente para um usuário válido do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a2e80-122">To run the Test-CsPhoneBootstrap cmdlet, you must, at a minimum, supply the phone number and client personal identification number (PIN) for a valid Lync Server user.</span></span> <span data-ttu-id="a2e80-123">Por exemplo, esse comando testa a capacidade de logon do usuário que tem o número de telefone 12065551219 e o pino 0712:</span><span class="sxs-lookup"><span data-stu-id="a2e80-123">For example, this command tests the logon ability for the user who has the phone number 12065551219 and the PIN 0712:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712"

<span data-ttu-id="a2e80-124">Para uma verificação mais abrangente, você também pode incluir o endereço SIP do usuário.</span><span class="sxs-lookup"><span data-stu-id="a2e80-124">For a more comprehensive check, you can also include the user’s SIP address.</span></span> <span data-ttu-id="a2e80-125">Nesse caso, o número de telefone, o PIN do cliente e o endereço SIP devem ser todos válidos para que o teste seja bem-sucedido:</span><span class="sxs-lookup"><span data-stu-id="a2e80-125">In that case, the phone number, client PIN, and SIP address must all be valid for the test to succeed:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -UserSipAddress "sip:kenmyer@litwareinc.com"

<span data-ttu-id="a2e80-126">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) .</span><span class="sxs-lookup"><span data-stu-id="a2e80-126">For more information, see the Help documentation for the [Test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="a2e80-127">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="a2e80-127">Determining success or failure</span></span>

<span data-ttu-id="a2e80-128">Se o usuário especificado tiver conseguido se conectar ao Lync Server, você receberá uma saída semelhante a isso, com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="a2e80-128">If the specified user was able to connect to Lync Server, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="a2e80-129">TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/</span><span class="sxs-lookup"><span data-stu-id="a2e80-129">TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/</span></span>

<span data-ttu-id="a2e80-130">CertProvisioningService. svc</span><span class="sxs-lookup"><span data-stu-id="a2e80-130">CertProvisioningService.svc</span></span>

<span data-ttu-id="a2e80-131">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a2e80-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a2e80-132">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="a2e80-132">Result : Success</span></span>

<span data-ttu-id="a2e80-133">Latência: 00:00:06.3981276</span><span class="sxs-lookup"><span data-stu-id="a2e80-133">Latency : 00:00:06.3981276</span></span>

<span data-ttu-id="a2e80-134">Erros</span><span class="sxs-lookup"><span data-stu-id="a2e80-134">Error :</span></span>

<span data-ttu-id="a2e80-135">Correto</span><span class="sxs-lookup"><span data-stu-id="a2e80-135">Diagnosis :</span></span>

<span data-ttu-id="a2e80-136">Se o usuário especificado não puder fazer uma conexão, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="a2e80-136">If the specified user was not able to make a connection, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="a2e80-137">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a2e80-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a2e80-138">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="a2e80-138">Result : Failure</span></span>

<span data-ttu-id="a2e80-139">Latência: 00:00:04.1993845</span><span class="sxs-lookup"><span data-stu-id="a2e80-139">Latency : 00:00:04.1993845</span></span>

<span data-ttu-id="a2e80-140">Erro: erro-nenhuma resposta recebida para o serviço de Web-Ticket.</span><span class="sxs-lookup"><span data-stu-id="a2e80-140">Error : ERROR - No response received for Web-Ticket service.</span></span>

<span data-ttu-id="a2e80-141">Correto</span><span class="sxs-lookup"><span data-stu-id="a2e80-141">Diagnosis :</span></span>

<span data-ttu-id="a2e80-142">A saída anterior informa que o teste falhou porque o serviço de tíquete da Web não respondeu.</span><span class="sxs-lookup"><span data-stu-id="a2e80-142">The previous output states that the test failed because the Web Ticket service did not respond.</span></span> <span data-ttu-id="a2e80-143">Isso pode ser devido a um problema com o próprio serviço ou pode ser devido ao endereço SIP, número de telefone ou PIN do cliente aprovado para Test-CsPhoneBootstrap.</span><span class="sxs-lookup"><span data-stu-id="a2e80-143">This could be due to a problem with the service itself, or it might be due to the SIP address, phone number, or client PIN passed to Test-CsPhoneBootstrap.</span></span> <span data-ttu-id="a2e80-144">Você pode verificar o endereço SIP do usuário e o número de telefone usando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="a2e80-144">You can verify the user’s SIP address and phone number by using a command similar to this one:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, LineUri

<span data-ttu-id="a2e80-145">E você pode verificar se o usuário tem um PIN válido usando um comando da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a2e80-145">And you can verify that the user has a valid PIN by using a command as follows:</span></span>

    Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="a2e80-146">Se Test-CsPhoneBootstrap falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="a2e80-146">If Test-CsPhoneBootstrap fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -Verbose

<span data-ttu-id="a2e80-147">Quando o parâmetro Verbose estiver incluído, Test-CsPhoneBootstrap retornará uma conta passo a passo de cada ação que tentou verificar quando verificou a capacidade do usuário especificado para fazer logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a2e80-147">When the Verbose parameter is included, Test-CsPhoneBootstrap will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="a2e80-148">Por exemplo, aqui está uma parte da saída de um logon malsucedido, uma sessão na qual um PIN incorreto foi incluído:</span><span class="sxs-lookup"><span data-stu-id="a2e80-148">For example, here is a portion of the output for an unsuccessful logon, a session in which an incorrect PIN was included:</span></span>

<span data-ttu-id="a2e80-149">Usando a autenticação de PIN com a extensão de telefone \\ : 12065551219 pino: 0712</span><span class="sxs-lookup"><span data-stu-id="a2e80-149">Using PIN auth with Phone\\Ext : 12065551219 Pin : 0712</span></span>

<span data-ttu-id="a2e80-150">Não foi possível obter a permissão da Web</span><span class="sxs-lookup"><span data-stu-id="a2e80-150">Could not get web ticket</span></span>

<span data-ttu-id="a2e80-151">SELECIONAR</span><span class="sxs-lookup"><span data-stu-id="a2e80-151">CHECK :</span></span>

<span data-ttu-id="a2e80-152">\- A URL do serviço Web é válida e os serviços Web são funcionais</span><span class="sxs-lookup"><span data-stu-id="a2e80-152">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="a2e80-153">\- Se estiver usando \\ o pino PhoneNo para autenticar, certifique-se de que correspondam ao URI do usuário</span><span class="sxs-lookup"><span data-stu-id="a2e80-153">\- If using PhoneNo\\PIN to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="a2e80-154">\- Se estiver usando a \\ autenticação Kerberos NTLM, certifique-se de que você forneceu credenciais válidas</span><span class="sxs-lookup"><span data-stu-id="a2e80-154">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="a2e80-155">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="a2e80-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="a2e80-156">Veja a seguir alguns motivos comuns para que Test-CsPhoneBootstrap possam falhar:</span><span class="sxs-lookup"><span data-stu-id="a2e80-156">Here are some common reasons why Test-CsPhoneBootstrap might fail:</span></span>

  - <span data-ttu-id="a2e80-157">Você pode ter especificado um endereço SIP que não é válido.</span><span class="sxs-lookup"><span data-stu-id="a2e80-157">You might have specified a SIP address that is not valid.</span></span> <span data-ttu-id="a2e80-158">Você pode verificar se um endereço SIP está correto usando um comando como este:</span><span class="sxs-lookup"><span data-stu-id="a2e80-158">You can verify that a SIP address is correct by using a command such as this one:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="a2e80-159">Você pode ter especificado um PIN que não é válido.</span><span class="sxs-lookup"><span data-stu-id="a2e80-159">You might have specified a PIN that is not valid.</span></span> <span data-ttu-id="a2e80-160">Embora não seja possível recuperar o número PIN do usuário, você pode verificar se o usuário pelo menos tem um número PIN usando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="a2e80-160">Although you can't retrieve the user’s PIN number, you can verify that the user at least has a PIN number by using a command similar to this:</span></span>
    
        Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="a2e80-161">Você pode ter especificado um número de telefone inválido.</span><span class="sxs-lookup"><span data-stu-id="a2e80-161">You might have specified a phone number that is not valid.</span></span> <span data-ttu-id="a2e80-162">Você pode verificar o telefone de um usuário usando um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="a2e80-162">You can verify a user’s phone by using a command similar to the following:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object LineUri

  - <span data-ttu-id="a2e80-163">O pool de registradores não está habilitado para DHCP.</span><span class="sxs-lookup"><span data-stu-id="a2e80-163">The Registrar pool is not DHCP-enabled.</span></span> <span data-ttu-id="a2e80-164">Para determinar se o pool de registrador está habilitado para DHCP, execute o cmdlet Get-CsRegistrarConfiguration e verifique o valor da propriedade EnableDHCPServer.</span><span class="sxs-lookup"><span data-stu-id="a2e80-164">To determine whether your Registrar pool is enabled for DHCP, run the Get-CsRegistrarConfiguration cmdlet and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="a2e80-165">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a2e80-165">For example:</span></span>
    
        Get-CsRegistrarConfiguration -Identity "global"

<span data-ttu-id="a2e80-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2e80-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

