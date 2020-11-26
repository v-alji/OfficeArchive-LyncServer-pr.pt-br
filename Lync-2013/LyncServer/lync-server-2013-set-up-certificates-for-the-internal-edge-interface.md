---
title: 'Lync Server 2013: Configurar certificados para a interface de borda interna'
description: 'Lync Server 2013: configurar certificados para a interface de borda interna.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the internal edge interface
ms:assetid: a1963cc9-87c5-4935-86c0-6bedc6afd0ac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412750(v=OCS.15)
ms:contentKeyID: 48184949
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 52473069735d4f48c247367194139c479e71293f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423994"
---
# <a name="set-up-certificates-for-the-internal-edge-interface-in-lync-server-2013"></a><span data-ttu-id="dd7a9-103">Configurar certificados para a interface de borda interna no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd7a9-103">Set up certificates for the internal edge interface in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd7a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd7a9-104">

<span> </span></span></span>

<span data-ttu-id="dd7a9-105">_**Tópico da última modificação:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="dd7a9-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="dd7a9-106">Ao executar o assistente de certificado, certifique-se de que você esteja conectado usando uma conta que seja membro de um grupo que tenha recebido as permissões apropriadas para o tipo de modelo de certificado que você vai usar.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-106">When you run the Certificate Wizard, ensure that you are logged in using an account that is a member of a group that has been assigned the appropriate permissions for the type of certificate template you will use.</span></span> <span data-ttu-id="dd7a9-107">Por padrão, uma solicitação de certificado do Lync Server 2013 usará o modelo de certificado de servidor Web.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-107">By default, a Lync Server 2013 certificate request will use the Web Server certificate template.</span></span> <span data-ttu-id="dd7a9-108">Se você usar uma conta que seja um membro do grupo RTCUniversalServerAdmins para solicitar um certificado usando esse modelo, verifique se o grupo recebeu as permissões de Registro necessárias para usar esse modelo.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-108">If you use an account that is a member of the RTCUniversalServerAdmins group to request a certificate using this template, verify that the group has been assigned the Enroll permissions required to use that template.</span></span>



</div>

<span data-ttu-id="dd7a9-109">É necessário um único certificado na interface interna de cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-109">A single certificate is required on the internal interface of each Edge Server.</span></span> <span data-ttu-id="dd7a9-110">Certificados para a interface interna podem ser emitidos por uma CA (autoridade de certificação) corporativa interna ou uma CA pública.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-110">Certificates for the internal interface can be issued by an internal enterprise certification authority (CA) or a public CA.</span></span> <span data-ttu-id="dd7a9-111">Se a sua organização tiver uma CA interna implantada, você poderá economizar na despesa de usar certificados públicos usando a CA interna para emitir o certificado para a interface interna.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-111">If your organization has an internal CA deployed you can save on the expense of using public certificates by using the internal CA to issue the certificate for the internal interface.</span></span> <span data-ttu-id="dd7a9-112">Você pode usar uma CA interna do Windows Server 2008 ou uma autoridade de certificação do Windows Server 2008 R2 para criar esses certificados.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-112">You can use an internal Windows Server 2008 CA or Windows Server 2008 R2 CA to create these certificates.</span></span>

