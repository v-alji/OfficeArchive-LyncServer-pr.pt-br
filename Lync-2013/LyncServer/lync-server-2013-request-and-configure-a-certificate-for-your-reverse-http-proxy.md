---
title: Solicitar e configurar um certificado para seu proxy HTTP reverso
description: Solicite e configure um certificado para seu proxy HTTP reverso.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Request and configure a certificate for your reverse HTTP proxy
ms:assetid: 4b70991e-5f10-40a3-b069-0b227c3a3a0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429704(v=OCS.15)
ms:contentKeyID: 48184085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdeaa080e3ccb6a9895e18a6ac02084e99a1e33e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442744"
---
# <a name="request-and-configure-a-certificate-for-your-reverse-http-proxy-in-lync-server-2013"></a><span data-ttu-id="ecfee-103">Solicitar e configurar um certificado para seu proxy HTTP reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecfee-103">Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ecfee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ecfee-104">

<span> </span></span></span>

<span data-ttu-id="ecfee-105">_**Tópico da última modificação:** 2014-02-14_</span><span class="sxs-lookup"><span data-stu-id="ecfee-105">_**Topic Last Modified:** 2014-02-14_</span></span>

<span data-ttu-id="ecfee-106">Você precisa instalar o certificado de autoridade de certificação (CA) raiz no servidor que executa o Microsoft Forefront Threat Management Gateway 2010 ou o IIS ARR para a infraestrutura da CA que emitiu os certificados do servidor para os servidores internos que executam o Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ecfee-106">You need to install the root certification authority (CA) certificate on the server running Microsoft Forefront Threat Management Gateway 2010 or IIS ARR for the CA infrastructure that issued the server certificates to the internal servers running Microsoft Lync Server 2013.</span></span>

<span data-ttu-id="ecfee-107">Você também deve instalar um certificado de servidor Web público em seu servidor proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="ecfee-107">You also must install a public web server certificate on your reverse proxy server.</span></span> <span data-ttu-id="ecfee-108">Os nomes alternativos da entidade deste certificado devem conter os nomes de domínio totalmente qualificados externos (FQDNs) publicados de cada pool que seja home para os usuários habilitados para acesso remoto e os FQDNs externos de todos os diretores ou pools de directors que serão usados nessa infraestrutura de borda.</span><span class="sxs-lookup"><span data-stu-id="ecfee-108">This certificate’s subject alternative names should contain the published external fully qualified domain names (FQDNs) of each pool that is home to users enabled for remote access, and the external FQDNs of all Directors or Director pools that will be used within that Edge infrastructure.</span></span> <span data-ttu-id="ecfee-109">O nome alternativo do assunto também deve conter a URL simples da reunião, a URL simples discada e, se você estiver implantando aplicativos móveis e planejar usar a descoberta automática, a URL do serviço de descoberta automática externa, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ecfee-109">The subject alternative name must also contain the meeting simple URL, the dial-in simple URL, and, if you are deploying mobile applications and plan to use automatic discovery, the external Autodiscover Service URL as shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ecfee-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ecfee-110">Value</span></span></th>
<th><span data-ttu-id="ecfee-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ecfee-111">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecfee-112">Nome do assunto</span><span class="sxs-lookup"><span data-stu-id="ecfee-112">Subject name</span></span></p></td>
<td><p><span data-ttu-id="ecfee-113">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="ecfee-113">Pool FQDN</span></span></p></td>
<td><p><span data-ttu-id="ecfee-114">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ecfee-114">webext.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecfee-115">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="ecfee-115">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="ecfee-116">FQDN do pool</span><span class="sxs-lookup"><span data-stu-id="ecfee-116">Pool FQDN</span></span></p></td>
<td><p><span data-ttu-id="ecfee-117">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ecfee-117">webext.contoso.com</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="ecfee-118">O nome do requerente também deve estar presente no nome alternativo do assunto.</span><span class="sxs-lookup"><span data-stu-id="ecfee-118">The subject name must also be present in the subject alternative name.</span></span>

