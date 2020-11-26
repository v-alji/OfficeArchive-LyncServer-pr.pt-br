---
title: Mesclar usando o assistente de mesclagem do construtor de topologia
description: Mesclar usando o assistente de mesclagem do construtor de topologias.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Merge using Topology Builder Merge wizard
ms:assetid: c3f3c425-dab6-4dcd-bf0e-d7fde05f2ebf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205243(v=OCS.15)
ms:contentKeyID: 48185343
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d71a63eef95e3e36802dedfa9fbc1a173d283b65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446929"
---
# <a name="merge-using-topology-builder-merge-wizard"></a><span data-ttu-id="d5639-103">Mesclar usando o assistente de mesclagem do construtor de topologia</span><span class="sxs-lookup"><span data-stu-id="d5639-103">Merge using Topology Builder Merge wizard</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5639-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5639-104">

<span> </span></span></span>

<span data-ttu-id="d5639-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d5639-105">_**Topic Last Modified:** 2012-10-02_</span></span>

1.  <span data-ttu-id="d5639-106">Baixe a implantação existente usando o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="d5639-106">Download the existing deployment using Topology Builder.</span></span>

2.  <span data-ttu-id="d5639-107">No menu **ação** , selecione **mesclar o Office communications Server 2007 R2**.</span><span class="sxs-lookup"><span data-stu-id="d5639-107">From the **Action** menu, select **Merge Office Communications Server 2007 R2**.</span></span>

3.  <span data-ttu-id="d5639-108">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="d5639-108">Click **Next**.</span></span>

