---
title: 'Lync Server 2013: Definir configurações de conta do usuário'
description: 'Lync Server 2013: configurar configurações de conta de usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure user account settings
ms:assetid: b7c74ecc-b924-4efc-8a56-3a5f94a9ef13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412896(v=OCS.15)
ms:contentKeyID: 48185200
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e6ab4c57ba3d3e8c084314e1093736334312d0c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390409"
---
# <a name="configure-user-account-settings-in-lync-server-2013"></a><span data-ttu-id="f0805-103">Definir configurações de conta do usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0805-103">Configure user account settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0805-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0805-104">

<span> </span></span></span>

<span data-ttu-id="f0805-105">_**Tópico da última modificação:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="f0805-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="f0805-106">Os usuários de discagem digitam o número de telefone ou a extensão e um PIN para participar nas conferências como usuários autenticados.</span><span class="sxs-lookup"><span data-stu-id="f0805-106">Dial-in users enter their phone number or extension and a PIN to join conferences as authenticated users.</span></span> <span data-ttu-id="f0805-107">O **URI de linha** de telefonia especificado nas contas de usuário do Lync Server é necessário para autenticação.</span><span class="sxs-lookup"><span data-stu-id="f0805-107">The telephony **Line URI** specified on Lync Server user accounts is required for authentication.</span></span>

<span data-ttu-id="f0805-108">O procedimento neste tópico descreve como atribuir um **URI da Linha** para uma única conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f0805-108">The procedure in this topic describes how to assign a **Line URI** for a single user account.</span></span> <span data-ttu-id="f0805-109">Se você precisar atribuir um **URI da Linha** para várias contas de usuários, poderá criar um script que usa o cmdlet **Set-CsUser**.</span><span class="sxs-lookup"><span data-stu-id="f0805-109">If you need to assign a **Line URI** for multiple user accounts, you can create a script that uses the **Set-CsUser** cmdlet.</span></span> <span data-ttu-id="f0805-110">Para obter detalhes sobre como usar um exemplo de script para atribuir **URI de linha** a várias contas de usuário, consulte "atribuir URIs de linha a vários usuários" em [https://go.microsoft.com/fwlink/p/?linkId=196945](https://go.microsoft.com/fwlink/p/?linkid=196945) .</span><span class="sxs-lookup"><span data-stu-id="f0805-110">For details about using a sample script to assign **Line URI** to multiple user accounts, see "Assign Line URIs to Multiple Users" at [https://go.microsoft.com/fwlink/p/?linkId=196945](https://go.microsoft.com/fwlink/p/?linkid=196945).</span></span>

<div>

## <a name="to-configure-user-account-settings"></a><span data-ttu-id="f0805-111">Para definir configurações de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="f0805-111">To configure user account settings</span></span>

1.  <span data-ttu-id="f0805-112">Faça logon no computador como membro do grupo RTCUniversalServerAdmins ou como membro da função **Cs-UserAdministrator** ou **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="f0805-112">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-UserAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="f0805-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f0805-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f0805-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f0805-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f0805-115">Na barra de navegação esquerda, clique em **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="f0805-115">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="f0805-116">No campo de pesquisa, digite o nome do usuário que você deseja configurar para conferência discada ou clique em **Adicionar filtro** para especificar os campos de pesquisa e clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="f0805-116">In the search field, type the name of the user you want to configure for dial-in conferencing or click **Add filter** to specify search fields, and then click **Find**.</span></span>

5.  <span data-ttu-id="f0805-117">Clique duas vezes no nome do usuário para abrir a caixa de diálogo **Editar usuário do Lync Server** .</span><span class="sxs-lookup"><span data-stu-id="f0805-117">Double-click the user name to open the **Edit Lync Server User** dialog box.</span></span>

6.  <span data-ttu-id="f0805-118">Em **Telefonia**, no campo **URI da Linha**, digite um número de telefone exclusivo e normalizado (por exemplo, tel:+14255550200).</span><span class="sxs-lookup"><span data-stu-id="f0805-118">Under **Telephony**, in the **Line URI** field, type a unique, normalized phone number (for example, tel:+14255550200).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f0805-119">Você pode especificar o <STRONG>URI de linha</STRONG> somente se <STRONG>Telefonia</STRONG> estiver definida como <STRONG>Somente PC para PC</STRONG>, <STRONG>Enterprise Voice</STRONG>,  <STRONG>Controle de chamada remota</STRONG> ou <STRONG>Somente controle de chamada remota</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f0805-119">You can specify <STRONG>Line URI</STRONG> only if <STRONG>Telephony</STRONG> is set to <STRONG>PC-to-PC only</STRONG>, <STRONG>Enterprise Voice</STRONG>, <STRONG>Remote call control</STRONG> or <STRONG>Remote call control only</STRONG>.</span></span>

    
    </div>

7.  <span data-ttu-id="f0805-120">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="f0805-120">Click **Commit**.</span></span>

<span data-ttu-id="f0805-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0805-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