</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecfee-119">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="ecfee-119">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="ecfee-120">Serviços Web de director opcionais (se o diretor for implantado)</span><span class="sxs-lookup"><span data-stu-id="ecfee-120">Optional Director Web Services (if Director is deployed)</span></span></p></td>
<td><p><span data-ttu-id="ecfee-121">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ecfee-121">webdirext.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecfee-122">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="ecfee-122">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="ecfee-123">URL simples de reunião</span><span class="sxs-lookup"><span data-stu-id="ecfee-123">Meeting simple URL</span></span></p>



> [!NOTE]
> <span data-ttu-id="ecfee-124">Todas as URLs simples de reunião devem estar no nome alternativo da entidade.</span><span class="sxs-lookup"><span data-stu-id="ecfee-124">All meeting simple URLs must be in the subject alternative name.</span></span> <span data-ttu-id="ecfee-125">Cada domínio SIP deve ter pelo menos uma URL simples de reunião ativa.</span><span class="sxs-lookup"><span data-stu-id="ecfee-125">Each SIP domain must have at least one active meeting simple URL.</span></span>

</td>
<td><p><span data-ttu-id="ecfee-126">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ecfee-126">meet.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecfee-127">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="ecfee-127">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="ecfee-128">URL simples de discagem</span><span class="sxs-lookup"><span data-stu-id="ecfee-128">Dial-in simple URL</span></span></p></td>
<td><p><span data-ttu-id="ecfee-129">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ecfee-129">dialin.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecfee-130">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="ecfee-130">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="ecfee-131">Servidor Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="ecfee-131">Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="ecfee-132">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ecfee-132">officewebapps01.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecfee-133">Nome alternativo de entidade</span><span class="sxs-lookup"><span data-stu-id="ecfee-133">Subject alternative name</span></span></p></td>
<td><p><span data-ttu-id="ecfee-134">URL do serviço de descoberta automática externo</span><span class="sxs-lookup"><span data-stu-id="ecfee-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="ecfee-135">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ecfee-135">lyncdiscover.contoso.com</span></span></p>



> [!NOTE]
> <span data-ttu-id="ecfee-136">Se você também estiver usando o Microsoft Exchange Server, também precisará configurar regras de proxy reverso para as URLs de serviços Web e descoberta automática do Exchange.</span><span class="sxs-lookup"><span data-stu-id="ecfee-136">If you are also using Microsoft Exchange Server you will also need to configure reverse proxy rules for the Exchange autodiscover and web services URLs.</span></span>

</td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]
> <span data-ttu-id="ecfee-137">Se a sua implantação interna consistir em mais de um servidor Standard Edition ou pool de front-end, você deverá configurar regras de publicação na Web para cada FQDN do Web farm externo e será necessário um ouvinte de certificado e Web para cada um, ou obter um certificado cujo nome alternativo da entidade contenha os nomes usados por todos os grupos, atribuí-los a um ouvinte da Web e compartilhe entre várias regras de publicação na Web.</span><span class="sxs-lookup"><span data-stu-id="ecfee-137">If your internal deployment consists of more than one Standard Edition server or Front End pool, you must configure web publishing rules for each external web farm FQDN and you will either need a certificate and web listener for each, or you must obtain a certificate whose subject alternative name contains the names used by all of the pools, assign it to a web listener, and share it among multiple web publishing rules.</span></span>



</div>

<div>

## <a name="create-a-certificate-request"></a><span data-ttu-id="ecfee-138">Criar uma solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="ecfee-138">Create a Certificate Request</span></span>

