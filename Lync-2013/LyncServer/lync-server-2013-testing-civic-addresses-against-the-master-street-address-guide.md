---
title: Testando endereços cívicos no guia de endereço principal do Street
description: Testando endereços cívicos em relação ao guia de endereço do endereço mestre.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing civic addresses against the master street address guide
ms:assetid: dc680de9-2a0f-4fd3-a99e-9bab0bc30ae5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690132(v=OCS.15)
ms:contentKeyID: 63969657
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16e0d721b70e3db175b2d23ddee6f59d13a13c4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439825"
---
# <a name="testing-civic-addresses-against-the-master-street-address-guide-in-lync-server-2013"></a><span data-ttu-id="ab7a8-103">Testando endereços cívicos em relação ao guia de endereço mestre do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab7a8-103">Testing civic addresses against the master street address guide in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab7a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab7a8-104">

<span> </span></span></span>

<span data-ttu-id="ab7a8-105">_**Tópico da última modificação:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="ab7a8-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab7a8-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="ab7a8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ab7a8-107">Diário</span><span class="sxs-lookup"><span data-stu-id="ab7a8-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab7a8-108">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="ab7a8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ab7a8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab7a8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab7a8-110">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="ab7a8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ab7a8-111">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="ab7a8-112">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsRegistration.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="ab7a8-113">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ab7a8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisCivicAddress &quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ab7a8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab7a8-114">Description</span></span>

<span data-ttu-id="ab7a8-115">O cmdlet Test-CsLisCivicAddress é usado para verificar os locais que foram adicionados ao seu banco de dados do serviço de informações de localização (LIS).</span><span class="sxs-lookup"><span data-stu-id="ab7a8-115">The Test-CsLisCivicAddress cmdlet is used to verify locations that were added to your Location Information service (LIS) database.</span></span> <span data-ttu-id="ab7a8-116">O cmdlet funciona comparando os locais com base nos locais encontrados no guia de endereço mestre do Street (MSAG) que pertence ao seu provedor de roteamento de rede do E9-1.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-116">The cmdlet works by comparing locations against the locations found in the Master Street Address Guide (MSAG) that belongs to your E9-1-1 Network Routing Provider.</span></span> <span data-ttu-id="ab7a8-117">Se você não tiver um provedor de roteamento de rede ou se o provedor não puder ser acessado, seus testes falharão.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-117">If you do not have a network routing provider or if the provider cannot be reached, then your tests will fail.</span></span>

<span data-ttu-id="ab7a8-118">Se você adicionar o parâmetro de opção opcional UpdateValidationStatus ao seu comando, a propriedade de banco de dados MSAGValid correspondente será definida como true para cada endereço passando pelo teste.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-118">If you add the optional switch parameter UpdateValidationStatus to your command, then the corresponding MSAGValid database property will be set to True for each address passing the test.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ab7a8-119">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="ab7a8-119">Running the test</span></span>

<span data-ttu-id="ab7a8-120">O cmdlet Test-CsLisCivicAddress pode ser usado para testar endereços individuais ou testar vários endereços.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-120">The Test-CsLisCivicAddress cmdlet can be used to test individual addresses or to test multiple addresses.</span></span> <span data-ttu-id="ab7a8-121">Por exemplo, este comando testa um único endereço localizado em Redmond, WA:</span><span class="sxs-lookup"><span data-stu-id="ab7a8-121">For example, this command tests a single address located in Redmond, WA:</span></span>

    Test-CsLisCivicAddress -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName Main -StreetSuffix St -PostDirectional "" -City Redmond -State WA -PostalCode 98052 -Country US -UpdateValidationStatus

<span data-ttu-id="ab7a8-122">Por comparação, esse comando testa todos os endereços atualmente em seu banco de dados LIS:</span><span class="sxs-lookup"><span data-stu-id="ab7a8-122">By comparison, this command tests all the addresses currently in your LIS database:</span></span>

    Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus

<span data-ttu-id="ab7a8-123">Para obter mais informações, consulte a documentação da ajuda para o cmdlet [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="ab7a8-123">For more information, see the Help documentation for the [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="ab7a8-124">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="ab7a8-124">Determining success or failure</span></span>

<span data-ttu-id="ab7a8-125">Test-CsLisCivicAddress reportará o sucesso ou a falha dos endereços fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-125">Test-CsLisCivicAddress will report back Success or Failure for the supplied addresses.</span></span> <span data-ttu-id="ab7a8-126">Um teste de endereço falhará se o endereço não for encontrado ou se não for possível entrar em contato com o provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-126">An address test will fail if the address cannot be found or if the service provider cannot be contacted.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="ab7a8-127">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="ab7a8-127">Reasons why the test might have failed</span></span>

<span data-ttu-id="ab7a8-128">Veja a seguir alguns motivos comuns para que Test-CsLisCivicAddress possam falhar:</span><span class="sxs-lookup"><span data-stu-id="ab7a8-128">Here are some common reasons why Test-CsLisCivicAddress might fail:</span></span>

  - <span data-ttu-id="ab7a8-129">O provedor de serviço LIS pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-129">The LIS service provider might not be available.</span></span> <span data-ttu-id="ab7a8-130">Você pode recuperar a URL do seu provedor de serviços LIS executando o cmdlet Get-CsLisConfiguration:</span><span class="sxs-lookup"><span data-stu-id="ab7a8-130">You can retrieve the URL of your LIS service provider by running the Get-CsLisConfiguration cmdlet:</span></span>
    
        Get-CsLisConfiguration 
    
    <span data-ttu-id="ab7a8-131">Em seguida, você pode executar o ping nesse URL para verificar se o provedor de serviço está disponível.</span><span class="sxs-lookup"><span data-stu-id="ab7a8-131">You can then ping that URL to verify that the service provider is available.</span></span>

<span data-ttu-id="ab7a8-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab7a8-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

