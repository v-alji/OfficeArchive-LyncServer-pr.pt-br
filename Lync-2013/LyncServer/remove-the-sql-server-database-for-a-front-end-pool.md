---
title: Remover o banco de dados do Servidor SQL para um pool Front-End
description: Remover o banco de dados do SQL Server de um pool de front-ends.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Front End pool
ms:assetid: 6bb932df-3ed7-49b6-ae17-61e4c6a5fe82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688084(v=OCS.15)
ms:contentKeyID: 49733681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c5d47e4c52197c5792fa3b7770da7bbd1b26cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390414"
---
# <a name="remove-the-sql-server-database-for-a-front-end-pool"></a>Remover o banco de dados do Servidor SQL para um pool Front-End

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-04_

Depois de remover um pool de front-end do Microsoft Lync Server 2010 ou reconfigurar o pool para usar um banco de dados diferente, você pode remover os bancos de dados do SQL Server que hospedavam os dados do pool. Use os procedimentos a seguir para remover as definições do construtor de topologias e, em seguida, remover os arquivos de banco de dados e de log do servidor de banco de dados.

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a>Para remover o banco de dados do SQL Server usando o construtor de topologias

1.  No servidor front-end do Lync Server 2013, abra o construtor de topologias e baixe a topologia existente.

2.  No construtor de topologias, navegue até **componentes compartilhados** e, em seguida, **repositórios do SQL Server**, clique com o botão direito do mouse na instância do SQL Server associada ao pool de front-end removido ou reconfigurado e clique em **excluir**.

3.  Publique a topologia e verifique o status de replicação.

</div>

<div>

## <a name="to-remove-user-and-application-databases-from-the-sql-server"></a>Para Remover bancos de dados de usuários e aplicativos do SQL Server

1.  Para remover os bancos de dados no SQL Server, você deve ser membro do grupo Administradores do SQL Server do SQL Server no qual está removendo os arquivos de banco de dados.

2.  Abrir o Shell de gerenciamento do Lync Server

3.  Para remover o banco de dados do armazenamento de usuários do pool, digite:
    
        Uninstall-CsDataBase -DatabaseType User -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    Onde \<FQDN\> é o nome de domínio totalmente qualificado (FQDN) do servidor de banco de dados e \<instance\> é a instância do banco de dados nomeado (ou seja, se um foi definido).

4.  Para remover o banco de dados do repositório de aplicativos do pool, digite:
    
        Uninstall-CsDataBase -DatabaseType Application -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    Onde \<FQDN\> é o FQDN do servidor de banco de dados e \<instance\> é a instância do banco de dados nomeado (ou seja, se um foi definido).

5.  Quando o cmdlet **Uninstall-CsDataBase** solicita que você confirme ações, leia as informações e, em seguida, pressione **Y** (ou pressione Enter) para continuar, ou pressione **N** e, em seguida, insira se você deseja parar o cmdlet (ou seja, em caso de erros).

</div>

</div>

<span> </span>

</div>

</div>

</div>