<span data-ttu-id="ecfee-139">Crie uma solicitação de certificado no proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="ecfee-139">You create a certificate request on the reverse proxy.</span></span> <span data-ttu-id="ecfee-140">Você cria uma solicitação em outro computador, mas deve exportar o certificado assinado com a chave privada e importá-lo para o proxy inverso após tê-lo recebido da autoridade de certificação pública.</span><span class="sxs-lookup"><span data-stu-id="ecfee-140">You create a request on another computer, but you must export the signed certificate with the private key and import it onto the reverse proxy once you have received it from the public certification authority.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="ecfee-141">Uma solicitação de certificado ou um CSR (solicitação de assinatura de certificado) é uma solicitação para uma autoridade de certificação pública (CA) confiável para validar e assinar a chave pública do computador solicitante.</span><span class="sxs-lookup"><span data-stu-id="ecfee-141">A certificate request or a certificate signing request (CSR) is a request to a trusted public certification authority (CA) to validate and sign the requesting computer’s public key.</span></span> <span data-ttu-id="ecfee-142">Quando um certificado é gerado, uma chave pública e uma chave privada são criadas.</span><span class="sxs-lookup"><span data-stu-id="ecfee-142">When a certificate is generated, a public key and a private key are created.</span></span> <span data-ttu-id="ecfee-143">Somente a chave pública é compartilhada e assinada.</span><span class="sxs-lookup"><span data-stu-id="ecfee-143">Only the public key is shared and signed.</span></span> <span data-ttu-id="ecfee-144">Como o nome indica, a chave pública é disponibilizada para qualquer solicitação Pública.</span><span class="sxs-lookup"><span data-stu-id="ecfee-144">As the name implies, the public key is made available to any public request.</span></span> <span data-ttu-id="ecfee-145">A chave pública é usada por clientes, servidores e outros solicitantes que precisam trocar informações com segurança e validar a identidade do computador.</span><span class="sxs-lookup"><span data-stu-id="ecfee-145">The public key is for use by clients, servers and other requesters that need to exchange information securely and validate a computer’s identity.</span></span> <span data-ttu-id="ecfee-146">A chave privada é mantida protegida e é usada somente pelo computador que criou o par de chaves para descriptografar mensagens criptografadas com sua chave pública.</span><span class="sxs-lookup"><span data-stu-id="ecfee-146">The private key is kept secured and is used only by the computer that created the key pair to decrypt messages encrypted with its public key.</span></span> <span data-ttu-id="ecfee-147">A chave privada pode ser usada para outras finalidades.</span><span class="sxs-lookup"><span data-stu-id="ecfee-147">The private key can be used for other purposes.</span></span> <span data-ttu-id="ecfee-148">Para fins de proxy reverso, a codificação de dados é o uso principal.</span><span class="sxs-lookup"><span data-stu-id="ecfee-148">For reverse proxy purposes, data encipherment is the primary use.</span></span> <span data-ttu-id="ecfee-149">O secondarily, a autenticação de certificado no nível da chave do certificado, é limitado apenas à validação de que um solicitante tem a chave pública do computador ou de que o computador com o qual você tem uma chave pública é realmente o computador que ele alega ser.</span><span class="sxs-lookup"><span data-stu-id="ecfee-149">Secondarily, the certificate authentication at the certificate key level is another use, and is limited only to validation that a requester has the computer’s public key, or that the computer that you have a public key for is actually the computer that it claims to be.</span></span>



</div>

<div>


