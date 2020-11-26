---
title: 'Lync Server 2013: testar a conexão do usuário com o correio de voz do Exchange UM'
description: 'Lync Server 2013: testando a conexão do usuário para o correio de voz do Exchange UM.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user connection to Exchange UM voicemail
ms:assetid: 574da104-8823-4061-9fb6-353639f1884d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727305(v=OCS.15)
ms:contentKeyID: 63969604
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b887b5b0df02a5864e0a39f2b62893d20105a86a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439707"
---
# <a name="testing-user-connection-to-exchange-um-voicemail-in-lync-server-2013"></a><span data-ttu-id="19119-103">Testando a conexão do usuário com o correio de voz do Exchange no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19119-103">Testing user connection to Exchange UM voicemail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19119-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19119-104">

<span> </span></span></span>

<span data-ttu-id="19119-105">_**Tópico da última modificação:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="19119-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19119-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="19119-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="19119-107">Diário</span><span class="sxs-lookup"><span data-stu-id="19119-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19119-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="19119-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="19119-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="19119-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19119-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="19119-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="19119-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="19119-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="19119-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet <strong>Test-CsExUMVoiceMail</strong> .</span><span class="sxs-lookup"><span data-stu-id="19119-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExUMVoiceMail</strong> cmdlet.</span></span> <span data-ttu-id="19119-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="19119-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExUMVoiceMail&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="19119-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="19119-114">Description</span></span>

<span data-ttu-id="19119-115">O cmdlet **Test-CsExUMVoiceMail** permite que os administradores verifiquem se um usuário pode acessar e usar o serviço de mensagens unificadas do Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="19119-115">The **Test-CsExUMVoiceMail** cmdlet enables administrators to verify that a user can access and use the Microsoft Exchange Server 2013 unified messaging service.</span></span> <span data-ttu-id="19119-116">Para fazer isso, o cmdlet se conecta ao serviço de Unificação de mensagens e deixa uma caixa postal na caixa de correio especificada.</span><span class="sxs-lookup"><span data-stu-id="19119-116">To do this, the cmdlet connects to the unified messaging service and leaves a voice mail in the specified mailbox.</span></span> <span data-ttu-id="19119-117">Pode ser uma caixa postal fornecida pelo sistema ou pode ser um personalizada. WAV que você mesmo gravou.</span><span class="sxs-lookup"><span data-stu-id="19119-117">This can be a system-supplied voice mail, or it can be a custom .WAV file that you have recorded yourself.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="19119-118">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="19119-118">Running the test</span></span>

<span data-ttu-id="19119-119">O exemplo a seguir testa a conectividade da caixa postal do Exchange Unified Messaging para o pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="19119-119">The following example tests Exchange Unified Messaging voice mail connectivity for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="19119-120">Esse comando funcionará apenas se os usuários de teste tiverem sido definidos para o pool atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="19119-120">This command will work only if test users were defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="19119-121">Se eles tiverem, o comando determinará se o primeiro usuário de teste pode usar a caixa postal de mensagens unificadas.</span><span class="sxs-lookup"><span data-stu-id="19119-121">If they have, then the command will determine whether the first test user can use Unified Messaging voice mail.</span></span> <span data-ttu-id="19119-122">Se os usuários de teste não tiverem sido configurados para o pool, o comando irá falhar.</span><span class="sxs-lookup"><span data-stu-id="19119-122">If test users were not configured for the pool then the command will fail.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="19119-123">Os comandos mostrados no próximo exemplo testam a conectividade da caixa postal do Exchange Unified Messaging para o usuário litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="19119-123">The commands shown in the next example test Exchange Unified Messaging voice mail connectivity for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="19119-124">Para fazer isso, o primeiro comando do exemplo usa o cmdlet **Get-Credential** para criar um objeto de credenciais da interface de linha de comando do Windows PowerShell para o usuário litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="19119-124">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="19119-125">Observe que você deve fornecer a senha desta conta para criar um objeto de credenciais válido e para garantir que o cmdlet **Test-CsExUMVoiceMail** possa executar sua verificação.</span><span class="sxs-lookup"><span data-stu-id="19119-125">Note that you must supply the password for this account to create a valid credentials object and to ensure that the **Test-CsExUMVoiceMail** cmdlet can run its check.</span></span>

<span data-ttu-id="19119-126">O segundo comando do exemplo usa o objeto de credenciais fornecido ($x) e o endereço SIP do usuário litwareinc \\ kenmyer para determinar se ou este usuário pode se conectar à caixa postal do Exchange Unified Messaging.</span><span class="sxs-lookup"><span data-stu-id="19119-126">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether or this user can connect to Exchange Unified Messaging voice mail.</span></span>

    $credential = Get-Credential "litwareinc\pilar" 
    
    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $credential 

