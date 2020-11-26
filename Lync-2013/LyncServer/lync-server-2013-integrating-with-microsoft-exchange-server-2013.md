---
title: 'Lync Server 2013: integrando com o Microsoft Exchange Server 2013'
description: 'Lync Server 2013: integrando com o Microsoft Exchange Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating Lync Server 2013 and Exchange Server 2013
ms:assetid: 795dc1c6-524f-4012-8b66-103b55198044
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688098(v=OCS.15)
ms:contentKeyID: 49733697
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54ab4a81e5455bc0a44677b1509876f39ff4d985
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426876"
---
# <a name="integrating-microsoft-lync-server-2013-and-microsoft-exchange-server-2013"></a><span data-ttu-id="e0b37-103">Integração do Microsoft Lync Server 2013 e do Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0b37-103">Integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0b37-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0b37-104">

<span> </span></span></span>

<span data-ttu-id="e0b37-105">_**Tópico da última modificação:** 2014-07-09_</span><span class="sxs-lookup"><span data-stu-id="e0b37-105">_**Topic Last Modified:** 2014-07-09_</span></span>

<span data-ttu-id="e0b37-106">O Exchange e o Lync Server têm uma longa história de integração e compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="e0b37-106">Exchange and Lync Server have a long history of integration and compatibility.</span></span> <span data-ttu-id="e0b37-107">Essa integração é mais perceptível em seus respectivos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="e0b37-107">This integration is most noticeable within their respective client application.</span></span> <span data-ttu-id="e0b37-108">Por exemplo, as informações de presença do Lync podem ser reportadas no Microsoft Outlook; da mesma forma, o Lync pode usar o calendário do Outlook para atualizar automaticamente essas informações de presença.</span><span class="sxs-lookup"><span data-stu-id="e0b37-108">For example, Lync presence information can be reported in Microsoft Outlook; likewise, Lync can use Outlook calendar to automatically update that presence information.</span></span> <span data-ttu-id="e0b37-109">(Por exemplo, o Lync pode alterar seu status para ocupado sempre que seu calendário mostrar que você tem uma reunião agendada.) Embora você não precise executar o Exchange para executar o Lync Server (ou vice-versa), há pouco a dúvida de que usar os dois produtos juntos epitomizes a grande definição do termo "melhor juntos".</span><span class="sxs-lookup"><span data-stu-id="e0b37-109">(For example, Lync can change your status to Busy any time your calendar shows that you have a meeting scheduled.) Although you do not have to run Exchange in order to run Lync Server (or vice-versa) there's little doubt that using the two products together epitomizes the very definition of the term "better together."</span></span>

