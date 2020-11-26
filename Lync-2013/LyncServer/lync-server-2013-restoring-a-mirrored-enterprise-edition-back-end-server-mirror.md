---
title: Restaurando um servidor back-end do espelhado Enterprise Edition-Mirror
description: Restaurando um servidor back-end do espelhado Enterprise Edition-Mirror.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a mirrored Enterprise Edition Back End Server - mirror
ms:assetid: 4b3c8eae-6f1f-4377-b39b-6699e725c517
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945626(v=OCS.15)
ms:contentKeyID: 51541471
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 011c0aaa10ffed6fef7d579dbc16993fd3341070
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436234"
---
# <a name="restoring-a-mirrored-enterprise-edition-back-end-server-in-lync-server-2013---mirror"></a><span data-ttu-id="3eedd-103">Restaurando um servidor back-end da edição Enterprise espelhada no Lync Server 2013-Mirror</span><span class="sxs-lookup"><span data-stu-id="3eedd-103">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3eedd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3eedd-104">

<span> </span></span></span>

<span data-ttu-id="3eedd-105">_**Tópico da última modificação:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="3eedd-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="3eedd-106">Se você tiver um servidor back-end do Enterprise Edition em uma configuração espelhada e somente o espelho falhar, siga os procedimentos desta seção.</span><span class="sxs-lookup"><span data-stu-id="3eedd-106">If you have an Enterprise Edition Back End Server in a mirrored configuration and only the mirror fails, follow the procedures in this section.</span></span> <span data-ttu-id="3eedd-107">Se o banco de dados primário e o espelhamento falharem, consulte [restaurando um servidor back-end do Enterprise Edition no Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span><span class="sxs-lookup"><span data-stu-id="3eedd-107">If both the primary database and mirror fail, see [Restoring an Enterprise Edition Back End Server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md).</span></span> <span data-ttu-id="3eedd-108">Se apenas o principal falhar, consulte [restaurando um servidor back-end do espelhado Enterprise Edition no Lync Server 2013-primário](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md).</span><span class="sxs-lookup"><span data-stu-id="3eedd-108">If only the primary fails, see [Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary](lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md).</span></span> <span data-ttu-id="3eedd-109">Se o banco de dados que hospeda o repositório de gerenciamento central falhar, consulte [restaurando o servidor que hospeda o repositório de gerenciamento central no Lync server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span><span class="sxs-lookup"><span data-stu-id="3eedd-109">If the database hosting the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span> <span data-ttu-id="3eedd-110">Se um servidor membro da edição Enterprise que não for o servidor back-end falhar, consulte [restaurando um servidor membro da Enterprise Edition no Lync server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span><span class="sxs-lookup"><span data-stu-id="3eedd-110">If an Enterprise Edition member server that is not the Back End Server fails, see [Restoring an Enterprise Edition member server in Lync Server 2013](lync-server-2013-restoring-an-enterprise-edition-member-server.md).</span></span>

<span data-ttu-id="3eedd-111">Recomendamos que você tire uma cópia da imagem do sistema antes de iniciar a restauração.</span><span class="sxs-lookup"><span data-stu-id="3eedd-111">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="3eedd-112">Você pode usar essa imagem como um ponto de recuperação, caso algo dê errado durante a restauração.</span><span class="sxs-lookup"><span data-stu-id="3eedd-112">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="3eedd-113">Talvez você queira fazer a cópia da imagem depois de instalar o sistema operacional e o SQL Server, e restaurar ou registrar novamente os certificados.</span><span class="sxs-lookup"><span data-stu-id="3eedd-113">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>

<div>

## <a name="to-restore-an-enterprise-edition-back-end-server-mirror-database"></a><span data-ttu-id="3eedd-114">Para restaurar um banco de dados espelho do servidor back-end do Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3eedd-114">To restore an Enterprise Edition Back End Server Mirror Database</span></span>

1.  <span data-ttu-id="3eedd-115">Em uma conta de usuário que seja um membro do grupo RTCUniversalServerAdmins, faça logon em um servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="3eedd-115">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

