---
title: 'Lync Server 2013: Usando cmdlets para reverter preparação da floresta'
description: 'Lync Server 2013: usando cmdlets para reverter a preparação da floresta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse forest preparation
ms:assetid: f48c7eb3-ccb0-48e6-ac79-ab7c7062b9d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413024(v=OCS.15)
ms:contentKeyID: 48185822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: acac87bdaeb7e730f93401fa62ea2678a713bb8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439636"
---
# <a name="using-cmdlets-to-reverse-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="88809-103">Usando cmdlets para reverter preparação da floresta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88809-103">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88809-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88809-104">

<span> </span></span></span>

<span data-ttu-id="88809-105">_**Tópico da última modificação:** 2013-06-19_</span><span class="sxs-lookup"><span data-stu-id="88809-105">_**Topic Last Modified:** 2013-06-19_</span></span>

<span data-ttu-id="88809-106">Use o cmdlet **Disable-CsAdForest** para reverter a etapa de preparação da floresta.</span><span class="sxs-lookup"><span data-stu-id="88809-106">Use the **Disable-CsAdForest** cmdlet to reverse the forest preparation step.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="88809-107">Se você executar o cmdlet <STRONG>Disable-CsAdForest</STRONG> em um ambiente em que você também tenha uma versão anterior do Lync Server implantada, as configurações globais para a versão anterior também serão excluídas.</span><span class="sxs-lookup"><span data-stu-id="88809-107">If you run the <STRONG>Disable-CsAdForest</STRONG> cmdlet in an environment where you also have a previous version of Lync Server deployed, the global settings for the previous version will also be deleted.</span></span>



</div>

<div>

## <a name="to-use-cmdlets-to-reverse-forest-preparation"></a><span data-ttu-id="88809-108">Para usar cmdlets para reverter a preparação da floresta</span><span class="sxs-lookup"><span data-stu-id="88809-108">To use cmdlets to reverse forest preparation</span></span>

1.  <span data-ttu-id="88809-109">Faça logon em um computador que esteja associado a um domínio como membro do grupo Domain admins no domínio raiz da floresta.</span><span class="sxs-lookup"><span data-stu-id="88809-109">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="88809-110">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="88809-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="88809-111">Execute:</span><span class="sxs-lookup"><span data-stu-id="88809-111">Run:</span></span>
    
        Disable-CsAdForest [-Force] [-GroupDomain <FQDN of the domain in which universal groups were created>]
    
    <span data-ttu-id="88809-112">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="88809-112">For example:</span></span>
    
        Disable-CsAdForest -Force -GroupDomain contoso.net
    
    <span data-ttu-id="88809-113">O parâmetro Force especifica se deve forçar a execução da tarefa.</span><span class="sxs-lookup"><span data-stu-id="88809-113">The Force parameter specifies whether to force running the task.</span></span> <span data-ttu-id="88809-114">Se esse parâmetro não estiver presente, o comando não será executado se mesmo um domínio na floresta ainda estiver preparado para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88809-114">If this parameter is not present, the command will not run if even one domain in the forest is still prepared for Lync Server 2013.</span></span> <span data-ttu-id="88809-115">Se o parâmetro Force for especificado, a ação continuará independentemente do estado de outros domínios na floresta.</span><span class="sxs-lookup"><span data-stu-id="88809-115">If the Force parameter is specified, the action will continue regardless of the state of other domains in the forest.</span></span>
    
    <span data-ttu-id="88809-116">Se você não especificar o parâmetro GroupDomain, o valor padrão será o domínio local.</span><span class="sxs-lookup"><span data-stu-id="88809-116">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="88809-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="88809-117">See Also</span></span>


[<span data-ttu-id="88809-118">Executando preparação de floresta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88809-118">Running forest preparation for Lync Server 2013</span></span>](lync-server-2013-running-forest-preparation.md)  


[<span data-ttu-id="88809-119">Preparando a floresta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88809-119">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="88809-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88809-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

