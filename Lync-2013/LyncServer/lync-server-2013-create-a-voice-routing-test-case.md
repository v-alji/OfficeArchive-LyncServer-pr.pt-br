---
title: 'Lync Server 2013: Criar um caso de teste de roteamento de voz'
description: 'Lync Server 2013: criar um caso de teste de roteamento de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a voice routing test case
ms:assetid: 43a07a5b-2f20-462a-81e5-d628c18391e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425935(v=OCS.15)
ms:contentKeyID: 48183979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d81f4d39a6e3972ebf036fdaca59936f3f6b86bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432034"
---
# <a name="create-a-voice-routing-test-case-in-lync-server-2013"></a><span data-ttu-id="5d759-103">Criar um caso de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d759-103">Create a voice routing test case in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d759-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d759-104">

<span> </span></span></span>

<span data-ttu-id="5d759-105">_**Tópico da última modificação:** 2014-02-07_</span><span class="sxs-lookup"><span data-stu-id="5d759-105">_**Topic Last Modified:** 2014-02-07_</span></span>

<div>

## <a name="to-create-a-test-case"></a><span data-ttu-id="5d759-106">Para criar um caso de teste</span><span class="sxs-lookup"><span data-stu-id="5d759-106">To create a test case</span></span>

1.  <span data-ttu-id="5d759-107">Faça logon no computador como um membro do grupo RTCUniversalServerAdmins ou como um membro da função CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="5d759-107">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="5d759-108">Para obter detalhes, consulte [delegar permissões de configuração no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="5d759-108">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="5d759-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d759-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5d759-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5d759-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5d759-111">Na barra de navegação à esquerda, clique em **Roteamento de voz** e, em seguida, clique em **testar roteamento de voz**.</span><span class="sxs-lookup"><span data-stu-id="5d759-111">In the left navigation bar, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

4.  <span data-ttu-id="5d759-112">Na página **testar roteamento de voz** , clique em **novo** para criar um novo caso de teste.</span><span class="sxs-lookup"><span data-stu-id="5d759-112">On the **Test Voice Routing** page, click **New** to create a new test case.</span></span>

5.  <span data-ttu-id="5d759-113">Em **nome**, digite um nome exclusivo para o caso de teste.</span><span class="sxs-lookup"><span data-stu-id="5d759-113">In **Name**, type in a unique name for the test case.</span></span>
    
    <span data-ttu-id="5d759-114">O nome deve ser exclusivo entre todos os casos de teste de roteamento de voz na sua implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="5d759-114">The name must be unique among all voice routing test cases in your Enterprise Voice deployment.</span></span> <span data-ttu-id="5d759-115">Pode ter até 32 caracteres de comprimento e pode conter qualquer caractere alfanumérico, além da barra invertida ( \\ ), ponto final (.) ou sublinhado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="5d759-115">It can be up to 32 characters in length and may contain any alphanumeric characters, in addition to the backslash (\\), period (.), or underscore (\_).</span></span>

6.  <span data-ttu-id="5d759-116">Em **número para testar**, digite o número discado que você deseja usar para testar a configuração de roteamento que você especificar para este caso de teste.</span><span class="sxs-lookup"><span data-stu-id="5d759-116">In **Dialed number to test**, type in the dialed number that you want to use to test the routing configuration that you specify for this test case.</span></span> <span data-ttu-id="5d759-117">Com base no plano de discagem, na rota e na política de voz, esse número será normalizado e exibido como saída.</span><span class="sxs-lookup"><span data-stu-id="5d759-117">Based on the dial plan, route, and voice policy, this number will be normalized and displayed as output.</span></span>

7.  <span data-ttu-id="5d759-118">Na lista **plano de discagem** , selecione o plano de discagem a ser usado ao executar o teste.</span><span class="sxs-lookup"><span data-stu-id="5d759-118">In the **Dial Plan** list, select the dial plan to use when running the test.</span></span> <span data-ttu-id="5d759-119">Padrão é o plano de discagem global.</span><span class="sxs-lookup"><span data-stu-id="5d759-119">Default is the Global dial plan.</span></span>

8.  <span data-ttu-id="5d759-120">Na lista **política de voz** , selecione a política de voz a ser usada ao executar o teste.</span><span class="sxs-lookup"><span data-stu-id="5d759-120">In the **Voice Policy** list, select the voice policy to use when running the test.</span></span> <span data-ttu-id="5d759-121">Padrão é a política de voz global.</span><span class="sxs-lookup"><span data-stu-id="5d759-121">Default is the Global voice policy.</span></span>

9.  <span data-ttu-id="5d759-122">Na **tradução esperada**, digite o número de telefone no formato que você espera que ele seja exibido após a tradução.</span><span class="sxs-lookup"><span data-stu-id="5d759-122">In **Expected translation**, type in the phone number in the format you expect to see it after translation.</span></span> <span data-ttu-id="5d759-123">Esse é o valor do número de telefone que você está testando depois que ele foi traduzido pela primeira regra de normalização que corresponde ao plano de discagem selecionado.</span><span class="sxs-lookup"><span data-stu-id="5d759-123">This is the value of the phone number that you are testing after it has been translated by the first normalization rule that matches in the selected dial plan.</span></span> <span data-ttu-id="5d759-124">Quando você executar o caso de teste, se o número que você está testando não resultar no valor na **conversão esperada**, o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="5d759-124">When you run the test case, if the number you are testing does not result in the value in **Expected translation**, the test fails.</span></span>

10. <span data-ttu-id="5d759-125">Adicionais Na lista de **uso de PSTN esperado** , você pode selecionar o registro de uso da rede de telefonia pública comutada (PSTN) que você espera usar quando executar o caso de teste, com base no plano de discagem e na política de voz especificados.</span><span class="sxs-lookup"><span data-stu-id="5d759-125">(Optional) In the **Expected PSTN usage** list, you can select the public switched telephone network (PSTN) usage record that you expect to be used when you run the test case, based on the specified dial plan and voice policy.</span></span> <span data-ttu-id="5d759-126">Se um registro de uso PSTN diferente for usado, o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="5d759-126">If a different PSTN usage record is used, the test fails.</span></span>

11. <span data-ttu-id="5d759-127">Adicionais Na lista de **rotas esperadas** , você pode selecionar a rota de voz que espera usar quando executar o caso de teste, com base no plano de discagem e na política de voz especificados.</span><span class="sxs-lookup"><span data-stu-id="5d759-127">(Optional) In the **Expected route** list, you can select the voice route that you expect to be used when you run the test case, based on the specified dial plan and voice policy.</span></span> <span data-ttu-id="5d759-128">Se for usada uma rota de voz diferente, o teste falhará.</span><span class="sxs-lookup"><span data-stu-id="5d759-128">If a different voice route is used, the test fails.</span></span>

12. <span data-ttu-id="5d759-129">Adicionais Clique em **executar** para executar o caso de teste.</span><span class="sxs-lookup"><span data-stu-id="5d759-129">(Optional) Click **Run** to run the test case.</span></span> <span data-ttu-id="5d759-130">Os resultados são mostrados no painel direito da página.</span><span class="sxs-lookup"><span data-stu-id="5d759-130">The results are shown in the right panel of the page.</span></span>

13. <span data-ttu-id="5d759-131">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d759-131">Click **OK**.</span></span>

14. <span data-ttu-id="5d759-132">Clique em **Confirmar** e, em seguida, clique em **Confirmar tudo**.</span><span class="sxs-lookup"><span data-stu-id="5d759-132">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5d759-133">Sempre que criar um caso de teste de roteamento de voz, você deve executar o comando <STRONG>Commit All</STRONG> para publicar a alteração de configuração.</span><span class="sxs-lookup"><span data-stu-id="5d759-133">Whenever you create a voice routing test case, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="5d759-134">Para obter detalhes, consulte <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">publicar alterações pendentes na configuração de roteamento de voz no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="5d759-134">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="5d759-135">Se o plano de discagem que está sendo empregado no teste normalizar números de telefone que comecem com um sinal de adição (por exemplo, + 12065551219), esse plano pode causar falha no teste de roteamento de voz.</span><span class="sxs-lookup"><span data-stu-id="5d759-135">If the dial plan being employed in the test normalizes phone numbers that begin with a plus sign (for example, +12065551219), that plan might cause the voice routing test to fail.</span></span> <span data-ttu-id="5d759-136">(O plano de discagem e a rota de voz funcionarão; na verdade, Test-CsDialPlan será bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5d759-136">(The dial plan and the voice route will work; in fact, Test-CsDialPlan will succeed.</span></span> <span data-ttu-id="5d759-137">No entanto, o teste de roteamento de voz pode falhar.) Isso é algo a ter em mente ao testar rotas de voz.</span><span class="sxs-lookup"><span data-stu-id="5d759-137">However, the voice routing test might fail.) This is something to keep in mind when testing voice routes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5d759-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d759-138">See Also</span></span>


[<span data-ttu-id="5d759-139">Exportar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d759-139">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)  
[<span data-ttu-id="5d759-140">Importar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d759-140">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  


[<span data-ttu-id="5d759-141">Configurando planos de discagem no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d759-141">Configuring dial plans in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-plans.md)  
[<span data-ttu-id="5d759-142">Configurar políticas de voz, registros de uso de PSTN e rotas de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d759-142">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)  
  

<span data-ttu-id="5d759-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d759-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

