---
title: 'Lync Server 2013: Protegendo o IIS'
description: 'Lync Server 2013: protegendo o IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Protecting IIS in Lync Server 2013
ms:assetid: a67171a6-6703-4e09-abb3-35d335bb674e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518332(v=OCS.15)
ms:contentKeyID: 62625492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51161f221c7235aad04850fdccc5d5e9db5cb579
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436836"
---
# <a name="protecting-iis-in-lync-server-2013"></a><span data-ttu-id="2bdfb-103">Protegendo o IIS no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2bdfb-103">Protecting IIS in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bdfb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bdfb-104">

<span> </span></span></span>

<span data-ttu-id="2bdfb-105">_**Tópico da última modificação:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="2bdfb-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="2bdfb-106">No Microsoft Office Communications Server 2007 e no Microsoft Office Communications Server 2007 R2, os serviços de informações da Internet (IIS) são executados em uma conta de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-106">In Microsoft Office Communications Server 2007 and Microsoft Office Communications Server 2007 R2, Internet Information Services (IIS) ran under a standard user account.</span></span> <span data-ttu-id="2bdfb-107">Isso teve o potencial de causar problemas: se essa senha tiver expirado, você poderá perder seus serviços Web, um problema que muitas vezes era difícil de diagnosticar.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-107">This had the potential to cause issues: if that password expired you could lose your Web Services, an issue that was often difficult to diagnose.</span></span> <span data-ttu-id="2bdfb-108">Para ajudar a evitar o problema de senhas expiradas, o Microsoft Lync Server 2013 permite que você crie uma conta de computador (para um computador que não existe realmente) que possa servir como a entidade de autenticação para todos os computadores em um site que executa o IIS.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-108">To help avoid the issue of expiring passwords, Microsoft Lync Server 2013 enables you to create a computer account (for a computer that doesn’t actually exist) that can serve as the authentication principal for all the computers in a site that are running IIS.</span></span> <span data-ttu-id="2bdfb-109">Como essas contas utilizam o protocolo de autenticação Kerberos, elas são referidas como contas Kerberos e o novo processo de autenticação é conhecido como autenticação Kerberos de Web.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-109">Because these accounts use the Kerberos authentication protocol, the accounts are referred to as Kerberos accounts, and the new authentication process is known as Kerberos web authentication.</span></span> <span data-ttu-id="2bdfb-110">Isso permite gerenciar todos os servidores IIS usando uma única conta.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-110">This enables you to manage all your IIS servers by using a single account.</span></span>

<span data-ttu-id="2bdfb-111">Para executar seus servidores nesse objeto de autenticação, primeiro você deve criar uma conta de computador usando o cmdlet New-CsKerberosAccount; Esta conta é atribuída a um ou mais sites.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-111">To run your servers under this authentication principal, you must first create a computer account by using the New-CsKerberosAccount cmdlet; this account is then assigned to one or more sites.</span></span> <span data-ttu-id="2bdfb-112">Após a atribuição ter sido feita, a associação entre a conta e o site do Lync Server 2013 é habilitada executando o cmdlet Enable-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-112">After the assignment has been made, the association between the account and the Lync Server 2013 site is enabled by running the Enable-CsTopology cmdlet.</span></span> <span data-ttu-id="2bdfb-113">Entre outras coisas, isso cria o SPN (nome da entidade de serviço) obrigatório nos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="2bdfb-113">Among other things, this creates the required service principal name (SPN) in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="2bdfb-114">Os SPNs proporcionam aos aplicativos cliente uma maneira de localizar um determinado serviço.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-114">SPNs provide a way for client applications to locate a particular service.</span></span> <span data-ttu-id="2bdfb-115">Para obter detalhes, consulte [New-CsKerberosAccount](https://docs.microsoft.com/powershell/module/skype/New-CsKerberosAccount) na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-115">For details, see [New-CsKerberosAccount](https://docs.microsoft.com/powershell/module/skype/New-CsKerberosAccount) in the Operations documentation.</span></span>

<div>

## <a name="best-practices"></a><span data-ttu-id="2bdfb-116">Práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="2bdfb-116">Best Practices</span></span>

<span data-ttu-id="2bdfb-117">Para ajudar a aumentar a segurança do IIS, recomendamos que você implemente uma conta Kerberos para o IIS.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-117">To help increase security of IIS, we recommend that you implement a Kerberos account for IIS.</span></span> <span data-ttu-id="2bdfb-118">Se você não implementar uma conta Kerberos, o IIS será executado em uma conta de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-118">If you do not implement a Kerberos account, IIS runs under a standard user account.</span></span>

<span data-ttu-id="2bdfb-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bdfb-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

