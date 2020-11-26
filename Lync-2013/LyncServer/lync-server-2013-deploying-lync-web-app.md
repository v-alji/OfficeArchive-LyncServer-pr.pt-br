---
title: 'Lync Server 2013: implantação do Lync Web App'
description: 'Lync Server 2013: implantação do Lync Web App.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Web App
ms:assetid: b6301e98-051c-4e4b-8e10-ec922a8f508a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205190(v=OCS.15)
ms:contentKeyID: 48185189
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce6fef02781afbd5bc5f315ce24bfb3bdb16df1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429899"
---
# <a name="deploying-lync-web-app-in-lync-server-2013"></a><span data-ttu-id="f7030-103">Implantação do Lync Web App no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7030-103">Deploying Lync Web App in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7030-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7030-104">

<span> </span></span></span>

<span data-ttu-id="f7030-105">_**Tópico da última modificação:** 2013-07-18_</span><span class="sxs-lookup"><span data-stu-id="f7030-105">_**Topic Last Modified:** 2013-07-18_</span></span>

<span data-ttu-id="f7030-106">O Lync Web App é um cliente da Web dos serviços de informações da Internet (IIS) que é instalado com o Lync Server 2013 e é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="f7030-106">Lync Web App is an Internet Information Services (IIS) web client that installs with Lync Server 2013 and is enabled by default.</span></span> <span data-ttu-id="f7030-107">Nenhuma etapa adicional é necessária para habilitar o Lync Web App no servidor ou implantar o cliente Web para os usuários.</span><span class="sxs-lookup"><span data-stu-id="f7030-107">No additional steps are necessary to either enable Lync Web App on the server or deploy the web client to users.</span></span> <span data-ttu-id="f7030-108">Sempre que um usuário clica em uma URL de reunião, mas não tem o cliente do Lync 2013 instalado, o usuário recebe a opção de ingressar na reunião usando a versão mais recente do Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="f7030-108">Whenever a user clicks a meeting URL but does not have the Lync 2013 client installed, the user is presented with the option to join the meeting by using the latest version of Lync Web App.</span></span>

<span data-ttu-id="f7030-109">Os recursos de voz, vídeo e compartilhamento no Lync Web App exigem um controle ActiveX da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f7030-109">The voice, video, and sharing features in Lync Web App require a Microsoft ActiveX control.</span></span> <span data-ttu-id="f7030-110">Você pode instalar o controle ActiveX antecipadamente ou permitir que os usuários o instalem quando solicitado, o que acontecerá na primeira vez em que usarem o Lync Web App ou na primeira vez que acessar um recurso que exija o controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f7030-110">You can either install the ActiveX control in advance or allow users to install it when prompted, which happens the first time they use Lync Web App or the first time they access a feature that requires the ActiveX control.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="f7030-111">Nas implantações do servidor de borda do Lync Server 2013, é necessário um proxy reverso HTTPS na rede de perímetro para acesso de cliente do Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="f7030-111">In Lync Server 2013 Edge Server deployments, an HTTPS reverse proxy in the perimeter network is required for Lync Web App client access.</span></span> <span data-ttu-id="f7030-112">Você também deve publicar URLs simples.</span><span class="sxs-lookup"><span data-stu-id="f7030-112">You must also publish simple URLs.</span></span> <span data-ttu-id="f7030-113">Para obter detalhes, consulte <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Configurando servidores proxy inversos para o Lync Server 2013</A> e <A href="lync-server-2013-planning-for-simple-urls.md">planejando para URLs simples no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f7030-113">For details, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A> and <A href="lync-server-2013-planning-for-simple-urls.md">Planning for simple URLs in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="enabling-multi-factor-authentication-for-lync-web-app"></a><span data-ttu-id="f7030-114">Habilitando a autenticação multifator para o Lync Web App</span><span class="sxs-lookup"><span data-stu-id="f7030-114">Enabling Multi-Factor Authentication for Lync Web App</span></span>

