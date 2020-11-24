---
title: 'Lync Server 2013: relatório de registro do usuário'
description: 'Lync Server 2013: relatório de registro do usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User Registration Report
ms:assetid: 151d5cc9-cc1b-4cfa-be9c-55ebe321f7a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558614(v=OCS.15)
ms:contentKeyID: 48183486
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adb8ef7e94a24f0fd088f12e009fc9d63f3be9d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389944"
---
# <a name="user-registration-report-in-lync-server-2013"></a><span data-ttu-id="ded37-103">Relatório de registro de usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ded37-103">User Registration Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ded37-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ded37-104">

<span> </span></span></span>

<span data-ttu-id="ded37-105">_**Tópico da última modificação:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="ded37-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="ded37-106">O relatório de registro de usuário fornece uma visão geral da atividade de logon do usuário, principalmente as informações sobre o número de usuários que se conectaram ao Microsoft Lync Server 2013 durante um período de tempo especificado (hora, diária, semanal, mensal).</span><span class="sxs-lookup"><span data-stu-id="ded37-106">The User Registration Report provides an overview of user logon activity, most notably information about the number of users who logged on to Microsoft Lync Server 2013 during a specified time period (hourly, daily, weekly, monthly).</span></span> <span data-ttu-id="ded37-107">Lembre-se de que o relatório mostra apenas quantas pessoas fizeram logon.</span><span class="sxs-lookup"><span data-stu-id="ded37-107">Keep in mind that the report only tells you how many people logged on.</span></span> <span data-ttu-id="ded37-108">Ele não mostra *quais* pessoas fizeram logon.</span><span class="sxs-lookup"><span data-stu-id="ded37-108">It does not tell you *which* people logged on.</span></span> <span data-ttu-id="ded37-109">Os relatórios de monitoramento não fornecem informações sobre quais usuários específicos estão usando o Lync Server 2013 (e quais não são).</span><span class="sxs-lookup"><span data-stu-id="ded37-109">Monitoring Reports do not provide information about which specific users are using Lync Server 2013 (and which ones are not).</span></span> <span data-ttu-id="ded37-110">No entanto, você pode obter uma estimativa aproximada de informações de usuário usando o Relatório de Atividades de Usuário.</span><span class="sxs-lookup"><span data-stu-id="ded37-110">However, you can get a rough estimate of user information by using the User Activity Report.</span></span>

<span data-ttu-id="ded37-111">Ao fornecer informações sobre logons de usuários, o Relatório de Registro de Usuário faz duas distinções importantes.</span><span class="sxs-lookup"><span data-stu-id="ded37-111">When providing information about user logons, the User Registration Report draws two important distinctions.</span></span> <span data-ttu-id="ded37-112">Primeiro, ele desdobra os logons em duas categorias primárias: logons internos e logons externos.</span><span class="sxs-lookup"><span data-stu-id="ded37-112">First, it breaks logons down into two primary categories: internal logons and external logons.</span></span> <span data-ttu-id="ded37-113">Logons internos representam usuários que fizeram logon de dentro do firewall de sua organização (isto é, enquanto estavam conectados à rede corporativa).</span><span class="sxs-lookup"><span data-stu-id="ded37-113">Internal logons represent users who logged on from inside your organization's firewall (that is, while connected to the corporate network).</span></span> <span data-ttu-id="ded37-114">Os logons externos representam os usuários que fizeram logon de fora do firewall por meio de um servidor de borda (por exemplo, um usuário que fez logon de um café da Internet conta como um logon externo).</span><span class="sxs-lookup"><span data-stu-id="ded37-114">External logons represent users who logged on from outside the firewall through an Edge Server (for example, a user who logged on from an Internet café counts as an external logon).</span></span> <span data-ttu-id="ded37-115">Caso precise saber quantos de seus usuários estão fazendo logon de fora do firewall, o Relatório de Registro de Usuário pode fornecer essa informação.</span><span class="sxs-lookup"><span data-stu-id="ded37-115">If you need to know how many of your users are logging on from outside the firewall, the User Registration Report can provide you with this information.</span></span>

