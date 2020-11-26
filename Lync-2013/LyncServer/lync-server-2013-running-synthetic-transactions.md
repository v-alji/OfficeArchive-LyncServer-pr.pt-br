---
title: 'Lync Server 2013: Executando transações sintéticas'
description: 'Lync Server 2013: Executando transações sintéticas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running synthetic transactions
ms:assetid: 2b56c7bd-8956-4fa1-8232-1876b959b258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720911(v=OCS.15)
ms:contentKeyID: 63969593
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26b0c26024f361dac196319eaf849c1847033cc9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442177"
---
# <a name="running-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="1140b-103">Executar transações sintéticas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1140b-103">Running synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1140b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1140b-104">

<span> </span></span></span>

<span data-ttu-id="1140b-105">_**Tópico da última modificação:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="1140b-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="1140b-106">As transações sintéticas geralmente são conduzidas de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="1140b-106">Synthetic transactions are typically conducted in two ways.</span></span> <span data-ttu-id="1140b-107">Você pode usar os cmdlets CsHealthMonitoringConfiguration para configurar usuários de teste para cada um dos seus pools de registradores.</span><span class="sxs-lookup"><span data-stu-id="1140b-107">You can use the CsHealthMonitoringConfiguration cmdlets to set up test users for each of their Registrar pools.</span></span> <span data-ttu-id="1140b-108">Esses usuários de teste são um par de usuários que foram pré-configurados para uso com transações sintéticas.</span><span class="sxs-lookup"><span data-stu-id="1140b-108">These test users are a pair of users who were preconfigured for use with synthetic transactions.</span></span> <span data-ttu-id="1140b-109">(Geralmente são contas de teste e não contas que pertencem a usuários reais.) Com os usuários de teste configurados para um pool, você pode executar uma transação sintéticada nesse pool sem ter que especificar as identidades de (e fornecer as credenciais) das contas de usuário envolvidas no teste.</span><span class="sxs-lookup"><span data-stu-id="1140b-109">(Typically these are test accounts and not accounts that belong to actual users.) With test users configured for a pool, you can run a synthetic transaction against that pool without having to specify the identities of (and supply the credentials for) the user accounts involved in the test.</span></span>

<span data-ttu-id="1140b-110">Ou você pode executar uma transação sintética usando contas de usuário reais.</span><span class="sxs-lookup"><span data-stu-id="1140b-110">Or, you can run a synthetic transaction by using actual user accounts.</span></span> <span data-ttu-id="1140b-111">Por exemplo, se dois usuários não conseguem trocar mensagens de chat, você pode executar uma transação sintética usando essas duas contas de usuário (em vez de um par de contas de teste) e, em seguida, tentar diagnosticar e solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="1140b-111">For example, if two users cannot exchange instant messages, you could run a synthetic transaction using those two user accounts (instead of a pair of test accounts), and then try to diagnose and resolve the issue.</span></span> <span data-ttu-id="1140b-112">Se você decidir conduzir uma transação sintética usando contas de usuário reais, deverá fornecer os nomes de logon e senhas para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="1140b-112">If you decide to conduct a synthetic transaction using actual user accounts, you must supply the logon names and passwords for each user.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="1140b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="1140b-113">See Also</span></span>


[<span data-ttu-id="1140b-114">Configurando os usuários de teste de nó do Inspetor e configurações de configuração no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1140b-114">Configuring watcher node test users and configuration settings in Lync Server 2013</span></span>](lync-server-2013-configuring-watcher-node-test-users-and-configuration-settings.md)  
[<span data-ttu-id="1140b-115">Instruções de configuração especiais para transações sintéticas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1140b-115">Special setup instructions for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md)  
  

<span data-ttu-id="1140b-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1140b-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