> [!TIP]
> <span data-ttu-id="ecfee-150">Se você planejar os certificados do servidor de borda e os certificados de proxy inversos ao mesmo tempo, observe que há uma excelente semelhança entre os dois requisitos de certificado.</span><span class="sxs-lookup"><span data-stu-id="ecfee-150">If you plan your Edge Server certificates and your reverse proxy certificates at the same time, you should notice that there is a great deal of similarity between the two certificate requirements.</span></span> <span data-ttu-id="ecfee-151">Ao configurar e solicitar o certificado do servidor de borda, combine o servidor de borda e os nomes alternativos de entidades de proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="ecfee-151">When you configure and request your Edge Server certificate, combine the Edge Server and the reverse proxy subject alternative names.</span></span> <span data-ttu-id="ecfee-152">Você pode usar o mesmo certificado para seu proxy reverso se exportar o certificado e a chave privada e copiar o arquivo exportado para o proxy reverso e, em seguida, importar o par de certificados/chaves e atribuí-lo conforme necessário nos procedimentos futuros.</span><span class="sxs-lookup"><span data-stu-id="ecfee-152">You can use the same certificate for your reverse proxy if you export the certificate and the private key and copy the exported file to the reverse proxy and then import the certificate/key pair and assign it as needed in the upcoming procedures.</span></span> <span data-ttu-id="ecfee-153">Consulte os requisitos de certificado para o plano do servidor de borda &nbsp; <A href="lync-server-2013-plan-for-edge-server-certificates.md">para certificados do servidor de borda no lync Server 2013</A> e o resumo de certificado de proxy reverso <A href="lync-server-2013-certificate-summary-reverse-proxy.md">-proxy reverso no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ecfee-153">Refer to the certificate requirements for the Edge Server&nbsp;<A href="lync-server-2013-plan-for-edge-server-certificates.md">Plan for Edge Server certificates in Lync Server 2013</A> and the reverse proxy <A href="lync-server-2013-certificate-summary-reverse-proxy.md">Certificate summary - Reverse proxy in Lync Server 2013</A>.</span></span> <span data-ttu-id="ecfee-154">Certifique-se de criar o certificado com uma chave privada exportável.</span><span class="sxs-lookup"><span data-stu-id="ecfee-154">Make sure that you create the certificate with an exportable private key.</span></span> <span data-ttu-id="ecfee-155">A criação do certificado e da solicitação de certificado com uma chave privada exportável é necessária para servidores de borda em pool, portanto, isso é uma prática normal e o assistente de certificado no assistente de implantação do Lync Server para o servidor de borda permite que você defina o sinalizador <STRONG>criar chave privada exportável</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ecfee-155">Creating the certificate and certificate request with an exportable private key is required for pooled Edge Servers, so this is a normal practice and the Certificate Wizard in the Lync Server Deployment Wizard for the Edge Server will allow you to set the <STRONG>Make private key exportable</STRONG> flag.</span></span> <span data-ttu-id="ecfee-156">Depois de receber a solicitação de certificado de volta da autoridade de certificação pública, você exportará o certificado e a chave privada.</span><span class="sxs-lookup"><span data-stu-id="ecfee-156">Once you receive the certificate request back from the public certification authority, you will export the certificate and the private key.</span></span> <span data-ttu-id="ecfee-157">Consulte a seção "para exportar o certificado com a chave privada para servidores de borda em um pool" no tópico <A href="lync-server-2013-set-up-certificates-for-the-external-edge-interface.md">configurar certificados para a interface de borda externa do Lync Server 2013</A> para obter detalhes sobre como criar e exportar seu certificado com uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="ecfee-157">See the section “To export the certificate with the private key for Edge Servers in a pool” in the topic <A href="lync-server-2013-set-up-certificates-for-the-external-edge-interface.md">Set up certificates for the external edge interface for Lync Server 2013</A> for details on how to create and export your certificate with a private key.</span></span> <span data-ttu-id="ecfee-158">A extensão do certificado deve ser do tipo <STRONG>. pfx</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ecfee-158">The extension of the certificate should be of type <STRONG>.pfx</STRONG>.</span></span>



</div>

<span data-ttu-id="ecfee-159">Para gerar uma solicitação de assinatura de certificado no computador em que o certificado e a chave privada serão atribuídos, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ecfee-159">To generate a certificate signing request on the computer where the certificate and private key will be assigned, you do the following:</span></span>

<span data-ttu-id="ecfee-160">**Criando uma solicitação de assinatura de certificado**</span><span class="sxs-lookup"><span data-stu-id="ecfee-160">**Creating a certificate signing request**</span></span>

1.  <span data-ttu-id="ecfee-161">Abra o console de gerenciamento Microsoft (MMC) e adicione o snap-in de certificados e selecione **computadores** e, em seguida, expanda **pessoal**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-161">Open the Microsoft Management Console (MMC) and add the Certificates snap-in and select **Computers**, then expand **Personal**.</span></span> <span data-ttu-id="ecfee-162">Para obter detalhes sobre como criar um console de certificados no console de gerenciamento Microsoft (MMC), consulte [https://go.microsoft.com/fwlink/?LinkId=282616](https://go.microsoft.com/fwlink/?linkid=282616) .</span><span class="sxs-lookup"><span data-stu-id="ecfee-162">For details on how to create a certificates console in the Microsoft Management Console (MMC), see [https://go.microsoft.com/fwlink/?LinkId=282616](https://go.microsoft.com/fwlink/?linkid=282616).</span></span>

2.  <span data-ttu-id="ecfee-163">Clique com o botão direito do mouse em **certificados**, clique em **todas as tarefas**, clique em **operações avançadas**, clique em **criar solicitação personalizada**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-163">Right-click **Certificates**, click **All Tasks**, click **Advanced Operations**, click **Create Custom Request**.</span></span>

3.  <span data-ttu-id="ecfee-164">Na página **registro de certificado** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-164">On the **Certificate Enrollment** page, click **Next**.</span></span>

