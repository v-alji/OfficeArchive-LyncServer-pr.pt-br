---
title: 'Lync Server 2013: problemas com o teste de ambiente'
description: 'Lync Server 2013: problemas com o teste de ambiente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the environment test
ms:assetid: ff1fe0d3-35b2-41ef-87e7-6a61e9e1d2ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205421(v=OCS.15)
ms:contentKeyID: 48185970
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 551d7e914480e178e0558c1d17eefcf060c0688e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426715"
---
# <a name="issues-with-the-environment-test-in-lync-server-2013"></a><span data-ttu-id="ae527-103">Problemas com o teste de ambiente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae527-103">Issues with the environment test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae527-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae527-104">

<span> </span></span></span>

<span data-ttu-id="ae527-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="ae527-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="ae527-106">O analisador de práticas recomendadas fornece uma maneira de verificar se o ambiente do Lync Server 2013 é uma configuração compatível.</span><span class="sxs-lookup"><span data-stu-id="ae527-106">Best Practices Analyzer provides a way for you to verify that your Lync Server 2013 environment is a supported configuration.</span></span> <span data-ttu-id="ae527-107">Como parte da verificação dos serviços de domínio Active Directory, o analisador de práticas recomendadas faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ae527-107">As part of the Active Directory Domain Services check, Best Practices Analyzer does the following:</span></span>

  - <span data-ttu-id="ae527-108">Verifica a floresta dos serviços de domínio Active Directory e a preparação do esquema.</span><span class="sxs-lookup"><span data-stu-id="ae527-108">Verifies the Active Directory Domain Services forest and schema preparation.</span></span>

  - <span data-ttu-id="ae527-109">Identifica o número de domínios e sites de serviços de domínio Active Directory na implantação.</span><span class="sxs-lookup"><span data-stu-id="ae527-109">Identifies the number of Active Directory Domain Services sites and domains in the deployment.</span></span>

  - <span data-ttu-id="ae527-110">Verifica os níveis da floresta e do domínio.</span><span class="sxs-lookup"><span data-stu-id="ae527-110">Checks the forest and domain levels.</span></span>

  - <span data-ttu-id="ae527-111">Verifica a versão do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="ae527-111">Checks the domain controller version.</span></span>

  - <span data-ttu-id="ae527-112">Identifica o contexto de domínio, configuração e nomenclatura de esquema.</span><span class="sxs-lookup"><span data-stu-id="ae527-112">Identifies the domain, configuration, and schema naming context.</span></span>

  - <span data-ttu-id="ae527-113">Identifica o número de usuários habilitados.</span><span class="sxs-lookup"><span data-stu-id="ae527-113">Identifies the number of enabled users.</span></span>

  - <span data-ttu-id="ae527-114">Verifica onde as configurações globais dos serviços de domínio Active Directory estão armazenadas.</span><span class="sxs-lookup"><span data-stu-id="ae527-114">Checks where the global Active Directory Domain Services settings are stored.</span></span>

  - <span data-ttu-id="ae527-115">Verifica os pontos de conexão de serviço (SCPs) do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ae527-115">Checks for the service connection points (SCPs) for Lync Server.</span></span>

  - <span data-ttu-id="ae527-116">Identifica a versão do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ae527-116">Identifies the database version.</span></span>

<div>

## <a name="resolving-issues-with-the-environment"></a><span data-ttu-id="ae527-117">Solucionando problemas com o ambiente</span><span class="sxs-lookup"><span data-stu-id="ae527-117">Resolving Issues with the Environment</span></span>

<span data-ttu-id="ae527-118">Se o teste de ambiente encontrou problemas em seu ambiente, esses problemas provavelmente são causados por problemas com a configuração do Active Directory ou com o nível de software em execução em servidores específicos.</span><span class="sxs-lookup"><span data-stu-id="ae527-118">If the environment test found problems with your environment, these problems are probably caused by issues with your Active Directory configuration or the level of software running on specific servers.</span></span> <span data-ttu-id="ae527-119">Por exemplo, se o analisador de práticas recomendadas identificar os controladores de domínio em seu ambiente que executam o Windows Server 2000, ele emitirá um aviso e você precisará atualizar esses controladores de domínio para uma versão com suporte do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ae527-119">For example, if Best Practices Analyzer identifies any domain controllers in your environment that are running Windows Server 2000, it will issue a warning and you will need to upgrade those domain controllers to a supported version of Windows Server.</span></span>

<span data-ttu-id="ae527-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae527-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

