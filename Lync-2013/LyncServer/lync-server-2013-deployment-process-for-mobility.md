---
title: 'Lync Server 2013: Processo de implantação para mobilidade'
description: 'Lync Server 2013: processo de implantação para mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for mobility
ms:assetid: 5a1cebda-c14b-4ff4-9c36-f7caa868160f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690023(v=OCS.15)
ms:contentKeyID: 48184220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b49d69af899f6d9f2ac1db5040d017a9d62ce9eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390243"
---
# <a name="deployment-process-for-mobility-in-lync-server-2013"></a><span data-ttu-id="48b6a-103">Processo de implantação para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48b6a-103">Deployment process for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48b6a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48b6a-104">

<span> </span></span></span>

<span data-ttu-id="48b6a-105">_**Tópico da última modificação:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="48b6a-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013. It is noted accordingly.

<span data-ttu-id="48b6a-106">Esta seção descreve a sequência de etapas necessárias para implantar o recurso de mobilidade do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48b6a-106">This section describes the sequence of steps required to deploy the Lync Server 2013 mobility feature.</span></span>

### <a name="mobility-deployment-process"></a><span data-ttu-id="48b6a-107">Processo de implantação de mobilidade</span><span class="sxs-lookup"><span data-stu-id="48b6a-107">Mobility Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48b6a-108">Fase</span><span class="sxs-lookup"><span data-stu-id="48b6a-108">Phase</span></span></th>
<th><span data-ttu-id="48b6a-109">Etapas</span><span class="sxs-lookup"><span data-stu-id="48b6a-109">Steps</span></span></th>
<th><span data-ttu-id="48b6a-110">Permissões</span><span class="sxs-lookup"><span data-stu-id="48b6a-110">Permissions</span></span></th>
<th><span data-ttu-id="48b6a-111">Documentação de Implantação</span><span class="sxs-lookup"><span data-stu-id="48b6a-111">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48b6a-112">Criar registros de sistema de nomes de domínio (DNS)</span><span class="sxs-lookup"><span data-stu-id="48b6a-112">Create Domain Name System (DNS) records</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="48b6a-113">Crie um registro DNS interno CNAME ou um registro (host, se IPv6, AAAA) para resolver a URL interna do serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="48b6a-113">Create an internal DNS CNAME or A (host, if IPv6, AAAA) record to resolve the internal Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-114">Crie um registro DNS externo ou um registro (host, se IPv6, AAAA) para resolver a URL externa do serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="48b6a-114">Create an external DNS CNAME or A (host, if IPv6, AAAA) record to resolve the external Autodiscover Service URL.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="48b6a-115">Admins. do Domínio</span><span class="sxs-lookup"><span data-stu-id="48b6a-115">Domain Admins</span></span></p>
<p><span data-ttu-id="48b6a-116">DnsAdmins</span><span class="sxs-lookup"><span data-stu-id="48b6a-116">DnsAdmins</span></span></p></td>
<td><p><span data-ttu-id="48b6a-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Criando registros de DNS para o Serviço de Autodiscover no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="48b6a-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Creating DNS records for the Autodiscover Service in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48b6a-118">Modificar certificados</span><span class="sxs-lookup"><span data-stu-id="48b6a-118">Modify certificates</span></span></p></td>
<td><p><span data-ttu-id="48b6a-119">Adicione entradas de nome alternativo à entidade aos seguintes certificados para dar suporte a conexões seguras para usuários móveis:</span><span class="sxs-lookup"><span data-stu-id="48b6a-119">Add subject alternative name entries to the following certificates to support secure connections for mobile users:</span></span></p>
<ul>
<li><p><span data-ttu-id="48b6a-120">Certificado de diretor</span><span class="sxs-lookup"><span data-stu-id="48b6a-120">Director certificate</span></span></p></li>
<li><p><span data-ttu-id="48b6a-121">Certificado de pool de front-end</span><span class="sxs-lookup"><span data-stu-id="48b6a-121">Front End pool certificate</span></span></p></li>
<li><p><span data-ttu-id="48b6a-122">Certificado de proxy reverso</span><span class="sxs-lookup"><span data-stu-id="48b6a-122">Reverse proxy certificate</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="48b6a-123">Administrador local</span><span class="sxs-lookup"><span data-stu-id="48b6a-123">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="48b6a-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Modificando certificados para mobilidade no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="48b6a-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Modifying certificates for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48b6a-125">Configurar o proxy inverso</span><span class="sxs-lookup"><span data-stu-id="48b6a-125">Configure the reverse proxy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="48b6a-126">Atribua certificados atualizados com nomes alternativos de entidades para o ouvinte Secure Sockets Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="48b6a-126">Assign certificates updated with subject alternative names to the Secure Sockets Layer (SSL) Listener.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-127">Reconfigure a regra de publicação na Web para a URL do serviço de descoberta automática externa.</span><span class="sxs-lookup"><span data-stu-id="48b6a-127">Reconfigure the web publishing rule for the external Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-128">Verifique se há uma regra de publicação na Web para a URL de serviços Web externos do Lync Server 2013 em seu pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="48b6a-128">Be sure that a web publishing rule exists for the external Lync Server 2013 Web Services URL on your Front End pool.</span></span></p></li>
</ul>
<p><span data-ttu-id="48b6a-129">Ou</span><span class="sxs-lookup"><span data-stu-id="48b6a-129">Or</span></span></p>
<ul>
<li><p><span data-ttu-id="48b6a-130">Se você optar por usar HTTP para a solicitação de descoberta automática inicial e não atualizar listas de nomes alternativos de entidades nos certificados, configure uma nova regra de publicação na Web ou RECONFIGURE uma regra de publicação existente para HTTP porta 80.</span><span class="sxs-lookup"><span data-stu-id="48b6a-130">If you choose to use HTTP for the initial Autodiscover request and do not update subject alternative name lists on the certificates, configure a new web publishing rule or reconfigure an existing publishing rule for port 80 HTTP.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="48b6a-131">Administrador local</span><span class="sxs-lookup"><span data-stu-id="48b6a-131">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="48b6a-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configurando o proxy reverso para mobilidade no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="48b6a-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48b6a-133">Testar a implantação de mobilidade do Lync 2010 Mobile usando o serviço de mobilidade MCX</span><span class="sxs-lookup"><span data-stu-id="48b6a-133">Test your mobility deployment for Lync 2010 Mobile using the Mcx Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="48b6a-134">Execute <strong>Test-CsMcxP2PIM</strong> para testar o envio de uma mensagem instantânea de uma pessoa para outra.</span><span class="sxs-lookup"><span data-stu-id="48b6a-134">Run <strong>Test-CsMcxP2PIM</strong> to test sending an instant message from one person to another.</span></span></p>
<p><span data-ttu-id="48b6a-135">Consulte a documentação do cmdlet do Shell de gerenciamento do Lync Server para <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">testar-CsMcxP2PIM</a> para obter uma lista completa de opções.</span><span class="sxs-lookup"><span data-stu-id="48b6a-135">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">Test-CsMcxP2PIM</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="48b6a-136">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="48b6a-136">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="48b6a-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verificando sua implantação de mobilidade no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="48b6a-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48b6a-138">Testar sua implantação de mobilidade para clientes móveis do Lync 2013 usando os componentes Web do UCWA</span><span class="sxs-lookup"><span data-stu-id="48b6a-138">Test your mobility deployment for Lync 2013 Mobile clients using the UCWA Web components</span></span></p></td>
<td><p><span data-ttu-id="48b6a-139">Use o cmdlet <strong>Test-CsUcwaConference</strong> para testar e verificar se usuários predefinidos de teste ou um par de usuários reais podem usar o UCWA para criar e participar de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="48b6a-139">Use the <strong>Test-CsUcwaConference</strong> cmdlet to test and verify that pre-defined test users or a pair of actual users can use UCWA to create and participate in a conference.</span></span></p>
<p><span data-ttu-id="48b6a-140">Consulte a documentação do cmdlet do Shell de gerenciamento do Lync Server para <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">testar-CsUcwaConference</a> para obter uma lista completa de opções.</span><span class="sxs-lookup"><span data-stu-id="48b6a-140">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">Test-CsUcwaConference</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="48b6a-141">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="48b6a-141">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="48b6a-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verificando sua implantação de mobilidade no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="48b6a-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48b6a-143">Configurar para notificações por push</span><span class="sxs-lookup"><span data-stu-id="48b6a-143">Configure for push notifications</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="48b6a-144">Para servidores de borda do Lync Server 2013, adicione um provedor de hospedagem online do Lync Server e configure a Federação do provedor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="48b6a-144">For Lync Server 2013 Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-145">Para servidores de borda do Lync Server 2010, adicione um provedor de hospedagem online do Lync Server e configure a Federação do provedor de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="48b6a-145">For Lync Server 2010  Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-146">Para servidores do Office Communications Server 2007 R2 Edge, adicione um parceiro federado.</span><span class="sxs-lookup"><span data-stu-id="48b6a-146">For Office Communications Server 2007 R2 Edge Servers, add a federated partner.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-147">Se você quiser dar suporte a notificações por push em uma rede Wi-Fi, configure uma regra de firewall de saída para a porta TCP 5223.</span><span class="sxs-lookup"><span data-stu-id="48b6a-147">If you want to support push notifications over a Wi-Fi network, configure a firewall rule outbound for TCP port 5223.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-148">Use o cmdlet <strong>set-CsPushNotificationConfiguration</strong> para habilitar as notificações por push para o serviço de notificação por push do Apple (APNS) e o serviço de notificação por push da Microsoft (MPNS).</span><span class="sxs-lookup"><span data-stu-id="48b6a-148">Use the <strong>Set-CsPushNotificationConfiguration</strong> cmdlet to enable push notifications to the Apple Push Notification Service (APNS) and Microsoft Push Notification Service (MPNS).</span></span> <span data-ttu-id="48b6a-149">Esse recurso está desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="48b6a-149">This feature is disabled by default.</span></span></p></li>
<li><p><span data-ttu-id="48b6a-150">Use o cmdlet <strong>Test-CsFederatedPartner</strong> para testar a configuração de Federação e o cmdlet <strong>Test-CsMCXPushNotification</strong> para testar as notificações por push.</span><span class="sxs-lookup"><span data-stu-id="48b6a-150">Use the <strong>Test-CsFederatedPartner</strong> cmdlet to test the federation configuration and the <strong>Test-CsMCXPushNotification</strong> cmdlet to test push notifications.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="48b6a-151">As notificações por push são usadas para clientes móveis do Lync 2010 em dispositivos Apple e Windows Phone</span><span class="sxs-lookup"><span data-stu-id="48b6a-151">Push notifications are used for Lync 2010 Mobile clients on Apple devices and Windows Phone</span></span><BR><span data-ttu-id="48b6a-152">A notificação por push é necessária para clientes móveis do Lync 2013 somente no Windows Phone</span><span class="sxs-lookup"><span data-stu-id="48b6a-152">Push notification is required for Lync 2013 Mobile clients on Windows Phone only</span></span>


