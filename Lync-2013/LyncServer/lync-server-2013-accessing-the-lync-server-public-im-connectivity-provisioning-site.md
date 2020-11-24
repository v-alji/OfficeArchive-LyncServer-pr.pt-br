---
title: Acessando o site de configuração de conectividade a redes públicas de mensagens instantâneas do Lync Server
description: Acessando o site de configuração de conectividade de IM pública do Lync Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Accessing the Lync Server public IM connectivity provisioning site
ms:assetid: 77a08234-6bcf-4f59-b43b-ee5fc1926585
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440174(v=OCS.15)
ms:contentKeyID: 57793364
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e12916b12de1ef3a3f990c6bee54c312ba6c1992
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389739"
---
# <a name="accessing-the-lync-server-public-im-connectivity-provisioning-site-from-lync-server-2013"></a><span data-ttu-id="c2792-103">Acessando o site de configuração de conectividade a redes públicas de mensagens instantâneas do Lync Server a partir do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2792-103">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2792-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2792-104">

<span> </span></span></span>

<span data-ttu-id="c2792-105">_**Tópico da última modificação:** 2019-03-22_</span><span class="sxs-lookup"><span data-stu-id="c2792-105">_**Topic Last Modified:** 2019-03-22_</span></span>

<span data-ttu-id="c2792-106">O processo de configuração para a conectividade do Lync-Skype mudou, em comparação com os métodos de provisionamento da PIC anteriores.</span><span class="sxs-lookup"><span data-stu-id="c2792-106">The provisioning process for Lync-Skype connectivity has changed, as compared to previous PIC provisioning methods.</span></span> <span data-ttu-id="c2792-107">Este processo de provisionamento pode levar até trinta dias para ser concluído.</span><span class="sxs-lookup"><span data-stu-id="c2792-107">This provisioning process can take up to thirty days to complete.</span></span> <span data-ttu-id="c2792-108">Recomendamos que você inicie esse processo primeiro, antes de realizar as demais etapas descritas neste documento.</span><span class="sxs-lookup"><span data-stu-id="c2792-108">We recommend that you start this process first, prior to completing the remaining steps in this document.</span></span> <span data-ttu-id="c2792-109">Depois que o processo de provisionamento do Lync-Skype for concluído para a sua conta, a conta será ativada e seus usuários qualificados serão habilitados para conectividade de mensagens de chat públicas.</span><span class="sxs-lookup"><span data-stu-id="c2792-109">After the Lync-Skype provisioning process is completed for your account, the account is activated and your eligible users are enabled for public IM connectivity.</span></span>

### <a name="to-provision-lync-skype-connectivity-you-need-the-following-information"></a><span data-ttu-id="c2792-110">Para configurar a conectividade do Lync-Skype, você precisa das seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="c2792-110">To provision Lync-Skype connectivity, you need the following information:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="c2792-111">Número do contrato da Microsoft</span><span class="sxs-lookup"><span data-stu-id="c2792-111">Microsoft Agreement Number</span></span></p></li>
<li><p><span data-ttu-id="c2792-112">Nome de domínio totalmente qualificado (FQDN) do serviço de Borda de Acesso</span><span class="sxs-lookup"><span data-stu-id="c2792-112">Access Edge service fully qualified domain name (FQDN)</span></span></p></li>
<li><p><span data-ttu-id="c2792-113">Domínios do protocolo SIP</span><span class="sxs-lookup"><span data-stu-id="c2792-113">Session Initiation Protocol (SIP) domain(s)</span></span></p></li>
<li><p><span data-ttu-id="c2792-114">Qualquer FQDN adicional do serviço de Borda de Acesso</span><span class="sxs-lookup"><span data-stu-id="c2792-114">Any additional Access Edge service FQDNs</span></span></p></li>
<li><p><span data-ttu-id="c2792-115">Informações de contato</span><span class="sxs-lookup"><span data-stu-id="c2792-115">Contact information</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2792-116">A partir de abril de 2019, interromperemos a coleta e a retenção de informações de contato para clientes provisionados para o Skype Federation pelo website da pic.lync.com.</span><span class="sxs-lookup"><span data-stu-id="c2792-116">Beginning in April 2019, we will stop the collection and retention of contact information for customers who are provisioned for Skype Federation via the pic.lync.com website.</span></span> <span data-ttu-id="c2792-117">Essa alteração está sendo feita para garantir que o sistema de provisionamento do pic.lync.com respeite as políticas de privacidade da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2792-117">This change is being made to ensure that the pic.lync.com provisioning system adheres to Microsoft privacy policies.</span></span> 

