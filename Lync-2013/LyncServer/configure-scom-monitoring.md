---
title: Configurar monitoramento SCOM
description: Configurar o monitoramento do SCOM.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure SCOM monitoring
ms:assetid: 4003d225-2a33-448c-abd9-571750661140
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688033(v=OCS.15)
ms:contentKeyID: 49733624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c93e10c705a1a1e08972d7534e00a33c472d23a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389846"
---
# <a name="configure-scom-monitoring"></a><span data-ttu-id="97c6c-103">Configurar monitoramento SCOM</span><span class="sxs-lookup"><span data-stu-id="97c6c-103">Configure SCOM monitoring</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97c6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97c6c-104">

<span> </span></span></span>

<span data-ttu-id="97c6c-105">_**Tópico da última modificação:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="97c6c-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="97c6c-106">Depois de migrar para o Microsoft Lync Server 2013, você deve concluir algumas tarefas para configurar o Lync Server 2013 para trabalhar com o System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="97c6c-106">After migrating to Microsoft Lync Server 2013, you must complete a few tasks to configure Lync Server 2013 to work with System Center Operations Manager.</span></span>

  - <span data-ttu-id="97c6c-107">Aplicar atualizações do Lync Server 2010 a um servidor escolhido para gerenciar a lógica de descoberta central.</span><span class="sxs-lookup"><span data-stu-id="97c6c-107">Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.</span></span>

  - <span data-ttu-id="97c6c-108">Atualize a chave do registro do servidor candidato à descoberta central.</span><span class="sxs-lookup"><span data-stu-id="97c6c-108">Update the central discovery candidate server registry key.</span></span>

  - <span data-ttu-id="97c6c-109">Configure o servidor de gerenciamento principal do System Center Operations Manager para substituir o nó de descoberta central de candidatos.</span><span class="sxs-lookup"><span data-stu-id="97c6c-109">Configure your primary System Center Operations Manager management server to override the candidate central discovery node.</span></span>

<span data-ttu-id="97c6c-110">As instruções para executar cada uma dessas tarefas são fornecidas abaixo.</span><span class="sxs-lookup"><span data-stu-id="97c6c-110">Instructions for carrying out each of these tasks are provided below.</span></span>

<span data-ttu-id="97c6c-111">**Aplicar atualizações do Lync Server 2010 a um servidor escolhido para gerenciar a lógica de descoberta central.**</span><span class="sxs-lookup"><span data-stu-id="97c6c-111">**Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.**</span></span>

1.  <span data-ttu-id="97c6c-112">Escolha um servidor que tenha os arquivos de agente do System Center Operations Manager instalados e esteja configurado como um nó de descoberta de candidatos.</span><span class="sxs-lookup"><span data-stu-id="97c6c-112">Elect a server that has the System Center Operations Manager agent files installed and is configured as a candidate discovery node.</span></span>

2.  <span data-ttu-id="97c6c-113">Aplicar atualizações do Lync Server 2010 a este servidor.</span><span class="sxs-lookup"><span data-stu-id="97c6c-113">Apply Lync Server 2010 updates to this server.</span></span> <span data-ttu-id="97c6c-114">Consulte o tópico [aplicar atualizações do Lync Server 2010](apply-lync-server-2010-updates.md).</span><span class="sxs-lookup"><span data-stu-id="97c6c-114">See the topic [Apply Lync Server 2010 updates](apply-lync-server-2010-updates.md).</span></span>

<span data-ttu-id="97c6c-115">**Atualize a chave do registro do servidor candidato à descoberta central.**</span><span class="sxs-lookup"><span data-stu-id="97c6c-115">**Update the central discovery candidate server registry key.**</span></span>

1.  <span data-ttu-id="97c6c-116">No servidor escolhido para gerenciar a lógica de descoberta central, abra uma janela de comando do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="97c6c-116">On the server elected to manage the central discovery logic, open a Windows PowerShell command window.</span></span>

2.  <span data-ttu-id="97c6c-117">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="97c6c-117">At the command line, type the following:</span></span>
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health"
       ```
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health\CentralDiscoveryCandidate"
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="97c6c-118">Sempre que você edita o registro, pode ocorrer um erro inque o comando falhou se a chave do registro já existe.</span><span class="sxs-lookup"><span data-stu-id="97c6c-118">Whenever you edit the registry, you may experience an error that the command failed if the registry key already exists.</span></span> <span data-ttu-id="97c6c-119">Se isso acontecer, você pode ignorar o erro com segurança.</span><span class="sxs-lookup"><span data-stu-id="97c6c-119">If you experience this, you can safely ignore the error.</span></span>

    
    </div>

<span data-ttu-id="97c6c-120">**Configure o servidor de gerenciamento principal do System Center Operations Manager para substituir o nó do inspetor da descoberta do candidato.**</span><span class="sxs-lookup"><span data-stu-id="97c6c-120">**Configure your primary System Center Operations Manager management server to override the candidate central discovery watcher node.**</span></span>

1.  <span data-ttu-id="97c6c-121">Em um computador em que o console System Center Operations Manager foi instalado, expanda os **objetos do pacote de gerenciamento** e selecione descobertas de **objetos**.</span><span class="sxs-lookup"><span data-stu-id="97c6c-121">On a computer where the System Center Operations Manager console has been installed, expand **Management Pack Objects** and then select **Object Discoveries**.</span></span>

2.  <span data-ttu-id="97c6c-122">Clique em **alterar escopo..** .</span><span class="sxs-lookup"><span data-stu-id="97c6c-122">Click **Change Scope...**</span></span>

3.  <span data-ttu-id="97c6c-123">Na página **objetos do pacote de gerenciamento de escopo** , selecione **candidato para descoberta ls**.</span><span class="sxs-lookup"><span data-stu-id="97c6c-123">From the **Scope Management Pack Objects** page, select **LS Discovery Candidate**.</span></span>

4.  <span data-ttu-id="97c6c-124">Substitua o **valor efetivo de candidato à descoberta ls** pelo nome do servidor de candidatos escolhido no procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="97c6c-124">Override the **LS Discovery Candidate Effective Value** to the name of the candidate server elected in the earlier procedure.</span></span>

<span data-ttu-id="97c6c-125">Por fim, para finalizar suas alterações, reinicie o serviço de integridade no servidor de gerenciamento raiz do System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="97c6c-125">Lastly, to finalize your changes, restart the health service on the System Center Operations Manager Root Management Server.</span></span>

<span data-ttu-id="97c6c-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97c6c-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

