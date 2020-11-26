---
title: Migração do Lync Server 2010, Chat em Grupo ou Office Communications Server 2007 R2 Group Chat para Lync Server 2013, Servidor de Chat Persistente
description: Migração do Lync Server 2010, chat em grupo ou Office Communications Server 2007 R2 Grupo chat para o Lync Server 2013, servidor de chat persistente.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446854"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a>Migração do Lync Server 2010, Chat em Grupo ou Office Communications Server 2007 R2 Group Chat para Lync Server 2013, Servidor de Chat Persistente

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-10-06_

Os tópicos desta seção guiam você pelo processo de migração do Lync Server 2010, do chat em grupo ou do Office Communications Server 2007 R2 Group Chat para o Lync Server 2013, servidor de chat persistente. Se você pretende que o seu Lync Server 2013, a implantação persistente do servidor de chat coexista com um Lync Server 2010, o chat em grupo ou o Office Communications Server 2007 R2 implantação de chat em grupo, este guia também inclui algumas informações essenciais para operar nesse ambiente misto. Este guia se concentra principalmente na migração de dados para o servidor de chat persistente. Para os usuários que estão migrando de versões herdadas do Lync Server para o Lync Server 2013, confira [migrar do Lync server 2010 para o Lync server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) e [migrar do Office communications Server 2007 R2 para o Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).

<div>


> [!IMPORTANT]  
> Este tópico pressupõe que você já instalou o Lync Server 2013 em coexistência com o Lync Server 2010 ou o Office Communications Server 2007 R2.



</div>

<div>


> [!IMPORTANT]  
> Este guia descreve as etapas geralmente necessárias para realizar cada fase da migração. Ele não trata cada possível topologia de implantação herdada ou todos os possíveis cenários de migração. Portanto, talvez você não precise executar todas as etapas descritas ou talvez seja necessário executar etapas adicionais, dependendo da sua implantação. O guia também fornece exemplos de etapas de verificação. Essas etapas de verificação são fornecidas para ajudá-lo a entender o que você precisa ter para se certificar de que cada fase seja concluída com êxito enquanto avança pela migração. Você pode modificar essas etapas de verificação para seu processo de migração específico.



</div>

Este guia fornece informações específicas para atualizar sua implantação existente. Ele não explica como alterar a topologia existente. Este guia não aborda a implementação de novos recursos. Quando um procedimento detalhado for documentado em outro lugar, este guia direcionará você para a seção do documento ou documento apropriado.

Este documento define termos conforme especificado na lista a seguir.

  - *migração*  
    Mover a implantação de uma versão anterior do servidor de chat persistente, anteriormente conhecida como servidor de chat em grupo, para o Lync Server 2013, servidor de chat persistente.

<!-- end list -->

  - *atualização*  
    Instalar uma versão mais recente do software em um computador cliente ou servidor.

<!-- end list -->

  - *coexistência*  
    O ambiente temporário que existe durante a migração, quando alguma funcionalidade foi migrada para o Lync Server 2013, servidor de chat persistente e outras funcionalidades ainda permanecem em uma versão anterior do servidor de chat de grupo.

O servidor de chat persistente é uma extensão da infraestrutura do Lync Server 2013. Dependendo da sua topologia, você pode migrar o Lync Server 2010, o chat em grupo ou o Office Communications Server 2007 R2 Grupo chat para o Lync Server 2013 servidor de chat persistente. Para obter detalhes sobre topologias disponíveis e os requisitos técnicos e de software para migração de servidor de chat em grupo, consulte [planejando o servidor de chat persistente no Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) na documentação de planejamento.

Se a sua organização exigir o suporte de conformidade, ele será automaticamente instalado em cada servidor de chat persistente. Um servidor separado não é mais necessário para a conformidade.

<div>


> [!IMPORTANT]  
> O servidor de chat persistente deve ser instalado em um sistema de arquivos NTFS para ajudar a reforçar a segurança do sistema de arquivos. FAT32 não é um sistema de arquivos com suporte para o servidor de chat persistente.<BR>Se a sua organização exigir o suporte de conformidade, ele será automaticamente instalado em cada servidor de chat persistente. Um servidor separado não é mais necessário para a conformidade. Para obter mais detalhes sobre alterações no servidor de chat persistente do Lync Server 2013 &nbsp; , consulte <A href="lync-server-2013-new-persistent-chat-server-features.md">novos recursos persistentes do servidor de chat no lync Server 2013</A> na documentação de introdução.



</div>

<div>

## <a name="in-this-section"></a>Nesta seção

  - [Cenário de migração padrão - nível alto](standard-migration-scenario-high-level.md)

  - [Processo de migração - detalhes](migration-process-details.md)

  - [Considerações de coexistência](coexistence-considerations.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