<span data-ttu-id="c2792-118">Depois que essa alteração ficar em tempo real, não poderemos mais fornecer atualizações de email em alterações de provisionamento pendentes.</span><span class="sxs-lookup"><span data-stu-id="c2792-118">Once this change goes live, we will no longer be able to provide email updates on pending provisioning changes.</span></span> <span data-ttu-id="c2792-119">As alterações de provisionamento de PIC geralmente são concluídas dentro de 24-48 horas após serem inseridas.</span><span class="sxs-lookup"><span data-stu-id="c2792-119">PIC provisioning changes typically complete within 24-48 hours after being entered.</span></span> <span data-ttu-id="c2792-120">Se você ainda tiver problemas com a Federação do Skype 48 horas após o envio de uma solicitação de provisionamento, entre em contato com o suporte técnico da Microsoft para investigar ainda mais.</span><span class="sxs-lookup"><span data-stu-id="c2792-120">If you are still experiencing Skype Federation issues 48 hours after submitting a provisioning request, please engage Microsoft Technical Support to investigate further.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2792-121">Como parte dessa mudança, todas as informações de contato inseridas anteriormente serão removidas do nosso sistema até o final de abril de 2019.</span><span class="sxs-lookup"><span data-stu-id="c2792-121">As part of this change, all previously entered contact information will be purged from our system by the end of April, 2019.</span></span>

### <a name="to-initiate-the-provisioning-process-for-lync-skype-connectivity"></a><span data-ttu-id="c2792-122">Para iniciar o processo de provisionamento para Lync-Skype conectividade:</span><span class="sxs-lookup"><span data-stu-id="c2792-122">To initiate the provisioning process for Lync-Skype connectivity:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="c2792-123">Entre no site, <strong>https://pic.lync.com</strong> usando o Microsoft Windows Live ID.</span><span class="sxs-lookup"><span data-stu-id="c2792-123">Sign in to the website, <strong>https://pic.lync.com</strong>, using your Microsoft Windows Live ID.</span></span></p></li>
<li><p><span data-ttu-id="c2792-124">Selecione o tipo de contrato de licenciamento da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2792-124">Select the Microsoft licensing agreement type.</span></span></p></li>
<li><p><span data-ttu-id="c2792-125">Marque a caixa de seleção, verificando se você leu e aceitou os direitos de uso do produto do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c2792-125">Select the check box, verifying that you have read and accept the Product Use Rights for Lync Server.</span></span></p></li>
<li><p><span data-ttu-id="c2792-126">Na página <strong>iniciar uma solicitação de provisionamento</strong> , clique no link apropriado para iniciar uma solicitação de provisionamento:</span><span class="sxs-lookup"><span data-stu-id="c2792-126">On the <strong>Initiate a Provisioning Request</strong> page, click the appropriate link to initiate a provisioning request:</span></span></p></li>
<li><p><span data-ttu-id="c2792-127">Na página <strong>especificar informações de provisionamento</strong> , insira o FQDN do <strong>serviço de borda de acesso</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2792-127">On the <strong>Specify Provisioning Information</strong> page, enter the <strong>Access Edge service FQDN</strong>.</span></span> <span data-ttu-id="c2792-128">Por exemplo, <strong>SIP.contoso.com</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2792-128">For example, <strong>sip.contoso.com</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="c2792-129">Após 1º de julho de 2017 a Microsoft exigirá que os clientes tenham o registro SRV DNS de Federação implantado para conectividade de IM pública para continuar a funcionar.</span><span class="sxs-lookup"><span data-stu-id="c2792-129">After July 1st, 2017 Microsoft will additionally require customers have the Federation DNS SRV record deployed for Public IM connectivity to continue to work.</span></span>

</li>
<li><p><span data-ttu-id="c2792-130">Digite pelo menos um ou mais nomes de domínio SIP e, em seguida, clique em <strong>Adicionar</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2792-130">Enter at least one or more SIP domain names, and then click <strong>Add</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="c2792-131">Pelo menos um servidor de borda de acesso e um domínio SIP são necessários para concluir o processo de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="c2792-131">At least one Access Edge server and one SIP domain are required to complete the provisioning process.</span></span> <span data-ttu-id="c2792-132">O domínio SIP e o servidor de Borda de Acesso devem estar ativos, em funcionamento e acessíveis na rede.</span><span class="sxs-lookup"><span data-stu-id="c2792-132">The SIP domain and the Access Edge server must be active, functioning, and reachable on the network.</span></span>

