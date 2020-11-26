---
title: 'Lync Server 2013: restaurar dados de monitoramento ou arquivamento'
description: 'Lync Server 2013: restaurando o monitoramento ou o arquivamento de dados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring monitoring or archiving data
ms:assetid: 60118526-13bb-4b03-803e-6ffae219d436
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202175(v=OCS.15)
ms:contentKeyID: 51541483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 169a5da2d606b97c7cd3f59d6cbae3d4c584e6e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442520"
---
# <a name="restoring-monitoring-or-archiving-data-in-lync-server-2013"></a><span data-ttu-id="26eaa-103">Restaurando o monitoramento ou arquivando dados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26eaa-103">Restoring monitoring or archiving data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26eaa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26eaa-104">

<span> </span></span></span>

<span data-ttu-id="26eaa-105">_**Tópico da última modificação:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="26eaa-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="26eaa-106">Não é necessário restaurar os dados de monitoramento e arquivamento para colocar o Lync Server em funcionamento após uma falha.</span><span class="sxs-lookup"><span data-stu-id="26eaa-106">Restoring monitoring and archiving data is not required to get Lync Server up and running after a failure.</span></span> <span data-ttu-id="26eaa-107">No entanto, se o monitoramento e o arquivamento de dados forem críticos para a sua organização, você desejará restaurar os dados após recriar os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="26eaa-107">However, if monitoring and archiving data is critical to your organization, you will want to restore the data after you re-create the databases.</span></span>

<span data-ttu-id="26eaa-108">O procedimento a seguir descreve como usar o SQL Server Management Studio para restaurar o arquivamento ou o monitoramento de dados.</span><span class="sxs-lookup"><span data-stu-id="26eaa-108">The following procedure describes how to use SQL Server Management Studio to restore archiving or monitoring data.</span></span>

<div>

## <a name="to-restore-monitoring-or-archiving-data-from-a-backup-file"></a><span data-ttu-id="26eaa-109">Para restaurar o monitoramento ou o arquivamento de dados de um arquivo de backup</span><span class="sxs-lookup"><span data-stu-id="26eaa-109">To restore monitoring or archiving data from a backup file</span></span>

1.  <span data-ttu-id="26eaa-110">Faça logon no servidor que você está restaurando como membro do grupo Administradores no computador local ou em um grupo com direitos de usuário equivalentes.</span><span class="sxs-lookup"><span data-stu-id="26eaa-110">Log on to the server that you are restoring as a member of the Administrators group on the local computer or a group with equivalent user rights.</span></span>

2.  <span data-ttu-id="26eaa-111">Abra o SQL Server Management Studio: clique em **Iniciar**, em **todos os programas**, em **Microsoft SQL Server 2012** ou **Microsoft SQL Server 2008 R2** e, em seguida, clique em **SQL Server Management Studio**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-111">Open SQL Server Management Studio: click **Start**, click **All Programs**, click **Microsoft SQL Server 2012** or **Microsoft SQL Server 2008 R2**, and then click **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="26eaa-112">Em **conectar-se ao servidor**, conecte-se à instância do SQL Server fornecendo pelo menos o nome do servidor e as informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="26eaa-112">In **Connect to Server**, connect to the SQL Server instance by providing at least the name of the server and the authentication information.</span></span>

4.  <span data-ttu-id="26eaa-113">No **Explorador de objetos**, clique com o botão direito do mouse em **bancos** de dados e clique em **restaurar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-113">In **Object Explorer**, right-click **Databases**, and then click **Restore Database**.</span></span>

5.  <span data-ttu-id="26eaa-114">Em **Selecione uma página**, clique em **geral** e, em seguida, no **banco de dados** , selecione o nome do banco de dados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="26eaa-114">Under **Select a page**, click **General**, and then in **To database** select the database name as follows:</span></span>
    
      - <span data-ttu-id="26eaa-115">Para um banco de dados de arquivamento, selecione **LcsLog**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-115">For an Archiving database, select **LcsLog**.</span></span>
    
      - <span data-ttu-id="26eaa-116">Para um banco de dados do recurso de gravação de detalhes de chamadas (CDR), selecione **LcsCDR**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-116">For a call detail recording (CDR) database, select **LcsCDR**.</span></span>
    
      - <span data-ttu-id="26eaa-117">Para um banco de dados de qualidade da experiência (QoE), selecione **QoEMetrics**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-117">For a Quality of Experience (QoE) database, select **QoEMetrics**.</span></span>

6.  <span data-ttu-id="26eaa-118">Clique em **do dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-118">Click **From device**.</span></span>

7.  <span data-ttu-id="26eaa-119">Em **Selecione os conjuntos de backup a serem restaurados**, clique no arquivo de backup e, em seguida, clique em **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-119">Under **Select the backup sets to restore**, click the backup file, and then click **Restore**.</span></span>

8.  <span data-ttu-id="26eaa-120">Em **Selecione uma página**, clique em **Opções**, verifique se o caminho do arquivo de dados e o caminho do log estão na pasta correta e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-120">Under **Select a page**, click **Options**, verify that the data file path and log path are in the correct folder, and then click **OK**.</span></span>

</div>

<div>

## <a name="to-make-sure-that-access-control-lists-acls-are-correct"></a><span data-ttu-id="26eaa-121">Para garantir que as listas de controle de acesso (ACLs) estejam corretas</span><span class="sxs-lookup"><span data-stu-id="26eaa-121">To make sure that access control lists (ACLs) are correct</span></span>

1.  <span data-ttu-id="26eaa-122">Expanda **bancos** de dados, expanda o arquivo de arquivamento ou monitoramento, expanda **segurança** e, em seguida, expanda **usuários**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-122">Expand **Databases**, expand the archiving or monitoring database, expand **Security**, and then expand **Users**.</span></span>

2.  <span data-ttu-id="26eaa-123">Verifique se o grupo de domínio RTCComponentUniversalServices existe como usuário.</span><span class="sxs-lookup"><span data-stu-id="26eaa-123">Verify that the domain group RTCComponentUniversalServices exists as a user.</span></span>

3.  <span data-ttu-id="26eaa-124">Se RTCComponentUniversalServices não existir em **usuários**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="26eaa-124">If RTCComponentUniversalServices does not exist under **Users**, do the following:</span></span>
    
    1.  <span data-ttu-id="26eaa-125">Clique com o botão direito do mouse em **usuários** e, em seguida, clique em **novo usuário**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-125">Right-click **Users**, and then click **New User**.</span></span>
    
    2.  <span data-ttu-id="26eaa-126">Em **nome de logon**, digite o nome do grupo ausente, RTCComponentUniversalServices.</span><span class="sxs-lookup"><span data-stu-id="26eaa-126">In **Login name**, type the missing group name, RTCComponentUniversalServices.</span></span>
    
    3.  <span data-ttu-id="26eaa-127">Em **Associação de função de banco de dados**, selecione a permissão **ServerRole** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="26eaa-127">Under **Database role membership**, select the **ServerRole** permission, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="26eaa-128">Você não precisa reiniciar o serviço de arquivamento ou monitoramento.</span><span class="sxs-lookup"><span data-stu-id="26eaa-128">You do not need to restart the archiving or monitoring service.</span></span>

    
    <span data-ttu-id="26eaa-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26eaa-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