</div></li>
</ul></td>
<td><p><span data-ttu-id="48b6a-153">RtcUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="48b6a-153">RtcUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="48b6a-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Configurando notificações por push no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="48b6a-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Configuring for push notifications in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48b6a-155">Configurar a política de mobilidade</span><span class="sxs-lookup"><span data-stu-id="48b6a-155">Configure mobility policy</span></span></p></td>
<td><p><span data-ttu-id="48b6a-156">Use o cmdlet <strong>set-CsMobilityPolicy</strong> para permitir ou proibir:</span><span class="sxs-lookup"><span data-stu-id="48b6a-156">Use the <strong>Set-CsMobilityPolicy</strong> cmdlet to allow or disallow:</span></span></p>
<ul>
<li><p><span data-ttu-id="48b6a-157">Chamada via Trabalho</span><span class="sxs-lookup"><span data-stu-id="48b6a-157">Call via Work</span></span></p></li>
<li><p><span data-ttu-id="48b6a-158">Habilitar áudio IP e vídeo IP</span><span class="sxs-lookup"><span data-stu-id="48b6a-158">Enable IP Audio and IP Video</span></span></p></li>
<li><p><span data-ttu-id="48b6a-159">Exigir WiFi para áudio IP e/ou vídeo IP</span><span class="sxs-lookup"><span data-stu-id="48b6a-159">Require WiFi for IP Audio and/or IP Video</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="48b6a-160">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="48b6a-160">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="48b6a-161"><a href="lync-server-2013-configuring-mobility-policy.md">Configurando a política de mobilidade no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="48b6a-161"><a href="lync-server-2013-configuring-mobility-policy.md">Configuring mobility policy in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="48b6a-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48b6a-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

