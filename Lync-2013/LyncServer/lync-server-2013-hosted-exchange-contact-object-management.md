---
title: 'Lync Server 2013: Gerenciamento de objeto de Contato no Exchange hospedado'
description: 'Lync Server 2013: Hosted gerenciamento de objeto de contato do Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Contact object management
ms:assetid: eead9d76-bc4f-4c1c-9779-683cb7a88410
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412978(v=OCS.15)
ms:contentKeyID: 48185748
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 691bcea10d3a4f8b523c6565f384d6c4c9a2a2a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427613"
---
# <a name="hosted-exchange-contact-object-management-in-lync-server-2013"></a><span data-ttu-id="23ed5-103">Gerenciamento de objeto de Contato no Exchange hospedado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23ed5-103">Hosted Exchange Contact object management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23ed5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23ed5-104">

<span> </span></span></span>

<span data-ttu-id="23ed5-105">_**Tópico da última modificação:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="23ed5-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="23ed5-106">Você precisa configurar um objeto de contato para cada número de autoatendimento e número de acesso do assinante em sua implantação interfuncional.</span><span class="sxs-lookup"><span data-stu-id="23ed5-106">You need to configure a Contact object for each auto-attendant number and subscriber access number in your cross-premises deployment.</span></span>

<span data-ttu-id="23ed5-107">Para a integração com o Exchange UM hospedado, ocsumutil.exe não pode ser usado para gerenciar objetos de contato, pois isso depende das configurações do Exchange UM do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="23ed5-107">For integration with hosted Exchange UM, ocsumutil.exe cannot be used to manage Contact objects, because it depends on Active Directory Exchange UM settings.</span></span> <span data-ttu-id="23ed5-108">Em uma implantação interfuncional, o Lync Server 2013 e o Exchange UM Hosted são instalados em florestas separadas sem nenhuma confiança entre elas.</span><span class="sxs-lookup"><span data-stu-id="23ed5-108">In a cross-premises deployment, Lync Server 2013 and hosted Exchange UM are installed in separate forests with no trust between them.</span></span> <span data-ttu-id="23ed5-109">Por motivos de segurança, os administradores do Lync Server 2013 não têm acesso direto às configurações do Active Directory de UM Exchange.</span><span class="sxs-lookup"><span data-stu-id="23ed5-109">For security reasons, Lync Server 2013 administrators have no direct access to Exchange UM Active Directory settings.</span></span> <span data-ttu-id="23ed5-110">Como resultado, o Lync Server 2013 fornece um modelo diferente para o gerenciamento de objetos de contato em um *espaço de endereço SIP compartilhado* que é acessível para o Lync Server 2013 e para o serviço um Hosted Exchange um.</span><span class="sxs-lookup"><span data-stu-id="23ed5-110">As a result, Lync Server 2013 provides a different model for managing Contact objects in a *shared SIP address space* that is accessible to both Lync Server 2013 and the hosted Exchange UM service.</span></span>

<div>

## <a name="hosted-contact-object-workflow"></a><span data-ttu-id="23ed5-111">Fluxo de trabalho do objeto de contato hospedado</span><span class="sxs-lookup"><span data-stu-id="23ed5-111">Hosted Contact Object Workflow</span></span>

<span data-ttu-id="23ed5-112">Veja a seguir as etapas gerais para trabalhar com o administrador de locatários do Exchange hospedado para gerenciar objetos de contato:</span><span class="sxs-lookup"><span data-stu-id="23ed5-112">The following are the general steps for working with your hosted Exchange tenant administrator to manage contact objects:</span></span>

1.  <span data-ttu-id="23ed5-113">O administrador do Exchange solicita números de telefone para o acesso do assinante do Exchange UM e objetos de contato do AutoAttendant.</span><span class="sxs-lookup"><span data-stu-id="23ed5-113">The Exchange administrator requests phone numbers for the Exchange UM subscriber access and auto-attendant Contact objects.</span></span>

2.  <span data-ttu-id="23ed5-114">O administrador do Lync Server 2013 cria um objeto de contato para cada número de telefone e atribui uma política de caixa postal hospedada a cada objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="23ed5-114">The Lync Server 2013 administrator creates a Contact object for each phone number and assigns a hosted voice mail policy to each Contact object.</span></span>

3.  <span data-ttu-id="23ed5-115">O administrador do Lync Server 2013 fornece os números de telefone para o administrador do Exchange.</span><span class="sxs-lookup"><span data-stu-id="23ed5-115">The Lync Server 2013 administrator provides the phone numbers to the Exchange administrator.</span></span>

4.  <span data-ttu-id="23ed5-116">O administrador do Exchange atribui os números de telefone aos planos de discagem de UM do Exchange apropriados para atendedores automáticos e acesso do Assinante.</span><span class="sxs-lookup"><span data-stu-id="23ed5-116">The Exchange administrator assigns the phone numbers to appropriate Exchange UM dial plans for auto attendants and subscriber access.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="23ed5-117">Não é necessário configurar nenhuma configuração de plano de discagem do Lync Server 2013 nos objetos de contato como há implantações locais.</span><span class="sxs-lookup"><span data-stu-id="23ed5-117">There is no need to configure any Lync Server 2013 dial plan settings on the Contact objects as there is with on-premises deployments.</span></span>



