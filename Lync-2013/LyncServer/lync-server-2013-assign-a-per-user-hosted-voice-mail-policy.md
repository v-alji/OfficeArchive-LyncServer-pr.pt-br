---
title: 'Lync Server 2013: atribuir uma política de correio de voz hospedada por usuário'
description: 'Lync Server 2013: atribua uma política de correio de voz hospedada por usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user hosted voice mail policy
ms:assetid: d44c71a0-4407-4ab4-b7e0-d671dde3425f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398919(v=OCS.15)
ms:contentKeyID: 48185456
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 071d504c452b4d3adb1b636cb5c4ff8835200107
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440518"
---
# <a name="assign-a-per-user-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="ecb14-103">Atribuir uma política de correio de voz hospedada por usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecb14-103">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>

 


<span data-ttu-id="ecb14-104">A implantação de uma ou mais políticas de correio de voz hospedadas por usuário é opcional.</span><span class="sxs-lookup"><span data-stu-id="ecb14-104">Deploying one or more per-user hosted voice mail policies is optional.</span></span> <span data-ttu-id="ecb14-105">Se você implantar políticas por usuário, deverá atribuí-las explicitamente a usuários, grupos ou objetos de contato.</span><span class="sxs-lookup"><span data-stu-id="ecb14-105">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact objects.</span></span>

<span data-ttu-id="ecb14-106">Para obter detalhes sobre como atribuir ou remover a atribuição de políticas de correio de voz hospedadas por usuário, consulte a documentação do Shell de gerenciamento do Lync Server para os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="ecb14-106">For details about assigning or removing the assignment of per-user hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="ecb14-107">Grant-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="ecb14-107">Grant-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="ecb14-108">Remove-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="ecb14-108">Remove-CsHostedVoicemailPolicy</span></span>

## <a name="to-assign-a-per-user-hosted-voice-mail-policy"></a><span data-ttu-id="ecb14-109">Para atribuir uma política de correio de voz hospedada por usuário</span><span class="sxs-lookup"><span data-stu-id="ecb14-109">To assign a per-user hosted voice mail policy</span></span>

1.  <span data-ttu-id="ecb14-110">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ecb14-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="ecb14-111">Execute o cmdlet Grant-CsHostedVoicemailPolicy para atribuir a política de caixa postal hospedada por usuário a usuários individuais, grupos e objetos de contato.</span><span class="sxs-lookup"><span data-stu-id="ecb14-111">Run the Grant-CsHostedVoicemailPolicy cmdlet to assign the per-user hosted voice mail policy to individual users, groups, and contact objects.</span></span> <span data-ttu-id="ecb14-112">Por exemplo, execute:</span><span class="sxs-lookup"><span data-stu-id="ecb14-112">For example, run:</span></span>
    
        Grant-CsHostedVoicemailPolicy -Identity "Ken Myer" -PolicyName ExRedmond
    
    <span data-ttu-id="ecb14-113">Este exemplo atribuiu a política de caixa postal hospedada pela webmail ao usuário Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="ecb14-113">This example assigned the ExRedmond hosted voice mail policy to user Ken Myer.</span></span>
    
    <span data-ttu-id="ecb14-114">**Identidade** especifica a conta de usuário a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="ecb14-114">**Identity** specifies the user account to be modified.</span></span> <span data-ttu-id="ecb14-115">O valor IDENTITY pode ser especificado usando qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="ecb14-115">The Identity value can be specified using any of the following formats:</span></span>
    
      - <span data-ttu-id="ecb14-116">O endereço SIP do usuário</span><span class="sxs-lookup"><span data-stu-id="ecb14-116">The user's SIP address</span></span>
    
      - <span data-ttu-id="ecb14-117">O nome de usuário do Active Directory do usuário do Active Directory</span><span class="sxs-lookup"><span data-stu-id="ecb14-117">The user's Active Directory User-Principal-Name</span></span>
    
      - <span data-ttu-id="ecb14-118">O nome de logon do domínio do usuário \\ (por exemplo, Contoso \\ kenmyer)</span><span class="sxs-lookup"><span data-stu-id="ecb14-118">The user's domain\\logon name (for example, contoso\\kenmyer)</span></span>
    
      - <span data-ttu-id="ecb14-119">Os serviços de domínio do Active Directory Display-Name do usuário (por exemplo, Ken Myer).</span><span class="sxs-lookup"><span data-stu-id="ecb14-119">The user's Active Directory Domain Services Display-Name (for example, Ken Myer).</span></span> <span data-ttu-id="ecb14-120">Se estiver usando o Display-Name como o valor de identidade, você pode usar o \* caractere curinga asterisco ().</span><span class="sxs-lookup"><span data-stu-id="ecb14-120">If using the Display-Name as the Identity value, you can use the asterisk (\*) wildcard character.</span></span> <span data-ttu-id="ecb14-121">Por exemplo, a identidade " \* Smith" retorna todos os usuários que têm um Display-Name que termina com o valor de cadeia de caracteres "Smith".</span><span class="sxs-lookup"><span data-stu-id="ecb14-121">For example, the Identity "\* Smith" returns all the users who have a Display-Name that ends with the string value "Smith".</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="ecb14-122">O nome de conta SAM do Active Directory do usuário não pode ser usado como o valor de identidade porque o SAM-Account-Name não é necessariamente exclusivo na floresta.</span><span class="sxs-lookup"><span data-stu-id="ecb14-122">The user’s Active Directory SAM-Account-Name cannot be used as the Identity value because the SAM-Account-Name is not necessarily unique in the forest.</span></span>


