---
title: Instalar o pacote de compatibilidade com versões anteriores do WMI
description: Instale o pacote de compatibilidade com versões anteriores do WMI.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439571"
---
# <a name="install-wmi-backward-compatibility-package"></a><span data-ttu-id="9aef3-103">Instalar o pacote de compatibilidade com versões anteriores do WMI</span><span class="sxs-lookup"><span data-stu-id="9aef3-103">Install WMI Backward Compatibility package</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9aef3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9aef3-104">

<span> </span></span></span>

<span data-ttu-id="9aef3-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="9aef3-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="9aef3-106">Se você tentar executar o assistente de mesclagem do construtor de topologia sem instalar o pacote de compatibilidade com versões anteriores do WMI, o seguinte erro será exibido:</span><span class="sxs-lookup"><span data-stu-id="9aef3-106">If you attempt to run the Topology Builder Merge wizard without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="9aef3-107">![Mensagem de erro WMI](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "Mensagem de erro WMI")</span><span class="sxs-lookup"><span data-stu-id="9aef3-107">![WMI error message](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI error message")</span></span>

<span data-ttu-id="9aef3-108">Se você tentar executar o cmdlet **Merge-CsLegacytopology** sem instalar o pacote de compatibilidade com versões anteriores do WMI, o seguinte erro será exibido:</span><span class="sxs-lookup"><span data-stu-id="9aef3-108">If you attempt to run the **Merge-CsLegacytopology** cmdlet without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="9aef3-109">![Erro do provedor WMI do Windows PowerShell](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Erro do provedor WMI do Windows PowerShell")</span><span class="sxs-lookup"><span data-stu-id="9aef3-109">![Windows PowerShell WMI Provider Error](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI Provider Error")</span></span>

<span data-ttu-id="9aef3-110">Para instalar o pacote de compatibilidade com versões anteriores do WMI</span><span class="sxs-lookup"><span data-stu-id="9aef3-110">To install the WMI Backward Compatibility Package</span></span>

1.  <span data-ttu-id="9aef3-111">Na mídia de instalação, navegue até \\ Setup \\ AMD64 \\ Setup \\OCSWMIBC.MSI.</span><span class="sxs-lookup"><span data-stu-id="9aef3-111">From your installation media, navigate to \\SETUP\\AMD64\\SETUP\\OCSWMIBC.MSI.</span></span>

2.  <span data-ttu-id="9aef3-112">Instale o OCSWMIBC.MSI.</span><span class="sxs-lookup"><span data-stu-id="9aef3-112">Install OCSWMIBC.MSI.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9aef3-113">OCSWMIBC.msi deve ser instalado no computador em que o assistente de mesclagem do construtor de topologias é executado.</span><span class="sxs-lookup"><span data-stu-id="9aef3-113">OCSWMIBC.msi must be installed on the computer where the Topology Builder Merge wizard is run.</span></span> <span data-ttu-id="9aef3-114">No entanto, recomendamos instalar OCSWMIBC.msi em todos os servidores de front-end na sua topologia.</span><span class="sxs-lookup"><span data-stu-id="9aef3-114">However, we recommend installing OCSWMIBC.msi on all Front End servers in your topology.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9aef3-115">OCSWMIBC.msi pode ser instalado em qualquer computador no domínio que tenha os componentes principais do Lync Server 2013 e o Shell de gerenciamento do Lync Server 2013 instalado e tenha acesso à topologia do Office Communications Server 2007 R2 (provedor WMI para os serviços de domínio Active Directory (AD DS) e ao SQL Server).</span><span class="sxs-lookup"><span data-stu-id="9aef3-115">OCSWMIBC.msi can be installed on any computer in the domain that has the Lync Server 2013 Core Components and the Lync Server 2013 Management Shell installed, and has access to the Office Communications Server 2007 R2 topology (WMI provider to Active Directory Domain Services (AD DS) and SQL Server).</span></span>

    
    <span data-ttu-id="9aef3-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9aef3-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

