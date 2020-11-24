---
title: 'Lync Server 2013: Etapas para preparar e implantar o ambiente híbrido do Lync Server'
description: 'Lync Server 2013: etapas para preparar e implantar o ambiente híbrido do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Steps to prepare and deploy Lync Server 2013 hybrid environment
ms:assetid: a50d4f7b-63f4-4663-af63-56ca87e4e3e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205157(v=OCS.15)
ms:contentKeyID: 48185060
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ffb791a8a45b2220d8987c8d688f346447747c00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389765"
---
# <a name="steps-to-prepare-and-deploy-lync-server-2013-hybrid-environment"></a><span data-ttu-id="41125-103">Etapas para preparar e implantar o ambiente híbrido do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41125-103">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41125-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41125-104">

<span> </span></span></span>

<span data-ttu-id="41125-105">_**Tópico da última modificação:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="41125-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="41125-106">A tabela a seguir lista as etapas necessárias para preparar o ambiente para uma implantação híbrida com o Skype for Business Online e o Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="41125-106">The following table lists the steps required to prepare your environment for a hybrid deployment with Skype for Business Online and Microsoft Office 365.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="41125-107">Concluído?</span><span class="sxs-lookup"><span data-stu-id="41125-107">Completed?</span></span></th>
<th><span data-ttu-id="41125-108">Etapa</span><span class="sxs-lookup"><span data-stu-id="41125-108">Step</span></span></th>
<th><span data-ttu-id="41125-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="41125-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="41125-110">Criar uma conta de locatário do Office 365 e habilitar o Lync Online</span><span class="sxs-lookup"><span data-stu-id="41125-110">Create a tenant account for Office 365 and enable Lync Online</span></span></p></td>
<td><p><span data-ttu-id="41125-111">Saiba mais sobre o Office 365 e o Lync Online no <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-111">Learn about Office 365 and Lync Online at <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">Office 365</a>.</span></span></p>
<p><span data-ttu-id="41125-112">Para garantir que seu ambiente esteja pronto para o Office 365, consulte os <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">requisitos do sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-112">To make sure that your environment is ready for Office 365, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">System Requirements</a>.</span></span></p>
<p><span data-ttu-id="41125-113">Para obter detalhes sobre a configuração do Office 365, consulte <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">introdução ao office 365</a> e <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">configurar o Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-113">For details about setting up Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Getting Started with Office 365</a> and <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Set Up Office 365</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="41125-114">Adicionar seu domínio e verificar quem é o proprietário</span><span class="sxs-lookup"><span data-stu-id="41125-114">Add your domain and verify ownership</span></span></p></td>
<td><p><span data-ttu-id="41125-115">Seu domínio também é mencionado algumas vezes como <em>domínio personalizado</em>.</span><span class="sxs-lookup"><span data-stu-id="41125-115">Your domain is sometimes also referred to as your <em>vanity domain</em>.</span></span> <span data-ttu-id="41125-116">Você deve adicionar seu domínio à sua organização do Office 365 e, em seguida, seguir as etapas para validar o domínio com o Office 365.</span><span class="sxs-lookup"><span data-stu-id="41125-116">You must add your domain to your Office 365 organization, and then follow the steps to validate the domain with Office 365.</span></span> <span data-ttu-id="41125-117">Isso serve para confirmar que você é o proprietário do domínio.</span><span class="sxs-lookup"><span data-stu-id="41125-117">This is to confirm that you are the owner of the domain.</span></span></p>
<p><span data-ttu-id="41125-118">Para adicionar seu domínio à sua organização do Office 365, siga as etapas descritas em <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Adicionar seu domínio ao Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-118">To add your domain to your Office 365 organization, follow the steps described at <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Add your domain to Office 365</a>.</span></span></p>
<p><span data-ttu-id="41125-119">Conclua todas as etapas em cada seção do tópico, incluindo &quot; editar registros DNS para seus serviços do Office 365.&quot;</span><span class="sxs-lookup"><span data-stu-id="41125-119">Complete all of the steps in each section in the topic, including &quot;Edit DNS records for your Office 365 services.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="41125-120">Verificar a preparação do ambiente</span><span class="sxs-lookup"><span data-stu-id="41125-120">Verify environment readiness</span></span></p></td>
<td><p><span data-ttu-id="41125-121">Você pode usar o assistente de configuração do Office 365 para ajudá-lo a implantar o Office 365.</span><span class="sxs-lookup"><span data-stu-id="41125-121">You can use the Office 365 Setup Assistant to help you deploy Office 365.</span></span> <span data-ttu-id="41125-122">Para obter mais informações, consulte <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">usar o assistente de configuração para determinar a preparação do Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-122">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">Use Setup Assistant to determine Office 365 readiness</a>.</span></span></p>
<p><span data-ttu-id="41125-123">Para obter detalhes sobre como usar a ferramenta e implantar o Office 365, consulte <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Guia de implantação do office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-123">For details about using the tool and deploying Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Office 365 deployment guide</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="41125-124">Preparar-se para a sincronização do Active Directory</span><span class="sxs-lookup"><span data-stu-id="41125-124">Prepare for Active Directory synchronization</span></span></p></td>
<td><p><span data-ttu-id="41125-125">A sincronização do Active Directory mantém a sincronização contínua do Active Directory no local com o Office 365.</span><span class="sxs-lookup"><span data-stu-id="41125-125">Active Directory synchronization keeps your on-premises Active Directory continuously synchronized with Office 365.</span></span> <span data-ttu-id="41125-126">Assim, é possível criar versões sincronizadas de cada grupo e conta de usuário e também habilitar a sincronização de lista de endereços global (GAL) do seu ambiente local do Microsoft Exchange Server para o Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="41125-126">This lets you create synchronized versions of each user account and group, and also enables global address list (GAL) synchronization from your local Microsoft Exchange Server environment to Microsoft Exchange Online.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="41125-127">Você precisa sincronizar as contas do anúncio para todos os usuários do Lync em sua organização entre suas implantações locais e online do Lync, mesmo se os usuários não forem movidos para o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="41125-127">You need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="41125-128">Se você não sincronizar todos os usuários, a comunicação entre os usuários locais e online na sua organização poderá não funcionar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="41125-128">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>


