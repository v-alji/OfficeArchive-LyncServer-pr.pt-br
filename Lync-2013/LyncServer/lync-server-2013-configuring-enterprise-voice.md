---
title: 'Lync Server 2013: Configurando o Enterprise Voice'
description: 'Lync Server 2013: Configurando o Enterprise Voice.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433119"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="f3c74-103">Configurando o Enterprise Voice no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3c74-103">Configuring Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3c74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3c74-104">

<span> </span></span></span>

<span data-ttu-id="f3c74-105">_**Tópico da última modificação:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="f3c74-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="f3c74-106">Para implantar o Enterprise Voice, você precisará configurar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f3c74-106">To deploy Enterprise Voice, you’ll need to configure the following:</span></span>

  - <span data-ttu-id="f3c74-107">Criar um tronco</span><span class="sxs-lookup"><span data-stu-id="f3c74-107">Create a Trunk</span></span>

  - <span data-ttu-id="f3c74-108">Definir uma política de voz</span><span class="sxs-lookup"><span data-stu-id="f3c74-108">Define a Voice Policy</span></span>

  - <span data-ttu-id="f3c74-109">Definir uma rota de voz</span><span class="sxs-lookup"><span data-stu-id="f3c74-109">Define a Voice Route</span></span>

  - <span data-ttu-id="f3c74-110">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="f3c74-110">Enable Users for Enterprise Voice</span></span>

<div>

## <a name="create-a-trunk"></a><span data-ttu-id="f3c74-111">Criar um tronco</span><span class="sxs-lookup"><span data-stu-id="f3c74-111">Create a Trunk</span></span>

<span data-ttu-id="f3c74-112">Você deve definir troncos na sua implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="f3c74-112">You must define trunks in your Enterprise Voice deployment.</span></span> <span data-ttu-id="f3c74-113">Para Location-Based roteamento, você deve criar uma configuração de tronco por tronco.</span><span class="sxs-lookup"><span data-stu-id="f3c74-113">For Location-Based Routing, you must create a trunk configuration per trunk.</span></span> <span data-ttu-id="f3c74-114">Use o construtor de topologia do Lync Server para definir seus troncos e use o comando do Windows PowerShell do Lync Server, o New-CsTrunkConfiguration ou o painel de controle do Lync Server para definir as configurações de tronco correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f3c74-114">Use the Lync Server Topology Builder to define your trunks, and use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, or the Lync Server Control Panel to define the corresponding trunk configurations.</span></span> <span data-ttu-id="f3c74-115">Mais informações sobre como habilitar o roteamento de Location-Based em configurações de tronco podem ser encontradas na seção, habilitar o roteamento de Location-Based para troncos, no tópico [habilitando Location-Based roteamento no Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="f3c74-115">More information on how to enable Location-Based Routing on trunk configurations can be found in the section, Enable Location-Based Routing to Trunks, in the topic, [Enabling Location-Based Routing in Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span></span> <span data-ttu-id="f3c74-116">Para este exemplo, a tabela a seguir ilustra os troncos usados nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="f3c74-116">For this example, the following table illustrates the trunks used in this scenario.</span></span>

