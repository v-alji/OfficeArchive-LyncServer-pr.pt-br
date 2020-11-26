---
title: Calculadora de planejamento de capacidade do Lync Server 2013
description: Calculadora de planejamento de capacidade do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Lync Server 2013 capacity planning calculator
ms:assetid: e86c1f05-1393-408a-9549-6001572ec50d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362852(v=OCS.15)
ms:contentKeyID: 56280894
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9f78019c98cf280f38249ac52cd063cede5319af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435576"
---
# <a name="using-the-capacity-planning-calculator-for-lync-server-2013"></a><span data-ttu-id="63a41-103">Usar a calculadora de planejamento de capacidade para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="63a41-103">Using the capacity planning calculator for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63a41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63a41-104">

<span> </span></span></span>

<span data-ttu-id="63a41-105">_**Tópico da última modificação:** 2013-11-21_</span><span class="sxs-lookup"><span data-stu-id="63a41-105">_**Topic Last Modified:** 2013-11-21_</span></span>

<span data-ttu-id="63a41-106">A calculadora de planejamento de capacidade do Microsoft® Lync™ Server 2013 está disponível para download em <https://www.microsoft.com/download/details.aspx?id=36828> .</span><span class="sxs-lookup"><span data-stu-id="63a41-106">The Microsoft® Lync™ Server 2013 capacity planning calculator is available for download at <https://www.microsoft.com/download/details.aspx?id=36828>.</span></span> <span data-ttu-id="63a41-107">Ele foi projetado para ajudar você a determinar os requisitos do servidor com base em números de usuários e modalidades de comunicação habilitados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="63a41-107">It is designed to assist you in determining server requirements based on numbers of users and communication modalities that are enabled at your organization.</span></span> <span data-ttu-id="63a41-108">Você insere o perfil da sua organização e a calculadora fornece recomendações que ajudam você a planejar sua topologia.</span><span class="sxs-lookup"><span data-stu-id="63a41-108">You enter your organization’s profile, and the calculator provides recommendations that help you plan your topology.</span></span>

