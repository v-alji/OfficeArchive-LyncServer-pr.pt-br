---
title: 'Lync Server 2013: Recursos obrigatórios para Servidor de Chat Persistente'
description: 'Lync Server 2013: recursos necessários para o servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Required resources
ms:assetid: bce50b95-f3c8-407e-963a-d8896ee77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205211(v=OCS.15)
ms:contentKeyID: 48185255
ms.date: 02/05/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18c81f0017428e4305e46fbcf5580a83af38accf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442693"
---
# <a name="required-resources-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="576fc-103">Recursos obrigatórios para Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="576fc-103">Required resources for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="576fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="576fc-104">

<span> </span></span></span>

<span data-ttu-id="576fc-105">_**Tópico da última modificação:** 2016-02-05_</span><span class="sxs-lookup"><span data-stu-id="576fc-105">_**Topic Last Modified:** 2016-02-05_</span></span>

<span data-ttu-id="576fc-106">A alta disponibilidade e a recuperação de desastres para o servidor de chat persistente exigem recursos adicionais além do que normalmente é necessário para operação completa.</span><span class="sxs-lookup"><span data-stu-id="576fc-106">High availability and disaster recovery for Persistent Chat Server requires additional resources beyond what is typically needed for full operation.</span></span> <span data-ttu-id="576fc-107">Antes de configurar o servidor de chat persistente para alta disponibilidade e recuperação de desastres, certifique-se de ter os seguintes recursos, além do que é necessário para a operação de servidor de chat persistente padrão.</span><span class="sxs-lookup"><span data-stu-id="576fc-107">Before configuring Persistent Chat Server for high availability and disaster recovery, ensure that you have the following resources in addition to what is required for standard Persistent Chat Server operation.</span></span> <span data-ttu-id="576fc-108">Para obter informações de configuração adicionais, consulte [Configurando o servidor de chat persistente no Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="576fc-108">For additional configuration information, see [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span></span>

  - <span data-ttu-id="576fc-109">Uma instância de banco de dados dedicada localizada no mesmo Data Center físico no qual o front-end de página inicial do serviço de servidor de chat persistente está localizado.</span><span class="sxs-lookup"><span data-stu-id="576fc-109">One dedicated database instance located in the same physical data center in which the home front end of the Persistent Chat Server service is located.</span></span> <span data-ttu-id="576fc-110">Esse banco de dados funcionará como o espelho do SQL Server para o banco de dados de chat persistente principal.</span><span class="sxs-lookup"><span data-stu-id="576fc-110">This database will serve as the SQL Server mirror for the primary Persistent Chat database.</span></span> <span data-ttu-id="576fc-111">Opcionalmente, designe um SQL Server adicional para atuar como a testemunha de espelhamento se desejar um failover automatizado para o banco de dados espelho.</span><span class="sxs-lookup"><span data-stu-id="576fc-111">Optionally, designate an additional SQL Server to serve as the mirroring witness if you want an automated failover to the mirror database.</span></span>

  - <span data-ttu-id="576fc-112">Uma instância de banco de dados dedicada localizada no outro data center físico.</span><span class="sxs-lookup"><span data-stu-id="576fc-112">One dedicated database instance located in the other physical data center.</span></span> <span data-ttu-id="576fc-113">Este banco de dados funcionará como o banco de dados secundário de envio de logs do SQL Server para o banco de dados no centro de dados principal.</span><span class="sxs-lookup"><span data-stu-id="576fc-113">This database will serve as the SQL Server Log Shipping secondary database for the database in the primary data center.</span></span>

  - <span data-ttu-id="576fc-114">Uma instância de banco de dados dedicada para servir como o espelho do SQL Server para o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="576fc-114">One dedicated database instance to serve as the SQL Server mirror for the secondary database.</span></span> <span data-ttu-id="576fc-115">Opcionalmente, designe um SQL Server adicional para o servidor como testemunha de espelhamento.</span><span class="sxs-lookup"><span data-stu-id="576fc-115">Optionally, designate an additional SQL Server to server as the mirroring witness.</span></span> <span data-ttu-id="576fc-116">Ambos devem estar localizados no mesmo data center físico que o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="576fc-116">Both of these must be located in the same physical data center as the secondary database.</span></span>

  - <span data-ttu-id="576fc-117">Se a conformidade com o servidor de chat persistente estiver habilitada, serão necessárias outras três instâncias de banco de dados dedicados.</span><span class="sxs-lookup"><span data-stu-id="576fc-117">If Persistent Chat Server compliance is enabled, an additional three dedicated database instances are required.</span></span> <span data-ttu-id="576fc-118">Sua distribuição é a mesma que a que foi descrita anteriormente para o banco de dados de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="576fc-118">Their distribution is the same as those previously outlined for the Persistent Chat database.</span></span> <span data-ttu-id="576fc-119">Embora seja possível que o banco de dados de conformidade compartilhe a mesma instância do SQL Server que o banco de dados de chat persistente, recomendamos instâncias autônomas para alta disponibilidade e recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="576fc-119">While it is possible for the compliance database to share the same SQL Server instance as the Persistent Chat database, we recommend standalone instances for high availability and disaster recovery.</span></span>

  - <span data-ttu-id="576fc-120">Um compartilhamento de arquivos deve ser criado e designado para os logs de transação de envio de logs do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="576fc-120">A file share must be created and designated for the SQL Server Log Shipping transaction logs.</span></span> <span data-ttu-id="576fc-121">Todos os SQL Servers nos dois data centers que executam bancos de dados de chat persistente devem ter acesso de leitura/gravação a este compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="576fc-121">All SQL Servers in both data centers that run Persistent Chat databases must have read/write access to this file share.</span></span> <span data-ttu-id="576fc-122">Esse compartilhamento não está definido como parte de uma função FileStore.</span><span class="sxs-lookup"><span data-stu-id="576fc-122">This share is not defined as part of a FileStore role.</span></span>

  - <span data-ttu-id="576fc-123">Um compartilhamento de arquivo no servidor de banco de dados secundário para atuar como a pasta de destino dos logs de transação do SQL Server que são copiados do compartilhamento de arquivos do servidor primário.</span><span class="sxs-lookup"><span data-stu-id="576fc-123">A file share on the secondary database server to serve as the destination folder for the SQL Server transaction logs that are copied from the primary server file share.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="576fc-124">Os servidores de chat ativos persistentes em um pool de servidores de chat persistente devem residir no mesmo fuso horário do pool de Lync do próximo salto definido na topologia.</span><span class="sxs-lookup"><span data-stu-id="576fc-124">Active Persistent Chat servers in a Persistent Chat Server pool MUST reside in the same time zone as the next hop Lync Pool defined in the topology.</span></span>



</div>

<span data-ttu-id="576fc-125">Os números a seguir fornecem exemplos sobre como o pool de servidores de chat inteiro persistente pode ser configurado nas duas topologias diferentes de pool estendidos:</span><span class="sxs-lookup"><span data-stu-id="576fc-125">The following figures provide examples about how the entire Persistent Chat Server pool can be configured in the two different stretched pool topologies:</span></span>

  - <span data-ttu-id="576fc-126">Pool de servidores de chat persistentes ampliados quando os data centers estão localizados geográficos com alta largura de banda/baixa latência.</span><span class="sxs-lookup"><span data-stu-id="576fc-126">Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.</span></span>

  - <span data-ttu-id="576fc-127">Pool de servidores de chat persistentes ampliados quando os centros de dados estiverem localizados na região de baixa largura de banda/alta latência.</span><span class="sxs-lookup"><span data-stu-id="576fc-127">Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="576fc-128">A figura a seguir mostra uma topologia de pool de servidores de chat persistente com Stretch em que os data centers são localizados geográficos com alta largura de banda/baixa latência.</span><span class="sxs-lookup"><span data-stu-id="576fc-128">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with high bandwidth/low latency.</span></span>

<span data-ttu-id="576fc-129">**Pool de servidores de chat persistentes ampliados quando os data centers estão localizados geográficos com alta largura de banda/baixa latência.**</span><span class="sxs-lookup"><span data-stu-id="576fc-129">**Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.**</span></span>

<span data-ttu-id="576fc-130">![Exame de configuração HBW do pool do servidor de chat persistente](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Exame de configuração HBW do pool do servidor de chat persistente")</span><span class="sxs-lookup"><span data-stu-id="576fc-130">![Persistent Chat Server pool HBW configuration exam](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Persistent Chat Server pool HBW configuration exam")</span></span>

<span data-ttu-id="576fc-131">A figura a seguir mostra uma topologia de pool de servidores de chat persistente com Stretch em que os data centers são localizados geográficos com largura de banda baixa/alta latência.</span><span class="sxs-lookup"><span data-stu-id="576fc-131">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="576fc-132">**Pool de servidores de chat persistentes ampliados quando os centros de dados estiverem localizados na região de baixa largura de banda/alta latência.**</span><span class="sxs-lookup"><span data-stu-id="576fc-132">**Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.**</span></span>

<span data-ttu-id="576fc-133">![Exame de configuração LBW do pool do servidor de chat persistente](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Exame de configuração LBW do pool do servidor de chat persistente")</span><span class="sxs-lookup"><span data-stu-id="576fc-133">![Persistent Chat Server pool LBW configuration exam](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Persistent Chat Server pool LBW configuration exam")</span></span>

<span data-ttu-id="576fc-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="576fc-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

