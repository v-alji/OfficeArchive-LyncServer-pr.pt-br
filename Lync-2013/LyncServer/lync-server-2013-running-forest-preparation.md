---
title: 'Lync Server 2013: Executando preparação de floresta'
description: 'Lync Server 2013: executando a preparação da floresta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running forest preparation
ms:assetid: 9d62f7be-bcfe-421d-8d8a-225567102a35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412732(v=OCS.15)
ms:contentKeyID: 48184991
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad3ef2d7583d541701d6606946ca1df1bbd8cf23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442212"
---
# <a name="running-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="62255-103">Executando preparação de floresta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62255-103">Running forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="62255-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="62255-104">

<span> </span></span></span>

<span data-ttu-id="62255-105">_**Tópico da última modificação:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="62255-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="62255-106">Você pode usar os cmdlets do Shell de gerenciamento do Lync Server e do setup para preparar a floresta.</span><span class="sxs-lookup"><span data-stu-id="62255-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the forest.</span></span> <span data-ttu-id="62255-107">O cmdlet que prepara a floresta é **Enable-CsAdForest**.</span><span class="sxs-lookup"><span data-stu-id="62255-107">The cmdlet that prepares the forest is **Enable-CsAdForest**.</span></span>

<span data-ttu-id="62255-108">Depois de preparar a floresta, você deve verificar se as configurações globais foram duplicadas antes de executar a preparação do domínio.</span><span class="sxs-lookup"><span data-stu-id="62255-108">After you prepare the forest, you must verify that global settings have been replicated before running domain preparation.</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-forest"></a><span data-ttu-id="62255-109">Para usar a instalação para preparar a floresta</span><span class="sxs-lookup"><span data-stu-id="62255-109">To use Setup to prepare the forest</span></span>

1.  <span data-ttu-id="62255-110">Faça logon em um computador que esteja associado a um domínio como membro do grupo Administradores de empresa do domínio raiz da floresta.</span><span class="sxs-lookup"><span data-stu-id="62255-110">Log on to a computer that is joined to a domain as a member of the Enterprise Admins group for the forest root domain.</span></span>

2.  <span data-ttu-id="62255-111">Na pasta de instalação ou mídia do Lync Server 2013, execute Setup.exe para iniciar o assistente de implantação.</span><span class="sxs-lookup"><span data-stu-id="62255-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="62255-112">Clique em **Preparar o Active Directory** e espere que o estado da implantação seja determinado.</span><span class="sxs-lookup"><span data-stu-id="62255-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="62255-113">Na **etapa 3: preparar a floresta atual**, clique em **executar**.</span><span class="sxs-lookup"><span data-stu-id="62255-113">At **Step 3: Prepare Current Forest**, click **Run**.</span></span>

5.  <span data-ttu-id="62255-114">Na página **preparar floresta** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="62255-114">On the **Prepare Forest** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="62255-115">A preparação da floresta permite que você escolha onde colocar os grupos universais do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62255-115">Forest Preparation allows you to choose where to place the Universal Groups for Lync Server 2013.</span></span> <span data-ttu-id="62255-116">Escolha um local que atenda aos requisitos de sua organização.</span><span class="sxs-lookup"><span data-stu-id="62255-116">Choose a location that is consistent with the requirements of your organization.</span></span>

    
    </div>