<span data-ttu-id="f7030-115">A versão do Lync Server 2013 do Lync Web App oferece suporte à autenticação multifator.</span><span class="sxs-lookup"><span data-stu-id="f7030-115">The Lync Server 2013 version of Lync Web App supports multi-factor authentication.</span></span> <span data-ttu-id="f7030-116">Além do nome de usuário e da senha, você pode exigir métodos de autenticação adicionais, como cartões inteligentes ou PINs, para autenticar os usuários que estão participando de redes externas quando entrarem em reuniões do Lync.</span><span class="sxs-lookup"><span data-stu-id="f7030-116">In addition to user name and password, you can require additional authentication methods, such as smart cards or PINs, to authenticate users who are joining from external networks when they sign in to Lync meetings.</span></span> <span data-ttu-id="f7030-117">Você pode habilitar a autenticação multifator implantando o servidor de Federação do AD FS (serviços de Federação do Active Directory) e habilitando a autenticação passiva no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7030-117">You can enable multi-factor authentication by deploying Active Directory Federation Service (AD FS) federation server and enabling passive authentication in Lync Server 2013.</span></span> <span data-ttu-id="f7030-118">Após a configuração do AD FS, os usuários externos que tentam ingressar em reuniões do Lync são apresentados com uma página da Web de autenticação multifator do AD FS que contém o nome de usuário e o desafio da senha, juntamente com qualquer método de autenticação adicional que você tenha configurado.</span><span class="sxs-lookup"><span data-stu-id="f7030-118">After AD FS is configured, external users who attempt to join Lync meetings are presented with an AD FS multi-factor authentication webpage that contains the user name and password challenge along with any additional authentication methods that you have configured.</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="f7030-119">As considerações a seguir são importantes se você deseja planejar a configuração do AD FS para a autenticação multifator:</span><span class="sxs-lookup"><span data-stu-id="f7030-119">The following are important considerations if you plan to configure AD FS for multi-factor authentication:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="f7030-p105">A autenticação multifator do ADFS funciona se o participante e o organizador da reunião estiverem na mesma organização ou forem de uma organização federada do AD FS. A autenticação do ADFS de vários fatores não funciona para usuários federados do Lync porque a infraestrutura da Web do servidor do Lync não dà suporte à ela atualmente.</span><span class="sxs-lookup"><span data-stu-id="f7030-p105">Multi-factor ADFS authentication works if the meeting participant and organizer are both in the same organization or are both from an AD FS federated organization. Multi-factor ADFS authentication does not work for Lync federated users because the Lync server web infrastructure does not currently support it.</span></span></P>
> <LI>
> <P><span data-ttu-id="f7030-122">Se você usar balanceadores de carga de hardware, habilite a persistência de cookies nos balanceadores de carga para que todas as solicitações do cliente do Lync Web App sejam manipuladas pelo mesmo servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="f7030-122">If you use hardware load balancers, enable cookie persistence on the load balancers so that all requests from the Lync Web App client are handled by the same Front End Server.</span></span></P>
> <LI>
> <P><span data-ttu-id="f7030-123">Quando você estabelece uma relação de confiança entre terceira parte confiável entre os servidores do Lync Server e do AD FS, atribua uma vida de token longa o suficiente para abranger o tamanho máximo de suas reuniões do Lync.</span><span class="sxs-lookup"><span data-stu-id="f7030-123">When you establish a relying party trust between Lync Server and AD FS servers, assign a token life that is long enough to span the maximum length of your Lync meetings.</span></span> <span data-ttu-id="f7030-124">Normalmente, uma vida de token de 240 minutos é suficiente.</span><span class="sxs-lookup"><span data-stu-id="f7030-124">Typically, a token life of 240 minutes is sufficient.</span></span></P>
> <LI>
> <P><span data-ttu-id="f7030-125">Esta configuração não se aplica aos clientes móveis do Lync.</span><span class="sxs-lookup"><span data-stu-id="f7030-125">This configuration does not apply to Lync mobile clients.</span></span></P></LI></UL>



</div>

<span data-ttu-id="f7030-126">**Para configurar a autenticação multifator**</span><span class="sxs-lookup"><span data-stu-id="f7030-126">**To Configure Multi-Factor Authentication**</span></span>

1.  <span data-ttu-id="f7030-127">Instale uma função de servidor de federação AD FS.</span><span class="sxs-lookup"><span data-stu-id="f7030-127">Install an AD FS federation server role.</span></span> <span data-ttu-id="f7030-128">Para obter detalhes, consulte o guia de implantação do serviços de Federação do Active Directory 2,0 em <https://go.microsoft.com/fwlink/p/?linkid=267511></span><span class="sxs-lookup"><span data-stu-id="f7030-128">For details, see the Active Directory Federation Services 2.0 Deployment Guide at <https://go.microsoft.com/fwlink/p/?linkid=267511></span></span>

