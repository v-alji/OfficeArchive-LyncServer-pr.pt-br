---
title: 'Lync Server 2013: Configurando os serviços de Federação do Active Directory (AD FS 2,0)'
description: 'Lync Server 2013: Configurando os serviços de Federação do Active Directory (AD FS 2,0).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Active Directory Federation Services (AD FS 2.0)
ms:assetid: 0ba8657f-55b8-41b3-960c-fdc5eeee6978
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308561(v=OCS.15)
ms:contentKeyID: 54973682
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bc21500273d8576f54f6110783e61764ec9723a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433399"
---
# <a name="configuring-active-directory-federation-services-ad-fs-20-for-lync-server-2013"></a><span data-ttu-id="913ab-103">Configurar os serviços de Federação do Active Directory (AD FS 2,0) para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="913ab-103">Configuring Active Directory Federation Services (AD FS 2.0) for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="913ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="913ab-104">

<span> </span></span></span>

<span data-ttu-id="913ab-105">_**Tópico da última modificação:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="913ab-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="913ab-106">A seção a seguir descreve como configurar o Serviços de Federação do Active Directory (AD FS 2.0) para dar suporte à autenticação multifator.</span><span class="sxs-lookup"><span data-stu-id="913ab-106">The following section describes how to configure Active Directory Federation Services (AD FS 2.0) to support multi-factor authentication.</span></span> <span data-ttu-id="913ab-107">Para obter informações sobre como instalar o AD FS 2,0, consulte guias do AD FS 2,0 passo a passo e como fazer guias em [https://go.microsoft.com/fwlink/p/?LinkId=313374](https://go.microsoft.com/fwlink/p/?linkid=313374) .</span><span class="sxs-lookup"><span data-stu-id="913ab-107">For information on how to install AD FS 2.0, see AD FS 2.0 Step-by-Step and How To Guides at [https://go.microsoft.com/fwlink/p/?LinkId=313374](https://go.microsoft.com/fwlink/p/?linkid=313374).</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="913ab-108">Ao instalar o AD FS 2.0, não use o Windows Server Manager para adicionar a função do Active Directory Federation.</span><span class="sxs-lookup"><span data-stu-id="913ab-108">When installing AD FS 2.0, do not use the Windows Server Manager to add the Active Directory Federation Services role.</span></span> <span data-ttu-id="913ab-109">Em vez disso, baixe e instale o pacote de serviços de Federação do Active Directory 2,0 RTW em <A href="https://go.microsoft.com/fwlink/p/?linkid=313375">https://go.microsoft.com/fwlink/p/?LinkId=313375</A> .</span><span class="sxs-lookup"><span data-stu-id="913ab-109">Instead, download and install the Active Directory Federation Services 2.0 RTW package at <A href="https://go.microsoft.com/fwlink/p/?linkid=313375">https://go.microsoft.com/fwlink/p/?LinkId=313375</A>.</span></span>



</div>

<div>


<span data-ttu-id="913ab-110">**Para configurar o AD FS para autenticação de dois fatores**</span><span class="sxs-lookup"><span data-stu-id="913ab-110">**To configure AD FS for two-factor Authentication**</span></span>

1.  <span data-ttu-id="913ab-111">Faça logon no computador do AD FS 2.0 utilizando uma conta de Administrador de Domínio.</span><span class="sxs-lookup"><span data-stu-id="913ab-111">Log in to the AD FS 2.0 computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="913ab-112">Inicie o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="913ab-112">Start Windows PowerShell.</span></span>

3.  <span data-ttu-id="913ab-113">Na linha de comando do Windows PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="913ab-113">From the Windows PowerShell command-line, run the following command:</span></span>
    ```powershell
    add-pssnapin Microsoft.Adfs.PowerShell
    ```
