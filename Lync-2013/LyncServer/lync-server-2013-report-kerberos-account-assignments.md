---
title: 'Lync Server 2013: Relatar atribuições da conta Kerberos'
description: 'Lync Server 2013: relatar atribuições de conta Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Report Kerberos account assignments
ms:assetid: 523231f6-81b3-454b-996d-663d9bd5cf83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398343(v=OCS.15)
ms:contentKeyID: 48184151
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23e40dddfc4538db70e2101b1bfcbbce2fe3fa8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442737"
---
# <a name="report-kerberos-account-assignments-in-lync-server-2013"></a><span data-ttu-id="8ff51-103">Relatar atribuições da conta Kerberos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ff51-103">Report Kerberos account assignments in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ff51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ff51-104">

<span> </span></span></span>

<span data-ttu-id="8ff51-105">_**Tópico da última modificação:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="8ff51-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="8ff51-106">Para concluir esse procedimento com êxito, você deve estar conectado como um usuário que é membro do grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="8ff51-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="8ff51-107">Você pode usar o cmdlet **Get-CsKerberosAccountAssignment** para consultar informações sobre as atribuições de conta de autenticação Kerberos e informações de relatório sobre as atribuições atuais na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="8ff51-107">You can use the **Get-CsKerberosAccountAssignment** cmdlet to query information about the Kerberos authentication account assignments and report information about the current assignments in your deployment.</span></span>

<div>

## <a name="to-query-kerberos-authentication-account-assignments-for-a-site"></a><span data-ttu-id="8ff51-108">Para consultar as atribuições de conta de autenticação Kerberos para um site</span><span class="sxs-lookup"><span data-stu-id="8ff51-108">To query Kerberos authentication account assignments for a site</span></span>

1.  <span data-ttu-id="8ff51-109">Como membro do grupo RTCUniversalServerAdmins, faça logon em um computador no domínio que está executando o Lync Server 2013 ou em um computador onde as ferramentas administrativas estão instaladas.</span><span class="sxs-lookup"><span data-stu-id="8ff51-109">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="8ff51-110">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8ff51-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="8ff51-111">Na linha de comando, execute um dos seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="8ff51-111">From the command line, run one of the following commands:</span></span>
    
      - <span data-ttu-id="8ff51-112">Para consultar todas as atribuições de conta de autenticação Kerberos em sua organização e retornar informações de atribuição sobre cada uma delas, execute o cmdlet sem parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8ff51-112">To query all Kerberos authentication account assignments in your organization and return assignment information about each of them, run the cmdlet without any parameters:</span></span>
        
            Get-CsKerberosAccountAssignment
    
      - <span data-ttu-id="8ff51-113">Para consultar todas as atribuições de conta de autenticação Kerberos na implantação e retornar informações de atribuição de site sobre cada uma delas, execute o cmdlet com o parâmetro de identidade:</span><span class="sxs-lookup"><span data-stu-id="8ff51-113">To query all Kerberos authentication account assignments in your deployment and return site assignment information about each of them, run the cmdlet with the Identity parameter:</span></span>
        
            Get-CsKerberosAccountAssignment -Identity "site:SiteName"
        
        <span data-ttu-id="8ff51-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8ff51-114">For example:</span></span>
        
            Get-CsKerberosAccountAssignment -Identity "site:Redmond"
    
      - <span data-ttu-id="8ff51-115">Para consultar todas as atribuições de conta de autenticação Kerberos em um único site e retornar informações de atribuição sobre cada uma delas, execute o cmdlet com o parâmetro de filtro:</span><span class="sxs-lookup"><span data-stu-id="8ff51-115">To query all Kerberos authentication account assignments in a single site and return assignment information about each of them, run the cmdlet with the Filter parameter:</span></span>
        
            Get-CsKerberosAccountAssignment -Filter "SiteName"
        
        <span data-ttu-id="8ff51-116">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8ff51-116">For example:</span></span>
        
            Get-CsKerberosAccountAssignment -Filter "*Redmond"
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8ff51-117">Especificar \* SiteName para o parâmetro Filter retorna informações sobre todos os sites que contêm o nome do site especificado em qualquer lugar no identificador de site (por exemplo, todos os sites que contêm a cadeia de caracteres Redmond no identificador do site).</span><span class="sxs-lookup"><span data-stu-id="8ff51-117">Specifying \*SiteName for the Filter parameter returns information about all sites that contain the specified site name anywhere in the site identifier (for example, all sites that contain the string Redmond in the site identifier).</span></span>

        
        <span data-ttu-id="8ff51-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ff51-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