4.  <span data-ttu-id="ecfee-165">Na página **selecionar política de registro de certificado** em **solicitação personalizada**, selecione **continuar sem política de registro**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-165">On the **Select Certificate Enrollment Policy** page under **Custom Request**, select **Proceed without enrollment policy**.</span></span> <span data-ttu-id="ecfee-166">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-166">Click **Next**.</span></span>

5.  <span data-ttu-id="ecfee-167">Na página **solicitação personalizada** , em **modelo** , selecione **(nenhum modelo) chave herdada**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-167">On the **Custom Request** page, for **Template** select **(No template) Legacy key**.</span></span> <span data-ttu-id="ecfee-168">A menos que seja direcionado de outra forma pelo seu provedor de certificado, deixe a opção **suprimir extensões padrão** desmarcada e a seleção de **formato de solicitação** em **PKCS \# 10**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-168">Unless otherwise directed by your certificate provider, leave **Suppress default extensions** unchecked and the **Request format** selection on **PKCS \#10**.</span></span> <span data-ttu-id="ecfee-169">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-169">Click **Next**.</span></span>

6.  <span data-ttu-id="ecfee-170">Na página **informações do certificado** , clique em **detalhes** e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-170">On the **Certificate Information** page, click **Details**, then click **Properties**.</span></span>

7.  <span data-ttu-id="ecfee-171">Na página **Propriedades do certificado** , na guia **geral** , no campo **nome amigável** , digite um nome para este certificado.</span><span class="sxs-lookup"><span data-stu-id="ecfee-171">On the **Certificate Properties** page on the **General** tab in the **Friendly Name** field, type a name for this certificate.</span></span> <span data-ttu-id="ecfee-172">Opcionalmente, digite uma descrição no campo **Descrição** .</span><span class="sxs-lookup"><span data-stu-id="ecfee-172">Optionally, type a description in the **Description** field.</span></span> <span data-ttu-id="ecfee-173">O nome amigável e a descrição geralmente são usados pelo administrador para identificar qual é a finalidade do certificado, como **ouvinte de proxy reverso para o Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-173">The Friendly Name and description are typically used by the Administrator to identify what the certificate purpose is, such as **Reverse Proxy Listener for Lync Server**.</span></span>

8.  <span data-ttu-id="ecfee-174">Selecione a guia **assunto** . Em **nome do assunto** do **tipo**, selecione **nome comum** para o tipo de nome do assunto.</span><span class="sxs-lookup"><span data-stu-id="ecfee-174">Select the **Subject** tab. Under **Subject name** for the **Type**, select **Common name** for the Subject name type.</span></span> <span data-ttu-id="ecfee-175">Para o **valor**, digite o nome do requerente que você usará para o proxy reverso e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-175">For the **Value**, type the subject name that you will use for the reverse proxy, and then click **Add**.</span></span> <span data-ttu-id="ecfee-176">No exemplo fornecido na tabela deste tópico, o nome do assunto é webext.contoso.com e seria digitado no campo valor para o nome do assunto.</span><span class="sxs-lookup"><span data-stu-id="ecfee-176">In the example provided in the table in this topic, the subject name is webext.contoso.com and would be typed into the Value field for the Subject name.</span></span>

9.  <span data-ttu-id="ecfee-177">Na guia **assunto** em **nome alternativo**, selecione **DNS** na lista suspensa para o **tipo**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-177">On the **Subject** tab under **Alternative name**, select **DNS** from the drop down for **Type**.</span></span> <span data-ttu-id="ecfee-178">Para cada nome alternativo de assunto definido que você precisa no certificado, digite o nome de domínio totalmente qualificado e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-178">For each defined subject alternative name that you require on the certificate, type the fully qualified domain name, then click **Add**.</span></span> <span data-ttu-id="ecfee-179">Por exemplo, na tabela, há três nomes alternativos de entidades, meet.contoso.com, dialin.contoso.com e lyncdiscover.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ecfee-179">For example, in the table there are three subject alternative names, meet.contoso.com, dialin.contoso.com, and lyncdiscover.contoso.com.</span></span> <span data-ttu-id="ecfee-180">No campo **valor** , digite Meet.contoso.com e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-180">In the **Value** field, type meet.contoso.com, then click **Add**.</span></span> <span data-ttu-id="ecfee-181">Repita para cada assunto nomes alternativos que você precisa definir.</span><span class="sxs-lookup"><span data-stu-id="ecfee-181">Repeat for each subject alternative names that you need to define.</span></span>