4.  <span data-ttu-id="d5639-109">Em **especificar a configuração de borda**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="d5639-109">In **Specify Edge Setup**, click **Add**.</span></span>
    
    <span data-ttu-id="d5639-110">![Assistente de topologia de mesclagem, especificar a página de configuração de borda](images/JJ205243.cdca609d-d4d5-47d9-9ff8-8b1daa4106e1(OCS.15).jpg "Assistente de topologia de mesclagem, especificar a página de configuração de borda")</span><span class="sxs-lookup"><span data-stu-id="d5639-110">![Merge Topology Wizard, Specify Edge Setup page](images/JJ205243.cdca609d-d4d5-47d9-9ff8-8b1daa4106e1(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="d5639-111">Em **especificar tipo de borda**, insira o tipo de configuração do servidor de borda e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d5639-111">In **Specify Edge Type**, enter the type of Edge Server configuration, and then click **Next**.</span></span> <span data-ttu-id="d5639-112">Este exemplo usa a opção **servidor de borda única** .</span><span class="sxs-lookup"><span data-stu-id="d5639-112">This example uses the **Single Edge Server** option.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d5639-113">A <STRONG>implantação de borda expandida</STRONG> não é uma configuração com suporte.</span><span class="sxs-lookup"><span data-stu-id="d5639-113"><STRONG>Expanded Edge deployment</STRONG> is not a supported configuration.</span></span> <span data-ttu-id="d5639-114">Um <STRONG>servidor de borda expandida</STRONG> deve primeiro ser convertido em um <STRONG>servidor de borda único</STRONG> ou em um servidor de <STRONG>borda consolidada com balanceamento de carga</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="d5639-114">An <STRONG>Expanded Edge Server</STRONG> must first be converted to a <STRONG>Single Edge Server</STRONG> or a <STRONG>Load-balanced consolidated Edge</STRONG> Server.</span></span>

    
    </div>

6.  <span data-ttu-id="d5639-115">Em **especificar as configurações de borda interna** , insira as informações relevantes para o FQDN e as portas internas do seu pool de bordas, conforme necessário, e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d5639-115">In **Specify Internal Edge Settings** , enter the relevant information for your Edge pool’s internal FQDN and ports as needed, and then click **Next**.</span></span>
    
    <span data-ttu-id="d5639-116">![Especificar a caixa de diálogo Configurações de borda interna](images/JJ205243.dd664761-839c-4ac8-bd1a-5525589dfbb0(OCS.15).jpg "Especificar a caixa de diálogo Configurações de borda interna")</span><span class="sxs-lookup"><span data-stu-id="d5639-116">![Specify Internal Edge Settings dialog](images/JJ205243.dd664761-839c-4ac8-bd1a-5525589dfbb0(OCS.15).jpg "Specify Internal Edge Settings dialog")</span></span>  

7.  <span data-ttu-id="d5639-117">Em **especificar borda externa**, insira as informações de FQDN do servidor de Webconferência para o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="d5639-117">In **Specify External Edge**, enter the web conferencing FQDN information for your Edge Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d5639-118">Antes de clicar em <STRONG>Avançar</STRONG>, siga o próximo passo deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="d5639-118">Before you click <STRONG>Next</STRONG>, do the next step in this procedure.</span></span> <span data-ttu-id="d5639-119">É muito importante que você não perca esta etapa.</span><span class="sxs-lookup"><span data-stu-id="d5639-119">It is very important that you do not miss this step.</span></span>

    
    </div>

8.  <span data-ttu-id="d5639-120">Marque a caixa de seleção **este pool de bordas é usado para a Federação e conectividade de mensagem de chat pública** se você planeja usar o servidor de borda herdado do Office Communications Server 2007 R2 para Federação.</span><span class="sxs-lookup"><span data-stu-id="d5639-120">Check the **This Edge pool is used for federation and public IM connectivity** check box if you plan to use the legacy Office Communications Server 2007 R2 Edge Server for federation.</span></span> <span data-ttu-id="d5639-121">Se você tiver vários servidores de Borda implantados, apenas um deles será habilitado para Federação.</span><span class="sxs-lookup"><span data-stu-id="d5639-121">If you have multiple Edge Servers deployed, only one of them will be enabled for federation.</span></span> <span data-ttu-id="d5639-122">Se você não marcar esta caixa e decidir mais tarde que deseja habilitar a Federação, execute o assistente de mesclagem do construtor de topologias e publique sua topologia novamente.</span><span class="sxs-lookup"><span data-stu-id="d5639-122">If you do not check this box and you decide later that you want to enable federation, you must run the Topology Builder Merge wizard and publish your topology again.</span></span>
    
    <span data-ttu-id="d5639-123">![Caixa de diálogo servidor de borda, especificar a página de borda externa](images/JJ205243.32e97ce5-92f0-477e-8125-5d2ece237b13(OCS.15).jpg "Caixa de diálogo servidor de borda, especificar a página de borda externa")</span><span class="sxs-lookup"><span data-stu-id="d5639-123">![Edge Server dialog, Specify External Edge page](images/JJ205243.32e97ce5-92f0-477e-8125-5d2ece237b13(OCS.15).jpg "Edge Server dialog, Specify External Edge page")</span></span>  

9.  <span data-ttu-id="d5639-124">Em **especificar próximo salto**, digite o nome de domínio totalmente qualificado (FQDN) do próximo local do salto em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="d5639-124">In **Specify Next Hop**, enter the fully qualified domain name (FQDN) of the next hop location in your environment.</span></span> <span data-ttu-id="d5639-125">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="d5639-125">Click **Finish**.</span></span>
    
    <span data-ttu-id="d5639-126">![Caixa de diálogo servidor de borda, especifique a página de próximo salto](images/JJ205243.e734ee0d-f91c-4f3f-8ae6-248ecabcf678(OCS.15).jpg "Caixa de diálogo servidor de borda, especifique a página de próximo salto")</span><span class="sxs-lookup"><span data-stu-id="d5639-126">![Edge Server dialog, Specify Next Hop page](images/JJ205243.e734ee0d-f91c-4f3f-8ae6-248ecabcf678(OCS.15).jpg "Edge Server dialog, Specify Next Hop page")</span></span>  

10. <span data-ttu-id="d5639-127">Em **especificar a configuração de borda**, se todos os seus servidores do Office Communications Server 2007 R2 Edge tiverem sido adicionados, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d5639-127">In **Specify Edge Setup**, if all your Office Communications Server 2007 R2 Edge Servers have been added, click **Next**.</span></span> <span data-ttu-id="d5639-128">Se você tiver mais servidores do Office Communications Server 2007 R2 Edge para adicionar, repita esse procedimento começando na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="d5639-128">If you have more Office Communications Server 2007 R2 Edge Servers to add, repeat this procedure starting at step 4.</span></span>

11. <span data-ttu-id="d5639-129">Em **especificar porta SIP interna** , selecione a configuração padrão (ou seja, se você não tiver modificado a porta SIP padrão).</span><span class="sxs-lookup"><span data-stu-id="d5639-129">In **Specify Internal SIP port** , select the default setting (that is, if you did not modify the default SIP port).</span></span> <span data-ttu-id="d5639-130">Altere conforme apropriado se você não estiver usando uma porta padrão do 5061 e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d5639-130">Change as appropriate if you are not using a default port of 5061, and then click **Next**.</span></span>

12. <span data-ttu-id="d5639-131">Em **Resumo**, clique em **Avançar** para começar a mesclar as topologias.</span><span class="sxs-lookup"><span data-stu-id="d5639-131">In **Summary**, click **Next** to begin merging the topologies.</span></span>

13. <span data-ttu-id="d5639-132">A página do assistente verifica se a mesclagem das topologias foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d5639-132">The wizard page verifies that the merging of the topologies was successful.</span></span>

14. <span data-ttu-id="d5639-133">Na coluna **status** , verifique se o valor é **êxito** e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="d5639-133">In the **Status** column, verify that the value is **Success**, and then click **Finish**.</span></span>

15. <span data-ttu-id="d5639-134">No painel esquerdo do construtor de topologias, agora você deve ver o **BackCompatSite**, que indica que o ambiente do Office Communications Server 2007 R2 foi mesclado com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d5639-134">In the left pane of Topology Builder, you should now see the **BackCompatSite**, which indicates that your Office Communications Server 2007 R2 environment has been merged with Lync Server 2013.</span></span>
    
    <span data-ttu-id="d5639-135">![Construtor de topologias mostrando uma topologia mesclada](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Construtor de topologias mostrando uma topologia mesclada")</span><span class="sxs-lookup"><span data-stu-id="d5639-135">![Topology Builder showing a merged topology](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder showing a merged topology")</span></span>  

16. <span data-ttu-id="d5639-136">No menu **ação** , clique em **publicar topologia** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d5639-136">From the **Action** menu, click **Publish Topology**, and then click **Next**.</span></span>

17. <span data-ttu-id="d5639-137">Quando o **Assistente de publicação** for concluído, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="d5639-137">When the **Publishing wizard** completes, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d5639-138">É importante que você conclua o próximo tópico, <A href="import-policies-and-settings.md">importar políticas e configurações</A>, para garantir que as configurações de política herdadas sejam importadas para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d5639-138">It’s important that you complete the next topic, <A href="import-policies-and-settings.md">Import policies and settings</A>, to ensure that the legacy policy settings are imported into Lync Server 2013.</span></span>

    
    <span data-ttu-id="d5639-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5639-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