<span data-ttu-id="ded37-116">Além disso, o Relatório de Registro de Usuário indica quantos usuários *ativos* estavam presentes durante um dado período de tempo.</span><span class="sxs-lookup"><span data-stu-id="ded37-116">In addition, the User Registration Report notes how many *active* users were present during a given time period.</span></span> <span data-ttu-id="ded37-117">Um usuário ativo é um usuário que fez parte de uma sessão de mensagens instantâneas (IM), participou em uma reunião do Lync, fez ou recebeu uma chamada telefônica ou, de outra forma, usava o Lync Server durante esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="ded37-117">An active user is a user who took part in an instant messaging (IM) session, participated in a Lync Meeting, made or received a phone call, or otherwise used Lync Server during that period of time.</span></span> <span data-ttu-id="ded37-118">Isso é diferente de um usuário que fez logon mas nunca usou o sistema de fato.</span><span class="sxs-lookup"><span data-stu-id="ded37-118">This is different from a user who logged on, but never actually used the system.</span></span>

<div>

## <a name="accessing-the-user-registration-report"></a><span data-ttu-id="ded37-119">Acessando o Relatório de Registro de Usuário</span><span class="sxs-lookup"><span data-stu-id="ded37-119">Accessing the User Registration Report</span></span>

<span data-ttu-id="ded37-p104">Você acessa o Relatório de Registro de Usuário apenas a partir da home page de Relatórios de Monitoramento. O Relatório de Registro de Usuário não vincula nenhum outro relatório.</span><span class="sxs-lookup"><span data-stu-id="ded37-p104">You access the User Registration Report only from the Monitoring Reports home page. The User Registration Report does not link to any other reports.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-user-registration-report"></a><span data-ttu-id="ded37-122">Usando o Relatório de Registro de Usuário da melhor maneira possível</span><span class="sxs-lookup"><span data-stu-id="ded37-122">Making the Best Use of the User Registration Report</span></span>

<span data-ttu-id="ded37-123">Depois de implantar o Lync Server, uma pergunta comumente: como posso saber se meus usuários estão realmente usando essa nova tecnologia?</span><span class="sxs-lookup"><span data-stu-id="ded37-123">After you've deployed Lync Server one commonly-asked question is this: How do I know if my users are actually using this new technology?</span></span> <span data-ttu-id="ded37-124">Embora tenha algumas limitações neste sentido, o Relatório de Registro de Usuário ajuda você a responder essa pergunta.</span><span class="sxs-lookup"><span data-stu-id="ded37-124">Although it has a few limitations in this regard, the User Registration Report can help you answer this question.</span></span> <span data-ttu-id="ded37-125">Para determinar se os usuários estão usando o Lync Server, você precisa fazer duas coisas.</span><span class="sxs-lookup"><span data-stu-id="ded37-125">To determine whether or not users are using Lync Server, you need to do two things.</span></span> <span data-ttu-id="ded37-126">Primeiro, obtenha o valor da métrica de Usuários de logon exclusivos, do Relatório de Registro de Usuário.</span><span class="sxs-lookup"><span data-stu-id="ded37-126">First, get the value of the Unique logon users metric from the User Registration Report.</span></span> <span data-ttu-id="ded37-127">Esse valor informa quantos indivíduos distintos estão conectados ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ded37-127">This value tells you how many distinct individuals logged on to Lync Server.</span></span>

