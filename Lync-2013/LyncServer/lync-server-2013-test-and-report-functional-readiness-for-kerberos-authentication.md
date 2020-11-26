---
title: Testar e relatar prontidão funcional para autenticação Kerberos
description: Testar e relatar a prontidão funcional para a autenticação Kerberos.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test and report functional readiness for Kerberos authentication
ms:assetid: d52c39e5-747d-4f29-88aa-30fd6f26b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398925(v=OCS.15)
ms:contentKeyID: 48185519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d32591a8cced7dce2e0bb78cc26189dce1900a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444298"
---
# <a name="test-and-report-functional-readiness-for-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="c92c5-103">Testar e relatar prontidão funcional para autenticação Kerberos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c92c5-103">Test and report functional readiness for Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c92c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c92c5-104">

<span> </span></span></span>

<span data-ttu-id="c92c5-105">_**Tópico da última modificação:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="c92c5-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="c92c5-106">Para concluir esse procedimento com êxito, você deve estar conectado como um usuário que é membro do grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="c92c5-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="c92c5-107">Você pode usar o cmdlet **Test-CsKerberosAccountAssignment** do Windows PowerShell para testar e relatar a prontidão funcional de uma atribuição de site para a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c92c5-107">You can use the **Test-CsKerberosAccountAssignment** Windows PowerShell cmdlet to test and report the functional readiness of a site assignment for Kerberos authentication.</span></span> <span data-ttu-id="c92c5-108">Esse comando consulta o site especificado no parâmetro Identity necessário.</span><span class="sxs-lookup"><span data-stu-id="c92c5-108">This command queries the site specified in the required Identity parameter.</span></span> <span data-ttu-id="c92c5-109">O parâmetro de relatório opcional faz com que o cmdlet escreva um relatório HTML para C: \\ registra o computador no qual o comando é executado.</span><span class="sxs-lookup"><span data-stu-id="c92c5-109">The optional Report parameter causes the cmdlet to write an HTML report to C:\\Logs on the computer on which the command is run.</span></span> <span data-ttu-id="c92c5-110">O parâmetro detalhado opcional relata as informações de atividade para a tela.</span><span class="sxs-lookup"><span data-stu-id="c92c5-110">The optional Verbose parameter reports activity information to the screen.</span></span>

<div>

## <a name="to-test-and-report-functional-readiness-for-kerberos-authentication-for-a-site"></a><span data-ttu-id="c92c5-111">Para testar e relatar a prontidão funcional para a autenticação Kerberos de um site</span><span class="sxs-lookup"><span data-stu-id="c92c5-111">To test and report functional readiness for Kerberos authentication for a site</span></span>

1.  <span data-ttu-id="c92c5-112">Como membro do grupo RTCUniversalServerAdmins, faça logon em um computador no domínio que está executando o Lync Server 2013 ou no computador onde as ferramentas administrativas estão instaladas.</span><span class="sxs-lookup"><span data-stu-id="c92c5-112">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to the computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="c92c5-113">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="c92c5-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c92c5-114">Na linha de comando, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="c92c5-114">From the command line, run the following command:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:SiteName" -Report "c:\logs\FileName.htm" -Verbose
    
    <span data-ttu-id="c92c5-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c92c5-115">For example:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "c:\logs\KerberosReport.htm" -Verbose

<span data-ttu-id="c92c5-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c92c5-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

