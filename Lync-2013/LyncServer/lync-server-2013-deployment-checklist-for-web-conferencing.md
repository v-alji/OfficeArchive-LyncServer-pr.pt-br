---
title: Lista de verificação da implantação do Lync Server 2013 para Webconferência
description: Lista de verificação de implantação do Lync Server 2013 para conferência via Web.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for web conferencing
ms:assetid: 9908ebe0-e5d3-4920-b9b1-85021f7e69e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205104(v=OCS.15)
ms:contentKeyID: 48184878
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6194cb71af268a45dc5c142c1814d8c1ef15c09e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429703"
---
# <a name="deployment-checklist-for-web-conferencing-in-lync-server-2013"></a><span data-ttu-id="5d2bc-103">Lista de verificação da implantação para Webconferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d2bc-103">Deployment checklist for web conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d2bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d2bc-104">

<span> </span></span></span>

<span data-ttu-id="5d2bc-105">_**Tópico da última modificação:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="5d2bc-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="5d2bc-106">Assim como com a implantação de outros componentes do Lync Server 2013, a implantação de Webconferência requer que você use o construtor de topologias para criar e publicar uma topologia que incorpore conferências.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-106">As with deployment of your other Lync Server 2013 components, deployment of web conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="5d2bc-107">Sequência de implantação</span><span class="sxs-lookup"><span data-stu-id="5d2bc-107">Deployment Sequence</span></span>

<span data-ttu-id="5d2bc-108">Você pode implantar conferências ao mesmo tempo em que implantar a sua topologia inicial ou depois de implantar pelo menos um pool de front-end ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="5d2bc-109">Processo de implantação de conferência</span><span class="sxs-lookup"><span data-stu-id="5d2bc-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="5d2bc-110">A tabela a seguir fornece uma visão geral das etapas necessárias para implantar a conferência em uma topologia existente.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d2bc-111">Fase</span><span class="sxs-lookup"><span data-stu-id="5d2bc-111">Phase</span></span></th>
<th><span data-ttu-id="5d2bc-112">Etapas</span><span class="sxs-lookup"><span data-stu-id="5d2bc-112">Steps</span></span></th>
<th><span data-ttu-id="5d2bc-113">Funções e associações de grupo</span><span class="sxs-lookup"><span data-stu-id="5d2bc-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="5d2bc-114">Documentação</span><span class="sxs-lookup"><span data-stu-id="5d2bc-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d2bc-115"><strong>Instalar pré-requisitos de hardware e software</strong></span><span class="sxs-lookup"><span data-stu-id="5d2bc-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="5d2bc-116">A conferência é executada em servidores front-end em um pool de front-end e em servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-116">Conferencing runs on Front End Servers in a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="5d2bc-117">Não há requisitos adicionais de hardware ou software além daqueles necessários para instalar esses servidores.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="5d2bc-118">O Lync Server 2013 usa o Office Web Apps e o Office Web Apps Server para lidar com o compartilhamento e a renderização de apresentações do PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="5d2bc-119">Para obter informações sobre como instalar e configurar o Office Web Apps Server, consulte <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configurando a integração com o Office Web Apps Server e o Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-119">For information about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="5d2bc-120">Domínio do usuário que é membro do grupo local de Administradores</span><span class="sxs-lookup"><span data-stu-id="5d2bc-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="5d2bc-121"><a href="lync-server-2013-supported-hardware.md">Hardware com suporte para o Lync Server 2013</a> na documentação de suporte</span><span class="sxs-lookup"><span data-stu-id="5d2bc-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="5d2bc-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Suporte de software e infraestrutura do servidor no Lync Server 2013</a> na documentação de suporte</span><span class="sxs-lookup"><span data-stu-id="5d2bc-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="5d2bc-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determinação dos requisitos do sistema para o Lync Server 2013</a> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="5d2bc-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Requisitos técnicos para arquivamento no Lync Server 2013</a> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d2bc-125"><strong>Crie a topologia interna apropriada para dar suporte à conferência</strong></span><span class="sxs-lookup"><span data-stu-id="5d2bc-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="5d2bc-126">Execute o construtor de topologias para adicionar conferências à topologia e, em seguida, publique a topologia.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="5d2bc-127">Para definir a topologia, uma conta que é membro do grupo local de Usuários</span><span class="sxs-lookup"><span data-stu-id="5d2bc-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="5d2bc-128">Para publicar a topologia, uma conta que é membro do grupo Domain admins e do grupo RTCUniversalServerAdmins e que tem permissões de controle total (ler/gravar/modificar) no compartilhamento de arquivos a ser usado para o repositório de arquivos do Lync Server 2013 (para que o construtor de topologias possa configurar as DACLs necessárias)</span><span class="sxs-lookup"><span data-stu-id="5d2bc-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="5d2bc-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Defina e configure uma topologia no construtor de topologias para o Lync Server 2013</a> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d2bc-130"><strong>Configurar políticas de conferência e suporte</strong></span><span class="sxs-lookup"><span data-stu-id="5d2bc-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="5d2bc-131">Use o painel de controle do Lync Server 2013 ou o Shell de gerenciamento do Lync Server para definir as configurações de conferência.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="5d2bc-132">Grupo RTCUniversalServerAdmins (somente Windows PowerShell) ou atribuir usuários à função [] ou CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="5d2bc-132">RTCUniversalServerAdmins group ( Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="5d2bc-133"><a href="lync-server-2013-conferencing-policies.md">Políticas de conferência no Lync Server 2013</a> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d2bc-134">O Lync Server 2013 agora inclui a configuração **MaxUploadFileSizeMb** , que limita o tamanho dos arquivos que podem ser carregados durante uma reunião.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-134">Lync Server 2013 now includes the **MaxUploadFileSizeMb** setting, which limits the size of files that can be uploaded during a meeting.</span></span> <span data-ttu-id="5d2bc-135">O valor padrão dessa configuração é de 500 MB.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-135">The default value for this setting is 500 MB.</span></span> <span data-ttu-id="5d2bc-136">Você pode ajustar **MaxUploadFileSizeMb** usando o cmdlet **set-CsConferencingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="5d2bc-136">You can adjust **MaxUploadFileSizeMb** using the **Set-CsConferencingConfiguration** cmdlet.</span></span>