<span data-ttu-id="ded37-128">Por comparação, a métrica de logons totais mostra quantas vezes todos se conectaram ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ded37-128">By comparison, the Total logons metric shows how many total times anyone logged on to Lync Server.</span></span> <span data-ttu-id="ded37-129">Por exemplo, suponha que Ken Myer esteja conectado ao Lync Server cinco vezes diferentes em um único dia.</span><span class="sxs-lookup"><span data-stu-id="ded37-129">For example, suppose Ken Myer logged on to Lync Server five different times in a single day.</span></span> <span data-ttu-id="ded37-130">Nesse caso, Ken Myer contaria como cinco sessões de logon separadas para a métrica de Total de logons, mas como apenas um usuário de logon para a métrica de Usuários de logon exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ded37-130">In that case, Ken Myer would count as five separate logon sessions for the Total logons metric, but just one logon user for the Unique logon users metric.</span></span> <span data-ttu-id="ded37-131">Do mesmo modo, não é incomum que um usuário faça logon de vários dispositivos ou locais.</span><span class="sxs-lookup"><span data-stu-id="ded37-131">Likewise, it's not uncommon for a user to log on from multiple devices or multiple locations.</span></span> <span data-ttu-id="ded37-132">Por exemplo, um usuário pode fazer logon usando seu computador de mesa, computador laptop e ele pode ter um telefone IP que se conecta automaticamente ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ded37-132">For example, a user can log on using her desktop computer, her laptop computer, and she can have an IP phone that automatically logs on to Lync Server.</span></span> <span data-ttu-id="ded37-133">Neste exemplo, temos um usuário exclusivo com três logons.</span><span class="sxs-lookup"><span data-stu-id="ded37-133">In this example, there is one unique user with three logons.</span></span>

<span data-ttu-id="ded37-134">Para explicar de modo mais aprofundado a diferença entre total de logons e logons exclusivos, considere os logons em determinado período de tempo na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ded37-134">To further explain the difference between total logons and unique logons, consider the logons for a given time period in the following table.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ded37-135">Usuário</span><span class="sxs-lookup"><span data-stu-id="ded37-135">User</span></span></th>
<th><span data-ttu-id="ded37-136">Horário de logon</span><span class="sxs-lookup"><span data-stu-id="ded37-136">Logon time</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ded37-137">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ded37-137">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ded37-138">7/7/2012 8:45 AM</span><span class="sxs-lookup"><span data-stu-id="ded37-138">7/7/2012 8:45 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded37-139">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ded37-139">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ded37-140">7/7/2012 8:46 AM</span><span class="sxs-lookup"><span data-stu-id="ded37-140">7/7/2012 8:46 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded37-141">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ded37-141">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ded37-142">7/7/2012 9:17 AM</span><span class="sxs-lookup"><span data-stu-id="ded37-142">7/7/2012 9:17 AM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded37-143">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="ded37-143">Ken Myer</span></span></p></td>
<td><p><span data-ttu-id="ded37-144">7/7/2012 9:22 AM</span><span class="sxs-lookup"><span data-stu-id="ded37-144">7/7/2012 9:22 AM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded37-145">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="ded37-145">Pilar Ackerman</span></span></p></td>
<td><p><span data-ttu-id="ded37-146">7/7/2012 9:31 AM</span><span class="sxs-lookup"><span data-stu-id="ded37-146">7/7/2012 9:31 AM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ded37-p107">Observe que há um total de cinco logons; no entanto, há apenas dois usuários de logon exclusivo: Ken Myer (que fez logon três vezes) e Pilar Ackerman (que fez logon duas vezes). Essa é a diferença entre logons e usuários de logon exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ded37-p107">Notice that there is a total of five logons; however, there are only two unique logon users: Ken Myer (who logged on three times) and Pilar Ackerman (who logged on twice). That's the difference between logons and unique logon users.</span></span>

<span data-ttu-id="ded37-149">Além de saber o número de logons exclusivos, você precisa saber o número total de usuários que foram habilitados para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ded37-149">In addition to knowing the number of unique logons, you need to know the total number of users who have been enabled for Lync Server.</span></span> <span data-ttu-id="ded37-150">Esse valor pode ser recuperado abrindo o Shell de gerenciamento do Lync Server 2013 e executando o seguinte comando do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ded37-150">That value can be retrieved by opening the Lync Server 2013 Management Shell and running the following Windows PowerShell command:</span></span>

    (Get-CsUser).Count

