---
title: 'Lync Server 2013: verificando o uso do disco'
description: 'Lync Server 2013: verificando o uso do disco.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking disk usage
ms:assetid: 0f0cb9bf-3f11-43ff-be10-5c8e1b5c4f08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720908(v=OCS.15)
ms:contentKeyID: 63969578
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7eddde772d156f0a416dab381efe1ab33ee202f9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434988"
---
# <a name="checking-disk-usage-in-lync-server-2013"></a><span data-ttu-id="6e354-103">Verificando o uso do disco no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e354-103">Checking disk usage in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e354-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e354-104">

<span> </span></span></span>

<span data-ttu-id="6e354-105">_**Tópico da última modificação:** 2014-04-30_</span><span class="sxs-lookup"><span data-stu-id="6e354-105">_**Topic Last Modified:** 2014-04-30_</span></span>

<span data-ttu-id="6e354-106">Unidades de discos rígidos são um componente importante da implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6e354-106">Hard disks drives are an important component of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="6e354-107">Sem um volume de disco livre suficiente, nem o sistema operacional nem os bancos de dados do Lync Server 2013 podem funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="6e354-107">Without sufficient free disk volume, neither the operating system nor the Lync Server 2013 databases can function correctly.</span></span> <span data-ttu-id="6e354-108">Você deve monitorar as estatísticas de banco de dados de back-end do Lync Server 2013 diariamente para ajudar a garantir que os servidores não fiquem sem espaço em disco e para se preparar para adicionar recursos de armazenamento conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="6e354-108">You must monitor the Lync Server 2013 back-end database statistics daily to help to make sure that servers do not run out of disk space, and to prepare to add storage resources as required.</span></span>

<span data-ttu-id="6e354-109">Além de verificar o espaço em discos que hospedam o sistema operacional, arquivos de programas, banco de dados e logs de transações (Lync Server 2013 back-end), você também deve monitorar o uso do sistema de arquivos que inclui espaço em disco para os compartilhamentos de arquivos que contêm os dados importantes a seguir:</span><span class="sxs-lookup"><span data-stu-id="6e354-109">Apart from checking space on disks hosting the operating system, program files, database, and transaction logs (Lync Server 2013 Back End), you should also monitor usage of the file system that includes disk space for file shares that contain the following important data:</span></span>

  - <span data-ttu-id="6e354-110">Conteúdo da reunião</span><span class="sxs-lookup"><span data-stu-id="6e354-110">Meeting content</span></span>

  - <span data-ttu-id="6e354-111">Metadados de conteúdo da reunião</span><span class="sxs-lookup"><span data-stu-id="6e354-111">Meeting content metadata</span></span>

  - <span data-ttu-id="6e354-112">Registros de conformidade para reuniões</span><span class="sxs-lookup"><span data-stu-id="6e354-112">Meeting compliance logs</span></span>

  - <span data-ttu-id="6e354-113">Arquivos de dados de aplicativo (usados internamente pelo componente de servidor de aplicativos)</span><span class="sxs-lookup"><span data-stu-id="6e354-113">Application data files (used internally by the application server component)</span></span>

  - <span data-ttu-id="6e354-114">Serviço Web e pastas de conformidade do servidor de chat em grupo (para armazenar arquivos carregados no serviço Web de chat de grupo)</span><span class="sxs-lookup"><span data-stu-id="6e354-114">Group Chat Server web service and compliance folders (to store files uploaded to the Group Chat web service)</span></span>

  - <span data-ttu-id="6e354-115">Arquivos XML de conformidade de chat em grupo (que contêm registros de conformidade de chat em grupo)</span><span class="sxs-lookup"><span data-stu-id="6e354-115">Group Chat compliance XML files (that contain Group Chat compliance records)</span></span>

  - <span data-ttu-id="6e354-116">Atualizar arquivos (para o serviço de atualização de dispositivo)</span><span class="sxs-lookup"><span data-stu-id="6e354-116">Update files (for Device Update Service)</span></span>

  - <span data-ttu-id="6e354-117">Arquivos do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="6e354-117">Address Book files</span></span>

