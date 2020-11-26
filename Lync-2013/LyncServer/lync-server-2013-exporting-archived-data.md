---
title: 'Lync Server 2013: exportar dados arquivados'
description: 'Lync Server 2013: exportar dados arquivados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting archived data
ms:assetid: 09450d54-769b-4741-924b-e390664d506f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204657(v=OCS.15)
ms:contentKeyID: 48183347
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 656751f1a2d03b50f0c938a8501ba3e95e304cff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428332"
---
# <a name="exporting-archived-data-from-lync-server-2013"></a><span data-ttu-id="15850-103">Exportando dados arquivados do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15850-103">Exporting archived data from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15850-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15850-104">

<span> </span></span></span>

<span data-ttu-id="15850-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="15850-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="15850-106">Os dados arquivados em bancos de dados de Arquivamento não estão em um formato legível ou com possibilidade de pesquisa, mas é possível usar o cmdlet Export-CsArchivingData para extrair registros do banco de dados e salvá-los como um arquivo do Outlook Electronic Mail (EML).</span><span class="sxs-lookup"><span data-stu-id="15850-106">Data archived in Archiving databases is not searchable or in a readable format, but you can use the Export-CsArchivingData cmdlet to extract records from the database and save them as an Outlook Electronic Mail (EML) file.</span></span> <span data-ttu-id="15850-107">Para obter detalhes sobre como exportar dados arquivados, consulte [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="15850-107">For details about exporting archived data, see [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) in the Operations documentation.</span></span>

<span data-ttu-id="15850-108">Se você habilitar a integração do Microsoft Exchange, os dados serão arquivados nas lojas do Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="15850-108">If you enable Microsoft Exchange integration, data is archived in Exchange 2013 stores.</span></span> <span data-ttu-id="15850-109">Os dados arquivados no Exchange 2013 são pesquisáveis e detectáveis.</span><span class="sxs-lookup"><span data-stu-id="15850-109">Data archived in Exchange 2013 is searchable and discoverable.</span></span> <span data-ttu-id="15850-110">Para obter detalhes sobre o suporte para comunicações integradas do Exchange 2013 e do Lync Server 2013, consulte [suporte à integração do Exchange Server e do SharePoint no Lync server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="15850-110">For details about support for integrated communications for Exchange 2013 and Lync Server 2013, see [Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="15850-111">Para obter detalhes sobre como acessar dados arquivados no Exchange, consulte a documentação do Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="15850-111">For details about accessing data that is archived in Exchange, see the Exchange 2013 documentation.</span></span>

<div>

## <a name="exporting-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="15850-112">Exportar dados de arquivamento usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="15850-112">Exporting Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="15850-113">O arquivamento de dados pode ser exportado usando o cmdlet Export-CSArchivingData.</span><span class="sxs-lookup"><span data-stu-id="15850-113">Archiving data can be exported by using the Export-CSArchivingData cmdlet.</span></span> <span data-ttu-id="15850-114">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15850-114">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="15850-115">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="15850-115">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<span data-ttu-id="15850-116">**Para exportar dados do arquivamento**</span><span class="sxs-lookup"><span data-stu-id="15850-116">**To export archiving data**</span></span>

  - <span data-ttu-id="15850-117">Esse comando exporta todos os dados de arquivamento gravados no banco de dados de arquivamento atl-sql-001.litwareinc.com desde 1 ° de junho de 2012.</span><span class="sxs-lookup"><span data-stu-id="15850-117">This command exports all the archiving data written to the archiving database atl-sql-001.litwareinc.com since June 1, 2012.</span></span> <span data-ttu-id="15850-118">O arquivo de saída resultante será armazenado na pasta C: \\ ArchivingExports.</span><span class="sxs-lookup"><span data-stu-id="15850-118">The resulting output file will be stored in the folder C:\\ArchivingExports.</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports"

<span data-ttu-id="15850-119">**Para exportar dados de arquivamento para um único usuário**</span><span class="sxs-lookup"><span data-stu-id="15850-119">**To export archiving data for a single user**</span></span>

  - <span data-ttu-id="15850-120">O comando a seguir exporta dados de arquivamento para um único usuário: kenmyer@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="15850-120">The following command exports archiving data for a single user: kenmyer@litwareinc.com.</span></span> <span data-ttu-id="15850-121">Isso é feito incluindo o parâmetro UserUri seguido pelo endereço SIP do usuário.</span><span class="sxs-lookup"><span data-stu-id="15850-121">This is done by including the UserUri parameter followed by the user’s SIP address.</span></span> <span data-ttu-id="15850-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="15850-122">For example:</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports" -UserUri "sip:kenmyer@litwareinc.com"

<span data-ttu-id="15850-123">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) .</span><span class="sxs-lookup"><span data-stu-id="15850-123">For more information, see the help topic for the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="15850-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="15850-124">See Also</span></span>


[<span data-ttu-id="15850-125">Suporte a Servidor Exchange e à integração com SharePoint no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15850-125">Exchange Server and SharePoint integration support in Lync Server 2013</span></span>](lync-server-2013-exchange-and-sharepoint-integration-support.md)  


[<span data-ttu-id="15850-126">Export-CsArchivingData</span><span class="sxs-lookup"><span data-stu-id="15850-126">Export-CsArchivingData</span></span>](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)  
[<span data-ttu-id="15850-127">Gerenciando Arquivamento do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15850-127">Managing Lync Server 2013 Archiving</span></span>](lync-server-2013-managing-archiving.md)  
  

<span data-ttu-id="15850-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15850-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

