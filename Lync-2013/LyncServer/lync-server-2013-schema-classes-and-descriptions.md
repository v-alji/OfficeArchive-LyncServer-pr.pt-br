---
title: 'Lync Server 2013: descrições e classes do esquema'
description: 'Lync Server 2013: classes e descrições de esquema.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema classes and descriptions
ms:assetid: 7d43b920-ac37-40cc-adfe-be289bda6e9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398625(v=OCS.15)
ms:contentKeyID: 48184612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec27c2e00a7f969dbc13c91b06313c8045894a9e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441967"
---
# <a name="schema-classes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="eff3a-103">Classes e descrições de esquema no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eff3a-103">Schema classes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eff3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eff3a-104">

<span> </span></span></span>

<span data-ttu-id="eff3a-105">_**Tópico da última modificação:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="eff3a-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="eff3a-106">Esta seção descreve todas as classes de esquema usadas pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eff3a-106">This section describes all the schema classes used by Lync Server 2013.</span></span>

<div>

## <a name="schema-classes-and-descriptions"></a><span data-ttu-id="eff3a-107">Classes e descrições de esquema</span><span class="sxs-lookup"><span data-stu-id="eff3a-107">Schema Classes and Descriptions</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eff3a-108">Classe</span><span class="sxs-lookup"><span data-stu-id="eff3a-108">Class</span></span></th>
<th><span data-ttu-id="eff3a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="eff3a-109">Description</span></span></th>
<th><span data-ttu-id="eff3a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="eff3a-110">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-111">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="eff3a-111">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="eff3a-112">Destinatário de email do Exchange Unified Messaging (UM).</span><span class="sxs-lookup"><span data-stu-id="eff3a-112">Exchange Unified Messaging (UM) email recipient.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-113">Essa classe auxiliar é compartilhada com o Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="eff3a-113">This auxiliary class is shared with Exchange UM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-114">msRTCSIP-ApplicationContacts</span><span class="sxs-lookup"><span data-stu-id="eff3a-114">msRTCSIP-ApplicationContacts</span></span></p></td>
<td><p><span data-ttu-id="eff3a-115">Essa classe é um contêiner para vários contatos de aplicativo e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-115">This class is a container for multiple application contacts and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-116">Novo no Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-116">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-117">msRTCSIP-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="eff3a-117">msRTCSIP-ApplicationServer</span></span></p></td>
<td><p><span data-ttu-id="eff3a-118">Essa classe contém a entrada para o ponto de controle de serviço para uma instância de serviços de aplicativos de comunicação unificada (UCAS).</span><span class="sxs-lookup"><span data-stu-id="eff3a-118">This class holds the entry for the service control point for an instance of Unified Communications Application Services (UCAS).</span></span></p></td>
<td><p><span data-ttu-id="eff3a-119">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-119">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-120">msRTCSIP-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="eff3a-120">msRTCSIP-ApplicationServerService</span></span></p></td>
<td><p><span data-ttu-id="eff3a-121">Essa classe fornece uma associação de um pool específico ao seu serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-121">This class provides an association from a specific pool to its Application service.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-122">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-122">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-123">msRTCSIP-ApplicationServerSettings</span><span class="sxs-lookup"><span data-stu-id="eff3a-123">msRTCSIP-ApplicationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="eff3a-124">Esta classe auxiliar para msRTCSIP-ApplicationServer mantém atributos representando configurações para instâncias do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-124">This auxiliary class to msRTCSIP-ApplicationServer holds attributes representing settings for instances of the Application service.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-125">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-125">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-126">msRTCSIP-arquivo morto (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-126">msRTCSIP-Archive (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-127">Esta classe auxiliar para msRTCSIP-GlobalContainer armazena todas as configurações relacionadas ao arquivamento.</span><span class="sxs-lookup"><span data-stu-id="eff3a-127">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to archiving.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-128">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-128">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-129">msRTCSIP-ArchivingServer (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-129">msRTCSIP-ArchivingServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-130">Essa classe representa um único servidor de arquivamento de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="eff3a-130">This class represents a single instant messaging Archiving Server.</span></span> <span data-ttu-id="eff3a-131">Uma instância dessa classe é criada quando um computador é ativado como um servidor de arquivamento de mensagens instantâneas, como um computador com o serviço de arquivamento de mensagens instantâneas instalado.</span><span class="sxs-lookup"><span data-stu-id="eff3a-131">An instance of this class is created when a computer is activated as an instant messaging Archiving Server, such as a computer with the Instant Messaging Archiving service installed.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-132">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-132">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-133">msRTCSIP-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="eff3a-133">msRTCSIP-ConferenceDirectories</span></span></p></td>
<td><p><span data-ttu-id="eff3a-134">Essa classe é um contêiner para várias instâncias de diretórios de conferência e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-134">This class is a container for multiple instances of conference directories and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-135">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-135">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-136">msRTCSIP-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="eff3a-136">msRTCSIP-ConferenceDirectory</span></span></p></td>
<td><p><span data-ttu-id="eff3a-137">Essa classe contém atributos que representam as configurações de um diretório de conferência específico.</span><span class="sxs-lookup"><span data-stu-id="eff3a-137">This class holds attributes representing settings for a specific conference directory.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-138">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-138">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-139">msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="eff3a-139">msRTCSIP-ConnectionPoint</span></span></p></td>
<td><p><span data-ttu-id="eff3a-140">Ponto de controle de serviço genérico (SCP) para especificar o computador como um servidor que executa o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eff3a-140">Generic service control point (SCP) to specify the computer as a server running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-141">Novo no Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-141">New in Lync 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-142">msRTCSIP-DefaultCWABank</span><span class="sxs-lookup"><span data-stu-id="eff3a-142">msRTCSIP-DefaultCWABank</span></span></p></td>
<td><p><span data-ttu-id="eff3a-143">Essa classe auxiliar mantém as configurações para um banco do Microsoft Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="eff3a-143">This auxiliary class holds the settings for a Microsoft Lync Web App bank.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-144">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-144">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-145">msRTCSIP-domínio</span><span class="sxs-lookup"><span data-stu-id="eff3a-145">msRTCSIP-Domain</span></span></p></td>
<td><p><span data-ttu-id="eff3a-146">Essa classe contém atributos que definem os domínios configurados do registrador SIP.</span><span class="sxs-lookup"><span data-stu-id="eff3a-146">This class holds attributes that define the configured domains of the SIP Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-147">msRTCSIP-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="eff3a-147">msRTCSIP-EdgeProxy</span></span></p></td>
<td><p><span data-ttu-id="eff3a-148">Esse contêiner de classe representa um único serviço de borda de acesso.</span><span class="sxs-lookup"><span data-stu-id="eff3a-148">This class container represents a single Access Edge service.</span></span> <span data-ttu-id="eff3a-149">Como um serviço de borda de acesso é implantado na rede de perímetro e os clientes geralmente não permitem o acesso dos serviços de domínio Active Directory da rede de perímetro, as instâncias do serviço de borda de acesso não estão associadas à rede do Active Directory da intranet.</span><span class="sxs-lookup"><span data-stu-id="eff3a-149">Because an Access Edge service is deployed in the perimeter network and customers usually do not allow Active Directory Domain Services access from the perimeter network, instances of Access Edge service are not joined to the intranet’s Active Directory network.</span></span> <span data-ttu-id="eff3a-150">Portanto, os proxies de acesso não são registrados automaticamente no AD DS.</span><span class="sxs-lookup"><span data-stu-id="eff3a-150">Therefore, Access Proxies are not automatically registered in AD DS.</span></span> <span data-ttu-id="eff3a-151">O administrador deve configurar manualmente a existência de cada instância do serviço de borda do Access no AD DS.</span><span class="sxs-lookup"><span data-stu-id="eff3a-151">The administrator must manually configure the existence of each instance of Access Edge service in AD DS.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-152">msRTCSIP-EnterpriseMCUSettings</span><span class="sxs-lookup"><span data-stu-id="eff3a-152">msRTCSIP-EnterpriseMCUSettings</span></span></p></td>
<td><p><span data-ttu-id="eff3a-153">Esta classe auxiliar para msRTCSIP-MCU armazena atributos que representam configurações para servidores de conferência.</span><span class="sxs-lookup"><span data-stu-id="eff3a-153">This auxiliary class to msRTCSIP-MCU holds attributes representing settings for Conferencing servers.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-154">Novo no Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-154">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-155">msRTCSIP-EnterpriseMediationServerSettings</span><span class="sxs-lookup"><span data-stu-id="eff3a-155">msRTCSIP-EnterpriseMediationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="eff3a-156">Esta classe auxiliar para msRTCSIP-MediationServer mantém atributos representando configurações para servidores de mediação.</span><span class="sxs-lookup"><span data-stu-id="eff3a-156">This auxiliary class to msRTCSIP-MediationServer holds attributes representing settings for Mediation Servers.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-157">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-157">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-158">msRTCSIP-EnterpriseServerSettings</span><span class="sxs-lookup"><span data-stu-id="eff3a-158">msRTCSIP-EnterpriseServerSettings</span></span></p></td>
<td><p><span data-ttu-id="eff3a-159">Essa classe auxiliar para o msRTCSIP-Server armazena atributos que representam configurações para servidores SIP.</span><span class="sxs-lookup"><span data-stu-id="eff3a-159">This auxiliary class to msRTCSIP-Server holds attributes representing settings for SIP servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-160">msRTCSIP-Federação</span><span class="sxs-lookup"><span data-stu-id="eff3a-160">msRTCSIP-Federation</span></span></p></td>
<td><p><span data-ttu-id="eff3a-161">Esta classe auxiliar para msRTCSIP-GlobalContainer armazena todas as configurações relacionadas à Federação.</span><span class="sxs-lookup"><span data-stu-id="eff3a-161">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to federation.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-162">msRTCSIP-GlobalContainer</span><span class="sxs-lookup"><span data-stu-id="eff3a-162">msRTCSIP-GlobalContainer</span></span></p></td>
<td><p><span data-ttu-id="eff3a-163">Essa classe contém todas as configurações que se aplicam em toda a implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eff3a-163">This class holds all settings that apply throughout a Lync Server deployment.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-164">msRTCSIP-GlobalUserPolicy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-164">msRTCSIP-GlobalUserPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-165">Essa classe representa uma única política de reunião do Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="eff3a-165">This class represents a single Office Communications Server meeting policy.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-166">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-166">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-167">msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="eff3a-167">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="eff3a-168">O objeto de configuração de topologia global local.</span><span class="sxs-lookup"><span data-stu-id="eff3a-168">The local global topology setting object.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-169">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-169">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-170">msRTCSIP-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="eff3a-170">msRTCSIP-GlobalTopologySettings</span></span></p></td>
<td><p><span data-ttu-id="eff3a-171">Contêiner para armazenar objetos de configuração de topologia global.</span><span class="sxs-lookup"><span data-stu-id="eff3a-171">Container to hold global topology setting objects.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-172">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-172">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-173">msRTCSIP-LocalNormalization</span><span class="sxs-lookup"><span data-stu-id="eff3a-173">msRTCSIP-LocalNormalization</span></span></p></td>
<td><p><span data-ttu-id="eff3a-174">Essa classe é um contêiner que representa uma instância de uma regra de normalização de localização.</span><span class="sxs-lookup"><span data-stu-id="eff3a-174">This class is a container that represents an instance of a location normalization rule.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-175">msRTCSIP-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="eff3a-175">msRTCSIP-LocationContactMapping</span></span></p></td>
<td><p><span data-ttu-id="eff3a-176">Essa classe é criada pelo aplicativo atendedor de conferência e mantém os atributos usados para categorizar números de telefone de conferência por região.</span><span class="sxs-lookup"><span data-stu-id="eff3a-176">This class is created by the Conferencing Attendant application and holds attributes used to categorize conference telephone numbers by region.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-177">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-177">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-178">msRTCSIP-LocationContactMappings</span><span class="sxs-lookup"><span data-stu-id="eff3a-178">msRTCSIP-LocationContactMappings</span></span></p></td>
<td><p><span data-ttu-id="eff3a-179">Essa classe é um contêiner para várias instâncias de mapeamentos de contatos de local e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-179">This class is a container for multiple instances of location contact mappings and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-180">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-180">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-181">msRTCSIP-LocationProfile</span><span class="sxs-lookup"><span data-stu-id="eff3a-181">msRTCSIP-LocationProfile</span></span></p></td>
<td><p><span data-ttu-id="eff3a-182">Essa classe é um contêiner que representa um perfil de local específico.</span><span class="sxs-lookup"><span data-stu-id="eff3a-182">This class is a container that represents a specific location profile.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-183">msRTCSIP-LocationProfiles (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-183">msRTCSIP-LocationProfiles (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-184">Essa classe é um contêiner para vários perfis de localização e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-184">This class is a container for multiple location profiles and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-185">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-185">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-186">msRTCSIP-LocalNormalizations (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-186">msRTCSIP-LocalNormalizations (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-187">Essa classe é um contêiner para várias regras de normalização locais e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-187">This class is a container for multiple local normalization rules and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-188">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-188">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-189">msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="eff3a-189">msRTCSIP-MCU</span></span></p></td>
<td><p><span data-ttu-id="eff3a-190">Essa classe representa um único servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="eff3a-190">This class represents a single Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-191">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-191">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-192">msRTCSIP-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="eff3a-192">msRTCSIP-MCUFactories</span></span></p></td>
<td><p><span data-ttu-id="eff3a-193">Essa classe contém várias classes msRTCSIP-MCUFactory e não tem nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-193">This class holds multiple msRTCSIP-MCUFactory classes and does not have attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-194">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-194">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-195">msRTCSIP-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="eff3a-195">msRTCSIP-MCUFactory</span></span></p></td>
<td><p><span data-ttu-id="eff3a-196">Essa classe é um contêiner que representa uma fábrica de servidor de conferência para um único tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="eff3a-196">This class is a container representing a Conferencing Server Factory for a single medium type.</span></span> <span data-ttu-id="eff3a-197">Uma instância dessa classe é criada quando o primeiro servidor de conferência para esse tipo e fornecedor específico é ativado.</span><span class="sxs-lookup"><span data-stu-id="eff3a-197">An instance of this class is created when the first Conferencing server for this particular type and vendor is activated.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-198">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-198">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-199">msRTCSIP-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="eff3a-199">msRTCSIP-MCUFactoryService</span></span></p></td>
<td><p><span data-ttu-id="eff3a-200">Essa classe fornece uma associação de um pool específico à sua fábrica do servidor de conferência.</span><span class="sxs-lookup"><span data-stu-id="eff3a-200">This class provides an association from a specific pool to its Conferencing Server Factory.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-201">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-201">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-202">msRTCSIP-MediationServer</span><span class="sxs-lookup"><span data-stu-id="eff3a-202">msRTCSIP-MediationServer</span></span></p></td>
<td><p><span data-ttu-id="eff3a-203">Essa classe contém a entrada para o ponto de controle de serviço para um servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="eff3a-203">This class holds the entry for the service control point for a Mediation Server.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-204">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-204">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-205">msRTCSIP – reunião (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-205">msRTCSIP-Meeting (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-206">Esta classe auxiliar para msRTCSIP-GlobalContainer mantém os atributos que representam as configurações de reunião configuráveis.</span><span class="sxs-lookup"><span data-stu-id="eff3a-206">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing configurable meeting settings.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-207">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-207">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-208">msRTCSIP – mobilidade</span><span class="sxs-lookup"><span data-stu-id="eff3a-208">msRTCSIP-Mobility</span></span></p></td>
<td><p><span data-ttu-id="eff3a-209">Contêiner que armazena as configurações de mobilidade global.</span><span class="sxs-lookup"><span data-stu-id="eff3a-209">Container that stores the global mobility settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-210">msRTCSIP-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="eff3a-210">msRTCSIP-MonitoringServer</span></span></p></td>
<td><p><span data-ttu-id="eff3a-211">Essa classe contém atributos que representam as configurações de um único servidor de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="eff3a-211">This class holds attributes that represent settings for a single Monitoring Server.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-212">Novo no Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="eff3a-212">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-213">msRTCSIP-PhoneRoute (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-213">msRTCSIP-PhoneRoute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-214">Essa classe é um contêiner que representa uma instância de uma rota de menor custo para um gateway ou conjunto de gateways.</span><span class="sxs-lookup"><span data-stu-id="eff3a-214">This class is a container representing an instance of a least cost route to a gateway or set of gateways.</span></span> <span data-ttu-id="eff3a-215">Essas informações são usadas por todos os pools ou servidores da empresa que executam o Standard Edition para direcionar chamadas feitas para a rede telefônica pública comutada (PSTN) da maneira mais econômica.</span><span class="sxs-lookup"><span data-stu-id="eff3a-215">This information is used by all Enterprise pools or servers running Standard Edition to route outgoing calls to the public switched telephone network (PSTN) in the most cost effective way.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-216">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-216">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-217">msRTCSIP-PhoneRoutes (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-217">msRTCSIP-PhoneRoutes (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-218">Essa classe é um contêiner para várias rotas de custo mínimo e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-218">This class is a container for multiple, least cost routes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-219">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-219">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-220">msRTCSIP-políticas (obsoletas)</span><span class="sxs-lookup"><span data-stu-id="eff3a-220">msRTCSIP-Policies (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-221">Essa classe contém várias classes de política do Lync Server e não tem nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-221">This class holds multiple Lync Server policy classes and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-222">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-222">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-223">msRTCSIP-pool</span><span class="sxs-lookup"><span data-stu-id="eff3a-223">msRTCSIP-Pool</span></span></p></td>
<td><p><span data-ttu-id="eff3a-224">Essa classe representa um único pool do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eff3a-224">This class represents a single Lync Server pool.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-225">msRTCSIP-Pools</span><span class="sxs-lookup"><span data-stu-id="eff3a-225">msRTCSIP-Pools</span></span></p></td>
<td><p><span data-ttu-id="eff3a-226">Essa classe contém vários pools do Lync Server e não tem nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-226">This class holds multiple Lync Server pools and does not have any attributes itself.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-227">msRTCSIP-PoolService</span><span class="sxs-lookup"><span data-stu-id="eff3a-227">msRTCSIP-PoolService</span></span></p></td>
<td><p><span data-ttu-id="eff3a-228">Essa classe representa o ponto de controle pointservice do controle de serviço de um pool.</span><span class="sxs-lookup"><span data-stu-id="eff3a-228">This class represents the service control pointservice control point of a pool.</span></span> <span data-ttu-id="eff3a-229">Os usuários hospedados em um pool têm seus atributos msRTCSIP-PrimaryHomeServer apontam para uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="eff3a-229">Users hosted on a pool have their msRTCSIP-PrimaryHomeServer attribute point to an instance of this class.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-230">msRTCSIP-presença</span><span class="sxs-lookup"><span data-stu-id="eff3a-230">msRTCSIP-Presence</span></span></p></td>
<td><p><span data-ttu-id="eff3a-231">Contêiner que armazena as configurações de presença global.</span><span class="sxs-lookup"><span data-stu-id="eff3a-231">Container that stores the global presence settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-232">msRTCSIP-registrador</span><span class="sxs-lookup"><span data-stu-id="eff3a-232">msRTCSIP-Registrar</span></span></p></td>
<td><p><span data-ttu-id="eff3a-233">Esta classe auxiliar para msRTCSIP-GlobalContainer mantém os atributos que representam as configurações de usuário mantidas pelos servidores de registradores SIP.</span><span class="sxs-lookup"><span data-stu-id="eff3a-233">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing user settings maintained by the SIP Registrar servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-234">msRTCSIP-RouteUsage (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-234">msRTCSIP-RouteUsage (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-235">Essa classe é um contêiner que representa uma instância de um uso de rota telefônica.</span><span class="sxs-lookup"><span data-stu-id="eff3a-235">This class is a container representing an instance of a phone route usage.</span></span> <span data-ttu-id="eff3a-236">Uma classe de uso de rota de telefone consiste em um campo de atributo e um campo de descrição.</span><span class="sxs-lookup"><span data-stu-id="eff3a-236">A phone route usage class consists of an attribute field and a description field.</span></span> <span data-ttu-id="eff3a-237">O campo Attribute define um tipo de uso.</span><span class="sxs-lookup"><span data-stu-id="eff3a-237">The attribute field defines a usage type.</span></span> <span data-ttu-id="eff3a-238">O campo Descrição permite que os administradores descrevam o uso para esse atributo na rota do telefone.</span><span class="sxs-lookup"><span data-stu-id="eff3a-238">The description field allows administrators to describe the usage for this attribute in the phone route.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-239">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-239">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-240">msRTCSIP-RouteUsages (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-240">msRTCSIP-RouteUsages (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-241">Essa classe contém várias instâncias da classe msRTCSIP-RouteUsage e não tem nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-241">This class holds multiple instances of the msRTCSIP-RouteUsage class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-242">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-243">msRTCSIP-pesquisa</span><span class="sxs-lookup"><span data-stu-id="eff3a-243">msRTCSIP-Search</span></span></p></td>
<td><p><span data-ttu-id="eff3a-244">Esta classe auxiliar para msRTCSIP-GlobalContainer mantém os atributos que limitam e controlam o escopo dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="eff3a-244">This auxiliary class to msRTCSIP-GlobalContainer holds attributes that limit and control the scope of search results.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-245">msRTCSIP-servidor</span><span class="sxs-lookup"><span data-stu-id="eff3a-245">msRTCSIP-Server</span></span></p></td>
<td><p><span data-ttu-id="eff3a-246">Essa classe representa um único servidor que executa o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="eff3a-246">This class represents a single server running Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-247">msRTCSIP-serviço</span><span class="sxs-lookup"><span data-stu-id="eff3a-247">msRTCSIP-Service</span></span></p></td>
<td><p><span data-ttu-id="eff3a-248">Essa classe mantém o contêiner de configurações globais e os objetos msRTCSIP-Domain.</span><span class="sxs-lookup"><span data-stu-id="eff3a-248">This class holds the global settings container and msRTCSIP-Domain objects.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-249">msRTCSIP-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="eff3a-249">msRTCSIP-TrustedMCU</span></span></p></td>
<td><p><span data-ttu-id="eff3a-250">Essa classe contém atributos que representam as configurações de um servidor de conferência confiável.</span><span class="sxs-lookup"><span data-stu-id="eff3a-250">This class holds attributes that represent settings for a trusted Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-251">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-251">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-252">msRTCSIP-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="eff3a-252">msRTCSIP-TrustedMCUs</span></span></p></td>
<td><p><span data-ttu-id="eff3a-253">Essa classe contém várias instâncias da classe msRTCSIP-TrustedMCU e não tem nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-253">This class holds multiple instances of the msRTCSIP-TrustedMCU class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-254">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-254">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-255">msRTCSIP-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="eff3a-255">msRTCSIP-TrustedProxies</span></span></p></td>
<td><p><span data-ttu-id="eff3a-256">Essa classe contém várias classes msRTCSIP-TrustedProxy e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-256">This class holds multiple msRTCSIP-TrustedProxy classes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-257">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-257">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-258">msRTCSIP-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="eff3a-258">msRTCSIP-TrustedProxy</span></span></p></td>
<td><p><span data-ttu-id="eff3a-259">Essa classe é um contêiner que representa um servidor de proxy em execução.</span><span class="sxs-lookup"><span data-stu-id="eff3a-259">This class is a container representing a server running Proxy Server.</span></span> <span data-ttu-id="eff3a-260">Uma instância dessa classe é criada ao ativar um novo servidor proxy em um computador associado ao AD DS.</span><span class="sxs-lookup"><span data-stu-id="eff3a-260">An instance of this class is created when activating a new Proxy Server on a computer joined to AD DS.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-261">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-261">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-262">msRTCSIP-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="eff3a-262">msRTCSIP-TrustedServer</span></span></p></td>
<td><p><span data-ttu-id="eff3a-263">Essa classe contém atributos que representam as configurações de um servidor confiável.</span><span class="sxs-lookup"><span data-stu-id="eff3a-263">This class holds attributes that represent settings for a trusted server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-264">msRTCSIP-TrustedService</span><span class="sxs-lookup"><span data-stu-id="eff3a-264">msRTCSIP-TrustedService</span></span></p></td>
<td><p><span data-ttu-id="eff3a-265">Essa classe é um contêiner que representa um serviço confiável que é roteável usando um endereço de URI (GRUU) do agente do usuário roteável globalmente.</span><span class="sxs-lookup"><span data-stu-id="eff3a-265">This class is a container representing a trusted service that is routable using a Globally Routable User Agent URI (GRUU) address.</span></span> <span data-ttu-id="eff3a-266">Uma instância dessa classe é criada quando um novo servidor confiável pelo Lync Server é ativado.</span><span class="sxs-lookup"><span data-stu-id="eff3a-266">An instance of this class is created when a new server that is trusted by Lync Server is activated.</span></span> <span data-ttu-id="eff3a-267">Este servidor confiável deve estar associado a um domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eff3a-267">This trusted server must be joined to an Active Directory domain.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-268">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-268">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-269">msRTCSIP-Confiáveisservices</span><span class="sxs-lookup"><span data-stu-id="eff3a-269">msRTCSIP-TrustedServices</span></span></p></td>
<td><p><span data-ttu-id="eff3a-270">Essa classe é um contêiner para vários servidores GRUU e não contém nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-270">This class is a container for multiple GRUU servers and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-271">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-271">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-272">msRTCSIP-TrustedWebComponentsServer</span><span class="sxs-lookup"><span data-stu-id="eff3a-272">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
<td><p><span data-ttu-id="eff3a-273">Essa classe contém atributos que representam as configurações para um componente da Web confiável.</span><span class="sxs-lookup"><span data-stu-id="eff3a-273">This class holds attributes that represent the settings for a trusted web component.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-274">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-274">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-275">msRTCSIP-TrustedWebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="eff3a-275">msRTCSIP-TrustedWebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="eff3a-276">Essa classe contém várias instâncias da classe msRTCSIP-TrustedWebComponentServer e não tem nenhum próprio atributo.</span><span class="sxs-lookup"><span data-stu-id="eff3a-276">This class holds multiple instances of the msRTCSIP-TrustedWebComponentServer class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-277">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-277">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-278">msRTCSIP-UnifiedCommunications (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="eff3a-278">msRTCSIP-UnifiedCommunications (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="eff3a-279">Esta classe auxiliar para msRTCSIP-GlobalContainer mantém os atributos relacionados à comunicação unificada.</span><span class="sxs-lookup"><span data-stu-id="eff3a-279">This auxiliary class to msRTCSIP-GlobalContainer holds attributes related to unified communications.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-280">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="eff3a-280">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-281">msRTCSIP-WebComponents</span><span class="sxs-lookup"><span data-stu-id="eff3a-281">msRTCSIP-WebComponents</span></span></p></td>
<td><p><span data-ttu-id="eff3a-282">Essa classe mantém o ponto de controle pointservice do controle de serviço para o Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="eff3a-282">This class holds the service control pointservice control point for Internet Information Server (IIS).</span></span> <span data-ttu-id="eff3a-283">Ele identifica um servidor como um servidor de componentes Web.</span><span class="sxs-lookup"><span data-stu-id="eff3a-283">It identifies a server as a web components server.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-284">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-284">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff3a-285">msRTCSIP-WebComponentsService</span><span class="sxs-lookup"><span data-stu-id="eff3a-285">msRTCSIP-WebComponentsService</span></span></p></td>
<td><p><span data-ttu-id="eff3a-286">Essa classe fornece uma associação de um pool específico para os componentes Web que o pool irá usar.</span><span class="sxs-lookup"><span data-stu-id="eff3a-286">This class provides an association from a specific pool to the web components that the pool will use.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-287">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-287">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff3a-288">msRTCSIP-WebComponentSettings</span><span class="sxs-lookup"><span data-stu-id="eff3a-288">msRTCSIP-WebComponentSettings</span></span></p></td>
<td><p><span data-ttu-id="eff3a-289">Esta classe auxiliar para msRTCSIP-WebComponents mantém atributos representando configurações para componentes Web.</span><span class="sxs-lookup"><span data-stu-id="eff3a-289">This auxiliary class to msRTCSIP-WebComponents holds attributes representing settings for web components.</span></span></p></td>
<td><p><span data-ttu-id="eff3a-290">Novo no Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="eff3a-290">New in Communications Server 2007.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="eff3a-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eff3a-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