</li>
<li><p><span data-ttu-id="c2792-133">Na lista de <strong>provedores de serviços públicos de mensagens instantâneas</strong>, selecione <strong>Skype</strong> e clique em <strong>Avançar</strong> para adicionar informações de contato e enviar a solicitação de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="c2792-133">In the list of <strong>Public IM Service providers</strong>, select <strong>Skype,</strong> and click <strong>Next</strong> to add contact information, and submit the provisioning request.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c2792-134">Após o envio da solicitação de provisionamento, pode levar até 30 dias para que a conta seja ativada e para que os usuários sejam habilitados para conectividade de IM pública.</span><span class="sxs-lookup"><span data-stu-id="c2792-134">After the provisioning request has been submitted, it can take up to 30 days for the account to activate and for users to be enabled for public IM connectivity.</span></span>

<div>

## <a name="enabling-federation-and-public-im-connectivity-pic"></a><span data-ttu-id="c2792-135">Habilitando a federação e a PIC</span><span class="sxs-lookup"><span data-stu-id="c2792-135">Enabling Federation and Public IM Connectivity (PIC)</span></span>

<span data-ttu-id="c2792-136">Depois de enviar a solicitação de provisionamento, você pode se concentrar no ambiente do Lync Server e nas tarefas administrativas necessárias para configurar a conectividade do Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="c2792-136">After you have submitted the provisioning request, you can focus on the Lync Server environment and administrative tasks required to configure Lync-Skype connectivity.</span></span> <span data-ttu-id="c2792-137">Nesta seção, presumimos que o administrador do Lync Server implantou o Lync Server e configurou o acesso externo.</span><span class="sxs-lookup"><span data-stu-id="c2792-137">In this section, we assume that the Lync Server administrator has deployed Lync Server and configured external access.</span></span> <span data-ttu-id="c2792-138">Para obter informações adicionais sobre como configurar o acesso externo para o Lync Server, consulte "planejando o acesso do usuário externo" em [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) e "Implantando o acesso ao usuário externo" em [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378) .</span><span class="sxs-lookup"><span data-stu-id="c2792-138">For additional information on configuring external access for Lync Server, see "Planning for External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) and "Deploying External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378).</span></span>

<span data-ttu-id="c2792-139">Para preparar o ambiente do Lync Server para Lync-Skype conectividade, o administrador do Lync Server deve completar as três tarefas a seguir:</span><span class="sxs-lookup"><span data-stu-id="c2792-139">To prepare the Lync Server environment for Lync-Skype connectivity, the Lync Server administrator must complete the following three tasks:</span></span>

<div>

## <a name="1-configure-federation-and-pic"></a><span data-ttu-id="c2792-140">1 \.</span><span class="sxs-lookup"><span data-stu-id="c2792-140">1\.</span></span> <span data-ttu-id="c2792-141">Configurar a federação e a PIC</span><span class="sxs-lookup"><span data-stu-id="c2792-141">Configure Federation and PIC</span></span>

<span data-ttu-id="c2792-142">A Federação é necessária para permitir que os usuários do Skype se comuniquem com usuários do Lync em sua organização.</span><span class="sxs-lookup"><span data-stu-id="c2792-142">Federation is required to enable Skype users to communicate with Lync users in your organization.</span></span> <span data-ttu-id="c2792-143">A PIC (conectividade de mensagens instantâneas) pública é uma classe de Federação e deve ser configurada para permitir que seus usuários do Lync se comuniquem com usuários do Skype.</span><span class="sxs-lookup"><span data-stu-id="c2792-143">Public Instant Messaging Connectivity (PIC) is a class of federation, and it must be configured to enable your Lync users to communicate with Skype users.</span></span> <span data-ttu-id="c2792-144">A Federação e a PIC são configuradas usando o painel de controle do Lync Server, mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="c2792-144">Federation and PIC are configured by using the Lync Server Control Panel, shown below.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="c2792-145">A federação de PIC não tem mais suporte no Live Communication Server 2005 SP1 e no Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="c2792-145">PIC federation is no longer supported by Live Communication Server 2005 SP1 or by Office Communications Server 2007.</span></span> <span data-ttu-id="c2792-146">As plataformas com suporte para a Federação PIC incluem o Lync Server 2013, o Lync Server 2010 e o Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c2792-146">The supported platforms for PIC federation include Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2.</span></span>



