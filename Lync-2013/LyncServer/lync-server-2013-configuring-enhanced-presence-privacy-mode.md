---
title: 'Lync Server 2013: Configurando o modo de privacidade de presença avançada'
description: 'Lync Server 2013: Configurando o modo de privacidade de presença avançada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring enhanced presence privacy mode
ms:assetid: e7a6b873-486d-4dfb-a967-c48f61f237f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399028(v=OCS.15)
ms:contentKeyID: 48185664
ms.date: 12/09/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c8eab347d233c23a9a4becf119dee673d3021dfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433168"
---
# <a name="configuring-enhanced-presence-privacy-mode-in-lync-server-2013"></a><span data-ttu-id="d25ba-103">Configurando o modo de privacidade de presença avançada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d25ba-103">Configuring enhanced presence privacy mode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d25ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d25ba-104">

<span> </span></span></span>

<span data-ttu-id="d25ba-105">_**Tópico da última modificação:** 2014-12-08_</span><span class="sxs-lookup"><span data-stu-id="d25ba-105">_**Topic Last Modified:** 2014-12-08_</span></span>

<span data-ttu-id="d25ba-106">Com o modo de privacidade de presença avançada, os usuários podem restringir as informações de presença para que fiquem visíveis somente para os contatos listados na lista de contatos do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="d25ba-106">With enhanced presence privacy mode, users can restrict their presence information so that it is visible only to the contacts listed in their Lync 2013 Contacts list.</span></span> <span data-ttu-id="d25ba-107">Os cmdlets **New-CsPrivacyConfiguration** e **set-CsPrivacyConfiguration** têm um parâmetro EnablePrivacyMode controla essa opção.</span><span class="sxs-lookup"><span data-stu-id="d25ba-107">The **New-CsPrivacyConfiguration** and **Set-CsPrivacyConfiguration** cmdlets have an EnablePrivacyMode parameter controls this option.</span></span> <span data-ttu-id="d25ba-108">Quando EnablePrivacyMode está definido como true, a opção de restringir as informações de presença aos contatos torna-se disponível nas opções de status do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="d25ba-108">When EnablePrivacyMode is set to True, the option to restrict presence information to contacts becomes available in the Lync 2013 Status options.</span></span> <span data-ttu-id="d25ba-109">Quando EnablePrivacyMode está definido como false, os usuários podem escolher para sempre permitir que todos vejam suas informações de presença ou para aderir a quaisquer alterações futuras feitas pelo administrador no modo de privacidade.</span><span class="sxs-lookup"><span data-stu-id="d25ba-109">When EnablePrivacyMode is set to False, users can choose either to always allow everyone to see their presence information or to adhere to any future changes the administrator makes to the privacy mode.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d25ba-110">As configurações de privacidade do Lync 2013 e Lync 2010 não são respeitadas pelas versões anteriores (Microsoft Office Communicator 2007 R2 ou Microsoft Office Communicator 2007).</span><span class="sxs-lookup"><span data-stu-id="d25ba-110">Lync 2013 and Lync 2010 privacy settings are not honored by previous versions (Microsoft Office Communicator 2007 R2 or Microsoft Office Communicator 2007).</span></span> <span data-ttu-id="d25ba-111">Se as versões anteriores do Office Communicator tiverem permissão para entrar, um status do usuário do Lync 2013, informações de contato ou imagem podem ser visualizados por alguém que não tenha sido autorizado a visualizá-lo.</span><span class="sxs-lookup"><span data-stu-id="d25ba-111">If previous versions of Office Communicator are allowed to sign in, a Lync 2013 user’s status, contact information, or picture could be viewed by someone who has not been authorized to view it.</span></span> <span data-ttu-id="d25ba-112">Além disso, as configurações de privacidade do usuário do Lync 2013 são redefinidas se entrarem em mais tarde com a versão anterior do Communicator.</span><span class="sxs-lookup"><span data-stu-id="d25ba-112">Additionally, a Lync 2013 user’s privacy settings are reset if he or she later signs in with previous version of Communicator.</span></span><BR><span data-ttu-id="d25ba-113">Por esses motivos, em um cenário de migração, antes de habilitar o modo de privacidade de presença avançada:</span><span class="sxs-lookup"><span data-stu-id="d25ba-113">For these reasons, in a migration scenario, before you enable enhanced presence privacy mode:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="d25ba-114">Certifique-se de que todos os usuários tenham o Lync 2013 instalado.</span><span class="sxs-lookup"><span data-stu-id="d25ba-114">Ensure that every user has Lync 2013 installed.</span></span></P>
> <LI>
> <P><span data-ttu-id="d25ba-115">Defina uma regra de política de versão do cliente para impedir que versões anteriores do Communicator entrem em entrar.</span><span class="sxs-lookup"><span data-stu-id="d25ba-115">Define a client version policy rule to prevent previous versions of Communicator from signing in.</span></span></P></LI></UL>



</div>

<div>

## <a name="to-enable-enhanced-presence-privacy-mode"></a><span data-ttu-id="d25ba-116">Para habilitar o modo de privacidade de presença avançada</span><span class="sxs-lookup"><span data-stu-id="d25ba-116">To enable enhanced presence privacy mode</span></span>

1.  <span data-ttu-id="d25ba-117">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d25ba-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="d25ba-118">Execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d25ba-118">Run the following command:</span></span>
    
        Get-CsPrivacyConfiguration | Set-CsPrivacyConfiguration -EnablePrivacyMode $True
    
    <span data-ttu-id="d25ba-119">Esse comando habilita o modo de privacidade para todas as configurações de privacidade em uso no momento na organização.</span><span class="sxs-lookup"><span data-stu-id="d25ba-119">This command enables privacy mode for all the privacy configuration settings currently in use in the organization.</span></span> <span data-ttu-id="d25ba-120">Para obter mais informações sobre como as configurações de política do modo de privacidade de presença avançada do Lync Server gerencia a presença de contatos para o cliente do Lync 2013, consulte o artigo Microsoft Knowledge base [habilitar o modo de privacidade de presença avançada do Lync Server atualiza o status de presença de alguns contatos do Lync para "não disponível"](https://support.microsoft.com/kb/3020057).</span><span class="sxs-lookup"><span data-stu-id="d25ba-120">For more information about how the Lync Server enhanced presence privacy mode policy configurations manages contact presence for the Lync 2013 client, see the Microsoft KB article [Enabling Lync Server enhanced presence privacy mode updates the presence status of some Lync contacts to "unavailable"](https://support.microsoft.com/kb/3020057).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d25ba-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d25ba-121">See Also</span></span>


[<span data-ttu-id="d25ba-122">Get-CsPrivacyConfiguration</span><span class="sxs-lookup"><span data-stu-id="d25ba-122">Get-CsPrivacyConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsPrivacyConfiguration)  
[<span data-ttu-id="d25ba-123">New-CsPrivacyConfiguration</span><span class="sxs-lookup"><span data-stu-id="d25ba-123">New-CsPrivacyConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsPrivacyConfiguration)  
[<span data-ttu-id="d25ba-124">Set-CsPrivacyConfiguration</span><span class="sxs-lookup"><span data-stu-id="d25ba-124">Set-CsPrivacyConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration)  
  

<span data-ttu-id="d25ba-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d25ba-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

