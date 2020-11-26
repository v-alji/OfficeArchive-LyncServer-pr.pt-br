---
title: Perguntas frequentes sobre a ferramenta de stress e desempenho do Lync Server 2013
description: Perguntas frequentes sobre a ferramenta stress e performance do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Stress and Performance Tool FAQ
ms:assetid: a5aff705-320c-4916-8094-23046b2a1b18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945600(v=OCS.15)
ms:contentKeyID: 51541426
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 716325390bc33df209be3bdc67ed8b6cd7d1ec30
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446434"
---
# <a name="lync-server-2013-stress-and-performance-tool-faq"></a><span data-ttu-id="f8593-103">Perguntas frequentes sobre a ferramenta de stress e desempenho do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f8593-103">Lync Server 2013 Stress and Performance Tool FAQ</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f8593-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f8593-104">

<span> </span></span></span>

<span data-ttu-id="f8593-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="f8593-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<div>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f8593-106">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="f8593-106">Frequently Asked Questions</span></span>

<span data-ttu-id="f8593-107">Aqui estão algumas perguntas frequentes sobre a ferramenta de stress e desempenho do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8593-107">Here are some frequently asked questions about the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="can-i-run-lyncperftoolexe-in-production"></a><span data-ttu-id="f8593-108">É possível executar o LyncPerfTool.exe em produção?</span><span class="sxs-lookup"><span data-stu-id="f8593-108">Can I run LyncPerfTool.exe in production?</span></span>

<span data-ttu-id="f8593-109">Não recomendamos isso.</span><span class="sxs-lookup"><span data-stu-id="f8593-109">We do not recommend this.</span></span> <span data-ttu-id="f8593-110">Essa ferramenta afetará o desempenho do servidor, a segurança e a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="f8593-110">This tool will impact server performance, security, and user experience.</span></span>

</div>

<div>

## <a name="i-am-logging-on-my-users-for-the-first-time-why-are-the-servers-running-at-such-high-load"></a><span data-ttu-id="f8593-111">Estou me conectando aos meus usuários pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="f8593-111">I am logging on my users for the first time.</span></span> <span data-ttu-id="f8593-112">Por que os servidores estão em execução em alta carga?</span><span class="sxs-lookup"><span data-stu-id="f8593-112">Why are the servers running at such high load?</span></span>

<span data-ttu-id="f8593-113">Na primeira vez que os usuários fazem logon, há operações adicionais que ocorrem.</span><span class="sxs-lookup"><span data-stu-id="f8593-113">The first time the users log on, there are additional operations that occur.</span></span> <span data-ttu-id="f8593-114">Como resultado, o desempenho no servidor back-end do Microsoft SQL Server será degradado.</span><span class="sxs-lookup"><span data-stu-id="f8593-114">As a result, the performance on the Microsoft SQL Server Back End Server will be degraded.</span></span> <span data-ttu-id="f8593-115">Recomendamos que você execute um teste curto que Registre todos os usuários e reinicie os clientes antes de medir os resultados.</span><span class="sxs-lookup"><span data-stu-id="f8593-115">We recommend that you run a short test that logs on all of the users, and then restart the clients before you measure results.</span></span> <span data-ttu-id="f8593-116">Não há suporte para mais de 12 sessões de logon de usuários simultâneas por segundo, mas isso depende da configuração do hardware.</span><span class="sxs-lookup"><span data-stu-id="f8593-116">We do not support more than 12 concurrent user logon sessions per second, but this depends on your hardware configuration.</span></span>

</div>

<div>

## <a name="my-clients-are-running-out-of-memory-what-should-i-do"></a><span data-ttu-id="f8593-117">Meus clientes estão ficando sem memória.</span><span class="sxs-lookup"><span data-stu-id="f8593-117">My clients are running out of memory.</span></span> <span data-ttu-id="f8593-118">O que devo fazer?</span><span class="sxs-lookup"><span data-stu-id="f8593-118">What should I do?</span></span>

<span data-ttu-id="f8593-119">Se os seus clientes estiverem ficando sem memória, você precisará reduzir o número de usuários por computador.</span><span class="sxs-lookup"><span data-stu-id="f8593-119">If your clients are running out of memory, you need to reduce the number of users per computer.</span></span>

</div>

<div>

## <a name="my-clients-are-at-100-percent-cpu-all-the-time-what-should-i-do"></a><span data-ttu-id="f8593-120">Meus clientes estão em 100% de CPU o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="f8593-120">My clients are at 100 percent CPU all the time.</span></span> <span data-ttu-id="f8593-121">O que devo fazer?</span><span class="sxs-lookup"><span data-stu-id="f8593-121">What should I do?</span></span>

