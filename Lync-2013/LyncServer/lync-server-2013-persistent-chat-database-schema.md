---
title: 'Lync Server 2013: Esquema do banco de dados de Chat Persistente'
description: 'Lync Server 2013: esquema de banco de dados de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat database schema
ms:assetid: 58d7d94f-42f5-4c3e-8fe5-901fbe92152e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558653(v=OCS.15)
ms:contentKeyID: 48184228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 66151201f65310cc8e6d3f2251be4f86ce2be15d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389969"
---
# <a name="persistent-chat-database-schema-in-lync-server-2013"></a>Esquema do banco de dados de Chat Persistente no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-09-18_

Isso documenta o esquema do banco de dados de chat persistente no software de comunicação do Lync Server 2013.

O banco de dados de chat persistente refere-se ao banco de dados correspondente às funções de servidor back-end **PersistentChatStore** do Lync Server 2013 (correspondente ao banco de dados do MGC) e **PersistentChatComplianceStore** (correspondente ao banco de dados do mgccomp). O objetivo de publicar esse esquema é habilitá-lo para criar consultas e obter algumas ideias para criar relatórios úteis sobre uso de chat, salas ativas, principais pôsters e assim por diante.

<div>


> [!IMPORTANT]  
> Reservamo-nos o direito de desenvolver este esquema. A Microsoft não faz nenhuma garantia para manter a compatibilidade com versões anteriores do esquema publicado.



</div>

Siga estas práticas recomendadas:

  - Não há \* suporte para Select//is porque a lista de colunas pode aumentar.

  - Não há suporte para modificações de esquema geradas pelo usuário.

  - Não há suporte para operações de gravação.

  - Teste todas as consultas que você cria em bancos de dados de tamanho representativo para ter certeza de que as consultas podem ser executadas em um nível para atender às suas necessidades.

<div>

## <a name="in-this-section"></a>Nesta seção

  - [Tabelas de lista de Servidores de Chat Persistente no Lync Server 2013](lync-server-2013-list-of-persistent-chat-server-tables.md)

  - [Lista de tabelas de conformidade do Servidor de Chat Persistente no Lync Server 2013](lync-server-2013-list-of-persistent-chat-server-compliance-tables.md)

  - [Detalhes da tabela do Servidor de Chat Persistente no Lync Server 2013](lync-server-2013-persistent-chat-server-table-details.md)

  - [Amostragem de consultas de banco de dados de Chat Persistente para Lync Server 2013](lync-server-2013-sample-persistent-chat-database-queries.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

