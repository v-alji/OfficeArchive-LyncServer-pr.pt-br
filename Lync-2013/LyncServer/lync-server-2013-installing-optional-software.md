---
title: 'Lync Server 2013: instalação de software opcional'
description: 'Lync Server 2013: instalação de software opcional.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing optional software
ms:assetid: b95b3301-fa1e-4b96-9af4-05b43d39db8d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615032(v=OCS.15)
ms:contentKeyID: 51541509
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7423c0d54b762fb4af7cedc8d7ba8745fd94bdf7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427023"
---
# <a name="installing-optional-software-in-lync-server-2013"></a><span data-ttu-id="504c9-103">Instalação de software opcional no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="504c9-103">Installing optional software in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="504c9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="504c9-104">

<span> </span></span></span>

<span data-ttu-id="504c9-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="504c9-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="504c9-106">O Microsoft Lync Server 2013, ferramenta de planejamento foi projetado para exportar para o Microsoft Excel e o Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="504c9-106">The Microsoft Lync Server 2013, Planning Tool is designed to export to Microsoft Excel and Microsoft Visio.</span></span> <span data-ttu-id="504c9-107">Embora esses aplicativos não sejam necessários para a operação da ferramenta de planejamento, eles adicionam um valor significativo à implantação e à documentação do seu design.</span><span class="sxs-lookup"><span data-stu-id="504c9-107">While these applications are not required for the operation of the Planning Tool, they do add significant value to the deployment and documentation of your design.</span></span>

<div>

## <a name="optional-software"></a><span data-ttu-id="504c9-108">Software opcional</span><span class="sxs-lookup"><span data-stu-id="504c9-108">Optional Software</span></span>

<div>

## <a name="microsoft-excel"></a><span data-ttu-id="504c9-109">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="504c9-109">Microsoft Excel</span></span>

<span data-ttu-id="504c9-110">Exportar seu design para Microsoft Excel cria um relatório que exibe sete guias na planilha:</span><span class="sxs-lookup"><span data-stu-id="504c9-110">Exporting your design to Microsoft Excel creates a report that displays seven tabs in the spreadsheet:</span></span>

  - <span data-ttu-id="504c9-111">Resumo - Exibe informações sobre a configuração de site, incluindo conta de usuário, configurações de capacidade e informações sobre o perfil do servidor.</span><span class="sxs-lookup"><span data-stu-id="504c9-111">Summary – Displays information on site configuration, including user count, capacity settings, and server profile information.</span></span>

  - <span data-ttu-id="504c9-p102">Perfil de hardware - Exibe um relatório das configurações de hardware recomendadas para servidores especificados na topologia, incluindo CPU, memória, disco e interface de rede. Também está incluída a quantidade e especificações recomendadas para os componentes do servidor. Cada servidor também é definido por site, para fornecer uma representação completa dos requisitos de servidor por cada site.</span><span class="sxs-lookup"><span data-stu-id="504c9-p102">Hardware Profile – Displays a report on the recommended hardware configurations for servers that are specified in the topology, including CPU, memory, disk, and network interface. The quantity and recommended specifications for the server components are also included. In addition, each server is defined by site to provide a complete representation of server requirements by site.</span></span>

  - <span data-ttu-id="504c9-p103">Requisitos de portas - Exibe um relatório de todas as portas habilitadas, além da associação com DNS LB (balanceamento de carga DNS) e HLB (balanceadores de carga de hardware). Esse relatório deve ser usado para planejar suas configurações de firewall e DNS LB e HLB.</span><span class="sxs-lookup"><span data-stu-id="504c9-p103">Ports Requirements – Displays a report of all ports that are enabled, and the association to Domain Name System load balancing (DNS LB) and hardware load balancers (HLB). You should use this report to plan your firewall and DNS LB and HLB configurations.</span></span>

  - <span data-ttu-id="504c9-117">Relatório de resumo – exibe o resumo geral das configurações necessárias para configurar sua rede de servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="504c9-117">Summary Report – Displays the general summary of the settings that are required to set up your Edge Server network.</span></span>

  - <span data-ttu-id="504c9-118">Relatório de certificados – mostra o nome do requerente e os nomes alternativos de assunto que são necessários para os certificados necessários para obter os servidores de borda em execução.</span><span class="sxs-lookup"><span data-stu-id="504c9-118">Certificates Report – Displays the subject name and subject alternate names that are required for the certificates needed to get the Edge Servers running.</span></span>

  - <span data-ttu-id="504c9-119">Relatório do firewall - exibe as portas de origem e destino e endereços IP para as interfaces internas e externas.</span><span class="sxs-lookup"><span data-stu-id="504c9-119">Firewall Report – Displays the source and destination ports and IP addresses for both External and Internal interfaces.</span></span>

  - <span data-ttu-id="504c9-120">Relatório de DNS - exibe o nome de domínio totalmente qualificado (FQDN) e endereços IP/VIP requeridos para cada entrada DNS que você criar.</span><span class="sxs-lookup"><span data-stu-id="504c9-120">DNS Report – Displays the fully qualified domain name (FQDN) and IP/VIP addresses required for each DNS entry that you create.</span></span>

