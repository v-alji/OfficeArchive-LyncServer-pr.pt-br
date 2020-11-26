---
title: 'Lync Server 2013: exibir configurações do servidor de borda'
description: 'Lync Server 2013: exibir configurações do servidor de borda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Edge Server settings
ms:assetid: 684154cc-cffc-4d2e-8baa-be52c625e5d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747890(v=OCS.15)
ms:contentKeyID: 63969612
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4318b8c97f53f267bb79953af504977f6437214d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446280"
---
# <a name="view-edge-server-settings-in-lync-server-2013"></a><span data-ttu-id="2c3ee-103">Exibir as configurações do servidor de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c3ee-103">View Edge Server settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c3ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c3ee-104">

<span> </span></span></span>

<span data-ttu-id="2c3ee-105">_**Tópico da última modificação:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="2c3ee-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="2c3ee-106">As configurações gerais do servidor de borda devem ser analisadas nos dados do banco de dados de gerenciamento de configuração, para ajudar a garantir que todas as alterações tenham sido documentadas de acordo com os procedimentos definidos de controle de alterações.</span><span class="sxs-lookup"><span data-stu-id="2c3ee-106">General Edge Server configurations should be reviewed against the data in the configuration management database—to help guarantee that all changes were documented as per the defined change control procedures.</span></span>

<span data-ttu-id="2c3ee-107">Verificações adicionais podem incluir aquelas descritas nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="2c3ee-107">Additional checks could include those that are described in the following sections:</span></span>

<div>

## <a name="verify-the-allow-and-block-lists"></a><span data-ttu-id="2c3ee-108">Verificar as listas permitir e bloquear</span><span class="sxs-lookup"><span data-stu-id="2c3ee-108">Verify the Allow and block lists</span></span>

<span data-ttu-id="2c3ee-109">Verifique as listas "permitir" e "bloquear" do URI SIP para domínios federados – para determinar se os namespaces listados ainda são válidos.</span><span class="sxs-lookup"><span data-stu-id="2c3ee-109">Verify the SIP URI "Allow" and "Block" lists for Federated domains—to determine whether listed namespaces are still valid.</span></span>

<span data-ttu-id="2c3ee-110">Você pode usar o Windows PowerShell para ver as listas autorizadas e bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="2c3ee-110">You can use Windows PowerShell to view the allowed and blocked lists.</span></span> <span data-ttu-id="2c3ee-111">Para examinar os domínios na lista de domínios permitidos, execute o seguinte comando do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="2c3ee-111">To review the domains on the Allowed Domains list, run the following Windows PowerShell command:</span></span>

`Get-CsAllowedDomain`

<span data-ttu-id="2c3ee-112">Esse comando retorna informações semelhantes a esta para os domínios na lista de domínios permitidos:</span><span class="sxs-lookup"><span data-stu-id="2c3ee-112">That command returns information similar to this for the domains on the Allowed Domains list:</span></span>

<span data-ttu-id="2c3ee-113">Identidade: contoso.com</span><span class="sxs-lookup"><span data-stu-id="2c3ee-113">Identity : contoso.com</span></span>

<span data-ttu-id="2c3ee-114">Domínio: contoso.com</span><span class="sxs-lookup"><span data-stu-id="2c3ee-114">Domain : contoso.com</span></span>

<span data-ttu-id="2c3ee-115">ProxyFqdn :</span><span class="sxs-lookup"><span data-stu-id="2c3ee-115">ProxyFqdn :</span></span>

<span data-ttu-id="2c3ee-116">Come</span><span class="sxs-lookup"><span data-stu-id="2c3ee-116">Comment :</span></span>

<span data-ttu-id="2c3ee-117">MarkForMonitoring: false</span><span class="sxs-lookup"><span data-stu-id="2c3ee-117">MarkForMonitoring : False</span></span>

<span data-ttu-id="2c3ee-118">Come</span><span class="sxs-lookup"><span data-stu-id="2c3ee-118">Comment :</span></span>

<span data-ttu-id="2c3ee-119">Para revisar os domínios na lista de domínios bloqueados, use este comando:</span><span class="sxs-lookup"><span data-stu-id="2c3ee-119">To review the domains on the blocked domains list, use this command:</span></span>

`Get-CsBlockedDomain`

<span data-ttu-id="2c3ee-120">Por sua vez, você receberá informações como essa para cada domínio bloqueado:</span><span class="sxs-lookup"><span data-stu-id="2c3ee-120">In turn, you'll receive information such as this for each blocked domain:</span></span>

<span data-ttu-id="2c3ee-121">Identidade: tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="2c3ee-121">Identity : tailspintoys.com</span></span>

<span data-ttu-id="2c3ee-122">Domínio: tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="2c3ee-122">Domain : tailspintoys.com</span></span>

<span data-ttu-id="2c3ee-123">O Windows PowerShell também permite que você verifique se você pode se conectar a domínios na lista de domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="2c3ee-123">Windows PowerShell also enables you to verify that you can connection to the domains on your Allowed Domains list.</span></span> <span data-ttu-id="2c3ee-124">Por exemplo, esse comando verifica a conexão entre o servidor de borda (o TargetFqdn) e o domínio federado contoso.com:</span><span class="sxs-lookup"><span data-stu-id="2c3ee-124">For example, this command verifies the connection between your Edge Server (the TargetFqdn) and the federated domain contoso.com:</span></span>

`Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"`

<span data-ttu-id="2c3ee-125">E esse comando verifica a conexão entre o servidor de borda e todos os domínios encontrados na lista de domínios permitidos:</span><span class="sxs-lookup"><span data-stu-id="2c3ee-125">And this command verifies the connection between your Edge Server and all of the domains found on your Allowed Domains list:</span></span>

`Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Domain}`

</div>

<div>

## <a name="verify-multiple-edge-servers-are-identical"></a><span data-ttu-id="2c3ee-126">Verificar se vários servidores de borda são idênticos</span><span class="sxs-lookup"><span data-stu-id="2c3ee-126">Verify multiple Edge Servers are identical</span></span>

<span data-ttu-id="2c3ee-127">Se vários servidores de borda forem implantados em uma matriz de carga balanceada, recomendamos verificar se todos os servidores de borda na matriz estão configurados da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="2c3ee-127">If multiple Edge Servers are deployed in a load balanced array, we recommend verifying that all Edge Servers in the array are configured in the same manner.</span></span>

<span data-ttu-id="2c3ee-128">Você pode visualizar as configurações dos servidores de borda no painel de detalhes da extensão 2013 do Lync Server para o snap-in Gerenciamento do computador.</span><span class="sxs-lookup"><span data-stu-id="2c3ee-128">You can view settings for Edge Servers in the details pane of the Lync Server 2013 extension for the Computer Management snap-in.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2c3ee-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c3ee-129">See Also</span></span>


[<span data-ttu-id="2c3ee-130">Get-CsAllowedDomain</span><span class="sxs-lookup"><span data-stu-id="2c3ee-130">Get-CsAllowedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAllowedDomain)  
[<span data-ttu-id="2c3ee-131">Get-CsBlockedDomain</span><span class="sxs-lookup"><span data-stu-id="2c3ee-131">Get-CsBlockedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsBlockedDomain)  
[<span data-ttu-id="2c3ee-132">Test-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="2c3ee-132">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
  

<span data-ttu-id="2c3ee-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c3ee-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

