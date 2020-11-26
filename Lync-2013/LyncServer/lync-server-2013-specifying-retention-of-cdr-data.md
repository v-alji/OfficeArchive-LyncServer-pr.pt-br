---
title: 'Lync Server 2013: especificando a retenção de dados de CDR'
description: 'Lync Server 2013: especificando a retenção de dados CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Specifying retention of CDR data
ms:assetid: c0fd6056-87bc-4136-902a-f1b37cd3a1ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182581(v=OCS.15)
ms:contentKeyID: 48185299
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9367721a2390ad701702818590ac14e69da0df9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423782"
---
# <a name="specifying-retention-of-cdr-data-in-lync-server-2013"></a><span data-ttu-id="7c60c-103">Especificando a retenção de dados de CDR no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c60c-103">Specifying retention of CDR data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c60c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c60c-104">

<span> </span></span></span>

<span data-ttu-id="7c60c-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="7c60c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="7c60c-p101">Por padrão, os dados de CDR (registro de detalhes das chamadas) são purgados após 60 dias. É possível usar as configurações da página **Registro de Detalhes das Chamadas** para manter os dados por um período maior ou menor. Se você desabilitar o CDR, os dados que foram capturados antes da desabilitação do CDR também poderão ser purgados.</span><span class="sxs-lookup"><span data-stu-id="7c60c-p101">By default, call detail recording (CDR) data is purged after 60 days. You can use the settings on the **Call Detail Recording** page to retain the data for a longer or shorter period of time. If you disable CDR, data that was captured before CDR was enabled will also be subject to purging.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7c60c-p102">Você deve configurar o CDR e a QoE (Qualidade da Experiência) para reter os dados durante o mesmo número de dias. Cada chamada nos CDRs (relatórios de detalhes de chamada), disponível na página da web de Relatórios do Monitoring Serve, inclui informações de CDR e QoE. Se a duração da limpeza de CDR e QoE for diferente, algumas chamadas poderão incluir apenas dados de CDR, enquanto outras poderão incluir apenas dados de QoE.</span><span class="sxs-lookup"><span data-stu-id="7c60c-p102">You should configure CDR and Quality of Experience (QoE) to retain data for the same number of days. Each call in the call detail reports (CDRs), available from the Monitoring Server Reports webpage, includes CDR and QoE information. If the purging duration for CDR and QoE is different, some calls might only include CDR data, while other may only include QoE data.</span></span>



</div>

<span data-ttu-id="7c60c-112">Use o procedimento a seguir para definir as configurações de limpeza de dados de CDR.</span><span class="sxs-lookup"><span data-stu-id="7c60c-112">Use the following procedures to configure purge settings for CDR data.</span></span>

<div>

## <a name="to-specify-retention-of-cdr-data"></a><span data-ttu-id="7c60c-113">Para especificar a retenção de dados de CDR</span><span class="sxs-lookup"><span data-stu-id="7c60c-113">To specify retention of CDR data</span></span>

1.  <span data-ttu-id="7c60c-114">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7c60c-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="7c60c-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7c60c-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7c60c-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7c60c-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7c60c-117">Na barra de navegação esquerda, clique em **Monitoramento e Arquivamento** e clique em **Registro de Detalhes de Chamada**.</span><span class="sxs-lookup"><span data-stu-id="7c60c-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="7c60c-118">Na página **Registro de Detalhes de Chamada**, clique no site apropriado na tabela, clique em **Editar** e em **Mostrar Detalhes**.</span><span class="sxs-lookup"><span data-stu-id="7c60c-118">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="7c60c-119">Para ativar a limpeza, selecione **Habilitar limpeza CDRs**.</span><span class="sxs-lookup"><span data-stu-id="7c60c-119">To turn on purging, select **Enable purging of CDRs**.</span></span>

6.  <span data-ttu-id="7c60c-120">Em **Manter CDRs por um período máximo (dias):** selecione o número máximo de dias que os registros de detalhes de chamada devem ser retidos.</span><span class="sxs-lookup"><span data-stu-id="7c60c-120">In **Keep CDRs for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="7c60c-121">Em **Manter dados de relatório de erros por um período máximo de (dias):** selecione o número máximo de dias que os relatórios de erros devem ser retidos.</span><span class="sxs-lookup"><span data-stu-id="7c60c-121">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="7c60c-122">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="7c60c-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="specifying-cdr-retention-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="7c60c-123">Especificando a retenção de CDR usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c60c-123">Specifying CDR Retention by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="7c60c-124">Você pode criar configurações de retenção de CDR usando o Windows PowerShell e o cmdlet Set-CsCdrConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7c60c-124">You can create CDR retention settings by using Windows PowerShell and the Set-CsCdrConfiguration cmdlet.</span></span> <span data-ttu-id="7c60c-125">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c60c-125">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="7c60c-126">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="7c60c-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-specify-cdr-retention-for-a-specific-location"></a><span data-ttu-id="7c60c-127">Para especificar a retenção de CDR para um local específico</span><span class="sxs-lookup"><span data-stu-id="7c60c-127">To specify CDR retention for a specific location</span></span>

  - <span data-ttu-id="7c60c-128">Este comando habilita a exclusão de dados CDR para o local Redmond e configura o local para manter os dados CDR e os dados do relatório de erro por 20 dias.</span><span class="sxs-lookup"><span data-stu-id="7c60c-128">This command enables purging of CDR data for the Redmond site, and configures the site to maintain both CDR data and error reports data for 20 days.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<div>

## <a name="to-specify-cdr-retention-for-multiple-locations"></a><span data-ttu-id="7c60c-129">Para especificar a retenção CDR para vários locais</span><span class="sxs-lookup"><span data-stu-id="7c60c-129">To specify CDR retention for multiple locations</span></span>

  - <span data-ttu-id="7c60c-130">Este comando configura a retenção CDR para todas as definições de configuração CDR em uso em uma organização.</span><span class="sxs-lookup"><span data-stu-id="7c60c-130">This command configures CDR retention for all the CDR configuration settings in use in an organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration-EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<span data-ttu-id="7c60c-131">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="7c60c-131">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7c60c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c60c-132">See Also</span></span>


[<span data-ttu-id="7c60c-133">Registro de detalhes de chamadas (CDR) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c60c-133">Call detail recording (CDR) in Lync Server 2013</span></span>](lync-server-2013-call-detail-recording-cdr.md)  
  

<span data-ttu-id="7c60c-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c60c-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

