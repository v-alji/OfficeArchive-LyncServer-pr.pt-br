---
title: 'Lync Server 2013: Configurando opções de arquivamento para um pool'
description: 'Lync Server 2013: Configurando opções de arquivamento para um pool.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Archiving options for a pool
ms:assetid: b7cb0fd8-3d31-4858-a75c-c66a7742556e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205200(v=OCS.15)
ms:contentKeyID: 48185230
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf3b28fd12fab5883e3be319bec169d13c539b1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433322"
---
# <a name="configuring-archiving-options-for-a-pool-in-lync-server-2013"></a><span data-ttu-id="867e6-103">Configurando opções de arquivamento para um pool no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="867e6-103">Configuring Archiving options for a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="867e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="867e6-104">

<span> </span></span></span>

<span data-ttu-id="867e6-105">_**Tópico da última modificação:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="867e6-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="867e6-106">Você pode especificar opções de arquivamento a serem aplicadas a pools específicos, criando e Configurando opções em uma configuração de arquivamento para cada um desses pools.</span><span class="sxs-lookup"><span data-stu-id="867e6-106">You can specify Archiving options to be applied to specific pools by creating and configuring options in an Archiving configuration for each of those pools.</span></span> <span data-ttu-id="867e6-107">Uma configuração de pool substitui a configuração global e de site, mas só se aplica ao pool específico definido na configuração de pool.</span><span class="sxs-lookup"><span data-stu-id="867e6-107">A pool configuration overrides the global configuration and site configuration, but only for the pool specified in the pool configuration.</span></span>

<span data-ttu-id="867e6-108">Para obter detalhes sobre como funcionam as configurações de arquivamento, incluindo a hierarquia para configurações globais, de site e de pool, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="867e6-108">For details about how Archiving configurations work, including the hierarchy for global, site, and pool configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="867e6-109">Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento.</span><span class="sxs-lookup"><span data-stu-id="867e6-109">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="867e6-110">Para obter detalhes, consulte <A href="lync-server-2013-configuring-archiving-options.md">Configurando opções de arquivamento no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="867e6-110">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-archiving-options-at-the-pool-level"></a><span data-ttu-id="867e6-111">Para configurar as opções de arquivamento no nível do pool</span><span class="sxs-lookup"><span data-stu-id="867e6-111">To configure archiving options at the pool level</span></span>

1.  <span data-ttu-id="867e6-112">Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="867e6-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="867e6-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="867e6-113">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="867e6-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server 2013, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="867e6-114">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="867e6-115">Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Configuração de Arquivamento**.</span><span class="sxs-lookup"><span data-stu-id="867e6-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="867e6-116">Na página **Configuração de arquivamento**, clique em **Nova** e em **Configuração de pool**.</span><span class="sxs-lookup"><span data-stu-id="867e6-116">On the **Archiving Configuration** page, click **New**, and then click **Pool Configuration**.</span></span>

5.  <span data-ttu-id="867e6-117">Em **Selecionar um serviço**, selecione o pool que será configurado para arquivamento.</span><span class="sxs-lookup"><span data-stu-id="867e6-117">In **Select a Service**, select the pool to be configured for archiving.</span></span>

6.  <span data-ttu-id="867e6-118">Em **Nova configuração de arquivamento**, na lista suspensa **Configuração de arquivamento**, selecione uma das seguintes opções de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="867e6-118">In **New Archiving Setting**, in the **Archiving setting** drop-down list, select one of the following archiving options:</span></span>
    
      - <span data-ttu-id="867e6-119">**Desativar arquivamento**</span><span class="sxs-lookup"><span data-stu-id="867e6-119">**Disable archiving**</span></span>
    
      - <span data-ttu-id="867e6-120">**Arquivar sessões de IM**</span><span class="sxs-lookup"><span data-stu-id="867e6-120">**Archive IM sessions**</span></span>
    
      - <span data-ttu-id="867e6-121">**Arquivar sessões de IM e conferência da Web**</span><span class="sxs-lookup"><span data-stu-id="867e6-121">**Archive IM and web conferencing sessions**</span></span>

7.  <span data-ttu-id="867e6-122">Na página **Nova configuração de arquivamento**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="867e6-122">Also in **New Archiving Setting** page, do the following:</span></span>
    
      - <span data-ttu-id="867e6-123">Para bloquear a atividade quando o arquivamento não estiver disponível, marque a caixa de seleção **Bloquear sessões de mensagem instantânea ou webconferência se o arquivamento falhar**.</span><span class="sxs-lookup"><span data-stu-id="867e6-123">To block activity when archiving is not available, select the **Block instant messaging (IM) or web conferencing sessions if archiving fails** check box.</span></span>
    
      - <span data-ttu-id="867e6-124">Para usar o Microsoft Exchange Server para armazenar dados de arquivamento, clique na caixa de seleção **integração do Microsoft Exchange** .</span><span class="sxs-lookup"><span data-stu-id="867e6-124">To use Microsoft Exchange Server to store archiving data, click the **Microsoft Exchange integration** check box.</span></span>
    
      - <span data-ttu-id="867e6-125">Para habilitar a exclusão de dados, marque a caixa de seleção **Habilitar exclusão dos dados de arquivamento** e execute uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="867e6-125">To enable data purging, select the **Enable purging of archiving data** check box, and then do one of the following:</span></span>
        
          - <span data-ttu-id="867e6-126">Para especificar a exclusão após um número específico de dias, clique em **Excluir dados de arquivamento exportados e dados de arquivamento armazenados após uma duração máxima (dias)** e especifique o número de dias.</span><span class="sxs-lookup"><span data-stu-id="867e6-126">To specify purging after a specific number of days, click **Purge exported archiving data and stored archiving data after maximum duration (days)**, and then specify the number of days.</span></span>
        
          - <span data-ttu-id="867e6-127">Para limitar a exclusão de dados de arquivamento que foram exportados, clique em **Excluir apenas dados de arquivamento exportados**.</span><span class="sxs-lookup"><span data-stu-id="867e6-127">To limit purging to archiving data that has been exported, click **Purge exported archiving data only**.</span></span>

8.  <span data-ttu-id="867e6-128">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="867e6-128">Click **Commit**.</span></span>

<span data-ttu-id="867e6-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="867e6-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