<span data-ttu-id="f3c74-117">Para obter mais informações, consulte [definir troncos adicionais no construtor de topologias no Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span><span class="sxs-lookup"><span data-stu-id="f3c74-117">For more information, see [Define additional trunks in Topology Builder in Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c74-118">Nome do tronco</span><span class="sxs-lookup"><span data-stu-id="f3c74-118">Trunk name</span></span></th>
<th><span data-ttu-id="f3c74-119">Tipo de sistema</span><span class="sxs-lookup"><span data-stu-id="f3c74-119">System type</span></span></th>
<th><span data-ttu-id="f3c74-120">Nome</span><span class="sxs-lookup"><span data-stu-id="f3c74-120">Name</span></span></th>
<th><span data-ttu-id="f3c74-121">Local</span><span class="sxs-lookup"><span data-stu-id="f3c74-121">Location</span></span></th>
<th><span data-ttu-id="f3c74-122">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="f3c74-122">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c74-123">Tronco 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="f3c74-123">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="f3c74-124">Gateway PSTN</span><span class="sxs-lookup"><span data-stu-id="f3c74-124">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="f3c74-125">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="f3c74-125">DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="f3c74-126">Delhi</span><span class="sxs-lookup"><span data-stu-id="f3c74-126">Delhi</span></span></p></td>
<td><p><span data-ttu-id="f3c74-127">MS1</span><span class="sxs-lookup"><span data-stu-id="f3c74-127">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c74-128">Tronco 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="f3c74-128">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="f3c74-129">Gateway PSTN</span><span class="sxs-lookup"><span data-stu-id="f3c74-129">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="f3c74-130">HYD-GW</span><span class="sxs-lookup"><span data-stu-id="f3c74-130">HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="f3c74-131">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f3c74-131">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="f3c74-132">MS1</span><span class="sxs-lookup"><span data-stu-id="f3c74-132">MS1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3c74-133">Tronco 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-133">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="f3c74-134">RESPECTIVA</span><span class="sxs-lookup"><span data-stu-id="f3c74-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="f3c74-135">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-135">DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="f3c74-136">Delhi</span><span class="sxs-lookup"><span data-stu-id="f3c74-136">Delhi</span></span></p></td>
<td><p><span data-ttu-id="f3c74-137">MS1</span><span class="sxs-lookup"><span data-stu-id="f3c74-137">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c74-138">Tronco 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-138">Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="f3c74-139">RESPECTIVA</span><span class="sxs-lookup"><span data-stu-id="f3c74-139">PBX</span></span></p></td>
<td><p><span data-ttu-id="f3c74-140">HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-140">HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="f3c74-141">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f3c74-141">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="f3c74-142">MS1</span><span class="sxs-lookup"><span data-stu-id="f3c74-142">MS1</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a><span data-ttu-id="f3c74-143">Define as políticas de voz</span><span class="sxs-lookup"><span data-stu-id="f3c74-143">Defines Voice Policies</span></span>

<span data-ttu-id="f3c74-144">Você deve definir políticas de voz para a implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="f3c74-144">You must define voice policies for your Enterprise Voice deployment.</span></span> <span data-ttu-id="f3c74-145">Defina uma política de voz para impor Location-Based restrições de roteamento a um subconjunto de usuários se apenas um subconjunto delas for necessário para usar o roteamento de Location-Based.</span><span class="sxs-lookup"><span data-stu-id="f3c74-145">Define a Voice Policy to enforce Location-Based Routing restrictions to a subset of users if only a subset of them is required to use Location-Based Routing.</span></span> <span data-ttu-id="f3c74-146">Para este exemplo, a tabela a seguir ilustra as políticas de voz usadas neste cenário.</span><span class="sxs-lookup"><span data-stu-id="f3c74-146">For this example, the following table illustrates the voice policies used in this scenario.</span></span> <span data-ttu-id="f3c74-147">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="f3c74-147">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="f3c74-148">Para obter mais informações, consulte [Configurando políticas de voz e registros de uso PSTN para autorizar os recursos e privilégios de chamada no Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="f3c74-148">For more information, see [Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f3c74-149">Política de voz 1</span><span class="sxs-lookup"><span data-stu-id="f3c74-149">Voice policy 1</span></span></th>
<th><span data-ttu-id="f3c74-150">Política de voz 2</span><span class="sxs-lookup"><span data-stu-id="f3c74-150">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c74-151">ID da política de voz</span><span class="sxs-lookup"><span data-stu-id="f3c74-151">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="f3c74-152">Política de voz de Délhi</span><span class="sxs-lookup"><span data-stu-id="f3c74-152">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="f3c74-153">Política de voz Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f3c74-153">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c74-154">Usos de PSTN</span><span class="sxs-lookup"><span data-stu-id="f3c74-154">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="f3c74-155">Uso de Delhi, uso do PBX, uso do PBX Hyd</span><span class="sxs-lookup"><span data-stu-id="f3c74-155">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="f3c74-156">Uso do Hyderabad, Hyd do PBX, uso do PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-156">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3c74-157">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="f3c74-157">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="f3c74-158">Falso</span><span class="sxs-lookup"><span data-stu-id="f3c74-158">False</span></span></p></td>
<td><p><span data-ttu-id="f3c74-159">Falso</span><span class="sxs-lookup"><span data-stu-id="f3c74-159">False</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a><span data-ttu-id="f3c74-160">Definir roteiros de voz</span><span class="sxs-lookup"><span data-stu-id="f3c74-160">Define Voice Routes</span></span>

<span data-ttu-id="f3c74-161">Você deve definir rotas de voz para a implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="f3c74-161">You must define voice routes for your Enterprise Voice deployment.</span></span> <span data-ttu-id="f3c74-162">Para este exemplo, a tabela a seguir ilustra as rotas de voz usadas nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="f3c74-162">For this example, the following table illustrates the voice routes used in this scenario.</span></span> <span data-ttu-id="f3c74-163">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="f3c74-163">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="f3c74-164">Para obter mais informações, consulte [Configurando rotas de voz para chamadas de saída no Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span><span class="sxs-lookup"><span data-stu-id="f3c74-164">For more information, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f3c74-165">Rota de voz 1</span><span class="sxs-lookup"><span data-stu-id="f3c74-165">Voice route 1</span></span></th>
<th><span data-ttu-id="f3c74-166">Rota de voz 2</span><span class="sxs-lookup"><span data-stu-id="f3c74-166">Voice route 2</span></span></th>
<th><span data-ttu-id="f3c74-167">Rota de voz 3</span><span class="sxs-lookup"><span data-stu-id="f3c74-167">Voice route 3</span></span></th>
<th><span data-ttu-id="f3c74-168">Rota de voz 4</span><span class="sxs-lookup"><span data-stu-id="f3c74-168">Voice route 4</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c74-169">Nome</span><span class="sxs-lookup"><span data-stu-id="f3c74-169">Name</span></span></p></td>
<td><p><span data-ttu-id="f3c74-170">Rota de Délhi</span><span class="sxs-lookup"><span data-stu-id="f3c74-170">Delhi route</span></span></p></td>
<td><p><span data-ttu-id="f3c74-171">Rota Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f3c74-171">Hyderabad route</span></span></p></td>
<td><p><span data-ttu-id="f3c74-172">Rota de del do PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-172">PBX Del route</span></span></p></td>
<td><p><span data-ttu-id="f3c74-173">Rota Hyd do PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-173">PBX Hyd route</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c74-174">Usos de PSTN</span><span class="sxs-lookup"><span data-stu-id="f3c74-174">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="f3c74-175">Uso de Delhi</span><span class="sxs-lookup"><span data-stu-id="f3c74-175">Delhi usage</span></span></p></td>
<td><p><span data-ttu-id="f3c74-176">Uso do Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f3c74-176">Hyderabad usage</span></span></p></td>
<td><p><span data-ttu-id="f3c74-177">Uso do PBX del</span><span class="sxs-lookup"><span data-stu-id="f3c74-177">PBX Del usage</span></span></p></td>
<td><p><span data-ttu-id="f3c74-178">Uso do Hyd do PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-178">PBX Hyd usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3c74-179">Tronco</span><span class="sxs-lookup"><span data-stu-id="f3c74-179">Trunk</span></span></p></td>
<td><p><span data-ttu-id="f3c74-180">Tronco 1 DEL-GW</span><span class="sxs-lookup"><span data-stu-id="f3c74-180">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="f3c74-181">Tronco 2 HYD-GW</span><span class="sxs-lookup"><span data-stu-id="f3c74-181">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="f3c74-182">Tronco 3 DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-182">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="f3c74-183">Tronco 4 HYD-PBX</span><span class="sxs-lookup"><span data-stu-id="f3c74-183">Trunk 4 HYD-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a><span data-ttu-id="f3c74-184">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="f3c74-184">Enable Users for Enterprise Voice</span></span>

<span data-ttu-id="f3c74-185">Habilite os usuários para o Enterprise Voice e atribua a eles uma política de voz que você definiu anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f3c74-185">Enable users for Enterprise Voice and assign them a voice policy you’ve previously defined.</span></span> <span data-ttu-id="f3c74-186">Para este exemplo, a tabela a seguir ilustra a atribuição usada neste cenário.</span><span class="sxs-lookup"><span data-stu-id="f3c74-186">For this example, the following table illustrates the assignment used in this scenario.</span></span> <span data-ttu-id="f3c74-187">Somente as configurações específicas do roteamento Location-Based são incluídas na tabela para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="f3c74-187">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="f3c74-188">Para obter mais informações, consulte [habilitar usuários para Enterprise Voice no Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c74-188">For more information, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f3c74-189">Usuários localizados em Delhi</span><span class="sxs-lookup"><span data-stu-id="f3c74-189">Users located in Delhi</span></span></th>
<th><span data-ttu-id="f3c74-190">Usuários localizados no Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f3c74-190">Users located in Hyderabad</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c74-191">Política de voz associada</span><span class="sxs-lookup"><span data-stu-id="f3c74-191">Associated voice policy</span></span></p></td>
<td><p><span data-ttu-id="f3c74-192">Política de voz de Délhi</span><span class="sxs-lookup"><span data-stu-id="f3c74-192">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="f3c74-193">Política de voz Hyderabad</span><span class="sxs-lookup"><span data-stu-id="f3c74-193">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c74-194">Usuários de exemplo</span><span class="sxs-lookup"><span data-stu-id="f3c74-194">Sample users</span></span></p></td>
<td><p><span data-ttu-id="f3c74-195">DEL-LYNC-1, DEL-LYNC-2, DEL-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="f3c74-195">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
<td><p><span data-ttu-id="f3c74-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span><span class="sxs-lookup"><span data-stu-id="f3c74-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f3c74-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3c74-197">See Also</span></span>


[<span data-ttu-id="f3c74-198">Configurando o Roteamento Baseado em Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3c74-198">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="f3c74-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3c74-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

