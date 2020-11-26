---
title: 'Lync Server 2013: criar um comunicado'
description: 'Lync Server 2013: criar um anúncio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create an announcement
ms:assetid: a6fd5922-fe46-41ba-94e3-c76b1101a31b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412783(v=OCS.15)
ms:contentKeyID: 48185005
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc064686ef86e04b89951fcaac7abbec28b7257c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432027"
---
# <a name="create-an-announcement-in-lync-server-2013"></a><span data-ttu-id="3998a-103">Criar um anúncio no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3998a-103">Create an announcement in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3998a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3998a-104">

<span> </span></span></span>

<span data-ttu-id="3998a-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="3998a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="3998a-106">Para criar um novo comunicado, é necessário executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3998a-106">To create a new announcement, you need to perform the following steps:</span></span>

1.  <span data-ttu-id="3998a-107">Para prompts de áudio, grave o arquivo de áudio usando seu aplicativo de gravação de áudio favorito.</span><span class="sxs-lookup"><span data-stu-id="3998a-107">For audio prompts, record the audio file by using your favorite audio recording application.</span></span>

2.  <span data-ttu-id="3998a-108">Para prompts de áudio, execute o cmdlet **Import-CsAnnouncementFile** para importar o conteúdo do arquivo de áudio para o Repositório de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="3998a-108">For audio prompts, run the **Import-CsAnnouncementFile** cmdlet to import the contents of the audio file to File Store.</span></span>

3.  <span data-ttu-id="3998a-109">Execute o cmdlet **New-CsAnnouncement** para criar e nomear o comunicado.</span><span class="sxs-lookup"><span data-stu-id="3998a-109">Run the **New-CsAnnouncement** cmdlet to create and name the announcement.</span></span> <span data-ttu-id="3998a-110">Execute esta etapa para criar comunicados com um prompt de áudio, um prompt TTS (text-to-speech), ou sem prompt.</span><span class="sxs-lookup"><span data-stu-id="3998a-110">Perform this step to create announcements with an audio prompt, a text-to-speech (TTS) prompt, or no prompt.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="3998a-111">Pode ser desejável criar um comunicado sem prompt (por exemplo, se você deseja transferir chamadas para um destino específico sem reproduzir uma mensagem).</span><span class="sxs-lookup"><span data-stu-id="3998a-111">You might want to create an announcement with no prompt (for example, if you want to transfer calls to a specific destination without playing a message).</span></span>

    
    </div>

4.  <span data-ttu-id="3998a-112">Atribua o novo comunicado a um intervalo numérico na tabela de números não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="3998a-112">Assign the new announcement to a number range in the unassigned number table.</span></span>

<span data-ttu-id="3998a-113">Este tópico descreve como importar e criar comunicados.</span><span class="sxs-lookup"><span data-stu-id="3998a-113">This topic describes how to import and create announcements.</span></span> <span data-ttu-id="3998a-114">Para obter detalhes sobre como atribuir anúncios na tabela número não atribuído, consulte [Configurar a tabela número não atribuído no Lync Server 2013](lync-server-2013-configure-the-unassigned-number-table.md).</span><span class="sxs-lookup"><span data-stu-id="3998a-114">For details about assigning announcements in the unassigned number table, see [Configure the unassigned number table in Lync Server 2013](lync-server-2013-configure-the-unassigned-number-table.md).</span></span>

<div>

## <a name="to-create-a-new-announcement"></a><span data-ttu-id="3998a-115">Para criar um novo comunicado</span><span class="sxs-lookup"><span data-stu-id="3998a-115">To create a new announcement</span></span>

1.  <span data-ttu-id="3998a-116">Para prompts de áudio, crie o arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="3998a-116">For audio prompts, create the audio file.</span></span>

