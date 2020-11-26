---
title: 'Lync Server 2013: Configurando políticas de site para arquivamento'
description: 'Lync Server 2013: configurar políticas de site para arquivar.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up site policies for Archiving
ms:assetid: dc2ea206-8b9c-44dd-a479-efb217593c89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205325(v=OCS.15)
ms:contentKeyID: 48185613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 27e5b80b7f62ddc18d418415307457c7f2c4010d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441687"
---
# <a name="setting-up-site-policies-for-archiving-in-lync-server-2013"></a>Configurando políticas de site para arquivamento no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-09_

Você pode habilitar ou desabilitar o arquivamento de sites específicos criando e configurando uma política de arquivamento para cada um desses sites. Uma política de local substitui a política global, mas as políticas de usuário substituem as políticas de local. As políticas de arquivamento só se aplicam se você não usar a integração com o Microsoft Exchange ou se usar a integração do Microsoft Exchange, mas tiver alguns usuários que não são hospedados no Exchange 2013 e ter suas caixas de correio colocadas em In-Place isenção.

Para obter detalhes sobre como as políticas de arquivamento funcionam, incluindo a hierarquia para políticas globais, de site e de usuário, consulte [como o arquivamento funciona na documentação de planejamento do Lync Server 2013](lync-server-2013-how-archiving-works.md) , documentação de implantação ou documentação de operações.

<div>


> [!NOTE]  
> Se você habilitar a integração do Microsoft Exchange para a implantação, as políticas de retenção do Exchange In-Place controlam se o arquivamento está habilitado para os usuários hospedados no Exchange 2013 e se as caixas de correio são colocadas In-Place isenção. Para obter detalhes, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Configurando políticas para arquivamento no Lync server 2013 ao usar a integração com o Exchange Server</A> na documentação de implantação.<BR>Você deve especificar todas as opções adequadas nas configurações de Arquivamento antes de habilitar o Arquivamento de comunicações externas ou internas nas políticas de Arquivamento. Para obter detalhes, consulte <A href="lync-server-2013-configuring-archiving-options.md">Configurando opções de arquivamento no Lync Server 2013</A> na documentação de implantação.



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site"></a>Para criar uma política de arquivamento para um site

1.  Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.

2.  Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server 2013.

3.  Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Política de Arquivamento**.
    
    Para obter detalhes sobre como as políticas de arquivamento funcionam, incluindo a hierarquia para políticas globais, de site e de usuário, consulte [como o arquivamento funciona na documentação de planejamento do Lync Server 2013](lync-server-2013-how-archiving-works.md) , documentação de implantação ou documentação de operações.

4.  Clique em **Nova** e em **Política de local**.

5.  Em **Selecionar um local**, clique no local ao qual a política deve ser aplicada.

6.  Em **Nova Política de Arquivamento**, faça o seguinte:
    
      - Em **Nome**, especifique um nome para a política do local.
    
      - Em **Descrição**, forneça as informações sobre a política de local (por exemplo, a política de local para Redmond).
    
      - Para controlar o arquivamento das comunicações internas do local especificado, marque ou desmarque a caixa de seleção **Arquivar comunicações internas**.
    
      - Para controlar o arquivamento das comunicações externas do local especificado, marque ou desmarque a caixa de seleção **Arquivar comunicações externas**.

7.  Clique em **Confirmar**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

