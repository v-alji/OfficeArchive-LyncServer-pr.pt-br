---
title: 'Lync Server 2013: executando e monitorando backups'
description: 'Lync Server 2013: executando e monitorando backups.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Performing and monitoring backups
ms:assetid: 2df415d4-0f37-460e-99ff-4035a9a2f445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720912(v=OCS.15)
ms:contentKeyID: 63969595
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fb8ce99e850f0918974be08eb10796ef1397225
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424622"
---
# <a name="performing-and-monitoring-backups-in-lync-server-2013"></a><span data-ttu-id="ff522-103">Executar e monitorar backups no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff522-103">Performing and monitoring backups in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff522-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff522-104">

<span> </span></span></span>

<span data-ttu-id="ff522-105">_**Tópico da última modificação:** 2014-05-15_</span><span class="sxs-lookup"><span data-stu-id="ff522-105">_**Topic Last Modified:** 2014-05-15_</span></span>

<span data-ttu-id="ff522-106">Suas prioridades de negócios devem conduzir a especificação de requisitos de backup e restauração para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="ff522-106">Your business priorities should drive the specification of backup and restoration requirements for your organization.</span></span> <span data-ttu-id="ff522-107">Executar backups dos servidores e dos dados é a primeira linha de defesa para planejar um desastre.</span><span class="sxs-lookup"><span data-stu-id="ff522-107">Performing backups of the servers and data is the first line of defense in planning for a disaster.</span></span>

<span data-ttu-id="ff522-108">Os computadores que executam serviços do Lync Server 2013 ou funções de servidor devem ter uma cópia da topologia atual, configurações de configuração atuais e políticas atuais para poderem funcionar na função de sua função.</span><span class="sxs-lookup"><span data-stu-id="ff522-108">Computers that run Lync Server 2013 services or server roles must have a copy of the current topology, current configuration settings, and current policies before they can function in their appointed role.</span></span> <span data-ttu-id="ff522-109">O Lync Server é responsável por verificar se essas informações são passadas para cada computador que precisar.</span><span class="sxs-lookup"><span data-stu-id="ff522-109">Lync Server is responsible for making sure that this information is passed along to each computer that needs it.</span></span>

<span data-ttu-id="ff522-110">Os cmdlets **Export-CsConfiguration** e **Import-CsConfiguration** são usados para fazer backup e restaurar a topologia do Lync Server, as configurações e políticas durante uma atualização do repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="ff522-110">The **Export-CsConfiguration** and **Import-CsConfiguration** cmdlets are used to back up and restore your Lync Server topology, configuration settings, and policies during a Central Management store upgrade.</span></span> <span data-ttu-id="ff522-111">Os cmdlets **Export-CsConfiguration** permitem que você exporte dados para um. Arquivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="ff522-111">The **Export-CsConfiguration** cmdlets enable you to export data to a .ZIP file.</span></span> <span data-ttu-id="ff522-112">Em seguida, você pode usar o cmdlet **Import-CsConfiguration** para lê-lo. ZIP File e restaurar a topologia, as configurações e as políticas para o repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="ff522-112">You can then use the **Import-CsConfiguration** cmdlet to read that .ZIP file and restore the topology, configuration settings, and policies to the Central Management store.</span></span> <span data-ttu-id="ff522-113">Depois disso, os serviços de replicação do Lync Server replicarão as informações restauradas para outros computadores que executam serviços do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ff522-113">After that, the replication services of Lync Server will replicate the restored information to other computers that are running Lync Server services.</span></span>