</div>
<p><span data-ttu-id="41125-129">Para preparar seu ambiente para a sincronização do Active Directory, siga as etapas descritas no <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">mapa de sincronização de diretório</a>, incluindo a configuração de logon único.</span><span class="sxs-lookup"><span data-stu-id="41125-129">To prepare your environment for Active Directory synchronization, follow the steps described in <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Directory synchronization Roadmap</a>, including setting up single sign-on.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="41125-130">Criar certificados para o AD FS (serviços de Federação do Active Directory)</span><span class="sxs-lookup"><span data-stu-id="41125-130">Create certificates for Active Directory Federation Services (AD FS)</span></span></p></td>
<td><p><span data-ttu-id="41125-131">Será necessário criar os certificados usados para a Federação de identidade com o Office 365.</span><span class="sxs-lookup"><span data-stu-id="41125-131">You will need to create the certificates that are used for identity federation with Office 365.</span></span> <span data-ttu-id="41125-132">Para obter mais informações, consulte a seção "certificados do servidor de Federação" do tópico planejar e implantar o AD FS para uso com o logon único na <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">lista de verificação: Use o AD FS para implementar e gerenciar o logon único</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-132">For more information, see the “Federation server certificates” section of the Plan for and deploy AD FS for use with single sign-on topic at <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">Checklist: Use AD FS to implement and manage single sign-on</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="41125-133">Atribuir certificados para o AD FS</span><span class="sxs-lookup"><span data-stu-id="41125-133">Assign certificates for AD FS</span></span></p></td>
<td><p><span data-ttu-id="41125-134">Depois de criar os certificados usados para a Federação de identidade com o Office 365, você deve instalá-los e atribuí-los.</span><span class="sxs-lookup"><span data-stu-id="41125-134">After you create the certificates that are used for identity federation with Office 365, you must install and assign them.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="41125-135">Mover os usuários piloto para o Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="41125-135">Move pilot users to Skype for Business Online</span></span></p></td>
<td><p><span data-ttu-id="41125-136">Depois de concluir as etapas para preparar e configurar seu ambiente para o Skype for Business Online, você pode começar a mover os usuários piloto para o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="41125-136">After you have completed the steps to prepare and configure your environment for Skype for Business Online, you can start moving pilot users to Lync Online.</span></span></p>
<p><span data-ttu-id="41125-137">Consulte <a href="lync-server-2013-move-users-to-lync-online.md">mover usuários para o Lync Online no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-137">See <a href="lync-server-2013-move-users-to-lync-online.md">Move users to Lync Online in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="41125-138">Administrando usuários em uma implantação híbrida</span><span class="sxs-lookup"><span data-stu-id="41125-138">Administering users in a hybrid deployment</span></span></p></td>
<td><p><span data-ttu-id="41125-139">Para obter detalhes sobre como administrar usuários em uma implantação híbrida, consulte <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">administrando usuários em uma implantação híbrida do Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="41125-139">For details about how to administer users in a hybrid deployment, see <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</a>.</span></span></p></td>
</tr><span data-ttu-id="41125-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41125-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

