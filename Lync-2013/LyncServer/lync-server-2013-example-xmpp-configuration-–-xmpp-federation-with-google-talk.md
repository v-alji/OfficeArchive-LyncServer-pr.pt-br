---
title: Exemplo de configuração de XMPP – federação XMPP com Google Talk
description: Exemplo de configuração do XMPP – Federação do XMPP com o Google Talk.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428445"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a><span data-ttu-id="98723-103">Exemplo de configuração de XMPP no Lync Server 2013 – federação XMPP com Google Talk</span><span class="sxs-lookup"><span data-stu-id="98723-103">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98723-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98723-104">

<span> </span></span></span>

<span data-ttu-id="98723-105">_**Tópico da última modificação:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="98723-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="98723-106">Um exemplo de configuração para a implantação do proxy XMPP define uma federação com o Google Talk.</span><span class="sxs-lookup"><span data-stu-id="98723-106">An example configuration for deploying the XMPP Proxy defines a federation with Google Talk.</span></span>

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a><span data-ttu-id="98723-107">Exemplo de configuração de XMPP – federação XMPP com Google Talk</span><span class="sxs-lookup"><span data-stu-id="98723-107">Example XMPP configuration – XMPP federation with Google Talk</span></span>

1.  <span data-ttu-id="98723-108">No servidor front-end, abra o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="98723-108">On the Front End Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="98723-109">Clique em **instalar** ou **atualizar o Lync Server System** e, em seguida, clique em **Configurar** ou **remover componentes do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="98723-109">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="98723-110">Clique em **executar novamente**.</span><span class="sxs-lookup"><span data-stu-id="98723-110">Click **Run Again**.</span></span>

2.  <span data-ttu-id="98723-111">Em **configurar componentes do Lync Server**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="98723-111">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="98723-112">A tela Resumo mostrará as ações conforme elas são executadas.</span><span class="sxs-lookup"><span data-stu-id="98723-112">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="98723-113">Após a conclusão da implantação, clique em **Exibir log** para exibir os arquivos de log disponíveis.</span><span class="sxs-lookup"><span data-stu-id="98723-113">After the deployment is complete, click **View Log** to view available log files.</span></span> <span data-ttu-id="98723-114">Clique em **concluir** para concluir a implantação.</span><span class="sxs-lookup"><span data-stu-id="98723-114">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="98723-115">No servidor de borda, abra o assistente de implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="98723-115">On the Edge Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="98723-116">Clique em **instalar** ou **atualizar o Lync Server System** e, em seguida, clique em **Configurar** ou **remover componentes do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="98723-116">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="98723-117">Clique em **executar novamente**.</span><span class="sxs-lookup"><span data-stu-id="98723-117">Click **Run Again**.</span></span>

4.  <span data-ttu-id="98723-118">Adicione o Google Talk como parceiro autorizado da XMPP.</span><span class="sxs-lookup"><span data-stu-id="98723-118">Add Google Talk as an XMPP allowed partner.</span></span> <span data-ttu-id="98723-119">No momento, o Google Talk só dá suporte a conexões TCP não criptografadas para a Federação do XMPP Server-to-Server e só dá suporte à verificação de identidades do servidor.</span><span class="sxs-lookup"><span data-stu-id="98723-119">Google Talk currently only supports unencrypted, TCP connections for server-to-server XMPP federation and only supports Server Dialback for identity verification.</span></span> <span data-ttu-id="98723-120">(Consulte <http://xmpp.org/extensions/xep-0220.html> ).</span><span class="sxs-lookup"><span data-stu-id="98723-120">(See <http://xmpp.org/extensions/xep-0220.html>).</span></span>
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  <span data-ttu-id="98723-121">Para habilitar a Federação de borda, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98723-121">To enable Edge Federation, type the following:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  <span data-ttu-id="98723-122">Em **configurar componentes do Lync Server**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="98723-122">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="98723-123">A tela Resumo mostrará as ações conforme elas são executadas.</span><span class="sxs-lookup"><span data-stu-id="98723-123">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="98723-124">Depois que a implantação for concluída, clique em **Exibir log** para exibir os arquivos de log disponíveis.</span><span class="sxs-lookup"><span data-stu-id="98723-124">After the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="98723-125">Clique em **concluir** para concluir a implantação.</span><span class="sxs-lookup"><span data-stu-id="98723-125">Click **Finish** to complete the deployment.</span></span>

7.  <span data-ttu-id="98723-126">No servidor de borda, no assistente de implantação do Lync Server, ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique **novamente em executar**.</span><span class="sxs-lookup"><span data-stu-id="98723-126">On the Edge Server, in the Lync Server Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="98723-127">Se você estiver implantando o servidor de borda pela primeira vez, você verá executar novamente em vez de executar novamente.</span><span class="sxs-lookup"><span data-stu-id="98723-127">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

8.  <span data-ttu-id="98723-128">Na página **Tarefas de Certificado Disponíveis**, clique em  **Criar uma nova solicitação de certificado**.</span><span class="sxs-lookup"><span data-stu-id="98723-128">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

9.  <span data-ttu-id="98723-129">Na página **solicitação de certificado** , clique em **certificado de borda externa**.</span><span class="sxs-lookup"><span data-stu-id="98723-129">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

10. <span data-ttu-id="98723-130">Na página **solicitação atrasada ou imediata** , marque a caixa de seleção **preparar a solicitação agora, mas enviá-la mais tarde** .</span><span class="sxs-lookup"><span data-stu-id="98723-130">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

11. <span data-ttu-id="98723-131">Na página **arquivo de solicitação de certificado** , digite o caminho completo e o nome do arquivo para o qual a solicitação deve ser salva (por exemplo, c: \\ CERT \_ guia \_ Edge. cer).</span><span class="sxs-lookup"><span data-stu-id="98723-131">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

12. <span data-ttu-id="98723-132">Na página **especificar modelo de certificado alternativo** , para usar um modelo diferente do modelo padrão do webserver, marque a caixa de seleção **usar modelo de certificado alternativo para a autoridade de certificação selecionada** .</span><span class="sxs-lookup"><span data-stu-id="98723-132">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

13. <span data-ttu-id="98723-133">Na página **configurações de nome e segurança** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98723-133">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="98723-134">Em **nome amigável**, digite um nome de exibição para o certificado</span><span class="sxs-lookup"><span data-stu-id="98723-134">In **Friendly name**, type a display name for the certificate</span></span>
    
    2.  <span data-ttu-id="98723-135">Em **comprimento de bit**, especifique o comprimento do bit (geralmente, o padrão de **2048**)</span><span class="sxs-lookup"><span data-stu-id="98723-135">In **Bit length**, specify the bit length (typically, the default of **2048**)</span></span>
    
    3.  <span data-ttu-id="98723-136">Verifique se a caixa de seleção **Marcar chave privada de certificado como exportável** está marcada</span><span class="sxs-lookup"><span data-stu-id="98723-136">Verify that the **Mark certificate private key as exportable** check box is selected</span></span>

14. <span data-ttu-id="98723-137">Na página **informações da organização** , digite o nome da organização e da unidade organizacional (por exemplo, uma divisão ou um departamento)</span><span class="sxs-lookup"><span data-stu-id="98723-137">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department)</span></span>

