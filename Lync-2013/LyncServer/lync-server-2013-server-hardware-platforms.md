---
title: 'Lync Server 2013: Plataformas de hardware de servidor'
description: Plataformas de hardware do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server hardware platforms
ms:assetid: c964c1c0-0153-472b-88ad-a38866e0df0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398835(v=OCS.15)
ms:contentKeyID: 48185395
ms.date: 07/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d55deec50994d70cf305b794662a630c16c3af14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441869"
---
# <a name="server-hardware-platforms-for-lync-server-2013"></a><span data-ttu-id="1c2c5-103">Plataformas de hardware de servidor para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c2c5-103">Server hardware platforms for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c2c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c2c5-104">

<span> </span></span></span>

<span data-ttu-id="1c2c5-105">_**Tópico da última modificação:** 2016-07-28_</span><span class="sxs-lookup"><span data-stu-id="1c2c5-105">_**Topic Last Modified:** 2016-07-28_</span></span>

<span data-ttu-id="1c2c5-106">As funções de servidor do Lync Server 2013 e os computadores executando as ferramentas administrativas do Lync Server exigem hardware de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-106">Lync Server 2013 server roles and computers running Lync Server administrative tools require 64-bit hardware.</span></span>

<span data-ttu-id="1c2c5-107">O hardware específico usado para a implantação do Lync Server 2013 pode variar, dependendo dos requisitos de tamanho e uso.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-107">The specific hardware used for Lync Server 2013 deployment can vary, depending on size and usage requirements.</span></span> <span data-ttu-id="1c2c5-108">Esta seção descreve o hardware recomendado.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-108">This section describes the recommended hardware.</span></span> <span data-ttu-id="1c2c5-109">Embora estas sejam recomendações, não obrigações, o uso de hardware que não atende a estas recomendações pode resultar em problemas significativos de desempenho e outros problemas.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-109">Although these are recommendations, not requirements, using hardware that does not meet these recommendations may result in significant performance issues and other issues.</span></span>

<div>

## <a name="recommended-hardware-platform"></a><span data-ttu-id="1c2c5-110">Plataforma de Hardware Recomendada</span><span class="sxs-lookup"><span data-stu-id="1c2c5-110">Recommended Hardware Platform</span></span>

<span data-ttu-id="1c2c5-111">Para obter o melhor desempenho, recomendamos que você execute o Lync Server em servidores com hardware que atenda aos requisitos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-111">For best performance, we recommend that you run Lync Server on servers with hardware that meets the requirements in the following table.</span></span> <span data-ttu-id="1c2c5-112">Se usar um hardware menos poderoso, você poderá enfrentar problemas de funcionalidade ou mau desempenho.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-112">If you use less powerful hardware, you may experience functionality problems or poor performance.</span></span> <span data-ttu-id="1c2c5-113">Observe que esses requisitos de hardware são maiores do que os das versões anteriores do Lync Server, principalmente porque no Lync Server 2013, todos os servidores de front-end executam o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-113">Note that these hardware requirements are higher than those of previous versions of Lync Server, primarily because in Lync Server 2013, all Front End Servers run SQL Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1c2c5-114">O agrupamento da NIC tem suporte e deve ser transparente para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-114">NIC teaming is supported and should be transparent to Lync Server.</span></span> <span data-ttu-id="1c2c5-115">Para obter detalhes, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">servidor de comunicações ou Lync Server e agrupamento de adaptadores de rede</A>.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-115">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">Communications Server or Lync Server and network adapter teaming</A>.</span></span>



</div>

