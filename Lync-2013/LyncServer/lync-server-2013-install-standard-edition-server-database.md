---
title: 'Lync Server 2013: Instalar o banco de dados do servidor Standard Edition'
description: 'Lync Server 2013: Instale o banco de dados do servidor Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Standard Edition server database
ms:assetid: 0bd3a804-aad6-48cb-981b-54725af032db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398167(v=OCS.15)
ms:contentKeyID: 48183385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a20d2c01de94ad88960555db78c57c6b79d92f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427149"
---
# <a name="install-standard-edition-server-database-for-lync-server-2013"></a><span data-ttu-id="8f837-103">Instalar o banco de dados do servidor Standard Edition para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f837-103">Install Standard Edition server database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f837-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f837-104">

<span> </span></span></span>

<span data-ttu-id="8f837-105">_**Tópico da última modificação:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="8f837-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="8f837-106">Configurar um servidor Standard Edition como o único servidor na sua infraestrutura que os usuários de casas, que diferem de outras instalações de servidor, há uma seleção no **Assistente de implantação** especificamente para configurar o servidor inicial.</span><span class="sxs-lookup"><span data-stu-id="8f837-106">Setting up a Standard Edition server as the only server in your infrastructure that homes users differs from other server installations in that there is a selection in the **Deployment Wizard** specifically for setting up the initial server.</span></span>

<div>

## <a name="to-install-a-standard-edition-server"></a><span data-ttu-id="8f837-107">Para instalar um servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="8f837-107">To install a Standard Edition server</span></span>

1.  <span data-ttu-id="8f837-108">Faça logon no servidor no qual você vai instalar o servidor Standard Edition como administrador local ou um equivalente a um domínio.</span><span class="sxs-lookup"><span data-stu-id="8f837-108">Log on to the server where you are going to install Standard Edition server as a local administrator or a domain equivalent.</span></span>

2.  <span data-ttu-id="8f837-109">Se você não tiver preparado os serviços de domínio Active Directory, execute esses procedimentos primeiro.</span><span class="sxs-lookup"><span data-stu-id="8f837-109">If you have not prepared Active Directory Domain Services, then first perform those procedures.</span></span> <span data-ttu-id="8f837-110">Para obter detalhes, consulte [preparando os serviços de domínio Active Directory para o Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="8f837-110">For details, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

3.  <span data-ttu-id="8f837-111">No assistente de implantação do Lync Server, clique em **preparar primeiro servidor Standard Edition**.</span><span class="sxs-lookup"><span data-stu-id="8f837-111">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="8f837-112">Na página **preparar único servidor de edição padrão** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8f837-112">On the **Prepare single Standard Edition Server** page, click **Next**.</span></span>

5.  <span data-ttu-id="8f837-113">Na página **comandos em execução** , o SQL Server 2012 Express está instalado como o repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="8f837-113">On the **Executing Commands** page, the SQL Server 2012 Express is installed as the Central Management store.</span></span> <span data-ttu-id="8f837-114">Regras de firewall necessárias são criadas.</span><span class="sxs-lookup"><span data-stu-id="8f837-114">Necessary firewall rules are created.</span></span> <span data-ttu-id="8f837-115">Quando a instalação do banco de dados e do software de pré-requisito estiver concluída, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="8f837-115">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8f837-116">A instalação inicial pode levar algum tempo sem atualizações visíveis para a tela Resumo da saída do comando.</span><span class="sxs-lookup"><span data-stu-id="8f837-116">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="8f837-117">Isso se deve à instalação do SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="8f837-117">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="8f837-118">Se você precisar monitorar a instalação do banco de dados, use o Gerenciador de tarefas para monitorar a configuração.</span><span class="sxs-lookup"><span data-stu-id="8f837-118">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

6.  <span data-ttu-id="8f837-119">Na página do assistente de implantação do Lync Server, clique em **instalar Construtor de topologia** se você não tiver instalado as ferramentas administrativas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8f837-119">On the Lync Server Deployment Wizard page, click **Install Topology Builder** if you have not previously installed the administrative tools.</span></span> <span data-ttu-id="8f837-120">Para obter detalhes, consulte [instalar as ferramentas administrativas do Lync Server 2013](lync-server-2013-install-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8f837-120">For details, see [Install Lync Server 2013 administrative tools](lync-server-2013-install-lync-server-administrative-tools.md).</span></span>

7.  <span data-ttu-id="8f837-121">Confirme se há marcas de seleção verdes ao lado de "preparar o Active Directory", "preparar primeiro servidor de edição padrão" e "instalar Construtor de topologia".</span><span class="sxs-lookup"><span data-stu-id="8f837-121">Confirm that there are green check marks next to “Prepare Active Directory,” “Prepare first Standard Edition server,” and “Install Topology Builder.”</span></span>

<span data-ttu-id="8f837-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f837-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

