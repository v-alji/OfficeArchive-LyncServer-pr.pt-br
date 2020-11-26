---
title: 'Lync Server 2013: Habilitar ou desabilitar descoberta de parceiros de federação'
description: 'Lync Server 2013: habilitar ou desabilitar a descoberta de parceiros de Federação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable discovery of federation partners
ms:assetid: 91fd036b-b1af-47cf-b1cf-0aa0a783c2aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182550(v=OCS.15)
ms:contentKeyID: 48184857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36b91120ffc1ce2bd6cd8b8114f0330e6d39d996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428899"
---
# <a name="enable-or-disable-discovery-of-federation-partners-in-lync-server-2013"></a><span data-ttu-id="e395f-103">Habilitar ou desabilitar descoberta de parceiros de federação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e395f-103">Enable or disable discovery of federation partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e395f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e395f-104">

<span> </span></span></span>

<span data-ttu-id="e395f-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e395f-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e395f-106">No momento em que você implantou seus servidores de borda e habilitou a Federação para a sua organização, você deve especificar se deseja dar suporte à descoberta automática de domínios de parceiro federado.</span><span class="sxs-lookup"><span data-stu-id="e395f-106">At the time you deployed your Edge Servers and enabled federation for your organization, you should have specified whether to support automatic discovery of federated partner domains.</span></span> <span data-ttu-id="e395f-107">Use o procedimento deste tópico para alterar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="e395f-107">Use the procedure in this topic to change that configuration.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e395f-108">O procedimento a seguir pressupõe que você já habilitou a Federação para sua organização.</span><span class="sxs-lookup"><span data-stu-id="e395f-108">The following procedure assumes that you have already enabled federation for your organization.</span></span> <span data-ttu-id="e395f-109">Para obter detalhes sobre como habilitar a Federação, consulte <A href="lync-server-2013-enable-or-disable-remote-user-access.md">habilitar ou desabilitar o acesso de usuário remoto no Lync Server 2013</A> na documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="e395f-109">For details about enabling federation, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A> in the Deployment documentation or the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-automatic-discovery-of-federated-domains-for-your-organization"></a><span data-ttu-id="e395f-110">Para habilitar ou desabilitar a descoberta automática de domínios federados para a sua organização</span><span class="sxs-lookup"><span data-stu-id="e395f-110">To enable or disable automatic discovery of federated domains for your organization</span></span>

1.  <span data-ttu-id="e395f-111">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="e395f-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e395f-112">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e395f-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e395f-113">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e395f-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e395f-114">Na barra de navegação à esquerda, clique em **acesso de usuário externo**, clique em **configuração de borda de acesso**.</span><span class="sxs-lookup"><span data-stu-id="e395f-114">In the left navigation bar, click **External User Access**, click **Access Edge Configuration**.</span></span>

4.  <span data-ttu-id="e395f-115">Na página **configuração de borda de acesso** , clique em **global**, clique em **Editar** e, em seguida, clique em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="e395f-115">On the **Access Edge Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="e395f-116">Em **Editar configuração de borda de acesso**, em **habilitar comunicações com usuários federados**, marque ou desmarque a caixa de seleção **habilitar descoberta de domínio parceiro** para habilitar ou desabilitar a descoberta automática de domínios de parceiros.</span><span class="sxs-lookup"><span data-stu-id="e395f-116">In **Edit Access Edge Configuration**, under **Enable communications with federated users**, select or clear the **Enable partner domain discovery** check box to enable or disable automatic discovery of partner domains.</span></span>

6.  <span data-ttu-id="e395f-117">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="e395f-117">Click **Commit**.</span></span>

<span data-ttu-id="e395f-118">Para habilitar os usuários federados a colaborar com os usuários na implantação do Lync Server, você também deve ter configurado pelo menos uma política de acesso externo para dar suporte ao acesso de usuários federados.</span><span class="sxs-lookup"><span data-stu-id="e395f-118">To enable federated users to collaborate with users in your Lync Server deployment, you must have also configured at least one external access policy to support federated user access.</span></span> <span data-ttu-id="e395f-119">Para obter detalhes, consulte [habilitar ou desabilitar a conectividade de mensagens de chat públicas e de Federação no Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) na documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="e395f-119">For details, see [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) in the Deployment documentation or the Operations documentation.</span></span> <span data-ttu-id="e395f-120">Para obter detalhes sobre o controle de acesso para domínios federados específicos, consulte [gerenciar domínios federados SIP para sua organização no Lync server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md), [gerenciar provedores federados SIP para sua organização no Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) e [gerenciar XMPP parceiros federados no Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="e395f-120">For details about controlling access for specific federated domains, see [Manage SIP federated domains for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md), [Manage SIP federated providers for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) and [Manage XMPP federated partners in Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) in the Operations documentation.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-discovery-of-federation-partners-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e395f-121">Habilitar ou desabilitar a descoberta de parceiros de Federação usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e395f-121">Enabling or Disabling Discovery of Federation Partners by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e395f-122">A descoberta de parceiros de Federação pode ser gerenciada usando o Windows PowerShell e o cmdlet Set-CsAccessEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e395f-122">Discovery of federation partners can be managed by using Windows PowerShell and the Set-CsAccessEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="e395f-123">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e395f-123">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e395f-124">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="e395f-124">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-discovery-of-federation-partners"></a><span data-ttu-id="e395f-125">Para habilitar a descoberta de parceiros de Federação</span><span class="sxs-lookup"><span data-stu-id="e395f-125">To enable discovery of federation partners</span></span>

  - <span data-ttu-id="e395f-126">Para habilitar a descoberta de parceiros de Federação, defina o valor da propriedade **EnablePartnerDiscovery** como True ($true).</span><span class="sxs-lookup"><span data-stu-id="e395f-126">To enable discovery of federation partners, set the value of the **EnablePartnerDiscovery** property to True ($True).</span></span> <span data-ttu-id="e395f-127">Observe que você deve habilitar o roteamento de SRV DNS para alterar esse valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e395f-127">Note that you must enable DNS SRV routing in order to change this property value.</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $True

</div>

<div>

## <a name="to-disable-discovery-of-federation-partners"></a><span data-ttu-id="e395f-128">Para desabilitar a descoberta de parceiros de Federação</span><span class="sxs-lookup"><span data-stu-id="e395f-128">To disable discovery of federation partners</span></span>

  - <span data-ttu-id="e395f-129">Para desabilitar a descoberta de parceiros de Federação, defina o valor da propriedade **EnablePartnerDiscovery** como False ($false):</span><span class="sxs-lookup"><span data-stu-id="e395f-129">To disable discovery of federation partners, set the value of the **EnablePartnerDiscovery** property to False ($False):</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $False

<span data-ttu-id="e395f-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e395f-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