<span data-ttu-id="5d2bc-137">**MaxUploadFileSizeMb** não limita a configuração de carregamento de arquivo do Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-137">**MaxUploadFileSizeMb** does not limit the file upload setting for Lync Web App.</span></span> <span data-ttu-id="5d2bc-138">O limite de carregamento do tamanho do arquivo do Lync Web App é definido como aproximadamente 30MB e é controlado pelo arquivo IIS web.config:/DataCollabWeb/Int \[ ext \] /Handler/web.config. Para configurar o limite de carregamento do tamanho do arquivo do Lync Web App, atualize `maxRequestLength` e `maxAllowedContentLength` no arquivo web.config como mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-138">The file size upload limit for Lync Web App is set to approximately 30MB and is controlled by the IIS web.config file: /DataCollabWeb/Int\[Ext\]/Handler/web.config. To configure the file size upload limit for Lync Web App, update `maxRequestLength` and `maxAllowedContentLength` in the web.config file as shown below.</span></span>

    <system.web>
        <!-- 
            Since this handler is used to upload files to DMCU the request size (in kilobytes) 
            has to fit max allowed file size uploaded by LWA client.
            The timeout has to reflect the min client bandwidth. Timeout of 600 secs 
            and 512 Kbits of *client* bandwidth would result into aproximately 30 Mbytes 
            for LWA upload size limit.
        -->
          <httpRuntime maxRequestLength="500000" executionTimeout="600" />
    
    
    
                    <security>
                    <requestFiltering>
                               <requestLimits maxAllowedContentLength="524288000" />
                    </requestFiltering>
                    </security>

<span data-ttu-id="5d2bc-139">Você deve atualizar o arquivo web.config para cada servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="5d2bc-139">You must update the web.config file for each Front End Server.</span></span>

<span data-ttu-id="5d2bc-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d2bc-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