4.  <span data-ttu-id="913ab-114">Estabeleça uma parceria com cada Lync Server 2013 com atualizações cumulativas para o Lync Server 2013: Director de julho de 2013, pool corporativo e servidor Standard Edition que será habilitado para autenticação passiva executando o seguinte comando, substituindo o nome do servidor específico à sua implantação:</span><span class="sxs-lookup"><span data-stu-id="913ab-114">Establish a partnership with each Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Director, Enterprise Pool, and Standard Edition server that will be enabled for passive authentication by running the following command, replacing the server name specific to your deployment:</span></span>
    ```powershell
    Add-ADFSRelyingPartyTrust -Name LyncPool01-PassiveAuth -MetadataURL https://lyncpool01.contoso.com/passiveauth/federationmetadata/2007-06/federationmetadata.xml
     ```
5.  <span data-ttu-id="913ab-115">No menu Ferramentas Administrativas, inicie o Console de Gerenciamento do AD FS 2.0.</span><span class="sxs-lookup"><span data-stu-id="913ab-115">From the Administrative Tools menu, launch the AD FS 2.0 Management console.</span></span>

6.  <span data-ttu-id="913ab-116">Expanda **relações de confiança** \> **confiança de terceira parte confiável**.</span><span class="sxs-lookup"><span data-stu-id="913ab-116">Expand **Trust Relationships** \> **Relying Party Trusts**.</span></span>

7.  <span data-ttu-id="913ab-117">Verifique se uma nova confiança foi criada para o Lync Server 2013 com atualizações cumulativas para o Lync Server 2013: julho de 2013 Enterprise pool ou Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="913ab-117">Verify that a new trust has been created for your Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Enterprise Pool or Standard Edition server.</span></span>

8.  <span data-ttu-id="913ab-118">Crie e atribua uma Regra de Autorização de Emissão para seu objeto de confiança de terceira parte confiável usando o Windows PowerShell executando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="913ab-118">Create and assign an Issuance Authorization Rule for your relying party trust using Windows PowerShell by running the following commands:</span></span>
    
       ```powershell
        $IssuanceAuthorizationRules = '@RuleTemplate = "AllowAllAuthzRule" => issue(Type = "http://schemas.microsoft.com/authorization/claims/permit", Value = "true");'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName LyncPool01-PassiveAuth 
        -IssuanceAuthorizationRules $IssuanceAuthorizationRules
       ```

9.  <span data-ttu-id="913ab-119">Crie e atribua uma Regra de Transformação de Emissão para seu objeto de confiança de terceira parte confiável usando o Windows PowerShell executando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="913ab-119">Create and assign an Issuance Transform Rule for your relying party trust using Windows PowerShell by running the following commands:</span></span>
    
       ```powershell
        $IssuanceTransformRules = '@RuleTemplate = "PassThroughClaims" @RuleName = "Sid" c:[Type == "http://schemas.microsoft.com/ws/2008/06/identity/claims/primarysid"]=> issue(claim = c);'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName LyncPool01-PassiveAuth -IssuanceTransformRules $IssuanceTransformRules
       ```

10. <span data-ttu-id="913ab-120">No Console de Gerenciamento do AD FS 2.0, clique com o botão direito no seu objeto de confiança de terceira parte confiável e selecione **Editar Regras de Declaração**.</span><span class="sxs-lookup"><span data-stu-id="913ab-120">From the AD FS 2.0 Management console, right click on your relying party trust and select **Edit Claim Rules**.</span></span>

11. <span data-ttu-id="913ab-121">Selecione a guia **Regras de Autorização de Emissão** e verifique se a nova regra de autorização foi criada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="913ab-121">Select the **Issuance Authorization Rules** tab and verify that the new authorization rule was created successfully.</span></span>

12. <span data-ttu-id="913ab-122">Selecione a guia **Regras de Transformação de Emissão** e verifique se a nova regra de transformação foi criada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="913ab-122">Select the **Issuance Transform Rules** tab and verify that the new transform rule was created successfully.</span></span>

<span data-ttu-id="913ab-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="913ab-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

