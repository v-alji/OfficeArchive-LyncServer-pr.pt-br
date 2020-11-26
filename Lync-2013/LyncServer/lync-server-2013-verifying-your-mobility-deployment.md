---
title: 'Lync Server 2013: Verificando sua implantação de mobilidade'
description: 'Lync Server 2013: verificando a implantação da mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verifying your mobility deployment
ms:assetid: 72f9b4d3-57b0-4705-9480-cfdca313a70c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690024(v=OCS.15)
ms:contentKeyID: 48184477
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eadda35438961e469fdd5fa7976762141b26a385
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438873"
---
# <a name="verifying-your-mobility-deployment-in-lync-server-2013"></a><span data-ttu-id="e353b-103">Verificando sua implantação de mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e353b-103">Verifying your mobility deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e353b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e353b-104">

<span> </span></span></span>

<span data-ttu-id="e353b-105">_**Tópico da última modificação:** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="e353b-105">_**Topic Last Modified:** 2013-02-12_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="e353b-106">Depois de implantar o serviço de mobilidade do Lync Server e o serviço de descoberta automática do Lync Server, execute uma transação de teste para verificar se sua implantação funciona corretamente.</span><span class="sxs-lookup"><span data-stu-id="e353b-106">After you deploy the Lync Server Mobility Service and Lync Server Autodiscover Service, run a test transaction to verify that your deployment works correctly.</span></span> <span data-ttu-id="e353b-107">Você pode executar **Test-CsUcwaConference** para testar a capacidade de dois usuários que estão usando clientes móveis do Lync 2013 para criar, ingressar e se comunicar em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="e353b-107">You can run **Test-CsUcwaConference** to test the ability of two users who are using Lync 2013 Mobile clients to create, join and communicate in a conference.</span></span> <span data-ttu-id="e353b-108">Para usar essa transação de teste, você precisa de dois usuários reais ou usuários de teste e suas credenciais completas.</span><span class="sxs-lookup"><span data-stu-id="e353b-108">To use this test transaction, you need two actual users or test users, and their full credentials.</span></span>

<span data-ttu-id="e353b-109">Use **Test-CsMcxP2PIM** para testar o envio de uma mensagem instantânea entre dois usuários que estão usando o Lync 2010 Mobile.</span><span class="sxs-lookup"><span data-stu-id="e353b-109">You use **Test-CsMcxP2PIM** to test sending an instant message between two users who are using Lync 2010 Mobile.</span></span> <span data-ttu-id="e353b-110">Semelhante a **Test-CsUcwaConference**, você usa dois usuários reais ou dois usuários de teste predefinidos.</span><span class="sxs-lookup"><span data-stu-id="e353b-110">Similar to **Test-CsUcwaConference**, you use two actual users or two predefined test users.</span></span>

<div>

## <a name="to-test-conferencing-for-lync-2013-mobile-clients"></a><span data-ttu-id="e353b-111">Para testar a conferência para clientes móveis do Lync 2013</span><span class="sxs-lookup"><span data-stu-id="e353b-111">To test conferencing for Lync 2013 Mobile clients</span></span>

1.  <span data-ttu-id="e353b-112">Faça logon como membro da função CsAdministrator em qualquer computador onde o Shell de Gerenciamento do Lync Server e o Ocscore estiverem instalados.</span><span class="sxs-lookup"><span data-stu-id="e353b-112">Log on as a member of the CsAdministrator role on any computer where Lync Server Management Shell and Ocscore are installed.</span></span>

