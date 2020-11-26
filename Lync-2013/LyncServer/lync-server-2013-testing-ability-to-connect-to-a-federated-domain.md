---
title: 'Lync Server 2013: testando a capacidade de se conectar a um domínio federado'
description: 'Lync Server 2013: testando a capacidade de se conectar a um domínio federado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to connect to a federated domain
ms:assetid: d8ccfade-ef54-47a4-9f87-36213a635ce5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743840(v=OCS.15)
ms:contentKeyID: 63969653
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf1f5bdef66d34b9ca2e39797df0b4ad32d9afde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441134"
---
# <a name="testing-ability-to-connect-to-a-federated-domain-from-lync-server-2013"></a><span data-ttu-id="66c61-103">Testar a capacidade de se conectar a um domínio federado pelo Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66c61-103">Testing ability to connect to a federated domain from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66c61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66c61-104">

<span> </span></span></span>

<span data-ttu-id="66c61-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="66c61-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66c61-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="66c61-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="66c61-107">Diário</span><span class="sxs-lookup"><span data-stu-id="66c61-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66c61-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="66c61-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="66c61-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="66c61-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66c61-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="66c61-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="66c61-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="66c61-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="66c61-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsFederatedPartner.</span><span class="sxs-lookup"><span data-stu-id="66c61-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsFederatedPartner cmdlet.</span></span> <span data-ttu-id="66c61-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="66c61-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsFederatedPartner&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="66c61-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="66c61-114">Description</span></span>

<span data-ttu-id="66c61-115">Test-CsFederatedPartner verifica sua capacidade de conexão com o domínio de um parceiro federado.</span><span class="sxs-lookup"><span data-stu-id="66c61-115">Test-CsFederatedPartner verifies your ability to connect to the domain of a federated partner.</span></span> <span data-ttu-id="66c61-116">Para verificar a conectividade de um domínio, esse domínio deve estar listado na coleção de domínios permitidos (federados).</span><span class="sxs-lookup"><span data-stu-id="66c61-116">To verify the connectivity to a domain, that domain must be listed in the collection of allowed (federated) domains.</span></span> <span data-ttu-id="66c61-117">Você pode recuperar uma lista dos domínios na lista de domínios permitidos usando este comando:</span><span class="sxs-lookup"><span data-stu-id="66c61-117">You can retrieve a list of the domains on your allowed domains list by using this command:</span></span>

    Get-CsAllowedDomain

<span data-ttu-id="66c61-118">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) .</span><span class="sxs-lookup"><span data-stu-id="66c61-118">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="66c61-119">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="66c61-119">Running the test</span></span>

<span data-ttu-id="66c61-120">O cmdlet Test-FederatedPartner exige dois tipos de informação: o FQDN do servidor de borda e o FQDN do parceiro federado.</span><span class="sxs-lookup"><span data-stu-id="66c61-120">The Test-FederatedPartner cmdlet requires two pieces of information: the FQDN of your Edge Server and the FQDN of the federated partner.</span></span> <span data-ttu-id="66c61-121">Por exemplo, este comando testa a capacidade de conexão com o domínio contoso.com:</span><span class="sxs-lookup"><span data-stu-id="66c61-121">For example, this command tests the ability to connect to the domain contoso.com:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"

<span data-ttu-id="66c61-122">Este comando permite testar as conexões com todos os domínios atualmente na lista de domínios permitidos:</span><span class="sxs-lookup"><span data-stu-id="66c61-122">This command enables you to test the connections to all the domains currently on your allowed domains list:</span></span>

    Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Identity}