</div>

</div>

<div>

## <a name="2-configure-at-least-one-policy-to-support-federated-user-access"></a><span data-ttu-id="c2792-147">2 \.</span><span class="sxs-lookup"><span data-stu-id="c2792-147">2\.</span></span> <span data-ttu-id="c2792-148">Configurar pelo menos uma política para dar suporte ao acesso de usuários federados</span><span class="sxs-lookup"><span data-stu-id="c2792-148">Configure at least one policy to support federated user access</span></span>

<span data-ttu-id="c2792-149">Usando o painel de controle do Lync Server, um administrador deve configurar uma ou mais políticas de acesso externo do usuário para controlar se os usuários do Skype podem colaborar com usuários internos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c2792-149">Using the Lync Server Control Panel, an administrator must configure one or more external user access policies to control whether Skype users can collaborate with internal Lync Server users.</span></span>

</div>

<div>

## <a name="3-configure-the-skype-pic-provider-setting-for-lync"></a><span data-ttu-id="c2792-150">3 \.</span><span class="sxs-lookup"><span data-stu-id="c2792-150">3\.</span></span> <span data-ttu-id="c2792-151">Configurar a configuração do provedor de PIC da Skype para o Lync</span><span class="sxs-lookup"><span data-stu-id="c2792-151">Configure the Skype PIC provider setting for Lync</span></span>

<span data-ttu-id="c2792-152">Usando o Shell de gerenciamento do Lync Server, um administrador deve configurar a política de cliente do Lync para exibir o Skype como um provedor de PIC adicional.</span><span class="sxs-lookup"><span data-stu-id="c2792-152">Using the Lync Server Management Shell, an administrator must configure the Lync client policy to display Skype as an additional PIC provider.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="c2792-153">Os usuários dos provedores de serviços de PIC não podem participar em mensagens instantâneas ou conferências em sua organização até que você também configure pelo menos uma política (etapa 2, anteriormente neste procedimento) para dar suporte à conectividade a redes públicas de mensagens instantâneas. </span><span class="sxs-lookup"><span data-stu-id="c2792-153">Users of the Public Instant Messaging Connectivity (PIC) service providers can’t participate in IM or conferences in your organization until you also configure at least one policy (step 2, earlier in this procedure) to support public IM connectivity.</span></span><BR><span data-ttu-id="c2792-154">Para configurar a Federação e a PIC, consulte "habilitar ou desabilitar a Federação e conectividade de IM pública" em <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A> .</span><span class="sxs-lookup"><span data-stu-id="c2792-154">To configure federation and PIC, see "Enable or Disable Federation and Public IM Connectivity" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A>.</span></span><BR><span data-ttu-id="c2792-155">Para configurar pelo menos uma política para dar suporte ao acesso de usuário federado, consulte "configurar políticas para controlar o acesso ao usuário público" em <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A> .</span><span class="sxs-lookup"><span data-stu-id="c2792-155">To configure at least one policy to support federated user access, see "Configure Policies to Control Public User Access" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A>.</span></span>



</div>