<span data-ttu-id="f8593-122">Se seus clientes estiverem sendo executados com uma CPU muito alta depois que todos os usuários estiverem conectados, você precisará reduzir o número de usuários por computador.</span><span class="sxs-lookup"><span data-stu-id="f8593-122">If your clients are running with very high CPU after all the users have logged on, you need to reduce the number of users per computer.</span></span> <span data-ttu-id="f8593-123">Altos picos de CPU são aceitáveis, mas se estiverem estáveis, você precisará reduzir a carga.</span><span class="sxs-lookup"><span data-stu-id="f8593-123">High CPU spikes are acceptable, but if it is sustained, you need to reduce the load.</span></span>

</div>

<div>

## <a name="can-i-run-the-tool-on-the-server-itself"></a><span data-ttu-id="f8593-124">É possível executar a ferramenta no próprio servidor?</span><span class="sxs-lookup"><span data-stu-id="f8593-124">Can I run the tool on the server itself?</span></span>

<span data-ttu-id="f8593-125">Não.</span><span class="sxs-lookup"><span data-stu-id="f8593-125">No.</span></span> <span data-ttu-id="f8593-126">Não há suporte para esse cenário e pode falhar devido a uma incompatibilidade binária.</span><span class="sxs-lookup"><span data-stu-id="f8593-126">This scenario is not supported and may fail due to a binary mismatch.</span></span> <span data-ttu-id="f8593-127">Além disso, como o ponto é medir o consumo de recursos no servidor, executar a ferramenta não renderizaria as medidas sem significado.</span><span class="sxs-lookup"><span data-stu-id="f8593-127">Also, because the point is to measure resource consumption on the server, running the tool there would render the measurements meaningless.</span></span>

</div>

<div>

## <a name="can-i-run-lyncperftoolexe-on-a-virtual-server-or-on-microsoft-hyper-v-server-20082012"></a><span data-ttu-id="f8593-128">É possível executar o LyncPerfTool.exe em um servidor virtual ou no Microsoft Hyper-V Server 2008/2012?</span><span class="sxs-lookup"><span data-stu-id="f8593-128">Can I run LyncPerfTool.exe on a Virtual Server or on Microsoft Hyper-V Server 2008/2012?</span></span>

<span data-ttu-id="f8593-129">Sim.</span><span class="sxs-lookup"><span data-stu-id="f8593-129">Yes.</span></span>

</div>

<div>

## <a name="what-does-mpop-mean"></a><span data-ttu-id="f8593-130">O que significa MPOP?</span><span class="sxs-lookup"><span data-stu-id="f8593-130">What does MPOP mean?</span></span>

<span data-ttu-id="f8593-131">MPOP significa vários pontos de presença.</span><span class="sxs-lookup"><span data-stu-id="f8593-131">MPOP stands for multiple points of presence.</span></span> <span data-ttu-id="f8593-132">Destina-se a simular o cenário em que os usuários estão conectados ao Lync 2013 de várias máquinas.</span><span class="sxs-lookup"><span data-stu-id="f8593-132">It is meant to simulate the scenario where users are logged on to Lync 2013 from multiple machines.</span></span> <span data-ttu-id="f8593-133">Observe que, em LyncPerfTool.exe, cada ponto de extremidade usa o perfil padrão (ou seja, o perfil não é dividido entre os dois pontos de presença).</span><span class="sxs-lookup"><span data-stu-id="f8593-133">Note that in LyncPerfTool.exe, each endpoint uses the default profile (that is, the profile is not split between the two points of presence).</span></span>

</div>

<div>

## <a name="i-started-lyncperftoolexe-but-nothing-is-happening-whats-going-on"></a><span data-ttu-id="f8593-134">Comecei LyncPerfTool.exe, mas nada está acontecendo.</span><span class="sxs-lookup"><span data-stu-id="f8593-134">I started LyncPerfTool.exe but nothing is happening.</span></span> <span data-ttu-id="f8593-135">O que está acontecendo?</span><span class="sxs-lookup"><span data-stu-id="f8593-135">What’s going on?</span></span>

