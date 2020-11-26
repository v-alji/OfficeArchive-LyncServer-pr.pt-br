---
title: 'Lync Server 2013: atributos e descrições do esquema'
description: 'Lync Server 2013: atributos e descrições do esquema.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes and descriptions
ms:assetid: b009df76-9c22-471d-b57a-bda009a98261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412841(v=OCS.15)
ms:contentKeyID: 48185083
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18888d20a772b3e84970e7d874bd6b6964affc75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444956"
---
# <a name="schema-attributes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="d4308-103">Atributos e descrições de esquema no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4308-103">Schema attributes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4308-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4308-104">

<span> </span></span></span>

<span data-ttu-id="d4308-105">_**Tópico da última modificação:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="d4308-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="d4308-106">Esta seção descreve todos os atributos de esquema usados pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d4308-106">This section describes all the schema attributes used by Lync Server 2013.</span></span> <span data-ttu-id="d4308-107">Para as classes associadas a atributos, consulte [atributos de esquema por classe no Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="d4308-107">For the classes associated with attributes, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span> <span data-ttu-id="d4308-108">Para obter uma lista de classes e atributos que são novos no Lync Server 2013, consulte [mudanças de esquema no Lync server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="d4308-108">For a list of classes and attributes that are new in Lync Server 2013, see [Schema changes in Lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span></span>

<span data-ttu-id="d4308-109">Os atributos que são pares vinculados são especificados como links de encaminhamento ou links para trás.</span><span class="sxs-lookup"><span data-stu-id="d4308-109">Attributes that are linked pairs are specified as forward links or back links.</span></span> <span data-ttu-id="d4308-110">Um atributo que faz referência a outro objeto é um link de encaminhamento; o atributo do outro objeto que faz referência novamente ao primeiro objeto é um link para trás.</span><span class="sxs-lookup"><span data-stu-id="d4308-110">An attribute that refers to another object is a forward link; the attribute of the other object that refers back to the first object is a back link.</span></span> <span data-ttu-id="d4308-111">Os links de encaminhamento são atualizáveis, enquanto links de volta são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d4308-111">Forward links are updatable, while back links are read-only.</span></span>

<span data-ttu-id="d4308-112">Alguns atributos têm um valor de máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="d4308-112">Some attributes have a bit-mask value.</span></span> <span data-ttu-id="d4308-113">Para esses atributos, cada configuração é representada por um bit, e o valor decimal exibido representa a posição do bit.</span><span class="sxs-lookup"><span data-stu-id="d4308-113">For these attributes, each setting is represented by a bit, and the displayed decimal value represents the bit position.</span></span> <span data-ttu-id="d4308-114">Posições de bit começam com bit 0.</span><span class="sxs-lookup"><span data-stu-id="d4308-114">Bit positions start with bit 0.</span></span> <span data-ttu-id="d4308-115">Por exemplo, 1 (binário) é bit 0 definido e 10000 (binário) é um bit 4 definido.</span><span class="sxs-lookup"><span data-stu-id="d4308-115">For example, 1 (binary) is bit 0 set and 10000 (binary) is bit 4 set.</span></span> <span data-ttu-id="d4308-116">Cada bit representa uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="d4308-116">Each bit represents a property.</span></span> <span data-ttu-id="d4308-117">Veja a seguir alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="d4308-117">The following are some examples:</span></span>

  - <span data-ttu-id="d4308-118">10000 (binário) tem um valor decimal de 16 (ou seja, bit 4 é definido).</span><span class="sxs-lookup"><span data-stu-id="d4308-118">10000 (binary) has a decimal value of 16 (that is, bit 4 is set).</span></span>

  - <span data-ttu-id="d4308-119">100 milhões (binário) tem um valor decimal de 256 (ou seja, o bit 8 é definido).</span><span class="sxs-lookup"><span data-stu-id="d4308-119">100000000 (binary) has a decimal value of 256 (that is, bit 8 is set).</span></span>

  - <span data-ttu-id="d4308-120">1100 (binário) tem um valor decimal de 12 (ou seja, os bits 2 e 3 são definidos; as propriedades representadas por ambos os bits são habilitadas).</span><span class="sxs-lookup"><span data-stu-id="d4308-120">1100 (binary) has a decimal value of 12 (that is, bits 2 and 3 are set; properties represented by both bits are enabled).</span></span>

  - <span data-ttu-id="d4308-121">1111000001 (binário) tem um valor decimal de 961 (ou seja, bits 0, 6, 7, 8 e 9 são definidos; as propriedades de cada um desses bits são habilitadas).</span><span class="sxs-lookup"><span data-stu-id="d4308-121">1111000001 (binary) has a decimal value of 961 (that is, bits 0, 6, 7, 8, and 9 are set; properties for each of these bits are enabled).</span></span>

<div id="sectionSection0" class="section">

### <a name="schema-attributes-for-lync-server-2013"></a><span data-ttu-id="d4308-122">Atributos de esquema do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4308-122">Schema Attributes for Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4308-123">Atributo</span><span class="sxs-lookup"><span data-stu-id="d4308-123">Attribute</span></span></th>
<th><span data-ttu-id="d4308-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4308-124">Description</span></span></th>
<th><span data-ttu-id="d4308-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4308-125">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4308-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="d4308-126">dnsHostName</span></span></p></td>
<td><p><span data-ttu-id="d4308-127">Um atributo existente nos serviços de domínio Active Directory que agora está associado às classes <strong>msRTCSIP-pool</strong> e <strong>msRTCSIP-MonitoringServer</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4308-127">An existing attribute in Active Directory Domain Services that is now associated with the <strong>msRTCSIP-Pool</strong> and <strong>msRTCSIP-MonitoringServer</strong> classes.</span></span> <span data-ttu-id="d4308-128">Esse atributo especifica o nome de domínio totalmente qualificado (FQDN) de um pool ou um servidor de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d4308-128">This attribute specifies the fully qualified domain name (FQDN) of a pool or Monitoring Server.</span></span></p>
<p><span data-ttu-id="d4308-129">Um valor válido para cada segmento é de 63 caracteres; um valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-129">A valid value for each segment is 63 characters; a valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="d4308-130">Novo no Microsoft Office Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-130">New in Microsoft Office Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-131">msDS-SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="d4308-131">msDS-SourceObjectDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-132">Esse atributo contém a representação de cadeia de caracteres do nome diferenciado (DN) do objeto em outra floresta que corresponde a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="d4308-132">This attribute contains the string representation of the distinguished name (DN) of the object in another forest that corresponds to this object.</span></span> <span data-ttu-id="d4308-133">Esse atributo é usado para expansão do grupo de distribuição e atendimento automático.</span><span class="sxs-lookup"><span data-stu-id="d4308-133">This attribute is used for distribution group expansion and auto attendance.</span></span> <span data-ttu-id="d4308-134">Esse atributo é definido no esquema padrão do Active Directory para Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-134">This attribute is defined in the default Active Directory schema for Windows Server 2003 R2.</span></span></p>
<p><span data-ttu-id="d4308-135">Para evitar a necessidade de uma atualização do AD DS para o Windows Server 2003 R2, a preparação do esquema do Active Directory estende o esquema do Windows Server 2003 com essa definição de atributo.</span><span class="sxs-lookup"><span data-stu-id="d4308-135">To avoid requiring an upgrade of AD DS to Windows Server 2003 R2, Active Directory schema preparation extends the Windows Server 2003 schema with this attribute definition.</span></span></p></td>
<td><p><span data-ttu-id="d4308-136">Novo no Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-136">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-137">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="d4308-137">msExchUCVoiceMailSettings</span></span></p></td>
<td><p><span data-ttu-id="d4308-138">Esse atributo com vários valores contém as configurações da caixa postal.</span><span class="sxs-lookup"><span data-stu-id="d4308-138">This multi-valued attribute holds voice mail settings.</span></span> <span data-ttu-id="d4308-139">Esse atributo é compartilhado com o Exchange Unified Messaging (UM).</span><span class="sxs-lookup"><span data-stu-id="d4308-139">This attribute is shared with Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="d4308-140">Novo no Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-140">New in Microsoft Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-141">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="d4308-141">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="d4308-142">Esse atributo de vários valores contém identificadores para políticas de retenção que se aplicam ao usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-142">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="d4308-143">As políticas de retenção preservam os itens da caixa de correio para o usuário durante o período de espera.</span><span class="sxs-lookup"><span data-stu-id="d4308-143">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="d4308-144">Esse atributo é compartilhado com o Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="d4308-144">This attribute is shared with Exchange 2013.</span></span></p></td>
<td><p><span data-ttu-id="d4308-145">Novo no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d4308-145">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-146">msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="d4308-146">msRTCSIP-AcpInfo</span></span></p></td>
<td><p><span data-ttu-id="d4308-147">Esse atributo armazena informações do provedor de audioconferência de áudio para um usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-147">This attribute stores audio conferencing provider information for a user.</span></span></p></td>
<td><p><span data-ttu-id="d4308-148">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-148">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-149">msRTCSIP-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="d4308-149">msRTCSIP-ApplicationDestination</span></span></p></td>
<td><p><span data-ttu-id="d4308-150">Esse atributo aponta para a entrada de serviço confiável do contato do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4308-150">This attribute points to the trusted service entry for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="d4308-151">Novo no Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-151">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-152">msRTCSIP-Aplicativolist</span><span class="sxs-lookup"><span data-stu-id="d4308-152">msRTCSIP-ApplicationList</span></span></p></td>
<td><p><span data-ttu-id="d4308-153">Esse atributo contém uma lista de aplicativos hospedados no servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d4308-153">This attribute contains a list of hosted applications on the application server.</span></span></p></td>
<td><p><span data-ttu-id="d4308-154">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-154">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-155">msRTCSIP – ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="d4308-155">msRTCSIP-ApplicationOptions</span></span></p></td>
<td><p><span data-ttu-id="d4308-156">Esse atributo especifica as opções para o contato do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4308-156">This attribute specifies the options for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="d4308-157">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-157">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-158">msRTCSIP-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="d4308-158">msRTCSIP-ApplicationPrimaryLanguage</span></span></p></td>
<td><p><span data-ttu-id="d4308-159">Esse atributo contém o idioma principal para o contato do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4308-159">This attribute contains the primary language for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="d4308-160">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-160">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-161">msRTCSIP-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="d4308-161">msRTCSIP-ApplicationSecondaryLanguages</span></span></p></td>
<td><p><span data-ttu-id="d4308-162">Esse atributo Multiple Value contém os idiomas secundários para o contato do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4308-162">This multiple value attribute contains the secondary languages for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="d4308-163">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-163">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-164">msRTCSIP-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="d4308-164">msRTCSIP-ApplicationServerBL</span></span></p></td>
<td><p><span data-ttu-id="d4308-165">Esse atributo contém uma lista de servidores de aplicativos que pertencem a este pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-165">This attribute contains a list of application servers that belong to this pool.</span></span> <span data-ttu-id="d4308-166">O link encaminhamento correspondente a este atributo de link regressivo é <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-166">The corresponding forward link to this back link attribute is <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-167">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-167">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-168">msRTCSIP-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="d4308-168">msRTCSIP-ApplicationServerPoolLink</span></span></p></td>
<td><p><span data-ttu-id="d4308-169">Esse atributo aponta para o pool ao qual esse servidor de aplicativos pertence.</span><span class="sxs-lookup"><span data-stu-id="d4308-169">This attribute points to the pool to which this application server belongs.</span></span> <span data-ttu-id="d4308-170">Este é o link encaminhar.</span><span class="sxs-lookup"><span data-stu-id="d4308-170">This is the forward link.</span></span> <span data-ttu-id="d4308-171">O link regressivo correspondente é <strong>msRTCSIP-ApplicationServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-171">The corresponding backward link is <strong>msRTCSIP-ApplicationServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-172">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-172">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-173">msRTCSIP-ArchiveDefault (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-173">msRTCSIP-ArchiveDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-174">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-174">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-175">Obsoleto no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-175">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-176">msRTCSIP-ArchiveDefaultFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-176">msRTCSIP-ArchiveDefaultFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-177">Esse atributo especifica o padrão global dentro do limite da floresta para arquivar todas as comunicações do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-177">This attribute specifies the global default within the forest boundary for archiving all user communications.</span></span> <span data-ttu-id="d4308-178">Isso é imposto pela camada do agente de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="d4308-178">This is enforced by the archiving agent layer.</span></span> <span data-ttu-id="d4308-179">O intervalo de valores para esse atributo é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4308-179">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-180"><strong>True</strong>: arquivar todos os usuários</span><span class="sxs-lookup"><span data-stu-id="d4308-180"><strong>TRUE</strong>: Archive all users</span></span></p></li>
<li><p><span data-ttu-id="d4308-181"><strong>False</strong>: Não arquivar todos os usuários</span><span class="sxs-lookup"><span data-stu-id="d4308-181"><strong>FALSE</strong>: Do not archive all users</span></span></p></li>
</ul>
<p><span data-ttu-id="d4308-182">Esse atributo controla globalmente, dentro do limite da floresta, como as comunicações do usuário em uma rede interna são arquivadas.</span><span class="sxs-lookup"><span data-stu-id="d4308-182">This attribute globally controls, within the forest boundary, how user communications within an internal network are archived.</span></span></p>
<p><span data-ttu-id="d4308-183"><strong>Comportamento do Live Communications Server 2005 (agora desativado)</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-183"><strong>Live Communications Server 2005 behavior (now retired)</strong></span></span></p>
<p><span data-ttu-id="d4308-184">O intervalo de valores para esse atributo é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4308-184">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-185">0: arquivar o corpo da mensagem [bit 0]</span><span class="sxs-lookup"><span data-stu-id="d4308-185">0: Archive the message body [bit 0]</span></span></p></li>
<li><p><span data-ttu-id="d4308-186">1: Não arquivar o corpo da mensagem [bit 0]</span><span class="sxs-lookup"><span data-stu-id="d4308-186">1: Do not archive the message body [bit 0]</span></span></p></li>
</ul>
<p><span data-ttu-id="d4308-187"><strong>Comportamento do Office Communications Server 2007</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-187"><strong>Office Communications Server 2007 behavior</strong></span></span></p>
<p><span data-ttu-id="d4308-188">O intervalo de valores para esse atributo é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4308-188">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-189">0: ArchiveFederationDefaultWithoutBody (desativado)</span><span class="sxs-lookup"><span data-stu-id="d4308-189">0: ArchiveFederationDefaultWithoutBody (retired)</span></span></p></li>
<li><p><span data-ttu-id="d4308-190">1-2: ArchiveInternalCommunications</span><span class="sxs-lookup"><span data-stu-id="d4308-190">1-2: ArchiveInternalCommunications</span></span></p></li>
<li><p><span data-ttu-id="d4308-191">3-4: ArchiveFederatedCommunications</span><span class="sxs-lookup"><span data-stu-id="d4308-191">3-4: ArchiveFederatedCommunications</span></span></p></li>
<li><p><span data-ttu-id="d4308-192">5: RecordPresenceRegistrations</span><span class="sxs-lookup"><span data-stu-id="d4308-192">5: RecordPresenceRegistrations</span></span></p></li>
<li><p><span data-ttu-id="d4308-193">6: RecordIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="d4308-193">6: RecordIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="d4308-194">7: RecordGroupIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="d4308-194">7: RecordGroupIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="d4308-195">8: RecordFileTransferInstances</span><span class="sxs-lookup"><span data-stu-id="d4308-195">8: RecordFileTransferInstances</span></span></p></li>
<li><p><span data-ttu-id="d4308-196">9: RecordAudioCallDetails</span><span class="sxs-lookup"><span data-stu-id="d4308-196">9: RecordAudioCallDetails</span></span></p></li>
<li><p><span data-ttu-id="d4308-197">10: RecordVideoCallDetails</span><span class="sxs-lookup"><span data-stu-id="d4308-197">10: RecordVideoCallDetails</span></span></p></li>
<li><p><span data-ttu-id="d4308-198">11: RecordRemoteAssistanceCallDetails</span><span class="sxs-lookup"><span data-stu-id="d4308-198">11: RecordRemoteAssistanceCallDetails</span></span></p></li>
<li><p><span data-ttu-id="d4308-199">12: RecordApplicationSharingDetails</span><span class="sxs-lookup"><span data-stu-id="d4308-199">12: RecordApplicationSharingDetails</span></span></p></li>
<li><p><span data-ttu-id="d4308-200">13: RecordMeetingInstantiations</span><span class="sxs-lookup"><span data-stu-id="d4308-200">13: RecordMeetingInstantiations</span></span></p></li>
<li><p><span data-ttu-id="d4308-201">14: RecordMeetingJoins</span><span class="sxs-lookup"><span data-stu-id="d4308-201">14: RecordMeetingJoins</span></span></p></li>
<li><p><span data-ttu-id="d4308-202">15: RecordDataJoins</span><span class="sxs-lookup"><span data-stu-id="d4308-202">15: RecordDataJoins</span></span></p></li>
<li><p><span data-ttu-id="d4308-203">16: RecordAVJoins</span><span class="sxs-lookup"><span data-stu-id="d4308-203">16: RecordAVJoins</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-204">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-204">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-205">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-205">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-206">msRTCSIP-ArchiveFederationDefault (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-206">msRTCSIP-ArchiveFederationDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-207">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-207">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-208">Obsoleto no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-208">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-209">msRTCSIP-ArchiveFederationDefaultFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-210">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-210">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-211">Obsoleto no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-211">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-212">msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="d4308-212">msRTCSIP-ArchivingEnabled</span></span></p></td>
<td><p><span data-ttu-id="d4308-213">Esse atributo é um inteiro usado como um campo de bits para controlar se as comunicações de um único usuário devem ser arquivadas.</span><span class="sxs-lookup"><span data-stu-id="d4308-213">This attribute is an integer used as a bit field to control whether a single user’s communications are to be archived.</span></span> <span data-ttu-id="d4308-214">Esse controle é imposto pela camada do agente de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="d4308-214">This control is enforced by the archiving agent layer.</span></span> <span data-ttu-id="d4308-215">Ele está marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-215">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="d4308-216">O escopo desse atributo é específico para um único usuário ou contato.</span><span class="sxs-lookup"><span data-stu-id="d4308-216">The scope of this attribute is specific to a single user or contact.</span></span> <span data-ttu-id="d4308-217">Os valores válidos (e posições de bit associadas) do Lync Server são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-217">The valid values (and associated bit positions) in Lync Server are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-218">0: Não arquivar (nenhum conjunto de bits)</span><span class="sxs-lookup"><span data-stu-id="d4308-218">0: Do not archive (no bit set)</span></span></p></li>
<li><p><span data-ttu-id="d4308-219">1: desativado (posição do bit 0)</span><span class="sxs-lookup"><span data-stu-id="d4308-219">1: Retired (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="d4308-220">2: desativado (posição do bit 1)</span><span class="sxs-lookup"><span data-stu-id="d4308-220">2: Retired (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="d4308-221">4: Arquivar comunicações internas (posição do bit 2)</span><span class="sxs-lookup"><span data-stu-id="d4308-221">4: Archive internal communications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="d4308-222">8: Arquivar comunicações federadas (posição de bit 3)</span><span class="sxs-lookup"><span data-stu-id="d4308-222">8: Archive federated communications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="d4308-223">Os valores válidos anteriormente no Live Communications Server 2005 são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-223">Previously valid values in Live Communications Server 2005 are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-224">0: Use o valor padrão definido por <strong>msRTCSIP-ArchiveDefault</strong> e <strong>msRTCSIP-ArchiveFederation</strong> nesta ordem de precedência:</span><span class="sxs-lookup"><span data-stu-id="d4308-224">0:Use the default value defined by <strong>msRTCSIP-ArchiveDefault</strong> and <strong>msRTCSIP-ArchiveFederation</strong> in this order of precedence:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-225">1: arquivo morto</span><span class="sxs-lookup"><span data-stu-id="d4308-225">1: Archive</span></span></p></li>
<li><p><span data-ttu-id="d4308-226">2: Não arquivar</span><span class="sxs-lookup"><span data-stu-id="d4308-226">2: Do not archive</span></span></p></li>
<li><p><span data-ttu-id="d4308-227">3: arquivar sem o corpo da mensagem</span><span class="sxs-lookup"><span data-stu-id="d4308-227">3: Archive without the message body</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="d4308-228">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-228">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-229">msRTCSIP-ArchivingServerData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-229">msRTCSIP-ArchivingServerData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-230">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-230">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-231">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-231">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-232">msRTCSIP-ArchivingServerVersion (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-232">msRTCSIP-ArchivingServerVersion (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-233">Esse atributo define a versão do serviço de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="d4308-233">This attribute defines the version of the Archiving service.</span></span> <span data-ttu-id="d4308-234">Esse atributo é um tipo de inteiro que aumenta o monotonously que aumenta com cada lançamento oficial do produto.</span><span class="sxs-lookup"><span data-stu-id="d4308-234">This attribute is a monotonously increasing integer type that increments with each official product release.</span></span> <span data-ttu-id="d4308-235">Os valores válidos possíveis são:</span><span class="sxs-lookup"><span data-stu-id="d4308-235">The possible valid values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-236">Indefinido: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4308-236">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="d4308-237">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="d4308-237">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="d4308-238">Live Communications Server 2005 com SP1</span><span class="sxs-lookup"><span data-stu-id="d4308-238">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="d4308-239">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d4308-239">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="d4308-240">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d4308-240">4: Office Communications Server 2007 R2</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-241">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-241">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-242">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-243">msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="d4308-243">msRTCSIP-BackEndServer</span></span></p></td>
<td><p><span data-ttu-id="d4308-244">Esse atributo especifica o FQDN do servidor back-end do pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-244">This attribute specifies the FQDN of the Back End Server of the pool.</span></span> <span data-ttu-id="d4308-245">Como só pode haver um único servidor back-end por pool, esse é um atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="d4308-245">Because there can only be a single Back End Server per pool, this is a single-valued attribute.</span></span></p>
<p><span data-ttu-id="d4308-246">O valor válido para cada segmento é de 63 caracteres; o valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-246">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="d4308-247">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-247">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-248">msRTCSIP-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="d4308-248">msRTCSIP-ConferenceDirectoryHomePool</span></span></p></td>
<td><p><span data-ttu-id="d4308-249">Esse atributo contém o identificador do pool que hospeda o diretório de conferências.</span><span class="sxs-lookup"><span data-stu-id="d4308-249">This attribute contains the identifier of the pool that hosts the conference directory.</span></span></p></td>
<td><p><span data-ttu-id="d4308-250">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-250">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-251">msRTCSIP-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="d4308-251">msRTCSIP-ConferenceDirectoryId</span></span></p></td>
<td><p><span data-ttu-id="d4308-252">Esse atributo contém o identificador de um diretório de conferências.</span><span class="sxs-lookup"><span data-stu-id="d4308-252">This attribute contains the identifier of a conference directory.</span></span></p></td>
<td><p><span data-ttu-id="d4308-253">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-253">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-254">msRTCSIP-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="d4308-254">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p></td>
<td><p><span data-ttu-id="d4308-255">Esse atributo contém o identificador do pool ao qual o diretório de conferências está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="d4308-255">This attribute contains the identifier of the pool to which the conference directory is being moved.</span></span></p></td>
<td><p><span data-ttu-id="d4308-256">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-256">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-257">msRTCSIP-padrão</span><span class="sxs-lookup"><span data-stu-id="d4308-257">msRTCSIP-Default</span></span></p></td>
<td><p><span data-ttu-id="d4308-258">Esse atributo booliano define se o uso do telefone é um uso padrão.</span><span class="sxs-lookup"><span data-stu-id="d4308-258">This Boolean attribute defines whether the phone usage is a default usage.</span></span> <span data-ttu-id="d4308-259">Se esse atributo estiver definido como <strong>true</strong>, o uso do telefone será um uso padrão e não poderá ser excluído pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="d4308-259">If this attribute is set to <strong>TRUE</strong>, the phone usage is a default usage and cannot be deleted by the administrator.</span></span> <span data-ttu-id="d4308-260">Se esse atributo estiver definido como <strong>false</strong>, o uso poderá ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d4308-260">If this attribute is set to <strong>FALSE</strong>, the usage can be deleted.</span></span></p></td>
<td><p><span data-ttu-id="d4308-261">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-261">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-262">msRTCSIP-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="d4308-262">msRTCSIP-DefaultCWAExternalURL</span></span></p></td>
<td><p><span data-ttu-id="d4308-263">Esse atributo identifica a URL do Communicator Web Access para usuários que estão fora da organização.</span><span class="sxs-lookup"><span data-stu-id="d4308-263">This attribute identifies the Communicator Web Access URL for users who are outside the organization.</span></span></p></td>
<td><p><span data-ttu-id="d4308-264">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-264">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-265">msRTCSIP-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="d4308-265">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
<td><p><span data-ttu-id="d4308-266">Esse atributo identifica a URL do Communicator Web Access para os usuários que estão dentro da organização.</span><span class="sxs-lookup"><span data-stu-id="d4308-266">This attribute identifies the Communicator Web Access URL for users who are inside the organization.</span></span></p></td>
<td><p><span data-ttu-id="d4308-267">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-267">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-268">msRTCSIP-DefaultLocationProfileLink (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-268">msRTCSIP-DefaultLocationProfileLink (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-269">Esse atributo com valor único contém o nome diferenciado (DN) de um objeto de classe de perfil de localização atribuído a ele.</span><span class="sxs-lookup"><span data-stu-id="d4308-269">This single-valued attribute contains the distinguished name (DN) of a location profile class object assigned to it.</span></span></p>
<p><span data-ttu-id="d4308-270">Link encaminhar: <strong>ID do link 11036</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-270">Forward link: <strong>Link ID 11036</strong></span></span></p>
<p><span data-ttu-id="d4308-271">O link regressivo correspondente é <strong>msRTCSIP-ServerReferenceBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-271">The corresponding backward link is <strong>msRTCSIP-ServerReferenceBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-272">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-272">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-273">msRTCSIP-DefaultPolicy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-273">msRTCSIP-DefaultPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-274">Esse atributo booliano especifica se a política é uma política padrão.</span><span class="sxs-lookup"><span data-stu-id="d4308-274">This Boolean attribute specifies whether the policy is a default policy.</span></span> <span data-ttu-id="d4308-275">A política é uma política padrão quando definida como <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-275">The policy is a default policy when set to <strong>TRUE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-276">Novo no Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d4308-276">New in Office Communications Server 2007</span></span></p>
<p><span data-ttu-id="d4308-277">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-277">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-278">msRTCSIP-DefaultRouteToEdgeProxy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-279">Esse atributo especifica o FQDN do servidor de borda que executa o serviço de borda de acesso, se ele puder ser acessado diretamente ou do balanceador de carga de hardware para um pool de servidores que executam o serviço de borda de acesso.</span><span class="sxs-lookup"><span data-stu-id="d4308-279">This attribute specifies the FQDN of either the Edge Server running the Access Edge service, if it can be accessed directly, or of the hardware load balancer for a pool of servers running Access Edge service.</span></span> <span data-ttu-id="d4308-280">Se os servidores que executam o serviço de borda de acesso só puderem ser acessados por meio de um ou mais directors, esse atributo especificará o FQDN e, opcionalmente, o número da porta do diretor ou do balanceador de carga de hardware que serve um pool de directors.</span><span class="sxs-lookup"><span data-stu-id="d4308-280">If the servers running Access Edge service can be accessed only through one or more Directors, this attribute specifies the FQDN and, optionally, the port number of the Director or of the hardware load balancer serving a Director pool.</span></span></p>
<p><span data-ttu-id="d4308-281">O valor válido para cada segmento é de 63 caracteres; o valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-281">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="d4308-282">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-282">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-283">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-283">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-285">Esse atributo representa o número da porta que deve ser usado para conexão com o serviço de borda de acesso do servidor que está executando.</span><span class="sxs-lookup"><span data-stu-id="d4308-285">This attribute represents the port number that should be used to connect to the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="d4308-286">O valor válido é um valor inteiro que especifica a porta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d4308-286">The valid value is an integer value specifying the port to be used.</span></span> <span data-ttu-id="d4308-287">O valor padrão é 5061.</span><span class="sxs-lookup"><span data-stu-id="d4308-287">The default value is 5061.</span></span></p></td>
<td><p><span data-ttu-id="d4308-288">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-288">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-289">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-289">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-291">Esse atributo representa o período de tempo limite da assinatura de presença padrão.</span><span class="sxs-lookup"><span data-stu-id="d4308-291">This attribute represents the default presence subscription time-out period.</span></span></p></td>
<td><p><span data-ttu-id="d4308-292">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-292">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-293">msRTCSIP-DefRegistrationTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-293">msRTCSIP-DefRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-294">Esse atributo representa a janela de tempo limite de registro padrão.</span><span class="sxs-lookup"><span data-stu-id="d4308-294">This attribute represents the default registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-295">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-295">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-297">Esse atributo representa a janela de tempo limite de assinatura de dados de roaming padrão.</span><span class="sxs-lookup"><span data-stu-id="d4308-297">This attribute represents the default roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-298">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-298">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-299">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="d4308-299">msRTCSIP-DeploymentLocator</span></span></p></td>
<td><p><span data-ttu-id="d4308-300">Esse atributo é usado em uma topologia de domínio dividido e contém um FQDN (nome de domínio totalmente qualificado).</span><span class="sxs-lookup"><span data-stu-id="d4308-300">This attribute is used in a split domain topology and contains a fully qualified domain name (FQDN).</span></span></p></td>
<td><p><span data-ttu-id="d4308-301">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-301">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-302">msRTCSIP-Descrição (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-302">msRTCSIP-Description (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-303">Este atributo de cadeia de caracteres UNICODE com valor único contém uma descrição amigável da regra de normalização ou rota telefônica.</span><span class="sxs-lookup"><span data-stu-id="d4308-303">This single-valued UNICODE string attribute contains a friendly description of this phone route or normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="d4308-304">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-304">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-305">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-305">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-306">msRTCSIP-DomainData</span><span class="sxs-lookup"><span data-stu-id="d4308-306">msRTCSIP-DomainData</span></span></p></td>
<td><p><span data-ttu-id="d4308-307">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-307">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-308">msRTCSIP-DomainName</span><span class="sxs-lookup"><span data-stu-id="d4308-308">msRTCSIP-DomainName</span></span></p></td>
<td><p><span data-ttu-id="d4308-309">Esse atributo representa um domínio configurado para o registrador.</span><span class="sxs-lookup"><span data-stu-id="d4308-309">This attribute represents a domain configured for the Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-310">msRTCSIP-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="d4308-310">msRTCSIP-EdgeProxyData</span></span></p></td>
<td><p><span data-ttu-id="d4308-311">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-311">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-312">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-312">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-313">msRTCSIP-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="d4308-313">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-314">Esse atributo especifica o FQDN do serviço de borda de acesso do servidor que está executando.</span><span class="sxs-lookup"><span data-stu-id="d4308-314">This attribute specifies the FQDN of the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="d4308-315">O valor válido para cada segmento é de 63 caracteres; o valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-315">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="d4308-316">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-316">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-317">msRTCSIP-EnableBestEffortNotify (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-317">msRTCSIP-EnableBestEffortNotify (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-318">Esse atributo controla se um servidor gera uma solicitação de notificação de melhor esforço (enviar notificação), em vez de uma solicitação de notificação, em resposta a uma solicitação de assinatura de um cliente.</span><span class="sxs-lookup"><span data-stu-id="d4308-318">This attribute controls whether a server generates a Best Effort NOTIFY (BENOTIFY) request, instead of a NOTIFY request, in response to a SUBSCRIBE request from a client.</span></span> <span data-ttu-id="d4308-319">Mynotify é uma extensão de aprimoramento do desempenho para o handshake de notificação de assinatura em que o servidor gera solicitações de notificação de notificação, em vez de solicitações regulares de notificação.</span><span class="sxs-lookup"><span data-stu-id="d4308-319">BENOTIFY is a performance-enhancing extension to the subscribe notification handshake where the server generates BENOTIFY requests, instead of regular NOTIFY requests.</span></span> <span data-ttu-id="d4308-320">O benefício do desempenho é que uma solicitação de notificação não requer uma resposta de 200 OK do cliente, pois a solicitação de notificação faz.</span><span class="sxs-lookup"><span data-stu-id="d4308-320">The performance benefit is that a BENOTIFY request does not require a 200 OK response from the client as the NOTIFY request does.</span></span></p>
<p><span data-ttu-id="d4308-321">Os valores válidos são <strong>true</strong> ou <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-321">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="d4308-322">O Live Communications Server 2003 não oferece suporte a solicitações de notificação de notificação.</span><span class="sxs-lookup"><span data-stu-id="d4308-322">Live Communications Server 2003 does not support BENOTIFY requests.</span></span> <span data-ttu-id="d4308-323">Para interoperar com os aplicativos do servidor escritos com a API do servidor do Live Communications Server 2003 em execução no Live Communications Server 2005 e em servidores de terceiros, as solicitações de notificação podem ser desabilitadas definindo seu valor como <STRONG>false</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d4308-323">To interoperate with server applications written with the Live Communications Server 2003 server API running on Live Communications Server 2005 and third-party servers, BENOTIFY requests can be disabled by setting its value to <STRONG>FALSE</STRONG>.</span></span> <span data-ttu-id="d4308-324">Mynotify não faz parte do processo de padronização SIP do IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="d4308-324">BENOTIFY is not currently part of the IETF (Internet Engineering Task Force) SIP standardization process.</span></span>


</div></td>
<td><p><span data-ttu-id="d4308-325">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-325">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-326">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-326">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-327">msRTCSIP-EnableFederation (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-327">msRTCSIP-EnableFederation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-328">Esse atributo é uma opção global que os administradores de ti usam para configurar se os usuários têm permissão para se comunicar com usuários de outras organizações.</span><span class="sxs-lookup"><span data-stu-id="d4308-328">This attribute is a global switch that IT administrators use to configure whether users are allowed to communicate with users from other organizations.</span></span> <span data-ttu-id="d4308-329">Ele permite que um administrador substitua o atributo <strong>FederationEnabled</strong> de um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="d4308-329">It enables an administrator to overwrite an individual user’s <strong>FederationEnabled</strong> attribute.</span></span> <span data-ttu-id="d4308-330">Esse atributo pode ser útil para ajudar a proteger a rede interna de ataques pela Internet que podem ser causados por worms, vírus ou ataques direcionados à empresa.</span><span class="sxs-lookup"><span data-stu-id="d4308-330">This attribute can be useful to help protect the internal network from Internet attacks that may be caused by worms, viruses, or targeted attacks on the company.</span></span></p>
<p><span data-ttu-id="d4308-331">Os valores válidos (e posições de bit associadas) são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-331">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-332">1: habilitado para conectividade de IM pública (posição do bit 0)</span><span class="sxs-lookup"><span data-stu-id="d4308-332">1: Enabled for public IM connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="d4308-333">2: reservado (posição do bit 1)</span><span class="sxs-lookup"><span data-stu-id="d4308-333">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="d4308-334">4: reservado (posição do bit 2)</span><span class="sxs-lookup"><span data-stu-id="d4308-334">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="d4308-335">8: reservado (posição do bit 3)</span><span class="sxs-lookup"><span data-stu-id="d4308-335">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="d4308-336">16: controle de chamada remota habilitado [telefonia] (posição de bit 4)</span><span class="sxs-lookup"><span data-stu-id="d4308-336">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="d4308-337">64: AllowOrganizeMeetingWithAnonymousParticipants (permite que os usuários convidem usuários anônimos para reuniões (posição de bit 6)</span><span class="sxs-lookup"><span data-stu-id="d4308-337">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="d4308-338">128: UCEnabled (habilitar usuários para comunicação unificada) (posição de bit 7)</span><span class="sxs-lookup"><span data-stu-id="d4308-338">128: UCEnabled (enable users for unified communications) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="d4308-339">256: EnabledForEnhancedPresence (habilitar usuário para conectividade de IM pública) (posição de bit 8)</span><span class="sxs-lookup"><span data-stu-id="d4308-339">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="d4308-340">512: RemoteCallControlDualMode (posição do bit 9)</span><span class="sxs-lookup"><span data-stu-id="d4308-340">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-341">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-341">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-342">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-342">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-343">msRTCSIP-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="d4308-343">msRTCSIP-EnterpriseServices</span></span></p></td>
<td><p><span data-ttu-id="d4308-344">Esse atributo indica se os serviços corporativos são carregados em determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="d4308-344">This attribute indicates whether the Enterprise Services are loaded on the given server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-345">msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="d4308-345">msRTCSIP-ExtensionData</span></span></p></td>
<td><p><span data-ttu-id="d4308-346">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-346">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-347">msRTCSIP-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="d4308-347">msRTCSIP-ExternalAccessCode</span></span></p></td>
<td><p><span data-ttu-id="d4308-348">Esse atributo contém o código de discagem para acesso externo.</span><span class="sxs-lookup"><span data-stu-id="d4308-348">This attribute contains the dial code for external access.</span></span></p></td>
<td><p><span data-ttu-id="d4308-349">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-349">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-350">msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="d4308-350">msRTCSIP-FederationEnabled</span></span></p></td>
<td><p><span data-ttu-id="d4308-351">Esse atributo controla se um único usuário está habilitado para Federação.</span><span class="sxs-lookup"><span data-stu-id="d4308-351">This attribute controls whether a single user is enabled for federation.</span></span> <span data-ttu-id="d4308-352">Ela é imposta pela camada de serviços corporativos.</span><span class="sxs-lookup"><span data-stu-id="d4308-352">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="d4308-353">Ele está marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-353">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="d4308-354">Os valores válidos são <strong>true</strong> ou <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-354">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-355">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-355">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-356">msRTCSIP-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="d4308-356">msRTCSIP-FrontEndServers</span></span></p></td>
<td><p><span data-ttu-id="d4308-357">Esse atributo é uma lista de vários valores dos nomes de domínio de todos os servidores Enterprise Edition associados a um pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-357">This attribute is a multi-valued list of the domain names of all Enterprise Edition servers associated with a pool.</span></span></p>
<p><span data-ttu-id="d4308-358">Link para trás: <strong>ID do link 11023</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-358">Back link: <strong>Link ID 11023</strong></span></span></p>
<p><span data-ttu-id="d4308-359">O link encaminhamento correspondente para esse link regressivo é <strong>msRTCSIP-PoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-359">The corresponding forward link to this back link is <strong>msRTCSIP-PoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-360">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-360">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-361">msRTCSIP-gateways (obsoletos)</span><span class="sxs-lookup"><span data-stu-id="d4308-361">msRTCSIP-Gateways (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-362">Este atributo de cadeia de caracteres de múltiplos valores contém uma lista de gateways e portas (por gateway).</span><span class="sxs-lookup"><span data-stu-id="d4308-362">This multi-valued string attribute contains a list of gateways and ports (per gateway).</span></span></p></td>
<td><p><span data-ttu-id="d4308-363">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-363">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-364">msRTCSIP-GlobalSettingsData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-364">msRTCSIP-GlobalSettingsData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-365">Esse atributo armazena nomes de valor: pares de valores.</span><span class="sxs-lookup"><span data-stu-id="d4308-365">This attribute stores name:value pairs.</span></span> <span data-ttu-id="d4308-366">O par de nomes já definido: é para a configuração <strong>permitir sondagem para presença</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4308-366">The already-defined name:value pair is for the <strong>allow polling for presence</strong> setting.</span></span></p></td>
<td><p><span data-ttu-id="d4308-367">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-367">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-368">msRTCSIP-Groupingid</span><span class="sxs-lookup"><span data-stu-id="d4308-368">msRTCSIP-GroupingID</span></span></p></td>
<td><p><span data-ttu-id="d4308-369">Esse atributo é um identificador exclusivo de um grupo usado para agrupar entradas do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="d4308-369">This attribute is a unique identifier of a group that is used to group address book entries.</span></span></p></td>
<td><p><span data-ttu-id="d4308-370">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-370">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-371">msRTCSIP-HomeServer (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-371">msRTCSIP-HomeServer (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-372">Novo no Live Communications Server 2003 (não usado).</span><span class="sxs-lookup"><span data-stu-id="d4308-372">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="d4308-373">Obsoleto no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-373">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-374">msRTCSIP-HomeServerString (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-374">msRTCSIP-HomeServerString (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-375">Novo no Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d4308-375">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="d4308-376">Obsoleto no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-376">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-377">msRTCSIP-HomeUsers (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-377">msRTCSIP-HomeUsers (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-378">Novo no Live Communications Server 2003 (não usado).</span><span class="sxs-lookup"><span data-stu-id="d4308-378">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="d4308-379">Obsoleto no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-379">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-380">msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="d4308-380">msRTCSIP-InternetAccessEnabled</span></span></p></td>
<td><p><span data-ttu-id="d4308-381">Esse atributo controla se um único usuário está habilitado para o acesso de usuário externo.</span><span class="sxs-lookup"><span data-stu-id="d4308-381">This attribute controls whether a single user is enabled for outside user access.</span></span> <span data-ttu-id="d4308-382">Ela é imposta pela camada de serviços corporativos.</span><span class="sxs-lookup"><span data-stu-id="d4308-382">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="d4308-383">Ele está marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-383">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="d4308-384">Os valores válidos são <strong>true</strong> ou <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-384">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-385">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-385">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-386">msRTCSIP-IsMaster (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-386">msRTCSIP-IsMaster (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-387">Novo no Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4308-387">New in Live Communications Server 2003</span></span></p>
<p><span data-ttu-id="d4308-388">Obsoleto no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-388">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-389">Linha de msRTCSIP</span><span class="sxs-lookup"><span data-stu-id="d4308-389">msRTCSIP-Line</span></span></p></td>
<td><p><span data-ttu-id="d4308-390">Esse atributo com valor único contém a ID do dispositivo (o URI SIP ou o URI do TEL do telefone que o usuário controla) usado pelo Lync para telefonia.</span><span class="sxs-lookup"><span data-stu-id="d4308-390">This single-valued attribute contains the device ID (either the SIP URI or the TEL URI of the phone the user controls) used by Lync for telephony.</span></span> <span data-ttu-id="d4308-391">Esse atributo está marcado para replicação de catálogo global e está indexado.</span><span class="sxs-lookup"><span data-stu-id="d4308-391">This attribute is marked for Global Catalog replication and is indexed.</span></span> <span data-ttu-id="d4308-392">Se um usuário estiver habilitado para o Enterprise Voice, esse atributo armazenará a versão normalizada E. 164 do número de telefone do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-392">If a user is enabled for Enterprise Voice, this attribute stores the E.164 normalized version of the user’s phone number.</span></span></p></td>
<td><p><span data-ttu-id="d4308-393">Novo no Microsoft Office Live Communications Server 2005 com SP1</span><span class="sxs-lookup"><span data-stu-id="d4308-393">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-394">msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="d4308-394">msRTCSIP-LineServer</span></span></p></td>
<td><p><span data-ttu-id="d4308-395">Esse atributo com valor único contém o URI SIP do servidor do gateway CSTA-SIP.</span><span class="sxs-lookup"><span data-stu-id="d4308-395">This single-valued attribute contains the SIP URI of the CSTA-SIP gateway server.</span></span> <span data-ttu-id="d4308-396">Esse atributo está marcado para replicação de catálogo global, mas não está indexado.</span><span class="sxs-lookup"><span data-stu-id="d4308-396">This attribute is marked for Global Catalog replication but is not indexed.</span></span></p></td>
<td><p><span data-ttu-id="d4308-397">Novo no Microsoft Office Live Communications Server 2005 com SP1</span><span class="sxs-lookup"><span data-stu-id="d4308-397">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-398">msRTCSIP-LocalNormalizationData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-398">msRTCSIP-LocalNormalizationData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-399">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-399">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-400">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-400">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-401">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-401">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-402">msRTCSIP-LocalNormalizationLinks (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-402">msRTCSIP-LocalNormalizationLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-403">Este atributo de valores múltiplos contém uma lista de nomes diferenciais de normalização (DN) locais associados a este perfil de local.</span><span class="sxs-lookup"><span data-stu-id="d4308-403">This multi-valued attribute contains a list of local normalization distinguished names (DN) associated with this location profile.</span></span> <span data-ttu-id="d4308-404">O tipo desse atributo é um binário DN.</span><span class="sxs-lookup"><span data-stu-id="d4308-404">The type of this attribute is a DN binary.</span></span> <span data-ttu-id="d4308-405">Há uma relação um-para-muitos entre o perfil de local e as regras de normalização locais.</span><span class="sxs-lookup"><span data-stu-id="d4308-405">There is a one-to-many relationship between location profile and local normalization rules.</span></span> <span data-ttu-id="d4308-406">A ordenação da lista de DNs de normalização local deve ser mantida na ordem especificada pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="d4308-406">The ordering of the list of local normalization DNs must be maintained in the order specified by the administrator.</span></span> <span data-ttu-id="d4308-407">A preservação do pedido é mantida pela parte binária do binário DN, que especifica o índice do pedido.</span><span class="sxs-lookup"><span data-stu-id="d4308-407">The preservation of order is maintained by the binary portion of the DN binary, which specifies the order index.</span></span></p>
<p><span data-ttu-id="d4308-408">Link encaminhar: <strong>ID do link 11034</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-408">Forward link: <strong>Link ID 11034</strong></span></span></p>
<p><span data-ttu-id="d4308-409">O link regressivo correspondente a este atributo de link de encaminhamento é <strong>msRTCSIP-LocationProfileBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-409">The corresponding back link to this forward link attribute is <strong>msRTCSIP-LocationProfileBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-410">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-410">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-411">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-411">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-412">msRTCSIP-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="d4308-412">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
<td><p><span data-ttu-id="d4308-413">Esse atributo contém uma lista de opções para a regra de normalização.</span><span class="sxs-lookup"><span data-stu-id="d4308-413">This attribute contains a list of options for the normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="d4308-414">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-414">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-415">msRTCSIP-LocationName (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-415">msRTCSIP-LocationName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-416">Esse atributo com valor único contém um nome amigável para o perfil de local que indica qual local esse perfil representa.</span><span class="sxs-lookup"><span data-stu-id="d4308-416">This single-valued attribute contains a friendly name for the location profile that indicates which location this profile represents.</span></span> <span data-ttu-id="d4308-417">Como pode haver vários perfis de localização, o administrador precisa de uma maneira de distinguir entre diferentes perfis.</span><span class="sxs-lookup"><span data-stu-id="d4308-417">Because there can be multiple location profiles, the administrator needs a way to distinguish between different profiles.</span></span></p></td>
<td><p><span data-ttu-id="d4308-418">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-418">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-419">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-419">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-420">msRTCSIP-locationProfileBL (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-420">msRTCSIP-locationProfileBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-421">Esse atributo com valores múltiplos contém uma lista de nomes distintos do perfil de local.</span><span class="sxs-lookup"><span data-stu-id="d4308-421">This multi-valued attribute contains a list of location profile distinguished names.</span></span> <span data-ttu-id="d4308-422">Esse atributo especifica o link back para um ou mais perfis de local.</span><span class="sxs-lookup"><span data-stu-id="d4308-422">This attribute specifies the back link to one or more location profiles.</span></span></p>
<p><span data-ttu-id="d4308-423">Link para trás: <strong>ID do link 11035</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-423">Back link: <strong>Link ID 11035</strong></span></span></p>
<p><span data-ttu-id="d4308-424">Esse atributo corresponde ao link Forward <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-424">This attribute corresponds to the forward link <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-425">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-425">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-426">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-426">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-427">msRTCSIP-LocationProfileData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-427">msRTCSIP-LocationProfileData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-428">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-428">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-429">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-429">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-430">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-430">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-431">msRTCSIP-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="d4308-431">msRTCSIP-LocationProfileOptions</span></span></p></td>
<td><p><span data-ttu-id="d4308-432">Esse atributo contém as opções do perfil de local.</span><span class="sxs-lookup"><span data-stu-id="d4308-432">This attribute contains the options for the location profile.</span></span></p></td>
<td><p><span data-ttu-id="d4308-433">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-433">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-434">msRTCSIP-MappingContact</span><span class="sxs-lookup"><span data-stu-id="d4308-434">msRTCSIP-MappingContact</span></span></p></td>
<td><p><span data-ttu-id="d4308-435">Este atributo de vários valores contém uma lista de contatos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4308-435">This multiple-value attribute holds a list of application contacts.</span></span></p></td>
<td><p><span data-ttu-id="d4308-436">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-436">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-437">msRTCSIP-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="d4308-437">msRTCSIP-MappingLocation</span></span></p></td>
<td><p><span data-ttu-id="d4308-438">Esse atributo de vários valores contém uma lista de perfis de localização.</span><span class="sxs-lookup"><span data-stu-id="d4308-438">This multiple-value attribute holds a list of location profiles.</span></span></p></td>
<td><p><span data-ttu-id="d4308-439">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-439">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-441">Esse atributo representa o número máximo de solicitações de pesquisa pendentes por servidor.</span><span class="sxs-lookup"><span data-stu-id="d4308-441">This attribute represents the maximum number of outstanding search requests per server.</span></span></p></td>
<td><p><span data-ttu-id="d4308-442">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-442">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-444">O atributo representa o número máximo de assinaturas por usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-444">The attribute represents the maximum number of subscriptions per user.</span></span></p></td>
<td><p><span data-ttu-id="d4308-445">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-445">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-447">Esse atributo representa a janela de tempo limite máximo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4308-447">This attribute represents the maximum subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-448">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-448">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-449">msRTCSIP-MaxRegistrationsTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-449">msRTCSIP-MaxRegistrationsTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-450">Esse atributo representa a janela de tempo limite de registros máximos.</span><span class="sxs-lookup"><span data-stu-id="d4308-450">This attribute represents the maximum registrations time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-451">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-451">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-453">Esse atributo representa a janela de tempo limite de máximo de assinaturas de roaming de dados.</span><span class="sxs-lookup"><span data-stu-id="d4308-453">This attribute represents the maximum roaming data subscriptions time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-454">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-454">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-455">msRTCSIP-MCUData</span><span class="sxs-lookup"><span data-stu-id="d4308-455">msRTCSIP-MCUData</span></span></p></td>
<td><p><span data-ttu-id="d4308-456">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-456">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-457">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-457">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-458">msRTCSIP-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="d4308-458">msRTCSIP-MCUFactoryAddress</span></span></p></td>
<td><p><span data-ttu-id="d4308-459">Esse atributo é um atributo de ponto de controle de serviço na classe Computer que especifica um link de volta para a fábrica da unidade de controle multiponto (MCU) à qual ele pertence.</span><span class="sxs-lookup"><span data-stu-id="d4308-459">This attribute is a service control point attribute under the computer class that specifies a link back to the multipoint control unit (MCU) Factory to which it belongs.</span></span> <span data-ttu-id="d4308-460">Esse atributo e este ponto de controle de serviço é criado para cada Microsoft MCU.</span><span class="sxs-lookup"><span data-stu-id="d4308-460">This service control point and attribute is created for every Microsoft MCU.</span></span> <span data-ttu-id="d4308-461">Cada Microsoft MCU deve encontrar o servidor back-end do pool ao qual ele pertence, para recuperar as configurações no nível do pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-461">Each Microsoft MCU must find the Back End Server of the pool to which it belongs, in order to retrieve pool-level settings from it.</span></span></p>
<p><span data-ttu-id="d4308-462">O valor desse atributo é o nome diferenciado (DN) da fábrica do MCU.</span><span class="sxs-lookup"><span data-stu-id="d4308-462">The value of this attribute is the distinguished name (DN) of the MCU Factory.</span></span> <span data-ttu-id="d4308-463">Esse é um atributo de valor único e marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-463">This is a single-valued attribute and marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="d4308-464">Link encaminhar: <strong>ID do link 11026</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-464">Forward link: <strong>Link ID 11026</strong></span></span></p>
<p><span data-ttu-id="d4308-465">O link regressivo correspondente a este atributo de link de encaminhamento é <strong>msRTCSIP-MCUServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-465">The corresponding back link to this forward link attribute is <strong>msRTCSIP-MCUServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-466">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-466">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-467">msRTCSIP-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="d4308-467">msRTCSIP-MCUFactoryData</span></span></p></td>
<td><p><span data-ttu-id="d4308-468">Este é um atributo reservado de várias cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-468">This is a multi-string reserved attribute.</span></span> <span data-ttu-id="d4308-469">As configurações armazenadas nesse atributo são representadas como pares nome = valor.</span><span class="sxs-lookup"><span data-stu-id="d4308-469">Settings stored in this attribute are represented as name=value pairs.</span></span> <span data-ttu-id="d4308-470">Pares nome = valor atualmente definidos são:</span><span class="sxs-lookup"><span data-stu-id="d4308-470">Currently defined name=value pairs are:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-471">FactoryURL = &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="d4308-471">FactoryURL = &lt;URL&gt;</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-472">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-472">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-473">msRTCSIP-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="d4308-473">msRTCSIP-MCUFactoryPath</span></span></p></td>
<td><p><span data-ttu-id="d4308-474">Esse é um atributo de valor único que contém o nome diferenciado (DN) de uma única fábrica de MCU associada a um pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-474">This is a single-valued attribute that contains the distinguished name (DN) of a single MCU factory associated with a pool.</span></span></p>
<p><span data-ttu-id="d4308-475">Link encaminhar: <strong>ID do link 11024</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-475">Forward link: <strong>Link ID 11024</strong></span></span></p>
<p><span data-ttu-id="d4308-476">O link regressivo correspondente a este atributo de link de encaminhamento é <strong>msRTCSIP-PoolAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-476">The corresponding back link to this forward link attribute is <strong>msRTCSIP-PoolAddresses</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-477">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-477">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-478">msRTCSIP-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="d4308-478">msRTCSIP-MCUFactoryProviderID</span></span></p></td>
<td><p><span data-ttu-id="d4308-479">Esse atributo é uma cadeia de caracteres com valor único que especifica o GUID do provedor de fábrica MCU.</span><span class="sxs-lookup"><span data-stu-id="d4308-479">This attribute is a single-valued string that specifies the GUID of the MCU factory provider.</span></span> <span data-ttu-id="d4308-480">Com base no valor GUID, o processo de fábrica do MCU determina se o tipo de MCU deve ser atendido.</span><span class="sxs-lookup"><span data-stu-id="d4308-480">Based on the GUID value, the MCU factory process determines whether to service this MCU type.</span></span> <span data-ttu-id="d4308-481">Se o valor GUID for <strong>{F0810510-424F-46ef-84fe-6CC720DF1791}</strong>, o processo de fábrica do MCU (disponível por padrão no Lync Server) o processará.</span><span class="sxs-lookup"><span data-stu-id="d4308-481">If the GUID value is <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, then the MCU factory process (available by default in Lync Server) will process it.</span></span> <span data-ttu-id="d4308-482">Para qualquer outro valor de GUID, o processo de fábrica da MCU não irá atender ao tipo de MCU.</span><span class="sxs-lookup"><span data-stu-id="d4308-482">For any other GUID value, the MCU factory process will not service the MCU type.</span></span></p></td>
<td><p><span data-ttu-id="d4308-483">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-483">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-484">msRTCSIP-MCUServers</span><span class="sxs-lookup"><span data-stu-id="d4308-484">msRTCSIP-MCUServers</span></span></p></td>
<td><p><span data-ttu-id="d4308-485">Esse atributo é uma lista com vários valores de nomes diferenciados (DN).</span><span class="sxs-lookup"><span data-stu-id="d4308-485">This attribute is a multi-valued list of distinguished names (DN).</span></span> <span data-ttu-id="d4308-486">Esse atributo contém uma lista de todos os servidores MCU do mesmo tipo e fornecedor associados a essa fábrica de MCU.</span><span class="sxs-lookup"><span data-stu-id="d4308-486">This attribute contains a list of all MCU servers of the same type and vendor associated with this MCU factory.</span></span> <span data-ttu-id="d4308-487">O valor válido para cada segmento é de 63 caracteres; o valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-487">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p>
<p><span data-ttu-id="d4308-488">Link para trás: ID do link 11027</span><span class="sxs-lookup"><span data-stu-id="d4308-488">Back link: Link ID 11027</span></span></p>
<p><span data-ttu-id="d4308-489">O link encaminhamento correspondente para esse link regressivo é <strong>msRTCSIP-MCUFactoryAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-489">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-490">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-490">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-491">msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="d4308-491">msRTCSIP-MCUType</span></span></p></td>
<td><p><span data-ttu-id="d4308-492">Esse atributo é uma cadeia de caracteres com valor único que especifica a mídia que a MCU pode manipular.</span><span class="sxs-lookup"><span data-stu-id="d4308-492">This attribute is a single-valued string that specifies the medium the MCU can handle.</span></span></p>
<p><span data-ttu-id="d4308-493">Os tipos válidos com suporte são:</span><span class="sxs-lookup"><span data-stu-id="d4308-493">Supported valid types are:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-494">reunião</span><span class="sxs-lookup"><span data-stu-id="d4308-494">meeting</span></span></p></li>
<li><p><span data-ttu-id="d4308-495">áudio-vídeo</span><span class="sxs-lookup"><span data-stu-id="d4308-495">audio-video</span></span></p></li>
<li><p><span data-ttu-id="d4308-496">chat</span><span class="sxs-lookup"><span data-stu-id="d4308-496">chat</span></span></p></li>
<li><p><span data-ttu-id="d4308-497">telefone-conf</span><span class="sxs-lookup"><span data-stu-id="d4308-497">phone-conf</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-498">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-498">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-499">msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="d4308-499">msRTCSIP-MCUVendor</span></span></p></td>
<td><p><span data-ttu-id="d4308-500">Esse atributo é uma cadeia de caracteres de valor único que especifica o nome de um fornecedor de MCU.</span><span class="sxs-lookup"><span data-stu-id="d4308-500">This attribute is a single-valued string that specifies an MCU vendor’s name.</span></span> <span data-ttu-id="d4308-501">Todos os Microsoft MCUs especificarão esse atributo para ser <strong>Microsoft Corporation</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-501">All Microsoft MCUs will specify this attribute to be <strong>Microsoft Corporation</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-502">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-502">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-503">msRTCSIP-MeetingFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-503">msRTCSIP-MeetingFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-504">Esse atributo define diferentes opções de reunião que são habilitadas globalmente para todos os usuários ou objetos de contato.</span><span class="sxs-lookup"><span data-stu-id="d4308-504">This attribute defines different meeting options that are enabled globally for all users or contact objects.</span></span> <span data-ttu-id="d4308-505">Esse atributo é um valor de máscara de bits do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="d4308-505">This attribute is a bit-mask value of integer type.</span></span></p>
<p><span data-ttu-id="d4308-506">Os valores válidos (e posições de bit associadas) são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-506">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-507">0: AllowOrganizeMeetingWithAnonymousParticipants é nenhum (não permitir que os usuários convidem usuários anônimos para reuniões) (nenhum bit definido)</span><span class="sxs-lookup"><span data-stu-id="d4308-507">0: AllowOrganizeMeetingWithAnonymousParticipants is None (do not allow users to invite anonymous users to meetings) (no bits set)</span></span></p></li>
<li><p><span data-ttu-id="d4308-508">4: o AllowOrganizeMeetingWithAnonymousParticipants é todos (permitir que todos os usuários convidem usuários anônimos para reuniões) (posição do bit 2)</span><span class="sxs-lookup"><span data-stu-id="d4308-508">4: AllowOrganizeMeetingWithAnonymousParticipants is Everyone (allow all users to invite anonymous users to meetings) (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="d4308-509">8: AllowOrganizeMeetingWithAnonymousParticipants é UsePerUserSetting (permitir que os usuários convidem usuários anônimos para reuniões com base na configuração por usuário) (posição de bit 3)</span><span class="sxs-lookup"><span data-stu-id="d4308-509">8: AllowOrganizeMeetingWithAnonymousParticipants is UsePerUserSetting (allow users to invite anonymous users to meetings based on per user setting) (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="d4308-510">16: UserPerUserMeetingPolicy (a política de reunião é definida por usuário) (posição 4 do bit)</span><span class="sxs-lookup"><span data-stu-id="d4308-510">16: UserPerUserMeetingPolicy (meeting policy is defined per user) (bit position 4)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-511">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-511">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-512">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-512">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-513">msRTCSIP-MeetingPolicy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-513">msRTCSIP-MeetingPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-514">Esse atributo especifica o nome diferenciado (DN) da política que o administrador atribuiu para este usuário como um atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="d4308-514">This attribute specifies the distinguished name (DN) of the policy the administrator has assigned for this user as a single-valued attribute.</span></span></p></td>
<td><p><span data-ttu-id="d4308-515">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-515">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-516">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-516">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-518">Esse atributo representa a janela de tempo limite de assinatura de presença mínima.</span><span class="sxs-lookup"><span data-stu-id="d4308-518">This attribute represents the minimum presence subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-519">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-519">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-520">msRTCSIP-MinRegistrationTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-520">msRTCSIP-MinRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-521">Esse atributo representa a janela de tempo limite de inscrição mínima.</span><span class="sxs-lookup"><span data-stu-id="d4308-521">This attribute represents the minimum registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-522">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-522">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-523">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-523">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-525">Esse atributo representa a janela de tempo limite de assinatura de dados de roaming mínimo.</span><span class="sxs-lookup"><span data-stu-id="d4308-525">This attribute represents the minimum roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="d4308-526">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-526">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-527">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-527">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-528">msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="d4308-528">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="d4308-529">Esse atributo é usado para armazenar o back-end do SQL Server espelhado usado pelo pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="d4308-529">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
<td><p><span data-ttu-id="d4308-530">Novo no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d4308-530">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-531">msRTCSIP-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="d4308-531">msRTCSIP-MobilityFlags</span></span></p></td>
<td><p><span data-ttu-id="d4308-532">Esse atributo contém opções e sinalizadores que definem as configurações de mobilidade.</span><span class="sxs-lookup"><span data-stu-id="d4308-532">This attribute contains options and flags that define mobility settings.</span></span></p></td>
<td><p><span data-ttu-id="d4308-533">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-533">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-534">msRTCSIP-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d4308-534">msRTCSIP-MobilityPolicy</span></span></p></td>
<td><p><span data-ttu-id="d4308-535">Esse atributo contém o DN para um objeto de política de mobilidade.</span><span class="sxs-lookup"><span data-stu-id="d4308-535">This attribute contains the DN for a mobility policy object.</span></span></p></td>
<td><p><span data-ttu-id="d4308-536">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-536">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-537">msRTCSIP-NumDevicesPerUser (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-537">msRTCSIP-NumDevicesPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-538">Esse atributo representa o número permitido de dispositivos nos quais um usuário pode se registrar para comunicações SIP e se inscrever na presença.</span><span class="sxs-lookup"><span data-stu-id="d4308-538">This attribute represents the allowed number of devices on which a user can register for SIP communications and subscribe to presence.</span></span></p></td>
<td><p><span data-ttu-id="d4308-539">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-539">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-540">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-540">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-541">msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="d4308-541">msRTCSIP-OptionFlags</span></span></p></td>
<td><p><span data-ttu-id="d4308-542">Esse atributo especifica as opções que são habilitadas para o objeto de contato ou usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-542">This attribute specifies the options that are enabled for the user or contact object.</span></span> <span data-ttu-id="d4308-543">Esse atributo é um valor de máscara de bits do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="d4308-543">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="d4308-544">Cada opção é representada por um pouco.</span><span class="sxs-lookup"><span data-stu-id="d4308-544">Each option is represented by a bit.</span></span> <span data-ttu-id="d4308-545">Esse atributo está marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-545">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="d4308-546">Os valores válidos (e posições de bit associadas) são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-546">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-547">1: habilitado para conectividade de mensagens instantâneas (IM) públicas (posição do bit 0)</span><span class="sxs-lookup"><span data-stu-id="d4308-547">1: Enabled for public instant messaging (IM) connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="d4308-548">2: reservado (posição do bit 1)</span><span class="sxs-lookup"><span data-stu-id="d4308-548">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="d4308-549">4: reservado (posição do bit 2)</span><span class="sxs-lookup"><span data-stu-id="d4308-549">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="d4308-550">8: reservado (posição do bit 3)</span><span class="sxs-lookup"><span data-stu-id="d4308-550">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="d4308-551">16: controle de chamada remota habilitado [telefonia] (posição de bit 4)</span><span class="sxs-lookup"><span data-stu-id="d4308-551">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="d4308-552">64: AllowOrganizeMeetingWithAnonymousParticipants (permite que os usuários convidem usuários anônimos para reuniões (posição de bit 6)</span><span class="sxs-lookup"><span data-stu-id="d4308-552">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="d4308-553">128: UCEnabled (habilitar usuários para UC) (posição do bit 7)</span><span class="sxs-lookup"><span data-stu-id="d4308-553">128: UCEnabled (enable users for UC) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="d4308-554">256: EnabledForEnhancedPresence (habilitar usuário para conectividade de IM pública) (posição de bit 8)</span><span class="sxs-lookup"><span data-stu-id="d4308-554">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="d4308-555">512: RemoteCallControlDualMode (posição do bit 9)</span><span class="sxs-lookup"><span data-stu-id="d4308-555">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-556">Novo no Live Communications Server 2005 com SP1.</span><span class="sxs-lookup"><span data-stu-id="d4308-556">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-557">msRTCSIP-OriginatorSID</span><span class="sxs-lookup"><span data-stu-id="d4308-557">msRTCSIP-OriginatorSID</span></span></p></td>
<td><p><span data-ttu-id="d4308-558">Esse atributo é usado em topologias de floresta central e de recursos para habilitar o logon único quando os objetos do usuário da conta principal do Windows NT Server são copiados para esse atributo do usuário ou do objeto de contato correspondente no recurso ou na floresta central.</span><span class="sxs-lookup"><span data-stu-id="d4308-558">This attribute is used in resource and central forest topologies to enable single sign-on when a user’s ObjectSID from the Windows NT Server principal account is copied into this attribute of the corresponding user or contact object in the resource or central forest.</span></span> <span data-ttu-id="d4308-559">O Communicator Web Access procura por um usuário no AD DS usando esse atributo ou o ObjectID do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-559">Communicator Web Access searches for a user in AD DS using this attribute or the user’s ObjectSID.</span></span> <span data-ttu-id="d4308-560">Esse atributo está marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-560">This attribute is marked for global catalog replication.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-561">msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="d4308-561">msRTCSIP-OwnerUrn</span></span></p></td>
<td><p><span data-ttu-id="d4308-562">Esse atributo é o nome de recurso uniforme (URN) do proprietário de um contato de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4308-562">This attribute is the Uniform Resource Name (URN) of the owner for an application contact.</span></span></p></td>
<td><p><span data-ttu-id="d4308-563">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-563">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-564">msRTCSIP-padrão (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-564">msRTCSIP-Pattern (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-565">Este atributo de cadeia de caracteres de valor único contém um padrão usado para números de discagem correspondentes no formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="d4308-565">This single-valued string attribute contains a pattern used for matching dial numbers into E.164 format.</span></span> <span data-ttu-id="d4308-566">Se o número de discagem coincidir com esse padrão, a tradução será aplicada ao número discado.</span><span class="sxs-lookup"><span data-stu-id="d4308-566">If the dial number matches this pattern, the translation is applied to the dialed number.</span></span></p></td>
<td><p><span data-ttu-id="d4308-567">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-567">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-568">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-568">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-569">msRTCSIP-PhoneRouteBL (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-569">msRTCSIP-PhoneRouteBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-570">Este atributo de valores múltiplos contém uma lista de nomes distintos de rota de telefone (DN).</span><span class="sxs-lookup"><span data-stu-id="d4308-570">This multi-valued attribute contains a list of phone route distinguished names (DN).</span></span> <span data-ttu-id="d4308-571">Esse atributo especifica o link para trás para uma ou mais rotas de telefone.</span><span class="sxs-lookup"><span data-stu-id="d4308-571">This attribute specifies the back link to one or more phone routes.</span></span></p>
<p><span data-ttu-id="d4308-572">Link para trás: <strong>ID do link 11033</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-572">Back link: <strong>Link ID 11033</strong></span></span></p>
<p><span data-ttu-id="d4308-573">Esse atributo corresponde ao link Forward <strong>msRTCSIP-RouteUsageLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-573">This attribute corresponds to the forward link <strong>msRTCSIP-RouteUsageLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-574">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-574">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-575">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-575">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-576">msRTCSIP-PhoneRouteData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-576">msRTCSIP-PhoneRouteData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-577">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-577">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-578">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-578">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-579">msRTCSIP-PhoneRouteName (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-579">msRTCSIP-PhoneRouteName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-580">Esse atributo de cadeia de caracteres UNICODE de valor único especifica o nome amigável da rota do telefone, para que ele possa ser referenciado facilmente pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="d4308-580">This single valued UNICODE string attribute specifies the friendly name of the phone route, so it can easily be referenced by the administrator.</span></span></p></td>
<td><p><span data-ttu-id="d4308-581">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-581">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-582">msRTCSIP-PhoneUsageData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-582">msRTCSIP-PhoneUsageData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-583">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-583">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-584">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-584">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-585">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-585">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-586">msRTCSIP-PolicyContent (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-586">msRTCSIP-PolicyContent (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-587">Esse atributo é uma cadeia de caracteres Unicode com um único valor.</span><span class="sxs-lookup"><span data-stu-id="d4308-587">This attribute is a single-valued Unicode string.</span></span> <span data-ttu-id="d4308-588">Este atributo de cadeia de caracteres contém a definição de política no formato XML.</span><span class="sxs-lookup"><span data-stu-id="d4308-588">This string attribute contains the policy definition in XML format.</span></span> <span data-ttu-id="d4308-589">A definição do esquema XML é comum em diferentes tipos de política, apenas as configurações são diferentes para cada tipo de política.</span><span class="sxs-lookup"><span data-stu-id="d4308-589">The XML schema definition is common across different policy types, only the settings are different for each policy type.</span></span></p>
<p><span data-ttu-id="d4308-590">A definição de esquema XML (XSD) é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d4308-590">The XML schema definition (XSD) is defined as follows:</span></span></p>
<pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;xs:schema id=&quot;instance&quot; xmlns=&quot;&quot; xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:msdata=&quot;urn:schemas-microsoft-com:xml-msdata&quot;&gt;
  &lt;xs:element name=&quot;instance&quot; msdata:IsDataSet=&quot;true&quot;&gt;
    &lt;xs:complexType&gt;
      &lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
        &lt;xs:element name=&quot;property&quot; nillable=&quot;true&quot;&gt;
          &lt;xs:complexType&gt;
            &lt;xs:simpleContent msdata:ColumnName=&quot;property_Text&quot; msdata:Ordinal=&quot;1&quot;&gt;
              &lt;xs:extension base=&quot;xs:string&quot;&gt;
                &lt;xs:attribute name=&quot;name&quot; type=&quot;xs:string&quot; /&gt;
              &lt;/xs:extension&gt;
            &lt;/xs:simpleContent&gt;
          &lt;/xs:complexType&gt;
        &lt;/xs:element&gt;
      &lt;/xs:choice&gt;
    &lt;/xs:complexType&gt;
  &lt;/xs:element&gt;
&lt;/xs:schema&gt;</code></pre></td>
<td><p><span data-ttu-id="d4308-591">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-591">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-592">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-592">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-593">msRTCSIP-PolicyData (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-593">msRTCSIP-PolicyData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-594">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-594">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-595">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-595">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-596">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-596">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-597">msRTCSIP-PolicyType (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-597">msRTCSIP-PolicyType (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-598">Esse atributo de cadeia de caracteres Unicode com valor único contém o tipo de política.</span><span class="sxs-lookup"><span data-stu-id="d4308-598">This single-valued Unicode string attribute contains the policy type.</span></span> <span data-ttu-id="d4308-599">Os tipos de política válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-599">Valid policy types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-600">reunião</span><span class="sxs-lookup"><span data-stu-id="d4308-600">meeting</span></span></p></li>
<li><p><span data-ttu-id="d4308-601">telefonia</span><span class="sxs-lookup"><span data-stu-id="d4308-601">telephony</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-602">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-602">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-603">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-603">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-604">msRTCSIP-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="d4308-604">msRTCSIP-PoolAddress</span></span></p></td>
<td><p><span data-ttu-id="d4308-605">Esse atributo especifica um link de volta para o pool ao qual um computador pertence.</span><span class="sxs-lookup"><span data-stu-id="d4308-605">This attribute specifies a link back to the pool to which a computer belongs.</span></span> <span data-ttu-id="d4308-606">Esse atributo é definido independentemente de o computador estar executando a edição Standard ou Enterprise do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4308-606">This attribute is set regardless of whether the computer is running the Standard Edition or the Enterprise Edition of Lync Server.</span></span> <span data-ttu-id="d4308-607">Esse atributo está marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-607">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="d4308-608">O valor válido é o nome de domínio do pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-608">The valid value is the domain name of the pool.</span></span></p>
<p><span data-ttu-id="d4308-609">Link encaminhar: <strong>ID do link 11022</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-609">Forward link: <strong>Link ID 11022</strong></span></span></p>
<p><span data-ttu-id="d4308-610">O link regressivo correspondente a este atributo de link de encaminhamento é <strong>msRTCSIP-FrontEndServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-610">The corresponding back link to this forward link attribute is <strong>msRTCSIP-FrontEndServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-611">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-611">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-612">msRTCSIP-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="d4308-612">msRTCSIP-PoolAddresses</span></span></p></td>
<td><p><span data-ttu-id="d4308-613">Esse é um atributo de valores múltiplos que contém uma lista de nomes diferenciados (DN) de pools com os quais a fábrica do MCU está associada.</span><span class="sxs-lookup"><span data-stu-id="d4308-613">This is a multi-valued attribute that contains a list of the distinguished names (DN) of pools with which the MCU factory is associated.</span></span></p>
<p><span data-ttu-id="d4308-614">Link para trás: <strong>ID do link 11025</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-614">Back link: <strong>Link ID 11025</strong></span></span></p>
<p><span data-ttu-id="d4308-615">O link encaminhamento correspondente para esse link regressivo é <strong>msRTCSIP-MCUFactoryPath</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-615">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryPath</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-616">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-616">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-617">msRTCSIP-PoolData</span><span class="sxs-lookup"><span data-stu-id="d4308-617">msRTCSIP-PoolData</span></span></p></td>
<td><p><span data-ttu-id="d4308-618">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-618">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-619">Novo no Live Communications Server 2005 com SP1.</span><span class="sxs-lookup"><span data-stu-id="d4308-619">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-620">msRTCSIP-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="d4308-620">msRTCSIP-PoolDisplayName</span></span></p></td>
<td><p><span data-ttu-id="d4308-621">Esse atributo especifica um nome arbitrário para um pool que é exibido pelo console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d4308-621">This attribute specifies an arbitrary name for a pool that is displayed by the management console.</span></span> <span data-ttu-id="d4308-622">Esse nome pode ser alterado pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="d4308-622">This name can be changed by the administrator.</span></span></p>
<p><span data-ttu-id="d4308-623">O valor válido é uma cadeia de caracteres que representa o nome de um pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-623">The valid value is a string representing the name of a pool.</span></span></p></td>
<td><p><span data-ttu-id="d4308-624">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-624">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-625">msRTCSIP-PoolDomainFQDN</span><span class="sxs-lookup"><span data-stu-id="d4308-625">msRTCSIP-PoolDomainFQDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-626">Esse atributo é um valor de cadeia de caracteres de valor único.</span><span class="sxs-lookup"><span data-stu-id="d4308-626">This attribute is a single-valued string value.</span></span> <span data-ttu-id="d4308-627">O valor desse atributo, quando presente, representa o FQDN do domínio do pool se o administrador quiser criar um pool de front-end com um FQDN que não esteja em conformidade com a estrutura de domínio do Active Directory na qual o pool de front-ends é criado (por exemplo, um namespace SIP desassociado do espaço para nome do sistema de nomes de domínio (DNS)).</span><span class="sxs-lookup"><span data-stu-id="d4308-627">The value of this attribute, when present, represents the pool’s domain FQDN if the administrator wants to create a Front End pool with an FQDN that does not conform to the Active Directory domain structure in which the Front End pool is created (for example, a SIP namespace disjoined from Domain Name System (DNS) namespace).</span></span></p>
<p><span data-ttu-id="d4308-628">Recomendamos que você mapeie o FQDN do domínio do pool de front-end para a parte do nome do domínio como o domínio do Active Directory no qual o pool reside.</span><span class="sxs-lookup"><span data-stu-id="d4308-628">We recommend that you map the Front End pool domain FQDN to the domain name portion as the Active Directory domain in which the pool resides.</span></span> <span data-ttu-id="d4308-629">Portanto, quando nenhum valor estiver presente nesse atributo, o FQDN do pool de front-end usará como padrão a estrutura de nomes de domínio do Active Directory, como indicado pelo atributo <strong>dNSHostName</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4308-629">Therefore, when no value is present in this attribute, the Front End pool FQDN will default to the Active Directory domain name structure, as denoted by the <strong>dnsHostName</strong> attribute.</span></span></p></td>
<td><p><span data-ttu-id="d4308-630">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-630">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-631">msRTCSIP-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="d4308-631">msRTCSIP-PoolFunctionality</span></span></p></td>
<td><p><span data-ttu-id="d4308-632">Uma lista de vários valores de todos os nomes de domínio de todos os servidores do Lync Server, Enterprise Edition associados a um pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-632">A multi-valued list of the domain names of all Lync Server, Enterprise Edition servers associated with a pool.</span></span> <span data-ttu-id="d4308-633">Esse atributo do tipo Integer define se o pool é capaz de enviar mensagens instantâneas (IM) e presença e reuniões.</span><span class="sxs-lookup"><span data-stu-id="d4308-633">This attribute of type integer defines whether the pool is capable of instant messaging (IM) and presence, and meetings.</span></span></p>
<p><span data-ttu-id="d4308-634">Os possíveis tipos de valor válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-634">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-635">Indefinido: serviço de mensagem instantânea e de presença (Live Communications Server 2005 e 2003)</span><span class="sxs-lookup"><span data-stu-id="d4308-635">Undefined: IM and Presence Service (Live Communications Server 2005 and 2003)</span></span></p></li>
<li><p><span data-ttu-id="d4308-636">1: serviço de mensagem instantânea e de presença (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="d4308-636">1: IM and Presence Service (Lync Server)</span></span></p></li>
<li><p><span data-ttu-id="d4308-637">2: mensagens de chat e presença e serviço de reunião (Lync Server)</span><span class="sxs-lookup"><span data-stu-id="d4308-637">2: IM and Presence and Meeting Service (Lync Server)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-638">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-638">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-639">msRTCSIP-Pooltype</span><span class="sxs-lookup"><span data-stu-id="d4308-639">msRTCSIP-PoolType</span></span></p></td>
<td><p><span data-ttu-id="d4308-640">Esse atributo especifica se um pool de servidores está executando o Standard Edition Server ou o Enterprise Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d4308-640">This attribute specifies whether a server pool is running Standard Edition server or Enterprise Edition server.</span></span> <span data-ttu-id="d4308-641">Esse atributo é um valor de máscara de bits do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="d4308-641">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="d4308-642">Cada opção é representada por um pouco.</span><span class="sxs-lookup"><span data-stu-id="d4308-642">Each option is represented by a bit.</span></span></p>
<p><span data-ttu-id="d4308-643">Os valores válidos (e posições de bit associadas) são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-643">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-644">1: servidor de edição padrão, usuários de host (posição do bit 0)</span><span class="sxs-lookup"><span data-stu-id="d4308-644">1: Standard Edition server, hosts users (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="d4308-645">2: Enterprise Edition Server, usuários de host (posição de bit 1)</span><span class="sxs-lookup"><span data-stu-id="d4308-645">2: Enterprise Edition server, hosts users (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="d4308-646">4: servidor Standard Edition, aplicativos de host (posição 2 do bit)</span><span class="sxs-lookup"><span data-stu-id="d4308-646">4: Standard Edition server, hosts applications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="d4308-647">8: Enterprise Edition Server, aplicativos de host (posição de bit 3)</span><span class="sxs-lookup"><span data-stu-id="d4308-647">8: Enterprise Edition server, hosts applications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="d4308-648">Como o Lync Server não oferece suporte a pools que hospedam apenas aplicativos, os únicos valores válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-648">Because Lync Server does not support pools that host only applications, the only valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-649">5: servidor Standard Edition, hospeda usuários e aplicativos (posições de bit 0 e 2)</span><span class="sxs-lookup"><span data-stu-id="d4308-649">5: Standard Edition server, hosts users and applications (bit positions 0 and 2)</span></span></p></li>
<li><p><span data-ttu-id="d4308-650">10: Enterprise Edition Server, hospeda usuários e aplicativos (posições de bit 1 e 3)</span><span class="sxs-lookup"><span data-stu-id="d4308-650">10: Enterprise Edition server, hosts users and applications (bit positions 1 and 3)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-651">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-651">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-652">msRTCSIP-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="d4308-652">msRTCSIP-PoolVersion</span></span></p></td>
<td><p><span data-ttu-id="d4308-653">Esse atributo define a versão do pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-653">This attribute defines the pool version.</span></span> <span data-ttu-id="d4308-654">É um tipo de inteiro que é incrementado com cada lançamento de produto principal.</span><span class="sxs-lookup"><span data-stu-id="d4308-654">It is an integer type that is incremented with each major product release.</span></span></p>
<p><span data-ttu-id="d4308-655">Os possíveis tipos de valor válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-655">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-656">0: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4308-656">0: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="d4308-657">1: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="d4308-657">1: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="d4308-658">2: Live Communications Server 2005 com SP1</span><span class="sxs-lookup"><span data-stu-id="d4308-658">2: Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="d4308-659">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d4308-659">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="d4308-660">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d4308-660">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="d4308-661">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d4308-661">5: Lync Server 2010</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-662">Live Communications Server 2005 com SP1.</span><span class="sxs-lookup"><span data-stu-id="d4308-662">Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-663">msRTCSIP-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="d4308-663">msRTCSIP-PresenceFlags</span></span></p></td>
<td><p><span data-ttu-id="d4308-664">Esse atributo contém opções e sinalizadores que definem as configurações de presença.</span><span class="sxs-lookup"><span data-stu-id="d4308-664">This attribute contains options and flags that define presence settings.</span></span></p></td>
<td><p><span data-ttu-id="d4308-665">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-665">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-666">msRTCSIP-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="d4308-666">msRTCSIP-PresencePolicy</span></span></p></td>
<td><p><span data-ttu-id="d4308-667">Esse atributo contém o DN para um objeto de política de presença.</span><span class="sxs-lookup"><span data-stu-id="d4308-667">This attribute contains the DN for a presence policy object.</span></span></p></td>
<td><p><span data-ttu-id="d4308-668">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-668">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-669">msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="d4308-669">msRTCSIP-PrimaryHomeServer</span></span></p></td>
<td><p><span data-ttu-id="d4308-670">Esse atributo habilita um usuário ou contato para mensagens SIP.</span><span class="sxs-lookup"><span data-stu-id="d4308-670">This attribute enables a user or contact for SIP messaging.</span></span> <span data-ttu-id="d4308-671">Ele é adicionado à classe Contact porque, na topologia de floresta central, objetos de contato, não objetos de usuário, estão habilitados para SIP.</span><span class="sxs-lookup"><span data-stu-id="d4308-671">It is added to the contact class because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="d4308-672">O valor válido é o DN do servidor Standard Edition ou do pool Front-end da edição Enterprise onde um usuário é hospedado.</span><span class="sxs-lookup"><span data-stu-id="d4308-672">The valid value is the DN of the Standard Edition server or Enterprise Edition Front End pool where a user is homed.</span></span></p></td>
<td><p><span data-ttu-id="d4308-673">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-673">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-674">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="d4308-674">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="d4308-675">Esse atributo contém o endereço SIP de um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-675">This attribute contains the SIP address of a given user.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-676">msRTCSIP-privado</span><span class="sxs-lookup"><span data-stu-id="d4308-676">msRTCSIP-PrivateLine</span></span></p></td>
<td><p><span data-ttu-id="d4308-677">Esse atributo contém a ID do dispositivo de linha particular.</span><span class="sxs-lookup"><span data-stu-id="d4308-677">This attribute contains the device ID of the private line device.</span></span></p></td>
<td><p><span data-ttu-id="d4308-678">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-678">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-679">msRTCSIP-roteável</span><span class="sxs-lookup"><span data-stu-id="d4308-679">msRTCSIP-Routable</span></span></p></td>
<td><p><span data-ttu-id="d4308-680">Esse atributo é um atributo booliano usado para determinar se o Lync Server está autorizado a direcionar para esse serviço usando seu endereço GRUU.</span><span class="sxs-lookup"><span data-stu-id="d4308-680">This attribute is a Boolean attribute used to determine whether Lync Server is authorized to route to this service using its GRUU address.</span></span> <span data-ttu-id="d4308-681">Se esse valor for definido como <strong>true</strong>, o Lync Server estará autorizado a direcionar para esse serviço.</span><span class="sxs-lookup"><span data-stu-id="d4308-681">If this value is set to <strong>TRUE</strong>, Lync Server is authorized to route to this service.</span></span> <span data-ttu-id="d4308-682">Se esse valor for definido como <strong>false</strong>, o Lync Server não será autorizado a encaminhar para esse serviço.</span><span class="sxs-lookup"><span data-stu-id="d4308-682">If this value is set to <strong>FALSE</strong>, Lync Server is not authorized to route to this service.</span></span></p></td>
<td><p><span data-ttu-id="d4308-683">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-683">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-684">msRTCSIP-RouteUsageAttribute (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-684">msRTCSIP-RouteUsageAttribute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-685">Este atributo de cadeia de caracteres UNICODE com valor único define um atributo que qualifica o uso de uma rota telefônica.</span><span class="sxs-lookup"><span data-stu-id="d4308-685">This single-valued UNICODE string attribute defines an attribute that qualifies the usage for a phone route.</span></span> <span data-ttu-id="d4308-686">A seleção de uma rota telefônica é determinada com base em dois elementos: o atributo Usage atribuído à rota do telefone e os atributos de uso da política permitidos do chamador.</span><span class="sxs-lookup"><span data-stu-id="d4308-686">Selection of a phone route is determined based on two elements: the usage attribute assigned to the phone route and the caller’s allowed policy usage attributes.</span></span> <span data-ttu-id="d4308-687">A primeira rota telefônica com um atributo Usage que corresponda ao uso permitido pelo chamador está selecionada.</span><span class="sxs-lookup"><span data-stu-id="d4308-687">The first phone route with a usage attribute that matches the caller’s allowed usage is selected.</span></span></p></td>
<td><p><span data-ttu-id="d4308-688">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-688">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-689">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-689">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-690">msRTCSIP-RouteUsageLinks (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-690">msRTCSIP-RouteUsageLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-691">Este atributo de nome diferenciado (DN) contém uma lista de nomes diferenciados de uso de rota.</span><span class="sxs-lookup"><span data-stu-id="d4308-691">This multi-valued distinguished name (DN) attribute contains a list of route usage distinguished names.</span></span></p>
<p><span data-ttu-id="d4308-692">Link encaminhar: <strong>ID do link 11032</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-692">Forward link: <strong>Link ID 11032</strong></span></span></p>
<p><span data-ttu-id="d4308-693">Esse atributo é um link de encaminhamento para o link regressivo correspondente <strong>msRTCSIP-PhoneRouteBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-693">This attribute is a forward link to the corresponding back link <strong>msRTCSIP-PhoneRouteBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-694">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-694">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-695">msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="d4308-695">msRTCSIP-RoutingPoolDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-696">Esse atributo contém o DN que aponta para o pool que todo o tráfego SIP endereçado a essa MCU ou serviço confiável deve passar.</span><span class="sxs-lookup"><span data-stu-id="d4308-696">This attribute contains the DN that points to the pool that all SIP traffic addressed to this MCU or Trusted Service must go through.</span></span></p></td>
<td><p><span data-ttu-id="d4308-697">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-697">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-698">msRTCSIP-RuleName (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-698">msRTCSIP-RuleName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-699">Esse atributo de cadeia de caracteres UNICODE com valor único especifica o nome amigável da regra de normalização para que possa ser referenciado facilmente por um administrador.</span><span class="sxs-lookup"><span data-stu-id="d4308-699">This single-valued UNICODE string attribute specifies the friendly name of the normalization rule, so it can easily be referenced by an administrator.</span></span></p></td>
<td><p><span data-ttu-id="d4308-700">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-700">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-701">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-701">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-702">msRTCSIP-SchemaVersion</span><span class="sxs-lookup"><span data-stu-id="d4308-702">msRTCSIP-SchemaVersion</span></span></p></td>
<td><p><span data-ttu-id="d4308-703">Esse atributo representa a versão do esquema atualmente implantada na organização.</span><span class="sxs-lookup"><span data-stu-id="d4308-703">This attribute represents the schema version currently deployed in the organization.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-704">msRTCSIP-SearchMaxRequests (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-704">msRTCSIP-SearchMaxRequests (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-705">Esse atributo limita o número de resultados da pesquisa a ser retornado de uma pesquisa de diretório quando um usuário pesquisa um contato usando o Communicator.</span><span class="sxs-lookup"><span data-stu-id="d4308-705">This attribute limits the number of search results to be returned from a directory search when a user searches for a contact using Communicator.</span></span> <span data-ttu-id="d4308-706">Esse atributo irá substituir o valor fornecido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="d4308-706">This attribute will override the value provided by the client.</span></span></p></td>
<td><p><span data-ttu-id="d4308-707">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-707">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-708">msRTCSIP-SearchMaxResults (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-708">msRTCSIP-SearchMaxResults (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-709">Esse atributo limita o número de solicitações de pesquisa retornadas.</span><span class="sxs-lookup"><span data-stu-id="d4308-709">This attribute limits the number of search requests returned.</span></span></p></td>
<td><p><span data-ttu-id="d4308-710">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-710">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-711">msRTCSIP-ServerBL</span><span class="sxs-lookup"><span data-stu-id="d4308-711">msRTCSIP-ServerBL</span></span></p></td>
<td><p><span data-ttu-id="d4308-712">Este atributo de valores múltiplos é um link regressivo que contém uma lista de nomes diferenciados (DN).</span><span class="sxs-lookup"><span data-stu-id="d4308-712">This multi-valued attribute is a back link that contains a list of distinguished names (DN).</span></span> <span data-ttu-id="d4308-713">Este DNs aponta para um objeto de pool ou <strong>TrustedService</strong> .</span><span class="sxs-lookup"><span data-stu-id="d4308-713">These DNs point to a pool or <strong>TrustedService</strong> object.</span></span></p>
<p><span data-ttu-id="d4308-714">Esse atributo corresponde ao link Forward <strong>msRTCSIP-TrustedServiceLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-714">This attribute corresponds to the forward link <strong>msRTCSIP-TrustedServiceLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-715">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-715">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-716">msRTCSIP-ServerData</span><span class="sxs-lookup"><span data-stu-id="d4308-716">msRTCSIP-ServerData</span></span></p></td>
<td><p><span data-ttu-id="d4308-717">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-717">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-718">msRTCSIP-ServerReferenceBL (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-718">msRTCSIP-ServerReferenceBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-719">Esse atributo de valores múltiplos contém uma lista de nomes distintos.</span><span class="sxs-lookup"><span data-stu-id="d4308-719">This multi-valued attribute contains a list of distinguished names.</span></span> <span data-ttu-id="d4308-720">Esses nomes diferenciados são links de volta que fazem referência a outros objetos do servidor que podem ser atribuídos a um perfil de local padrão.</span><span class="sxs-lookup"><span data-stu-id="d4308-720">These distinguished names are back links that reference other server objects that can be assigned a default location profile.</span></span></p>
<p><span data-ttu-id="d4308-721">Link para trás: <strong>ID do link 11037</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-721">Back link: <strong>Link ID 11037</strong></span></span></p>
<p><span data-ttu-id="d4308-722">O link encaminhamento correspondente para esse link regressivo é <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-722">The corresponding forward link to this back link is <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span></span></p>
<p><span data-ttu-id="d4308-723">Este atributo back link faz referência a pools e somente servidores de mediação.</span><span class="sxs-lookup"><span data-stu-id="d4308-723">This back link attribute references pools and Mediation Servers only.</span></span></p></td>
<td><p><span data-ttu-id="d4308-724">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-724">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-725">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-725">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-726">msRTCSIP-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="d4308-726">msRTCSIP-ServerVersion</span></span></p></td>
<td><p><span data-ttu-id="d4308-727">Esse atributo define as informações sobre a versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="d4308-727">This attribute defines the version information of the server.</span></span> <span data-ttu-id="d4308-728">Este número de versão se aplica a todas as funções de servidor.</span><span class="sxs-lookup"><span data-stu-id="d4308-728">This version number applies to all server roles.</span></span> <span data-ttu-id="d4308-729">É um número inteiro monotonously que aumenta em incrementos com cada lançamento oficial do produto.</span><span class="sxs-lookup"><span data-stu-id="d4308-729">It is a monotonously increasing integer that increments with each official product release.</span></span></p>
<p><span data-ttu-id="d4308-730">Os valores válidos possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-730">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-731">Indefinido: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4308-731">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="d4308-732">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="d4308-732">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="d4308-733">Live Communications Server 2005 com SP1</span><span class="sxs-lookup"><span data-stu-id="d4308-733">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="d4308-734">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d4308-734">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="d4308-735">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d4308-735">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="d4308-736">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d4308-736">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="d4308-737">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4308-737">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-738">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-738">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-739">msRTCSIP-SourceObjectType</span><span class="sxs-lookup"><span data-stu-id="d4308-739">msRTCSIP-SourceObjectType</span></span></p></td>
<td><p><span data-ttu-id="d4308-740">Esse atributo de valor único de tipo inteiro especifica o tipo de objeto ao qual o <strong>msDS-SourceObjectDN</strong> aponta, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d4308-740">This single-valued attribute of integer type specifies the type of object the <strong>msDS-SourceObjectDN</strong> points to, as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-741">nulo | 0x00000001: representa um objeto de usuário principal do Windows NT Server de uma floresta diferente</span><span class="sxs-lookup"><span data-stu-id="d4308-741">null | 0x00000001: Represents a Windows NT Server principal user object from a different forest</span></span></p></li>
<li><p><span data-ttu-id="d4308-742">Os atributos a seguir representam um tipo de grupo de uma floresta diferente para expansão do grupo de distribuição:</span><span class="sxs-lookup"><span data-stu-id="d4308-742">The following attributes represent a group type from a different forest for distribution group expansion:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="d4308-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="d4308-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="d4308-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="d4308-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="d4308-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="d4308-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="d4308-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="d4308-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span><span class="sxs-lookup"><span data-stu-id="d4308-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span></span></p></li>
<li><p><span data-ttu-id="d4308-748">0x90000000: representa um objeto de atendente automático ou de acesso do assinante da mesma floresta ou de uma floresta diferente</span><span class="sxs-lookup"><span data-stu-id="d4308-748">0x90000000: Represents an Auto-Attendant or subscriber access object from the same forest or a different forest</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="d4308-749">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-749">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-750">msRTCSIP-SubscriptionAuthRequired (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-750">msRTCSIP-SubscriptionAuthRequired (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-751">Novo no Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d4308-751">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="d4308-752">Obsoleto no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-752">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-753">msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="d4308-753">msRTCSIP-TargetHomeServer</span></span></p></td>
<td><p><span data-ttu-id="d4308-754">Esse atributo permite mover um usuário ou objeto de contato de um pool do Lync Server para outro.</span><span class="sxs-lookup"><span data-stu-id="d4308-754">This attribute enables you to move a user or contact object from one Lync Server pool to another.</span></span> <span data-ttu-id="d4308-755">Esse atributo é adicionado à classe Contact, porque na topologia de floresta central, objetos de contato, não objetos de usuário, são SIP habilitados.</span><span class="sxs-lookup"><span data-stu-id="d4308-755">This attribute is added to the contact class, because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="d4308-756">O valor válido é o DN do servidor de edição padrão ou do pool de front-end para o qual um usuário deve ser movido.</span><span class="sxs-lookup"><span data-stu-id="d4308-756">The valid value is the DN of the destination Standard Edition server or Front End pool to which a user is to be moved.</span></span></p></td>
<td><p><span data-ttu-id="d4308-757">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-757">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-758">msRTCSIP-TargetPhoneNumber (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-758">msRTCSIP-TargetPhoneNumber (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-759">Este atributo de cadeia de caracteres de valor único contém um padrão ou um intervalo de números de telefone para direcionar para os gateways especificados definidos em <strong>msRTCSIP-gateways</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-759">This single-valued string attribute contains a phone number pattern or range to route to the specified gateways defined in <strong>msRTCSIP-Gateways</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-760">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-760">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-761">msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="d4308-761">msRTCSIP-TargetUserPolicies</span></span></p></td>
<td><p><span data-ttu-id="d4308-762">Esse atributo armazena pares de nome-valor para políticas de destino para usuários do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4308-762">This attribute stores name-value pairs for target policies for Lync Server users.</span></span></p></td>
<td><p><span data-ttu-id="d4308-763">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-763">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-764">msRTCSIP-Tenantid</span><span class="sxs-lookup"><span data-stu-id="d4308-764">msRTCSIP-TenantId</span></span></p></td>
<td><p><span data-ttu-id="d4308-765">Esse atributo armazena o identificador exclusivo de um locatário.</span><span class="sxs-lookup"><span data-stu-id="d4308-765">This attribute stores the unique identifier for a tenant.</span></span></p></td>
<td><p><span data-ttu-id="d4308-766">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-766">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-767">msRTCSIP-tradução (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-767">msRTCSIP-Translation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-768">Esse atributo é usado pelo recurso de voz do Lync Server e contém a cadeia de caracteres de tradução para aplicar o número discado, se for encontrada uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="d4308-768">This attribute is used by the voice feature of Lync Server and contains the translation string to apply on the dialed number, if a match is found.</span></span></p></td>
<td><p><span data-ttu-id="d4308-769">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-769">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="d4308-770">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-770">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-771">msRTCSIP-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="d4308-771">msRTCSIP-TrustedMCUData</span></span></p></td>
<td><p><span data-ttu-id="d4308-772">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-772">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-773">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-773">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-774">msRTCSIP-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="d4308-774">msRTCSIP-TrustedMCUFQDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-775">Esse atributo é um valor de cadeia de caracteres que contém o FQDN do MCU.</span><span class="sxs-lookup"><span data-stu-id="d4308-775">This attribute is a string value that contains the FQDN of the MCU.</span></span> <span data-ttu-id="d4308-776">Esse é um atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="d4308-776">This is a single-valued attribute.</span></span> <span data-ttu-id="d4308-777">O valor válido para cada segmento é de 63 caracteres; o valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-777">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="d4308-778">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-778">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-779">msRTCSIP-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="d4308-779">msRTCSIP-TrustedProxyData</span></span></p></td>
<td><p><span data-ttu-id="d4308-780">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-780">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-781">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-781">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-782">msRTCSIP-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="d4308-782">msRTCSIP-TrustedProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-783">Esse atributo é um valor de cadeia de caracteres que contém o FQDN do servidor que está executando o servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="d4308-783">This attribute is a string value that contains the FQDN of the server running Proxy Server.</span></span> <span data-ttu-id="d4308-784">Esse atributo tem valor único.</span><span class="sxs-lookup"><span data-stu-id="d4308-784">This attribute is single-valued.</span></span> <span data-ttu-id="d4308-785">O valor válido para cada segmento é de 63 caracteres; o valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-785">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="d4308-786">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-786">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-787">msRTCSIP-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="d4308-787">msRTCSIP-TrustedServerData</span></span></p></td>
<td><p><span data-ttu-id="d4308-788">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-788">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-789">msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="d4308-789">msRTCSIP-TrustedServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-790">Esse atributo é um atributo de valor único que representa o FQDN de um servidor confiável.</span><span class="sxs-lookup"><span data-stu-id="d4308-790">This attribute is a single-valued attribute that represents the FQDN of a trusted server.</span></span></p></td>
<td><p><span data-ttu-id="d4308-791">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-791">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-792">msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="d4308-792">msRTCSIP-TrustedServerVersion</span></span></p></td>
<td><p><span data-ttu-id="d4308-793">Esse atributo especifica o número da versão de um servidor na lista de servidores confiáveis.</span><span class="sxs-lookup"><span data-stu-id="d4308-793">This attribute specifies the version number of a server in the trusted server list.</span></span></p>
<p><span data-ttu-id="d4308-794">Os valores válidos possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-794">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-795">NULL: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="d4308-795">NULL: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="d4308-796">2: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="d4308-796">2: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="d4308-797">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="d4308-797">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="d4308-798">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d4308-798">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="d4308-799">5: Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d4308-799">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="d4308-800">6: Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4308-800">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-801">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-801">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-802">msRTCSIP-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="d4308-802">msRTCSIP-TrustedServiceFlags</span></span></p></td>
<td><p><span data-ttu-id="d4308-803">Esse atributo define as opções que são habilitadas para o serviço confiável.</span><span class="sxs-lookup"><span data-stu-id="d4308-803">This attribute defines the options that are enabled for the trusted service.</span></span></p></td>
<td><p><span data-ttu-id="d4308-804">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-804">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-805">msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="d4308-805">msRTCSIP-TrustedServiceLinks</span></span></p></td>
<td><p><span data-ttu-id="d4308-806">Esse atributo com vários valores contém uma lista de nomes diferenciados (DN) que fazem referência a um objeto de serviço confiável, como um serviço de autenticação de retransmissão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d4308-806">This multi-valued attribute contains a list of distinguished names (DN) that reference a trusted service object, such as a Media Relay Authentication Service.</span></span> <span data-ttu-id="d4308-807">Um serviço de autenticação de retransmissão de mídia (posicionado fisicamente no servidor de borda executando o serviço de conferência A/V) deve estar associado a um pool para dar suporte a cenários de áudio para usuários remotos.</span><span class="sxs-lookup"><span data-stu-id="d4308-807">A Media Relay Authentication Service (physically collocated on the Edge Server running the A/V Conferencing service) must be associated with a pool to support audio scenarios for remote users.</span></span></p>
<p><span data-ttu-id="d4308-808">O link regressivo correspondente a este atributo de link de encaminhamento é <strong>msRTCSIP-ServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-808">The corresponding back link to this forward link attribute is <strong>msRTCSIP-ServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-809">UC</span><span class="sxs-lookup"><span data-stu-id="d4308-809">UC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-810">msRTCSIP-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="d4308-810">msRTCSIP-TrustedServicePort</span></span></p></td>
<td><p><span data-ttu-id="d4308-811">Esse atributo é um inteiro que define o número da porta usada para se conectar a este serviço GRUU.</span><span class="sxs-lookup"><span data-stu-id="d4308-811">This attribute is an integer that defines the port number used to connect to this GRUU service.</span></span></p></td>
<td><p><span data-ttu-id="d4308-812">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-812">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-813">msRTCSIP-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="d4308-813">msRTCSIP-TrustedServiceType</span></span></p></td>
<td><p><span data-ttu-id="d4308-814">Esse atributo é um valor de cadeia de caracteres que define o tipo de serviço GRUU que ele representa.</span><span class="sxs-lookup"><span data-stu-id="d4308-814">This attribute is a string value that defines the type of GRUU service it represents.</span></span></p>
<p><span data-ttu-id="d4308-815">Os tipos de serviço GRUU válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-815">The valid GRUU service types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-816">MediationServer</span><span class="sxs-lookup"><span data-stu-id="d4308-816">MediationServer</span></span></p></li>
<li><p><span data-ttu-id="d4308-817">Gateway</span><span class="sxs-lookup"><span data-stu-id="d4308-817">Gateway</span></span></p></li>
<li><p><span data-ttu-id="d4308-818">Serviço de autenticação de retransmissão de mídia (MRAS)</span><span class="sxs-lookup"><span data-stu-id="d4308-818">Media Relay Authentication Service (MRAS)</span></span></p></li>
<li><p><span data-ttu-id="d4308-819">QoSM</span><span class="sxs-lookup"><span data-stu-id="d4308-819">QoSM</span></span></p></li>
<li><p><span data-ttu-id="d4308-820">msRTCSIP-userextension CWA</span><span class="sxs-lookup"><span data-stu-id="d4308-820">msRTCSIP-UserExtension CWA</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-821">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-821">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-822">msRTCSIP-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="d4308-822">msRTCSIP-TrustedWebComponentsServerData</span></span></p></td>
<td><p><span data-ttu-id="d4308-823">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-823">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-824">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-824">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-825">msRTCSIP-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="d4308-825">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="d4308-826">Esse atributo é um valor de cadeia de caracteres que contém o FQDN do IIS que executa serviços Web do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4308-826">This attribute is a string value that contains the FQDN of the IIS running Lync Server Web Services.</span></span> <span data-ttu-id="d4308-827">Esse é um atributo de valor único.</span><span class="sxs-lookup"><span data-stu-id="d4308-827">This is a single-valued attribute.</span></span> <span data-ttu-id="d4308-828">O valor válido para cada segmento é de 63 caracteres; o valor válido para o FQDN inteiro é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4308-828">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="d4308-829">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-829">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-830">msRTCSIP-UCFlags (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-830">msRTCSIP-UCFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-831">Esse atributo define opções de comunicação unificadas diferentes que são habilitadas globalmente para todos os objetos de contato ou usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-831">This attribute defines different UC options that are enabled globally to all user or contact objects.</span></span> <span data-ttu-id="d4308-832">Esse atributo é um valor de máscara de bits do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="d4308-832">This attribute is a bit-mask value of integer type.</span></span> <span data-ttu-id="d4308-833">Cada opção é representada pela presença de um pouco.</span><span class="sxs-lookup"><span data-stu-id="d4308-833">Each option is represented by the presence of a bit.</span></span></p>
<p><span data-ttu-id="d4308-834">O possível valor válido (e a posição de bit associado) são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-834">The possible valid value (and associated bit position) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-835">4: UsePerUserUCPolicy (posição do bit 2)</span><span class="sxs-lookup"><span data-stu-id="d4308-835">4: UsePerUserUCPolicy (bit position 2)</span></span></p></li>
</ul>
<p><span data-ttu-id="d4308-836">Quando este bit é definido, a política de UC é definida por usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-836">When this bit is set, the UC policy is defined per user.</span></span></p></td>
<td><p><span data-ttu-id="d4308-837">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-837">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-838">msRTCSIP-UCPolicy (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-838">msRTCSIP-UCPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-839">Esse atributo com valor único contém o DN (nome distinto) da política de UC que o administrador atribuiu para este usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-839">This single-valued attribute contains the distinguished name (DN) of the UC policy that the administrator has assigned for this user.</span></span></p></td>
<td><p><span data-ttu-id="d4308-840">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-840">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-841">msRTCSIP-userdomainlist (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-841">msRTCSIP-UserDomainList (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="d4308-842">Esse atributo fornece uma lista de todos os domínios em uma floresta que hospeda usuários habilitados para SIP.</span><span class="sxs-lookup"><span data-stu-id="d4308-842">This attribute provides a list of all the domains in a forest that host SIP-enabled users.</span></span> <span data-ttu-id="d4308-843">O padrão é uma lista vazia, indicando que todos os domínios na floresta são habilitados para SIP.</span><span class="sxs-lookup"><span data-stu-id="d4308-843">The default is an empty list, indicating that all domains in the forest are SIP-enabled.</span></span></p>
<p><span data-ttu-id="d4308-844">Os valores válidos são várias cadeias de caracteres que representam os nomes de domínio de domínios individuais.</span><span class="sxs-lookup"><span data-stu-id="d4308-844">Valid values are multiple strings representing the domain names of individual domains.</span></span></p></td>
<td><p><span data-ttu-id="d4308-845">Novo no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-845">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="d4308-846">Obsoleto no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-846">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-847">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="d4308-847">msRTCSIP-UserEnabled</span></span></p></td>
<td><p><span data-ttu-id="d4308-848">Esse atributo determina se o usuário está habilitado no momento para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d4308-848">This attribute determines whether the user is currently enabled for Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-849">msRTCSIP-userextension</span><span class="sxs-lookup"><span data-stu-id="d4308-849">msRTCSIP-UserExtension</span></span></p></td>
<td><p><span data-ttu-id="d4308-850">Este atributo de valores múltiplos contém uma lista de pares de nomes e valores no formato de &quot; nome = valor. &quot; Esse atributo está marcado para replicação de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="d4308-850">This multi-valued attribute contains a list of name-value pairs in the format of &quot;name=value.&quot; This attribute is marked for global catalog replication.</span></span></p></td>
<td><p><span data-ttu-id="d4308-851">Novo no Live Communications Server 2005 com SP1.</span><span class="sxs-lookup"><span data-stu-id="d4308-851">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-852">msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="d4308-852">msRTCSIP-UserLocationProfile</span></span></p></td>
<td><p><span data-ttu-id="d4308-853">Esse atributo contém o nome diferenciado (DN) que aponta para um objeto de perfil de local.</span><span class="sxs-lookup"><span data-stu-id="d4308-853">This attribute contains the distinguished name (DN) that points to a location profile object.</span></span></p></td>
<td><p><span data-ttu-id="d4308-854">Novo no Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d4308-854">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-855">msRTCSIP-políticas do</span><span class="sxs-lookup"><span data-stu-id="d4308-855">msRTCSIP-UserPolicies</span></span></p></td>
<td><p><span data-ttu-id="d4308-856">Esse atributo armazena pares de nome-valor para políticas de usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-856">This attribute stores name-value pairs for user policies.</span></span></p></td>
<td><p><span data-ttu-id="d4308-857">Novo no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d4308-857">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-858">msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="d4308-858">msRTCSIP-UserPolicy</span></span></p></td>
<td><p><span data-ttu-id="d4308-859">Esse é um atributo com valores múltiplos que contém uma lista de nomes diferenciados com binário (DN_WITH_BINARY) apontando para políticas de usuários globais de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="d4308-859">This is a multi-valued attribute containing a list of distinguished names with binary (DN_WITH_BINARY) pointing to global user policies of different types.</span></span> <span data-ttu-id="d4308-860">A parte binária indica o tipo de política para a qual a parte DN aponta.</span><span class="sxs-lookup"><span data-stu-id="d4308-860">The binary part indicates the type of policy to which the DN portion points.</span></span></p>
<p><span data-ttu-id="d4308-861">Os valores binários válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d4308-861">The valid binary values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-862">0x00000001: política de reunião</span><span class="sxs-lookup"><span data-stu-id="d4308-862">0x00000001: Meeting policy</span></span></p></li>
<li><p><span data-ttu-id="d4308-863">0x00000002: política de UC</span><span class="sxs-lookup"><span data-stu-id="d4308-863">0x00000002: UC policy</span></span></p></li>
<li><p><span data-ttu-id="d4308-864">0x00000005: política de presença</span><span class="sxs-lookup"><span data-stu-id="d4308-864">0x00000005: Presence policy</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-865">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-865">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-866">msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="d4308-866">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="d4308-867">Esta é a ID do grupo de roteamento SIP.</span><span class="sxs-lookup"><span data-stu-id="d4308-867">This is the SIP routing group ID.</span></span> <span data-ttu-id="d4308-868">Os usuários no mesmo grupo serão registrados no mesmo servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="d4308-868">Users in the same group will register to the same Front End Server.</span></span></p></td>
<td><p><span data-ttu-id="d4308-869">Novo no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d4308-869">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-870">msRTCSIP-WebComponentsData</span><span class="sxs-lookup"><span data-stu-id="d4308-870">msRTCSIP-WebComponentsData</span></span></p></td>
<td><p><span data-ttu-id="d4308-871">Esse é um atributo com vários valores.</span><span class="sxs-lookup"><span data-stu-id="d4308-871">This is a multi-valued attribute.</span></span> <span data-ttu-id="d4308-872">Esse atributo é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4308-872">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="d4308-873">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-873">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-874">msRTCSIP-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="d4308-874">msRTCSIP-WebComponentsPoolAddress</span></span></p></td>
<td><p><span data-ttu-id="d4308-875">Esse atributo de valor único aponta para o servidor do pool ou da edição padrão ao qual os componentes Web pertencem.</span><span class="sxs-lookup"><span data-stu-id="d4308-875">This single-valued attribute points to the pool or Standard Edition server to which the web components belong.</span></span></p>
<p><span data-ttu-id="d4308-876">Link encaminhar: <strong>ID do link 11028</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-876">Forward link: <strong>Link ID 11028</strong></span></span></p>
<p><span data-ttu-id="d4308-877">O link regressivo correspondente a este atributo de link de encaminhamento é <strong>msRTCSIP-WebComponentsServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-877">The corresponding back link to this forward link attribute is <strong>msRTCSIP-WebComponentsServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-878">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-878">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-879">msRTCSIP-WebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="d4308-879">msRTCSIP-WebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="d4308-880">Esse atributo é uma lista de vários valores de nomes distintos.</span><span class="sxs-lookup"><span data-stu-id="d4308-880">This attribute is a multi-valued list of distinguished names.</span></span> <span data-ttu-id="d4308-881">Esse atributo contém uma lista de todos os servidores da Web associados a este pool.</span><span class="sxs-lookup"><span data-stu-id="d4308-881">This attribute contains a list of all Web servers associated with this pool.</span></span></p>
<p><span data-ttu-id="d4308-882">Link para trás: <strong>ID do link 11029</strong></span><span class="sxs-lookup"><span data-stu-id="d4308-882">Back link: <strong>Link ID 11029</strong></span></span></p>
<p><span data-ttu-id="d4308-883">O link encaminhamento correspondente para esse link regressivo é <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4308-883">The corresponding forward link to this back link is <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="d4308-884">Novo no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="d4308-884">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-885">msRTCSIP-WMIInstanceId (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="d4308-885">msRTCSIP-WMIInstanceId (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="d4308-886">Novo no Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d4308-886">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="d4308-887">Obsoleto no Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="d4308-887">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-888">OtherIPPhone</span><span class="sxs-lookup"><span data-stu-id="d4308-888">OtherIPPhone</span></span></p></td>
<td><p><span data-ttu-id="d4308-889">Esse atributo existente do Active Directory é usado por telefonia para especificar a lista de endereços TCP/IP alternativos para um telefone.</span><span class="sxs-lookup"><span data-stu-id="d4308-889">This existing Active Directory attribute is used by telephony to specify the list of alternate TCP/IP addresses for a phone.</span></span></p></td>
<td><p><span data-ttu-id="d4308-890">Novo no sistema operacional Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d4308-890">New in Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-891">PhoneOfficeOther</span><span class="sxs-lookup"><span data-stu-id="d4308-891">PhoneOfficeOther</span></span></p></td>
<td><p><span data-ttu-id="d4308-892">Esse atributo existente do Active Directory é usado pelos componentes de voz no Lync Server, somente para objetos de contato, com a finalidade de direcionar chamadas para o atendedor automático da Unificação de mensagens e os números de acesso do Assinante.</span><span class="sxs-lookup"><span data-stu-id="d4308-892">This existing Active Directory attribute is used by the voice components in Lync Server, for contact objects only, for the purpose of routing calls to the unified messaging auto-attendant and subscriber access numbers.</span></span> <span data-ttu-id="d4308-893">O endereço de encaminhamento de chamadas incondicionais é armazenado nesse atributo de vários valores.</span><span class="sxs-lookup"><span data-stu-id="d4308-893">The unconditional call forwarding address is stored in this multi-valued attribute.</span></span> <span data-ttu-id="d4308-894">Esta conta é criada para o propósito específico de acesso automático e do Assinante.</span><span class="sxs-lookup"><span data-stu-id="d4308-894">This account is created for the specific purpose of auto-attendant and subscriber access.</span></span> <span data-ttu-id="d4308-895">Os atributos da conta não devem ser modificados pelos administradores.</span><span class="sxs-lookup"><span data-stu-id="d4308-895">This account’s attributes should not be modified by administrators.</span></span></p></td>
<td><p><span data-ttu-id="d4308-896">Novo no sistema operacional Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d4308-896">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4308-897">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="d4308-897">ProxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="d4308-898">Este atributo de vários valores do Active Directory existente faz parte do esquema base do Active Directory introduzido no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d4308-898">This existing Active Directory multi-valued attribute is part of the base Active Directory schema introduced in Windows 2000.</span></span> <span data-ttu-id="d4308-899">Esse atributo contém os vários endereços X400, X500 e SMTP do email do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-899">This attribute contains the various X400, X500, and SMTP addresses of the user’s email.</span></span> <span data-ttu-id="d4308-900">No Live Communications Server 2003 e posterior, o URI SIP do usuário é adicionado a essa lista usando a &quot; marca SIP: &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4308-900">In Live Communications Server 2003 and later, the user’s SIP URI is added to this list, using the &quot;sip:&quot; tag.</span></span></p>
<p><span data-ttu-id="d4308-901">Os seguintes aplicativos pesquisam o URI do SIP do usuário deste atributo:</span><span class="sxs-lookup"><span data-stu-id="d4308-901">The following applications search the user’s SIP URI from this attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4308-902">Cliente de mensagens e colaboração do Microsoft Office Outlook 2003</span><span class="sxs-lookup"><span data-stu-id="d4308-902">Microsoft Office Outlook 2003 messaging and collaboration client</span></span></p></li>
<li><p><span data-ttu-id="d4308-903">Microsoft Office SharePoint Server 2007</span><span class="sxs-lookup"><span data-stu-id="d4308-903">Microsoft Office SharePoint Server 2007</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d4308-904">Novo no sistema operacional Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d4308-904">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4308-905">TelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="d4308-905">TelephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="d4308-906">Esse atributo existente do Active Directory contém o número de telefone do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4308-906">This existing Active Directory attribute contains the telephone number for the user.</span></span></p></td>
<td><p><span data-ttu-id="d4308-907">Novo no sistema operacional Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d4308-907">New in Windows 2000 operating system.</span></span></p></td>
</tr><span data-ttu-id="d4308-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4308-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