10. <span data-ttu-id="ecfee-182">Na página **Propriedades do certificado** , clique na guia **extensões** . Nesta página, você definirá os objetivos da chave criptográfica em **uso da chave** e o uso estendido da chave em **uso estendido da chave (políticas de aplicativo)**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-182">On the **Certificate Properties** page, click the **Extensions** tab. On this page, you will define the cryptographic key purposes in **Key usage** and the extended key usage in **Extended Key Usage (application policies)**.</span></span>

11. <span data-ttu-id="ecfee-183">Clique na seta **uso da chave** para mostrar as **opções disponíveis**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-183">Click the **Key usage** arrow to show the **Available options**.</span></span> <span data-ttu-id="ecfee-184">Em opções disponíveis, clique em **assinatura digital** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-184">Under Available options, click **Digital signature**, then click **Add**.</span></span> <span data-ttu-id="ecfee-185">Clique em **codificação de chave** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-185">Click **Key encipherment**, then click **Add**.</span></span> <span data-ttu-id="ecfee-186">Se a caixa de seleção **fazer com que esses usos de chave críticos** estiver desmarcada, marque a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="ecfee-186">If the checkbox for **Make these key usages critical** is unchecked, select the checkbox.</span></span>

12. <span data-ttu-id="ecfee-187">Clique na seta **uso estendido da chave (políticas do aplicativo)** para mostrar as **opções disponíveis**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-187">Click the **Extended Key Usage (application policies)** arrow to show the **Available options**.</span></span> <span data-ttu-id="ecfee-188">Em opções disponíveis, clique em **autenticação do servidor** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-188">Under Available options, click **Server Authentication**, then click **Add**.</span></span> <span data-ttu-id="ecfee-189">Clique em **autenticação do cliente** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-189">Click **Client Authentication**, then click **Add**.</span></span> <span data-ttu-id="ecfee-190">Se a caixa de seleção para fazer com que **os usos da chave estendida** forem marcada, desmarque a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="ecfee-190">If the check box for **Make the Extended Key Usages critical** is checked, unselect the checkbox.</span></span> <span data-ttu-id="ecfee-191">Ao contrário da caixa de seleção uso da chave (que deve ser marcada), você deve ter certeza de que a caixa de seleção uso estendido da chave não está marcada.</span><span class="sxs-lookup"><span data-stu-id="ecfee-191">Contrary to the Key usage checkbox (which must be checked) you must be sure that the Extended Key Usage checkbox is not checked.</span></span>

13. <span data-ttu-id="ecfee-192">Na página **Propriedades do certificado** , clique na guia **chave privada** . Clique na seta de **Opções de tecla** .</span><span class="sxs-lookup"><span data-stu-id="ecfee-192">On the **Certificate Properties** page, click the **Private Key** tab. Click the **Key options** arrow.</span></span> <span data-ttu-id="ecfee-193">Em **tamanho da chave**, selecione **2048** na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="ecfee-193">For **Key size**, select **2048** from the drop down.</span></span> <span data-ttu-id="ecfee-194">Se você estiver gerando este par de chaves e o CSR em um computador diferente do proxy inverso ao qual esse certificado se destina, selecione **tornar a chave privada exportável**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-194">If you are generating this key pair and CSR on a computer other than the reverse proxy that this certificate is intended for, select **Make private key exportable**.</span></span>
    
    <div>
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg398321.security(OCS.15).gif" title="segurança" alt="security" /><span data-ttu-id="ecfee-196">Observação de segurança:</span><span class="sxs-lookup"><span data-stu-id="ecfee-196">Security Note:</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="ecfee-197">Selecionar <strong>tornar uma chave privada exportável</strong> geralmente é avisado quando você tem mais de um proxy reverso em um farm, pois você copiará o certificado e a chave privada para cada máquina no farm.</span><span class="sxs-lookup"><span data-stu-id="ecfee-197">Selecting <strong>Make a private key exportable</strong> is generally advised when you have more than one reverse proxy in a farm because you will copy the certificate and the private key to each machine in the farm.</span></span> <span data-ttu-id="ecfee-198">Se você permitir uma chave privada exportável, deve tomar cuidado com o certificado e o computador em que ele é gerado.</span><span class="sxs-lookup"><span data-stu-id="ecfee-198">If you do allow for an exportable private key, you must take extra care with the certificate and the computer that it is generated on.</span></span> <span data-ttu-id="ecfee-199">A chave privada, se comprometida, tornará o certificado inútil, bem como exporá potencialmente o computador ou computadores a acesso externo e outras vulnerabilidades de segurança.</span><span class="sxs-lookup"><span data-stu-id="ecfee-199">The private key, if compromised, will render the certificate useless as well as potentially expose the computer or computers to external access and other security vulnerabilities.</span></span></td>
    </tr>
    </tbody>
    </table>
    
    </div>

