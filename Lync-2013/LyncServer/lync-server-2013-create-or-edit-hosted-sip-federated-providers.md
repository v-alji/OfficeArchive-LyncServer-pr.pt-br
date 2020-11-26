---
title: 'Lync Server 2013: Criar ou editar provedores hospedados federados SIP'
description: 'Lync Server 2013: crie ou edite provedores federados SIP hospedados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit hosted SIP federated providers
ms:assetid: 0dd6dcb6-a88d-46b8-9c96-b35967309bcd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552445(v=OCS.15)
ms:contentKeyID: 48679556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aaaa1b29b9a85332b85dfb7a1f258503fa4e9c77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431901"
---
# <a name="create-or-edit-hosted-sip-federated-providers-lync-server-2013"></a><span data-ttu-id="793c4-103">Criar ou editar provedores hospedados federados SIP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="793c4-103">Create or edit hosted SIP federated providers Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="793c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="793c4-104">

<span> </span></span></span>

<span data-ttu-id="793c4-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="793c4-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="793c4-106">A conectividade de mensagens instantâneas do provedor hospedado permite que os usuários em sua organização usem mensagens instantâneas para se comunicar com os usuários de serviços de mensagens instantâneas fornecidos pelos provedores hospedados, incluindo o Microsoft 365 e o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="793c4-106">Hosted provider instant messaging (IM) connectivity enables users in your organization to use IM to communicate with users of IM services provided by hosted providers, including Microsoft 365 and Lync Online.</span></span>

<span data-ttu-id="793c4-107">Cada provedor hospedado é configurado com o nome de domínio totalmente qualificado do servidor de borda do provedor, e o nível de verificação padrão **permite que os usuários se comuniquem somente com as pessoas da lista de contatos que usam esse provedor**.</span><span class="sxs-lookup"><span data-stu-id="793c4-107">Each hosted provider is configured with the provider’s Edge server fully qualified domain name, and the default verification level **Allow users to communicate only with people on their Contacts list who use this provider**.</span></span>

<span data-ttu-id="793c4-108">Use o procedimento a seguir para criar ou editar provedores hospedados:</span><span class="sxs-lookup"><span data-stu-id="793c4-108">Use the following procedure to create or edit Hosted providers:</span></span>

<div>

## <a name="to-create-or-edit-hosted-providers"></a><span data-ttu-id="793c4-109">Para criar ou editar provedores hospedados</span><span class="sxs-lookup"><span data-stu-id="793c4-109">To create or edit hosted providers</span></span>

1.  <span data-ttu-id="793c4-110">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="793c4-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="793c4-111">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="793c4-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="793c4-112">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="793c4-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="793c4-113">Na barra de navegação à esquerda, clique em **Federação e acesso externo** e, em seguida, clique em **provedores federados SIP**.</span><span class="sxs-lookup"><span data-stu-id="793c4-113">In the left navigation bar, click **Federation and External Access**, and then click **SIP Federated Providers**.</span></span>

4.  <span data-ttu-id="793c4-114">Se você precisar criar um novo provedor hospedado, clique em **novo** e em **provedor hospedado**.</span><span class="sxs-lookup"><span data-stu-id="793c4-114">If you need to create a new Hosted provider, click **New** and then click **Hosted provider**.</span></span>

5.  <span data-ttu-id="793c4-115">Se você precisar editar uma entrada da lista de provedores hospedados, selecione um provedor hospedado, clique em **Editar** e, em seguida, clique em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="793c4-115">If you need to edit an entry from the list of Hosted providers, select a hosted provider, click **Edit**, then click **Show details**.</span></span>

6.  <span data-ttu-id="793c4-116">Na página **Editar Provedor federado SIP** , você pode digitar ou editar as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="793c4-116">On the **Edit SIP Federated Provider** page, you can type or edit the following settings:</span></span>
    
      - <span data-ttu-id="793c4-117">**Habilitar comunicações com este provedor**   Selecionar essa configuração permite a comunicação com os usuários do provedor.</span><span class="sxs-lookup"><span data-stu-id="793c4-117">**Enable communications with this provider**   Selecting this setting enables communications with this provider’s users.</span></span>
    
      - <span data-ttu-id="793c4-118">**Nome do provedor:**   Uma propriedade necessária, digite o nome do provedor como ele será refletido na listagem de provedores Federados da SIP.</span><span class="sxs-lookup"><span data-stu-id="793c4-118">**Provider name:**   A required property, type the name of the provider as it will be reflected in the listing of SIP Federated Providers.</span></span>
    
      - <span data-ttu-id="793c4-119">**Serviço de borda de acesso (FQDN):**   Uma propriedade necessária, digite o nome de domínio totalmente qualificado do serviço de borda de acesso do provedor hospedado que você está configurando.</span><span class="sxs-lookup"><span data-stu-id="793c4-119">**Access Edge service (FQDN):**   A required property, type the fully qualified domain name of the Access Edge service of the hosted provider that you are configuring.</span></span> <span data-ttu-id="793c4-120">Essas informações devem ser fornecidas pelo provedor de hospedagem e só devem ser alteradas se o provedor hospedado fizer uma alteração no FQDN do serviço de borda de acesso no provedor hospedado.</span><span class="sxs-lookup"><span data-stu-id="793c4-120">This information should be provided by the hosted provider, and should only be changed if the hosted provider makes a change to the FQDN of the Access Edge service at the hosted provider.</span></span>
    
      - <span data-ttu-id="793c4-121">**Nível de verificação padrão:**   A configuração padrão, **permitir que os usuários se comuniquem com as pessoas da lista de contatos que usam esse provedor** limitarão a comunicação a contatos que você aceitou e estão em sua lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="793c4-121">**Default verification level:**   The default setting, **Allow users to communicate with people on their Contacts list who use this provider** will limit communication to contacts that you have accepted and are in your contact list.</span></span>
        
        <span data-ttu-id="793c4-122">Selecionar **permitir que os usuários se comuniquem com todos que usam esse provedor** remove a restrição que você deve ter recebido e aceito um convite de contato.</span><span class="sxs-lookup"><span data-stu-id="793c4-122">Selecting **Allow users to communicate with everyone using this provider** removes the restriction that you must have received and accepted a contact invite.</span></span> <span data-ttu-id="793c4-123">Essa configuração não limita quem pode contatá-lo na rede do provedor hospedado.</span><span class="sxs-lookup"><span data-stu-id="793c4-123">This setting does not limit who can contact you from the hosted provider’s network.</span></span>

7.  <span data-ttu-id="793c4-124">Quando terminar de definir as configurações, clique em **confirmar** para salvar ou clique em **Cancelar** para descartar as alterações.</span><span class="sxs-lookup"><span data-stu-id="793c4-124">When you are done configuring the settings, click **Commit** to save, or click **Cancel** to discard your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="793c4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="793c4-125">See Also</span></span>


[<span data-ttu-id="793c4-126">Configurar políticas para controlar o acesso de usuário público no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="793c4-126">Configure policies to control public user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-public-user-access.md)  
[<span data-ttu-id="793c4-127">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="793c4-127">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
  

<span data-ttu-id="793c4-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="793c4-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

