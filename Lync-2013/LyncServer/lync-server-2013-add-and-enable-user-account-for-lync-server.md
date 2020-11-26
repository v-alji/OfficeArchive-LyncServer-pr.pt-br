---
title: 'Lync Server 2013: Adicionar e habilitar a conta de usuário para o Lync Server'
description: 'Lync Server 2013: Adicionar e habilitar a conta de usuário para o Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add and enable user account for Lync Server
ms:assetid: 1edd1c1c-307d-450b-abea-33aaf56bdf13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520961(v=OCS.15)
ms:contentKeyID: 48183578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f70ae2da122a0db3986a75677c1d29234fbe0e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439370"
---
# <a name="add-and-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="76fa1-103">Adicionar e habilitar a conta de usuário para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76fa1-103">Add and enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76fa1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76fa1-104">

<span> </span></span></span>

<span data-ttu-id="76fa1-105">_**Tópico da última modificação:** 2012-11-02_</span><span class="sxs-lookup"><span data-stu-id="76fa1-105">_**Topic Last Modified:** 2012-11-02_</span></span>

<span data-ttu-id="76fa1-106">Depois de habilitar uma conta de usuário em usuários e computadores do Active Directory, você pode usar o painel de controle do Lync Server para criar e habilitar as novas contas de usuário do Lync Server 2013 adicionando um usuário do Active Directory ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="76fa1-106">After enabling a user account in Active Directory Users and Computers, you can use Lync Server Control Panel to create and enable new Lync Server 2013 user accounts by adding an Active Directory user to Lync Server.</span></span>

<div>

## <a name="to-add-and-enable-a-new-lync-server-user"></a><span data-ttu-id="76fa1-107">Para adicionar e habilitar um novo usuário do Lync Server</span><span class="sxs-lookup"><span data-stu-id="76fa1-107">To add and enable a new Lync Server user</span></span>

1.  <span data-ttu-id="76fa1-108">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="76fa1-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="76fa1-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="76fa1-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="76fa1-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="76fa1-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="76fa1-111">Na barra de navegação esquerda, clique em **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="76fa1-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="76fa1-112">Clique em **habilitar usuários**.</span><span class="sxs-lookup"><span data-stu-id="76fa1-112">Click **Enable users**.</span></span>

5.  <span data-ttu-id="76fa1-113">Na caixa de diálogo **novo usuário do Lync Server** , clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="76fa1-113">On the **New Lync Server User** dialog, click **Add**.</span></span>

6.  <span data-ttu-id="76fa1-114">Na caixa **Pesquisar usuários** , digite toda ou a primeira parte do nome, nome para exibição, nome, sobrenome, nome da conta do Gerenciador de contas de segurança (Sam) nome da conta, endereço de email, nome UPN ou número de telefone da conta de usuário do Active Directory que você deseja e clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="76fa1-114">In the **Search users** box, type all or the first portion of the name, display name, first name, last name, Security Accounts Manager (SAM) account name, email address, User Principal Name (UPN), or phone number of the Active Directory user account that you want, and then click **Find**.</span></span>

7.  <span data-ttu-id="76fa1-115">Na tabela, selecione a conta que você deseja adicionar ao Lync Server e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="76fa1-115">In the table, select the account you want to add to Lync Server, and then click **OK**.</span></span>

8.  <span data-ttu-id="76fa1-116">Atribua o usuário a um pool, especifique os detalhes adicionais e atribua as políticas ao usuário desejado e, em seguida, clique em **habilitar**.</span><span class="sxs-lookup"><span data-stu-id="76fa1-116">Assign the user to a pool, specify any additional details, and assign the policies to the user you want, and then click **Enable**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="76fa1-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="76fa1-117">See Also</span></span>


[<span data-ttu-id="76fa1-118">Desabilitar ou habilitar novamente a conta de usuário para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76fa1-118">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="76fa1-119">Remover uma conta de usuário do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76fa1-119">Remove a user account from Lync Server 2013</span></span>](lync-server-2013-remove-a-user-account-from-lync-server.md)  


[<span data-ttu-id="76fa1-120">Habilitando e desabilitando usuários do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76fa1-120">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="76fa1-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76fa1-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