### <a name="recommended-hardware-for-front-end-servers-back-end-servers-standard-edition-servers-persistent-chat-servers-and-persistent-chat-store-and-persistent-chat-compliance-store-back-end-server-roles-for-persistent-chat-server"></a><span data-ttu-id="1c2c5-116">Hardware recomendado para Servidores de Front-End, Servidores de Back-End, Servidores de Edição Padrão, Servidores de Chat Persistente e Armazenamento de Chat Persistente e Armazenamento de Conformidade de Chat Persistente (Funções de Servidores de Back-End para Servidores de Chat Persistente)</span><span class="sxs-lookup"><span data-stu-id="1c2c5-116">Recommended Hardware for Front End Servers, Back End Servers, Standard Edition Servers, Persistent Chat Servers, and Persistent Chat Store and Persistent Chat Compliance Store (Back End Server Roles for Persistent Chat Server)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c2c5-117">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="1c2c5-117">Hardware component</span></span></th>
<th><span data-ttu-id="1c2c5-118">Recomendado</span><span class="sxs-lookup"><span data-stu-id="1c2c5-118">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c2c5-119">CPU</span><span class="sxs-lookup"><span data-stu-id="1c2c5-119">CPU</span></span></p></td>
<td><p><span data-ttu-id="1c2c5-120">Processador duplo de 64 bits, núcleo hexagonal, 2.26 gigahertz (GHz) ou superior.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-120">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="1c2c5-121">Não há suporte para processadores Intel Itanium para funções de servidor do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-121">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2c5-122">Memória</span><span class="sxs-lookup"><span data-stu-id="1c2c5-122">Memory</span></span></p></td>
<td><p><span data-ttu-id="1c2c5-123">32 gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="1c2c5-123">32 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2c5-124">Disco</span><span class="sxs-lookup"><span data-stu-id="1c2c5-124">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1c2c5-125">Oito ou mais unidades de disco rígido de 10.000 RPM com pelo menos 72 GB de espaço em disco livre.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-125">8 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="1c2c5-126">Dois dos discos devem usar RAID 1 e seis devem usar RAID 10.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-126">Two of the disks should use RAID 1, and six should use RAID 10.</span></span></p>
<p><span data-ttu-id="1c2c5-127">- OR</span><span class="sxs-lookup"><span data-stu-id="1c2c5-127">- OR -</span></span></p></li>
<li><p><span data-ttu-id="1c2c5-128">Drivers de estado sólido (SSDs) que oferecem desempenho semelhante a 8 drivers de disco mecânico de 10.000-RPM.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-128">Solid state drives (SSDs) which provide performance similar to 8 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2c5-129">Rede</span><span class="sxs-lookup"><span data-stu-id="1c2c5-129">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1c2c5-130">1 adaptador de rede de porta dupla, 1 Gbps ou superior (2 recomendados, que exige agrupamento com um único endereço MAC e um único endereço IP).</span><span class="sxs-lookup"><span data-stu-id="1c2c5-130">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="1c2c5-131">Não há suporte para configurações de duas ou várias bases para servidores front-end, servidores back-end, servidores de edição padrão e servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-131">Dual or multi-homed configurations are not supported for Front End Servers, Back End Servers, Standard Edition servers, and Persistent Chat Servers.</span></span><BR><span data-ttu-id="1c2c5-132">ILO/DRAC/etc. as conexões não expostas ao sistema operacional e usadas para monitorar e gerenciar o hardware do servidor não constituem um servidor de hospedagem múltipla e, assim, é compatível.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-132">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="recommended-hardware-for-edge-servers-standalone-mediation-servers-and-directors"></a><span data-ttu-id="1c2c5-133">Hardware recomendado para Servidores de Borda, Servidores de Mediação Autônomo e Diretores</span><span class="sxs-lookup"><span data-stu-id="1c2c5-133">Recommended Hardware for Edge Servers, Standalone Mediation Servers, and Directors</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c2c5-134">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="1c2c5-134">Hardware component</span></span></th>
<th><span data-ttu-id="1c2c5-135">Recomendado</span><span class="sxs-lookup"><span data-stu-id="1c2c5-135">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c2c5-136">CPU</span><span class="sxs-lookup"><span data-stu-id="1c2c5-136">CPU</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1c2c5-137">processador dual de 64 bits, Quad-Core, 2,0 gigahertz (GHz) ou superior.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-137">64-bit dual processor, quad-core, 2.0 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="1c2c5-138">- OR</span><span class="sxs-lookup"><span data-stu-id="1c2c5-138">- OR -</span></span></p></li>
<li><p><span data-ttu-id="1c2c5-139">processador de 4 vias de 64 bits, Dual-Core, 2,0 GHz ou superior.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-139">64-bit 4-way processor, dual-core, 2.0 GHz or higher.</span></span></p></li>
</ul>
<p><span data-ttu-id="1c2c5-140">Não há suporte para processadores Intel Itanium para funções de servidor do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-140">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2c5-141">Memória</span><span class="sxs-lookup"><span data-stu-id="1c2c5-141">Memory</span></span></p></td>
<td><p><span data-ttu-id="1c2c5-142">16 gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="1c2c5-142">16 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2c5-143">Disco</span><span class="sxs-lookup"><span data-stu-id="1c2c5-143">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1c2c5-144">4 ou mais 10.000 unidades de disco rígido RPM com pelo menos 72 GB de espaço livre em disco.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-144">4 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="1c2c5-145">Os discos devem estar em uma configuração 2x RAID 1.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-145">The disks should be in a 2x RAID 1 configuration.</span></span></p>
<p><span data-ttu-id="1c2c5-146">- OR</span><span class="sxs-lookup"><span data-stu-id="1c2c5-146">- OR -</span></span></p></li>
<li><p><span data-ttu-id="1c2c5-147">Unidades de estado sólido (SSDs) que ofereçam desempenho semelhante a quatro unidades de disco mecânico de 10.000 RPM.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-147">Solid state drives (SSDs) which provide performance similar to 4 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2c5-148">Rede</span><span class="sxs-lookup"><span data-stu-id="1c2c5-148">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1c2c5-149">1 adaptador de rede de porta dupla, 1 Gbps ou superior (2 recomendados, que exige agrupamento com um único endereço MAC e um único endereço IP).</span><span class="sxs-lookup"><span data-stu-id="1c2c5-149">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span> <span data-ttu-id="1c2c5-150">duas interfaces de rede são necessárias em servidores de borda e têm suporte em servidores de mediação autônomos.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-150">2 network interfaces are required on Edge Servers, and are supported on standalone Mediation Servers.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="1c2c5-151">Não há suporte para configurações de duas ou várias bases para os directors.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-151">Dual or multi-homed configurations are not supported for Directors.</span></span><BR><span data-ttu-id="1c2c5-152">ILO/DRAC/etc. as conexões não expostas ao sistema operacional e usadas para monitorar e gerenciar o hardware do servidor não constituem um servidor de hospedagem múltipla e, assim, é compatível.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-152">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div>
<p><span data-ttu-id="1c2c5-153">Os servidores de borda exigem duas interfaces de rede que sejam adaptadores de rede de duas portas, 1 Gbps ou superior (ou dois adaptadores de rede emparelhados, para um total de quatro, cada par sendo agrupado com um único endereço MAC e um único endereço IP, para um total de dois pares).</span><span class="sxs-lookup"><span data-stu-id="1c2c5-153">Edge Servers will require two network interfaces that are dual-port network adapters, 1 Gbps or higher (or two paired network adapters, for a total of four, each pair being teamed with a single MAC address and a single IP address, for a total of two pairs).</span></span></p>
<p><span data-ttu-id="1c2c5-154">A instalação de placas de interface de rede adicionais (NICs) para permitir a configuração de um endereço IP PSTN específico tem suporte em servidores de mediação autônomos.</span><span class="sxs-lookup"><span data-stu-id="1c2c5-154">Installation of additional network interface cards (NICs) to allow the configuration of a specific PSTN IP address is supported on standalone Mediation Servers.</span></span></p><span data-ttu-id="1c2c5-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c2c5-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

