---
title: 'Lync Server 2013: Configurando a página de ingresso na reunião'
description: 'Lync Server 2013: Configurando a página de ingresso na reunião.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the meeting join page
ms:assetid: 45880423-47f4-49af-b825-cbd8e3fc1046
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204861(v=OCS.15)
ms:contentKeyID: 48184037
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0e7c9dde0fdb6829da7bd11e16261a4bd76b7554
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432531"
---
# <a name="configuring-the-meeting-join-page-in-lync-server-2013"></a><span data-ttu-id="1a87a-103">Configurando a página de ingresso na reunião no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a87a-103">Configuring the meeting join page in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1a87a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1a87a-104">

<span> </span></span></span>

<span data-ttu-id="1a87a-105">_**Tópico da última modificação:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="1a87a-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="1a87a-106">Quando um usuário clica em um link de reunião em uma solicitação de reunião, a página ingressar na reunião detecta se um cliente do Lync 2013 já está instalado no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="1a87a-106">When a user clicks a meeting link in a meeting request, the meeting join page detects whether a Lync 2013 client is already installed on the user’s computer.</span></span> <span data-ttu-id="1a87a-107">Se um cliente já estiver instalado, o cliente abrirá e ingressará na reunião.</span><span class="sxs-lookup"><span data-stu-id="1a87a-107">If a client is already installed, the client opens and joins the meeting.</span></span> <span data-ttu-id="1a87a-108">Se um cliente não estiver instalado, por padrão, a versão 2013 do Lync Web App será aberta.</span><span class="sxs-lookup"><span data-stu-id="1a87a-108">If a client is not installed, by default the 2013 version of Lync Web App opens.</span></span>

<span data-ttu-id="1a87a-109">Você pode modificar o comportamento da página de associação de reunião se desejar permitir que os usuários ingressem em reuniões com o Office Communicator 2007 R2 ou o Lync 2010 Attendant.</span><span class="sxs-lookup"><span data-stu-id="1a87a-109">You can modify the behavior of the meeting join page if you want to allow users to join meetings with Office Communicator 2007 R2 or Lync 2010 Attendant.</span></span> <span data-ttu-id="1a87a-110">Essas opções de configuração foram removidas do painel de controle do Lync Server 2013, mas você as configura usando o cmdlet Set-CsWebServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1a87a-110">These configuration options have been removed from the Lync Server 2013 Control Panel, but you configure them by using the Set-CsWebServiceConfiguration cmdlet.</span></span>

### <a name="meeting-join-page-set-cswebserviceconfiguration-parameters"></a><span data-ttu-id="1a87a-111">Página de ingresso na reunião Set-CsWebServiceConfiguration parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a87a-111">Meeting Join Page Set-CsWebServiceConfiguration Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a87a-112">Set-CsWebServiceConfiguration parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a87a-112">Set-CsWebServiceConfiguration Parameter</span></span></th>
<th><span data-ttu-id="1a87a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a87a-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a87a-114">ShowJoinUsingLegacyClientLink</span><span class="sxs-lookup"><span data-stu-id="1a87a-114">ShowJoinUsingLegacyClientLink</span></span></p></td>
<td><p><span data-ttu-id="1a87a-115">Se definido como true, os usuários que ingressam em uma reunião usando um aplicativo cliente que não seja o Lync terão a oportunidade de ingressar na reunião usando o Office Communicator 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="1a87a-115">If set to True, users joining a meeting by using a client application other than Lync will be given the opportunity to join the meeting by using Office Communicator 2007 R2.</span></span> <span data-ttu-id="1a87a-116">O valor padrão é False.</span><span class="sxs-lookup"><span data-stu-id="1a87a-116">The default value is False.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a87a-117">ShowAlternateJoinOptionsExpanded</span><span class="sxs-lookup"><span data-stu-id="1a87a-117">ShowAlternateJoinOptionsExpanded</span></span></p></td>
<td><p><span data-ttu-id="1a87a-118">Quando definida como true, as opções alternativas para ingressar em uma conferência online (como o Office Communicator 2007 R2) serão expandidas automaticamente e exibidas para os usuários.</span><span class="sxs-lookup"><span data-stu-id="1a87a-118">When set to True then alternate options for joining an online conference (such as Office Communicator 2007 R2) will automatically be expanded and shown to users.</span></span> <span data-ttu-id="1a87a-119">Quando definido como falso (o valor padrão), essas opções estarão disponíveis, mas o usuário precisará exibir a lista de opções para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="1a87a-119">When set to False (the default value) these options will be available, but the user will have to display the list of options for themselves.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-the-meeting-join-page-by-using-lync-server-2013-management-shell"></a><span data-ttu-id="1a87a-120">Para configurar a página ingressar na reunião usando o Shell de gerenciamento do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1a87a-120">To configure the meeting join page by using Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="1a87a-121">Inicie o Shell de gerenciamento do Lync Server 2013: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="1a87a-121">Start the Lync Server 2013 Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1a87a-122">Para exibir as configurações de serviço Web, execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1a87a-122">To view the web service configuration settings, run the following cmdlet:</span></span>
    
        Get-CsWebServiceConfiguration

3.  <span data-ttu-id="1a87a-123">Execute o comando a seguir, com os parâmetros definidos como verdadeiro ou falso, dependendo da sua preferência (para obter detalhes sobre os parâmetros para esse cmdlet, consulte [set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration) na documentação do Shell de gerenciamento do Lync Server 2013):</span><span class="sxs-lookup"><span data-stu-id="1a87a-123">Run the following command, with the parameters set to True or False, depending on your preference (for details about the parameters for this cmdlet, see [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration) in the Lync Server 2013 Management Shell documentation):</span></span>
    
        Set-CsWebServiceConfiguration -Identity global -ShowJoinUsingLegacyClientLink $True

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1a87a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a87a-124">See Also</span></span>


[<span data-ttu-id="1a87a-125">Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a87a-125">Set-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)  
  

<span data-ttu-id="1a87a-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1a87a-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

