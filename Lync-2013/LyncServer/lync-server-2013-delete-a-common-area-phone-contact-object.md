---
title: 'Lync Server 2013: excluir um objeto de contato de telefone de área comum'
description: 'Lync Server 2013: excluir um objeto de contato de telefone de área comum.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a common area phone Contact object
ms:assetid: f4c139dc-f07c-4c75-9345-e291aea41173
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994087(v=OCS.15)
ms:contentKeyID: 51803999
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e918f7a46269f70577f28b2c3e55297959430721
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390346"
---
# <a name="delete-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="a7b07-103">Excluir um objeto de contato de telefone de área comum no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7b07-103">Delete a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7b07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7b07-104">

<span> </span></span></span>

<span data-ttu-id="a7b07-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="a7b07-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="a7b07-106">Talvez você queira excluir o objeto de contato associado a um telefone de área comum.</span><span class="sxs-lookup"><span data-stu-id="a7b07-106">You might want to delete the contact object associated with a common area phone.</span></span> <span data-ttu-id="a7b07-107">Por exemplo, se você remover o telefone de um funcionário de descanso, não será necessário ter um objeto de contato associado a esse telefone.</span><span class="sxs-lookup"><span data-stu-id="a7b07-107">For example, if you remove the phone from an employee lounge, there’s no need to have a contact object associated with that phone.</span></span> <span data-ttu-id="a7b07-108">O cmdlet **Remove-CsCommonAreaPhone** fornece uma maneira de você excluir contas de telefone comuns de área.</span><span class="sxs-lookup"><span data-stu-id="a7b07-108">The **Remove-CsCommonAreaPhone** cmdlet provides a way for you to delete common area phone accounts.</span></span> <span data-ttu-id="a7b07-109">Quando você executa esse cmdlet, o telefone é excluído da lista de telefones celulares comuns retornados por **Get-CsCommonAreaPhone**.</span><span class="sxs-lookup"><span data-stu-id="a7b07-109">When you run this cmdlet, the phone is deleted from the list of common area phones returned by **Get-CsCommonAreaPhone**.</span></span> <span data-ttu-id="a7b07-110">Além disso, o objeto de contato associado a esse telefone é excluído dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7b07-110">In addition, the contact object associated with that phone is deleted from Active Directory Domain Services.</span></span>

<span data-ttu-id="a7b07-111">Use **Remove-CsCommonAreaPhone** para remover um telefone de área comum ou todos os celulares comuns que têm um elemento comum, como um nome de exibição ou um país e um código de área.</span><span class="sxs-lookup"><span data-stu-id="a7b07-111">Use **Remove-CsCommonAreaPhone** to remove one common area phone or all common area phones that have a common element, such as a display name or country and area code.</span></span> <span data-ttu-id="a7b07-112">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7b07-112">You can run this cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a7b07-113">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="a7b07-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="removing-a-specified-common-area-phone"></a><span data-ttu-id="a7b07-114">Como remover um telefone de área comum especificado</span><span class="sxs-lookup"><span data-stu-id="a7b07-114">Removing a Specified Common Area Phone</span></span>

  - <span data-ttu-id="a7b07-115">O comando a seguir remove o telefone de área comum com o endereço SIP sip:mainlobby@litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="a7b07-115">The following command removes the common area phone with the SIP address sip:mainlobby@litwareinc.com:</span></span>
    
        Remove-CsCommonAreaPhone -Identity "sip:mainlobby@litwareinc.com"

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-display-name"></a><span data-ttu-id="a7b07-116">Removendo telefones celulares comuns com base em seu nome de exibição</span><span class="sxs-lookup"><span data-stu-id="a7b07-116">Removing Common Area Phones Based on Their Display Name</span></span>

  - <span data-ttu-id="a7b07-117">Esse comando Remove todos os telefones celulares comuns onde o nome de exibição inclui o valor de cadeia de caracteres "Building 14":</span><span class="sxs-lookup"><span data-stu-id="a7b07-117">This command removes all the common area phones where the display name includes the string value "Building 14":</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.DisplayName -match "Building 14"} | Remove-CsCommonAreaPhone

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-country-and-area-codes"></a><span data-ttu-id="a7b07-118">Removendo telefones celulares comuns com base em seus códigos de país e área</span><span class="sxs-lookup"><span data-stu-id="a7b07-118">Removing Common Area Phones Based on Their Country and Area Codes</span></span>

  - <span data-ttu-id="a7b07-119">Esse comando Remove todos os telefones fixos de área comuns para os Estados Unidos (código de país 1) e o código de área 425:</span><span class="sxs-lookup"><span data-stu-id="a7b07-119">This command removes all the common area phones for the United States (country code 1) and the area code 425:</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.LineUri  -match "^tel:\+1425"} | Remove-CsCommonAreaPhone

</div>

<span data-ttu-id="a7b07-120">Para obter detalhes, consulte o tópico da ajuda para o cmdlet [Remove-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) .</span><span class="sxs-lookup"><span data-stu-id="a7b07-120">For details, see the Help topic for the [Remove-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a7b07-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7b07-121">See Also</span></span>


[<span data-ttu-id="a7b07-122">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="a7b07-122">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="a7b07-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7b07-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

