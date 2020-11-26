---
title: 'Lync Server 2013: cmdlets do Active Directory'
description: 'Lync Server 2013: cmdlets do Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory cmdlets
ms:assetid: 313d73cb-f3db-4bc4-8708-de4da1d719c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415640(v=OCS.15)
ms:contentKeyID: 48183769
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c5e87cda24d5517b9c4501523fd06804ea20020
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439468"
---
# <a name="active-directory-cmdlets-in-lync-server-2013"></a><span data-ttu-id="cbd9c-103">Cmdlets do Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cbd9c-103">Active Directory cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cbd9c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cbd9c-104">

<span> </span></span></span>

<span data-ttu-id="cbd9c-105">_**Tópico da última modificação:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="cbd9c-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="cbd9c-106">Os cmdlets do Active Directory geralmente são usados pelo programa de instalação e raramente serão chamados diretamente por um administrador.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-106">The Active Directory cmdlets are typically used by Setup, and will rarely be called directly by an administrator.</span></span> <span data-ttu-id="cbd9c-107">No entanto, os administradores podem usar esses cmdlets para preparar (ou despreparar) um domínio ou floresta para o Microsoft Lync Server 2013 e instalar os arquivos de esquema obrigatórios do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cbd9c-107">However, administrators can use these cmdlets to prepare (or unprepare) a domain or forest for Microsoft Lync Server 2013, and to install the required Active Directory schema files.</span></span>

<div>

## <a name="active-directory-cmdlets"></a><span data-ttu-id="cbd9c-108">Cmdlets do Active Directory</span><span class="sxs-lookup"><span data-stu-id="cbd9c-108">Active Directory Cmdlets</span></span>

<span data-ttu-id="cbd9c-109">Veja a seguir uma lista de cmdlets relacionados diretamente ao gerenciamento de configurações do Active Directory do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="cbd9c-109">The following is a list of cmdlets that relate directly to managing Lync Server 2013 Active Directory settings:</span></span>

<span data-ttu-id="cbd9c-110">**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="cbd9c-110">**Active Directory**</span></span>

  - <span></span>  
    <span data-ttu-id="cbd9c-111">[Disable-CsAdDomain](https://technet.microsoft.com/library/Gg398785(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-111">[Disable-CsAdDomain](https://technet.microsoft.com/library/Gg398785(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="cbd9c-112">[Enable-CsAdDomain](https://technet.microsoft.com/library/Gg412764(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-112">[Enable-CsAdDomain](https://technet.microsoft.com/library/Gg412764(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="cbd9c-113">[Get-CsAdDomain](https://technet.microsoft.com/library/Gg398453(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-113">[Get-CsAdDomain](https://technet.microsoft.com/library/Gg398453(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="cbd9c-114">[Disable-CsAdForest](https://technet.microsoft.com/library/Gg398122(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-114">[Disable-CsAdForest](https://technet.microsoft.com/library/Gg398122(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="cbd9c-115">[Enable-CsAdForest](https://technet.microsoft.com/library/Gg425713(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-115">[Enable-CsAdForest](https://technet.microsoft.com/library/Gg425713(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="cbd9c-116">[Get-CsAdForest](https://technet.microsoft.com/library/Gg412995(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-116">[Get-CsAdForest](https://technet.microsoft.com/library/Gg412995(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="cbd9c-117">[Get-CsAdServerSchema](https://technet.microsoft.com/library/Gg413070(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-117">[Get-CsAdServerSchema](https://technet.microsoft.com/library/Gg413070(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="cbd9c-118">[Install-CsAdServerSchema](https://technet.microsoft.com/library/Gg398681(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="cbd9c-118">[Install-CsAdServerSchema](https://technet.microsoft.com/library/Gg398681(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cbd9c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbd9c-119">See Also</span></span>


[<span data-ttu-id="cbd9c-120">Blog do PowerShell do Lync Server</span><span class="sxs-lookup"><span data-stu-id="cbd9c-120">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="cbd9c-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cbd9c-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

