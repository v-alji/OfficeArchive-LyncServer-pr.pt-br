---
title: 'Lync Server 2013: Configurando o proxy reverso para mobilidade'
description: 'Lync Server 2013: Configurando o proxy reverso para mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the reverse proxy for mobility
ms:assetid: 3f4a9e33-77e4-4c18-a73f-24d4bec8ea9c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690011(v=OCS.15)
ms:contentKeyID: 48183946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b4e1a71f97bc1737299d54cc0f4c56f0f5981bef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432482"
---
# <a name="configuring-the-reverse-proxy-for-mobility-in-lync-server-2013"></a><span data-ttu-id="af21c-103">Configurando o proxy reverso para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af21c-103">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af21c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af21c-104">

<span> </span></span></span>

<span data-ttu-id="af21c-105">_**Tópico da última modificação:** 2014-03-20_</span><span class="sxs-lookup"><span data-stu-id="af21c-105">_**Topic Last Modified:** 2014-03-20_</span></span>

<span data-ttu-id="af21c-106">Se quiser usar a descoberta automática para clientes de dispositivos móveis, você precisará modificar uma nova regra de publicação na Web para o proxy reverso se você atualizou ou não as listas de nomes alternativos de entidades nos certificados de proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="af21c-106">If you want to use automatic discovery for mobile device clients, you need to modify an existing or create a new web publishing rule for the reverse proxy whether or not you update the subject alternative name lists on the reverse proxy certificates.</span></span>

<span data-ttu-id="af21c-107">Se você decidir usar HTTPS para solicitações iniciais de serviço de descoberta automática do Lync Server 2013 e atualizar as listas de nomes alternativos de entidades nos certificados de proxy reverso, será necessário atribuir o certificado público atualizado ao ouvinte SSL (Secure Sockets Layer) no seu proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="af21c-107">If you decide to use HTTPS for initial Lync Server 2013 Autodiscover Service requests and update the subject alternative names lists on the reverse proxy certificates, you need to assign the updated public certificate to the Secure Sockets Layer (SSL) Listener on your reverse proxy.</span></span> <span data-ttu-id="af21c-108">Para obter detalhes sobre as entradas de nomes alternativos de entidades necessárias, consulte [requisitos técnicos de mobilidade no Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="af21c-108">For details about the required subject alternative name entries, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span> <span data-ttu-id="af21c-109">Em seguida, você precisará modificar o ouvinte existente para os serviços Web externos ou criar uma nova regra de publicação na Web para a URL externa do serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="af21c-109">You then need to modify the existing listener for the external web services or create a new web publishing rule for the external Autodiscover Service URL.</span></span> <span data-ttu-id="af21c-110">Se você ainda não tiver uma regra de publicação na Web para a URL externa de serviços Web do Lync Server 2013 para seu pool de front-ends, também precisará publicar uma regra para isso.</span><span class="sxs-lookup"><span data-stu-id="af21c-110">If you do not already have a web publishing rule for the external Lync Server 2013 Web Services URL for your Front End pool, you also need to publish a rule for that.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="af21c-111">A regra de publicação de proxy reverso e a escuta podem atender tanto os serviços Web externos quanto o serviço de descoberta automática, desde que o certificado atribuído ao ouvinte contenha o nome da entidade e os nomes alternativos de assunto necessários para ambos.</span><span class="sxs-lookup"><span data-stu-id="af21c-111">The reverse proxy publishing rule and listener can service both the external web services and the Autodiscover Service, as long as the certificate assigned to the listener contains the necessary subject name and subject alternative names for both.</span></span> <span data-ttu-id="af21c-112">Para obter detalhes sobre a configuração padrão do ouvinte da Web e da regra de publicação, consulte <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Configurando servidores proxy reverso para o Lync Server 2013</A> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="af21c-112">For details on the default configuration of the web listener and publishing rule, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A> for more details.</span></span>



</div>

<span data-ttu-id="af21c-113">Se você decidir usar HTTP para solicitações de serviço de descoberta automática iniciais para que você não precise atualizar nomes alternativos de entidades para o proxy reverso, será necessário criar ou modificar uma regra de publicação na Web para a porta 80.</span><span class="sxs-lookup"><span data-stu-id="af21c-113">If you decide to use HTTP for initial Autodiscover Service requests so that you do not need to update subject alternative names for the reverse proxy, you need to create or modify a web publishing rule for port 80.</span></span>

<span data-ttu-id="af21c-114">Os procedimentos desta seção descrevem como criar ou modificar as regras de publicação na Web no Microsoft Forefront Threat Management Gateway 2010 para descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="af21c-114">The procedures in this section describe how to create or modify the web publishing rules in Microsoft Forefront Threat Management Gateway 2010 for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="af21c-115">Esses procedimentos pressupõem que você tenha instalado a edição padrão do Forefront Threat Management Gateway (TMG) 2010.</span><span class="sxs-lookup"><span data-stu-id="af21c-115">These procedures assume that you have installed the Standard Edition of Forefront Threat Management Gateway (TMG) 2010.</span></span> <span data-ttu-id="af21c-116">Se você estiver usando outro proxy reverso, os procedimentos serão similares, mas precisarão ser mapeados para a documentação do produto de terceiros.</span><span class="sxs-lookup"><span data-stu-id="af21c-116">If you are using another reverse proxy, the procedures are similar, but will need to be mapped to the documentation for the third-party product.</span></span>



</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-the-external-autodiscover-url"></a><span data-ttu-id="af21c-117">Para criar uma regra de publicação na Web para a URL de descoberta automática externa</span><span class="sxs-lookup"><span data-stu-id="af21c-117">To create a web publishing rule for the external Autodiscover URL</span></span>

1.  <span data-ttu-id="af21c-118">Clique em **Iniciar**, aponte para **programas**, aponte para **Microsoft Forefront TMG** e clique em **Gerenciamento do Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="af21c-118">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="af21c-119">No painel esquerdo, expanda **ServerName**, clique com o botão direito do mouse em **política de firewall**, aponte para **novo** e clique em regra de **publicação de site da Web**.</span><span class="sxs-lookup"><span data-stu-id="af21c-119">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="af21c-120">Na página **Bem-vindo à nova regra de publicação na Web** , digite um nome para exibição para a nova regra de publicação (por exemplo, LyncDiscoveryURL).</span><span class="sxs-lookup"><span data-stu-id="af21c-120">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, LyncDiscoveryURL).</span></span>