15. <span data-ttu-id="98723-138">Na página **informações geográficas** , especifique as informações de localização</span><span class="sxs-lookup"><span data-stu-id="98723-138">On the **Geographical Information** page, specify the location information</span></span>

16. <span data-ttu-id="98723-139">Na página **nome do assunto/nomes alternativos de assunto** , as informações a serem automaticamente preenchidas pelo assistente serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="98723-139">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="98723-140">Se forem necessários nomes alternativos de entidades adicionais, você os especificará nas duas próximas etapas</span><span class="sxs-lookup"><span data-stu-id="98723-140">If additional subject alternative names are needed, you specify them in the next two steps</span></span>

17. <span data-ttu-id="98723-141">Na **configuração de domínio SIP na página de nomes alternativos de entidades (SANs)** , marque a caixa de seleção domínio para adicionar um SIP.</span><span class="sxs-lookup"><span data-stu-id="98723-141">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.</span></span> <span data-ttu-id="98723-142">\<sipdomain\> entrada para a lista nomes alternativos da entidade.</span><span class="sxs-lookup"><span data-stu-id="98723-142">\<sipdomain\> entry to the subject alternative names list.</span></span>

18. <span data-ttu-id="98723-143">Na página **configurar nomes alternativos de entidades adicionais** , especifique os nomes alternativos de entidades adicionais necessários.</span><span class="sxs-lookup"><span data-stu-id="98723-143">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="98723-144">Se o proxy XMPP estiver instalado, por padrão, o nome de domínio (como contoso.com) será preenchido nas entradas de SAN.</span><span class="sxs-lookup"><span data-stu-id="98723-144">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="98723-145">Se você precisar de mais entradas, adicione-as nesta etapa.</span><span class="sxs-lookup"><span data-stu-id="98723-145">If you require more entries, add them in this step.</span></span>

    
    </div>

19. <span data-ttu-id="98723-146">Na página **Resumo da solicitação** , examine as informações do certificado a serem usadas para gerar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="98723-146">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

20. <span data-ttu-id="98723-147">Após a conclusão da execução dos comandos, você pode **Exibir o log** ou clicar em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="98723-147">After the commands finish running, you can **View Log**, or click **Next** to continue.</span></span>

21. <span data-ttu-id="98723-148">Na página **arquivo de solicitação de certificado** , você pode exibir o arquivo de solicitação de assinatura de certificado (CSR) gerado clicando em **Exibir** ou em sair do assistente de certificado clicando em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="98723-148">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

22. <span data-ttu-id="98723-149">Copie o arquivo de solicitação e envie para sua autoridade de certificação pública.</span><span class="sxs-lookup"><span data-stu-id="98723-149">Copy the request file and submit to your public certification authority.</span></span>

23. <span data-ttu-id="98723-150">Depois de receber, importar e atribuir o certificado público, você deve parar e reiniciar os serviços do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="98723-150">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="98723-151">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**...</span><span class="sxs-lookup"><span data-stu-id="98723-151">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**..</span></span> <span data-ttu-id="98723-152">No Shell de gerenciamento do Lync Server, digite:</span><span class="sxs-lookup"><span data-stu-id="98723-152">In the Lync Server Management Shell, type:</span></span>
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. <span data-ttu-id="98723-153">Para configurar o DNS para a Federação do XMPP, adicione o seguinte registro SRV para DNS externo: \_ XMPP-Server. \_ Protocol.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="98723-153">To configure DNS for XMPP federation, you add the following SRV record to external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="98723-154">O registro SRV será resolvido para o FQDN de borda de acesso do servidor de borda, com um valor de porta de 5269</span><span class="sxs-lookup"><span data-stu-id="98723-154">The SRV record will resolve to the access edge FQDN of the Edge server, with a port value of 5269</span></span>

25. <span data-ttu-id="98723-155">Configure uma nova política de acesso externo para permitir que todos os usuários abram o Shell de gerenciamento do Lync Server em um servidor front-end e digitem:</span><span class="sxs-lookup"><span data-stu-id="98723-155">Configure a new External Access Policy to enable all users by opening the Lync Server Management Shell on a Front End Server and typing:</span></span>
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

<span data-ttu-id="98723-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98723-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