<span data-ttu-id="63a41-109">As recomendações criadas pela calculadora são somente para fins de planejamento.</span><span class="sxs-lookup"><span data-stu-id="63a41-109">The recommendations created by the calculator are for planning purposes only.</span></span> <span data-ttu-id="63a41-110">A simulação de carga real é necessária para garantir que o Lync Server 2013 seja provisionado de forma adequada.</span><span class="sxs-lookup"><span data-stu-id="63a41-110">Actual load simulation is required to ensure that Lync Server 2013 is adequately provisioned.</span></span> <span data-ttu-id="63a41-111">Para executar testes de stress em uma carga simulada, use a [ferramenta de stress e desempenho do Lync Server 2013](https://go.microsoft.com/fwlink/?linkid=282724).</span><span class="sxs-lookup"><span data-stu-id="63a41-111">To perform stress testing under a simulated load, use the [Lync Server 2013 Stress and Performance Tool](https://go.microsoft.com/fwlink/?linkid=282724).</span></span>

<span data-ttu-id="63a41-112">Depois de determinar seu perfil de usuário e as modalidades que você deseja habilitar para seus usuários, é hora de usar a calculadora para planejar o número de servidores, memória e largura de banda de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="63a41-112">After you have determined your user profile and the modalities that you want to enable for your users, it is time to use the calculator to plan the number of servers, memory, and bandwidth that you need.</span></span> <span data-ttu-id="63a41-113">Esta versão da calculadora não fornece orientação quanto às exigências de E/S do disco.</span><span class="sxs-lookup"><span data-stu-id="63a41-113">This version of the calculator does not provide guidance for disk I/O requirements.</span></span>

<span data-ttu-id="63a41-114">Esta calculadora complementa o [Microsoft Lync Server](https://go.microsoft.com/fwlink/?linkid=282725) e o [Microsoft Lync Server](lync-server-2013-planning.md).</span><span class="sxs-lookup"><span data-stu-id="63a41-114">This calculator complements the [Microsoft Lync Server](https://go.microsoft.com/fwlink/?linkid=282725) and [Microsoft Lync Server](lync-server-2013-planning.md).</span></span> <span data-ttu-id="63a41-115">Use a calculadora após ter revisado o guia e criado uma topologia recomendada usando a Ferramenta de Planejamento.</span><span class="sxs-lookup"><span data-stu-id="63a41-115">Use the calculator after you have reviewed the guide and created a recommended topology by using the Planning Tool.</span></span>

<span data-ttu-id="63a41-p105">Você poderá aproveitar grande parte da calculadora se tiver informações precisas e detalhadas sobre seu perfil do usuário específico. Por exemplo, a porcentagem dos usuários de voz, chamadas médias por usuário e por hora, duração da chamada e porcentagem dos usuários simultâneos em conferências podem fazer uma diferença enorme nas exigências do servidor. A precisão das recomendações criadas pela calculadora depende da precisão das informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="63a41-p105">You can benefit most from the calculator if you have accurate, detailed information about your specific user profile. For example, the percentage of voice-enabled users, average calls per user per hour, call duration, and the percentage of concurrent users in conferences can make a huge difference in server requirements. The accuracy of the recommendations created by the calculator depends on the accuracy of the information that you provide.</span></span>

<div>

## <a name="using-the-capacity-calculator"></a><span data-ttu-id="63a41-119">Usando a capacidade da calculadora</span><span class="sxs-lookup"><span data-stu-id="63a41-119">Using the Capacity Calculator</span></span>

<span data-ttu-id="63a41-120">A calculadora é uma planilha® do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="63a41-120">The calculator is a Microsoft Excel® spreadsheet.</span></span> <span data-ttu-id="63a41-121">As células coloridas em laranja são para entrada a partir de você.</span><span class="sxs-lookup"><span data-stu-id="63a41-121">Orange-colored cells are for input from you.</span></span> <span data-ttu-id="63a41-122">Os valores padrão são inseridos (os usuários do 80.000 em um pool com doze servidores front-end), mas você pode alterar esses valores de acordo com as necessidades da sua organização.</span><span class="sxs-lookup"><span data-stu-id="63a41-122">Default values are entered (80,000 users in one pool with twelve Front End Servers), but you can change these values according to your organization’s needs.</span></span>

<span data-ttu-id="63a41-123">O modelo de uso contém as seguintes seções.</span><span class="sxs-lookup"><span data-stu-id="63a41-123">The usage model contains the following sections.</span></span> <span data-ttu-id="63a41-124">Para calcular seus requisitos de capacidade, insira os dados conforme descrito:</span><span class="sxs-lookup"><span data-stu-id="63a41-124">To calculate your capacity requirements, enter data as described:</span></span>

<span data-ttu-id="63a41-125">**Mensagem instantânea e presença**</span><span class="sxs-lookup"><span data-stu-id="63a41-125">**Instant Messaging and Presence**</span></span>

  - <span data-ttu-id="63a41-126">Em número de usuários, digite o número de usuários que entrarão simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="63a41-126">Under Number of Users, type the number of users who will be concurrently signed in.</span></span> <span data-ttu-id="63a41-127">Esse número normalmente é 80% do número total de usuários provisionados.</span><span class="sxs-lookup"><span data-stu-id="63a41-127">This number is typically 80% of the total number of provisioned users.</span></span> <span data-ttu-id="63a41-128">Na maioria das situações, 100% de seus usuários simultâneos estarão ativados para mensagens instantâneas e presença.</span><span class="sxs-lookup"><span data-stu-id="63a41-128">In most situations, 100% of your concurrent users will be enabled for IM and Presence.</span></span> <span data-ttu-id="63a41-129">O padrão é 80.000.</span><span class="sxs-lookup"><span data-stu-id="63a41-129">The default is 80,000.</span></span>

  - <span data-ttu-id="63a41-130">Número médio de contatos na lista Contatos indica o número de contatos que nós estamos usando para validar as exigências de seu sistema.</span><span class="sxs-lookup"><span data-stu-id="63a41-130">Average number of contacts in Contact list indicates the number of contacts that we are using to validate your system requirements.</span></span> <span data-ttu-id="63a41-131">Esse número não é alterado.</span><span class="sxs-lookup"><span data-stu-id="63a41-131">This number is not changeable.</span></span>

<span data-ttu-id="63a41-132">**Enterprise Voice**</span><span class="sxs-lookup"><span data-stu-id="63a41-132">**Enterprise Voice**</span></span>

  - <span data-ttu-id="63a41-133">Em usuários habilitados para o Enterprise Voice, digite a porcentagem dos seus usuários que estão habilitados para o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="63a41-133">In Users enabled for Enterprise Voice, type the percentage of your users who are enabled for Enterprise Voice.</span></span> <span data-ttu-id="63a41-134">O padrão é 60%</span><span class="sxs-lookup"><span data-stu-id="63a41-134">The default is 60%.</span></span>

  - <span data-ttu-id="63a41-135">Em número médio de chamadas por hora por hora (pico), digite o número de chamadas por hora em que você espera que o usuário médio participe durante horários de carga de pico.</span><span class="sxs-lookup"><span data-stu-id="63a41-135">In Average number of calls per user per hour (peak), type the number of calls per hour that you expect the average user to participate in during times of peak load.</span></span> <span data-ttu-id="63a41-136">O padrão é 4.</span><span class="sxs-lookup"><span data-stu-id="63a41-136">The default is 4.</span></span>

  - <span data-ttu-id="63a41-137">Em Porcentagem de chamadas que usam o bypass de mídia, digite a porcentagem de chamadas feitas por seus usuários que ignorará o Servidor de Mediação.</span><span class="sxs-lookup"><span data-stu-id="63a41-137">In Percentage of calls that use media bypass, type the percentage of calls placed by your users that will bypass the Mediation Server.</span></span> <span data-ttu-id="63a41-138">O padrão é 65%.</span><span class="sxs-lookup"><span data-stu-id="63a41-138">The default is 65%.</span></span>

  - <span data-ttu-id="63a41-139">Em Porcentagem de usuários por voz envolvidos nas chamadas UC-PSTN, digite a porcentagem de chamadas de sua organização que são chamadas telefônicas UC-PSTN.</span><span class="sxs-lookup"><span data-stu-id="63a41-139">In Percentage of voice users involved in UC-PSTN calls, type the percentage of your organization’s calls which are UC-PSTN phone calls.</span></span> <span data-ttu-id="63a41-140">O padrão é 60%</span><span class="sxs-lookup"><span data-stu-id="63a41-140">The default is 60%</span></span>

  - <span data-ttu-id="63a41-141">Em porcentagem de usuários de voz envolvidos nas chamadas de comunicação unificada, mostra a porcentagem de usuários que estão habilitados para o Enterprise Voice que serão habilitados somente para as chamadas UC-UC.</span><span class="sxs-lookup"><span data-stu-id="63a41-141">In Percentage of voice users involved in UC-UC calls shows the percentage of users who are enabled for Enterprise Voice who will be enabled only for UC-UC calls.</span></span> <span data-ttu-id="63a41-142">Esse número é calculado com base no que você digita para a Porcentagem de usuários de voz ativados para as chamadas UC-PSTN.</span><span class="sxs-lookup"><span data-stu-id="63a41-142">This number is calculated based on what you input for Percentage of voice users enabled for UC-PSTN calls.</span></span>

<span data-ttu-id="63a41-143">**Conferências**</span><span class="sxs-lookup"><span data-stu-id="63a41-143">**Conferencing**</span></span>

  - <span data-ttu-id="63a41-144">Em porcentagem de usuários em conferências simultâneas, digite a porcentagem de usuários que participarão de conferências de forma simultânea.</span><span class="sxs-lookup"><span data-stu-id="63a41-144">In Percentage of users in concurrent conferences, type the percentage of users who will be concurrently participating in conferences.</span></span> <span data-ttu-id="63a41-145">O padrão é 5%.</span><span class="sxs-lookup"><span data-stu-id="63a41-145">The default is 5%.</span></span>

  - <span data-ttu-id="63a41-146">Em porcentagem de conferências com apenas mensagens de chat em grupo (sem voz), digite a porcentagem de conferências das quais as conferências envolverão apenas mensagens instantâneas; ou seja, que não incluem um componente de áudio.</span><span class="sxs-lookup"><span data-stu-id="63a41-146">In Percentage of conferences with group IM only (no voice), type the percentage of conferences whose conferences will involve instant messaging only; that is, that do not include an audio component.</span></span> <span data-ttu-id="63a41-147">O padrão é 10%</span><span class="sxs-lookup"><span data-stu-id="63a41-147">The default is 10%</span></span>

  - <span data-ttu-id="63a41-148">Em porcentagem de usuários usando conferência discada, digite a porcentagem de participantes simultâneos em conferências que usarão a conferência discada.</span><span class="sxs-lookup"><span data-stu-id="63a41-148">In Percentage of users using dial-in conferencing, type the percentage of concurrent participants in conferences who will be using dial-in conferencing.</span></span> <span data-ttu-id="63a41-149">O padrão é 15%.</span><span class="sxs-lookup"><span data-stu-id="63a41-149">The default is 15%.</span></span>

  - <span data-ttu-id="63a41-150">Em porcentagem de conferências usando voz, digite a porcentagem de conferências que incluirão um componente de áudio.</span><span class="sxs-lookup"><span data-stu-id="63a41-150">In Percentage of conferences using voice, type the percentage of conferences that will include an audio component.</span></span>
    
      - <span data-ttu-id="63a41-151">Se 20% das conferências de voz incluírem também um vídeo normal, marque a caixa de seleção Incluir vídeo (sem Multi-View).</span><span class="sxs-lookup"><span data-stu-id="63a41-151">If 20% of your voice conferences will also include regular video, select the Including video (no Multi View) check box.</span></span>
    
      - <span data-ttu-id="63a41-152">Se 20% de suas conferências incluírem o vídeo Multi-View, marque a caixa de seleção Incluir Multi-View.</span><span class="sxs-lookup"><span data-stu-id="63a41-152">If 20% of your conferences will also include Multi-View video, select the Including Multi View check box.</span></span>
    
      - <span data-ttu-id="63a41-153">Se 50% de suas conferências de voz incluírem o compartilhamento de aplicativos, marque a caixa de seleção Incluir compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="63a41-153">If 50% of your voice conferences will also include application sharing, select the Including application sharing check box.</span></span>
    
      - <span data-ttu-id="63a41-154">Se 20% das suas conferências de voz incluírem carregamentos de dados, como apresentações do Microsoft PowerPoint®, marque a caixa de seleção incluir Webconferência.</span><span class="sxs-lookup"><span data-stu-id="63a41-154">If 20% of your voice conferences include data uploads, such as Microsoft PowerPoint® presentations, select the Including web conferencing check box.</span></span>

<span data-ttu-id="63a41-155">**Mobilidade**</span><span class="sxs-lookup"><span data-stu-id="63a41-155">**Mobility**</span></span>

  - <span data-ttu-id="63a41-156">Em porcentagem de usuários habilitados para mobilidade, digite a porcentagem dos usuários que serão habilitadas para se conectar ao Lync Server usando dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="63a41-156">In Percentage of users enabled for Mobility, type the percentage of your users who will be enabled to connect to Lync Server using mobile devices.</span></span> <span data-ttu-id="63a41-157">O padrão é 40%.</span><span class="sxs-lookup"><span data-stu-id="63a41-157">The default is 40%.</span></span>

<span data-ttu-id="63a41-158">Quando você tiver digitado todas as informações necessárias, a calculadora de capacidade estimará as exigências.</span><span class="sxs-lookup"><span data-stu-id="63a41-158">When you have entered all the necessary information, the capacity calculator estimates your requirements.</span></span> <span data-ttu-id="63a41-159">As células amarelas mostram os valores calculados para requisitos de CPU, memória e largura de banda com base nos testes executados nos laboratórios de desempenho do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="63a41-159">The yellow cells show calculated values for CPU, memory, and bandwidth requirements based on tests performed in Lync Server 2013 performance labs.</span></span> <span data-ttu-id="63a41-160">Os números são fornecidos como uma diretriz e nem toda variação é testada e validada.</span><span class="sxs-lookup"><span data-stu-id="63a41-160">The numbers are provided as a guideline, not every single variation is tested and validated.</span></span> <span data-ttu-id="63a41-161">Os seguintes valores são calculados:</span><span class="sxs-lookup"><span data-stu-id="63a41-161">The following values are calculated:</span></span>

  - <span data-ttu-id="63a41-162">CPU de front-end: porcentagem de uso da CPU se a carga inteira estivesse sendo manipulada por um servidor front-end das mesmas especificações do servidor usado no teste da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63a41-162">Front End CPU: Percentage of CPU usage if the entire load were being handled by one Front End Server of the same specifications as the server that was used in Microsoft testing.</span></span>

  - <span data-ttu-id="63a41-163">Rede em Mbps: as exigências da largura de banda em megabits por segundo (Mbps) para a carga de trabalho correspondente.</span><span class="sxs-lookup"><span data-stu-id="63a41-163">Network in Mbps: Bandwidth requirements in megabits per second (Mbps) for the corresponding workload.</span></span>

  - <span data-ttu-id="63a41-164">Memória em GB: a memória requerida em gigabytes (GB) para a carga de trabalho correspondente.</span><span class="sxs-lookup"><span data-stu-id="63a41-164">Memory in GB: Memory required in gigabytes (GB) for the corresponding workload.</span></span>

<span data-ttu-id="63a41-165">As células verdes mostram as recomendações para o modelo de uso inserido.</span><span class="sxs-lookup"><span data-stu-id="63a41-165">The green cells show recommendations for the usage model that you entered.</span></span>

  - <span data-ttu-id="63a41-166">Total de servidores front end: o número de servidores físicos necessários é baseado em servidores dedicados que executam o Lync Server 2013 com processador duplo,-Core, com 2.260 megacycles.</span><span class="sxs-lookup"><span data-stu-id="63a41-166">Total Front End Servers: The number of physical servers required are based on dedicated servers running Lync Server 2013 with dual processor, hex-core, with 2,260 megacycles.</span></span>

  - <span data-ttu-id="63a41-167">Note que é recomendado ativar o hyperthreading e foi comprovado que melhora o desempenho para os servidores que suportam áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="63a41-167">Note that enabling hyperthreading is recommended and has been proven to improve performance for servers that support audio/video.</span></span>

  - <span data-ttu-id="63a41-168">Servidores de borda: o número de Servidores de borda requeridos, com base em 30% de todos os usuários simultâneos comunicando-se por meio dos Servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="63a41-168">Edge Servers: The number of Edge Servers required, based on 30% of all concurrent users communicating through the Edge Servers.</span></span> <span data-ttu-id="63a41-169">Essa porcentagem não pode ser alterada na calculadora.</span><span class="sxs-lookup"><span data-stu-id="63a41-169">This percentage cannot be changed in the calculator.</span></span>

  - <span data-ttu-id="63a41-170">Armazenamento de serviços de Arquivamento/Registro de detalhes da camada/Qualidade da experiência: o número de armazenamentos requeridos para os recursos de Arquivamento ou Monitoramento, se estiverem ativados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="63a41-170">Archiving/Call Detail Recording/Quality of Experience services Store: The number of stores required for Archiving or Monitoring features, if they are enabled in your organization.</span></span>

  - <span data-ttu-id="63a41-171">Servidor requerido do banco de dados de back-end (pools requeridos): o número de servidores do banco de dados de back-end requeridos para suportar a carga de trabalho selecionada.</span><span class="sxs-lookup"><span data-stu-id="63a41-171">Back End Database Server Required (Pools Required): The number of back-end database servers required to support the selected workload.</span></span>

<span data-ttu-id="63a41-172">E mais, na linha próxima de 'Servidores de front-end totais, mais informações são fornecidas sobre a carga em seus servidores e rede para todas as cargas de trabalho planejadas e combinadas.</span><span class="sxs-lookup"><span data-stu-id="63a41-172">Additionally, in the row next to Total Front End Servers, more information is provided about the load on your servers and network for all the planned workloads combined.</span></span>

  - <span data-ttu-id="63a41-173">Carga média da CPU: o uso médio da CPU por servidor de front-end server.</span><span class="sxs-lookup"><span data-stu-id="63a41-173">Average CPU Load: The average CPU usage per Front End server.</span></span>

  - <span data-ttu-id="63a41-174">Rede em Mbps: a alocação da largura de banda requerida para suportar o modelo de uso fornecido.</span><span class="sxs-lookup"><span data-stu-id="63a41-174">Network in Mbps: The required bandwidth allocation to support the usage model that you entered.</span></span>

  - <span data-ttu-id="63a41-175">Memória em GB: a memória, em gigabytes, requerida para cada servidor de front-end server.</span><span class="sxs-lookup"><span data-stu-id="63a41-175">Memory in GB: Memory, in gigabytes, required for each Front End server.</span></span>

</div>

<div>

## <a name="adjusting-for-your-processors"></a><span data-ttu-id="63a41-176">Ajustando para seus processadores</span><span class="sxs-lookup"><span data-stu-id="63a41-176">Adjusting For Your Processors</span></span>

<span data-ttu-id="63a41-177">Todos os valores de uso da CPU supõem que cada servidor tem um processador dual, núcleo hex com 2.26 GHz, pelo menos 32 GB de memória, 8 ou mais drives de disco rídigo com 10.000 RPM e pelo menos 72 GB de espaço em disco livre.</span><span class="sxs-lookup"><span data-stu-id="63a41-177">All the CPU usage figures in the spreadsheet assume that each server has a dual processor, hex-core with 2.26 GHz, at least 32 GB of memory, and 8 or more 10,000-RPM hard disk drives with at least 72 GB free disk space.</span></span>

<span data-ttu-id="63a41-178">Se seus servidores tiverem processadores diferentes, você poderá ajustar os valores para corresponderem ao seu hardware.</span><span class="sxs-lookup"><span data-stu-id="63a41-178">If your servers have different processors, you can adjust the figures to match your hardware.</span></span>

<span data-ttu-id="63a41-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63a41-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