2.  <span data-ttu-id="3eedd-116">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="3eedd-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3eedd-117">Desinstale o espelhamento.</span><span class="sxs-lookup"><span data-stu-id="3eedd-117">Uninstall mirroring.</span></span> <span data-ttu-id="3eedd-118">Primeiro, digite o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3eedd-118">First, type the following cmdlet:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn <PrimaryServerFqdn> -SqlInstanceName <SQLInstance> -verbose
    
    <span data-ttu-id="3eedd-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3eedd-119">For example:</span></span>
    
        Uninstall -CsMirrorDatabase -DatabaseType User -SqlServerFqdn server4.contoso.com -SqlInstanceName archinst -verbose
    
    <span data-ttu-id="3eedd-120">Faça isso para todos os tipos de banco de dados neste servidor.</span><span class="sxs-lookup"><span data-stu-id="3eedd-120">Do this for all database types on this server.</span></span>

4.  <span data-ttu-id="3eedd-121">Crie um servidor limpo ou novo que tenha o mesmo nome de domínio totalmente qualificado (FQDN) (DB1.contoso.com) que o computador com falha, instale o sistema operacional e, em seguida, restaure ou registre novamente os certificados.</span><span class="sxs-lookup"><span data-stu-id="3eedd-121">Create a clean or new server that has the same fully qualified domain name (FQDN) (DB1.contoso.com) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span> <span data-ttu-id="3eedd-122">Este servidor funcionará como o novo espelho.</span><span class="sxs-lookup"><span data-stu-id="3eedd-122">This server will function as the new mirror.</span></span>

5.  <span data-ttu-id="3eedd-123">Em uma conta de usuário que seja um membro do grupo RTCUniversalServerAdmins, faça logon no novo servidor.</span><span class="sxs-lookup"><span data-stu-id="3eedd-123">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the new server.</span></span>

6.  <span data-ttu-id="3eedd-124">Instale o SQL Server 2012 ou o SQL Server 2008 R2, mantendo os nomes das instâncias iguais aos anteriores à falha.</span><span class="sxs-lookup"><span data-stu-id="3eedd-124">Install SQL Server 2012 or SQL Server 2008 R2, keeping the instance names the same as before the failure.</span></span>

7.  <span data-ttu-id="3eedd-125">Em uma conta de usuário que seja um membro do grupo RTCUniversalServerAdmins, faça logon em um servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="3eedd-125">From a user account that is a member of the RTCUniversalServerAdmins group, log on to a Front End Server.</span></span>

8.  <span data-ttu-id="3eedd-126">Use o construtor de topologias para instalar o banco de dados espelho.</span><span class="sxs-lookup"><span data-stu-id="3eedd-126">Use Topology Builder to install the mirror database.</span></span> <span data-ttu-id="3eedd-127">Faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3eedd-127">Perform the following:</span></span>
    
      - <span data-ttu-id="3eedd-128">Iniciar o construtor de topologias: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Construtor de topologias do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="3eedd-128">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
      - <span data-ttu-id="3eedd-129">Clique com o botão direito do mouse no nó do Lync Server 2013, clique em **topologia** e clique em **instalar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="3eedd-129">Right-click the Lync Server 2013 node, click **Topology**, and then click **Install Database**.</span></span>
    
      - <span data-ttu-id="3eedd-130">Siga o assistente de **instalação de banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="3eedd-130">Follow the **Install Database** wizard.</span></span> <span data-ttu-id="3eedd-131">Na página **criar bancos de dados** , selecione os bancos de dados que você deseja recriar.</span><span class="sxs-lookup"><span data-stu-id="3eedd-131">On the **Create databases** page, select the databases that you want to recreate.</span></span>
    
      - <span data-ttu-id="3eedd-132">Siga o assistente até que o prompt **criar banco de dados espelho** seja exibido.</span><span class="sxs-lookup"><span data-stu-id="3eedd-132">Follow the wizard until a prompt of **Create Mirror Database** appears.</span></span> <span data-ttu-id="3eedd-133">Selecione o banco de dados que você deseja instalar e conclua esse processo.</span><span class="sxs-lookup"><span data-stu-id="3eedd-133">Select the database that you want to install and complete this process.</span></span>
        
        <div>
        

        > [!TIP]
        > <span data-ttu-id="3eedd-134">Em vez de executar o construtor de topologias, você pode usar o cmdlet <STRONG>install-CsMirrorDatabase</STRONG> para configurar o espelhamento.</span><span class="sxs-lookup"><span data-stu-id="3eedd-134">Instead of running Topology Builder, you can use the <STRONG>Install-CsMirrorDatabase</STRONG> cmdlet to configure mirroring.</span></span> <span data-ttu-id="3eedd-135">Para obter detalhes, consulte a documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3eedd-135">For details, see the Lync Server Management Shell documentation.</span></span>

        
        <span data-ttu-id="3eedd-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3eedd-136"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