<span data-ttu-id="e0b37-110">Isso é especialmente verdadeiro com o lançamento do Microsoft Lync Server 2013 e do Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0b37-110">This is especially true with the release of Microsoft Lync Server 2013 and Microsoft Exchange Server 2013.</span></span> <span data-ttu-id="e0b37-111">Além dos recursos, como mensagens unificadas e mensagens INSTANTÂNEAs e presença, que estão disponíveis no Microsoft Exchange Server 2010 e no Microsoft Lync Server 2010, as versões do 2013 dos produtos do servidor incluem uma série de novos recursos.</span><span class="sxs-lookup"><span data-stu-id="e0b37-111">In addition to features, such as unified messaging and IM and presence, that are found in Microsoft Exchange Server 2010 and Microsoft Lync Server 2010, the 2013 releases of the server products include a number of new capabilities.</span></span> <span data-ttu-id="e0b37-112">Esses recursos incluem itens como:</span><span class="sxs-lookup"><span data-stu-id="e0b37-112">These capabilities include such things as:</span></span>

  - <span data-ttu-id="e0b37-113">**Integração de arquivamento do Lync**.</span><span class="sxs-lookup"><span data-stu-id="e0b37-113">**Lync Archiving Integration**.</span></span> <span data-ttu-id="e0b37-114">No Lync Server 2013, os administradores ainda têm a opção de ter mensagens instantâneas e transcrições de Webconferência arquivadas no SQL Server (da mesma forma como essas transcrições foram arquivadas no Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="e0b37-114">In Lync Server 2013 administrators still have the option of having instant messaging and Web conferencing transcripts archived to SQL Server (the same way these transcripts were archived in Lync Server 2010).</span></span> <span data-ttu-id="e0b37-115">Como alternativa, no entanto, os administradores podem optar por fazer transcrições arquivadas no Exchange 2013, armazenando essas transcrições nas caixas de correio de usuário individuais da mesma forma que o Exchange arquiva comunicações.</span><span class="sxs-lookup"><span data-stu-id="e0b37-115">Alternatively, however, administrators can choose to have transcripts archived to Exchange 2013, storing those transcripts in the individual user mailboxes in the same way in which Exchange archives communications.</span></span> <span data-ttu-id="e0b37-116">Isso significa um único repositório para todas as suas comunicações eletrônicas (do Exchange e do Lync Server), o que torna muito mais fácil pesquisar e recuperar essas comunicações arquivadas caso a necessidade seja necessária.</span><span class="sxs-lookup"><span data-stu-id="e0b37-116">That means a single repository for all your electronic communications (from both Exchange and Lync Server), which makes it much easier to search for and retrieve those archived communications should the need arise.</span></span>

  - <span data-ttu-id="e0b37-117">**Repositório de contatos unificado**.</span><span class="sxs-lookup"><span data-stu-id="e0b37-117">**Unified Contact Store**.</span></span> <span data-ttu-id="e0b37-118">No Lync Server 2010, os usuários tinham que manter listas de contatos separadas no Outlook e no Lync; na verdade, para garantir que você tinha os mesmos contatos disponíveis nos dois produtos que você tinha para manter as listas de contatos duplicadas, uma para o Outlook e outra para o Lync.</span><span class="sxs-lookup"><span data-stu-id="e0b37-118">In Lync Server 2010, users had to maintain separate contact lists in Outlook and Lync; in fact, to ensure that you had the same contacts available in both products you had to maintain duplicate contact lists, one for Outlook and one for Lync.</span></span> <span data-ttu-id="e0b37-119">No Lync Server 2013, no entanto, os contatos do usuário podem ser armazenados no Exchange 2013 e no repositório de contatos unificado.</span><span class="sxs-lookup"><span data-stu-id="e0b37-119">With Lync Server 2013, however, user contacts can be stored in Exchange 2013 and the unified contact store.</span></span> <span data-ttu-id="e0b37-120">Usar um único repositório de contatos permite que os usuários mantenham apenas um conjunto de contatos, com o mesmo conjunto de contatos disponível no Lync 2013, no Outlook 2013 e no Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e0b37-120">Using a single contact store enables users to maintain just one set of contacts, with that same set of contacts being available in Lync 2013, Outlook 2013, and Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="e0b37-121">**Agendamento de reunião do Lync do OWA**.</span><span class="sxs-lookup"><span data-stu-id="e0b37-121">**Lync Meeting Scheduling from OWA**.</span></span> <span data-ttu-id="e0b37-122">Com a integração do Lync Server 2013 e do Exchange 2013, os usuários podem agendar reuniões do Lync a partir do Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e0b37-122">With Lync Server 2013 and Exchange 2013 integration, users can schedule Lync meetings from Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="e0b37-123">**Fotos de alta resolução**.</span><span class="sxs-lookup"><span data-stu-id="e0b37-123">**High resolution photos**.</span></span> <span data-ttu-id="e0b37-124">O Lync 2010 pode exibir apenas fotos pequenas de seus contatos; Isso ocorre porque essas fotos foram armazenadas no Active Directory e o Active Directory impõe um 48 pixel por 48 limite de tamanho de pixel em fotos armazenadas.</span><span class="sxs-lookup"><span data-stu-id="e0b37-124">Lync 2010 could only display small photos of your contacts; that's because those photos were stored in Active Directory, and Active Directory imposes a 48 pixel by 48 pixel size limitation on stored photos.</span></span> <span data-ttu-id="e0b37-125">No Lync Server 2013, no entanto, as fotos podem ser armazenadas no Microsoft Exchange; Isso permite fotos de alta resolução tão grandes quanto 648 pixels por 648 pixels.</span><span class="sxs-lookup"><span data-stu-id="e0b37-125">With Lync Server 2013, however, photos can be stored in Microsoft Exchange; that allows for high-resolution photos as large as 648 pixels by 648 pixels.</span></span> <span data-ttu-id="e0b37-126">Como você pode esperar, o Lync 2013 foi atualizado para permitir a exibição dessas fotografias de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="e0b37-126">As you might expect, Lync 2013 has been upgraded to allow for the display of these high-resolution photographs.</span></span>

<span data-ttu-id="e0b37-127">Lembre-se de que esses novos recursos exigem o uso do Lync Server 2013 e do Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="e0b37-127">Keep in mind that these new features require the use of both Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="e0b37-128">Além disso, os usuários que esperam aproveitar todos esses novos recursos devem ter contas no Lync Server 2013 e no Exchange 2013 e devem estar usando as versões mais recentes do software cliente (por exemplo, Lync 2013).</span><span class="sxs-lookup"><span data-stu-id="e0b37-128">In addition to that, users who hope to take full advantage of these new capabilities must have accounts on Lync Server 2013 and Exchange 2013, and must be using the latest versions of the client software (e.g., Lync 2013).</span></span> <span data-ttu-id="e0b37-129">Por exemplo, o repositório de contatos unificado não está disponível para os usuários que foram hospedados no Lync Server 2010; da mesma forma, fotos de alta resolução não podem ser exibidas no Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="e0b37-129">For example, the unified contact store is not available to users who have been homed on Lync Server 2010; likewise, high-resolution photos cannot be displayed in Lync 2010.</span></span>

<span data-ttu-id="e0b37-130">Esta documentação fornece informações sobre a integração do Lync Server 2013 e do Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="e0b37-130">This documentation provides information on integrating Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="e0b37-131">incluindo informações passo a passo sobre como habilitar novos recursos, como integração de arquivamento e repositório de contatos unificado.</span><span class="sxs-lookup"><span data-stu-id="e0b37-131">including step-by-step information on enabling new features such archiving Integration and the unified contact store.</span></span> <span data-ttu-id="e0b37-132">O que essa documentação não faz é discutir a configuração e a configuração iniciais desses dois produtos.</span><span class="sxs-lookup"><span data-stu-id="e0b37-132">What this documentation does not do is discuss the initial setup and configuration of these two products.</span></span> <span data-ttu-id="e0b37-133">Para obter detalhes sobre a implantação do Lync Server 2013, consulte o Lync Server 2013 Tech Center em [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127) .</span><span class="sxs-lookup"><span data-stu-id="e0b37-133">For details about deploying Lync Server 2013 see the Lync Server 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127).</span></span> <span data-ttu-id="e0b37-134">Para obter detalhes sobre a implantação do Exchange 2013, consulte o Exchange 2013 Tech Center em [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528) .</span><span class="sxs-lookup"><span data-stu-id="e0b37-134">For details about deploying Exchange 2013 see the Exchange 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e0b37-135">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e0b37-135">In This Section</span></span>

