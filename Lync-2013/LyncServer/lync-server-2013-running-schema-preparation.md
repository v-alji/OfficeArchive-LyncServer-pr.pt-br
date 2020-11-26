---
title: 'Lync Server 2013: Executando preparação de esquema'
description: 'Lync Server 2013: executando a preparação do esquema.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running schema preparation
ms:assetid: 9d02bdb1-ff29-417a-bcce-b068b31207d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412729(v=OCS.15)
ms:contentKeyID: 48184911
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0991bbff7f54f8b8b9eb01fc87f752e00f3dcbfd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442191"
---
# <a name="running-active-directory-schema-preparation-in-lync-server-2013"></a><span data-ttu-id="8fe43-103">Executando preparação de esquema de Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8fe43-103">Running Active Directory schema preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8fe43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8fe43-104">

<span> </span></span></span>

<span data-ttu-id="8fe43-105">_**Tópico da última modificação:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="8fe43-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="8fe43-106">Você pode usar os cmdlets do Shell de gerenciamento do Lync Server e do setup para preparar o esquema do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8fe43-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the Active Directory schema.</span></span> <span data-ttu-id="8fe43-107">O cmdlet que estende o esquema do Active Directory é **install-CsAdServerSchema**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-107">The cmdlet that extends the Active Directory schema is **Install-CsAdServerSchema**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8fe43-108">O cmdlet de preparação do esquema (<STRONG>install-CsAdServerSchema</STRONG>) deve acessar o mestre de esquema, que requer que o serviço do registro remoto esteja em execução e que a chave do registro remoto esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="8fe43-108">The schema preparation cmdlet (<STRONG>Install-CsAdServerSchema</STRONG>) must access the schema master, which requires that the remote registry service is running and that the remote registry key is enabled.</span></span> <span data-ttu-id="8fe43-109">Se o serviço de registro remoto não puder ser habilitado no mestre de esquema, você poderá executar o cmdlet localmente no mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="8fe43-109">If the remote registry service cannot be enabled on the schema master, you can run the cmdlet locally on the schema master.</span></span> <span data-ttu-id="8fe43-110">Para obter detalhes sobre o acesso remoto ao registro, consulte o artigo 314837 da base de dados de conhecimento Microsoft, "como gerenciar o acesso remoto ao registro" <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A> .</span><span class="sxs-lookup"><span data-stu-id="8fe43-110">For details about registry remote access, see Microsoft Knowledge Base article 314837, "How to Manage Remote Access to the Registry," at <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A>.</span></span>



</div>

