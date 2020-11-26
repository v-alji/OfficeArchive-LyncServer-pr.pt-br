---
title: 'Lync Server 2013: Configurar uma senha da conta de autenticação Kerberos authentication em um servidor'
description: 'Lync Server 2013: definir uma senha da conta de autenticação Kerberos em um servidor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set a Kerberos authentication account password on a server
ms:assetid: 902d3292-678d-4512-9248-586053cb638b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398734(v=OCS.15)
ms:contentKeyID: 48184787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 723392e670ca0b4bc9796cd62dab3b1a61f99dd1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444781"
---
# <a name="set-a-kerberos-authentication-account-password-on-a-server-in-lync-server-2013"></a><span data-ttu-id="b3f6f-103">Configurar uma senha da conta de autenticação Kerberos authentication em um servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3f6f-103">Set a Kerberos authentication account password on a server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3f6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3f6f-104">

<span> </span></span></span>

<span data-ttu-id="b3f6f-105">_**Tópico da última modificação:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="b3f6f-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="b3f6f-106">Para concluir esse procedimento com êxito, você deve estar conectado como um usuário que é membro do grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="b3f6f-107">Você deve configurar uma senha na conta Kerberos para cada site que tenha servidores front-end, servidores de edição padrão e directors.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-107">You must set up a password on the Kerberos account for each site that has Front End Servers, Standard Edition servers, and Directors.</span></span> <span data-ttu-id="b3f6f-108">Você pode configurar a senha executando o cmdlet **set-CsKerberosAccountPassword** do Windows PowerShell em um servidor no site (por exemplo, um servidor front-end).</span><span class="sxs-lookup"><span data-stu-id="b3f6f-108">You can set up the password by running the **Set-CsKerberosAccountPassword** Windows PowerShell cmdlet on one server in the site (for example, one Front End Server).</span></span> <span data-ttu-id="b3f6f-109">Para cada site, você deve executar o cmdlet **set-CsKerberosAccountPassword** .</span><span class="sxs-lookup"><span data-stu-id="b3f6f-109">For each site, you must run the **Set-CsKerberosAccountPassword** cmdlet.</span></span> <span data-ttu-id="b3f6f-110">O cmdlet configura o IIS (serviços de informações da Internet) para o serviço de serviços Web e define a senha na conta do computador nos serviços de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-110">The cmdlet configures Internet Information Services (IIS) for the Web Services service, and then sets the password on the computer account in Active Directory Domain Services.</span></span> <span data-ttu-id="b3f6f-111">Um método alternativo, com base em qual parâmetro é usado com o cmdlet, configura o IIS em um servidor enquanto usa outro servidor que tenha sido configurado como a origem da senha da conta Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-111">An alternate method, based on which parameter is used with the cmdlet, configures IIS on one server while using another server that has been configured as the source of the Kerberos account password.</span></span>

<span data-ttu-id="b3f6f-112">Quando você usa o cmdlet **set-CsKerberosAccountPassword** para definir uma senha, o Kerberos define a senha como uma cadeia de caracteres gerada aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-112">When you use the **Set-CsKerberosAccountPassword** cmdlet to set a password, Kerberos sets the password to a randomly generated string.</span></span> <span data-ttu-id="b3f6f-113">Este cmdlet entra em contato com todas as instâncias do IIS em todos os sites centrais do Lync Server 2013 aos quais essa conta foi atribuída.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-113">This cmdlet contacts all IIS instances in all Lync Server 2013 central sites to which this account is assigned.</span></span>

<div>

## <a name="to-set-a-password-for-a-kerberos-authentication-account"></a><span data-ttu-id="b3f6f-114">Para definir uma senha para uma conta de autenticação Kerberos</span><span class="sxs-lookup"><span data-stu-id="b3f6f-114">To set a password for a Kerberos authentication account</span></span>

1.  <span data-ttu-id="b3f6f-115">Faça logon em qualquer computador do domínio com o Shell de gerenciamento do Lync Server instalado como membro do grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-115">Log on to any domain computer with Lync Server Management Shell installed as a member of the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="b3f6f-116">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="b3f6f-117">Na linha de comando, execute os dois comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="b3f6f-117">From the command line, run the following two commands:</span></span>
    
        Set-CsKerberosAccountPassword -UserAccount "Domain\UserAccount"
    
    <span data-ttu-id="b3f6f-118">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b3f6f-118">For example:</span></span>
    
        Set-CsKerberosAccountPassword -UserAccount "contoso\KerbAuth"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b3f6f-119">Você deve especificar o parâmetro USERACCOUNT usando o formato domínio \ usuário.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-119">You must specify the UserAccount parameter by using the Domain\User format.</span></span> <span data-ttu-id="b3f6f-120">Não há suporte para o formato de extensão User@Domain. para fazer referência aos objetos de computador criados para fins de autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-120">The User@Domain.extension format is not supported for referencing the computer objects created for Kerberos authentication purposes.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b3f6f-121">Depois de fazer qualquer alteração na autenticação Kerberos, como adicionar uma conta ou remover uma conta, você deve executar <STRONG>Enable-CsTopology</STRONG> no prompt de comando do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b3f6f-121">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="b3f6f-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3f6f-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