<span data-ttu-id="f8593-136">Verifique o contador total de pontos de extremidade ativos nos clientes para ver se os usuários estão se conectando.</span><span class="sxs-lookup"><span data-stu-id="f8593-136">Check the Total Active Endpoints counter on the clients to see if the users are connecting.</span></span> <span data-ttu-id="f8593-137">Se os usuários não estiverem se conectando, verifique a configuração do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8593-137">If users are not connecting, verify your Lync Server 2013 configuration.</span></span> <span data-ttu-id="f8593-138">Geralmente, esse problema ocorre porque o nome do servidor, o prefixo do usuário ou a senha estão incorretos.</span><span class="sxs-lookup"><span data-stu-id="f8593-138">This issue usually occurs because the server name, the user prefix, or the password is incorrect.</span></span> <span data-ttu-id="f8593-139">Observe que os clientes externos devem especificar o proxy de acesso como o valor TargetServer.</span><span class="sxs-lookup"><span data-stu-id="f8593-139">Note that external clients should specify the Access Proxy as the TargetServer value.</span></span> <span data-ttu-id="f8593-140">Verifique a porta no arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="f8593-140">Verify the port in the configuration file.</span></span>

</div>

<div>

## <a name="how-do-i-know-something-is-happening"></a><span data-ttu-id="f8593-141">Como posso saber se algo está acontecendo?</span><span class="sxs-lookup"><span data-stu-id="f8593-141">How do I know something is happening?</span></span>

<span data-ttu-id="f8593-142">Os vários contadores de desempenho do LyncPerfTool indicam se os usuários estão se conectando e executando ações.</span><span class="sxs-lookup"><span data-stu-id="f8593-142">The various LyncPerfTool performance counters indicate whether or not users are connecting and performing actions.</span></span> <span data-ttu-id="f8593-143">No entanto, uma maneira fácil de verificar é fazer logon em uma das contas usando o Lync 2013 e executando a ação desejada.</span><span class="sxs-lookup"><span data-stu-id="f8593-143">However, an easy way to check is to log on to one of the accounts by using Lync 2013 and performing the action you want.</span></span>

</div>

<div>

## <a name="i-have-live-communications-server-2007-r2-capacity-planning-tools-andor-lync-server-2010-installed-is-that-ok"></a><span data-ttu-id="f8593-144">Tenho ferramentas de planejamento de capacidade do Live Communications Server 2007 R2 e/ou Lync Server 2010 instaladas.</span><span class="sxs-lookup"><span data-stu-id="f8593-144">I have Live Communications Server 2007 R2 Capacity Planning Tools and/or Lync Server 2010 installed.</span></span> <span data-ttu-id="f8593-145">Isso é tudo OK?</span><span class="sxs-lookup"><span data-stu-id="f8593-145">Is that OK?</span></span>

<span data-ttu-id="f8593-146">Não.</span><span class="sxs-lookup"><span data-stu-id="f8593-146">No.</span></span> <span data-ttu-id="f8593-147">Há problemas de interoperabilidade, e você deve desinstalar todas as versões anteriores deste produto.</span><span class="sxs-lookup"><span data-stu-id="f8593-147">There are interoperability issues, and you must uninstall all previous versions of this product.</span></span>

</div>

<div>

## <a name="will-the-stress-and-performance-tools-set-up-the-caa-call-information-server-topology"></a><span data-ttu-id="f8593-148">As ferramentas de stress e desempenho configuram a CAA Call Information Server Topology?</span><span class="sxs-lookup"><span data-stu-id="f8593-148">Will the Stress and Performance tools set up the CAA Call Information server topology?</span></span>

<span data-ttu-id="f8593-149">Não.</span><span class="sxs-lookup"><span data-stu-id="f8593-149">No.</span></span> <span data-ttu-id="f8593-150">As ferramentas apenas criam usuários, contatos e listas de distribuição e simulam a carga do usuário.</span><span class="sxs-lookup"><span data-stu-id="f8593-150">The tools only create users, contacts, and distribution lists, and simulate user load.</span></span>

</div>

<div>

## <a name="what-is-the-maximum-number-of-users-that-the-tools-support"></a><span data-ttu-id="f8593-151">Qual é o número máximo de usuários com suporte para as ferramentas?</span><span class="sxs-lookup"><span data-stu-id="f8593-151">What is the maximum number of users that the tools support?</span></span>

<span data-ttu-id="f8593-152">Criamos até um total de 80.000 usuários e executamos testes totalizando 30.000 usuários, usando essas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="f8593-152">We have created up to a total of 80,000 users and executed tests totaling 30,000 users, using these tools.</span></span> <span data-ttu-id="f8593-153">Sugerimos um máximo de 120.000 usuários, embora as limitações técnicas permitam um valor mais alto, dependendo do hardware do cliente e do servidor disponível.</span><span class="sxs-lookup"><span data-stu-id="f8593-153">We suggest a maximum of 120,000 users, although the technical limitations allow for a higher value, depending on the client and server hardware available.</span></span>

<span data-ttu-id="f8593-154"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f8593-154"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