<span data-ttu-id="ded37-151">Se o comando anterior retornar um valor de 1.236 e os usuários de logon exclusivos retornarem um valor médio de 667, isso indica que uma pequena parte da metade dos usuários habilitada para o Lync está realmente conectando-se ao sistema por dia (ou seja, 667 dividida por 1.236, que é aproximadamente 54%).</span><span class="sxs-lookup"><span data-stu-id="ded37-151">If the preceding command returns a value of 1,236 and Unique logon users metric returns an average value of 667, that suggests that a little over half of your users enable for Lync are actually logging on to the system each day (that is, 667 divided by 1,236, which is approximately 54%).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="ded37-152">Lembre-se de que as métricas de logon registram usuários que realmente fizeram logons durante o período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="ded37-152">Keep in mind that the logon metrics record users who actually logged on during the specified time period.</span></span> <span data-ttu-id="ded37-153">Elas não rastreiam os usuários que já estão logados no sistema.</span><span class="sxs-lookup"><span data-stu-id="ded37-153">They don't keep track of users who were already logged on to the system.</span></span> <span data-ttu-id="ded37-154">Por exemplo, se a sua métrica de Usuários de logon exclusivos mostrar 667 logons e você tiver 1.236 usuários, isso sugere que metade de seus usuários estão fazendo logon no sistema.</span><span class="sxs-lookup"><span data-stu-id="ded37-154">For example, if your Unique logon users metric shows 667 logons and you have 1,236 users, that suggests that about half your users are logging on to the system.</span></span> <span data-ttu-id="ded37-155">No entanto, suponhamos que 300 usuários já estavam logados no sistema no momento em que você começou a verificar os dados de logon.</span><span class="sxs-lookup"><span data-stu-id="ded37-155">However, suppose 300 users were already logged on to the system at the time you began checking the logon data.</span></span> <span data-ttu-id="ded37-156">Isso significa que você realmente tinha quase 1.000 usuários conectados ao Lync Server, o que significa que mais perto do 80% dos seus usuários estavam conectados.</span><span class="sxs-lookup"><span data-stu-id="ded37-156">That would mean that you actually had nearly 1,000 users logged on to Lync Server, which would mean that closer to 80% of your users were logged on.</span></span>



</div>

<span data-ttu-id="ded37-157">Você também deve comparar o valor de Usuários de logon exclusivos com o valor da métrica de Usuários ativos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ded37-157">You should also compare the Unique logon users value with the value of the Unique active users metric.</span></span> <span data-ttu-id="ded37-158">A métrica de usuários ativos exclusivos informa quantos usuários exclusivos realmente usaram o Lync Server: ele fez uma chamada telefônica, ele ingressou em uma reunião do Lync ou ele participou em uma sessão de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="ded37-158">The Unique active users metric tells you how many unique users actually used Lync Server: they made a phone call, they joined a Lync Meeting, or they participated in an IM session.</span></span> <span data-ttu-id="ded37-159">Isso é uma informação útil, porque o Microsoft Lync 2013 pode ser configurado para ser iniciado automaticamente sempre que um usuário iniciar o Windows.</span><span class="sxs-lookup"><span data-stu-id="ded37-159">This is useful information, because Microsoft Lync 2013 can be configured to automatically start each time a user starts Windows.</span></span> <span data-ttu-id="ded37-160">Por isso, você pode ter um grande número de usuários que fazem logon automaticamente no Lync quando eles fazem logon no Windows todos os dias, mas nunca usam realmente o Lync Server durante esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="ded37-160">Because of that, you might have a large number of users who automatically log on to Lync when they log on to Windows each day, but then never actually use Lync Server during that time period.</span></span>

