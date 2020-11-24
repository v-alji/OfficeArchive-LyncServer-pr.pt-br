---
title: 'Lync Server 2013: relatório de lista de falhas'
description: 'Lync Server 2013: relatório de lista de falhas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure List Report
ms:assetid: b6f3a605-e0c6-461e-b17a-41d8039ace9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615446(v=OCS.15)
ms:contentKeyID: 48185194
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7467144fe207ab61fd086cd35aac74779fd4f771
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389782"
---
# <a name="failure-list-report-in-lync-server-2013"></a><span data-ttu-id="9a04e-103">Relatório lista de falhas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a04e-103">Failure List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a04e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a04e-104">

<span> </span></span></span>

<span data-ttu-id="9a04e-105">_**Tópico da última modificação:** 2012-07-02_</span><span class="sxs-lookup"><span data-stu-id="9a04e-105">_**Topic Last Modified:** 2012-07-02_</span></span>

<span data-ttu-id="9a04e-p101">O Relatório da lista de falhas fornece informações sobre os participantes individuais de uma sessão de conferência ou ponto a ponto com falha. Essas informações incluem o URI do usuário que teve o problema, bem como o código de resposta SIP e o ID de diagnóstico associado à falha.</span><span class="sxs-lookup"><span data-stu-id="9a04e-p101">The Failure List report provides information about the individual participants who took part in a failed peer-to-peer or conferencing session. This information includes the URI of the user who experienced the problem, as well as the SIP Response code and Diagnostic ID associated with the failure.</span></span>

<div>

## <a name="accessing-the-failure-list-report"></a><span data-ttu-id="9a04e-108">Acessando o Relatório da lista de falhas</span><span class="sxs-lookup"><span data-stu-id="9a04e-108">Accessing the Failure List Report</span></span>

