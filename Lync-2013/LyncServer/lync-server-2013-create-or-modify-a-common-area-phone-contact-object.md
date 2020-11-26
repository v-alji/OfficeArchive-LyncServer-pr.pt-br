---
title: 'Lync Server 2013: criar ou modificar um objeto de contato de telefone de área comum'
description: 'Lync Server 2013: crie ou modifique um objeto de contato de telefone de área comum.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a common area phone Contact object
ms:assetid: eec33ad1-e4f2-49b2-91d6-d5a9d2e1714b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994083(v=OCS.15)
ms:contentKeyID: 51803995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5ede23f495a63b2d556b556817d4171a08723
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431838"
---
# <a name="create-or-modify-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="a96ff-103">Criar ou modificar um objeto de contato de telefone de área comum no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a96ff-103">Create or modify a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a96ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a96ff-104">

<span> </span></span></span>

<span data-ttu-id="a96ff-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="a96ff-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="a96ff-106">Para criar objetos de contato dos serviços de domínio Active Directory para todos os seus telefones de área comuns, use o cmdlet **New-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="a96ff-106">To create Active Directory Domain Services contact objects for all your common area phones, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="a96ff-107">Esse cmdlet pode criar novos objetos de contato para uso com telefones de área comuns ou pode associar objetos de contato existentes a um novo telefone comum de área.</span><span class="sxs-lookup"><span data-stu-id="a96ff-107">This cmdlet can either create new contact objects for use with common area phones, or it can associate existing contact objects with a new common area phone.</span></span> <span data-ttu-id="a96ff-108">Para modificar as propriedades dos objetos de contato associados a telefones de área comuns, use o cmdlet **set-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="a96ff-108">To modify the properties of the contact objects associated with common area phones, use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="a96ff-109">Os parâmetros opcionais para **set-CsCommonAreaPhone** permitem que você altere itens, como o nome de exibição do Active Directory do contato ou o URI (Uniform Resource Identifier) da linha associado ao telefone e habilite e desabilite a conta para uso com o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a96ff-109">Optional parameters for **Set-CsCommonAreaPhone** enable you to change items, such as the contact’s Active Directory display name or the line Uniform Resource Identifier (URI) associated with the phone, and enable and disable the account for use with Lync Server.</span></span> <span data-ttu-id="a96ff-110">Para obter detalhes sobre todas as modificações disponíveis, consulte a seção parâmetros em [set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone).</span><span class="sxs-lookup"><span data-stu-id="a96ff-110">For details about all the available modifications, see the Parameters section at [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone).</span></span> <span data-ttu-id="a96ff-111">Para obter detalhes sobre os parâmetros **New-CsCommonAreaPhone** , consulte [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone).</span><span class="sxs-lookup"><span data-stu-id="a96ff-111">For details about **New-CsCommonAreaPhone** parameters, see [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone).</span></span>

<span data-ttu-id="a96ff-112">Você pode executar esses dois cmdlets a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a96ff-112">You can run these two cmdlets from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a96ff-113">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="a96ff-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="creating-a-common-area-phone-contact-object"></a><span data-ttu-id="a96ff-114">Criando um objeto de contato de telefone de área comum</span><span class="sxs-lookup"><span data-stu-id="a96ff-114">Creating a common area phone contact object</span></span>

  - <span data-ttu-id="a96ff-115">Para criar um novo objeto de contato de telefone de área comum, use o cmdlet **New-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="a96ff-115">To create a new common area phone contact object, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="a96ff-116">No mínimo, você deve fornecer as seguintes informações ao criar um objeto de contato:</span><span class="sxs-lookup"><span data-stu-id="a96ff-116">At a minimum, you must supply the following information when creating a contact object:</span></span>
    
      - <span data-ttu-id="a96ff-117">**LineUri**: o número de telefone atribuído ao telefone comum da área.</span><span class="sxs-lookup"><span data-stu-id="a96ff-117">**LineUri**: The telephone number assigned to the common area phone.</span></span> <span data-ttu-id="a96ff-118">Observe que você deve usar o formato E. 164 ao especificar o número de telefone.</span><span class="sxs-lookup"><span data-stu-id="a96ff-118">Note that you must use the E.164 format when specifying the phone number.</span></span>
    
      - <span data-ttu-id="a96ff-119">**RegistrarPool**: o nome de domínio totalmente qualificado (FQDN) do pool de registradores que hospedará o objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="a96ff-119">**RegistrarPool**: The fully qualified domain name (FQDN) of the Registrar pool that will host the contact object.</span></span>
    
      - <span data-ttu-id="a96ff-120">**Ou**: nome diferenciado do contêiner do Active Directory em que o objeto de contato será criado.</span><span class="sxs-lookup"><span data-stu-id="a96ff-120">**OU**: Distinguished name of the Active Directory container where the contact object will be created.</span></span>
    
    <span data-ttu-id="a96ff-121">Também recomendamos que você forneça um nome de exibição dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a96ff-121">We also recommend that you provide an Active Directory Domain Services display name.</span></span> <span data-ttu-id="a96ff-122">Caso contrário, será necessário usar um GUID para especificar a identidade do telefone.</span><span class="sxs-lookup"><span data-stu-id="a96ff-122">Otherwise, you will need to use a GUID to specify the phone Identity.</span></span> <span data-ttu-id="a96ff-123">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a96ff-123">For example:</span></span>
    
        New-CsCommonAreaPhone -LineUri "tel:+12065551219" -RegistrarPool "atl-cs-001.litwareinc.com" -OU "OU=Phones,dc=litwareinc,dc=com" -DisplayName "Lobby"

</div>

<div>

## <a name="modifying-a-common-area-phone-contact-object"></a><span data-ttu-id="a96ff-124">Modificando um objeto de contato de telefone de área comum</span><span class="sxs-lookup"><span data-stu-id="a96ff-124">Modifying a common area phone contact object</span></span>

  - <span data-ttu-id="a96ff-125">Para modificar as propriedades de um telefone de área comum existente, objeto de contato use o cmdlet **set-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="a96ff-125">To modify the properties of an existing common area phone, contact object use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="a96ff-126">Por exemplo, esse comando configura o endereço SIP para o telefone de área comum com o lobby DisplayName:</span><span class="sxs-lookup"><span data-stu-id="a96ff-126">For example, this command configures the SIP address for the common area phone with the DisplayName Lobby:</span></span>
    
        Set-CsCommonAreaPhone -Identity "Lobby" -SipAddress "sip:lobby@litwareinc.com"

</div>

<span data-ttu-id="a96ff-127">Para obter detalhes, consulte os tópicos da ajuda para o cmdlet [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) e o cmdlet [set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) .</span><span class="sxs-lookup"><span data-stu-id="a96ff-127">For details, see the Help topics for the [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) cmdlet and the [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) cmdlet.</span></span>

<span data-ttu-id="a96ff-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a96ff-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