<span data-ttu-id="ff522-114">A capacidade de exportar e importar dados de configuração também é usada durante a configuração inicial de computadores localizados na sua rede de perímetro (por exemplo, servidores de borda).</span><span class="sxs-lookup"><span data-stu-id="ff522-114">The ability to export and import configuration data is also used during the initial configuration of computers that are located in your perimeter network (for example, Edge Servers).</span></span> <span data-ttu-id="ff522-115">Ao configurar um computador na rede de perímetro, você deve primeiro executar uma replicação manual usando os cmdlets CsConfiguration: você deve exportar os dados de configuração usando **Export-CsConfiguration** e, em seguida, copiar o. Arquivo ZIP para o computador na rede de perímetro.</span><span class="sxs-lookup"><span data-stu-id="ff522-115">When configuring a computer in the perimeter network, you must first perform a manual replication using the CsConfiguration cmdlets: you must export the configuration data by using **Export-CsConfiguration** and then copy the .ZIP file to the computer in the perimeter network.</span></span> <span data-ttu-id="ff522-116">Depois disso, você pode usar **Import-CsConfiguration** e o parâmetro LocalStore para importar os dados.</span><span class="sxs-lookup"><span data-stu-id="ff522-116">After that, you can use **Import-CsConfiguration** and the LocalStore parameter to import the data.</span></span> <span data-ttu-id="ff522-117">Você só precisa fazer isso uma vez.</span><span class="sxs-lookup"><span data-stu-id="ff522-117">You only have to do this one time.</span></span> <span data-ttu-id="ff522-118">Depois disso, a duplicação ocorrerá automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ff522-118">After that, replication will occur automatically.</span></span>

<span data-ttu-id="ff522-119">Quem pode executar este cmdlet: por padrão, os membros dos grupos a seguir estão autorizados a executar o cmdlet **Export-CsConfiguration** localmente: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="ff522-119">Who can run this cmdlet: By default, members of the following groups are authorized to run the **Export-CsConfiguration** cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="ff522-120">Para retornar uma lista de todas as funções RBAC, esse cmdlet é atribuído (incluindo qualquer função RBAC personalizada que você tenha criado), execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ff522-120">To return a list of all RBAC roles, this cmdlet is assigned to (including any custom RBAC roles that you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

`Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Export-CsConfiguration"}`

<span data-ttu-id="ff522-121">Todos os bancos de dados back-end do SQL 2012 devem ser reproduzidos de acordo com [as práticas recomendadas do SQL](https://go.microsoft.com/fwlink/p/?linkid=290716).</span><span class="sxs-lookup"><span data-stu-id="ff522-121">All SQL 2012 Back End databases should be backed up as per [SQL best practices](https://go.microsoft.com/fwlink/p/?linkid=290716).</span></span>

<span data-ttu-id="ff522-122">O teste regular do plano de recuperação de desastres para sua infraestrutura do Lync Server 2013 deve ser executado em um ambiente de laboratório que imita o ambiente de produção o mais próximo possível.</span><span class="sxs-lookup"><span data-stu-id="ff522-122">Regular testing of the Disaster Recovery Plan for your Lync Server 2013 infrastructure should be performed in a lab environment that mimics the production environment as closely as possible.</span></span> <span data-ttu-id="ff522-123">Consulte as tarefas mensais para obter mais informações sobre testes de recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="ff522-123">Refer to the Monthly Tasks for more information about Disaster Recovery Testing.</span></span>

<span data-ttu-id="ff522-124">Observe que a frequência de backup pode ser ajustada, com base nos objetivos do ponto de restauração e ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ff522-124">Note that the backup frequency can be adjusted, based on your Restore Point and Recovery Point objectives.</span></span> <span data-ttu-id="ff522-125">Como prática recomendada, faça instantâneos periódicos periódicos ao longo do dia.</span><span class="sxs-lookup"><span data-stu-id="ff522-125">As a best practice, take regular, periodic snapshots throughout the day.</span></span> <span data-ttu-id="ff522-126">Geralmente, você deve executar backups completos a cada 24 horas.</span><span class="sxs-lookup"><span data-stu-id="ff522-126">Generally, you should perform full backups every 24 hours.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="ff522-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff522-127">See Also</span></span>


[<span data-ttu-id="ff522-128">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff522-128">Import-CsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsConfiguration)  
[<span data-ttu-id="ff522-129">Export-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff522-129">Export-CsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Export-CsConfiguration)  
[<span data-ttu-id="ff522-130">Práticas recomendadas do SQL</span><span class="sxs-lookup"><span data-stu-id="ff522-130">SQL best practices</span></span>](https://go.microsoft.com/fwlink/p/?linkid=290716)  
  

<span data-ttu-id="ff522-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff522-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