[<span data-ttu-id="e0b37-136">Pré-requisitos para a integração do Microsoft Lync Server 2013 e do Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0b37-136">Prerequisites for integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-prerequisites-for-integrating-with-exchange-server-2013.md)

[<span data-ttu-id="e0b37-137">Configurando aplicativos de parceiros no Microsoft Lync Server 2013 e no Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0b37-137">Configuring partner applications in Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-configuring-partner-applications-in-lync-server-2013-and-exchange-server-2013.md)

[<span data-ttu-id="e0b37-138">Configurando o Microsoft Lync Server 2013 para usar o Microsoft Exchange Server 2013 Archiving</span><span class="sxs-lookup"><span data-stu-id="e0b37-138">Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving</span></span>](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md)

[<span data-ttu-id="e0b37-139">Configurando o Microsoft SharePoint Server 2013 para pesquisar dados do Microsoft Lync Server 2013 arquivados</span><span class="sxs-lookup"><span data-stu-id="e0b37-139">Configuring Microsoft SharePoint Server 2013 to search for archived Microsoft Lync Server 2013 data</span></span>](lync-server-2013-configuring-microsoft-sharepoint-server-2013-to-search-for-archived-lync-server-2013-data.md)

[<span data-ttu-id="e0b37-140">Configurando o Microsoft Lync Server 2013 para usar o repositório de contatos unificado</span><span class="sxs-lookup"><span data-stu-id="e0b37-140">Configuring Microsoft Lync Server 2013 to use the unified contact store</span></span>](lync-server-2013-configuring-lync-server-to-use-the-unified-contact-store.md)

[<span data-ttu-id="e0b37-141">Configurando o uso de fotos de alta resolução no Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0b37-141">Configuring the use of high-resolution photos in Microsoft Lync Server 2013</span></span>](lync-server-2013-configuring-the-use-of-high-resolution-photos.md)

[<span data-ttu-id="e0b37-142">Configurando o Microsoft Exchange Server 2013 Unified Messaging para o Microsoft Lync Server 2013 voice mail</span><span class="sxs-lookup"><span data-stu-id="e0b37-142">Configuring Microsoft Exchange Server 2013 Unified Messaging for Microsoft Lync Server 2013 voice mail</span></span>](lync-server-2013-configuring-microsoft-exchange-server-2013-unified-messaging-for-lync-server-2013-voice-mail.md)

[<span data-ttu-id="e0b37-143">Integração do Microsoft Lync Server 2013 e do Microsoft Outlook Web App 2013</span><span class="sxs-lookup"><span data-stu-id="e0b37-143">Integrating Microsoft Lync Server 2013 and Microsoft Outlook Web App 2013</span></span>](lync-server-2013-integrating-lync-server-and-outlook-web-app-2013.md)

<span data-ttu-id="e0b37-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0b37-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