<span data-ttu-id="6e354-118">O Lync Server 2013 precisa do espaço do disco rígido para armazenar seus bancos de dados e logs de transação, além de arquivos em compartilhamento de arquivos listados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6e354-118">Lync Server 2013 needs hard disk space to store its databases and transaction logs in addition to files on file shares previously listed.</span></span>

<span data-ttu-id="6e354-119">Você deve monitorar o espaço em disco regularmente para ajudar a garantir que a implantação do Lync Server 2013 não seja afetada de forma adversa devido a recursos de armazenamento insuficientes.</span><span class="sxs-lookup"><span data-stu-id="6e354-119">You should monitor the disk space regularly to help to make sure that the Lync Server 2013 deployment is not adversely affected because of insufficient storage resources.</span></span>

<span data-ttu-id="6e354-120">Comparar e manter as informações estatísticas sobre o espaço disponível em disco em cada volume do Lync Server 2013 e o crescimento esperado dos arquivos de log de transação e bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="6e354-120">Compare and maintain statistical information about available disk space on each Lync Server 2013 volume and expected growth of the databases and transaction log files.</span></span> <span data-ttu-id="6e354-121">Isso ajuda a planejar a capacidade e a adicionar armazenamento quando os recursos de armazenamento são necessários.</span><span class="sxs-lookup"><span data-stu-id="6e354-121">This helps with capacity planning and adding storage when the storage resources are required.</span></span>

<span data-ttu-id="6e354-122">Para acomodar as situações de solução de problemas e recuperação de desastres, recomendamos que o espaço disponível no volume seja igual ou superior a 110% do tamanho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6e354-122">To accommodate troubleshooting and disaster recovery situations, we recommend that available free volume space be equal or greater than 110 percent of the size of database.</span></span>

<span data-ttu-id="6e354-123">Você pode verificar o espaço livre em disco usando os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="6e354-123">You can check free disk space by using the following methods:</span></span>

1.  <span data-ttu-id="6e354-124">**Gerenciador de operações do System Center**   O System Center Operations Manager pode ser usado para avisar os administradores quando o espaço do volume é restringido.</span><span class="sxs-lookup"><span data-stu-id="6e354-124">**System Center Operations Manager**   System Center Operations Manager can be used to warn administrators when volume space is constrained.</span></span>

2.  <span data-ttu-id="6e354-125">**Executar um script**   Monitore o espaço em disco executando um script que envia uma mensagem para você se o espaço disponível no disco rígido ficar abaixo de 20%.</span><span class="sxs-lookup"><span data-stu-id="6e354-125">**Running a script**   Monitor disk space by running a script that sends you a message if the available hard disk space falls below 20 percent.</span></span> <span data-ttu-id="6e354-126">Você pode encontrar um exemplo de script no Microsoft Script Center no TechNet, examine: [https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard%20disk%20alert\&f%5B0%5D.Value=hard%20disk%20alert\&f%5B0%5D.Type=SearchText\&ac=5](https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard+disk+alert%26f%5b0%5d.value=hard+disk+alert%26f%5b0%5d.type=searchtext%26ac=5)</span><span class="sxs-lookup"><span data-stu-id="6e354-126">You can find a sample script on Microsoft Script Center on TechNet, examine: [https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard%20disk%20alert\&f%5B0%5D.Value=hard%20disk%20alert\&f%5B0%5D.Type=SearchText\&ac=5](https://gallery.technet.microsoft.com/scriptcenter/site/search?query=hard+disk+alert%26f%5b0%5d.value=hard+disk+alert%26f%5b0%5d.type=searchtext%26ac=5)</span></span>

3.  <span data-ttu-id="6e354-127">**Explorador do Windows**   Use o Windows Explorer para verificar o espaço em disco em volumes que armazenam logs e bancos de dados do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6e354-127">**Windows Explorer**   Use Windows Explorer to check for disk space on volumes that store Lync Server 2013 logs and databases.</span></span>

<span data-ttu-id="6e354-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e354-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

