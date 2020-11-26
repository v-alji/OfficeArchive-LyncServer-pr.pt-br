---
title: 'Lync Server 2013: lista de verificação de implantação de controle de admissão de chamadas'
description: 'Lync Server 2013: lista de verificação de implantação de controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control deployment checklist
ms:assetid: d56a525f-3da5-4ac0-a311-0c5efd98c9df
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398928(v=OCS.15)
ms:contentKeyID: 48185525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: db7a69bda3048f93089a47b43a0b433946b783f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435912"
---
# <a name="call-admission-control-deployment-checklist-for-lync-server-2013"></a><span data-ttu-id="6669e-103">Lista de verificação de implantação de controle de admissão de chamadas para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6669e-103">Call admission control deployment checklist for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6669e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6669e-104">

<span> </span></span></span>

<span data-ttu-id="6669e-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="6669e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="6669e-106">Use a lista de verificação a seguir para verificar se você concluiu todas as tarefas de configuração necessárias para implantar o controle de admissão de chamadas (CAC).</span><span class="sxs-lookup"><span data-stu-id="6669e-106">Use the following checklist to verify that you have completed all the necessary configuration tasks to deploy call admission control (CAC).</span></span>

  - <span data-ttu-id="6669e-107">Se um ou mais servidores Edge estiverem implantados, cada endereço IP de interface externa precisará ser adicionado à lista de sub-rede nas configurações de configuração de rede, com uma máscara de bits de 32.</span><span class="sxs-lookup"><span data-stu-id="6669e-107">If one or more Edge Servers are deployed, each external interface IP address must be added to the subnet list in the network configuration settings, with a bit mask of 32.</span></span> <span data-ttu-id="6669e-108">Associe também essa sub-rede (endereço IP) ao ID do site da rede para o local geográfico onde o serviço de Borda A/V está implantado.</span><span class="sxs-lookup"><span data-stu-id="6669e-108">You should also associate this subnet (IP address) with the network site ID for the geographic location where the A/V Edge service is deployed.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6669e-109">Os servidores de borda não precisam implementar o CAC.</span><span class="sxs-lookup"><span data-stu-id="6669e-109">Edge servers are not required to implement CAC.</span></span>

    
    </div>

  - <span data-ttu-id="6669e-110">Verifique se o CAC está habilitado, seja por meio do painel de controle do Lync Server ou executando o cmdlet conforme especificado em [habilitar o controle de admissão de chamadas no Lync Server 2013](lync-server-2013-enable-call-admission-control.md).</span><span class="sxs-lookup"><span data-stu-id="6669e-110">Make sure that CAC is enabled, either through Lync Server Control Panel or by running the cmdlet as specified in [Enable call admission control in Lync Server 2013](lync-server-2013-enable-call-admission-control.md).</span></span>

  - <span data-ttu-id="6669e-111">Certifique-se de que o CAC está habilitado em todos os sites centrais.</span><span class="sxs-lookup"><span data-stu-id="6669e-111">Make sure that CAC is enabled in all central sites.</span></span> <span data-ttu-id="6669e-112">Isso pode ser feito por meio do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="6669e-112">This can be done through the Topology Builder.</span></span> <span data-ttu-id="6669e-113">Se um aviso for gerado durante a publicação, *não* ignore-o.</span><span class="sxs-lookup"><span data-stu-id="6669e-113">If a warning is generated when you publish, *do not* ignore it.</span></span>

  - <span data-ttu-id="6669e-114">Certifique-se de que todas as subredes gerenciadas na rede corporativa estão definidas nas configurações de rede.</span><span class="sxs-lookup"><span data-stu-id="6669e-114">Make sure that all the subnets that are managed in the enterprise network are configured in the network configuration settings.</span></span> <span data-ttu-id="6669e-115">Também é essencial que cada sub-rede seja associada a um site de rede, conforme explicado em [associar uma sub-rede a um site de rede no Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="6669e-115">It is also essential that every subnet be associated to a network site, as explained in [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span></span>

  - <span data-ttu-id="6669e-116">Certifique-se de que a subrede ou os endereços IP de todos os Servidores Front-End, Aparelhos de Filial Persistentes (SBAs), Servidores de Conferência de Áudio/Vídeo (se estiverem em um pool separado) e Servidores de Mediação estejam definidos nas configurações de rede.</span><span class="sxs-lookup"><span data-stu-id="6669e-116">Make sure that the subnet or IP addresses of all Front End Servers, Survivable Branch Appliances (SBAs), Audio/Video Conferencing Servers (if in a separate pool), and Mediation Servers are configured in the network configuration settings.</span></span>

<span data-ttu-id="6669e-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6669e-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

