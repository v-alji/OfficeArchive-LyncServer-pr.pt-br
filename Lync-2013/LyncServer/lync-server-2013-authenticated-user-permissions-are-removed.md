---
title: 'Lync Server 2013: Permissões de usuário autenticado são removidas'
description: 'Lync Server 2013: as permissões do usuário autenticado são removidas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Authenticated user permissions are removed
ms:assetid: 5fcd70a5-813a-4076-9bb6-5b0d47505038
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398425(v=OCS.15)
ms:contentKeyID: 48184304
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59da0ec893395405010afdd0263bd6be5d646881
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438152"
---
# <a name="authenticated-user-permissions-are-removed-in-lync-server-2013"></a>Permissões de usuário autenticado são removidas no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-21_

Em um ambiente bloqueado do Active Directory, as entradas de controle de acesso (ACEs) do usuário autenticado são removidas dos recipientes padrão do Active Directory, incluindo usuários, configuração ou sistema e unidades organizacionais (UOs) onde os objetos de usuário e computador são armazenados. A remoção de ACEs de usuários autenticados impede o acesso de leitura às informações do Active Directory. No entanto, a remoção das ACEs cria problemas para o Lync Server 2013 porque depende das permissões de leitura para esses contêineres para permitir que os usuários executem a preparação do domínio.

Nessa situação, a associação no grupo Domain admins, que é necessária para executar a preparação do domínio, a ativação do servidor e a criação de pool, não concede mais acesso de leitura às informações do Active Directory armazenadas nos contêineres padrão. Você deve conceder manualmente permissões de acesso de leitura em vários recipientes do domínio raiz da floresta para verificar se o procedimento de preparação da floresta de pré-requisito está concluído.

Para permitir que um usuário execute a preparação do domínio, a ativação do servidor ou a criação de pool em qualquer domínio raiz que não seja da floresta, você tem as seguintes opções:

  - Use uma conta que seja um membro do grupo Administradores da empresa para executar a preparação do domínio.

  - Use uma conta que seja um membro do grupo Domain admins e conceda esta conta às permissões de leitura de conta em cada um dos seguintes recipientes no domínio raiz da floresta:
    
      - Domínio
    
      - Configuração ou sistema

Se você não quiser usar uma conta que seja membro do grupo Administradores da empresa para executar a preparação do domínio ou outras tarefas de configuração, conceda explicitamente à conta que você deseja usar o acesso de leitura nos contêineres relevantes na raiz da floresta.

<div>

## <a name="to-give-users-read-access-permissions-on-containers-in-the-forest-root-domain"></a>Para conceder aos usuários permissões de acesso de leitura em contêineres no domínio raiz da floresta

1.  Faça logon no computador associado ao domínio raiz da floresta com uma conta que seja membro do grupo Domain admins do domínio raiz da floresta.

2.  Execute ADSIEdit. msc para o domínio raiz da floresta.
    
    Se as ACEs do usuário autenticado tiverem sido removidas do contêiner de domínio, configuração ou sistema, você deverá conceder permissões somente leitura para o contêiner, conforme descrito nas etapas a seguir.

3.  Clique com o botão direito do mouse no contêiner e, em seguida, clique em **Propriedades**.

4.  Clique na guia **segurança** .

5.  Clique em **Avançado**.

6.  Na guia **permissões** , clique em **Adicionar**.

7.  Digite o nome do usuário ou do grupo permissões de recebimento usando o seguinte formato: `domain\account name` e clique em **OK**.

8.  Na guia **objetos** , em **aplica-se a**, clique **somente neste objeto**.

9.  Em **permissões**, selecione as seguintes ACEs de permissão clicando no botão **permitir** coluna: **listar o conteúdo**, **ler todas as propriedades** e **ler permissões**.

10. Clique em **OK** duas vezes.

11. Repita essas etapas para qualquer um dos recipientes relevantes listados na etapa 2.

</div>

</div>

<span> </span>

</div>

</div>

</div>

