---
title: Configurar uma entrada de aplicativo confiável para controle de chamada remota
description: Configurar uma entrada de aplicativo confiável para o controle de chamada remota.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trusted application entry for remote call control
ms:assetid: 37777f93-8b24-40cf-808e-7c6230eb2132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558636(v=OCS.15)
ms:contentKeyID: 48183829
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa5341dc220853670cf000f5b0d5dc379c02fa51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434148"
---
# <a name="configure-a-trusted-application-entry-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="ce87a-103">Configurar uma entrada de aplicativo confiável para controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce87a-103">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce87a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce87a-104">

<span> </span></span></span>

<span data-ttu-id="ce87a-105">_**Tópico da última modificação:** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="ce87a-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="ce87a-106">O gateway SIP/CSTA deve ser configurado como um aplicativo confiável para que o Lync Server aplique uma rota estática para chamadas de roteamento para o gateway.</span><span class="sxs-lookup"><span data-stu-id="ce87a-106">The SIP/CSTA gateway must be configured as a trusted application in order for Lync Server to apply a static route to route calls to the gateway.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="ce87a-107">Se você estiver migrando usuários de uma versão anterior da implantação do Lync Server, certifique-se de que removeu todas as entradas de aplicativo confiáveis existentes (anteriormente conhecidas como entradas de host autorizadas) que você criou para o gateway SIP/CSTA antes de seguir os procedimentos deste tópico.</span><span class="sxs-lookup"><span data-stu-id="ce87a-107">If you're migrating users from a previous version of Lync Server deployment, be sure that you removed all existing trusted application entries (previously known as authorized host entries) you created for the SIP/CSTA gateway before following the procedures in this topic.</span></span> <span data-ttu-id="ce87a-108">Para obter detalhes, consulte <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">remover um host autorizado herdado no Lync Server 2013 (opcional)</A>.</span><span class="sxs-lookup"><span data-stu-id="ce87a-108">For details, see <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Remove a legacy authorized host in Lync Server 2013 (optional)</A>.</span></span><BR><span data-ttu-id="ce87a-109">Se você planeja implantar um novo controle de chamada remota usando uma conexão TCP (Transmission Control Protocol), você precisará verificar se o <STRONG>uso do serviço de limite para endereços IP selecionados</STRONG> deve ser definido em pools e aplicativos confiáveis existentes, se você quiser usar a mesma porta TCP para o novo aplicativo confiável.</span><span class="sxs-lookup"><span data-stu-id="ce87a-109">If you plan to deploy new remote call control by using a Transmission Control Protocol (TCP) connection, you need to verify that <STRONG>Limit service usage to selected IP addresses</STRONG> should be set on existing trusted applications and pools, if you want to use the same TCP port for the new trusted application.</span></span>



</div>

<div>

## <a name="to-configure-a-trusted-application-entry-for-the-sipcsta-gateway"></a><span data-ttu-id="ce87a-110">Para configurar uma entrada de aplicativo confiável para o gateway SIP/CSTA</span><span class="sxs-lookup"><span data-stu-id="ce87a-110">To configure a trusted application entry for the SIP/CSTA gateway</span></span>

1.  <span data-ttu-id="ce87a-111">Faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo RTCUniversalServerAdmins ou uma função de controle de acesso baseado em função (RBAC) à qual você atribuiu o cmdlet **New-CsTrustedApplicationPool** .</span><span class="sxs-lookup"><span data-stu-id="ce87a-111">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or a role-based access control (RBAC) role to which you have assigned the **New-CsTrustedApplicationPool** cmdlet.</span></span>

2.  <span data-ttu-id="ce87a-112">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ce87a-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ce87a-113">Para criar uma entrada de aplicativo confiável, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="ce87a-113">To create a trusted application entry, do one of the following:</span></span>
    
      - <span data-ttu-id="ce87a-114">Para uma conexão de TLS (Transport Layer Security), digite o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce87a-114">For a Transport Layer Security (TLS) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="ce87a-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ce87a-115">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity rccgateway.contoso.net -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true
    
      - <span data-ttu-id="ce87a-116">Para uma conexão TCP (Transmission Control Protocol), digite o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce87a-116">For a Transmission Control Protocol (TCP) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <IP address or FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="ce87a-117">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ce87a-117">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity 192.168.0.240 -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true

4.  <span data-ttu-id="ce87a-118">Para adicionar o aplicativo confiável ao pool, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="ce87a-118">To add the trusted application to the pool, do one of the following:</span></span>
    
      - <span data-ttu-id="ce87a-119">Para uma conexão TLS, digite o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce87a-119">For a TLS connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway>
        
        <span data-ttu-id="ce87a-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ce87a-120">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn rccgateway.contoso.net -Port 5065
    
      - <span data-ttu-id="ce87a-121">Para uma conexão TCP, digite o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce87a-121">For a TCP connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <IP address or FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway> -EnableTcp
        
        <span data-ttu-id="ce87a-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ce87a-122">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn 192.169.0.240 -Port 5065 -EnableTcp

5.  <span data-ttu-id="ce87a-123">Para implementar as alterações publicadas feitas à topologia, digite o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce87a-123">To implement the published changes you have made to the topology, type the following at the command prompt:</span></span>
    
        Enable-CsTopology

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ce87a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce87a-124">See Also</span></span>


[<span data-ttu-id="ce87a-125">Configurar uma rota estática para controle de chamada remota no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce87a-125">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)  
[<span data-ttu-id="ce87a-126">Definir um endereço SIP de gateway SIP/CSTA no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce87a-126">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)  
  

<span data-ttu-id="ce87a-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce87a-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