</div>

</div>

<div>

## <a name="configuring-hosted-contact-objects"></a><span data-ttu-id="23ed5-118">Configurar objetos de contato hospedados</span><span class="sxs-lookup"><span data-stu-id="23ed5-118">Configuring Hosted Contact Objects</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="23ed5-119">Os objetos de contato do Lync Server 2013 podem ser habilitados para o Exchange UM hospedado, uma política de caixa postal hospedada que se aplica a ele deve ser implantada.</span><span class="sxs-lookup"><span data-stu-id="23ed5-119">Before Lync Server 2013 Contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="23ed5-120">A política pode ser do escopo global, no nível do site ou por usuário, desde que ele se aplique ao objeto de contato que você deseja habilitar.</span><span class="sxs-lookup"><span data-stu-id="23ed5-120">The policy can be of global, site-level, or per-user scope, as long as it applies to the contact object you want to enable.</span></span> <span data-ttu-id="23ed5-121">Para obter detalhes, consulte <A href="lync-server-2013-hosted-voice-mail-policies.md">políticas de caixa postal hospedadas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="23ed5-121">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="23ed5-122">Para configurar objetos de contato de atendedor automático hospedado e de acesso ao assinante em uma implantação em várias instalações, você deve usar os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="23ed5-122">To configure hosted auto-attendant and subscriber access Contact objects in a cross-premises deployment, you must use the following cmdlets:</span></span>

  - <span data-ttu-id="23ed5-123">**New-CsExUmContact** cria um novo objeto de contato para um hospedado.</span><span class="sxs-lookup"><span data-stu-id="23ed5-123">**New-CsExUmContact** creates a new Contact object for hosted UM.</span></span>

  - <span data-ttu-id="23ed5-124">**Set-CsExUmContact** modifica um objeto de contato existente para o Exchange um hospedado.</span><span class="sxs-lookup"><span data-stu-id="23ed5-124">**Set-CsExUmContact** modifies an existing Contact object for hosted Exchange UM.</span></span>

<span data-ttu-id="23ed5-125">O exemplo a seguir cria um objeto de contato de atendente automático:</span><span class="sxs-lookup"><span data-stu-id="23ed5-125">The following example creates an auto-attendant Contact object:</span></span>

    New-CsExUmContact -SipAddress sip:exumaa1@fabrikam.com -RegistrarPool RedmondPool.litwareinc.com -OU "OU=ExUmContacts,DC=litwareinc,DC=com" -DisplayNumber 2065559876 -AutoAttendant $True

<span data-ttu-id="23ed5-126">Este exemplo cria um novo objeto de contato do Exchange UM com o endereço SIP sip:exumaa1@fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="23ed5-126">This example creates a new Exchange UM Contact object with the SIP address sip:exumaa1@fabrikam.com.</span></span> <span data-ttu-id="23ed5-127">O nome do pool onde o serviço registrador do Lync Server 2013 está em execução é RedmondPool.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="23ed5-127">The name of the pool where the Lync Server 2013 Registrar service is running is RedmondPool.litwareinc.com.</span></span> <span data-ttu-id="23ed5-128">A unidade organizacional do Active Directory na qual essas informações serão armazenadas é OU = ExUmContacts, DC = litwareinc, DC = com.</span><span class="sxs-lookup"><span data-stu-id="23ed5-128">The Active Directory organizational unit where this information will be stored is OU=ExUmContacts,DC=litwareinc,DC=com.</span></span> <span data-ttu-id="23ed5-129">O número de telefone do objeto de contato é 2065554567.</span><span class="sxs-lookup"><span data-stu-id="23ed5-129">The phone number of the Contact object is 2065554567.</span></span> <span data-ttu-id="23ed5-130">O parâmetro opcional-AutoAttendant $True especifica que esse objeto é um objeto de contato do atendente automático.</span><span class="sxs-lookup"><span data-stu-id="23ed5-130">The optional -AutoAttendant $True parameter specifies that this object is an auto-attendant Contact object.</span></span> <span data-ttu-id="23ed5-131">Definir o parâmetro-AutoAttendant como false (o padrão) especifica um objeto de contato do acesso do Assinante.</span><span class="sxs-lookup"><span data-stu-id="23ed5-131">Setting the -AutoAttendant parameter to False (the default) specifies a subscriber access Contact object.</span></span>

<span data-ttu-id="23ed5-132">Para obter detalhes sobre os cmdlets New-CsExUmContact e Set-CsExUmContact, consulte a documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="23ed5-132">For details about the New-CsExUmContact and Set-CsExUmContact cmdlets, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="23ed5-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23ed5-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

