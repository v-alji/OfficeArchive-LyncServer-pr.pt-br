---
title: 'Lync Server 2013: Configurando opções de arquivamento para um site'
description: 'Lync Server 2013: Configurando opções de arquivamento para um site.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options for a site
ms:assetid: 59b48fd9-d5fc-40b4-abae-e9cf89ee5573
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204930(v=OCS.15)
ms:contentKeyID: 48184247
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2db164d7c4c1cdda158387be62c0eb535fac662f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433324"
---
# <a name="configuring-archiving-options-for-a-site-in-lync-server-2013"></a><span data-ttu-id="e117e-103">Configurando opções de arquivamento para um site no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e117e-103">Configuring Archiving options for a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e117e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e117e-104">

<span> </span></span></span>

<span data-ttu-id="e117e-105">_**Tópico da última modificação:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="e117e-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="e117e-106">Você pode especificar opções de arquivamento a serem aplicadas a sites específicos criando e Configurando opções em uma configuração de arquivamento para cada um desses sites.</span><span class="sxs-lookup"><span data-stu-id="e117e-106">You can specify Archiving options to be applied to specific sites by creating and configuring options in an Archiving configuration for each of those sites.</span></span> <span data-ttu-id="e117e-107">Uma configuração de site substitui a configuração global, mas só se aplica ao site específico definido na configuração de site.</span><span class="sxs-lookup"><span data-stu-id="e117e-107">A site configuration overrides the global configuration, but only for the site specified in the site configuration.</span></span> <span data-ttu-id="e117e-108">Configurações de pool substituir configurações de site</span><span class="sxs-lookup"><span data-stu-id="e117e-108">Pool configurations override site configurations</span></span>

<span data-ttu-id="e117e-109">Para obter detalhes sobre como funcionam as configurações de arquivamento, incluindo a hierarquia para configurações globais, de site e de pool, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="e117e-109">For details about how Archiving configurations work, including the hierarchy for global, site, and pool configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e117e-110">Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento.</span><span class="sxs-lookup"><span data-stu-id="e117e-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e117e-111">Para habilitar o arquivamento, você deve especificar políticas de arquivamento para controlar o arquivamento de comunicações externas e internas ao nível global e, caso seja apropriado, nos níveis de site e usuário.</span><span class="sxs-lookup"><span data-stu-id="e117e-111">To enable archiving, you must specify archiving policies to control the archiving of internal and external communications at the global level and, if appropriate, at site and user levels.</span></span> <span data-ttu-id="e117e-112">Caso configure políticas de nível de usuário, você também deve atribuir as políticas de usuários para usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="e117e-112">If you configure user-level policies, you must also assign the user policies to specific users.</span></span> <span data-ttu-id="e117e-113">Para obter detalhes sobre como criar e configurar as políticas de arquivamento, consulte <A href="lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md">Gerenciando o arquivamento de comunicações internas e externas no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="e117e-113">For details about creating and configuring archiving policies, see <A href="lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md">Managing the Archiving of internal and external communications in Lync Server 2013</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-configure-archiving-options-at-the-site-level"></a><span data-ttu-id="e117e-114">Para configurar as opções de arquivamento no nível do site</span><span class="sxs-lookup"><span data-stu-id="e117e-114">To configure archiving options at the site level</span></span>

1.  <span data-ttu-id="e117e-115">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="e117e-115">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e117e-116">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e117e-116">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="e117e-117">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server 2013, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e117e-117">For details about the different methods you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e117e-118">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Configuração de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="e117e-118">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="e117e-119">Na página **Configuração do Arquivamento**, clique em **Nova** e depois em **Configuração do site**.</span><span class="sxs-lookup"><span data-stu-id="e117e-119">On the **Archiving Configuration** page, click **New**, and then click **Site Configuration**.</span></span>

5.  <span data-ttu-id="e117e-120">Em **Selecionar um Site**, selecione o site a ser configurado para arquivamento.</span><span class="sxs-lookup"><span data-stu-id="e117e-120">In **Select a Site**, select the site to be configured for archiving.</span></span>

6.  <span data-ttu-id="e117e-121">Em **Nova configuração de arquivamento**, na caixa de lista suspensa **Configuração de arquivamento**, execute uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="e117e-121">In **New Archiving Setting**, in the **Archiving setting** drop-down list box, do one of the following:</span></span>
    
      - <span data-ttu-id="e117e-122">Para habilitar o arquivamento apenas para sessões de IM, clique em **Arquivar sessões de IM**.</span><span class="sxs-lookup"><span data-stu-id="e117e-122">To enable archiving only for instant messaging (IM) sessions, click **Archive IM sessions**.</span></span>
    
      - <span data-ttu-id="e117e-123">Para habilitar o arquivamento para sessões de IM e conferências, clique em **Arquivar sessões de IM e webconferência**.</span><span class="sxs-lookup"><span data-stu-id="e117e-123">To enable archiving for both IM sessions and conferences, click **Archive IM and web conferencing sessions**.</span></span>
    
      - <span data-ttu-id="e117e-124">Para desabilitar o arquivamento da política, clique em **Desabilitar arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="e117e-124">To disable archiving for the policy, click **Disable archiving**.</span></span>

7.  <span data-ttu-id="e117e-125">Também em **Nova configuração de arquivamento**, execute uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="e117e-125">Also in **New Archiving Setting**, do the following:</span></span>
    
      - <span data-ttu-id="e117e-126">Para bloquear a atividade quando o arquivamento não estiver disponível, marque a caixa de seleção **Bloquear sessões de mensagem instantânea ou webconferência se o arquivamento falhar**.</span><span class="sxs-lookup"><span data-stu-id="e117e-126">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="e117e-127">Para usar o Microsoft Exchange Server para armazenar dados de arquivamento, clique na caixa de seleção **integração do Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="e117e-127">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="e117e-128">Para habilitar a exclusão de dados, marque a caixa de seleção **Habilitar exclusão dos dados de arquivamento** e execute uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="e117e-128">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="e117e-129">Para especificar a exclusão após um número específico de dias, clique em **Excluir dados de arquivamento exportados e dados de arquivamento armazenados após uma duração máxima (dias)** e especifique o número de dias.</span><span class="sxs-lookup"><span data-stu-id="e117e-129">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="e117e-130">Para limitar a exclusão de dados de arquivamento que foram exportados, clique em **Excluir apenas dados de arquivamento exportados**.</span><span class="sxs-lookup"><span data-stu-id="e117e-130">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

8.  <span data-ttu-id="e117e-131">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="e117e-131">Click **Commit**.</span></span>

<span data-ttu-id="e117e-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e117e-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