6.  <span data-ttu-id="62255-117">Na página **Executando Comandos**, procure por **Status da tarefa: Concluída** e clique em **Exibir Log**.</span><span class="sxs-lookup"><span data-stu-id="62255-117">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="62255-118">Na coluna **Action (ação** ), expanda **Forest prep**, procure um **\<Success\>** resultado de execução no final de cada tarefa para verificar se a preparação da floresta foi concluída com êxito, feche o log e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="62255-118">Under the **Action** column, expand **Forest Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that forest preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="62255-119">Aguarde a conclusão da replicação do Active Directory ou force a replicação para todos os controladores de domínio listados no snap-in **sites e serviços do Active Directory** para o controlador de domínio raiz da floresta, antes de executar a preparação do domínio.</span><span class="sxs-lookup"><span data-stu-id="62255-119">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span> <span data-ttu-id="62255-120">Force a replicação entre os controladores de domínio em todos os sites do Active Directory para fazer com que a replicação dentro dos sites ocorra em minutos.</span><span class="sxs-lookup"><span data-stu-id="62255-120">Force replication between the domain controllers in all Active Directory sites to cause replication within the sites to occur within minutes.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-forest"></a><span data-ttu-id="62255-121">Para usar cmdlets para preparar a floresta</span><span class="sxs-lookup"><span data-stu-id="62255-121">To use cmdlets to prepare the forest</span></span>

1.  <span data-ttu-id="62255-122">Faça logon em um computador que esteja associado a um domínio como membro do grupo Domain admins no domínio raiz da floresta.</span><span class="sxs-lookup"><span data-stu-id="62255-122">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="62255-123">Instale os componentes principais do Lync Server da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="62255-123">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="62255-124">Na pasta de instalação ou mídia do Lync Server 2013, execute Setup.exe para iniciar o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62255-124">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="62255-125">Se você for solicitado a instalar o Microsoft Visual C++ Redistributable, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="62255-125">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="62255-126">A caixa de diálogo instalação do Lync Server 2013 solicita um local para instalar os arquivos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62255-126">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="62255-127">Escolha o local padrão ou **navegue** até um local de sua escolha e clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="62255-127">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="62255-128">Na página contrato de licença, marque **a opção aceito os termos do contrato de licença** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="62255-128">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="62255-129">O instalador instala os componentes principais do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62255-129">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="62255-130">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="62255-130">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="62255-131">Execute:</span><span class="sxs-lookup"><span data-stu-id="62255-131">Run:</span></span>
    
        Enable-CsAdForest [-GroupDomain <FQDN of the domain in which to create the universal groups>]
    
    <span data-ttu-id="62255-132">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="62255-132">For example:</span></span>
    
        Enable-CsAdForest -GroupDomain domain1.contoso.com 
    
    <span data-ttu-id="62255-133">Se você não especificar o parâmetro GroupDomain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="62255-133">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span> <span data-ttu-id="62255-134">Se grupos universais foram criados anteriormente em um domínio que não seja o domínio padrão, você deve especificar o parâmetro GroupDomain explicitamente.</span><span class="sxs-lookup"><span data-stu-id="62255-134">If universal groups were created previously in a domain that is not the default domain, you must specify the GroupDomain parameter explicitly.</span></span>

5.  <span data-ttu-id="62255-135">Aguarde a conclusão da replicação do Active Directory ou force a replicação para todos os controladores de domínio listados no snap-in **sites e serviços do Active Directory** para o controlador de domínio raiz da floresta, antes de executar a preparação do domínio.</span><span class="sxs-lookup"><span data-stu-id="62255-135">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span>

6.  <span data-ttu-id="62255-136">Verifique se a preparação da floresta foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="62255-136">Verify that forest preparation was successful.</span></span> <span data-ttu-id="62255-137">Execute:</span><span class="sxs-lookup"><span data-stu-id="62255-137">Run:</span></span>
    
        Get-CsAdForest 
    
    <span data-ttu-id="62255-138">Esse cmdlet retorna um valor do **\_ estado FORESTSETTINGS da LC \_ \_ pronto** se a preparação da floresta tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="62255-138">This cmdlet returns a value of **LC\_FORESTSETTINGS\_STATE\_READY** if forest preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="62255-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="62255-139">See Also</span></span>


[<span data-ttu-id="62255-140">Usando cmdlets para reverter preparação da floresta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62255-140">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)  


[<span data-ttu-id="62255-141">Preparando a floresta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62255-141">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="62255-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="62255-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