2.  <span data-ttu-id="f7030-129">Crie certificados para o AD FS.</span><span class="sxs-lookup"><span data-stu-id="f7030-129">Create certificates for AD FS.</span></span> <span data-ttu-id="f7030-130">Para obter mais informações, consulte a seção "certificados do servidor de Federação" do tópico planejar e implantar o AD FS para uso com o tópico logon único em [https://go.microsoft.com/fwlink/p/?LinkId=285376](https://go.microsoft.com/fwlink/p/?linkid=285376) .</span><span class="sxs-lookup"><span data-stu-id="f7030-130">For more information, see the "Federation server certificates" section of the Plan for and deploy AD FS for use with single sign-on topic at [https://go.microsoft.com/fwlink/p/?LinkId=285376](https://go.microsoft.com/fwlink/p/?linkid=285376).</span></span>

3.  <span data-ttu-id="f7030-131">Na interface de linha de comando do Windows PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f7030-131">From the Windows PowerShell command-line interface, run the following command:</span></span>
    ```powershell
    add-pssnapin Microsoft.Adfs.powershell
    ```
4.  <span data-ttu-id="f7030-132">Estabeleça uma parceria executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f7030-132">Establish a partnership by running the following command:</span></span>
    ```powershell
    Add-ADFSRelyingPartyTrust -Name ContosoApp -MetadataURL https://lyncpool.contoso.com/passiveauth/federationmetadata/2007-06/federationmetadata.xml
     ```
5.  <span data-ttu-id="f7030-133">Defina as seguintes regras de confiabilidade de parte:</span><span class="sxs-lookup"><span data-stu-id="f7030-133">Set the following relying party rules:</span></span>
    
       ```powershell
        $IssuanceAuthorizationRules = '@RuleTemplate = "AllowAllAuthzRule" => issue(Type = "http://schemas.contoso.com/authorization/claims/permit", Value = "true");'
        $IssuanceTransformRules = '@RuleTemplate = "PassThroughClaims" @RuleName = "Sid" c:[Type == "http://schemas.contoso.com/ws/2008/06/identity/claims/primarysid"]=> issue(claim = c);'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName ContosoApp -IssuanceAuthorizationRules $IssuanceAuthorizationRules -IssuanceTransformRules $IssuanceTransformRules
       ```
    
       ```powershell
        Set-CsWebServiceConfiguration -UseWsFedPassiveAuth $true -WsFedPassiveMetadataUri https://dc.contoso.com/federationmetadata/2007-06/federationmetadata.xml
       ```

</div>

<div>

## <a name="branchcache-configuration"></a><span data-ttu-id="f7030-134">Configuração do BranchCache</span><span class="sxs-lookup"><span data-stu-id="f7030-134">BranchCache Configuration</span></span>

<span data-ttu-id="f7030-135">O recurso BranchCache no Windows 7 e no Windows Server 2008 R2 pode interferir nos componentes Web do Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="f7030-135">The BranchCache feature in Windows 7 and Windows Server 2008 R2 can interfere with Lync Web App web components.</span></span> <span data-ttu-id="f7030-136">Para evitar problemas para usuários do Lync Web App, verifique se o BranchCache não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f7030-136">To prevent issues for Lync Web App users, make sure that BranchCache is not enabled.</span></span>

<span data-ttu-id="f7030-137">Para obter detalhes sobre como desabilitar o BranchCache, consulte o guia de implantação do BranchCache, que está disponível no formato do Word no centro de download da Microsoft em [https://go.microsoft.com/fwlink/p/?LinkId=268788](https://go.microsoft.com/fwlink/p/?linkid=268788) formato HTML na biblioteca técnica do Windows Server 2008 R2 em [https://go.microsoft.com/fwlink/p/?LinkId=268789](https://go.microsoft.com/fwlink/p/?linkid=268789) .</span><span class="sxs-lookup"><span data-stu-id="f7030-137">For details about disabling BranchCache, see the BranchCache Deployment Guide, which is available in Word format at the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268788](https://go.microsoft.com/fwlink/p/?linkid=268788) and in HTML format in the Windows Server 2008 R2 Technical Library at [https://go.microsoft.com/fwlink/p/?LinkId=268789](https://go.microsoft.com/fwlink/p/?linkid=268789).</span></span>

</div>

<div>

## <a name="verifying-lync-web-app-deployment"></a><span data-ttu-id="f7030-138">Verificando a implantação do Lync Web App</span><span class="sxs-lookup"><span data-stu-id="f7030-138">Verifying Lync Web App Deployment</span></span>

<span data-ttu-id="f7030-139">Você pode usar o cmdlet Test-CsUcwaConference para verificar se um par de usuários de teste pode participar de uma conferência usando a UCWA (Unified Communications Web API).</span><span class="sxs-lookup"><span data-stu-id="f7030-139">You can use the Test-CsUcwaConference cmdlet to verify that a pair of test users can participate in a conference using the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="f7030-140">Para obter detalhes sobre esse cmdlet, consulte [Test-CsUcwaConference](https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference) na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f7030-140">For details about this cmdlet, see [Test-CsUcwaConference](https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="troubleshooting-plug-in-installation-on-windows-server-2008-r2"></a><span data-ttu-id="f7030-141">Solução de problemas de instalação do plug-in no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7030-141">Troubleshooting Plug-in Installation on Windows Server 2008 R2</span></span>

<span data-ttu-id="f7030-142">Se a instalação do plug-in falhar em um computador executando o Windows Server 2008 R2, talvez seja necessário modificar a configuração de segurança do Internet Explorer ou a configuração da chave do registro DisableMSI.</span><span class="sxs-lookup"><span data-stu-id="f7030-142">If installation of the plug-in fails on a computer running Windows Server 2008 R2, you may need to modify the Internet Explorer security setting or the DisableMSI registry key setting.</span></span>

<span data-ttu-id="f7030-143">**Para modificar a configuração de segurança no Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="f7030-143">**To modify the security setting in Internet Explorer**</span></span>

1.  <span data-ttu-id="f7030-144">Abra o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f7030-144">Open Internet Explorer.</span></span>

2.  <span data-ttu-id="f7030-145">Clique em **Ferramentas**, em **Opções da Internet** e em **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="f7030-145">Click **Tools**, click **Internet Options**, and then click **Advanced**.</span></span>

3.  <span data-ttu-id="f7030-146">Role para baixo até a seção **Segurança**.</span><span class="sxs-lookup"><span data-stu-id="f7030-146">Scroll down to the **Security** section.</span></span>

4.  <span data-ttu-id="f7030-147">Desmarque **Não salvar páginas criptografadas no disco** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7030-147">Clear **Do not save encrypted pages to disk**, and then click **OK**.</span></span>
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="f7030-148">Se selecionado, essa configuração também causará um erro ao tentar baixar um anexo do Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="f7030-148">If selected, this setting will also cause an error when trying to download an attachment from Lync Web App.</span></span>

    
    </div>

5.  <span data-ttu-id="f7030-149">Reingresse na reunião.</span><span class="sxs-lookup"><span data-stu-id="f7030-149">Rejoin the meeting.</span></span> <span data-ttu-id="f7030-150">O download do plug-in deve ocorrer sem erros.</span><span class="sxs-lookup"><span data-stu-id="f7030-150">The plug-in should download without errors.</span></span>

<span data-ttu-id="f7030-151">**Para modificar a configuração do registro DisableMSI**</span><span class="sxs-lookup"><span data-stu-id="f7030-151">**To modify the DisableMSI Registry setting**</span></span>

1.  <span data-ttu-id="f7030-152">Clique em  **Iniciar** e em  **Executar**.</span><span class="sxs-lookup"><span data-stu-id="f7030-152">Click **Start**, and then click **Run**.</span></span>

2.  <span data-ttu-id="f7030-153">Para acessar o Editor do Registro, digite **regedit**.</span><span class="sxs-lookup"><span data-stu-id="f7030-153">To access the Registry Editor, type **regedit**.</span></span>

3.  <span data-ttu-id="f7030-154">Navegue até HKEY \_ local \_ Machine \\ software \\ Policies \\ Microsoft \\ Windows \\ Installer.</span><span class="sxs-lookup"><span data-stu-id="f7030-154">Navigate to HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer.</span></span>

4.  <span data-ttu-id="f7030-155">Edite ou adicione a chave do registro DisableMSI do tipo REG \_ DWORD e defina-o como 0.</span><span class="sxs-lookup"><span data-stu-id="f7030-155">Edit or add the DisableMSI registry key of type REG\_DWORD and set it to 0.</span></span>

5.  <span data-ttu-id="f7030-156">Reingresse na reunião.</span><span class="sxs-lookup"><span data-stu-id="f7030-156">Rejoin the meeting.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f7030-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7030-157">See Also</span></span>


[<span data-ttu-id="f7030-158">Configurando a página de ingresso na reunião no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7030-158">Configuring the meeting join page in Lync Server 2013</span></span>](lync-server-2013-configuring-the-meeting-join-page.md)  
[<span data-ttu-id="f7030-159">Plataformas compatíveis com o Lync Web App para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7030-159">Lync Web App supported platforms for Lync Server 2013</span></span>](lync-server-2013-lync-web-app-supported-platforms.md)  
  

<span data-ttu-id="f7030-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7030-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

