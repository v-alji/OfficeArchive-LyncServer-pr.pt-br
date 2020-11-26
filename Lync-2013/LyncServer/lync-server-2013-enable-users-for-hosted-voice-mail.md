---
title: 'Lync Server 2013: Habilitar usuários para correio de voz hospedado'
description: 'Lync Server 2013: habilitar usuários para caixa postal hospedada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for hosted voice mail
ms:assetid: fa559f8f-ef99-43a1-b580-9e998b95efb8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413062(v=OCS.15)
ms:contentKeyID: 48185919
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3853a70d433c09029a02f2ca6256b5988defdcb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437466"
---
# <a name="enable-users-for-hosted-voice-mail-in-lync-server-2013"></a><span data-ttu-id="5d88b-103">Habilitar usuários para correio de voz hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d88b-103">Enable users for hosted voice mail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d88b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d88b-104">

<span> </span></span></span>

<span data-ttu-id="5d88b-105">_**Tópico da última modificação:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="5d88b-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="5d88b-106">Siga o procedimento para habilitar os usuários do Lync Server 2013 para a caixa postal em um serviço do Exchange Unified Messaging (UM) hospedado.</span><span class="sxs-lookup"><span data-stu-id="5d88b-106">Follow the procedure to enable Lync Server 2013 users for voice mail on a hosted Exchange Unified Messaging (UM) service.</span></span>

<span data-ttu-id="5d88b-107">Para obter detalhes, consulte [Gerenciamento de usuários hospedados do Exchange no Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="5d88b-107">For details, see [Hosted Exchange user management in Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="5d88b-108">Para obter detalhes sobre o cmdlet [set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) , consulte a documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5d88b-108">For details about the [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5d88b-109">Para que um usuário do Lync Server 2013 possa ser habilitado para a caixa postal hospedada, uma política de caixa postal hospedada que se aplica à conta de usuário deve ser implantada.</span><span class="sxs-lookup"><span data-stu-id="5d88b-109">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to their user account must be deployed.</span></span> <span data-ttu-id="5d88b-110">Para obter detalhes, consulte <A href="lync-server-2013-hosted-voice-mail-policies.md">políticas de caixa postal hospedadas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5d88b-110">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-users-for-hosted-voice-mail"></a><span data-ttu-id="5d88b-111">Para habilitar usuários para a caixa postal hospedada</span><span class="sxs-lookup"><span data-stu-id="5d88b-111">To enable users for hosted voice mail</span></span>

1.  <span data-ttu-id="5d88b-112">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="5d88b-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="5d88b-113">Execute o cmdlet Set-CsUser para configurar a conta de usuário para a caixa postal hospedada.</span><span class="sxs-lookup"><span data-stu-id="5d88b-113">Run the Set-CsUser cmdlet to configure the user account for hosted voice mail.</span></span> <span data-ttu-id="5d88b-114">Por exemplo, execute:</span><span class="sxs-lookup"><span data-stu-id="5d88b-114">For example, run:</span></span>
    
        Set-CsUser -HostedVoiceMail $True -Identity "contoso\kenmyer"
    
    <span data-ttu-id="5d88b-115">O exemplo anterior define os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="5d88b-115">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="5d88b-116">O **HostedVoiceMail** permite que as chamadas de correio de voz de um usuário sejam roteadas para UM Exchange um hospedado.</span><span class="sxs-lookup"><span data-stu-id="5d88b-116">**HostedVoiceMail** enables a user’s voice mail calls to be routed to hosted Exchange UM.</span></span> <span data-ttu-id="5d88b-117">Ele também sinaliza o Microsoft Lync 2013 para iluminar o indicador "Call voice mail".</span><span class="sxs-lookup"><span data-stu-id="5d88b-117">It also signals Microsoft Lync 2013 to light up the “call voice mail” indicator.</span></span>
    
      - <span data-ttu-id="5d88b-118">**Identidade** especifica a conta de usuário a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="5d88b-118">**Identity** specifies the user account to be modified.</span></span> <span data-ttu-id="5d88b-119">O valor IDENTITY pode ser especificado usando qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="5d88b-119">The Identity value can be specified using any of the following formats:</span></span>
        
          - <span data-ttu-id="5d88b-120">O endereço SIP do usuário</span><span class="sxs-lookup"><span data-stu-id="5d88b-120">The user's SIP address</span></span>
        
          - <span data-ttu-id="5d88b-121">O nome de usuário do Active Directory do usuário do Active Directory</span><span class="sxs-lookup"><span data-stu-id="5d88b-121">The user's Active Directory User-Principal-Name</span></span>
        
          - <span data-ttu-id="5d88b-122">O nome de logon do domínio do usuário \\ (por exemplo, Contoso \\ kenmyer)</span><span class="sxs-lookup"><span data-stu-id="5d88b-122">The user's domain\\logon name (for example, contoso\\kenmyer)</span></span>
        
          - <span data-ttu-id="5d88b-123">Os serviços de domínio do Active Directory Display-Name do usuário (por exemplo, Ken Myer).</span><span class="sxs-lookup"><span data-stu-id="5d88b-123">The user's Active Directory Domain Services Display-Name (for example, Ken Myer).</span></span> <span data-ttu-id="5d88b-124">Se estiver usando o Display-Name como o valor de identidade, você pode usar o \* caractere curinga asterisco ().</span><span class="sxs-lookup"><span data-stu-id="5d88b-124">If using the Display-Name as the Identity value, you can use the asterisk (\*) wildcard character.</span></span> <span data-ttu-id="5d88b-125">Por exemplo, a identidade " \* Smith" retorna todos os usuários que têm um Display-Name que termina com o valor de cadeia de caracteres "Smith".</span><span class="sxs-lookup"><span data-stu-id="5d88b-125">For example, the Identity "\* Smith" returns all the users who have a Display-Name that ends with the string value "Smith".</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="5d88b-126">O nome de conta SAM do Active Directory do usuário não pode ser usado como o valor de identidade porque o SAM-Account-Name não é necessariamente exclusivo na floresta.</span><span class="sxs-lookup"><span data-stu-id="5d88b-126">The user’s Active Directory SAM-Account-Name cannot be used as the Identity value because the SAM-Account-Name is not necessarily unique in the forest.</span></span>

        
        <span data-ttu-id="5d88b-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d88b-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