<span data-ttu-id="ded37-161">A métrica de usuários ativos exclusivos também fornece dados mais significativos em uma organização, onde os usuários geralmente não fazem logoff do Windows no final do dia.</span><span class="sxs-lookup"><span data-stu-id="ded37-161">The Unique active users metric also provides more meaningful data in an organization where users typically do not log off Windows at the end of the day.</span></span> <span data-ttu-id="ded37-162">Em vez disso, eles simplesmente bloqueiam seus computadores e deixam o Windows e o Lync em execução.</span><span class="sxs-lookup"><span data-stu-id="ded37-162">Instead, they simply lock their computers and leave Windows and Lync running.</span></span> <span data-ttu-id="ded37-163">Em uma situação assim, você pode acabar com poucos logons por dia, pois seus usuários fizeram logon vários dias atrás e nunca fizeram o logoff.</span><span class="sxs-lookup"><span data-stu-id="ded37-163">In a situation like that, you might end up with very few logons per day because your users logged on several days ago and never logged off.</span></span> <span data-ttu-id="ded37-164">No entanto, usuários ativos exclusivos informa se os usuários estão ativamente usando o Lync ou outro cliente do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ded37-164">However, Unique active users tells you whether users are actively using Lync or another Lync Server client.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="ded37-165">Filtros</span><span class="sxs-lookup"><span data-stu-id="ded37-165">Filters</span></span>

<span data-ttu-id="ded37-166">Filtros fornecem uma forma de retornar um conjunto de dados mais focado ou exibir os dados retornados de diferentes formas.</span><span class="sxs-lookup"><span data-stu-id="ded37-166">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways.</span></span> <span data-ttu-id="ded37-167">Por exemplo, o relatório de registro de usuário permite que você exiba dados de todos os seus servidores de registro de registradores e de borda ou exiba dados de um pool individual.</span><span class="sxs-lookup"><span data-stu-id="ded37-167">For example, the User Registration Report enables you to view data for all your Registrar pool and Edge Servers or to view data for an individual pool.</span></span> <span data-ttu-id="ded37-168">Você também pode escolher como os dados devem ser agrupados.</span><span class="sxs-lookup"><span data-stu-id="ded37-168">You can also choose how data should be grouped.</span></span> <span data-ttu-id="ded37-169">Nesse caso, registros agrupados por hora, dia, semana ou mês.</span><span class="sxs-lookup"><span data-stu-id="ded37-169">In this case, registrations grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="ded37-170">A tabela a seguir lista os filtros que você pode usar com o Relatório de registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="ded37-170">The following table lists the filters that you can use with the User Registration Report.</span></span>