<span data-ttu-id="9a04e-109">O relatório lista de falhas é acessado clicando em qualquer uma das seguintes métricas no [relatório distribuição de falha no Lync Server 2013](lync-server-2013-failure-distribution-report.md):</span><span class="sxs-lookup"><span data-stu-id="9a04e-109">The Failure List Report is accessed by clicking any of the following metrics on the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md):</span></span>

  - <span data-ttu-id="9a04e-110">Principais motivos diagnósticos (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-110">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="9a04e-111">Principais modalidades (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-111">Top modalities (sessions)</span></span>

  - <span data-ttu-id="9a04e-112">Principais pools (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-112">Top pools (sessions)</span></span>

  - <span data-ttu-id="9a04e-113">Principais fontes (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-113">Top sources (sessions)</span></span>

  - <span data-ttu-id="9a04e-114">Principais componentes (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-114">Top components (sessions)</span></span>

  - <span data-ttu-id="9a04e-115">Principais usuários "De" (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-115">Top from users (sessions)</span></span>

  - <span data-ttu-id="9a04e-116">Principais usuários "Para" (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-116">Top to users (sessions)</span></span>

  - <span data-ttu-id="9a04e-117">Principais agentes do usuários "De" (sessões)</span><span class="sxs-lookup"><span data-stu-id="9a04e-117">Top from user agents (sessions)</span></span>

<span data-ttu-id="9a04e-118">No relatório lista de falhas, você pode acessar o [relatório de detalhes da sessão ponto a ponto no Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) clicando na métrica de detalhes da sessão de uma sessão ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="9a04e-118">From the Failure List Report you can access the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) by clicking the Session detail metric for a peer-to-peer session.</span></span> <span data-ttu-id="9a04e-119">Você também pode acessar o Relatório de detalhes da conferência clicando na métrica Conferência de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="9a04e-119">You can also access the Conference Detail Report by clicking the Conference metric for a conference.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-failure-list-report"></a><span data-ttu-id="9a04e-120">Aprimorando o uso do Relatório da lista de falhas</span><span class="sxs-lookup"><span data-stu-id="9a04e-120">Making the Best Use of the Failure List Report</span></span>

<span data-ttu-id="9a04e-p103">No Relatório da lista de falhas, é possível visualizar uma descrição para cada código de resposta ou cada ID de diagnóstico simplesmente passando o mouse sobre o valor em questão. Por exemplo, se você passar o mouse sobre o ID de diagnóstico 7025, verá a seguinte mensagem em uma dica de ferramenta:</span><span class="sxs-lookup"><span data-stu-id="9a04e-p103">In the Failure List Report, you can view a description for each Response code or each Diagnostic ID simply by holding your mouse over that value. For example, if you hold your mouse over Diagnostic ID 7025 you'll see the following displayed in a tooltip:</span></span>

<span data-ttu-id="9a04e-123">Internal server error creating media for user.</span><span class="sxs-lookup"><span data-stu-id="9a04e-123">Internal server error creating media for user.</span></span>

<span data-ttu-id="9a04e-124">É importante notar que o Relatório da lista de falhas não fornece uma maneira simples de recuperar diretamente uma lista de todos os usuários que participaram de pelo menos uma sessão com falha, nem fornece uma maneira de determinar quais usuários geralmente estavam envolvidos em uma sessão com falha.</span><span class="sxs-lookup"><span data-stu-id="9a04e-124">It's important to note that the Failure List Report does not provide a straightforward way to directly retrieve a list of all the users who participated in at least one failed session, nor does it provide a way to determine which users were most-often involved in a failed session.</span></span> <span data-ttu-id="9a04e-125">(Por um motivo, o relatório lista de falhas não tem funcionalidades de filtragem.) No entanto, se exportar os dados e convertê-los em um arquivo de valores separados por vírgula, você poderá usar o Windows PowerShell para encontrar as respostas a perguntas como essas.</span><span class="sxs-lookup"><span data-stu-id="9a04e-125">(For one thing, the Failure List Report has no filtering capabilities.) However, if you export the data and then convert it to a comma-separated values file, you can use Windows PowerShell to find the answers to questions like those.</span></span> <span data-ttu-id="9a04e-126">Por exemplo, suponha que você salve os dados em um. Arquivo CSV denominado C: \\ falha de dados \\ \_List.csv.</span><span class="sxs-lookup"><span data-stu-id="9a04e-126">For example, suppose you save the data to a .CSV file named C:\\Data\\Failure\_List.csv.</span></span> <span data-ttu-id="9a04e-127">Com base nos dados salvos nesse arquivo, esse comando lista os usuários que estavam envolvidos em pelo menos uma sessão com falha:</span><span class="sxs-lookup"><span data-stu-id="9a04e-127">Based on the data saved in that file, this command lists all the users who were involved in at least one failed session:</span></span>

    $failures = Import-Csv -Path " C:\Data\Failure_List.csv"
    $failure |Sort-Object "From user" | Select-Object "From user" -Unique

<span data-ttu-id="9a04e-128">Esse comando retornará uma lista semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="9a04e-128">That command will return a list similar to this:</span></span>

    From user
    ----
    Pilar.Ackerman@litwareinc.com
    Henrik.Jensen@litwareinc.com
    Gilead.Amosnino@litwareinc.com
    David.Ahs@litwareinc.com
    Ken.Myer@litwareinc.com

<span data-ttu-id="9a04e-129">Esses dois comandos relatam o número total de sessões com falha em que cada usuário estava envolvido:</span><span class="sxs-lookup"><span data-stu-id="9a04e-129">These two commands report back the total number of failed sessions that each user was involved in:</span></span>

    $failures = Import-Csv -Path "C:\Data\Failure_List.csv"
    $failures | Group-Object "From user" | Select-Object Count, Name | Sort-Object -Property Count -Descending

<span data-ttu-id="9a04e-130">Serão retornados dados semelhantes a estes:</span><span class="sxs-lookup"><span data-stu-id="9a04e-130">That will return data similar to this:</span></span>

    Count    Name
     -----    ----
        20    Pilar.Ackerman@litwareinc.com
        20    David.Ahs@litwareinc.com
        16    Gilead.Amosnino@litwareinc.com
        16    Ken.Myero@litwareinc.com
        14    Henrik.Jensen@litwareinc.com

</div>

<div>

## <a name="filters"></a><span data-ttu-id="9a04e-131">Filtros</span><span class="sxs-lookup"><span data-stu-id="9a04e-131">Filters</span></span>

<span data-ttu-id="9a04e-p105">Nenhum. Não é possível filtrar o Relatório de Lista de Falhas.</span><span class="sxs-lookup"><span data-stu-id="9a04e-p105">None. You cannot filter the Failure List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="9a04e-134">Métricas</span><span class="sxs-lookup"><span data-stu-id="9a04e-134">Metrics</span></span>

<span data-ttu-id="9a04e-135">A tabela a seguir lista as informações fornecidas no Relatório de Lista de Falhas para cada chamada mal-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9a04e-135">The following table lists the information provided in the Failure List Report for each failed call.</span></span>

### <a name="failure-list-report-metrics"></a><span data-ttu-id="9a04e-136">Métricas do Relatório de Lista de Falhas</span><span class="sxs-lookup"><span data-stu-id="9a04e-136">Failure List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a04e-137">Nome</span><span class="sxs-lookup"><span data-stu-id="9a04e-137">Name</span></span></th>
<th><span data-ttu-id="9a04e-138">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="9a04e-138">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="9a04e-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a04e-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a04e-140"><strong>Hora de relatório</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-140"><strong>Reported time</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-141">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-141">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-142">Data e hora do registro do relatório.</span><span class="sxs-lookup"><span data-stu-id="9a04e-142">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a04e-143"><strong>Solicitação</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-143"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-144">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-144">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-p106">Tipo de solicitação SIP que falhou. Por exemplo, CONVIDAR ou ATÉ LOGO.</span><span class="sxs-lookup"><span data-stu-id="9a04e-p106">SIP request type that failed. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a04e-147"><strong>Código da resposta</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-147"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-148">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-148">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-149">Código da resposta SIP enviado quando a conferência falhou.</span><span class="sxs-lookup"><span data-stu-id="9a04e-149">SIP response code sent when the conference failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a04e-150"><strong>ID do Diagnóstico</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-150"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-151">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-151">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-152">Identificador exclusivo (na forma de um cabeçalho de diagnóstico-ms) anexado a uma mensagem SIP que fornece informações úteis sobre os erros de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="9a04e-152">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a04e-153"><strong>Join cost time (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-153"><strong>Join cost time (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-154">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-154">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-155">Tempo (em milissegundos) necessário para o usuário participar da conferência.</span><span class="sxs-lookup"><span data-stu-id="9a04e-155">Amount of time (in milliseconds) required for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a04e-156"><strong>Usuário "De"</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-156"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-157">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-157">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-158">Endereço SIP do usuário que iniciou a chamada.</span><span class="sxs-lookup"><span data-stu-id="9a04e-158">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a04e-159"><strong>Agente do usuário de origem</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-159"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-160">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-160">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-161">Software usado pelo ponto de extremidade do usuário que iniciou a chamada.</span><span class="sxs-lookup"><span data-stu-id="9a04e-161">Software used by the endpoint of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a04e-162"><strong>Usuário "Para"</strong></span><span class="sxs-lookup"><span data-stu-id="9a04e-162"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="9a04e-163">Não</span><span class="sxs-lookup"><span data-stu-id="9a04e-163">No</span></span></p></td>
<td><p><span data-ttu-id="9a04e-164">Endereço SIP do usuário que estava recebendo a chamada.</span><span class="sxs-lookup"><span data-stu-id="9a04e-164">SIP address of the user who was being called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9a04e-165">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a04e-165">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

