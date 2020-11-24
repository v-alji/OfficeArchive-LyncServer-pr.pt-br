---
title: Combinando cmdlets do Skype for Business online com outros cmdlets do Windows PowerShell no
description: Combinando cmdlets do Skype for Business online com outros cmdlets do Windows PowerShell em.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets
ms:assetid: 8bb8800a-f966-4570-8c8b-db87a91ad783
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362816(v=OCS.15)
ms:contentKeyID: 56558835
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bd18f60891d48a54eb2f77f189ea8417e0b5e93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390014"
---
# <a name="combining-skype-for-business-online-cmdlets-with-other-windows-powershell-cmdlets-in"></a><span data-ttu-id="83c81-103">Combinando cmdlets do Skype for Business online com outros cmdlets do Windows PowerShell no</span><span class="sxs-lookup"><span data-stu-id="83c81-103">Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets in</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83c81-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83c81-104">

<span> </span></span></span>

<span data-ttu-id="83c81-105">_**Tópico da última modificação:** 2013-07-05_</span><span class="sxs-lookup"><span data-stu-id="83c81-105">_**Topic Last Modified:** 2013-07-05_</span></span>

<span data-ttu-id="83c81-106">Quando você se conecta ao Skype for Business online usando o Windows PowerShell, cerca de 40 cmdlets do Skype for Business online estarão disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="83c81-106">When you connect to Skype for Business Online by using Windows PowerShell, approximately 40 Skype for Business Online cmdlets will available for your use.</span></span> <span data-ttu-id="83c81-107">No entanto, você não está limitado a usar apenas os cmdlets do 40 ao gerenciar o Skype for Business online.</span><span class="sxs-lookup"><span data-stu-id="83c81-107">However, you are not limited to using just those 40 cmdlets when managing Skype for Business Online.</span></span> <span data-ttu-id="83c81-108">Além dos cmdlets do Skype for Business Online, você também pode usar quaisquer outros cmdlets do Windows PowerShell instalados no seu computador.</span><span class="sxs-lookup"><span data-stu-id="83c81-108">In addition to the Skype for Business Online cmdlets, you can also use any other Windows PowerShell cmdlets that are installed on your computer.</span></span> <span data-ttu-id="83c81-109">(Quando você instala o Windows PowerShell 3,0, centenas de cmdlets do Windows PowerShell básicos também são instalados.) Seus comandos podem misturar e combinar cmdlets do Skype for Business Online e quaisquer outros cmdlets disponíveis no seu computador.</span><span class="sxs-lookup"><span data-stu-id="83c81-109">(When you install Windows PowerShell 3.0, hundreds of core Windows PowerShell cmdlets are installed, as well.) Your commands can mix and match Skype for Business Online cmdlets and any other cmdlets available on your computer.</span></span>

<span data-ttu-id="83c81-110">Embora um curso completo do Windows PowerShell 3,0 ultrapasse o escopo deste artigo, aqui estão alguns exemplos que mostram porque você pode querer combinar e comparar cmdlets.</span><span class="sxs-lookup"><span data-stu-id="83c81-110">Although a complete course in Windows PowerShell 3.0 goes beyond the scope of this article, here are a few examples that show why you might want to mix and match cmdlets.</span></span> <span data-ttu-id="83c81-111">Em primeiro lugar, nenhum dos cmdlets do Skype for Business Online inclui um comando de impressão, e esse comando não pode ser encontrado no console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83c81-111">First of all, none of the Skype for Business Online cmdlets include a Print command, and no such command can be found in the Windows PowerShell console, either.</span></span> <span data-ttu-id="83c81-112">Então, como você obtém uma cópia impressa das informações recuperadas por um cmdlet?</span><span class="sxs-lookup"><span data-stu-id="83c81-112">So how do you get a printout of the information retrieved by a cmdlet?</span></span> <span data-ttu-id="83c81-113">Uma maneira é recuperar as informações e, em seguida, enviar essas informações para o cmdlet **Out-Printer** :</span><span class="sxs-lookup"><span data-stu-id="83c81-113">One way is to retrieve the information, and then send that information to the **Out-Printer** cmdlet:</span></span>

    Get-CsTenant | Out-Printer

<span data-ttu-id="83c81-114">Como nenhum parâmetro adicional está incluído, todas as informações retornadas pelo cmdlet **Out-Printer** serão impressas na impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="83c81-114">Because no additional parameters are included, all the information returned by **the Out-Printer** cmdlet will be printed to the default printer.</span></span>

<span data-ttu-id="83c81-115">Da mesma forma, nenhum dos cmdlets do Skype for Business Online inclui um parâmetro que permite salvar dados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="83c81-115">Likewise, none of the Skype for Business Online cmdlets include a parameter that allows you to save data to a file.</span></span> <span data-ttu-id="83c81-116">Mas tudo bem: esse comando usa o cmdlet **Out-File** para salvar as informações retornadas no arquivo de texto C: \\ logs \\Tenants.txt:</span><span class="sxs-lookup"><span data-stu-id="83c81-116">But that’s OK: this command uses the **Out-File** cmdlet to save the returned information to the text file C:\\Logs\\Tenants.txt:</span></span>

    Get-Tenant | Out-File -FilePath "C:\Logs\Tenants.txt"

