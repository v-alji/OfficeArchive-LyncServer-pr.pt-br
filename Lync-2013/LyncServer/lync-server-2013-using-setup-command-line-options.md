---
title: 'Lync Server 2013: usando as opções de linha de comando de configuração'
description: 'Lync Server 2013: usando as opções de linha de comando de configuração.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Setup command-line options
ms:assetid: 99878c3c-ff31-48e2-8424-580d7b07a7bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205129(v=OCS.15)
ms:contentKeyID: 48184957
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15c3490ead090766462ce83cb13ffe62355032cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389741"
---
# <a name="using-setup-command-line-options-in-lync-server-2013"></a><span data-ttu-id="dc82d-103">Usando as opções de linha de comando de configuração no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc82d-103">Using Setup command-line options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc82d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc82d-104">

<span> </span></span></span>

<span data-ttu-id="dc82d-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="dc82d-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="dc82d-p101">A linha de comando Setup.exe é usada em poucas operações na instalação do Office. Em vez de usar as opções da linha de comando Setup, você geralmente usa a Ferramenta de personalização do Office e o arquivo Config.xml file para instalação do produto e personalização de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc82d-p101">The Setup.exe command line is used for very few operations in Office setup. Instead of using the Setup command-line options, you’ll typically use the Office Customization Tool and the Config.xml file for product setup and feature customization.</span></span>

<span data-ttu-id="dc82d-108">A linha de comando Setup.exe do Office reconhece as opções de linha de comando descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc82d-108">The Office Setup.exe command line recognizes the command-line options described in the following table.</span></span>

### <a name="office-setup-command-line-options"></a><span data-ttu-id="dc82d-109">Opções de linha de comando Setup do Office</span><span class="sxs-lookup"><span data-stu-id="dc82d-109">Office Setup Command-Line Options</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc82d-110">Opção de linha de comando Setup</span><span class="sxs-lookup"><span data-stu-id="dc82d-110">Setup Command-Line Option</span></span></th>
<th><span data-ttu-id="dc82d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc82d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc82d-112">/admin</span><span class="sxs-lookup"><span data-stu-id="dc82d-112">/admin</span></span></p></td>
<td><p><span data-ttu-id="dc82d-113">Executa a Ferramenta de personalização do Office para criar um arquivo de personalização de Setup (arquivo .msp).</span><span class="sxs-lookup"><span data-stu-id="dc82d-113">Runs the Office Customization Tool to create a Setup customization file (.msp file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc82d-114">/adminfile [caminho]</span><span class="sxs-lookup"><span data-stu-id="dc82d-114">/adminfile [path]</span></span></p></td>
<td><p><span data-ttu-id="dc82d-p102">Aplica o arquivo de personalização de Setup à instalação. Você pode especificar um caminho de arquivo de personalização específico (arquivo .msp) ou a pasta onde você armazena os arquivos de personalização.</span><span class="sxs-lookup"><span data-stu-id="dc82d-p102">Applies the specified Setup customization file to the installation. You can specify a path of a specific customization file (.msp file) or to the folder where you store customization files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc82d-117">/config [caminho]</span><span class="sxs-lookup"><span data-stu-id="dc82d-117">/config [path]</span></span></p></td>
<td><p><span data-ttu-id="dc82d-118">Especifica o arquivo Config.xml que o Setup usa durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="dc82d-118">Specifies the Config.xml file that Setup uses during the installation.</span></span> <span data-ttu-id="dc82d-119">Use a opção/config para especificar o arquivo Config.xml personalizado para instalações do Lync 2013, por exemplo: <code>/config \\server\share\Lync15\Lync.WW\Config.xml</code></span><span class="sxs-lookup"><span data-stu-id="dc82d-119">Use the /config option to specify the Config.xml file you customized for Lync 2013 installations, for example: <code>/config \\server\share\Lync15\Lync.WW\Config.xml</code></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc82d-120">/Modify Lync</span><span class="sxs-lookup"><span data-stu-id="dc82d-120">/modify Lync</span></span></p></td>
<td><p><span data-ttu-id="dc82d-121">Usado com um arquivo Config.xml modificado para executar o Setup em modo de manutenção e fazer alterações à instalação existente do Office.</span><span class="sxs-lookup"><span data-stu-id="dc82d-121">Used with a modified Config.xml file to run Setup in maintenance mode and make changes to an existing Office installation.</span></span> <span data-ttu-id="dc82d-122">Por exemplo, você pode usar a opção/Modify para adicionar ou remover recursos do Lync.</span><span class="sxs-lookup"><span data-stu-id="dc82d-122">For example, you can use the /modify option to add or remove Lync features.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc82d-123">/Repair Lync</span><span class="sxs-lookup"><span data-stu-id="dc82d-123">/repair Lync</span></span></p></td>
<td><p><span data-ttu-id="dc82d-124">Executa a instalação a partir do computador do usuário para reparar o Lync.</span><span class="sxs-lookup"><span data-stu-id="dc82d-124">Runs Setup from the user’s computer to repair Lync.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc82d-125">/Uninstall Lync</span><span class="sxs-lookup"><span data-stu-id="dc82d-125">/uninstall Lync</span></span></p></td>
<td><p><span data-ttu-id="dc82d-126">Executa a instalação para remover o Lync do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc82d-126">Runs Setup to remove Lync from the user’s computer.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc82d-127">Para obter detalhes sobre como usar as opções de linha de comando de configuração, consulte <https://go.microsoft.com/fwlink/p/?linkid=267515> .</span><span class="sxs-lookup"><span data-stu-id="dc82d-127">For details about using the setup command-line options, see <https://go.microsoft.com/fwlink/p/?linkid=267515>.</span></span>

<span data-ttu-id="dc82d-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc82d-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