<span data-ttu-id="dd7a9-113">Para obter detalhes sobre esse e outros requisitos de certificado, consulte [requisitos de certificado para acesso de usuários externos no Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-113">For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span></span>

<span data-ttu-id="dd7a9-114">Para configurar certificados na interface de borda interna em um site, use os procedimentos desta seção para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-114">To set up certificates on the internal edge interface at a site, use the procedures in this section to do the following:</span></span>

1.  <span data-ttu-id="dd7a9-115">Baixe a cadeia de certificação da CA para a interface interna para cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-115">Download the CA certification chain for the internal interface to each Edge Server.</span></span>

2.  <span data-ttu-id="dd7a9-116">Importar a cadeia de certificação da CA para a interface interna, em cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-116">Import the CA certification chain for the internal interface, on each Edge Server.</span></span>

3.  <span data-ttu-id="dd7a9-117">Crie a solicitação de certificado para a interface interna, em um servidor de borda, chamado de primeiro servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-117">Create the certificate request for the internal interface, on one Edge Server, called the first Edge Server.</span></span>

4.  <span data-ttu-id="dd7a9-118">Importar o certificado para a interface interna no primeiro servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-118">Import the certificate for the internal interface on the first Edge Server.</span></span>

5.  <span data-ttu-id="dd7a9-119">Importar o certificado nos outros servidores de borda neste site (ou implantado atrás deste balanceador de carga).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-119">Import the certificate on the other Edge Servers at this site (or deployed behind this load balancer).</span></span>

6.  <span data-ttu-id="dd7a9-120">Atribua o certificado para a interface interna de cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-120">Assign the certificate for the internal interface of every Edge Server.</span></span>

<span data-ttu-id="dd7a9-121">Se você tiver mais de um site com servidores de borda (ou seja, uma topologia de borda de vários sites) ou conjuntos separados de servidores de Borda implantados por meio de balanceadores de carga diferentes, você precisará seguir estas etapas para cada site que tenha servidores de borda e para cada conjunto de servidores de Borda implantados atrás de um balanceador de carga diferente.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-121">If you have more than one site with Edge Servers (that is, a multiple-site edge topology), or separate sets of Edge Servers deployed behind different load balancers, you need to follow these steps for each site that has Edge Servers, and for each set of Edge Servers deployed behind a different load balancer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dd7a9-122">As etapas para procedimentos nesta seção se baseiam no uso de uma autoridade de certificação do Windows Server &nbsp; 2008, do Windows server 2008 R2, da autoridade de certificação &nbsp; &nbsp; do Windows Server 2012 ou da autoridade de certificação do Windows Server 2012 R2 para criar um certificado para cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-122">The steps for procedures in this section are based on using a Windows Server&nbsp;2008 CA, Windows Server&nbsp;2008&nbsp;R2 CA, Windows Server 2012 CA, or Windows Server 2012 R2 CA to create a certificate for each Edge Server.</span></span> <span data-ttu-id="dd7a9-123">Para obter orientação passo a passo para qualquer outra autoridade de certificação, consulte a documentação dessa CA.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-123">For step-by-step guidance for any other CA, consult the documentation for that CA.</span></span> <span data-ttu-id="dd7a9-124">Por padrão, todos os usuários autenticados têm os direitos de usuário adequados para solicitar certificados.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-124">By default, all authenticated users have the appropriate user rights to request certificates.</span></span><BR><span data-ttu-id="dd7a9-125">Os procedimentos desta seção se baseiam na criação de solicitações de certificado no servidor de borda como parte do processo de implantação do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-125">The procedures in this section are based on creating certificate requests on the Edge Server as part of the Edge Server deployment process.</span></span> <span data-ttu-id="dd7a9-126">É possível criar solicitações de certificado usando o servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-126">It is possible to create certificate requests using the Front End Server.</span></span> <span data-ttu-id="dd7a9-127">Você pode fazer isso para concluir a solicitação de certificado no início do processo de planejamento e implantação antes de iniciar a implantação dos servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-127">You can do this to complete the certificate request early in the planning and deployment process, before you start deployment of the Edge Servers.</span></span> <span data-ttu-id="dd7a9-128">Para fazer isso, você deve certificar-se de que o certificado que você solicitou está definido com uma chave privada exportável.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-128">To do this, you must ensure that the certificate you request is defined with an exportable private key.</span></span><BR><span data-ttu-id="dd7a9-129">Os procedimentos desta seção descrevem o uso de um arquivo. cer e de um arquivo. p7b para o certificado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-129">The procedures in this section describe using a .cer and a .p7b file for the certificate.</span></span> <span data-ttu-id="dd7a9-130">Se você usar um tipo de arquivo diferente, modifique esses procedimentos conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-130">If you use a different type of file, modify these procedures as appropriate.</span></span>



</div>

<div>

## <a name="to-download-the-ca-certification-chain-for-the-internal-interface-using-certsrv-web-site"></a><span data-ttu-id="dd7a9-131">Para baixar a cadeia de certificação CA para a interface interna usando o site do certsrv</span><span class="sxs-lookup"><span data-stu-id="dd7a9-131">To download the CA certification chain for the internal interface using certsrv Web site</span></span>

1.  <span data-ttu-id="dd7a9-132">Faça logon em um servidor do Lync Server 2013 na rede interna (ou seja, não no servidor de borda) como membro do grupo **Administradores** .</span><span class="sxs-lookup"><span data-stu-id="dd7a9-132">Log on to an Lync Server 2013 server in the internal network (that is, not the Edge Server) as a member of the **Administrators** group.</span></span>

2.  <span data-ttu-id="dd7a9-133">Execute o seguinte comando em um prompt de comando clicando em **Iniciar**, em **executar** e, em seguida, digitando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-133">Run the following command at a command prompt by clicking **Start**, clicking **Run**, and then typing the following:</span></span>
    
        https://<name of your Issuing CA Server>/certsrv
    
    <span data-ttu-id="dd7a9-134">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-134">For example:</span></span>
    
        https://ca01.contoso.net/certsrv
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dd7a9-135">Se estiver usando uma autoridade de certificação empresarial do Windows Server 2008 ou do Windows Server 2008 R2, você deve usar HTTPS, não http.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-135">If you are using a Windows Server 2008 or Windows Server 2008 R2 enterprise CA, you must use https, not http.</span></span>

    
    </div>

3.  <span data-ttu-id="dd7a9-136">Na página web certsrv da AC emissora, em  **Selecione uma tarefa**, clique em **Download de um Certificado de Autoridade de Certificação, Cadeia de Certificados ou Lista de Certificados Revogados**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-136">On the issuing CA’s certsrv web page, under **Select a task**, click **Download a CA certificate, certificate chain, or CRL**.</span></span>

4.  <span data-ttu-id="dd7a9-137">Em **baixar um certificado de autoridade de certificação, uma cadeia de certificados ou uma CRL**, clique em **baixar cadeia de certificados da CA**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-137">Under **Download a CA Certificate, Certificate Chain, or CRL**, click **Download CA certificate chain**.</span></span>

5.  <span data-ttu-id="dd7a9-138">Na caixa de diálogo **download de arquivo** , clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-138">In the **File Download** dialog box, click **Save**.</span></span>

6.  <span data-ttu-id="dd7a9-139">Salve o arquivo. p7b na unidade de disco rígido no servidor e copie-o para uma pasta em cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-139">Save the .p7b file to the hard disk drive on the server, and then copy it to a folder on each Edge Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dd7a9-140">O arquivo. p7b contém todos os certificados que estão no caminho de certificação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-140">The .p7b file contains all of the certificates that are in the certification path.</span></span> <span data-ttu-id="dd7a9-141">Para exibir o caminho de certificação, abra o certificado do servidor e clique no caminho de certificação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-141">To view the certification path, open the server certificate and click the certification path.</span></span>

    
    </div>

</div>

<div>

## <a name="to-export-the-ca-certification-chain-for-the-internal-interface-using-mmc"></a><span data-ttu-id="dd7a9-142">Para exportar a cadeia de certificação da CA para a interface interna usando o MMC</span><span class="sxs-lookup"><span data-stu-id="dd7a9-142">To export the CA certification chain for the internal interface using MMC</span></span>

1.  <span data-ttu-id="dd7a9-143">Você pode exportar o certificado raiz da autoridade de certificação de qualquer computador ingressado no domínio usando o console de gerenciamento Microsoft (MMC).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-143">You can export the CA root certificate from any domain joined machine using the Microsoft Management Console (MMC).</span></span> <span data-ttu-id="dd7a9-144">Clique em **Iniciar**, clique em **executar** e digite **MMC**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-144">Click **Start**, click **Run**, and then type **MMC**.</span></span>

2.  <span data-ttu-id="dd7a9-145">No console MMC, clique em **arquivo**, clique em **Adicionar/remover**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-145">In the MMC console, click **File**, click **Add/Remove**.</span></span>

3.  <span data-ttu-id="dd7a9-146">Na lista de diálogo **Adicionar ou remover snap-ins** , selecione **certificados** e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-146">From the **Add or Remove Snap-ins** dialog list, select **Certificates**, then click **Add**.</span></span> <span data-ttu-id="dd7a9-147">Quando solicitado, selecione **conta do computador**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-147">When prompted, select **Computer Account**.</span></span> <span data-ttu-id="dd7a9-148">Na caixa de diálogo **Selecionar Computador**, selecione **Computador Local**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-148">On the **Select Computer** dialog, select **Local Computer**.</span></span> <span data-ttu-id="dd7a9-149">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-149">Click **Finish**.</span></span> <span data-ttu-id="dd7a9-150">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-150">Click **OK**.</span></span>

4.  <span data-ttu-id="dd7a9-151">Expanda **Certificates (computador local)**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-151">Expand **Certificates (Local Computer)**.</span></span> <span data-ttu-id="dd7a9-152">Expanda **autoridades de certificação raiz confiáveis**, selecione **certificados**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-152">Expand **Trusted Root Certification Authorities**, select **Certificates**.</span></span>

5.  <span data-ttu-id="dd7a9-153">Clique no certificado raiz emitido por sua AC.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-153">Click the root certificate issued by your CA.</span></span> <span data-ttu-id="dd7a9-154">Clique com o botão direito do mouse no certificado, selecione **todas as tarefas**, selecione **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-154">Right click the certificate, select **All Tasks**, select **Export**.</span></span> <span data-ttu-id="dd7a9-155">O **Assistente para exportação de certificados** será aberto.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-155">The **Certificate Export Wizard** will open.</span></span>

6.  <span data-ttu-id="dd7a9-156">No **Assistente de Exportação de Certificado**, clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-156">In the **Certificate Export Wizard**, click **Next**.</span></span>

7.  <span data-ttu-id="dd7a9-157">Na caixa de diálogo **exportar formato de arquivo** , selecione um formato para o qual exportar.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-157">On the **Export File Format** dialog, select a format to export to.</span></span> <span data-ttu-id="dd7a9-158">Recomendamos o **padrão de sintaxe da mensagem criptográfica – \# Certificados PKCS 7 (. P7B)**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-158">We recommend the **Cryptographic Message Syntax Standard – PKCS \#7 Certificates (.P7B)**.</span></span> <span data-ttu-id="dd7a9-159">Se você selecionar o **padrão de sintaxe da mensagem criptográfica – \# Certificados PKCS 7 (. P7B)**, marque a caixa de seleção **incluir todos os certificados no caminho de certificação, se possível** , para exportar a cadeia de certificados, incluindo o certificado da CA raiz e qualquer certificado de autoridade de certificação intermediário.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-159">If you select the **Cryptographic Message Syntax Standard – PKCS \#7 Certificates (.P7B)**, select the **Include all certificates in the certification path if possible** checkbox to export the certificate chain, including the root CA certificate and any Intermediate CA certificates.</span></span> <span data-ttu-id="dd7a9-160">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-160">Click **Next**.</span></span>

8.  <span data-ttu-id="dd7a9-161">Na caixa de diálogo **arquivo para exportação** na entrada nome do arquivo, digite um nome de caminho e arquivo (extensão padrão é. p7b) para o certificado exportado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-161">On the **File to Export** dialog in the file name entry, type a path and file name (default extension is .p7b) for the exported certificate.</span></span> <span data-ttu-id="dd7a9-162">Opcionalmente, clique em **procurar**, localize um diretório para colocar o certificado exportado e forneça um nome para o certificado exportado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-162">Optionally, click **Browse**, locate a directory to place the exported certificate in and provide a name for the exported certificate.</span></span> <span data-ttu-id="dd7a9-163">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-163">Click **Save**.</span></span> <span data-ttu-id="dd7a9-164">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-164">Click **Next**.</span></span>

9.  <span data-ttu-id="dd7a9-165">Examine o resumo de ações e clique em **concluir** para concluir a exportação do certificado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-165">Review the summary of actions, and click **Finish** to complete the export of the certificate.</span></span> <span data-ttu-id="dd7a9-166">Clique em **OK** para confirmar que a exportação foi bem sucedida.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-166">Click **OK** to confirm the successful export.</span></span>

</div>

<div>

## <a name="to-import-the-ca-certification-chain-for-the-internal-interface"></a><span data-ttu-id="dd7a9-167">Para importar a cadeia de certificação da CA para a interface interna</span><span class="sxs-lookup"><span data-stu-id="dd7a9-167">To import the CA certification chain for the internal interface</span></span>

1.  <span data-ttu-id="dd7a9-168">Em cada servidor de borda, abra o MMC (console de gerenciamento Microsoft) clicando em **Iniciar**, clicando em **executar**, digitando **MMC** na caixa **abrir** e, em seguida, clicando em **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-168">On each Edge Server, open the Microsoft Management Console (MMC) by clicking **Start**, clicking **Run**, typing **mmc** in the **Open** box, and then clicking **OK**.</span></span>

2.  <span data-ttu-id="dd7a9-169">No menu **arquivo** , clique em **Adicionar/remover snap-in** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-169">On the **File** menu, click **Add/Remove Snap-in**, and then click **Add**.</span></span>

3.  <span data-ttu-id="dd7a9-170">Na caixa **Adicionar Snap-ins Autônomos** , clique em **certificados** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-170">In the **Add Standalone Snap-ins** box, click **Certificates**, and then click **Add**.</span></span>

4.  <span data-ttu-id="dd7a9-171">Na caixa de diálogo  **Snap-in de certificados**, clique em  **Conta de computador** e, em seguida, clique em  **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-171">In the **Certificate snap-in** dialog box, click **Computer account**, and then click **Next**.</span></span>

5.  <span data-ttu-id="dd7a9-172">Na caixa de diálogo **Selecionar computador** , verifique se a caixa de seleção **computador local: (o computador em que este console está sendo executado)** está marcada e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-172">In the **Select Computer** dialog box, ensure that the **Local computer: (the computer this console is running on)** check box is selected, and then click **Finish**.</span></span>

6.  <span data-ttu-id="dd7a9-173">Clique em **fechar** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-173">Click **Close**, and then click **OK**.</span></span>

7.  <span data-ttu-id="dd7a9-174">Na árvore de console, expanda **certificados (computador local)**, clique com o botão direito do mouse em **autoridades de certificação raiz confiáveis**, aponte para **todas as tarefas** e, em seguida, clique em **importar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-174">In the console tree, expand **Certificates (Local Computer)**, right-click **Trusted Root Certification Authorities**, point to **All Tasks**, and then click **Import**.</span></span>

8.  <span data-ttu-id="dd7a9-175">No assistente, em **arquivo a ser importado**, especifique o nome do arquivo do certificado (ou seja, o nome que você especificou quando baixou a cadeia de certificação CA para a interface interna no procedimento anterior).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-175">In the wizard, in **File to Import**, specify the file name of the certificate (that is, the name of that you specified when you downloaded the CA certification chain for the internal interface in the previous procedure).</span></span>

9.  <span data-ttu-id="dd7a9-176">Repita esse procedimento em cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-176">Repeat this procedure on each Edge Server.</span></span>

</div>

<div>

## <a name="to-create-the-certificate-request-for-the-internal-interface"></a><span data-ttu-id="dd7a9-177">Para criar a solicitação de certificado para a interface interna</span><span class="sxs-lookup"><span data-stu-id="dd7a9-177">To create the certificate request for the internal interface</span></span>

1.  <span data-ttu-id="dd7a9-178">Em um dos servidores de borda, inicie o assistente de implantação e, em seguida, ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique em **executar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-178">On one of the Edge Servers, start the Deployment Wizard, and next to **Step 3: Request, Install, or Assign Certificates**, click **Run**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dd7a9-179">Se você tiver vários servidores de borda em um local em um pool, poderá executar o assistente de certificado em qualquer um dos servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-179">If you have multiple Edge Servers in one location in a pool, you can run the Certificate Wizard on any one of the Edge Servers.</span></span><BR><span data-ttu-id="dd7a9-180">Depois de executar a etapa 3 na primeira vez, o botão muda para <STRONG>executar novamente</STRONG>, e uma marca de seleção verde que indica que a conclusão bem-sucedida da tarefa não é exibida até que todos os certificados exijam a solicitação, instalação e atribuição.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-180">After you run Step 3 the first time, the button changes to <STRONG>Run again</STRONG>, and a green check mark that indicates successful completion of the task is not displayed until all require certificates have been requested, installed, and assigned.</span></span>

    
    </div>

2.  <span data-ttu-id="dd7a9-181">Na página **Tarefas de Certificado Disponíveis**, clique em  **Criar uma nova solicitação de certificado**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-181">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

3.  <span data-ttu-id="dd7a9-182">Na página **solicitação de certificado** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-182">On the **Certificate Request** page, click **Next**.</span></span>

4.  <span data-ttu-id="dd7a9-183">Na página  **Solicitações Atrasadas ou Imediatas**, clique em  **Preparar a solicitação agora, mas enviá-la depois**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-183">On the **Delayed or Immediate Requests** page, click **Prepare the request now, but send it later**.</span></span>

5.  <span data-ttu-id="dd7a9-184">Na página **arquivo de solicitação de certificado** , digite o caminho completo e o nome do arquivo para o qual a solicitação deve ser salva (por exemplo, **c: \\ borda interna do CERT \_ \_ . cer**).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-184">On the **Certificate Request File** page, type the full path and file name to which the request is to be saved (for example, **c:\\cert\_internal\_edge.cer**).</span></span>

6.  <span data-ttu-id="dd7a9-185">Na página **especificar modelo de certificado alternativo** , para usar um modelo diferente do modelo padrão do webserver, marque a caixa de seleção **usar modelo de certificado alternativo para a autoridade de certificação selecionada** .</span><span class="sxs-lookup"><span data-stu-id="dd7a9-185">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected Certificate Authority** check box.</span></span>

7.  <span data-ttu-id="dd7a9-186">Na página **configurações de nome e segurança** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-186">On the **Name and Security Settings** page, do the following:</span></span>
    
      - <span data-ttu-id="dd7a9-187">Em **nome amigável**, digite um nome de exibição para o certificado (por exemplo, borda interna).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-187">In **Friendly name**, type a display name for the certificate (for example, Internal Edge).</span></span>
    
      - <span data-ttu-id="dd7a9-188">Em **comprimento de bit**, especifique o comprimento do bit (geralmente, o padrão de **2048**).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-188">In **Bit length**, specify the bit length (typically, the default of **2048**).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="dd7a9-189">Comprimentos de bit mais altos oferecem mais segurança, mas têm um impacto negativo na velocidade.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-189">Higher bit lengths offer more security, but they have a negative impact on speed.</span></span>

        
        </div>
    
      - <span data-ttu-id="dd7a9-190">Se o certificado precisar ser exportável, marque a caixa de seleção **Marcar chave privada de certificado como exportável** .</span><span class="sxs-lookup"><span data-stu-id="dd7a9-190">If the certificate needs to be exportable, select the **Mark certificate private key as exportable** check box.</span></span>

8.  <span data-ttu-id="dd7a9-191">Na página **informações da organização** , digite o nome da organização e a unidade organizacional (ou) (por exemplo, uma divisão ou um departamento).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-191">On the **Organization Information** page, type the name for the organization and the organizational unit (OU) (for example, a division or department).</span></span>

9.  <span data-ttu-id="dd7a9-192">Na página **informações geográficas** , especifique as informações de localização.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-192">On the **Geographical Information** page, specify the location information.</span></span>

10. <span data-ttu-id="dd7a9-193">Na página **nome do assunto/nomes alternativos de assunto** , as informações a serem automaticamente preenchidas pelo assistente serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-193">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span>

11. <span data-ttu-id="dd7a9-194">Na página **configurar nomes alternativos de entidades adicionais** , especifique os nomes alternativos de entidades adicionais necessários.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-194">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>

12. <span data-ttu-id="dd7a9-195">Na página **Resumo da solicitação** , examine as informações do certificado que serão usadas para gerar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-195">On the **Request Summary** page, review the certificate information that is going to be used to generate the request.</span></span>

13. <span data-ttu-id="dd7a9-196">Depois que os comandos forem concluídos, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-196">After the commands complete, do the following:</span></span>
    
      - <span data-ttu-id="dd7a9-197">Para exibir o log para a solicitação de certificado, clique em **Exibir log**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-197">To view the log for the certificate request, click **View Log**.</span></span>
    
      - <span data-ttu-id="dd7a9-198">Para concluir a solicitação de certificado, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-198">To complete the certificate request, click **Next**.</span></span>

14. <span data-ttu-id="dd7a9-199">Na página **arquivo de solicitação de certificado** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-199">On the **Certificate Request File** page, do the following:</span></span>
    
      - <span data-ttu-id="dd7a9-200">Para exibir o arquivo de solicitação de assinatura de certificado (CSR) gerado, clique em **Exibir**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-200">To view the generated certificate signing request (CSR) file, click **View**.</span></span>
    
      - <span data-ttu-id="dd7a9-201">Para fechar o assistente, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-201">To close the wizard, click **Finish**.</span></span>

15. <span data-ttu-id="dd7a9-202">Envie este arquivo para a sua CA (por email ou outro método compatível com sua organização para a sua CA corporativa) e, quando você receber o arquivo de resposta, copie o novo certificado para este computador para que ele esteja disponível para importação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-202">Submit this file to your CA (by email or other method supported by your organization for your enterprise CA) and, when you receive the response file, copy the new certificate to this computer so that it is available for import.</span></span>

</div>

<div>

## <a name="to-import-the-certificate-for-the-internal-interface"></a><span data-ttu-id="dd7a9-203">Para importar o certificado para a interface interna</span><span class="sxs-lookup"><span data-stu-id="dd7a9-203">To import the certificate for the internal interface</span></span>

1.  <span data-ttu-id="dd7a9-204">Faça logon no servidor de borda em que você criou a solicitação de certificado como membro do grupo Administradores local.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-204">Log on to the Edge Server on which you created the certificate request as a member of the local Administrators group.</span></span>

2.  <span data-ttu-id="dd7a9-205">No assistente de implantação, ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique **novamente em executar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-205">In the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <span data-ttu-id="dd7a9-206">Depois de executar a etapa 3 na primeira vez, o botão muda para **executar novamente**, mas uma marca de seleção verde (indicando a conclusão bem-sucedida da tarefa) não é exibida até que todos os certificados exijam que os certificados tenham sido solicitados, instalados e atribuídos.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-206">After you run Step 3 the first time, the button changes to **Run again**, but a green check mark (indicating successful completion of the task) is not displayed until all require certificates have been requested, installed, and assigned.</span></span>

3.  <span data-ttu-id="dd7a9-207">Na página **tarefas de certificado disponíveis** , clique em **importar um certificado de a. Arquivo P7b,. pfx ou. cer**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-207">On the **Available Certificate Tasks** page, click **Import a certificate from a .P7b, .pfx or .cer file**.</span></span>

4.  <span data-ttu-id="dd7a9-208">Na página **importar certificado** , digite o caminho completo e o nome do arquivo do certificado que você solicitou e recebeu para a interface interna deste servidor de borda (ou clique em **procurar** para localizar e selecionar o arquivo).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-208">On the **Import Certificate** page, type the full path and file name of the certificate that you requested and received for the internal interface of this Edge Server (or, click **Browse** to locate and select the file).</span></span>

5.  <span data-ttu-id="dd7a9-209">Se você estiver importando certificados para outros membros do pool um certificado contendo uma chave privada, marque a caixa de seleção o **arquivo de certificado contém a chave privada da Certifcate** e especifique a senha.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-209">If you are importing certificates for other members of the pool a certificate containing a private key, select the **Certificate file contains certifcate’s private key** check box and specify the password.</span></span>

</div>

<div>

## <a name="to-export-the-certificate-with-the-private-key-for-edge-servers-in-a-pool"></a><span data-ttu-id="dd7a9-210">Para exportar o certificado com a chave privada para servidores de borda em um pool</span><span class="sxs-lookup"><span data-stu-id="dd7a9-210">To export the certificate with the private key for Edge Servers in a pool</span></span>

1.  <span data-ttu-id="dd7a9-211">Faça logon como membro do grupo Administradores para o mesmo servidor de borda no qual você importou o certificado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-211">Log on as a member of the Administrators group to the same Edge Server on which you imported the certificate.</span></span>

2.  <span data-ttu-id="dd7a9-212">Clique em **Iniciar**, clique em **executar** e digite **MMC**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-212">Click **Start**, click **Run**, and type **MMC**.</span></span>

3.  <span data-ttu-id="dd7a9-213">No console do MMC, clique em **arquivo**, clique em **Adicionar/remover snap-in**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-213">From the MMC console, click **File**, click **Add/Remove Snap-in**.</span></span>

4.  <span data-ttu-id="dd7a9-214">Na página Adicionar ou remover snap-ins, clique em **certificados** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-214">From Add or Remove Snap-ins page, click **Certificates**, click **Add**.</span></span>

5.  <span data-ttu-id="dd7a9-215">Na caixa de diálogo snap-in de certificados, selecione **conta de computador**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-215">In the Certificates snap-in dialog, select **Computer account**.</span></span> <span data-ttu-id="dd7a9-216">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-216">Click **Next**.</span></span> <span data-ttu-id="dd7a9-217">Em Selecionar computador, selecione **computador local: (o computador no qual este console está sendo executado)**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-217">In Select Computer, select **Local computer: (the computer this console is running on)**.</span></span> <span data-ttu-id="dd7a9-218">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-218">Click **Finish**.</span></span> <span data-ttu-id="dd7a9-219">Clique em **OK** para concluir a configuração do console MMC.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-219">Click **OK** to complete configuration of the MMC console.</span></span>

6.  <span data-ttu-id="dd7a9-220">Clique duas vezes em **Certificados (Computador Local)** para expandir os repositórios de certificados.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-220">Double-click **Certificates (Local Computer)** to expand the certificate stores.</span></span> <span data-ttu-id="dd7a9-221">Clique duas vezes em **pessoal** e, em seguida, clique duas vezes em **certificados**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-221">Double-click **Personal**, then double-click **Certificates**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="dd7a9-222">Se não houver certificados no armazenamento pessoal de certificados do computador local, não há uma chave privada associada ao certificado que foi importado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-222">If there are no certificates in the Certificates Personal store for the local computer, there is no private key associated with the certificate that was imported.</span></span> <span data-ttu-id="dd7a9-223">Examine as etapas de solicitação e importação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-223">Review the request and import steps.</span></span> <span data-ttu-id="dd7a9-224">Se o problema persistir, entre em contato com o administrador ou o provedor da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-224">If the problem persists, contact your certification authority administrator or provider.</span></span>

    
    </div>

7.  <span data-ttu-id="dd7a9-225">No armazenamento de certificados pessoal do computador local, clique com o botão direito do mouse no certificado que você está exportando.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-225">In the Certificates Personal store for the local computer, right-click the certificate that you are exporting.</span></span> <span data-ttu-id="dd7a9-226">Clique em **todas as tarefas**, clique em **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-226">Click **All Tasks**, click **Export**.</span></span>

8.  <span data-ttu-id="dd7a9-227">No Assistente para exportação de certificados, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-227">In the Certificate Export Wizard, click **Next**.</span></span> <span data-ttu-id="dd7a9-228">Selecione **Sim, exportar a chave privada**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-228">Select **Yes, export the private key**.</span></span> <span data-ttu-id="dd7a9-229">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-229">Click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dd7a9-230">Se a seleção <STRONG>Sim, exportar a chave privada</STRONG> não estiver disponível, a chave privada associada a esse certificado não foi marcada para exportação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-230">If the selection <STRONG>Yes, export the private key</STRONG> is not available, the private key associated with this certificate was not marked for export.</span></span> <span data-ttu-id="dd7a9-231">Você precisará solicitar o certificado novamente, certificando-se de que o certificado esteja marcado para permitir a exportação da chave privada antes de continuar com a exportação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-231">You will need to request the certificate again, ensuring that the certificate is marked to allow for the export of the private key before you can continue with the export.</span></span> <span data-ttu-id="dd7a9-232">Entre em contato com o administrador ou provedor da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-232">Contact your certification authority administrator or provider.</span></span>

    
    </div>

9.  <span data-ttu-id="dd7a9-233">Na caixa de diálogo Exportar formatos de arquivo, selecione **troca de informações pessoais – PKCS \# 12 (. PFX)** e, em seguida, selecione o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd7a9-233">On the Export File Formats dialog, select **Personal Information Exchange – PKCS\#12 (.PFX)** and then select the following:</span></span>
    
      - <span data-ttu-id="dd7a9-234">Incluir todos os certificados no caminho de certificação, se possível</span><span class="sxs-lookup"><span data-stu-id="dd7a9-234">Include all certificates in the certification path if possible</span></span>
    
      - <span data-ttu-id="dd7a9-235">Exportar todas as propriedades estendidas</span><span class="sxs-lookup"><span data-stu-id="dd7a9-235">Export all extended properties</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="dd7a9-236">Ao exportar o certificado de um servidor de borda, não selecione <STRONG>excluir a chave privada se a exportação for bem-sucedida</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-236">When exporting the certificate from an Edge server, do not select <STRONG>Delete the private key if the export is successful</STRONG>.</span></span> <span data-ttu-id="dd7a9-237">Selecionar essa opção exigirá que você importe o certificado e a chave privada para esse servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-237">Selecting this option will require that you import the certificate and the private key to this Edge server.</span></span>

        
        </div>
    
    <span data-ttu-id="dd7a9-238">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-238">Click **Next** to continue.</span></span>

10. <span data-ttu-id="dd7a9-239">Se você quiser atribuir uma senha para proteger a chave privada, digite uma senha para a chave privada.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-239">If you want to assign password to protect the private key, type a password for the private key.</span></span> <span data-ttu-id="dd7a9-240">Digite a senha novamente para confirmá-la.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-240">Re-enter the password to confirm.</span></span> <span data-ttu-id="dd7a9-241">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-241">Click **Next**.</span></span>

11. <span data-ttu-id="dd7a9-242">Digite um caminho e o nome de arquivo para o certificado exportado, usando uma extensão de arquivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-242">Type a path and file name for the exported certificate, using a file extension of .pfx.</span></span> <span data-ttu-id="dd7a9-243">O caminho deve ser acessível a todos os outros servidores de borda do pool ou disponível para transporte por meio de mídia removível-por exemplo, uma unidade flash USB.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-243">The path must either be accessible to all other Edge servers in the pool or available to transport by means of removable media - for example, a USB flash drive.</span></span> <span data-ttu-id="dd7a9-244">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-244">Click **Next**.</span></span>

12. <span data-ttu-id="dd7a9-245">Examine o resumo na caixa de diálogo concluindo o assistente para exportação de certificados.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-245">Review the summary on the Completing the Certificate Export Wizard dialog.</span></span> <span data-ttu-id="dd7a9-246">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-246">Click **Finish**.</span></span>

13. <span data-ttu-id="dd7a9-247">Clique em **OK** na caixa de diálogo da exportação com sucesso.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-247">Click **OK** in the successful export dialog.</span></span>

14. <span data-ttu-id="dd7a9-248">Importe o arquivo de certificado exportado para os outros servidores de borda seguindo as etapas descritas nos procedimentos [configurar certificados para a interface de borda externa dos procedimentos do Lync Server 2013](lync-server-2013-set-up-certificates-for-the-external-edge-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="dd7a9-248">Import the exported certificate file to the other Edge servers following the steps outlined in the [Set up certificates for the external edge interface for Lync Server 2013](lync-server-2013-set-up-certificates-for-the-external-edge-interface.md) procedures.</span></span>

</div>

<div>

## <a name="to-assign-the-internal-certificate-on-the-edge-servers"></a><span data-ttu-id="dd7a9-249">Para atribuir o certificado interno nos servidores de borda</span><span class="sxs-lookup"><span data-stu-id="dd7a9-249">To assign the internal certificate on the Edge Servers</span></span>

1.  <span data-ttu-id="dd7a9-250">Em cada servidor de borda, no assistente de implantação, ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique **novamente em executar**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-250">On each Edge Server, in the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>

2.  <span data-ttu-id="dd7a9-251">Na página **tarefas de certificado disponíveis** , clique em **atribuir um certificado existente**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-251">On the **Available Certificate Tasks** page, click **Assign an existing certificate**.</span></span>

3.  <span data-ttu-id="dd7a9-252">Na página **Atribuição de Certificado**, selecione  **Interno à Borda** na lista.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-252">On the **Certificate Assignment** page, select **Edge Internal** in the list.</span></span>

4.  <span data-ttu-id="dd7a9-253">Na página **repositório de certificados** , selecione o certificado que você importou para a borda interna (do procedimento anterior).</span><span class="sxs-lookup"><span data-stu-id="dd7a9-253">On the **Certificate Store** page, select the certificate that you imported for the internal edge (from the previous procedure).</span></span>

5.  <span data-ttu-id="dd7a9-254">Na página **Resumo de atribuição de certificado** , examine suas configurações e clique em **Avançar** para atribuir os certificados.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-254">On the **Certificate Assignment Summary** page, review your settings, and then click **Next** to assign the certificates.</span></span>

6.  <span data-ttu-id="dd7a9-255">Na página de conclusão do assistente, clique em  **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-255">On the wizard completion page, click **Finish**.</span></span>

7.  <span data-ttu-id="dd7a9-256">Depois de usar esse procedimento para atribuir o certificado de borda interno, abra o snap-in de certificado em cada servidor, expanda **certificados (computador local)**, expanda **pessoal**, clique em **certificados** e verifique no painel de detalhes se o certificado de borda interna está listado.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-256">After using this procedure to assign the internal edge certificate, open the Certificate snap-in on each server, expand **Certificates (Local computer)**, expand **Personal**, click **Certificates**, and then verify in the details pane that the internal edge certificate is listed.</span></span>

8.  <span data-ttu-id="dd7a9-257">Se a sua implantação incluir vários servidores de borda, repita esse procedimento para cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="dd7a9-257">If your deployment includes multiple Edge Servers, repeat this procedure for each Edge Server.</span></span>

<span data-ttu-id="dd7a9-258"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd7a9-258"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

