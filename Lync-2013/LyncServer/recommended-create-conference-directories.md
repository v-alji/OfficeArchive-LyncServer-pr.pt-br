---
title: (Recomendado) Criar diretórios de conferência
description: Usar Criar diretórios de conferências.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: (Recommended) Create Conference Directories
ms:assetid: 787f4c94-1c96-468a-a74d-e06b7bd4b8a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn832056(v=OCS.15)
ms:contentKeyID: 63146389
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b14982893fbc14a87818875a787d0f776da84ae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443262"
---
# <a name="recommended-create-conference-directories"></a><span data-ttu-id="fb156-103">(Recomendado) Criar diretórios de conferência</span><span class="sxs-lookup"><span data-stu-id="fb156-103">(Recommended) Create Conference Directories</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb156-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb156-104">

<span> </span></span></span>

<span data-ttu-id="fb156-105">_**Tópico da última modificação:** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="fb156-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="fb156-106">As pastas de conferência mantêm um mapeamento entre a ID de reunião alfanumérica que um participante usa para ingressar em uma conferência ao usar o Lync 2013 e a ID de conferência somente numérico que um participante de conferência discada usa para participar da conferência.</span><span class="sxs-lookup"><span data-stu-id="fb156-106">Conference directories maintain a mapping between the alphanumeric meeting ID that a participant uses to join a conference when using Lync 2013, and the numeric-only conference ID that a dial-in conferencing participant uses to join the conference.</span></span> <span data-ttu-id="fb156-107">O formato do ID de conferência é como segue:</span><span class="sxs-lookup"><span data-stu-id="fb156-107">The format of the conference ID is as follows:</span></span>

    <housekeeping digit (1 digit)><conference directory (usually 1-2 digits)><conference number (variable number of digits><check digit (1 digit)>

<span data-ttu-id="fb156-108">Criar vários diretórios de conferência garantirá que os IDs de conferência sejam curtos até que uma quantidade significativa de conferências seja criada.</span><span class="sxs-lookup"><span data-stu-id="fb156-108">Creating multiple conference directories will ensure that conference IDs will stay short until a significant amount of conferences have been created.</span></span> <span data-ttu-id="fb156-109">Em uma organização com um número comum de conferências por usuário, recomendamos criar um diretório de conferência para cada 999 usuários no pool.</span><span class="sxs-lookup"><span data-stu-id="fb156-109">In an organization with a typical number of conferences per user, we recommend that you create one conference directory for every 999 users in the pool.</span></span> <span data-ttu-id="fb156-110">Usando esta diretriz, as IDs de conferência geralmente podem ser mantidas pequenas.</span><span class="sxs-lookup"><span data-stu-id="fb156-110">Using this guideline the conference IDs can generally be kept small.</span></span> <span data-ttu-id="fb156-111">No entanto, assim que o número de diretórios de conferência (em todos os pools) ultrapassar 9, o tamanho do ID de conferência aumentará para suportar conferências adicionais.</span><span class="sxs-lookup"><span data-stu-id="fb156-111">However, once the number of conference directories (across the pools) exceed 9, the Conference ID length will grow to support additional conferences.</span></span>

<div>

## <a name="creating-a-conference-directory"></a><span data-ttu-id="fb156-112">Criando um diretório de conferência</span><span class="sxs-lookup"><span data-stu-id="fb156-112">Creating a conference directory</span></span>

1.  <span data-ttu-id="fb156-113">No Shell de gerenciamento do Lync Server, digite o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fb156-113">In Lync Server Management Shell, type the following cmdlet:</span></span>
    
        New-CsConferenceDirectory -Identity <XdsGlobalRelativeIdentity> -HomePool <String> [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
    
    <span data-ttu-id="fb156-114">Por exemplo, o seguinte cria um diretório de conferência com a identidade 42, hospedada na atl-cs-001.litwareinc.com do pool:</span><span class="sxs-lookup"><span data-stu-id="fb156-114">For example, the following creates a conference directory with the identity 42, hosted on the pool atl-cs-001.litwareinc.com:</span></span>
    
        New-CsConferenceDirectory -Identity 42 -HomePool "atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fb156-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb156-115">See Also</span></span>


[<span data-ttu-id="fb156-116">Requisitos de conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb156-116">Dial-in conferencing requirements in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-requirements.md)  


[<span data-ttu-id="fb156-117">New-CsConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="fb156-117">New-CsConferenceDirectory</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsConferenceDirectory)  
  

<span data-ttu-id="fb156-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb156-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