### <a name="user-registration-report-filters"></a><span data-ttu-id="ded37-171">Filtros do Relatório de registro do usuário</span><span class="sxs-lookup"><span data-stu-id="ded37-171">User Registration Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ded37-172">Nome</span><span class="sxs-lookup"><span data-stu-id="ded37-172">Name</span></span></th>
<th><span data-ttu-id="ded37-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="ded37-173">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ded37-174"><strong>De</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-174"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-p113">Data e hora de início do intervalo de tempo. Para ver os dados por hora, insira a data e hora de início desta forma:</span><span class="sxs-lookup"><span data-stu-id="ded37-p113">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="ded37-177">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ded37-177">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ded37-p114">Se você não inserir a hora de início, o relatório começará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="ded37-p114">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ded37-180">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ded37-180">7/7/2012</span></span></p>
<p><span data-ttu-id="ded37-181">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="ded37-181">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ded37-182">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ded37-182">7/3/2012</span></span></p>
<p><span data-ttu-id="ded37-183">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="ded37-183">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded37-184"><strong>Até</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-184"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-p115">Data e hora final para o intervalo de tempo. Para exibir os dados por hora, insira a data e hora final como a seguir:</span><span class="sxs-lookup"><span data-stu-id="ded37-p115">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="ded37-187">7/7/2012 1:00 PM</span><span class="sxs-lookup"><span data-stu-id="ded37-187">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="ded37-p116">Se você não inserir a hora final, o relatório terminará automaticamente à meia-noite do dia especificado. Para ver os dados por dia, insira somente a data:</span><span class="sxs-lookup"><span data-stu-id="ded37-p116">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="ded37-190">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="ded37-190">7/7/2012</span></span></p>
<p><span data-ttu-id="ded37-191">Para exibir por semana ou mês, insira uma data dentro da semana ou mês que deseja exibir (não é necessário inserir o primeiro dia da semana ou mês):</span><span class="sxs-lookup"><span data-stu-id="ded37-191">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="ded37-192">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="ded37-192">7/3/2012</span></span></p>
<p><span data-ttu-id="ded37-193">As semanas sempre vão de domingo a sábado.</span><span class="sxs-lookup"><span data-stu-id="ded37-193">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded37-194"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-194"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-p117">Intervalo de tempo. Selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="ded37-p117">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="ded37-197">Por hora (é possível exibir no máximo 25 horas)</span><span class="sxs-lookup"><span data-stu-id="ded37-197">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ded37-198">Diariamente (é possível exibir no máximo 31 dias)</span><span class="sxs-lookup"><span data-stu-id="ded37-198">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ded37-199">Semanalmente (é possível exibir no máximo 12 semanas)</span><span class="sxs-lookup"><span data-stu-id="ded37-199">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="ded37-200">Mensalmente (é possível exibir no máximo 12 meses)</span><span class="sxs-lookup"><span data-stu-id="ded37-200">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="ded37-201">Se as datas de início e término excederem o número máximo de valores permitidos para o intervalo selecionado, apenas o número máximo de valores (começando pela data de início) será exibido.</span><span class="sxs-lookup"><span data-stu-id="ded37-201">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="ded37-202">Por exemplo, se você selecionar o intervalo diário com uma data de início de 7/7/2012 e uma data de término de 2/28/2012, os dados serão exibidos para os dias 8/7/2012 12:00 AM a 9/7/2012 12:00 AM (ou seja, um total de 31 dias da importância dos dados).</span><span class="sxs-lookup"><span data-stu-id="ded37-202">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded37-203"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-203"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-204">FQDN (Nome de domínio totalmente qualificado) do pool de Registradores Avançados ou Servidores de Borda.</span><span class="sxs-lookup"><span data-stu-id="ded37-204">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server.</span></span> <span data-ttu-id="ded37-205">Você pode selecionar um pool individual ou escolher <strong>[Todos]</strong> para visualizar os dados de todos os pools.</span><span class="sxs-lookup"><span data-stu-id="ded37-205">You can either select an individual pool or choose <strong>[All]</strong> to view data for all the pools.</span></span> <span data-ttu-id="ded37-206">Essa lista suspensa é automaticamente preenchida com base nos registros no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ded37-206">This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="ded37-207">Métricas</span><span class="sxs-lookup"><span data-stu-id="ded37-207">Metrics</span></span>

<span data-ttu-id="ded37-208">A tabela a seguir lista as informações fornecidas no Relatório de Registro de Usuário.</span><span class="sxs-lookup"><span data-stu-id="ded37-208">The following table lists the information provided in the User Registration Report.</span></span>