2.  <span data-ttu-id="e353b-113">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e353b-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e353b-114">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="e353b-114">At the command line, type:</span></span>
    
        Test-CsUcwaConference -TargetFqdn <FQDN of Front End pool> -Authentication <TrustedServer | Negotiate | ClientCertificate | LiveID> -OrganizerSipAddress sip:<SIP address of test user 1> -OrganizerCredential <test user 1 credentials> -ParticipantSipAddress sip:<SIP address of test user 2> -ParticipantCredential <test user 2 credentials> -v
    
    <span data-ttu-id="e353b-115">Você pode definir credenciais em um script e passá-las para o cmdlet de teste.</span><span class="sxs-lookup"><span data-stu-id="e353b-115">You can set credentials in a script and pass them to the test cmdlet.</span></span> <span data-ttu-id="e353b-116">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e353b-116">For example:</span></span>
    
        $passwd1 = ConvertTo-SecureString "Password01" -AsPlainText -Force
        $passwd2 = ConvertTo-SecureString "Password02" -AsPlainText -Force
        $testuser1 = New-Object Management.Automation.PSCredential("contoso\UserName1", $passwd1)
        $testuser2 = New-Object Management.Automation.PSCredential("contoso\UserName2", $passwd2)
        Test-CsUcwaConference -TargetFqdn pool01.contoso.com -Authentication Negotiate -OrganizerSipAddress sip:UserName1@contoso.com -OrganizerCredential $testuser1 -ParticipantSipAddress sip:UserName2@contoso.com -ParticipantCredential $testuser2 -v

</div>

<div>

## <a name="to-test-person-to-person-instant-messaging-im-for-lync-2010-mobile"></a><span data-ttu-id="e353b-117">Para testar o sistema de mensagens instantâneas de pessoa para pessoa (IM) para o Lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="e353b-117">To test person-to-person instant messaging (IM) for Lync 2010 Mobile</span></span>

1.  <span data-ttu-id="e353b-118">Faça logon como membro da função CsAdministrator em qualquer computador onde o Shell de Gerenciamento do Lync Server e o Ocscore estiverem instalados.</span><span class="sxs-lookup"><span data-stu-id="e353b-118">Log on as a member of the CsAdministrator role on any computer where Lync Server Management Shell and Ocscore are installed.</span></span>

2.  <span data-ttu-id="e353b-119">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e353b-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e353b-120">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="e353b-120">At the command line, type:</span></span>
    
        Test-CsMcxP2PIM -TargetFqdn <FQDN of Front End pool> -Authentication <TrustedServer | Negotiate | ClientCertificate | LiveID> -SenderSipAddress sip:<SIP address of test user 1> -SenderCredential <test user 1 credentials> -ReceiverSipAddress sip:<SIP address of test user 2> -ReceiverCredential <test user 2 credentials> -v
    
    <span data-ttu-id="e353b-121">Você pode definir credenciais em um script e passá-las para o cmdlet de teste.</span><span class="sxs-lookup"><span data-stu-id="e353b-121">You can set credentials in a script and pass them to the test cmdlet.</span></span> <span data-ttu-id="e353b-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e353b-122">For example:</span></span>
    
        $passwd1 = ConvertTo-SecureString "Password01" -AsPlainText -Force
        $passwd2 = ConvertTo-SecureString "Password02" -AsPlainText -Force
        $tuc1 = New-Object Management.Automation.PSCredential("contoso\UserName1", $passwd1)
        $tuc2 = New-Object Management.Automation.PSCredential("contoso\UserName2", $passwd2)
        Test-CsMcxP2PIM -TargetFqdn pool01.contoso.com -Authentication Negotiate -SenderSipAddress sip:UserName1@contoso.com -SenderCredential $tuc1 -ReceiverSipAddress sip:UserName2@contoso.com -ReceiverCredential $tuc2 -v

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e353b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e353b-123">See Also</span></span>


[<span data-ttu-id="e353b-124">Test-CsMcxP2PIM</span><span class="sxs-lookup"><span data-stu-id="e353b-124">Test-CsMcxP2PIM</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM)  
[<span data-ttu-id="e353b-125">Test-CsUcwaConference</span><span class="sxs-lookup"><span data-stu-id="e353b-125">Test-CsUcwaConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference)  
  

<span data-ttu-id="e353b-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e353b-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

