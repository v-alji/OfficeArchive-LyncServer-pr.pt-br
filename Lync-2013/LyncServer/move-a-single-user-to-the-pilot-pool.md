---
title: Mover um único usuário para o pool piloto
description: Mover um único usuário para o pool piloto.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move a single user to the pilot pool
ms:assetid: e9de81a8-40dd-4446-81e7-a2b810eaea50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205401(v=OCS.15)
ms:contentKeyID: 48185905
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5f7396ed2d92c7015f01ff6cd6e90fd3998219d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389935"
---
# <a name="move-a-single-user-to-the-pilot-pool"></a><span data-ttu-id="5b64b-103">Mover um único usuário para o pool piloto</span><span class="sxs-lookup"><span data-stu-id="5b64b-103">Move a single user to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b64b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b64b-104">

<span> </span></span></span>

<span data-ttu-id="5b64b-105">_**Tópico da última modificação:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="5b64b-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="5b64b-106">Você pode mover um usuário do pool do Lync Server 2010 para o pool piloto do Lync Server 2013 usando o painel de controle do Lync Server 2013 ou o Shell de gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b64b-106">You can move a user from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="5b64b-107">No exemplo a seguir, na coluna pool de registradores, **pool01.contoso.net** é o pool do Lync Server 2010 e todos os seis usuários estão conectados a esse pool.</span><span class="sxs-lookup"><span data-stu-id="5b64b-107">In the example below, in the Registrar pool column, **pool01.contoso.net** is the Lync Server 2010 pool, and all six of these users are connected to this pool.</span></span> <span data-ttu-id="5b64b-108">Use os procedimentos a seguir para mover um usuário para o pool do Lync Server 2013 usando o painel de controle do Lync Server 2013 e o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5b64b-108">Use the following procedures to move a user to your Lync Server 2013 pool using Lync Server 2013 Control Panel and Lync Server Management Shell.</span></span>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="5b64b-109">Para mover um usuário usando o painel de controle do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b64b-109">To move a user by using the Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="5b64b-110">**Lista de usuários no painel de controle do Lync Server 2013**</span><span class="sxs-lookup"><span data-stu-id="5b64b-110">**List of users in the Lync Server 2013 Control Panel**</span></span>

<span data-ttu-id="5b64b-111">![Painel de controle do Lync Server, caixa de diálogo mover usuário](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Painel de controle do Lync Server, caixa de diálogo mover usuário")</span><span class="sxs-lookup"><span data-stu-id="5b64b-111">![Lync Server Control Panel, Move User dialog](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server Control Panel, Move User dialog")</span></span>

1.  <span data-ttu-id="5b64b-112">Faça logon no Servidor Front-end com uma conta que seja membro do grupo de RTCUniversalServerAdmins ou membro da função administrativa do CsAdministrator ou CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="5b64b-112">Log on to the Front End Server with an account that is a member of the RTCUniversalServerAdmins group or a member of the CsAdministrator or CsUserAdministrator administrative role.</span></span>

2.  <span data-ttu-id="5b64b-113">Abra o **Painel de Controle do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="5b64b-113">Open **Lync Server Control Panel**.</span></span>

3.  <span data-ttu-id="5b64b-114">Clique em **Usuários**, em Pesquisar e em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="5b64b-114">Click **Users**, click Search, and then click **Find**.</span></span>

4.  <span data-ttu-id="5b64b-115">Selecione o usuário que você deseja mover para o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b64b-115">Select a user that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="5b64b-116">Neste exemplo, moveremos a usuária Sara Davis.</span><span class="sxs-lookup"><span data-stu-id="5b64b-116">In this example, we will move user Sara Davis.</span></span>

5.  <span data-ttu-id="5b64b-117">No menu **Ação**, selecione **Mover usuários selecionados para o pool**.</span><span class="sxs-lookup"><span data-stu-id="5b64b-117">On the **Action** menu, select **Move selected users to pool**.</span></span>

6.  <span data-ttu-id="5b64b-118">Na lista suspensa, selecione o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b64b-118">From the drop-down list, select the Lync Server 2013 pool.</span></span>

7.  <span data-ttu-id="5b64b-119">Clique em **Ação** e em **Mover usuários selecionados para o pool**.</span><span class="sxs-lookup"><span data-stu-id="5b64b-119">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="5b64b-120">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b64b-120">Click **OK**.</span></span>
    
    <span data-ttu-id="5b64b-121">![Caixa de diálogo mover usuários, pool de registradores de destino](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Caixa de diálogo mover usuários, pool de registradores de destino")</span><span class="sxs-lookup"><span data-stu-id="5b64b-121">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

8.  <span data-ttu-id="5b64b-122">Verifique se a coluna do **pool de registradores** do usuário agora contém o pool do Lync Server 2013, que indica que o usuário foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="5b64b-122">Verify that the **Registrar pool** column for the user now contains the Lync Server 2013 pool, which indicates that the user has been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="5b64b-123">Para mover um usuário usando o Shell de gerenciamento do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b64b-123">To move a user by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="5b64b-124">Abra o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5b64b-124">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="5b64b-125">Na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5b64b-125">At the command line, type the following:</span></span>
    
        Move-CsUser -Identity "David Pelton" -Target "pool02.contoso.net"

3.  <span data-ttu-id="5b64b-126">Em seguida, na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5b64b-126">Next, at the command line, type the following:</span></span>
    
        Get-CsUser -Identity "David Pelton"

4.  <span data-ttu-id="5b64b-127">A identidade **RegistrarPool** agora aponta para o pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b64b-127">The **RegistrarPool** identity now points to the Lync Server 2013 pool.</span></span> <span data-ttu-id="5b64b-128">A presença dessa identidade confirma que o usuário foi movido com êxito.</span><span class="sxs-lookup"><span data-stu-id="5b64b-128">The presence of this identity confirms that the user has been successfully moved.</span></span>
    
    <span data-ttu-id="5b64b-129">![Saída do cmdlet Get-CsUser com o filtro de identidade](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Saída do cmdlet Get-CsUser com o filtro de identidade")</span><span class="sxs-lookup"><span data-stu-id="5b64b-129">![Output from Get-CsUser cmdlet with Identity filter](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Output from Get-CsUser cmdlet with Identity filter")</span></span>  
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5b64b-130">Para obter detalhes sobre o cmdlet <STRONG>Get-CsUser</STRONG> , execute: <STRONG>Get-Help Get-CsUser – detailed</STRONG></span><span class="sxs-lookup"><span data-stu-id="5b64b-130">For details about the <STRONG>Get-CsUser</STRONG> cmdlet, run: <STRONG>Get-Help Get-CsUser –Detailed</STRONG></span></span>

    
    <span data-ttu-id="5b64b-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b64b-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

