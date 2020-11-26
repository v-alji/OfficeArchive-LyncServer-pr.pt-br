---
title: 'Lync Server 2013: Configurar certificados para a interface de borda externa'
description: 'Lync Server 2013: configurar certificados para a interface de borda externa.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the external edge interface
ms:assetid: 5d78182c-88d8-4483-95ad-74b17f2d5fac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398409(v=OCS.15)
ms:contentKeyID: 48184287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aeca6edf0a3b50ab5dcaf9ecdbaea931d7bdf947
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441750"
---
# <a name="set-up-certificates-for-the-external-edge-interface-for-lync-server-2013"></a><span data-ttu-id="b4fb3-103">Configurar certificados para a interface de borda externa para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b4fb3-103">Set up certificates for the external edge interface for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b4fb3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b4fb3-104">

<span> </span></span></span>

<span data-ttu-id="b4fb3-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="b4fb3-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b4fb3-106">Ao executar o assistente de certificado, certifique-se de que você esteja conectado usando uma conta que seja membro de um grupo que tenha recebido as permissões apropriadas para o tipo de modelo de certificado que você vai usar.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-106">When you run the Certificate Wizard, ensure that you are logged in using an account that is a member of a group that has been assigned the appropriate permissions for the type of certificate template you will use.</span></span> <span data-ttu-id="b4fb3-107">Por padrão, uma solicitação de certificado do Lync Server vai usar o modelo de certificado de servidor Web.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-107">By default, a Lync Server certificate request will use the Web Server certificate template.</span></span> <span data-ttu-id="b4fb3-108">Se você usar uma conta que seja um membro do grupo RTCUniversalServerAdmins para solicitar um certificado usando esse modelo, verifique se o grupo recebeu as permissões de Registro necessárias para usar esse modelo.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-108">If you use an account that is a member of the RTCUniversalServerAdmins group to request a certificate using this template, verify that the group has been assigned the Enroll permissions required to use that template.</span></span>



</div>

<span data-ttu-id="b4fb3-109">Cada servidor de borda requer um certificado público na interface entre a rede de perímetro e a Internet, e o nome alternativo do sujeito do certificado deve conter os nomes externos dos FQDNs (nomes de domínio totalmente qualificados do serviço de borda de acesso e Web de Webconferência).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-109">Each Edge Server requires a public certificate on the interface between the perimeter network and the Internet, and the certificate’s subject alternative name must contain the external names of the Access Edge service and Web Conferencing Edge service fully qualified domain names (FQDNs).</span></span>