<span data-ttu-id="19119-127">O comando mostrado no próximo exemplo é uma variação do comando mostrado no exemplo 1; Nesse caso, o parâmetro OutLoggerVariable é incluído para gerar um log detalhado de cada etapa feita pelo **Test-CsExUMVoiceMail** cmdletand o êxito ou falha de cada uma dessas etapas.</span><span class="sxs-lookup"><span data-stu-id="19119-127">The command shown in the next example is a variation of the command shown in Example 1; in this case, the OutLoggerVariable parameter is included to generate a detailed log of every step done by the **Test-CsExUMVoiceMail** cmdletand the success or failure of each of those steps.</span></span> <span data-ttu-id="19119-128">Para fazer isso, o parâmetro OutLoggerVariable é adicionado juntamente com o valor de parâmetro ExumText; Isso faz com que as informações de registro detalhadas sejam armazenadas em uma variável chamada $ExumTest.</span><span class="sxs-lookup"><span data-stu-id="19119-128">To do this, the OutLoggerVariable parameter is added alongside the parameter value ExumText; that causes detailed logging information to be stored in a variable named $ExumTest.</span></span> <span data-ttu-id="19119-129">No comando final do exemplo, o método ToXML () é usado para converter as informações de log em formato XML.</span><span class="sxs-lookup"><span data-stu-id="19119-129">In the final command in the example, the ToXML() method is used to convert the log information to XML format.</span></span> <span data-ttu-id="19119-130">Em seguida, esses dados XML são gravados em um arquivo chamado C: \\ Logs \\VoicemailTest.xml usando o cmdlet Out-File.</span><span class="sxs-lookup"><span data-stu-id="19119-130">That XML data is then written to a file that is named C:\\Logs\\VoicemailTest.xml by using the Out-File cmdlet.</span></span>

    Test-CsExUMVoiceMail -TargetFqdn "atl-cs-001.litwareinc.com" -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -OutLoggerVariable VoicemailTest 
     
    $VoicemailTest.ToXML() | Out-File C:\Logs\VoicemailTest.xml

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="19119-131">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="19119-131">Determining success or failure</span></span>

<span data-ttu-id="19119-132">Se a integração com o Exchange estiver configurada corretamente, você receberá uma saída semelhante a isso, com a propriedade Result marcada como **Success**:</span><span class="sxs-lookup"><span data-stu-id="19119-132">If Exchange integration is correctly configured, you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="19119-133">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="19119-133">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="19119-134">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="19119-134">Result : Success</span></span>

<span data-ttu-id="19119-135">Latência: 00:00:02.9911345</span><span class="sxs-lookup"><span data-stu-id="19119-135">Latency : 00:00:02.9911345</span></span>

<span data-ttu-id="19119-136">Mensagem de erro:</span><span class="sxs-lookup"><span data-stu-id="19119-136">Error Message :</span></span>

<span data-ttu-id="19119-137">Correto</span><span class="sxs-lookup"><span data-stu-id="19119-137">Diagnosis :</span></span>

<span data-ttu-id="19119-138">Se o usuário especificado não conseguir se conectar ao correio de voz, o resultado será mostrado como uma **falha**, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="19119-138">If the specified user can't connect to voicemail, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="19119-139">Aviso: falha ao ler o número da porta do registrador para o número da porta de dados totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="19119-139">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="19119-140">FQDN (nome de domínio).</span><span class="sxs-lookup"><span data-stu-id="19119-140">domain name (FQDN).</span></span> <span data-ttu-id="19119-141">Usando o número da porta do registrador padrão.</span><span class="sxs-lookup"><span data-stu-id="19119-141">Using default Registrar port number.</span></span> <span data-ttu-id="19119-142">Extremamente</span><span class="sxs-lookup"><span data-stu-id="19119-142">Exception:</span></span>

<span data-ttu-id="19119-143">System. InvalidOperationException: nenhum cluster correspondente localizado na topologia.</span><span class="sxs-lookup"><span data-stu-id="19119-143">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="19119-144">como</span><span class="sxs-lookup"><span data-stu-id="19119-144">at</span></span>

<span data-ttu-id="19119-145">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="19119-145">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="19119-146">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="19119-146">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="19119-147">FQDN de destino: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="19119-147">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="19119-148">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="19119-148">Result : Failure</span></span>

<span data-ttu-id="19119-149">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="19119-149">Latency : 00:00:00</span></span>

<span data-ttu-id="19119-150">Mensagem de erro: 10060, falha na tentativa de conexão porque a parte conectada</span><span class="sxs-lookup"><span data-stu-id="19119-150">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="19119-151">Não respondeu corretamente após um período de tempo ou</span><span class="sxs-lookup"><span data-stu-id="19119-151">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="19119-152">a conexão estabelecida falhou porque o host conectado tem</span><span class="sxs-lookup"><span data-stu-id="19119-152">established connection failed because connected host has</span></span>

<span data-ttu-id="19119-153">Falha ao responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="19119-153">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="19119-154">Exceção interna: falha na tentativa de conexão porque o</span><span class="sxs-lookup"><span data-stu-id="19119-154">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="19119-155">a parte conectada não respondeu corretamente após um período de</span><span class="sxs-lookup"><span data-stu-id="19119-155">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="19119-156">falha na hora ou estabelecida a conexão porque o host conectado</span><span class="sxs-lookup"><span data-stu-id="19119-156">time, or established connection failed because connected host</span></span>

<span data-ttu-id="19119-157">falhou ao responder 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="19119-157">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="19119-158">Correto</span><span class="sxs-lookup"><span data-stu-id="19119-158">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="19119-159">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="19119-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="19119-160">Aqui estão alguns motivos comuns pelos quais **Test-CsExUMVoiceMail** pode falhar:</span><span class="sxs-lookup"><span data-stu-id="19119-160">Here are some common reasons why **Test-CsExUMVoiceMail** might fail:</span></span>

  - <span data-ttu-id="19119-161">Um valor de parâmetro incorreto foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="19119-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="19119-162">Se usado, os parâmetros opcionais devem ser configurados corretamente ou o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="19119-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="19119-163">Execute o comando novamente sem os parâmetros opcionais e veja se isso é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="19119-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="19119-164">Esse comando falhará se o Exchange Server estiver configurado incorretamente ou ainda não foi implantado.</span><span class="sxs-lookup"><span data-stu-id="19119-164">This command will fail if the Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="19119-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="19119-165">See Also</span></span>


[<span data-ttu-id="19119-166">Test-CsExUMConnectivity</span><span class="sxs-lookup"><span data-stu-id="19119-166">Test-CsExUMConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExUMConnectivity)  
  

<span data-ttu-id="19119-167"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19119-167"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

