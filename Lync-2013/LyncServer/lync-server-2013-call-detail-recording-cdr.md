---
title: 'Lync Server 2013: registro de detalhes de chamadas (CDR)'
description: 'Lync Server 2013: registro de detalhes de chamadas (CDR).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call detail recording (CDR)
ms:assetid: 67726075-c77c-4191-a64f-a1cf5c7bcbb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688079(v=OCS.15)
ms:contentKeyID: 49733675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 590f99fd0b8649ffb3c4df039488dc54a8f3b7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435772"
---
# <a name="call-detail-recording-cdr-in-lync-server-2013"></a><span data-ttu-id="232a5-103">Registro de detalhes de chamadas (CDR) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="232a5-103">Call detail recording (CDR) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="232a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="232a5-104">

<span> </span></span></span>

<span data-ttu-id="232a5-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="232a5-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="232a5-106">O CDR (registro de detalhes das chamadas) registra informações de uso e diagnóstico sobre atividades ponto a ponto, incluindo serviço de mensagens instantâneas, chamadas VoIP, compartilhamento de aplicativos, transferência de arquivos e reuniões.</span><span class="sxs-lookup"><span data-stu-id="232a5-106">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities, including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings.</span></span> <span data-ttu-id="232a5-107">Os dados de uso podem ser utilizados para calcular o retorno sobre o investimento, enquanto os dados de diagnóstico podem ser usados para solucionar problemas de atividades ponto a ponto e reuniões.</span><span class="sxs-lookup"><span data-stu-id="232a5-107">The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span> <span data-ttu-id="232a5-108">Ao instalar o Lync Server 2013, você também instalará um conjunto predefinido de configurações globais de configuração para CDR.</span><span class="sxs-lookup"><span data-stu-id="232a5-108">When you install Lync Server 2013, you will also install a predefined collection of global configuration settings for CDR.</span></span> <span data-ttu-id="232a5-109">Use os tópicos desta seção para configurar o CDR.</span><span class="sxs-lookup"><span data-stu-id="232a5-109">Use the topics in this section to configure CDR.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="232a5-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="232a5-110">In This Section</span></span>

  - [<span data-ttu-id="232a5-111">Exibir informações de configuração de CDR no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="232a5-111">View CDR configuration information in Lync Server 2013</span></span>](lync-server-2013-view-cdr-configuration-information.md)

  - [<span data-ttu-id="232a5-112">Habilitar a gravação de detalhes de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="232a5-112">Enable call detail recording in Lync Server 2013</span></span>](lync-server-2013-enable-call-detail-recording.md)

  - [<span data-ttu-id="232a5-113">Criar ou modificar uma coleção de definições de configuração de CDR no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="232a5-113">Create or modify a collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="232a5-114">Excluir uma coleção existente de definições de configuração de CDR no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="232a5-114">Delete an existing collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="232a5-115">Como limpar manualmente a gravação de detalhes da chamada e os bancos de dados de qualidade da experiência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="232a5-115">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>](lync-server-2013-manually-purging-the-call-detail-recording-and-quality-of-experience-databases.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="232a5-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="232a5-116">See Also</span></span>


[<span data-ttu-id="232a5-117">Configurando a gravação de detalhes da chamada e as configurações de qualidade de experiência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="232a5-117">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md)  
  

<span data-ttu-id="232a5-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="232a5-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