<span data-ttu-id="b4fb3-110">Para obter detalhes sobre esse e outros requisitos de certificado, consulte [requisitos de certificado para acesso de usuários externos no Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-110">For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span></span>

<span data-ttu-id="b4fb3-111">Para obter uma lista de autoridades de certificação (CAs) públicas que fornecem certificados compatíveis com requisitos específicos para certificados de comunicação unificada e que têm parceria com a Microsoft para garantir que elas funcionem com o assistente de certificado do Lync Server 2013, consulte o artigo 929395, "parceiros de certificado de comunicação unificada para Exchange Server e para comunicações Server" em [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) .</span><span class="sxs-lookup"><span data-stu-id="b4fb3-111">For a list of public certification authorities (CAs) that provide certificates that comply with specific requirements for unified communications certificates and have partnered with Microsoft to ensure they work with the Lync Server 2013 Certificate Wizard, see Microsoft Knowledge Base article 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<div>

## <a name="configuring-certificates-on-the-external-interfaces"></a><span data-ttu-id="b4fb3-112">Configurar certificados nas interfaces externas</span><span class="sxs-lookup"><span data-stu-id="b4fb3-112">Configuring Certificates on the External Interfaces</span></span>

<span data-ttu-id="b4fb3-113">Para configurar um certificado na interface de borda externa em um site, use os procedimentos desta seção para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4fb3-113">To set up a certificate on the external edge interface at a site, use the procedures in this section to do the following:</span></span>

  - <span data-ttu-id="b4fb3-114">Crie a solicitação de certificado para a interface externa do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-114">Create the certificate request for the external interface of the Edge Server.</span></span>

  - <span data-ttu-id="b4fb3-115">Envie a solicitação para sua CA pública.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-115">Submit the request to your public CA.</span></span>

  - <span data-ttu-id="b4fb3-116">Importar o certificado para a interface externa de cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-116">Import the certificate for the external interface of each Edge Server.</span></span>

  - <span data-ttu-id="b4fb3-117">Atribua o certificado para a interface externa de cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-117">Assign the certificate for the external interface of each Edge Server.</span></span>

  - <span data-ttu-id="b4fb3-118">Se a sua implantação inclui vários servidores de borda, exporte o certificado juntamente com sua chave particular e copie-o para outros servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-118">If your deployment includes multiple Edge Servers, export the certificate along with its private key, and then copy it to the other Edge Servers.</span></span> <span data-ttu-id="b4fb3-119">Em seguida, para cada servidor de borda, importe-o e atribua-o conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-119">Then, for each Edge Server, import it and assign it as previously described.</span></span> <span data-ttu-id="b4fb3-120">Repita esse procedimento para cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-120">Repeat this procedure for each Edge Server.</span></span>

<span data-ttu-id="b4fb3-121">Você pode solicitar certificados públicos diretamente de uma CA (autoridade de certificação) pública (por exemplo, do site de uma CA pública).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-121">You can request public certificates directly from a public certification authority (CA) (such as from the website of a public CA).</span></span> <span data-ttu-id="b4fb3-122">Os procedimentos desta seção usam o assistente de certificado para a maioria das tarefas de certificado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-122">The procedures in this section use the Certificate Wizard for most certificate tasks.</span></span> <span data-ttu-id="b4fb3-123">Se você optou por solicitar um certificado diretamente de uma CA pública, será necessário modificar cada procedimento conforme apropriado para solicitar, transportar e importar o certificado e também para importar a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-123">If you chose to request a certificate directly from a public CA, then you will need to modify each procedure as appropriate to request, transport, and import the certificate and also to import the certificate chain.</span></span>

<span data-ttu-id="b4fb3-124">Quando você solicita um certificado de uma autoridade de certificação externa, as credenciais fornecidas devem ter direitos de solicitar um certificado dessa CA.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-124">When you request a certificate from an External CA, the credentials provided must have rights to request a certificate from that CA.</span></span> <span data-ttu-id="b4fb3-125">Cada CA tem uma política de segurança que define quais credenciais (ou seja, nomes de usuário e grupo específicos) têm permissão para solicitar, emitir, gerenciar ou ler certificados.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-125">Each CA has a security policy that defines which credentials (that is, specific user and group names) are allowed to request, issue, manage, or read certificates.</span></span>

<span data-ttu-id="b4fb3-126">Se você decidir usar o console de gerenciamento da Microsoft (MMC) de certificados para importar a cadeia de certificados e o certificado, será necessário importá-los para o repositório de certificados do computador.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-126">If you decide to use the Certificates Microsoft Management Console (MMC) to import the certificate chain and certificate, you must import them to the certificate store for the computer.</span></span> <span data-ttu-id="b4fb3-127">Se você importá-los para o repositório de certificados do usuário ou do serviço, o certificado não estará disponível para atribuição no assistente de certificado do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-127">If you import them to the user or service certificate store, the certificate will not be available for assignment in the Lync Server 2013 Certificate Wizard.</span></span>

<div>

## <a name="to-create-the-certificate-request-for-the-external-interface-of-the-edge-server"></a><span data-ttu-id="b4fb3-128">Para criar a solicitação de certificado para a interface externa do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="b4fb3-128">To create the certificate request for the external interface of the Edge Server</span></span>

1.  <span data-ttu-id="b4fb3-129">No servidor de borda, no assistente de implantação, ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique **novamente em executar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-129">On the Edge Server, in the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b4fb3-130">Se a sua organização quiser dar suporte à conectividade de mensagens instantâneas (IM) pública com a AOL, você não poderá usar o assistente de implantação do Lync Server para solicitar o certificado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-130">If your organization wants to support public instant messaging (IM) connectivity with AOL, you cannot use the Lync Server Deployment Wizard to request the certificate.</span></span> <span data-ttu-id="b4fb3-131">Em vez disso, execute as etapas na etapa "para criar uma solicitação de certificado para a interface externa do servidor de borda para dar suporte à conectividade de IM pública com a AOL", mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-131">Instead, perform the steps in the “To create a certificate request for the external interface of the Edge Server to support public IM connectivity with AOL” procedure later in this topic.</span></span><BR><span data-ttu-id="b4fb3-132">Se você tiver vários servidores de borda em um local em um pool, poderá executar o assistente de certificado do Lync Server 2013 em qualquer um dos servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-132">If you have multiple Edge Servers in one location in a pool, you can run the Lync Server 2013 Certificate Wizard on any one of the Edge Servers.</span></span>

    
    </div>

2.  <span data-ttu-id="b4fb3-133">Na página **Tarefas de Certificado Disponíveis**, clique em  **Criar uma nova solicitação de certificado**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-133">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

3.  <span data-ttu-id="b4fb3-134">Na página **solicitação de certificado** , clique em **certificado de borda externa**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-134">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

4.  <span data-ttu-id="b4fb3-135">Na página **solicitação atrasada ou imediata** , marque a caixa de seleção **preparar a solicitação agora, mas enviá-la mais tarde** .</span><span class="sxs-lookup"><span data-stu-id="b4fb3-135">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

5.  <span data-ttu-id="b4fb3-136">Na página **arquivo de solicitação de certificado** , digite o caminho completo e o nome do arquivo para o qual a solicitação deve ser salva (por exemplo, c: \\ CERT \_ guia \_ Edge. cer).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-136">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

6.  <span data-ttu-id="b4fb3-137">Na página **especificar modelo de certificado alternativo** , para usar um modelo diferente do modelo padrão do webserver, marque a caixa de seleção **usar modelo de certificado alternativo para a autoridade de certificação selecionada** .</span><span class="sxs-lookup"><span data-stu-id="b4fb3-137">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

7.  <span data-ttu-id="b4fb3-138">Na página **configurações de nome e segurança** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4fb3-138">On the **Name and Security Settings** page, do the following:</span></span>
    
      - <span data-ttu-id="b4fb3-139">Em **nome amigável**, digite um nome de exibição para o certificado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-139">In **Friendly name**, type a display name for the certificate.</span></span>
    
      - <span data-ttu-id="b4fb3-140">Em **comprimento de bit**, especifique o comprimento do bit (geralmente, o padrão de **2048**).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-140">In **Bit length**, specify the bit length (typically, the default of **2048**).</span></span>
    
      - <span data-ttu-id="b4fb3-141">Verifique se a caixa de seleção **Marcar chave privada de certificado como exportável** está marcada.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-141">Verify that the **Mark certificate private key as exportable** check box is selected.</span></span>

8.  <span data-ttu-id="b4fb3-142">Na página **informações da organização** , digite o nome da organização e da unidade organizacional (por exemplo, uma divisão ou um departamento).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-142">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department).</span></span>

9.  <span data-ttu-id="b4fb3-143">Na página **informações geográficas** , especifique as informações de localização.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-143">On the **Geographical Information** page, specify the location information.</span></span>

10. <span data-ttu-id="b4fb3-144">Na página **nome do assunto/nomes alternativos de assunto** , as informações a serem automaticamente preenchidas pelo assistente serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-144">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="b4fb3-145">Se forem necessários nomes alternativos de entidades adicionais, especifique-os nas próximas duas etapas.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-145">If additional subject alternative names are needed, you specify them in the next two steps.</span></span>

11. <span data-ttu-id="b4fb3-146">Na **configuração de domínio SIP na página de nomes alternativos de entidades (SANs)** , marque a caixa de seleção domínio para adicionar um SIP.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="b4fb3-146">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.\<sipdomain\></span></span> <span data-ttu-id="b4fb3-147">entrada para a lista nomes alternativos da entidade.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-147">entry to the subject alternative names list.</span></span>

12. <span data-ttu-id="b4fb3-148">Na página **configurar nomes alternativos de entidades adicionais** , especifique os nomes alternativos de entidades adicionais necessários.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-148">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>

13. <span data-ttu-id="b4fb3-149">Na página **Resumo da solicitação** , examine as informações do certificado a serem usadas para gerar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-149">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

14. <span data-ttu-id="b4fb3-150">Depois que os comandos terminarem de ser executados, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4fb3-150">After the commands finish running, do the following:</span></span>
    
      - <span data-ttu-id="b4fb3-151">Para exibir o log para a solicitação de certificado, clique em **Exibir log**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-151">To view the log for the certificate request, click **View Log**.</span></span>
    
      - <span data-ttu-id="b4fb3-152">Para concluir a solicitação de certificado, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-152">To complete the certificate request, click **Next**.</span></span>

15. <span data-ttu-id="b4fb3-153">Na página **arquivo de solicitação de certificado** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4fb3-153">On the **Certificate Request File** page, do the following:</span></span>
    
      - <span data-ttu-id="b4fb3-154">Para exibir o arquivo de solicitação de assinatura de certificado (CSR) gerado, clique em **Exibir**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-154">To view the generated certificate signing request (CSR) file, click **View**.</span></span>
    
      - <span data-ttu-id="b4fb3-155">Para fechar o assistente, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-155">To close the wizard, click **Finish**.</span></span>

16. <span data-ttu-id="b4fb3-156">Copie o arquivo de saída para um local onde você possa enviá-lo para a CA pública.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-156">Copy the output file to a location where you can submit it to the public CA.</span></span>

</div>

<div>

## <a name="to-create-a-certificate-request-for-the-external-interface-of-the-edge-server-to-support-public-im-connectivity-with-aol"></a><span data-ttu-id="b4fb3-157">Para criar uma solicitação de certificado para a interface externa do servidor de borda para dar suporte à conectividade de mensagem de chat pública com a AOL</span><span class="sxs-lookup"><span data-stu-id="b4fb3-157">To create a certificate request for the external interface of the Edge Server to support public IM connectivity with AOL</span></span>

1.  <span data-ttu-id="b4fb3-158">Quando o modelo obrigatório estiver disponível para a autoridade de certificação, use o seguinte cmdlet do Windows PowerShell no servidor de borda para solicitar o certificado:</span><span class="sxs-lookup"><span data-stu-id="b4fb3-158">When the required template is available to the CA, use the following Windows PowerShell cmdlet from at the Edge Server to request the certificate:</span></span>
    
        Request-CsCertificate -New -Type AccessEdgeExternal  -Output C:\ <certfilename.txt or certfilename.csr>  -ClientEku $true -Template <template name>
    
    <span data-ttu-id="b4fb3-159">O nome de certificado padrão do modelo fornecido no Lync Server 2013 é o servidor Web.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-159">The default certificate name of the template provided in Lync Server 2013 is Web Server.</span></span> <span data-ttu-id="b4fb3-160">Somente especifique o \<template name\> se você precisar usar um modelo diferente do modelo padrão.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-160">Only specify the \<template name\> if you need to use a template that is different from the default template.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b4fb3-161">Se a sua organização quiser dar suporte à conectividade de mensagem instantânea pública com a AOL, você deve usar o Windows PowerShell em vez do assistente de certificado para solicitar que o certificado seja atribuído à borda externa do serviço de borda de acesso.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-161">If your organization wants to support public IM connectivity with AOL, you must use Windows PowerShell instead of the Certificate Wizard to request the certificate to be assigned to the external edge for the Access Edge service.</span></span> <span data-ttu-id="b4fb3-162">Isso ocorre porque o modelo de servidor Web do Lync Server 2013 que o assistente de certificado usa para solicitar um certificado não dá suporte à configuração de EKU de cliente.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-162">This is because the Lync Server 2013 Web Server template that the Certificate Wizard uses to request a certificate does not support client EKU configuration.</span></span> <span data-ttu-id="b4fb3-163">Antes de usar o Windows PowerShell para criar o certificado, o administrador da CA deve criar e implantar um novo modelo compatível com o EKU do cliente.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-163">Before using Windows PowerShell to create the certificate, the CA administrator must create and deploy a new template that supports client EKU.</span></span>

    
    </div>

</div>

<div>

## <a name="to-submit-a-request-to-a-public-certification-authority"></a><span data-ttu-id="b4fb3-164">Para enviar uma solicitação para uma autoridade de certificação pública</span><span class="sxs-lookup"><span data-stu-id="b4fb3-164">To submit a request to a public certification authority</span></span>

1.  <span data-ttu-id="b4fb3-165">Abra o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-165">Open the output file.</span></span>

2.  <span data-ttu-id="b4fb3-166">Copie e cole o conteúdo da solicitação de assinatura de certificado (CSR).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-166">Copy and paste the contents of the Certificate Signing Request (CSR).</span></span>

3.  <span data-ttu-id="b4fb3-167">Se solicitado, especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4fb3-167">If prompted, specify the following:</span></span>
    
      - <span data-ttu-id="b4fb3-168">A **Microsoft** como a plataforma do servidor.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-168">**Microsoft** as the server platform.</span></span>
    
      - <span data-ttu-id="b4fb3-169">**IIS** como a versão.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-169">**IIS** as the version.</span></span>
    
      - <span data-ttu-id="b4fb3-170">**Servidor Web** como o tipo de uso.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-170">**Web Server** as the usage type.</span></span>
    
      - <span data-ttu-id="b4fb3-171">**PKCS7** como o formato de resposta.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-171">**PKCS7** as the response format.</span></span>

4.  <span data-ttu-id="b4fb3-172">Quando a autoridade de certificação pública tiver verificado suas informações, você receberá uma mensagem de email com o texto necessário para o seu certificado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-172">When the public CA has verified your information, you will receive an email message containing text required for your certificate.</span></span>

5.  <span data-ttu-id="b4fb3-173">Copie o texto da mensagem de email e salve o conteúdo em um arquivo de texto (. txt) em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-173">Copy the text from the email message and save the contents in a text file (.txt) on your local computer.</span></span>

</div>

<div>

## <a name="to-import-the-certificate-for-the-external-interface-of-the-edge-server"></a><span data-ttu-id="b4fb3-174">Para importar o certificado para a interface externa do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="b4fb3-174">To import the certificate for the external interface of the Edge Server</span></span>

1.  <span data-ttu-id="b4fb3-175">Faça logon como membro do grupo Administradores para o mesmo servidor de borda em que você criou a solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-175">Log on as a member of the Administrators group to the same Edge Server on which you created the certificate request.</span></span>

2.  <span data-ttu-id="b4fb3-176">No assistente de implantação, na página **implantar servidor de borda** , ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique **novamente em executar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-176">In the Deployment Wizard, on the **Deploy Edge Server** page, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>

3.  <span data-ttu-id="b4fb3-177">Na página **tarefas de certificado disponíveis** , clique em **importar um certificado de um arquivo. p7b, pfx ou. cer**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-177">On the **Available Certificate Tasks** page, click **Import a certificate from a .p7b, pfx or .cer file**.</span></span>

4.  <span data-ttu-id="b4fb3-178">Na página **importar certificado** , clique em **procurar** para localizar e selecionar o certificado que você solicitou para a interface externa do servidor de borda (ou, você pode digitar o caminho completo e o nome do arquivo).</span><span class="sxs-lookup"><span data-stu-id="b4fb3-178">On the **Import Certificate** page, click **Browse** to locate and select the certificate that you requested for the external interface of the Edge Server (or, you can type the full path and file name).</span></span> <span data-ttu-id="b4fb3-179">Se o certificado contiver uma chave privada, selecione **arquivo de certificado contém a chave privada do certificado** e digite a senha da chave privada.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-179">If the certificate contains a private key, select **Certificate file contains certificate’s private key** and type the password for the private key.</span></span> <span data-ttu-id="b4fb3-180">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-180">Click **Next**.</span></span>

5.  <span data-ttu-id="b4fb3-181">Na página **importar Resumo do certificado** , examine o resumo e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-181">On **Import Certificate Summary** page, review the summary and then click **Next**.</span></span>

6.  <span data-ttu-id="b4fb3-182">Na **execução de comandos**, examine os resultados da importação, clique em **Exibir log** para obter mais informações conforme necessário e clique em **concluir** para concluir a importação de certificado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-182">On **Executing Commands**, review the results of the import, click **View Log** for more information as needed, and then click **Finish** to complete the certificate import.</span></span>

7.  <span data-ttu-id="b4fb3-183">Se você estiver configurando um pool do servidor de borda, exporte o certificado com sua chave privada, conforme descrito no procedimento "para exportar o certificado com a chave privada para servidores de borda em um pool" mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-183">If you are configuring an Edge Server pool, export the certificate with its private key as outlined in the “To export the certificate with the private key for Edge Servers in a pool” procedure later in this topic.</span></span> <span data-ttu-id="b4fb3-184">Copie o arquivo de certificado exportado para os outros servidores de borda e importe-o para a loja do computador em cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-184">Copy the exported certificate file to the other Edge Servers, and import it into the computer store on each Edge Server.</span></span>

</div>

<div>

## <a name="to-export-the-certificate-with-the-private-key-for-edge-servers-in-a-pool"></a><span data-ttu-id="b4fb3-185">Para exportar o certificado com a chave privada para servidores de borda em um pool</span><span class="sxs-lookup"><span data-stu-id="b4fb3-185">To export the certificate with the private key for Edge Servers in a pool</span></span>

1.  <span data-ttu-id="b4fb3-186">Faça logon como membro do grupo Administradores para o mesmo servidor de borda no qual você importou o certificado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-186">Log on as a member of the Administrators group to the same Edge Server on which you imported the certificate.</span></span>

2.  <span data-ttu-id="b4fb3-187">Clique em **Iniciar**, clique em **executar** e digite **MMC**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-187">Click **Start**, click **Run**, and type **MMC**.</span></span>

3.  <span data-ttu-id="b4fb3-188">No console do console de gerenciamento Microsoft (MMC), clique em **arquivo** e, em seguida, clique em **Adicionar/remover snap-in**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-188">In the Microsoft Management Console (MMC) console, click **File**, and then click **Add/Remove Snap-in**.</span></span>

4.  <span data-ttu-id="b4fb3-189">Em **Adicionar ou remover snap-ins**, clique em **certificados** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-189">In **Add or Remove Snap-ins**, click **Certificates**, and then click **Add**.</span></span>

5.  <span data-ttu-id="b4fb3-190">Na caixa de diálogo **certificados** , selecione **conta de computador**, clique em **Avançar**, selecione **computador local: (o computador em que este console está sendo executado)** em **Selecionar computador**, clique em **concluir** e, em seguida, clique em **OK** para concluir a configuração do console do MMC.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-190">In the **Certificates** dialog box, select **Computer account**, click **Next**, select **Local computer: (the computer this console is running on)** in **Select Computer**, click **Finish** and then click **OK** to complete configuration of the MMC console.</span></span>

6.  <span data-ttu-id="b4fb3-191">Clique duas vezes em **certificados (computador local)** para expandir os repositórios de certificados, clique duas vezes em **pessoal** e, em seguida, clique duas vezes em **certificados**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-191">Double-click **Certificates (Local Computer)** to expand the certificate stores, double-click **Personal**, and then double-click **Certificates**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b4fb3-192">Se não houver certificados no armazenamento pessoal de certificados do computador local, não há uma chave privada associada ao certificado que foi importado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-192">If there are no certificates in the Certificates Personal store for the local computer, there is no private key associated with the certificate that was imported.</span></span> <span data-ttu-id="b4fb3-193">Examine as etapas de solicitação e importação.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-193">Review the request and import steps.</span></span> <span data-ttu-id="b4fb3-194">Se o problema persistir, entre em contato com o administrador ou o provedor da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-194">If the problem persists, contact your certification authority administrator or provider.</span></span>

    
    </div>

7.  <span data-ttu-id="b4fb3-195">No **repositório pessoal de certificados do computador local**, clique com o botão direito do mouse no certificado que você está exportando, clique em **todas as tarefas** e, em seguida, clique em **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-195">In the **Certificates Personal store for the local computer**, right-click the certificate that you are exporting, click **All Tasks**, and then click **Export**.</span></span>

8.  <span data-ttu-id="b4fb3-196">No Assistente para exportação de certificados, clique em **Avançar**, selecione **Sim, exportar a chave particular** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-196">In the Certificate Export Wizard, click **Next**, select **Yes, export the private key**, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b4fb3-197">Se a seleção <STRONG>Sim, exportar a chave privada</STRONG> não estiver disponível, a chave privada associada a esse certificado não foi marcada para exportação.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-197">If the selection <STRONG>Yes, export the private key</STRONG> is not available, the private key associated with this certificate was not marked for export.</span></span> <span data-ttu-id="b4fb3-198">Você precisará solicitar o certificado novamente, certificando-se de que o certificado esteja marcado para permitir a exportação da chave privada antes de continuar com a exportação.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-198">You will need to request the certificate again, ensuring that the certificate is marked to allow for the export of the private key before you can continue with the export.</span></span> <span data-ttu-id="b4fb3-199">Entre em contato com o administrador ou provedor da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-199">Contact your certification authority administrator or provider.</span></span>

    
    </div>

9.  <span data-ttu-id="b4fb3-200">Na caixa de diálogo Exportar formatos de arquivo, selecione **troca de informações pessoais – PKCS \# 12 (. PFX)** e, em seguida, selecione o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4fb3-200">On the Export File Formats dialog, select **Personal Information Exchange – PKCS\#12 (.PFX)** and then select the following:</span></span>
    
      - <span data-ttu-id="b4fb3-201">Incluir todos os certificados no caminho de certificação, se possível</span><span class="sxs-lookup"><span data-stu-id="b4fb3-201">Include all certificates in the certification path if possible</span></span>
    
      - <span data-ttu-id="b4fb3-202">Exportar todas as propriedades estendidas</span><span class="sxs-lookup"><span data-stu-id="b4fb3-202">Export all extended properties</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="b4fb3-203">Ao exportar o certificado de um servidor de borda, não selecione <STRONG>excluir a chave privada se a exportação for bem-sucedida</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-203">When exporting the certificate from an Edge server, do not select <STRONG>Delete the private key if the export is successful</STRONG>.</span></span> <span data-ttu-id="b4fb3-204">Selecionar essa opção exigirá que você importe o certificado e a chave privada para esse servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-204">Selecting this option will require that you import the certificate and the private key to this Edge server.</span></span>

        
        </div>

10. <span data-ttu-id="b4fb3-205">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-205">Click **Next**.</span></span>

11. <span data-ttu-id="b4fb3-206">Digite uma senha para a chave privada, digite a senha novamente para confirmá-la e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-206">Type a password for the private key, type the password again to confirm, and then click **Next**.</span></span>

12. <span data-ttu-id="b4fb3-207">Digite um caminho e o nome de arquivo para o certificado exportado, usando uma extensão de arquivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-207">Type a path and file name for the exported certificate, using a file extension of .pfx.</span></span> <span data-ttu-id="b4fb3-208">O caminho deve ser acessível a todos os outros servidores de borda do pool ou disponível para transporte por meio de mídia removível-por exemplo, uma unidade flash USB.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-208">The path must either be accessible to all other Edge servers in the pool or available to transport by means of removable media - for example, a USB flash drive.</span></span> <span data-ttu-id="b4fb3-209">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-209">Click **Next**.</span></span>

13. <span data-ttu-id="b4fb3-210">Examine o resumo em **concluindo o assistente para exportação de certificados** e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-210">Review the summary in **Completing the Certificate Export Wizard**, and then click **Finish**.</span></span>

14. <span data-ttu-id="b4fb3-211">Na caixa de diálogo exportação bem-sucedida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-211">In the successful export dialog box, click **OK**.</span></span>

15. <span data-ttu-id="b4fb3-212">Importe o arquivo de certificado exportado para os outros servidores de borda seguindo as etapas descritas no procedimento "para importar o certificado para a interface externa do servidor de borda" anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-212">Import the exported certificate file to the other Edge servers following the steps outlined in the “To import the certificate for the external interface of the Edge Server” procedure earlier in this topic.</span></span>

</div>

<div>

## <a name="to-assign-the-certificate-for-the-external-interface-of-the-edge-server"></a><span data-ttu-id="b4fb3-213">Para atribuir o certificado para a interface externa do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="b4fb3-213">To assign the certificate for the external interface of the Edge Server</span></span>

1.  <span data-ttu-id="b4fb3-214">Em cada servidor de borda, no assistente de implantação, ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique **novamente em executar**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-214">On each Edge Server, in the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>

2.  <span data-ttu-id="b4fb3-215">Na página **tarefas de certificado disponíveis** , clique em **atribuir um certificado existente**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-215">On the **Available Certificate Tasks** page, click **Assign an existing certificate**.</span></span>

3.  <span data-ttu-id="b4fb3-216">Na página **atribuição de certificado** , clique em **certificado de borda externa** e marque a caixa de seleção **usos avançados de certificado** .</span><span class="sxs-lookup"><span data-stu-id="b4fb3-216">On the **Certificate Assignment** page, click **External Edge Certificate** and select the **Advanced Certificate Usages** check box.</span></span>

4.  <span data-ttu-id="b4fb3-217">Na página **usos avançados de certificado** , marque todas as caixas de seleção para atribuir o certificado para todos os usos.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-217">On the **Advanced Certificate Usages** page, select all check boxes to assign the certificate for all usages.</span></span>

5.  <span data-ttu-id="b4fb3-218">Na página **repositório de certificados** , selecione o certificado público que você solicitou e importou para a interface externa do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-218">On the **Certificate Store** page, select the public certificate that you requested and imported for the external interface of the Edge Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b4fb3-219">Se o certificado que você solicitou e importado não estiver na lista, um dos métodos de solução de problemas será verificar se o nome da entidade e os nomes alternativos da entidade do certificado atendem a todos os requisitos do certificado e, se você importou manualmente o certificado e a cadeia de certificados em vez de usar os procedimentos anteriores, se o certificado estiver no repositório de certificados correto , não o usuário ou o repositório de certificados do serviço.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-219">If the certificate you requested and imported is not in the list, one of the trouble shooting methods is to verify that subject name and subject alternative names of the certificate meet all requirements for the certificate and, if you manually imported the certificate and certificate chain instead of using the preceding procedures, that the certificate is in the correct certificate store (the computer certificate store, not the user or service certificate store).</span></span>

    
    </div>

6.  <span data-ttu-id="b4fb3-220">Na página **Resumo de atribuição de certificado** , examine suas configurações e clique em **Avançar** para atribuir os certificados.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-220">On the **Certificate Assignment Summary** page, review your settings, and then click **Next** to assign the certificates.</span></span>

7.  <span data-ttu-id="b4fb3-221">Na página de conclusão do assistente, clique em  **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-221">On the wizard completion page, click **Finish**.</span></span>

8.  <span data-ttu-id="b4fb3-222">Depois de usar esse procedimento para atribuir o certificado de borda, abra o snap-in de certificado em cada servidor, expanda **certificados (computador local)**, expanda **pessoal**, clique em **certificados** e verifique no painel de detalhes se o certificado está listado.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-222">After using this procedure to assign the edge certificate, open the Certificate snap-in on each server, expand **Certificates (Local computer)**, expand **Personal**, click **Certificates**, and then verify in the details pane that the certificate is listed.</span></span>

9.  <span data-ttu-id="b4fb3-223">Se a sua implantação incluir vários servidores de borda, repita esse procedimento para cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="b4fb3-223">If your deployment includes multiple Edge Servers, repeat this procedure for each Edge Server.</span></span>

<span data-ttu-id="b4fb3-224"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b4fb3-224"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