<span data-ttu-id="83c81-117">E esse comando usa o cmdlet **Select-Object** para limitar os dados que são retornados e exibidos na tela.</span><span class="sxs-lookup"><span data-stu-id="83c81-117">And this command uses the **Select-Object** cmdlet to limit the data that is returned and displayed onscreen.</span></span> <span data-ttu-id="83c81-118">Neste exemplo, o cmdlet [Get-CsOnlineUser](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) recupera informações de todos os seus usuários do Skype for Business Online e, em seguida, o cmdlet **Select-Object** é usado para limitar os dados exibidos ao valor de identidade do usuário e às políticas de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="83c81-118">In this example, the [Get-CsOnlineUser](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) cmdlet retrieves information for all of your Skype for Business Online users, and then the **Select-Object** cmdlet is used to limit the displayed data to the user’s Identity value and their archiving policy:</span></span>

    Get-CsOnlineUser | Select-Object Identity, ArchivingPolicy

<span data-ttu-id="83c81-119">Como há centenas de cmdlets disponíveis para serem usados em seu computador, você pode ter dificuldade em determinar quais cmdlets são cmdlets do Skype for Business Online e quais não são.</span><span class="sxs-lookup"><span data-stu-id="83c81-119">Because there will be hundreds of cmdlets available for use on your computer, you might have difficulty determining which cmdlets are Skype for Business Online cmdlets and which ones are not.</span></span> <span data-ttu-id="83c81-120">Para retornar uma lista dos cmdlets do Skype for Business online (e somente cmdlets do Skype for Business online), primeiro você deve determinar o nome do módulo do Windows PowerShell temporário que contém todos os cmdlets do Skype for Business online.</span><span class="sxs-lookup"><span data-stu-id="83c81-120">To return a list of the Skype for Business Online cmdlets (and only Skype for Business Online cmdlets), you must first determine the name of the temporary Windows PowerShell module that contains all the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="83c81-121">Para fazer isso, execute este comando a partir do prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="83c81-121">To do that, run this command from the Windows PowerShell prompt:</span></span>

    Get-Module

<span data-ttu-id="83c81-122">As informações semelhantes às seguintes serão exibidas na tela:</span><span class="sxs-lookup"><span data-stu-id="83c81-122">Information similar to the following will appear onscreen:</span></span>

    ModuleType Name                 ExportedCommands
    ---------- ----                 ----------------
    Manifest   Microsoft.PowerS...  {Add-Computer, Add-Content, A...}
    Script     tmp_5astd3uh.m5v     {Disable-CsMeetingRoom, Enabl...}

<span data-ttu-id="83c81-123">O módulo com o script ModuleType é o módulo que contém os cmdlets do Skype for Business online.</span><span class="sxs-lookup"><span data-stu-id="83c81-123">The module with the ModuleType Script is the module that contains the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="83c81-124">Para retornar uma lista desses cmdlets, execute o cmdlet **Get-Command** usando o nome do módulo de script como o nome do módulo:</span><span class="sxs-lookup"><span data-stu-id="83c81-124">To return a list of those cmdlets, run the **Get-Command** cmdlet, using the name of the Script module as the module name:</span></span>

    Get-Command -Module tmp_5astd3uh.m5v

<span data-ttu-id="83c81-125">É possível que você tenha vários módulos com um ModuleType igual a script.</span><span class="sxs-lookup"><span data-stu-id="83c81-125">It’s possible that you could have multiple modules with a ModuleType equal to Script.</span></span> <span data-ttu-id="83c81-126">Nesse caso, você pode executar o seguinte comando para descobrir qual módulo inclui o cmdlet **Get-CsTenant** :</span><span class="sxs-lookup"><span data-stu-id="83c81-126">In that case, you can run the following command to find out which module includes the **Get-CsTenant** cmdlet:</span></span>

    Get-Command Get-CsTenant

<span data-ttu-id="83c81-127">O módulo retornado para o cmdlet **Get-CsTenant** será o módulo que contém todos os cmdlets do Skype for Business Online:</span><span class="sxs-lookup"><span data-stu-id="83c81-127">The module returned for the **Get-CsTenant** cmdlet will be the module containing all the Skype for Business Online cmdlets:</span></span>

    CommandType     Name                                               ModuleName
    -----------     ----                                               ----------
    Function        Get-CsTenant                                       tmp_5astd3uh.m5v

<div>

## <a name="see-also"></a><span data-ttu-id="83c81-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="83c81-128">See Also</span></span>


<span data-ttu-id="83c81-129">[Uma introdução ao Windows PowerShell e ao Skype for Business Online](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="83c81-129">[An introduction to Windows PowerShell and Skype for Business Online](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span></span>  
  

<span data-ttu-id="83c81-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83c81-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

