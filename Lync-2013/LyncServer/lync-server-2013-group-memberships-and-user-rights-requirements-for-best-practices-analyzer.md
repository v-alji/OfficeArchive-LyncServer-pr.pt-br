---
title: Associações de grupo e requisitos de direitos de usuário para o analisador de práticas recomendadas
description: Associações de grupo e requisitos de direitos de usuário para o analisador de práticas recomendadas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group memberships and user rights requirements for Best Practices Analyzer
ms:assetid: f812e343-8f75-454e-b7a8-1b404e32071a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591354(v=OCS.15)
ms:contentKeyID: 48185869
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 64a7d785a77701c6796488178a7cce10caf54f42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427821"
---
# <a name="group-memberships-and-user-rights-requirements-for-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="4dcf8-103">Associações de grupo e requisitos de direitos de usuário para o analisador de práticas recomendadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4dcf8-103">Group memberships and user rights requirements for Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4dcf8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4dcf8-104">

<span> </span></span></span>

<span data-ttu-id="4dcf8-105">_**Tópico da última modificação:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="4dcf8-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="4dcf8-106">Para executar com êxito o analisador de práticas recomendadas, a conta de usuário que você usa para fazer logon deve ser um membro do grupo Administradores no computador local.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-106">To successfully run Best Practices Analyzer, the user account that you use to log on must be a member of the Administrators group on the local computer.</span></span> <span data-ttu-id="4dcf8-107">Além disso, para verificar seu ambiente, a conta de usuário deve ser um membro dos seguintes grupos:</span><span class="sxs-lookup"><span data-stu-id="4dcf8-107">Additionally, to scan your environment, the user account must be a member of the following groups:</span></span>

  - <span data-ttu-id="4dcf8-108">**Administradores de domínio**   Para enumerar as informações dos serviços de domínio Active Directory e chamar os provedores de instrumentação de gerenciamento do Windows (WMI) nos controladores de domínio e nos servidores de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-108">**Domain Admins**   To enumerate Active Directory Domain Services information and to call the Windows Management Instrumentation (WMI) providers on domain controllers and global catalog servers.</span></span>

  - <span data-ttu-id="4dcf8-109">**Administradores**   do   Obrigatório em cada computador interno do Lync Server 2013 e em cada servidor de borda para chamar os provedores de instrumentação de gerenciamento do Windows (WMI) e acessar o registro.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-109">**Administrators**   Required on each Lync Server 2013 internal computer and each Edge Server to call the Windows Management Instrumentation (WMI) providers and to access the registry.</span></span>

  - <span data-ttu-id="4dcf8-110">**RTCUniversalReadOnlyAdmins**   Direitos administrativos totais ou delegados somente leitura do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-110">**RTCUniversalReadOnlyAdmins**   Full or delegated read only Lync Server 2013 administrative rights.</span></span>

  - <span data-ttu-id="4dcf8-111">**Administrador somente para exibição do Exchange**   Administrador do Exchange somente para exibição completa ou delegada na organização do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-111">**Exchange View Only Administrator**   Full or delegated Exchange View Only Administrator on the Microsoft Exchange organization.</span></span>

<span data-ttu-id="4dcf8-112">Se a sua conta de usuário não tiver direitos de usuário suficientes, você terá duas opções:</span><span class="sxs-lookup"><span data-stu-id="4dcf8-112">If your user account does not have sufficient user rights, you have two options:</span></span>

  - <span data-ttu-id="4dcf8-113">Em um prompt de comando, use o comando **runas** para executar a ferramenta em uma conta que tem direitos de usuário suficientes.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-113">At a command prompt, use the **runas** command to run the tool under an account that does have sufficient user rights.</span></span> <span data-ttu-id="4dcf8-114">A sintaxe é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="4dcf8-114">The syntax is as follows:</span></span>
    
        runas /netonly /user:<domain>\<userName> rtcbpa.exe

  - <span data-ttu-id="4dcf8-115">Na página **conectar-se ao Active Directory** , defina as credenciais das contas que você planeja usar para executar o analisador de práticas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-115">On the **Connect to Active Directory** page, set the credentials for the accounts that you plan to use to run Best Practices Analyzer.</span></span> <span data-ttu-id="4dcf8-116">Clique em **Mostrar opções avançadas de login**.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-116">Click **Show advanced login options**.</span></span> <span data-ttu-id="4dcf8-117">Você pode inserir três contas: uma para conectar-se aos serviços de domínio do Active Directory, uma para conexão com servidores de borda do Lync Server 2013 e outra para conexão com os servidores Exchange.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-117">You can enter three accounts: one for connecting to Active Directory Domain Services, one for connecting to Lync Server 2013 Edge Servers, and one for connecting to the Exchange Servers.</span></span> <span data-ttu-id="4dcf8-118">Se você não especificar nenhuma dessas contas, a conta de usuário que você usou para fazer logon e executar o analisador de práticas recomendadas será usada.</span><span class="sxs-lookup"><span data-stu-id="4dcf8-118">If you do not specify any of these accounts, the user account that you used to log on and run Best Practices Analyzer is used.</span></span>

<span data-ttu-id="4dcf8-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4dcf8-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