### <a name="user-registration-report-metrics"></a><span data-ttu-id="ded37-209">Métrica do Relatório de Registro de Usuário</span><span class="sxs-lookup"><span data-stu-id="ded37-209">User Registration Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ded37-210">Nome</span><span class="sxs-lookup"><span data-stu-id="ded37-210">Name</span></span></th>
<th><span data-ttu-id="ded37-211">Você pode classificar este item?</span><span class="sxs-lookup"><span data-stu-id="ded37-211">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="ded37-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="ded37-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ded37-213"><strong>Por hora</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-213"><strong>Hourly</strong></span></span></p>
<p><span data-ttu-id="ded37-214"><strong>Diário</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-214"><strong>Daily</strong></span></span></p>
<p><span data-ttu-id="ded37-215"><strong>Semanal</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-215"><strong>Weekly</strong></span></span></p>
<p><span data-ttu-id="ded37-216"><strong>Mensal</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-216"><strong>Monthly</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-217">Não</span><span class="sxs-lookup"><span data-stu-id="ded37-217">No</span></span></p></td>
<td><p><span data-ttu-id="ded37-218">Indica o intervalo de tempo selecionado na barra de ferramentas de filtro.</span><span class="sxs-lookup"><span data-stu-id="ded37-218">Indicates the time interval that you selected on the filter toolbar.</span></span> <span data-ttu-id="ded37-219">Quando aplicável, é possível clicar em determinado intervalo de tempo para exibir informações detalhadas sobre ele.</span><span class="sxs-lookup"><span data-stu-id="ded37-219">Where applicable, you can click a given time interval to view detailed information for that interval.</span></span> <span data-ttu-id="ded37-220">Por exemplo, se você estiver usando o intervalo diário e clicar em 7/7/2012, verá um detalhamento por hora da atividade de registro do usuário para essa data.</span><span class="sxs-lookup"><span data-stu-id="ded37-220">For example, if you are using the Daily interval and you click 7/7/2012, you see an hourly breakdown of user registration activity for that date.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded37-221"><strong>Total de logons</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-221"><strong>Total logons</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-222">Não</span><span class="sxs-lookup"><span data-stu-id="ded37-222">No</span></span></p></td>
<td><p><span data-ttu-id="ded37-223">Número total de sessões de logon bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="ded37-223">Total number of successful logon sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded37-224"><strong>Logons internos</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-224"><strong>Internal logons</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-225">Não</span><span class="sxs-lookup"><span data-stu-id="ded37-225">No</span></span></p></td>
<td><p><span data-ttu-id="ded37-226">Número total de logons dentro da rede interna.</span><span class="sxs-lookup"><span data-stu-id="ded37-226">Total number of logons within the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded37-227"><strong>Logons externos</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-227"><strong>External logons</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-228">Não</span><span class="sxs-lookup"><span data-stu-id="ded37-228">No</span></span></p></td>
<td><p><span data-ttu-id="ded37-229">Número total logons de fora da rede interna, usando o Servidor de Borda.</span><span class="sxs-lookup"><span data-stu-id="ded37-229">Total number of logons from outside the internal network, using the Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ded37-230"><strong>Usuários de logon exclusivo</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-230"><strong>Unique logon users</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-231">Não</span><span class="sxs-lookup"><span data-stu-id="ded37-231">No</span></span></p></td>
<td><p><span data-ttu-id="ded37-p121">Número total de usuário com ao menos uma sessão de logon. Um usuário com várias sessões de logon conta como um usuário, da mesma forma que uma pessoa que teve uma única sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="ded37-p121">Total number of users who had at least one logon session. A user who had multiple logon sessions counts as one user, the same as a person who had just a single logon session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ded37-234"><strong>Usuários ativos exclusivos</strong></span><span class="sxs-lookup"><span data-stu-id="ded37-234"><strong>Unique active users</strong></span></span></p></td>
<td><p><span data-ttu-id="ded37-235">Não</span><span class="sxs-lookup"><span data-stu-id="ded37-235">No</span></span></p></td>
<td><p><span data-ttu-id="ded37-p122">Número total de usuários envolvidos em uma sessão ponto a ponto ou de conferência. Um usuário com várias sessões de logon conta como um usuário, da mesma forma que uma pessoa que teve uma única sessão.</span><span class="sxs-lookup"><span data-stu-id="ded37-p122">Total number of users who were involved in a peer-to-peer or conferencing session. A user who had multiple sessions counts as one user, the same as a person who had just a single session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ded37-238">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ded37-238">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

