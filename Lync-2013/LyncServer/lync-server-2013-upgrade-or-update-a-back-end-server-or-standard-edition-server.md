---
title: Atualizar ou atualizar um servidor back-end do servidor ou Standard Edition
description: Atualize ou atualize um servidor back-end ou Standard Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Upgrade or update a Back End Server or Standard Edition server
ms:assetid: f95f8d3a-e039-484e-97bd-d727db21a12b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721942(v=OCS.15)
ms:contentKeyID: 49733879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c529546bdcf88ada6fd82399d3b65b46b4312db0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440819"
---
# <a name="upgrade-or-update-a-back-end-server-or-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="390e9-103">Atualizar ou atualizar um servidor back-end do servidor ou da edição Standard no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="390e9-103">Upgrade or update a Back End Server or Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="390e9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="390e9-104">

<span> </span></span></span>

<span data-ttu-id="390e9-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="390e9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="390e9-106">Este tópico explica como instalar uma atualização em um servidor back-end da edição Enterprise ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="390e9-106">This topic explains how to install an update on an Enterprise Edition Back End Server or a Standard Edition server.</span></span>

<span data-ttu-id="390e9-107">Se um servidor back-end estiver inoperante durante pelo menos 30 minutos enquanto você estiver atualizando, os usuários poderão entrar no modo de resiliência.</span><span class="sxs-lookup"><span data-stu-id="390e9-107">If a Back End Server is down for at least 30 minutes while you are upgrading it, users may then go into resiliency mode.</span></span> <span data-ttu-id="390e9-108">Quando a atualização estiver concluída e os servidores back-end novamente conectados com os servidores de front-end do pool, os usuários retornarão à funcionalidade completa.</span><span class="sxs-lookup"><span data-stu-id="390e9-108">When the upgrade is finished and the Back End Servers has again connected with the Front End Servers in the pool, users are returned to full functionality.</span></span> <span data-ttu-id="390e9-109">Se a atualização levar menos de 30 minutos, os usuários não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="390e9-109">If the upgrade takes less than 30 minutes, users will not be affected.</span></span>

<div>

## <a name="to-update-a-back-end-server-or-standard-edition-server"></a><span data-ttu-id="390e9-110">Para atualizar um servidor Back End ou um servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="390e9-110">To update a back end server or Standard Edition server</span></span>

1.  <span data-ttu-id="390e9-111">Faça logon no servidor que você estiver atualizando como um membro da função CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="390e9-111">Log on to the server you are upgrading as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="390e9-112">Faça o download do pacote de atualizações e extraia os arquivos para um disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="390e9-112">Download the update and extract it to the local hard disk.</span></span>

3.  <span data-ttu-id="390e9-113">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="390e9-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="390e9-114">Pare os serviços do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="390e9-114">Stop Lync Server services.</span></span> <span data-ttu-id="390e9-115">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="390e9-115">At the command line, type:</span></span>
    
        Stop-CsWindowsService

5.  <span data-ttu-id="390e9-116">Pare o serviço World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="390e9-116">Stop the World Wide Web service.</span></span> <span data-ttu-id="390e9-117">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="390e9-117">At the command line, type:</span></span>
    
        net stop w3svc

6.  <span data-ttu-id="390e9-118">Feche todas as janelas do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="390e9-118">Close all Lync Server Management Shell windows.</span></span>

7.  <span data-ttu-id="390e9-119">Atualize a atualização.</span><span class="sxs-lookup"><span data-stu-id="390e9-119">Install the update.</span></span>

8.  <span data-ttu-id="390e9-120">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="390e9-120">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

9.  <span data-ttu-id="390e9-121">Pare os serviços do Lync Server novamente para capturar assemblies global assembly cache (GAC) – d.</span><span class="sxs-lookup"><span data-stu-id="390e9-121">Stop Lync Server services again to catch Global Assembly Cache (GAC) –d assemblies.</span></span> <span data-ttu-id="390e9-122">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="390e9-122">At the command line, type:</span></span>
    
        Stop-CsWindowsService

10. <span data-ttu-id="390e9-123">Reinicie o serviço World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="390e9-123">Restart the World Wide Web service.</span></span> <span data-ttu-id="390e9-124">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="390e9-124">At the command line, type:</span></span>
    
        net start w3svc

11. <span data-ttu-id="390e9-125">Aplique as alterações feitas por LyncServerUpdateInstaller.exe aos bancos de dados do SQL Server seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="390e9-125">Apply the changes made by LyncServerUpdateInstaller.exe to the SQL Server databases by doing one of the following:</span></span>
    
      - <span data-ttu-id="390e9-126">Se este for um servidor back-end da edição Enterprise e não houver bancos de dados posicionados neste servidor, como arquivar ou monitorar bancos de dados, digite o seguinte na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="390e9-126">If this is an Enterprise Edition Back End Server and there are no collocated databases on this server, such as Archiving or Monitoring databases, then type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>
    
      - <span data-ttu-id="390e9-127">Se este for um servidor back-end do Enterprise Edition e houver bancos de dados posicionados neste servidor, digite o seguinte em uma linha de comando:</span><span class="sxs-lookup"><span data-stu-id="390e9-127">If this is an Enterprise Edition Back End Server and there are collocated databases on this server, then type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>  -ExcludeCollocatedStores
    
      - <span data-ttu-id="390e9-128">Se esse for um servidor Standard Edition, digite o seguinte em uma linha de comando:</span><span class="sxs-lookup"><span data-stu-id="390e9-128">If this is an Standard Edition server, type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -LocalDatabases

<span data-ttu-id="390e9-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="390e9-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