</div>

<div>

## <a name="microsoft-visio"></a><span data-ttu-id="504c9-121">Microsoft Visio</span><span class="sxs-lookup"><span data-stu-id="504c9-121">Microsoft Visio</span></span>

<span data-ttu-id="504c9-p104">Exportar seu design para o Microsoft Visio cria um diagrama para ser usado com seus objetivos de documentação de sua topologia e infraestrutura configuradas. O diagrama importado pode ser editado e reorganizado a fim de atender às suas necessidades de documentação. O diagrama típico do Visio incluirá:</span><span class="sxs-lookup"><span data-stu-id="504c9-p104">Exporting your design to Microsoft Visio creates a diagram for use in your documentation purposes of your configured topology and infrastructure. The imported diagram can be edited and rearranged to meet your documentation needs. The typical Visio diagram will include:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="504c9-125">Se o seu design for grande o suficiente para exigir mais do que três servidores front-end, uma página adicional será criada para o pool de front-end, servidores front-end, o computador que executa o SQL Server, endereços IP e FQDNs.</span><span class="sxs-lookup"><span data-stu-id="504c9-125">If your design is large enough to require more than three Front End Servers, an additional page will be created for the Front End pool, Front End Servers, the computer running SQL Server, IP addresses, and FQDNs.</span></span>



</div>

  - <span data-ttu-id="504c9-126">Topologia global – diagrama dos sites do Lync Server 2013 configurados.</span><span class="sxs-lookup"><span data-stu-id="504c9-126">Global Topology – Diagram of configured Lync Server 2013 sites.</span></span>

  - <span data-ttu-id="504c9-127">Guia nome do site – exibe a topologia de configuração do site com o servidor de borda, o firewall, a PSTN (rede telefônica pública comutada) com gateways e a implantação de servidor interno.</span><span class="sxs-lookup"><span data-stu-id="504c9-127">Site Name tab – Displays the site configuration topology with Edge Server, firewall, public switched telephone network (PSTN) with gateways, and the internal server deployment.</span></span> <span data-ttu-id="504c9-128">A implantação interna consiste em servidores e pools configurados, incluindo os pools de front-end, servidores baseados no SQL Server, serviços de domínio do Active Directory, directors, servidores de Unificação de mensagens (UM), servidores de caixa de correio do Exchange, servidores do Office Web Apps, servidores de mediação e servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="504c9-128">Internal deployment consists of configured servers and pools, including the Front End pools, SQL Server-based servers, Active Directory Domain Services, Directors, Exchange Unified Messaging (UM) servers, Exchange Mailbox Servers, Office Web Apps Servers, Mediation Servers, and Persistent Chat Servers.</span></span>

  - <span data-ttu-id="504c9-129">Diagrama de rede de borda – diagrama detalhando a configuração do servidor de borda com endereços IP e FQDNs associados.</span><span class="sxs-lookup"><span data-stu-id="504c9-129">Edge Network Diagram – Diagram detailing the Edge Server configuration with associated IP addresses and FQDNs.</span></span> <span data-ttu-id="504c9-130">Balanceamento de carga de DNS e balanceadores de carga de hardware também estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="504c9-130">DNS load balancing and hardware load balancers are also included.</span></span> <span data-ttu-id="504c9-131">Além disso, os diretores e o servidor front-end ou o pool de front-end são exibidos com o DNS LB ou o HLB associado e o endereço IP atribuído (a ferramenta de planejamento oferece suporte aos endereços IPv4 e IPv6) e ao FQDN.</span><span class="sxs-lookup"><span data-stu-id="504c9-131">Additionally, Directors and the Front End Server or Front End pool are displayed, with associated DNS LB or HLB and the assigned IP address (the Planning Tool supports both IPv4 and IPv6 addresses) and FQDN.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="504c9-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="504c9-132">See Also</span></span>


[<span data-ttu-id="504c9-133">Instalando a Ferramenta de Planejamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="504c9-133">Installing the Planning Tool in Lync Server 2013</span></span>](lync-server-2013-installing-the-planning-tool.md)  
  

<span data-ttu-id="504c9-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="504c9-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