<span data-ttu-id="8fe43-111">Depois de concluir a preparação do esquema, verifique manualmente se a partição do esquema foi replicada antes de prosseguir com a preparação da floresta.</span><span class="sxs-lookup"><span data-stu-id="8fe43-111">After you complete schema preparation, manually verify that the schema partition has been replicated before proceeding to forest preparation.</span></span> <span data-ttu-id="8fe43-112">Para obter detalhes, consulte [verificando a replicação de esquema do Active Directory no Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="8fe43-112">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="8fe43-113">Para usar a instalação para preparar o esquema da floresta atual</span><span class="sxs-lookup"><span data-stu-id="8fe43-113">To use Setup to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="8fe43-114">Faça logon em um servidor na sua floresta como membro do grupo Administradores de esquemas e com direitos de administrador no mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="8fe43-114">Log on to a server in your forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="8fe43-115">Na pasta de instalação ou mídia do Lync Server 2013, execute Setup.exe para iniciar o assistente de implantação.</span><span class="sxs-lookup"><span data-stu-id="8fe43-115">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="8fe43-116">Se você for solicitado a instalar o Microsoft Visual C++ Redistributable, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-116">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>

4.  <span data-ttu-id="8fe43-117">A caixa de diálogo instalação do Lync Server 2013 solicita um local para instalar os arquivos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8fe43-117">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="8fe43-118">Escolha o local padrão ou **navegue** até um local de sua escolha e clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-118">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>

5.  <span data-ttu-id="8fe43-119">Na página contrato de licença, marque **a opção aceito os termos do contrato de licença** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-119">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span>

6.  <span data-ttu-id="8fe43-120">O instalador instala os componentes principais do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8fe43-120">The installer installs the Lync Server Core Components.</span></span>

7.  <span data-ttu-id="8fe43-121">Quando o assistente de implantação estiver pronto, clique em **preparar o Active Directory** e aguarde o estado de implantação ser determinado.</span><span class="sxs-lookup"><span data-stu-id="8fe43-121">When the Deployment Wizard is ready, click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

8.  <span data-ttu-id="8fe43-122">Na **etapa 1: preparar o esquema**, clique em **executar**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-122">At **Step 1: Prepare Schema**, click **Run**.</span></span>

9.  <span data-ttu-id="8fe43-123">Na página **preparar esquema** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-123">On the **Prepare Schema** page, click **Next**.</span></span>

10. <span data-ttu-id="8fe43-124">Na página **Executando Comandos**, procure por **Status da tarefa: Concluída** e clique em **Exibir Log**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-124">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

11. <span data-ttu-id="8fe43-125">Na coluna **Action (ação** ), expanda **Schema prep**, procure o **\<Success\>** resultado de execução no final de cada tarefa para verificar se a preparação do esquema foi concluída com êxito, feche o log e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-125">Under the **Action** column, expand **Schema Prep**, look for the **\<Success\>** Execution Result at the end of each task to verify that schema preparation completed successfully, close the log, and then click **Finish**.</span></span>

12. <span data-ttu-id="8fe43-126">Aguarde a conclusão da replicação do Active Directory ou force a replicação.</span><span class="sxs-lookup"><span data-stu-id="8fe43-126">Wait for Active Directory replication to complete or force replication.</span></span>

13. <span data-ttu-id="8fe43-127">Verifique manualmente se as alterações de esquema foram duplicadas para todos os outros controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="8fe43-127">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="8fe43-128">Para obter detalhes, consulte [verificando a replicação de esquema do Active Directory no Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="8fe43-128">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="8fe43-129">Usar cmdlets para preparar o esquema da floresta atual</span><span class="sxs-lookup"><span data-stu-id="8fe43-129">To use cmdlets to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="8fe43-130">Faça logon em um computador na floresta como membro do grupo Administradores de esquemas e com direitos de administrador no mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="8fe43-130">Log on to a computer in the forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="8fe43-131">Instale os componentes principais do Lync Server da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8fe43-131">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="8fe43-132">Na pasta de instalação ou mídia do Lync Server 2013, execute Setup.exe para iniciar o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8fe43-132">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="8fe43-133">Se você for solicitado a instalar o Microsoft Visual C++ Redistributable, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-133">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="8fe43-134">A caixa de diálogo instalação do Lync Server 2013 solicita um local para instalar os arquivos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8fe43-134">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="8fe43-135">Escolha o local padrão ou **navegue** até um local de sua escolha e clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-135">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="8fe43-136">Na página contrato de licença, marque **a opção aceito os termos do contrato de licença** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-136">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="8fe43-137">O instalador instala os componentes principais do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8fe43-137">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="8fe43-138">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8fe43-138">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="8fe43-139">Execute:</span><span class="sxs-lookup"><span data-stu-id="8fe43-139">Run:</span></span>
    
        Install-CsAdServerSchema [-Ldf <directory where the .ldf file is located>] 
    
    <span data-ttu-id="8fe43-140">Se você não especificar o parâmetro ldf, o valor padrão será o caminho de instalação do Lync Server 2013 lido do registro.</span><span class="sxs-lookup"><span data-stu-id="8fe43-140">If you do not specify the Ldf parameter, the default value is the Lync Server 2013 installation path that is read from the registry.</span></span>
    
    <span data-ttu-id="8fe43-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8fe43-141">For example:</span></span>
    
        Install-CsAdServerSchema -Ldf "C:\Program Files\Microsoft Lync Server 2013\Deployment\Setup"

5.  <span data-ttu-id="8fe43-142">Use o cmdlet a seguir para verificar se a conclusão da preparação do esquema foi concluída.</span><span class="sxs-lookup"><span data-stu-id="8fe43-142">Use the following cmdlet to verify that schema preparation ran to completion.</span></span>
    
        Get-CsAdServerSchema 
    
    <span data-ttu-id="8fe43-143">Esse cmdlet retorna um valor de **estado de versão do esquema \_ \_ \_ atual** se a preparação do esquema foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8fe43-143">This cmdlet returns a value of **SCHEMA\_VERSION\_STATE\_CURRENT** if schema preparation was successful.</span></span>

6.  <span data-ttu-id="8fe43-144">Aguarde a conclusão da replicação do Active Directory ou force a replicação.</span><span class="sxs-lookup"><span data-stu-id="8fe43-144">Wait for Active Directory replication to complete or force replication.</span></span>

7.  <span data-ttu-id="8fe43-145">Verifique manualmente se as alterações de esquema foram duplicadas para todos os outros controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="8fe43-145">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="8fe43-146">Para obter detalhes, consulte [verificando a replicação de esquema do Active Directory no Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="8fe43-146">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8fe43-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fe43-147">See Also</span></span>


[<span data-ttu-id="8fe43-148">Verificando a replicação de esquema do Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8fe43-148">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)  


[<span data-ttu-id="8fe43-149">Preparando o esquema do Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8fe43-149">Preparing the Active Directory schema in Lync Server 2013</span></span>](lync-server-2013-preparing-the-active-directory-schema.md)  
  

<span data-ttu-id="8fe43-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8fe43-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