2.  <span data-ttu-id="3998a-117">Faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo RTCUniversalServerAdmins ou com os direitos de usuário necessários, conforme descrito em [permissões de configuração de representante no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="3998a-117">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

3.  <span data-ttu-id="3998a-118">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="3998a-118">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="3998a-119">Para prompts de áudio, execute:</span><span class="sxs-lookup"><span data-stu-id="3998a-119">For audio prompts, run:</span></span>
    
        Import-CsAnnouncementFile -Parent <service of the Application Server running the Announcement application> -FileName <name for file in File Store> -Content Byte [<contents of file in byte array>]

5.  <span data-ttu-id="3998a-120">Execute:</span><span class="sxs-lookup"><span data-stu-id="3998a-120">Run:</span></span>
    
        New-CsAnnouncement -Parent <service of Application Server running the Announcement application, in the form: service:ApplicationServer:<fqdn>> -Name <unique name to be used as destination in unassigned number table> [-AudioFilePrompt <FileName specified in Import-CsAnnouncementFile>] [-TextToSpeechPrompt <text string to be converted to speech>] [-Language <Language for playing the TTS prompt (required for PromptTts)>] [-TargetUri sip:SIPAddress for transferring caller after announcement]
    
    <span data-ttu-id="3998a-p103">Para transferir chamadas para a caixa postal, digite o SIPAddress no formato sip:nomedousuário@nomedodomínio;opaque=app:voicemail (por exemplo, sip:bob@contoso.com;opaque=app:voicemail). Para transferir chamadas para um número de telefone, digite o SIPAddress no formato sip:número@nomedodomínio;user=phone (por exemplo, sip:+ 14255550121@contoso.com;user=phone).</span><span class="sxs-lookup"><span data-stu-id="3998a-p103">For transferring calls to voice mail, type SIPAddress in the format sip:username@domainname;opaque=app:voicemail (for example, sip:bob@contoso.com;opaque=app:voicemail). For transferring calls to a phone number, type SIPAddress in the format sip:number@domainname;user=phone (for example, sip:+ 14255550121@contoso.com;user=phone).</span></span>
    
    <span data-ttu-id="3998a-123">Por exemplo, para especificar um prompt de áudio:</span><span class="sxs-lookup"><span data-stu-id="3998a-123">For example, to specify an audio prompt:</span></span>
    
        $a = Get-Content ".\PromptFile.wav" -ReadCount 0 -Encoding Byte
        Import-CsAnnouncementFile -Parent service:ApplicationServer:pool0@contoso.com -FileName "ChangedNumberMessage.wav" -Content $a
        New-CsAnnouncement -Parent service:ApplicationServer:pool0.contoso.com -Name "Number Changed Announcement" -AudioFilePrompt "ChangedNumberMessage.wav"
    
    <span data-ttu-id="3998a-124">Por exemplo, para especificar um prompt TTS:</span><span class="sxs-lookup"><span data-stu-id="3998a-124">For example, to specify a TTS prompt:</span></span>
    
        New-CsAnnouncement -Parent service:ApplicationServer:pool0.contoso.com -Name "Help Desk Announcement" -TextToSpeechPrompt "The Help Desk number has changed. Please dial 5550100." -Language "en-US"
    
    <span data-ttu-id="3998a-125">Para obter mais detalhes sobre esses cmdlets e ver uma lista dos códigos de idioma a serem usados no parâmetro **TextToSpeechPrompt** , consulte [New-CsAnnouncement](https://docs.microsoft.com/powershell/module/skype/New-CsAnnouncement).</span><span class="sxs-lookup"><span data-stu-id="3998a-125">For more detail about these cmdlets, and to see a list of the language codes to use in the **TextToSpeechPrompt** parameter, see [New-CsAnnouncement](https://docs.microsoft.com/powershell/module/skype/New-CsAnnouncement).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3998a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3998a-126">See Also</span></span>


[<span data-ttu-id="3998a-127">Import-CsAnnouncementFile</span><span class="sxs-lookup"><span data-stu-id="3998a-127">Import-CsAnnouncementFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsAnnouncementFile)  
[<span data-ttu-id="3998a-128">New-CsAnnouncement</span><span class="sxs-lookup"><span data-stu-id="3998a-128">New-CsAnnouncement</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsAnnouncement)  
[<span data-ttu-id="3998a-129">Configurar a tabela de número não atribuído no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3998a-129">Configure the unassigned number table in Lync Server 2013</span></span>](lync-server-2013-configure-the-unassigned-number-table.md)  
  

<span data-ttu-id="3998a-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3998a-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

