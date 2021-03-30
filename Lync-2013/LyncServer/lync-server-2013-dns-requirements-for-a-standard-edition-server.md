---
title: 'Lync Server 2013: Requisitos de DNS para servidor Standard Edition'
description: 'Lync Server 2013: requisitos dns para um servidor Standard Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390306"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="c37bf-103">Requisitos de DNS para servidor Standard Edition no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c37bf-103">DNS requirements for a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c37bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c37bf-104">

<span> </span></span></span>

<span data-ttu-id="c37bf-105">_**Tópico Última Modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="c37bf-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="c37bf-106">Esta seção descreve os registros DNS (Sistema de Nomes de Domínio) necessários para a implantação de servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="c37bf-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="c37bf-107">Registros DNS para servidores Standard Edition</span><span class="sxs-lookup"><span data-stu-id="c37bf-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="c37bf-108">A tabela a seguir especifica os requisitos DNS para a implantação do servidor Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="c37bf-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c37bf-109">Cenário da implantação</span><span class="sxs-lookup"><span data-stu-id="c37bf-109">Deployment scenario</span></span></th>
<th><span data-ttu-id="c37bf-110">Requisitos de DNS</span><span class="sxs-lookup"><span data-stu-id="c37bf-110">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c37bf-111">Servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="c37bf-111">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="c37bf-112">Um registro A interno que resolve o nome de domínio totalmente qualificado (FQDN) do servidor para seu endereço IP.</span><span class="sxs-lookup"><span data-stu-id="c37bf-112">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c37bf-113">Entrada automática do cliente</span><span class="sxs-lookup"><span data-stu-id="c37bf-113">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="c37bf-114">Para cada domínio SIP com suporte, um registro SRV para _sipinternaltls._tcp. &lt; domínio &gt; sobre a porta 5061 que mapeia para o FQDN do servidor Standard Edition que autentica e redireciona solicitações de cliente para entrada.</span><span class="sxs-lookup"><span data-stu-id="c37bf-114">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="c37bf-115">Para obter detalhes, consulte REQUISITOS DNS para entrada automática do <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">cliente no Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="c37bf-115">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c37bf-116">Descoberta do serviço Web de Atualização de Dispositivo por dispositivos UC (Comunicações Unificadas)</span><span class="sxs-lookup"><span data-stu-id="c37bf-116">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="c37bf-117">Um registro A interno com o nome ucupdates-r2. &lt; Domínio SIP que resolve para o endereço IP do servidor Standard Edition que hospeda &gt; o serviço Web de Atualização de Dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c37bf-117">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="c37bf-118">Na situação em que um dispositivo UC está ligado, mas um usuário nunca fez logons no dispositivo, o registro A permite que o dispositivo descubra o servidor que hospeda o serviço Web de Atualização de Dispositivo e obtenha atualizações.</span><span class="sxs-lookup"><span data-stu-id="c37bf-118">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="c37bf-119">Caso contrário, os dispositivos obtêm essas informações por meio do provisionamento em banda na primeira vez que o usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="c37bf-119">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span> <span data-ttu-id="c37bf-120">Para obter detalhes, consulte <a href="lync-server-2013-device-update-web-service.md">Device Update Web service in Lync Server 2013</a> na documentação Operações.</span><span class="sxs-lookup"><span data-stu-id="c37bf-120">For details, see <a href="lync-server-2013-device-update-web-service.md">Device Update Web service in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c37bf-121">Um proxy reverso para dar suporte ao tráfego HTTP</span><span class="sxs-lookup"><span data-stu-id="c37bf-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="c37bf-122">Um registro A externo que resolve o FQDN do farm web externo para o endereço IP externo do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="c37bf-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="c37bf-123">Os clientes e dispositivos UC usam esse registro para se conectar ao proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="c37bf-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="c37bf-124">Para obter detalhes, <a href="lync-server-2013-determine-dns-requirements.md">consulte Determine DNS requirements for Lync Server 2013</a> na documentação planejamento.</span><span class="sxs-lookup"><span data-stu-id="c37bf-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c37bf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c37bf-125">See Also</span></span>


[<span data-ttu-id="c37bf-126">Requisitos dns para entrada automática do cliente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c37bf-126">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[<span data-ttu-id="c37bf-127">Determinar requisitios de DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c37bf-127">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="c37bf-128">Serviço Web de Atualização de Dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c37bf-128">Device Update Web service in Lync Server 2013</span></span>](lync-server-2013-device-update-web-service.md)  
  

<span data-ttu-id="c37bf-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c37bf-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

