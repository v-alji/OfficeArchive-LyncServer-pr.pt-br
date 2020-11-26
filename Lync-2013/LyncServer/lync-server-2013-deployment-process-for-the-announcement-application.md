---
title: 'Lync Server 2013: processo de implantação para o aplicativo de anúncio'
description: 'Lync Server 2013: processo de implantação para o aplicativo de anúncio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for the Announcement application
ms:assetid: 72c66249-c4ce-48ce-b1b9-90ebf77d7805
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398545(v=OCS.15)
ms:contentKeyID: 48184500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 559977c32f63fae312164b5b0c36698fa13afb09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429640"
---
# <a name="deployment-process-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="b3ce5-103">Processo de implantação do aplicativo de anúncio no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3ce5-103">Deployment process for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3ce5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3ce5-104">

<span> </span></span></span>

<span data-ttu-id="b3ce5-105">_**Tópico da última modificação:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="b3ce5-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="b3ce5-106">Esta seção fornece uma visão geral das etapas envolvidas na implantação do aplicativo de anúncio.</span><span class="sxs-lookup"><span data-stu-id="b3ce5-106">This section provides an overview of the steps involved in deploying the Announcement application.</span></span> <span data-ttu-id="b3ce5-107">Você deve implantar o Enterprise Voice antes de configurar comunicados.</span><span class="sxs-lookup"><span data-stu-id="b3ce5-107">You must deploy Enterprise Voice before you configure announcements.</span></span> <span data-ttu-id="b3ce5-108">Os componentes exigidos pelo aplicativo de anúncio são instalados e habilitados durante a implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="b3ce5-108">The components required by the Announcement application are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="announcement-deployment-process"></a><span data-ttu-id="b3ce5-109">Processo de implantação do comunicado</span><span class="sxs-lookup"><span data-stu-id="b3ce5-109">Announcement Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3ce5-110">Fase</span><span class="sxs-lookup"><span data-stu-id="b3ce5-110">Phase</span></span></th>
<th><span data-ttu-id="b3ce5-111">Etapas</span><span class="sxs-lookup"><span data-stu-id="b3ce5-111">Steps</span></span></th>
<th><span data-ttu-id="b3ce5-112">Funções</span><span class="sxs-lookup"><span data-stu-id="b3ce5-112">Roles</span></span></th>
<th><span data-ttu-id="b3ce5-113">Documentação de implantação</span><span class="sxs-lookup"><span data-stu-id="b3ce5-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3ce5-114">Definir configurações do comunicado</span><span class="sxs-lookup"><span data-stu-id="b3ce5-114">Configure Announcement settings</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="b3ce5-115">Crie o comunicado através da gravação e carregamento de arquivos de áudio ou usando texto em fala (TTS).</span><span class="sxs-lookup"><span data-stu-id="b3ce5-115">Create the announcement by recording and uploading audio files or by using text-to-speech (TTS).</span></span></p></li>
<li><p><span data-ttu-id="b3ce5-116">Configure os intervalos de números não atribuídos na tabela de número não atribuída e os associe com o comunicado adequado.</span><span class="sxs-lookup"><span data-stu-id="b3ce5-116">Configure the unassigned number ranges in the unassigned number table and associate them with the appropriate announcement.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="b3ce5-117">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="b3ce5-117">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="b3ce5-118">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="b3ce5-118">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="b3ce5-119">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="b3ce5-119">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="b3ce5-120">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="b3ce5-120">CsAdministrator</span></span></p>
<p><span data-ttu-id="b3ce5-121">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="b3ce5-121">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="b3ce5-122"><a href="lync-server-2013-create-an-announcement.md">Criar um anúncio no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b3ce5-122"><a href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="b3ce5-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configurar a tabela de número não atribuído no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b3ce5-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configure the unassigned number table in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3ce5-124">Verifique a implantação do comunicado</span><span class="sxs-lookup"><span data-stu-id="b3ce5-124">Verify your Announcement deployment</span></span></p></td>
<td><p><span data-ttu-id="b3ce5-125">Faça o teste escutando os comunicados para verificar se sua configuração funciona como o esperado.</span><span class="sxs-lookup"><span data-stu-id="b3ce5-125">Test by listening to announcements to verify that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="b3ce5-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">Adicionais Verificar a implantação do lançamento no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b3ce5-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">(Optional) Verify Announcement deployment in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b3ce5-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3ce5-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