14. <span data-ttu-id="ecfee-200">Na guia **chave privada** , clique na seta **tipo de chave** .</span><span class="sxs-lookup"><span data-stu-id="ecfee-200">On the **Private Key** tab, click the **Key type** arrow.</span></span> <span data-ttu-id="ecfee-201">Selecione a opção **Exchange** .</span><span class="sxs-lookup"><span data-stu-id="ecfee-201">Select the **Exchange** option.</span></span>

15. <span data-ttu-id="ecfee-202">Clique em **OK** para salvar as **Propriedades de certificado** que você definiu.</span><span class="sxs-lookup"><span data-stu-id="ecfee-202">Click **OK** to save the **Certificate Properties** that you have set.</span></span>

16. <span data-ttu-id="ecfee-203">Na página **registro de certificado** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-203">On the **Certificate Enrollment** page, click **Next**.</span></span>

17. <span data-ttu-id="ecfee-204">Na página **onde você deseja salvar a solicitação offline?** , você será solicitado a fornecer um **nome de arquivo** e um formato de **arquivo** para salvar a solicitação de assinatura de certificado.</span><span class="sxs-lookup"><span data-stu-id="ecfee-204">On the **Where do you want to save the offline request?** page, you are prompted for a **File Name** and a **File Format** for saving the certificate signing request.</span></span>

18. <span data-ttu-id="ecfee-205">No campo de entrada **nome do arquivo** , digite um caminho e um nome de arquivo para a solicitação ou clique em **procurar** para selecionar um local para o arquivo e digite o nome do arquivo para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ecfee-205">In the **File Name** entry field, type a path and filename for the request, or click **Browse** to select a location for the file and type the filename for the request.</span></span>

19. <span data-ttu-id="ecfee-206">Em **formato de arquivo**, clique em **base 64** ou **binário**.</span><span class="sxs-lookup"><span data-stu-id="ecfee-206">For **File format**, click either **Base 64** or **Binary**.</span></span> <span data-ttu-id="ecfee-207">Selecione **Base 64** , a menos que você seja instruído de outra forma pelo fornecedor dos seus certificados.</span><span class="sxs-lookup"><span data-stu-id="ecfee-207">Select **Base 64** unless you are instructed otherwise by the vendor for your certificates.</span></span>

20. <span data-ttu-id="ecfee-208">Localize o arquivo de solicitação que você salvou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="ecfee-208">Locate the request file that you saved in the previous step.</span></span> <span data-ttu-id="ecfee-209">Envie à sua autoridade de certificação pública.</span><span class="sxs-lookup"><span data-stu-id="ecfee-209">Submit to your public certification authority.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="ecfee-210">A Microsoft identificou CAs públicas que atendem aos requisitos para fins de comunicação unificada.</span><span class="sxs-lookup"><span data-stu-id="ecfee-210">Microsoft has identified Public CAs that meets the requirements for Unified Communications purposes.</span></span> <span data-ttu-id="ecfee-211">Uma lista é mantida no seguinte artigo da base de dados de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="ecfee-211">A list is maintained in the following knowledge base article.</span></span> <A href="https://go.microsoft.com/fwlink/?linkid=282625">https://go.microsoft.com/fwlink/?LinkId=282625</A>

    
    <span data-ttu-id="ecfee-212"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ecfee-212"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

