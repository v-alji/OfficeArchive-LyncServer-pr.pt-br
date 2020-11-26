---
title: 'Lync Server 2013: processo de implantação de cliente móvel'
description: 'Lync Server 2013: processo de implantação de cliente móvel.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobile client deployment process
ms:assetid: 6498235b-2fa9-421d-bfa0-0ccc09508dbd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690982(v=OCS.15)
ms:contentKeyID: 51541484
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fa4e9e1d272915e06009df5c06480309ce104e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425560"
---
# <a name="mobile-client-deployment-process-in-lync-server-2013"></a><span data-ttu-id="1050a-103">Processo de implantação de cliente móvel no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1050a-103">Mobile client deployment process in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1050a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1050a-104">

<span> </span></span></span>

<span data-ttu-id="1050a-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="1050a-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="1050a-106">Após a conclusão da implantação do Microsoft Lync Server 2013, os usuários podem instalar o aplicativo Lync 2013 do Mobile Marketplace em que estão acostumados a usar para seu dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="1050a-106">After a deployment of Microsoft Lync Server 2013 has been completed, users can install the Lync 2013 app from the mobile marketplace that they are accustomed to using for their specific device.</span></span>

<div>

## <a name="lync-mobile-deployment-process"></a><span data-ttu-id="1050a-107">Processo de implantação do Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="1050a-107">Lync Mobile Deployment Process</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1050a-108">Fase</span><span class="sxs-lookup"><span data-stu-id="1050a-108">Phase</span></span></th>
<th><span data-ttu-id="1050a-109">Etapas</span><span class="sxs-lookup"><span data-stu-id="1050a-109">Steps</span></span></th>
<th><span data-ttu-id="1050a-110">Permissões</span><span class="sxs-lookup"><span data-stu-id="1050a-110">Permissions</span></span></th>
<th><span data-ttu-id="1050a-111">Documentação</span><span class="sxs-lookup"><span data-stu-id="1050a-111">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1050a-112">Executar tarefas anteriores à configuração.</span><span class="sxs-lookup"><span data-stu-id="1050a-112">Perform pre-setup tasks.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="1050a-113">Verifique a implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1050a-113">Verify Lync Server 2013 deployment.</span></span></p></li>
<li><p><span data-ttu-id="1050a-114">Verifique os requisitos de certificado.</span><span class="sxs-lookup"><span data-stu-id="1050a-114">Verify certificate requirements.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="1050a-115">Administrador</span><span class="sxs-lookup"><span data-stu-id="1050a-115">Administrator</span></span></p></td>
<td><p><span data-ttu-id="1050a-116"><a href="lync-server-2013-planning-for-mobility.md">Planejando a mobilidade no Lync Server 2013</a> na documentação de planejamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="1050a-116"><a href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</a> in the server planning documentation.</span></span></p>
<p><span data-ttu-id="1050a-117"><a href="lync-server-2013-deploying-mobility.md">Implantação de mobilidade no Lync Server 2013</a> na documentação de implantação do servidor.</span><span class="sxs-lookup"><span data-stu-id="1050a-117"><a href="lync-server-2013-deploying-mobility.md">Deploying mobility in Lync Server 2013</a> in the server deployment documentation.</span></span></p>
<p><span data-ttu-id="1050a-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Requisitos de infraestrutura de certificado para o Lync Server 2013</a> na documentação de planejamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="1050a-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Certificate infrastructure requirements for Lync Server 2013</a> in the server planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1050a-119">Instale o aplicativo do Lync em um dispositivo de teste.</span><span class="sxs-lookup"><span data-stu-id="1050a-119">Install the Lync application on a test device.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="1050a-120">Instalar pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="1050a-120">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="1050a-121">Instale do Marketplace específico para o dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="1050a-121">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="1050a-122">Administrador</span><span class="sxs-lookup"><span data-stu-id="1050a-122">Administrator</span></span></p></td>
<td><p><span data-ttu-id="1050a-123">Instruções de instalação específicas ao dispositivo móvel em <a href="lync-server-2013-deploying-mobile-clients.md">implantando clientes móveis no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1050a-123">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1050a-124">Configurar o cliente.</span><span class="sxs-lookup"><span data-stu-id="1050a-124">Configure the client.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1050a-125">Configurar as configurações de entrada e as informações do servidor.</span><span class="sxs-lookup"><span data-stu-id="1050a-125">Configure sign-in settings and server information.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="1050a-126">Administrador</span><span class="sxs-lookup"><span data-stu-id="1050a-126">Administrator</span></span></p></td>
<td><p><span data-ttu-id="1050a-127"><a href="lync-server-2013-deploying-mobile-clients.md">Implantando clientes móveis no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="1050a-127"><a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1050a-128">Testar cenários móveis.</span><span class="sxs-lookup"><span data-stu-id="1050a-128">Test mobile scenarios.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="1050a-129">Testar mensagens instantâneas (IM) e presença.</span><span class="sxs-lookup"><span data-stu-id="1050a-129">Test instant messaging (IM) and presence.</span></span></p></li>
<li><p><span data-ttu-id="1050a-130">Teste a conferência discada.</span><span class="sxs-lookup"><span data-stu-id="1050a-130">Test dial-out conferencing.</span></span></p></li>
<li><p><span data-ttu-id="1050a-131">Procure um contato no diretório corporativo.</span><span class="sxs-lookup"><span data-stu-id="1050a-131">Search for a contact in the corporate directory.</span></span></p></li>
<li><p><span data-ttu-id="1050a-132">Teste as notificações por push.</span><span class="sxs-lookup"><span data-stu-id="1050a-132">Test push notifications.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="1050a-133">Administrador</span><span class="sxs-lookup"><span data-stu-id="1050a-133">Administrator</span></span></p></td>
<td><p><span data-ttu-id="1050a-134">Instruções de verificação específicas do dispositivo móvel em <a href="lync-server-2013-deploying-mobile-clients.md">implantando clientes móveis no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1050a-134">Verification instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1050a-135">Instale o aplicativo do Lync em telefones celulares.</span><span class="sxs-lookup"><span data-stu-id="1050a-135">Install the Lync application on mobile phones.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="1050a-136">Instalar pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="1050a-136">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="1050a-137">Instale do Marketplace específico para o dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="1050a-137">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="1050a-138">Usuário</span><span class="sxs-lookup"><span data-stu-id="1050a-138">User</span></span></p></td>
<td><p><span data-ttu-id="1050a-139">Instruções de instalação específicas ao dispositivo móvel em <a href="lync-server-2013-deploying-mobile-clients.md">implantando clientes móveis no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="1050a-139">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1050a-140">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1050a-140">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

