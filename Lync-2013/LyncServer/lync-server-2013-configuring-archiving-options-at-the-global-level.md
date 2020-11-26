---
title: 'Lync Server 2013: Configurando opções de arquivamento no nível global'
description: 'Lync Server 2013: Configurando opções de arquivamento no nível global.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options at the global level
ms:assetid: bfe415f7-2abf-41ee-a1cb-cf48b2d59c0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205233(v=OCS.15)
ms:contentKeyID: 48185303
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44b8939ec95d00afa2aa7632f4555bc6fef89834
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433336"
---
# <a name="configuring-archiving-options-at-the-global-level-in-lync-server-2013"></a><span data-ttu-id="4faf1-103">Configuração de opções de arquivamento no nível global do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4faf1-103">Configuring Archiving options at the global level in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4faf1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4faf1-104">

<span> </span></span></span>

<span data-ttu-id="4faf1-105">_**Tópico da última modificação:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="4faf1-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="4faf1-106">Quando você adiciona o arquivamento à sua topologia e publica a topologia, o Lync Server cria uma configuração global para arquivamento.</span><span class="sxs-lookup"><span data-stu-id="4faf1-106">When you add Archiving to your topology and publish the topology, Lync Server creates a global configuration for Archiving.</span></span> <span data-ttu-id="4faf1-107">Por padrão, nenhuma opção de arquivamento está habilitada na configuração global.</span><span class="sxs-lookup"><span data-stu-id="4faf1-107">By default, no Archiving options are enabled in the global configuration.</span></span> <span data-ttu-id="4faf1-108">A configuração global controla quais opções são habilitadas para toda a sua implantação, a não ser que você defina configurações de site ou pool que substituam a configuração global.</span><span class="sxs-lookup"><span data-stu-id="4faf1-108">The global configuration controls which options are enabled for your entire deployment, unless you set up site or pool configurations, which override the global configuration.</span></span>

<span data-ttu-id="4faf1-109">Para obter detalhes sobre como funcionam as configurações de arquivamento, incluindo a hierarquia para configurações globais, de site e de pool, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="4faf1-109">For details about how Archiving configurations work, including the hierarchy for global, site, and pool configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4faf1-110">Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento.</span><span class="sxs-lookup"><span data-stu-id="4faf1-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span>



</div>

<div>

## <a name="to-configure-archiving-options-at-the-global-level"></a><span data-ttu-id="4faf1-111">Para configurar opções de arquivamento no nível global</span><span class="sxs-lookup"><span data-stu-id="4faf1-111">To configure archiving options at the global level</span></span>

1.  <span data-ttu-id="4faf1-112">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="4faf1-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4faf1-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4faf1-113">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="4faf1-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server 2013, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4faf1-114">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4faf1-115">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Configuração de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="4faf1-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="4faf1-116">Na página **Configuração de arquivamento**, clique em **Global**, **Editar** e **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="4faf1-116">On the **Archiving Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="4faf1-117">Em **Editar configuração de arquivamento - Global**, na lista suspensa **Configuração de arquivamento**, selecione uma das seguintes opções de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="4faf1-117">In **Edit Archiving Setting - Global**, in the **Archiving setting** drop-down list, select one of the following archiving options:</span></span>
    
      - <span data-ttu-id="4faf1-118">**Desativar arquivamento**</span><span class="sxs-lookup"><span data-stu-id="4faf1-118">**Disable archiving**</span></span>
    
      - <span data-ttu-id="4faf1-119">**Arquivar sessões de IM**</span><span class="sxs-lookup"><span data-stu-id="4faf1-119">**Archive IM sessions**</span></span>
    
      - <span data-ttu-id="4faf1-120">**Arquivar sessões de IM e conferência da Web**</span><span class="sxs-lookup"><span data-stu-id="4faf1-120">**Archive IM and web conferencing sessions**</span></span>

6.  <span data-ttu-id="4faf1-121">Na página **Editar configuração de arquivamento – Global**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4faf1-121">Also on the **Edit Archiving Setting – Global** page, do the following:</span></span>
    
      - <span data-ttu-id="4faf1-122">Para bloquear a atividade quando o arquivamento não estiver disponível, marque a caixa de seleção **Bloquear sessões de mensagem instantânea ou webconferência se o arquivamento falhar**.</span><span class="sxs-lookup"><span data-stu-id="4faf1-122">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="4faf1-123">Para usar o Microsoft Exchange Server para armazenar dados de arquivamento, clique na caixa de seleção **integração do Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="4faf1-123">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="4faf1-124">Para habilitar a exclusão de dados, marque a caixa de seleção **Habilitar exclusão dos dados de arquivamento** e execute uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="4faf1-124">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="4faf1-125">Para especificar a exclusão após um número específico de dias, clique em **Excluir dados de arquivamento exportados e dados de arquivamento armazenados após uma duração máxima (dias)** e especifique o número de dias.</span><span class="sxs-lookup"><span data-stu-id="4faf1-125">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="4faf1-126">Para limitar a exclusão de dados de arquivamento que foram exportados, clique em **Excluir apenas dados de arquivamento exportados**.</span><span class="sxs-lookup"><span data-stu-id="4faf1-126">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

7.  <span data-ttu-id="4faf1-127">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="4faf1-127">Click **Commit**.</span></span>

<span data-ttu-id="4faf1-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4faf1-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

