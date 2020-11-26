---
title: 'Lync Server 2013: excluir um comunicado'
description: 'Lync Server 2013: excluir um anúncio.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an announcement
ms:assetid: 26ea7149-4470-4c22-9bab-8a4065aca44e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687998(v=OCS.15)
ms:contentKeyID: 49733588
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 722028f684734504d86bfc986250a2a1dd17fabc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430620"
---
# <a name="delete-an-announcement-in-lync-server-2013"></a><span data-ttu-id="9fbe6-103">Excluir um comunicado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fbe6-103">Delete an announcement in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9fbe6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9fbe6-104">

<span> </span></span></span>

<span data-ttu-id="9fbe6-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9fbe6-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9fbe6-106">Use o procedimento a seguir para excluir um anúncio que é usado para chamadas para números não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="9fbe6-106">Use the following procedure to delete an announcement that is used for calls to unassigned numbers.</span></span>

<div>

## <a name="to-delete-an-announcement"></a><span data-ttu-id="9fbe6-107">Para excluir um anúncio</span><span class="sxs-lookup"><span data-stu-id="9fbe6-107">To delete an announcement</span></span>

1.  <span data-ttu-id="9fbe6-108">Faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo RTCUniversalServerAdmins ou com os direitos de usuário necessários, conforme descrito em [permissões de configuração de representante no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="9fbe6-108">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="9fbe6-109">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="9fbe6-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="9fbe6-p101">Lista todos os anúncios em sua organização. Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="9fbe6-p101">List all the announcements in your organization. At the command line, run:</span></span>
    
        Get-CsAnnouncement

4.  <span data-ttu-id="9fbe6-p102">Na lista resultante, localize o anúncio que deseja excluir e copie o GUID. Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="9fbe6-p102">In the resulting list, locate the announcement you want to delete, and copy the GUID. Then, at the command line, run:</span></span>
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>" 
    
    <span data-ttu-id="9fbe6-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9fbe6-114">For example:</span></span>
    
        Remove-CsAnnouncement -Identity "ApplicationServer:Redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9fbe6-115">Para obter detalhes sobre mais opções, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsAnnouncement">Get-CsAnnouncement</A> e <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsAnnouncement">Remove-CsAnnouncement</A>.</span><span class="sxs-lookup"><span data-stu-id="9fbe6-115">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsAnnouncement">Get-CsAnnouncement</A> and <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsAnnouncement">Remove-CsAnnouncement</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9fbe6-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fbe6-116">See Also</span></span>


[<span data-ttu-id="9fbe6-117">Criar um anúncio no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fbe6-117">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)  


[<span data-ttu-id="9fbe6-118">Remove-CsAnnouncement</span><span class="sxs-lookup"><span data-stu-id="9fbe6-118">Remove-CsAnnouncement</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsAnnouncement)  
[<span data-ttu-id="9fbe6-119">Get-CsAnnouncement</span><span class="sxs-lookup"><span data-stu-id="9fbe6-119">Get-CsAnnouncement</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAnnouncement)  
  

<span data-ttu-id="9fbe6-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9fbe6-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

