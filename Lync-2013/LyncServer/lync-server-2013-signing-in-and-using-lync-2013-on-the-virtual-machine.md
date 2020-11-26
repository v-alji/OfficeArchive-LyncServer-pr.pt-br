---
title: 'Lync Server 2013: Entrando e usando o Lync 2013 na máquina virtual'
description: 'Lync Server 2013: entrando e usando o Lync 2013 na máquina virtual.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Signing in and using Lync 2013 on the virtual machine
ms:assetid: 6140fc19-5bef-4b58-9b0f-19112b5ecd00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204948(v=OCS.15)
ms:contentKeyID: 48184318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad9a92d450fb9d60aed70617089d95280528892f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444691"
---
# <a name="signing-in-and-using-lync-2013-on-the-virtual-machine"></a><span data-ttu-id="ffb5a-103">Entrando e usando o Lync 2013 na máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ffb5a-103">Signing in and using Lync 2013 on the virtual machine</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffb5a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffb5a-104">

<span> </span></span></span>

<span data-ttu-id="ffb5a-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="ffb5a-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="ffb5a-106">Depois que o plug-in VDI estiver habilitado, as seguintes etapas ocorrerão quando o usuário entrar no Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-106">After the VDI plug-in is enabled, the following steps occur when the user signs in to Lync 2013.</span></span>

1.  <span data-ttu-id="ffb5a-107">O usuário digita suas credenciais no cliente do Lync 2013 em execução na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-107">The user types his or her credentials in to the Lync 2013 client running on the virtual machine.</span></span>

2.  <span data-ttu-id="ffb5a-108">Depois que o Lync detecta a disponibilidade do plug-in VDI, o Lync solicita que o usuário digite novamente suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-108">After Lync detects the availability of the VDI plug-in, Lync prompts the user to re-enter his or her credentials.</span></span> <span data-ttu-id="ffb5a-109">Nessa caixa de diálogo, é recomendável que o usuário marque a caixa de seleção **Salvar minha senha** para que não precise inserir as credenciais na próxima entrada.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-109">In this dialog box, we recommend that the user select the **Save my password** check box so that he or she will not be required to enter credentials during subsequent sign in.</span></span>

3.  <span data-ttu-id="ffb5a-110">O Lync começa a emparelhar com o plug-in VDI.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-110">Lync begins pairing with the VDI plug-in.</span></span> <span data-ttu-id="ffb5a-111">Antes da conclusão do emparelhamento, o cliente exibe dois ícones na barra de status do Lync.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-111">Before pairing is complete, the client displays two icons in the Lync status bar.</span></span> <span data-ttu-id="ffb5a-112">O ícone no canto inferior esquerdo indica que não há dispositivos de áudio disponíveis, e o ícone piscante no canto inferior direito indica que o emparelhamento VDI está em andamento, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="ffb5a-112">The icon in the lower left indicates that no audio devices are available, and the blinking icon in the lower right indicates that the VDI pairing is in progress, as shown:</span></span>
    
    <span data-ttu-id="ffb5a-113">![Ícone de VDI do Lync mostrando o emparelhamento com êxito](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Ícone de VDI do Lync mostrando o emparelhamento com êxito")</span><span class="sxs-lookup"><span data-stu-id="ffb5a-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>  

4.  <span data-ttu-id="ffb5a-114">Após o emparelhamento bem-sucedido de VDI, os ícones mudarão para indicar o dispositivo de áudio que será usado para chamadas e o êxito do emparelhamento de VDI:</span><span class="sxs-lookup"><span data-stu-id="ffb5a-114">After VDI pairing is successful, the icons change to indicate the audio device that will be used for calls and the VDI pairing success:</span></span>
    
    <span data-ttu-id="ffb5a-115">![Ícone de emparelhamento da VDI do Lync mostrando sucesso](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Ícone de emparelhamento da VDI do Lync mostrando sucesso")</span><span class="sxs-lookup"><span data-stu-id="ffb5a-115">![Lync VDI pairing icon showing success](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Lync VDI pairing icon showing success")</span></span>  

5.  <span data-ttu-id="ffb5a-116">Após os pares do Lync com o plug-in VDI, o usuário pode ver sua presença em dispositivos compatíveis com o Lync conectados ao computador local.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-116">After Lync pairs with the VDI plug-in, the user can see his or her presence on Lync compatible devices that are connected to the local computer.</span></span> <span data-ttu-id="ffb5a-117">Agora o usuário pode fazer e atender chamadas normalmente.</span><span class="sxs-lookup"><span data-stu-id="ffb5a-117">The user can now place and answer calls as usual.</span></span>

<span data-ttu-id="ffb5a-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffb5a-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

