---
title: 'Lync Server 2013: criar uma política de arquivamento para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sites ou usuários específicos'
description: 'Lync Server 2013: criar uma política de arquivamento para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sites ou usuários específicos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431985"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a>Criar uma política de arquivamento no Lync Server 2013 para habilitar ou desabilitar o arquivamento de comunicações internas ou externas para sites ou usuários específicos

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-23_

No Lync Server 2013, você usa políticas para habilitar e desabilitar o arquivamento para comunicações internas e comunicações externas para usuários hospedados no Lync Server 2013. Isso inclui as seguintes políticas de arquivamento:

  - Uma política global criada por padrão quando você implanta o Lync Server 2013.

  - Políticas opcionais no nível do site e no nível do usuário que você pode criar e usar para especificar como o arquivamento é implementado para sites ou usuários específicos.

Inicialmente, você define as políticas de arquivamento ao implantar o arquivamento, mas pode alterar, adicionar e excluir políticas após a implantação. No painel de controle do Lync Server 2013, você pode usar a página **política de arquivamento** do grupo **arquivamento e monitoramento** para gerenciar políticas em nível global, nível de site e nível de usuário. Se você integrar o armazenamento do Lync Server ao armazenamento do Exchange 2013, as políticas de usuário do Exchange terão precedência sobre as políticas de arquivamento do Lync Server 2013.

Para obter detalhes sobre como as políticas são implementadas, incluindo a hierarquia de políticas, consulte [como o arquivamento funciona no Lync Server 2013](lync-server-2013-how-archiving-works.md) na documentação de planejamento, documentação de implantação ou documentação de operações.

<div>


> [!NOTE]
> Para controlar a implementação do arquivamento, você deve especificar opções em configurações de arquivamento, como se deseja arquivar mensagens instantâneas ou conferências, o uso do modo crítico e as opções de limpeza. Por padrão, nenhuma opção é habilitada na configuração de arquivamento global ou em qualquer configuração de arquivamento de site ou de pool. Você deve especificar todas as opções adequadas nas configurações de arquivamento antes de habilitar o arquivamento para comunicações internas ou externas nas políticas de arquivamento. Para obter detalhes, consulte <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Gerenciando opções de configuração de arquivamento no Lync Server 2013 para sua organização, sites e pools</A> na documentação de operações.<BR>Se você tiver habilitado a integração do Microsoft Exchange para a implantação, as políticas do Exchange controlarão se o arquivamento está habilitado para os usuários que são hospedados no Exchange 2013 e ter suas caixas de correio colocadas em In-Place isenção. Para obter detalhes, consulte <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Configurando políticas para arquivamento no Lync server 2013 ao usar a integração com o Exchange Server</A> na documentação de implantação.



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a>Para criar uma política de arquivamento para um site ou usuários

1.  Usando uma conta de usuário atribuída à função CsArchivingAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.

2.  Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server. Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Na barra de navegação da esquerda, clique em **Monitoramento e Arquivamento**, e depois, clique em **Política de Arquivamento**.

4.  Clique em **Novo** e execute uma das seguintes ações:
    
      - Para criar uma política de arquivamento no nível do site, clique em **política do site** e, em **Selecione um site**, clique no site ao qual a política deve ser aplicada.
    
      - Para criar uma política de arquivamento em nível do usuário, clique em **Política de usuário**.

5.  Em **Nova Política de Arquivamento**, faça o seguinte:
    
      - Em **Nome**, especifique um nome para a nova política (por exemplo, externalContoso).
    
      - Em **Descrição**, forneça os detalhes sobre a política (por exemplo, a política de arquivamento de usuário externo da Contoso).
    
      - Para controlar o arquivamento das comunicações com usuários internos, marque ou desmarque a caixa de seleção **Arquivar comunicações internas**.
    
      - Para controlar o arquivamento das comunicações com usuários externos, marque ou desmarque a caixa de seleção **Arquivar comunicações externas**.

6.  Clique em **Confirmar**.
    
    <div>
    

    > [!IMPORTANT]
    > As configurações de uma política do usuário se aplicam somente a usuários específicos e grupos de usuários aos quais você aplica a política. Para obter detalhes, consulte <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">aplicando uma política de arquivamento a usuários no Lync Server 2013</A>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a>Criando uma política de arquivamento usando cmdlets do Windows PowerShell

As políticas de arquivamento podem ser criadas usando o Windows PowerShell e o cmdlet **Remove-CsArchivingPolicy** . Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell. Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a>Para criar uma nova política de arquivamento no escopo do site

  - Este comando cria uma nova política de arquivamento para o site de Redmond:
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a>Para criar uma nova política de arquivamento no escopo por usuário

  - Para criar uma nova política de arquivamento no escopo por usuário, basta especificar uma identidade exclusiva ao criar a política:
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a>Para criar uma nova política de arquivamento que permita o arquivamento de sessões de comunicação interna

  - Como nenhum parâmetros foi especificado (além do parâmetro obrigatório Identity) nos comandos anteriores, as novas políticas utilizarão os valores padrão para todas as suas propriedades. Para criar políticas que utilizam valores de propriedades diferentes, basta incluir o parâmetro e o valor de parâmetro apropriado. Por exemplo, para criar uma política de arquivamento que permita o arquivamento de sessões de mensagens instantâneas internas, use um comando como este:
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a>Para criar uma nova política de arquivamento que permita o arquivamento de sessões de comunicação interna e externa

  - Vários valores de propriedade podem ser modificados, incluindo vários parâmetros. Por exemplo, esse comando configura a nova política para arquivar sessões de mensagens instantâneas internas e externas:
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

Para obter mais informações, consulte o tópico da ajuda para o cmdlet [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .

</div>

<div>

## <a name="see-also"></a>Confira também


[Gerenciar o arquivamento de comunicações internas e externas no Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

