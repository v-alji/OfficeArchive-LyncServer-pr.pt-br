---
title: 'Lync Server 2013: configurar a Federação para um provedor de serviços de audioconferência'
description: 'Lync Server 2013: configurar a Federação para um provedor de serviços de audioconferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure federation for an audio conferencing provider
ms:assetid: 08dedcce-0d3f-45da-8282-cf2634a41665
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn510996(v=OCS.15)
ms:contentKeyID: 60595883
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c74654224c42618768d881a95031d58be4d55df5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434050"
---
# <a name="configure-federation-for-an-audio-conferencing-provider-in-lync-server-2013"></a><span data-ttu-id="253d8-103">Configurar a Federação para um provedor de audioconferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="253d8-103">Configure federation for an audio conferencing provider in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="253d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="253d8-104">

<span> </span></span></span>

<span data-ttu-id="253d8-105">_**Tópico da última modificação:** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="253d8-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="253d8-106">Se quiser usar um ACP (provedor de serviços de audioconferência) na sua implantação híbrida (Lync Server local com o Lync Online), você precisará configurar a Federação entre a implantação do Lync local e o parceiro ACP como um servidor parceiro autorizado.</span><span class="sxs-lookup"><span data-stu-id="253d8-106">If you want to use an Audio Conferencing Provider (ACP) in your hybrid deployment (Lync Server on-premises with Lync Online), you need to configure federation between your on-premises Lync deployment and the ACP partner as an Allowed Partner Server.</span></span> <span data-ttu-id="253d8-107">É possível configurar a federação adicionando o domínio do parceiro ACP e o servidor de Borda (também conhecido como Proxy de Acesso) à lista de Domínios de Federação para sua implantação no local.</span><span class="sxs-lookup"><span data-stu-id="253d8-107">You can configure federation by adding the ACP partner domain and Edge server (this may also be called the Access Proxy) to the Federated Domains list for your on-premises deployment.</span></span> <span data-ttu-id="253d8-108">Seu parceiro ACP precisará adicionar o FQDN de seu pool de Servidor de Borda no local à lista de domínios de federação permitidos.</span><span class="sxs-lookup"><span data-stu-id="253d8-108">Your ACP partner then needs to add the FQDN of your on-premises Edge Server pool to their allowed federated domains list.</span></span> <span data-ttu-id="253d8-109">Entre em contato com seu provedor de ACP para obter um parceiro detailsYour ACP adicional e, em seguida, precisa adicionar o FQDN do pool de servidores de borda local à lista de domínios federados permitidos.</span><span class="sxs-lookup"><span data-stu-id="253d8-109">Contact your ACP provider for additional detailsYour ACP partner then needs to add the FQDN of your on-premises Edge Server pool to their allowed federated domains list.</span></span>

  - <span data-ttu-id="253d8-110">**Adição do domínio ACP e do servidor de borda como um domínio federado permitido**</span><span class="sxs-lookup"><span data-stu-id="253d8-110">**Adding the ACP Domain and Edge Server as an Allowed Federated Domain**</span></span>
    
    <span data-ttu-id="253d8-111">Para adicionar o domínio ACP como um servidor parceiro permitido (domínio federado permitido), siga as etapas em [Configurar o suporte para domínios externos permitidos no Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span><span class="sxs-lookup"><span data-stu-id="253d8-111">To add the ACP domain as an Allowed Partner Server (allowed Federated Domain), follow the steps in [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span></span> <span data-ttu-id="253d8-112">Para o Servidor de borda, adicione o FQDN do servidor de borda do parceiro ACP.</span><span class="sxs-lookup"><span data-stu-id="253d8-112">For the Edge Server, add the FQDN of the ACP partner’s Edge Server.</span></span> <span data-ttu-id="253d8-113">Pode ser necessário entrar em contato com seu parceiro ACP para obter o FQDN do Servidor de Borda, que também pode ser mencionado pelo ACP como Proxy de Acesso.</span><span class="sxs-lookup"><span data-stu-id="253d8-113">You may need to contact your ACP partner to obtain the FQDN for their Edge Server, which may also be referred to by your ACP as their Access Proxy.</span></span>

  - <span data-ttu-id="253d8-114">**Forneça o FQDN do seu pool do servidor de borda ao parceiro ACP**</span><span class="sxs-lookup"><span data-stu-id="253d8-114">**Provide the FQDN of your Edge Server Pool to the ACP partner**</span></span>
    
    <span data-ttu-id="253d8-115">O parceiro ACP precisa configurar a federação para adicionar seu domínio no local como um Servidor Parceiro Permitido, adicionando o FQDN de seu pool de Servidor de Borda como um domínio de Federação permitido.</span><span class="sxs-lookup"><span data-stu-id="253d8-115">The ACP partner needs to configure federation to add your on-premises domain as an Allowed Partner Server by adding the FQDN of your Edge Server pool as an allowed Federated domain.</span></span>

<span data-ttu-id="253d8-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="253d8-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

