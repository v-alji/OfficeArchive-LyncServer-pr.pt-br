---
title: 'Lync Server 2013: Criar objetos de contato para Exchange UM hospedado'
description: 'Lync Server 2013: criar objetos de contato para o Exchange UM hospedado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create contact objects for hosted Exchange UM
ms:assetid: a39be52f-488a-4523-ad5f-ce1f0d681959
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412765(v=OCS.15)
ms:contentKeyID: 48185045
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9760e2a39b5182f9b5194e364e059bddc6a63d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431971"
---
# <a name="create-contact-objects-for-hosted-exchange-um-in-lync-server-2013"></a><span data-ttu-id="531f6-103">Criar objetos de contato para Exchange UM hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="531f6-103">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="531f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="531f6-104">

<span> </span></span></span>

<span data-ttu-id="531f6-105">_**Tópico da última modificação:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="531f6-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="531f6-106">O procedimento a seguir explica como criar objetos de contato do atendedor automático (AA) ou do Subscriber Access (SA) para a Unificação de mensagens (UM) hospedada pelo Exchange.</span><span class="sxs-lookup"><span data-stu-id="531f6-106">The following procedure explains how to create Auto Attendant (AA) or Subscriber Access (SA) contact objects for hosted Exchange Unified Messaging (UM).</span></span>

<span data-ttu-id="531f6-107">Para obter detalhes, consulte [Gerenciamento de objeto de contato do Exchange hospedado no Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="531f6-107">For details, see [Hosted Exchange Contact object management in Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="531f6-108">Para obter detalhes sobre como configurar objetos de contato, consulte a documentação do Shell de gerenciamento do Lync Server para os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="531f6-108">For details about configuring contact objects, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="531f6-109">New-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="531f6-109">New-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExUmContact)

  - [<span data-ttu-id="531f6-110">Set-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="531f6-110">Set-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExUmContact)

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="531f6-111">Os objetos de contato do Lync Server 2013 podem ser habilitados para o Exchange UM hospedado, uma política de caixa postal hospedada que se aplica a ele deve ser implantada.</span><span class="sxs-lookup"><span data-stu-id="531f6-111">Before Lync Server 2013 contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="531f6-112">Para obter detalhes, consulte <A href="lync-server-2013-hosted-voice-mail-policies.md">políticas de caixa postal hospedadas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="531f6-112">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-aa-or-sa-contact-objects-for-hosted-exchange-um"></a><span data-ttu-id="531f6-113">Para criar objetos de contato AA ou SA para o Exchange UM hospedado</span><span class="sxs-lookup"><span data-stu-id="531f6-113">To create AA or SA contact objects for hosted Exchange UM</span></span>

1.  <span data-ttu-id="531f6-114">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="531f6-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="531f6-115">Execute o cmdlet New-CsExUmContact para criar qualquer objeto de contato necessário para a sua implantação.</span><span class="sxs-lookup"><span data-stu-id="531f6-115">Run the New-CsExUmContact cmdlet to create any contact objects required for your deployment.</span></span> <span data-ttu-id="531f6-116">Por exemplo, execute o seguinte para criar um objeto de contato AA e a SA:</span><span class="sxs-lookup"><span data-stu-id="531f6-116">For example, run the following to create an AA and an SA contact object:</span></span>
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumaa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101" -AutoAttendant $True
       ```
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumsa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101"
       ```
    
    <span data-ttu-id="531f6-117">Estes exemplos definem os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="531f6-117">These examples set the following parameters:</span></span>
    
      - <span data-ttu-id="531f6-118">**SipAddress** especifica o endereço SIP do objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="531f6-118">**SipAddress** specifies the SIP address of the contact object.</span></span> <span data-ttu-id="531f6-119">Isso deve ser um endereço que ainda não foi usado para configurar um objeto de usuário ou de contato nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="531f6-119">This must be an address that has not already been used to configure a user or contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="531f6-120">Esse valor deve estar no formato "SIP: \<*SIP address*\> ", conforme mostrado nos exemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="531f6-120">This value must be in the format “sip:\<*SIP address*\>“ as shown in the previous examples.</span></span>
    
      - <span data-ttu-id="531f6-121">**RegistrarPool** especifica o nome de domínio totalmente qualificado (FQDN) do pool no qual o serviço registrador está em execução.</span><span class="sxs-lookup"><span data-stu-id="531f6-121">**RegistrarPool** specifies the fully qualified domain name (FQDN) of the pool on which the Registrar service is running.</span></span>
        
        <div class=" ">
        

        > [!NOTE]  
        > <span data-ttu-id="531f6-122">Os objetos de contato de UM Exchange não podem ser movidos para pools que fazem parte de implantações do Lync Server 2013 anteriores ao Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="531f6-122">Exchange UM contact objects cannot be moved to pools that are part of Lync Server 2013 deployments prior to Lync Server 2013.</span></span>

        
        </div>
    
      - <span data-ttu-id="531f6-123">**Ou** especifica a unidade organizacional do Active Directory na qual esse objeto de contato será localizado.</span><span class="sxs-lookup"><span data-stu-id="531f6-123">**OU** specifies the Active Directory organizational unit where this contact object will be located.</span></span>
    
      - <span data-ttu-id="531f6-124">**DisplayNumber** especifica o número de telefone do objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="531f6-124">**DisplayNumber** specifies the telephone number of the contact object.</span></span> <span data-ttu-id="531f6-125">O número de telefone de cada objeto de contato deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="531f6-125">The phone number for each contact object must be unique.</span></span>
    
      - <span data-ttu-id="531f6-126">**AutoAttendant** especifica se o objeto de contato é um atendedor automático.</span><span class="sxs-lookup"><span data-stu-id="531f6-126">**AutoAttendant** specifies whether the Contact object is an Auto Attendant.</span></span> <span data-ttu-id="531f6-127">O atendedor automático oferece um conjunto de prompts de voz que permitem que os chamadores naveguem pelo sistema telefônico e atinjam a parte que desejam entrar em contato.</span><span class="sxs-lookup"><span data-stu-id="531f6-127">Auto Attendant provides a set of voice prompts that allow callers to navigate the phone system and reach the party that they want to contact.</span></span> <span data-ttu-id="531f6-128">Um valor de **false** (o padrão) para esse parâmetro indica um objeto de contato de acesso ao Assinante.</span><span class="sxs-lookup"><span data-stu-id="531f6-128">A value of **False** (the default) for this parameter indicates a Subscriber Access contact object.</span></span>

<span data-ttu-id="531f6-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="531f6-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