<span data-ttu-id="66c61-123">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) .</span><span class="sxs-lookup"><span data-stu-id="66c61-123">For more information, see the Help documentation for the [Test-CsFederatedPartner](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="66c61-124">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="66c61-124">Determining success or failure</span></span>

<span data-ttu-id="66c61-125">Se o domínio especificado puder ser contatado, você receberá uma saída semelhante a isso com a propriedade Result marcada como **Success:**</span><span class="sxs-lookup"><span data-stu-id="66c61-125">If the specified domain can be contacted, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="66c61-126">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="66c61-126">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="66c61-127">Resultado: êxito</span><span class="sxs-lookup"><span data-stu-id="66c61-127">Result : Success</span></span>

<span data-ttu-id="66c61-128">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66c61-128">Latency : 00:00:00</span></span>

<span data-ttu-id="66c61-129">Erros</span><span class="sxs-lookup"><span data-stu-id="66c61-129">Error :</span></span>

<span data-ttu-id="66c61-130">Correto</span><span class="sxs-lookup"><span data-stu-id="66c61-130">Diagnosis :</span></span>

<span data-ttu-id="66c61-131">Se o domínio especificado não puder ser contatado, o resultado será mostrado como uma falha, e informações adicionais serão gravadas nas propriedades de erro e diagnóstico:</span><span class="sxs-lookup"><span data-stu-id="66c61-131">If the specified domain cannot be contacted, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="66c61-132">TargetFqdn: atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="66c61-132">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="66c61-133">Resultado: falha</span><span class="sxs-lookup"><span data-stu-id="66c61-133">Result : Failure</span></span>

<span data-ttu-id="66c61-134">Latência: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66c61-134">Latency : 00:00:00</span></span>

<span data-ttu-id="66c61-135">Erro: 504, tempo limite do servidor</span><span class="sxs-lookup"><span data-stu-id="66c61-135">Error : 504, Server time-out</span></span>

<span data-ttu-id="66c61-136">Diagnóstico: ErrorCode = 2, origem = ATL-cs-001. litwareinc. com, motivo = Veja</span><span class="sxs-lookup"><span data-stu-id="66c61-136">Diagnosis : ErrorCode=2, Source=atl-cs-001.litwareinc.com,Reason=See</span></span>

<span data-ttu-id="66c61-137">código de resposta e frase de motivo.</span><span class="sxs-lookup"><span data-stu-id="66c61-137">response code and reason phrase.</span></span>

<span data-ttu-id="66c61-138">Microsoft. RTC. Signaling. DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="66c61-138">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="66c61-139">Por exemplo, a saída anterior informa que o teste falhou devido a um erro de tempo limite do servidor.</span><span class="sxs-lookup"><span data-stu-id="66c61-139">For example, the previous output states that the test failed because of a server time-out error.</span></span> <span data-ttu-id="66c61-140">Isso geralmente indica problemas de conectividade de rede ou problemas para entrar em contato com o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="66c61-140">This typically indicates either network connectivity problems or problems contacting the Edge Server.</span></span>

<span data-ttu-id="66c61-141">Se Test-CsFederatedPartner falhar, talvez você queira executar novamente o teste, desta vez, incluindo o parâmetro Verbose:</span><span class="sxs-lookup"><span data-stu-id="66c61-141">If Test-CsFederatedPartner fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com" -Verbose

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="66c61-142">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="66c61-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="66c61-143">Veja a seguir alguns motivos comuns para que Test-CsFederatedPartner possam falhar:</span><span class="sxs-lookup"><span data-stu-id="66c61-143">Here are some common reasons why Test-CsFederatedPartner might fail:</span></span>

  - <span data-ttu-id="66c61-144">O servidor de borda pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="66c61-144">The Edge Server might not be available.</span></span> <span data-ttu-id="66c61-145">Você pode usar este comando para os FQDNs dos seus servidores de borda:</span><span class="sxs-lookup"><span data-stu-id="66c61-145">You can the FQDNs of your Edge Servers by using this command:</span></span>
    
        Get-CsService -EdgeServer | Select-Object PoolFqdn
    
    <span data-ttu-id="66c61-146">Em seguida, você pode efetuar ping em cada servidor de borda para verificar se ele pode ser acessado pela rede.</span><span class="sxs-lookup"><span data-stu-id="66c61-146">You can then ping each Edge Server to verify that it can be accessed over the network.</span></span> <span data-ttu-id="66c61-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="66c61-147">For example:</span></span>
    
        ping atl-edge-001.litwareinc.com

  - <span data-ttu-id="66c61-148">O domínio especificado pode não estar listado na lista de domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="66c61-148">The specified domain might not be listed on the allowed domains list.</span></span> <span data-ttu-id="66c61-149">Para verificar os domínios que foram adicionados à lista de domínios permitidos, use este comando:</span><span class="sxs-lookup"><span data-stu-id="66c61-149">To verify the domains that were added to the allowed domains list, use this command:</span></span>
    
        Get-CsAllowedDomain
    
    <span data-ttu-id="66c61-150">Se você quiser ver uma lista de domínios com os quais os usuários estavam bloqueados e, em seguida, use este comando:</span><span class="sxs-lookup"><span data-stu-id="66c61-150">If you’d like to see a list of domains that users were blocked from communicating with, then use this command:</span></span>
    
        Get-CsBlockedDomain

<span data-ttu-id="66c61-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66c61-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