4.  <span data-ttu-id="af21c-121">Na página **Selecionar ação da regra** , selecione **permitir**.</span><span class="sxs-lookup"><span data-stu-id="af21c-121">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="af21c-122">Na página **tipo de publicação** , selecione **publicar um único site da Web ou um balanceador de carga**.</span><span class="sxs-lookup"><span data-stu-id="af21c-122">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="af21c-123">Na página **segurança de conexão do servidor** , selecione **usar SSL para se conectar ao servidor Web ou ao farm de servidores publicado**.</span><span class="sxs-lookup"><span data-stu-id="af21c-123">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="af21c-124">Na página **detalhes da publicação interna** , em **nome do site interno**, digite o nome de domínio totalmente qualificado (FQDN) do seu pool de diretor (por exemplo, lyncdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="af21c-124">On the **Internal Publishing Details** page, in **Internal Site name**, type the fully qualified domain name (FQDN) of your Director pool (for example, lyncdir01.contoso.local).</span></span> <span data-ttu-id="af21c-125">Se você estiver criando uma regra para a URL de serviços Web externos no pool de front-ends, digite o endereço VIP do balanceador de carga de hardware (HLB) na frente do pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="af21c-125">If you are creating a rule for the external Web Services URL on the Front End pool, type the VIP address of the Hardware Load Balancer (HLB) in front of the Front End pool.</span></span>

8.  <span data-ttu-id="af21c-126">Na página **detalhes da publicação interna** , em **caminho (opcional)**, digite **/ \* *_ como o caminho da pasta a ser publicada e, em seguida, selecione _* encaminhar o cabeçalho original do host**.</span><span class="sxs-lookup"><span data-stu-id="af21c-126">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header\*\*.</span></span>

9.  <span data-ttu-id="af21c-127">Na página de **detalhes do nome público** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="af21c-127">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="af21c-128">Em **aceitar solicitações por**, selecione **este nome de domínio**.</span><span class="sxs-lookup"><span data-stu-id="af21c-128">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="af21c-129">Em **nome público**, digite **lyncdiscover.**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="af21c-129">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="af21c-130">(a URL do serviço de descoberta automática externa).</span><span class="sxs-lookup"><span data-stu-id="af21c-130">(the external Autodiscover Service URL).</span></span> <span data-ttu-id="af21c-131">Se você estiver criando uma regra para a URL de serviços Web externos no pool de front-ends, digite o FQDN dos serviços Web externos em seu pool de front-ends (por exemplo, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="af21c-131">If you are creating a rule for the external Web Services URL on the Front End pool, type the FQDN for the external Web Services on your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>
    
      - <span data-ttu-id="af21c-132">Em **caminho**, digite \* */\** _.</span><span class="sxs-lookup"><span data-stu-id="af21c-132">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="af21c-133">Na página _ \*selecionar Web listener\*\*, no **ouvinte da Web**, selecione seu ouvinte SSL existente com o certificado público atualizado.</span><span class="sxs-lookup"><span data-stu-id="af21c-133">On _ *Select Web Listener*\* page, in **Web Listener**, select your existing SSL Listener with the updated public certificate.</span></span>

11. <span data-ttu-id="af21c-134">Na página **delegação de autenticação** , selecione **sem delegação, mas o cliente pode autenticar diretamente**.</span><span class="sxs-lookup"><span data-stu-id="af21c-134">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly**.</span></span>

12. <span data-ttu-id="af21c-135">Na página **conjunto de usuários** , selecione **todos os usuários**.</span><span class="sxs-lookup"><span data-stu-id="af21c-135">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="af21c-136">Na página **concluindo o assistente de nova regra de publicação na Web** , verifique se as configurações da regra de publicação da Web estão corretas e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="af21c-136">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="af21c-137">Na lista do Forefront TMG de regras de publicação na Web, clique duas vezes na nova regra que você acabou de adicionar para abrir **as propriedades**.</span><span class="sxs-lookup"><span data-stu-id="af21c-137">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="af21c-138">Na guia **para** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="af21c-138">On the **To** tab, do the following:</span></span>
    
      - <span data-ttu-id="af21c-139">Selecione **encaminhar o cabeçalho original do host em vez do verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="af21c-139">Select **Forward the original host header instead of the actual one**.</span></span>
    
      - <span data-ttu-id="af21c-140">**As solicitações selecionadas parecem vir do computador com o FOREFRONT TMG**.</span><span class="sxs-lookup"><span data-stu-id="af21c-140">Select **Requests appear to come from the Forefront TMG computer**.</span></span>

16. <span data-ttu-id="af21c-141">Na guia **ponte** , configure o seguinte:</span><span class="sxs-lookup"><span data-stu-id="af21c-141">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="af21c-142">Selecione **servidor Web**.</span><span class="sxs-lookup"><span data-stu-id="af21c-142">Select **Web server**.</span></span>
    
      - <span data-ttu-id="af21c-143">Selecione **redirecionar solicitações para porta http** e digite **8080** para o número da porta.</span><span class="sxs-lookup"><span data-stu-id="af21c-143">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="af21c-144">Selecione **redirecionar solicitações para porta SSL** e digite **4443** para o número da porta.</span><span class="sxs-lookup"><span data-stu-id="af21c-144">Select **Redirect requests to SSL port**, and type **4443** for the port number.</span></span>

17. <span data-ttu-id="af21c-145">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="af21c-145">Click **OK**.</span></span>

18. <span data-ttu-id="af21c-146">Clique em **aplicar** no painel detalhes para salvar as alterações e atualizar a configuração.</span><span class="sxs-lookup"><span data-stu-id="af21c-146">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

19. <span data-ttu-id="af21c-147">Clique em **testar regra** para verificar se a nova regra está configurada corretamente.</span><span class="sxs-lookup"><span data-stu-id="af21c-147">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-modify-an-existing-web-publishing-rule-to-add-the-external-autodiscover-san-and-url"></a><span data-ttu-id="af21c-148">Para modificar uma regra de publicação da Web existente para adicionar a SAN e a URL de descoberta automática externa</span><span class="sxs-lookup"><span data-stu-id="af21c-148">To modify an existing web publishing rule to add the external Autodiscover SAN and URL</span></span>

1.  <span data-ttu-id="af21c-149">Clique em **Iniciar**, aponte para **programas**, aponte para **Microsoft Forefront TMG** e clique em **Gerenciamento do Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="af21c-149">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="af21c-150">Você irá repetir a modificação para cada regra de publicação e ouvinte que você tiver.</span><span class="sxs-lookup"><span data-stu-id="af21c-150">You will repeat the modification for each publishing rule and listener that you have.</span></span> <span data-ttu-id="af21c-151">Geralmente, isso será uma regra e um ouvinte para os pools de front-end e um para os directors opcionais ou os pools de directors, se você os tiver implantado.</span><span class="sxs-lookup"><span data-stu-id="af21c-151">Typically, this will be one rule and listener for the Front End pools and one for the optional Directors or Director pools, if you have deployed them.</span></span>

    
    </div>

2.  <span data-ttu-id="af21c-152">No painel esquerdo, expanda **ServerName**, clique com o botão direito do mouse em **política de firewall**, clique na regra aplicável.</span><span class="sxs-lookup"><span data-stu-id="af21c-152">In the left pane, expand **ServerName**, right-click **Firewall Policy**, click the applicable rule.</span></span> <span data-ttu-id="af21c-153">Na guia **tarefas** , clique em **Editar regra selecionada**.</span><span class="sxs-lookup"><span data-stu-id="af21c-153">On the **Tasks** tab, click **Edit Selected rule**.</span></span>

3.  <span data-ttu-id="af21c-154">Na guia **nome público** , nesta **regra aplica-se a**, selecione **solicitações para os seguintes sites da Web**.</span><span class="sxs-lookup"><span data-stu-id="af21c-154">On the **Public Name** tab, in **This rule applies to**, select **Requests for the following Web sites**.</span></span>

4.  <span data-ttu-id="af21c-155">Clique em **Adicionar**, digite o nome do novo site de descoberta automática (por exemplo, "lyncdiscover.contoso.com") e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="af21c-155">Click **Add**, type the name of the new Autodiscover site (for example, “lyncdiscover.contoso.com”), and then click **OK**.</span></span>

5.  <span data-ttu-id="af21c-156">Na guia **ouvinte** , clique em **Selecionar certificado** e atribua o novo certificado às entradas adicionadas de San de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="af21c-156">On the **Listener** tab, click **Select Certificate** and assign the new certificate with the added Autodiscover SAN entries.</span></span> <span data-ttu-id="af21c-157">Feche as propriedades do ouvinte e publicação na Web.</span><span class="sxs-lookup"><span data-stu-id="af21c-157">Close the Listener and Web Publishing properties.</span></span>

6.  <span data-ttu-id="af21c-158">Clique em **aplicar** no painel detalhes para salvar as alterações e atualizar a configuração.</span><span class="sxs-lookup"><span data-stu-id="af21c-158">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

7.  <span data-ttu-id="af21c-159">Clique em **testar regra** para verificar se a nova regra está configurada corretamente.</span><span class="sxs-lookup"><span data-stu-id="af21c-159">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-port-80"></a><span data-ttu-id="af21c-160">Para criar uma regra de publicação na Web para a porta 80</span><span class="sxs-lookup"><span data-stu-id="af21c-160">To create a web publishing rule for port 80</span></span>

1.  <span data-ttu-id="af21c-161">Clique em **Iniciar**, aponte para **programas**, aponte para **Microsoft Forefront TMG** e clique em **Gerenciamento do Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="af21c-161">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="af21c-162">No painel esquerdo, expanda **ServerName**, clique com o botão direito do mouse em **política de firewall**, aponte para **novo** e clique em regra de **publicação de site da Web**.</span><span class="sxs-lookup"><span data-stu-id="af21c-162">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="af21c-163">Na página **Bem-vindo à nova regra de publicação na Web** , digite um nome para exibição para a nova regra de publicação (por exemplo, descoberta automática do LYNC (http)).</span><span class="sxs-lookup"><span data-stu-id="af21c-163">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, Lync Autodiscover (HTTP)).</span></span>

4.  <span data-ttu-id="af21c-164">Na página **Selecionar ação da regra** , selecione **permitir**.</span><span class="sxs-lookup"><span data-stu-id="af21c-164">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="af21c-165">Na página **tipo de publicação** , selecione **publicar um único site da Web ou um balanceador de carga**.</span><span class="sxs-lookup"><span data-stu-id="af21c-165">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="af21c-166">Na página **segurança de conexão do servidor** , selecione **usar conexões não seguras para se conectar ao servidor Web ou ao farm de servidores publicado**.</span><span class="sxs-lookup"><span data-stu-id="af21c-166">On the **Server Connection Security** page, select **Use non-secured connections to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="af21c-167">Na página **detalhes da publicação interna** , em **nome do site interno**, digite o endereço VIP do balanceador de carga de hardware (HLB) na frente do pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="af21c-167">On the **Internal Publishing Details** page, in **Internal Site name**, type the VIP address of the Hardware Load Balancer (HLB) in front of the Front End pool.</span></span>

8.  <span data-ttu-id="af21c-168">Na página **detalhes da publicação interna** , em **caminho (opcional)**, digite **/ \* *_ como o caminho da pasta a ser publicada e, em seguida, selecione _* encaminhar o cabeçalho do host original em vez do especificado no campo nome do site interno**.</span><span class="sxs-lookup"><span data-stu-id="af21c-168">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header instead of the one specified in the Internal site name field\*\*.</span></span>

9.  <span data-ttu-id="af21c-169">Na página de **detalhes do nome público** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="af21c-169">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="af21c-170">Em **aceitar solicitações por**, selecione **este nome de domínio**.</span><span class="sxs-lookup"><span data-stu-id="af21c-170">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="af21c-171">Em **nome público**, digite **lyncdiscover.**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="af21c-171">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="af21c-172">(a URL do serviço de descoberta automática externa).</span><span class="sxs-lookup"><span data-stu-id="af21c-172">(the external Autodiscover Service URL).</span></span>
    
      - <span data-ttu-id="af21c-173">Em **caminho**, digite \* */\** _.</span><span class="sxs-lookup"><span data-stu-id="af21c-173">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="af21c-174">Na página _ \*selecionar Web listener\*\*, no **ouvinte da Web**, selecione um ouvinte da Web ou use o assistente de definição de Web listener novo para criar um novo.</span><span class="sxs-lookup"><span data-stu-id="af21c-174">On _ *Select Web Listener*\* page, in **Web Listener**, select a Web Listener or use the New Web Listener Definition Wizard to create a new one.</span></span>

11. <span data-ttu-id="af21c-175">Na página **delegação de autenticação** , selecione **sem delegação e o cliente não pode autenticar diretamente**.</span><span class="sxs-lookup"><span data-stu-id="af21c-175">On the **Authentication Delegation** page, select **No delegation, and client cannot authenticate directly**.</span></span>

12. <span data-ttu-id="af21c-176">Na página **conjunto de usuários** , selecione **todos os usuários**.</span><span class="sxs-lookup"><span data-stu-id="af21c-176">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="af21c-177">Na página **concluindo o assistente de nova regra de publicação na Web** , verifique se as configurações da regra de publicação da Web estão corretas e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="af21c-177">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="af21c-178">Na lista do Forefront TMG de regras de publicação na Web, clique duas vezes na nova regra que você acabou de adicionar para abrir **as propriedades**.</span><span class="sxs-lookup"><span data-stu-id="af21c-178">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="af21c-179">Na guia **ponte** , configure o seguinte:</span><span class="sxs-lookup"><span data-stu-id="af21c-179">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="af21c-180">Selecione **servidor Web**.</span><span class="sxs-lookup"><span data-stu-id="af21c-180">Select **Web server**.</span></span>
    
      - <span data-ttu-id="af21c-181">Selecione **redirecionar solicitações para porta http** e digite **8080** para o número da porta.</span><span class="sxs-lookup"><span data-stu-id="af21c-181">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="af21c-182">Verifique se **a seleção redirecionar solicitações para a porta SSL** não está selecionada.</span><span class="sxs-lookup"><span data-stu-id="af21c-182">Verify that **Redirect requests to SSL port** is not selected.</span></span>

16. <span data-ttu-id="af21c-183">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="af21c-183">Click **OK**.</span></span>

17. <span data-ttu-id="af21c-184">Clique em **aplicar** no painel detalhes para salvar as alterações e atualizar a configuração.</span><span class="sxs-lookup"><span data-stu-id="af21c-184">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

18. <span data-ttu-id="af21c-185">Clique em **testar regra** para verificar se a nova regra está configurada corretamente.</span><span class="sxs-lookup"><span data-stu-id="af21c-185">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

19. <span data-ttu-id="af21c-186">Verifique se a URL do serviço de descoberta automática externa não está definida em nenhuma outra regra de publicação na Web.</span><span class="sxs-lookup"><span data-stu-id="af21c-186">Verify that the external Autodiscover Service URL is not defined on any other web publishing rule.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="af21c-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="af21c-187">See Also</span></span>


[<span data-ttu-id="af21c-188">Configurando servidores de proxy reverso para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af21c-188">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)  
[<span data-ttu-id="af21c-189">Requisitos técnicos para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af21c-189">Technical requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-mobility.md)  
  

<span data-ttu-id="af21c-190"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af21c-190"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