1.  <span data-ttu-id="c2792-156">Em um servidor front-end do Lync Server, abra o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c2792-156">From a Lync Server Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="c2792-157">Execute estes dois comandos:</span><span class="sxs-lookup"><span data-stu-id="c2792-157">Run the following two commands:</span></span>
    
      - `Remove-CsPublicProvider -Identity <identity-name>`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="c2792-158">Se você ainda não tiver um provedor PIC em seu ambiente e estiver criando um novo provedor PIC, você não precisará executar o cmdlet <STRONG>Remove-CsPublicProvider</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c2792-158">If you do not already have a PIC provider in your environment and are creating a new PIC provider then you do not need to run the <STRONG>Remove-CsPublicProvider</STRONG> cmdlet.</span></span>

        
        </div>
    
      - `New-CsPublicProvider -ProxyFqdn federation.messenger.msn.com -Enabled 1 -Identity Skype  -VerificationLevel 2 -NameDecorationRoutingDomain msn.com -NameDecorationExcludedDomainList "msn.com,outlook.com,live.com,hotmail.com" -IconUrl "https://images.edge.messenger.live.com/Messenger_16x16.png"`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="c2792-159">Adicionado ao Lync Server 2013 CU5 &amp; o cliente de área de trabalho Lync no Office 2013 SP1, o NameDecorationRoutingDomain e o NameDecorationExcludedDomainList melhoram a situação em que os usuários do Lync adicionam contatos do Skype necessários para "decorar" domínios não-Microsoft para identificar e roteá-los para o Skype (o formato de: usuário (contoso. com) @msn. com).</span><span class="sxs-lookup"><span data-stu-id="c2792-159">Added in Lync Server 2013 CU5 &amp; Lync desktop client in Office 2013 SP1, the NameDecorationRoutingDomain and NameDecorationExcludedDomainList improve the situation where Lync users adding Skype contacts needed to “decorate” non-Microsoft domains to identify and route them to Skype (the format of: user(contoso.com)@msn.com).</span></span> <span data-ttu-id="c2792-160">Essas novas configurações permitem a formatação automática dos endereços que o usuário inserir na caixa de diálogo "Adicionar contato do Skype" com o NameDecorationRoutingDomain (que deve ser configurado como msn.com) se não contiver os domínios de NameDecorationExcludedDomainList (no momento, damos suporte a msn.com, live.com, Hotmail.com, outlook.com).</span><span class="sxs-lookup"><span data-stu-id="c2792-160">These new settings will allow automatic formatting of the address user’s enter in the “Add Skype contact” dialog box with the NameDecorationRoutingDomain (which should be set to msn.com) if it does not contain the domains in the NameDecorationExcludedDomainList (we currently can support msn.com, live.com, Hotmail.com, outlook.com).</span></span>

        
        </div>

3.  <span data-ttu-id="c2792-161">Em um cliente Lync, agora você pode selecionar Skype como o provedor de PIC e adicionar um cliente Skype especificando a conta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2792-161">From a Lync client, you can now select Skype as the PIC provider, and add a Skype client by specifying their Microsoft account.</span></span> <span data-ttu-id="c2792-162">Além disso, um usuário do Skype que mesclou e fez logon com a conta da Microsoft pode enviar solicitação de contato para os usuários do Lync.</span><span class="sxs-lookup"><span data-stu-id="c2792-162">In addition, a Skype user who has merged and logged in with their Microsoft account can send contact request to Lync users.</span></span> <span data-ttu-id="c2792-163">Para obter mais informações sobre contas da Microsoft, consulte [o que é uma conta da Microsoft?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span><span class="sxs-lookup"><span data-stu-id="c2792-163">For more information about Microsoft accounts, see [What is a Microsoft account?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span></span> <span data-ttu-id="c2792-164">Para obter informações adicionais sobre como adicionar clientes ao Lync, consulte [usando Lync-Skype conectividade no Lync Server 2013 como usuário final](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span><span class="sxs-lookup"><span data-stu-id="c2792-164">For additional information on adding clients to Lync, see [Using Lync-Skype connectivity in Lync Server 2013 as an end user](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span></span>

4.  <span data-ttu-id="c2792-165">Para obter informações detalhadas sobre como modificar provedores hospedados, consulte "criar ou editar provedores federados SIP hospedados" em [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065) .</span><span class="sxs-lookup"><span data-stu-id="c2792-165">For detailed information on modifying hosted providers, see "Create or Edit Hosted SIP Federated Providers" at [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065).</span></span>

<span data-ttu-id="c2792-166">Isso conclui as tarefas administrativas que devem ser executadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="c2792-166">This completes the administrative tasks that must be performed on the server.</span></span> <span data-ttu-id="c2792-167">Agora você está pronto para a conectividade do Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="c2792-167">You are now set up for Lync-Skype connectivity.</span></span>

</div>

</div>

<div>

## <a name="additional-resources"></a><span data-ttu-id="c2792-168">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="c2792-168">Additional Resources</span></span>

[<span data-ttu-id="c2792-169">Usando a conectividade Lync-Skype no Lync Server 2013 como usuário final</span><span class="sxs-lookup"><span data-stu-id="c2792-169">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

[<span data-ttu-id="c2792-170">Guia de configuração para conectividade Lync-Skype no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2792-170">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-provisioning-guide-for-lync-skype-connectivity.md)

<span data-ttu-id="c2792-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2792-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

