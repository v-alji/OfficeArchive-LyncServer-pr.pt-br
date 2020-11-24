---
title: Criar ou modificar um conjunto de definições de configuração de atualização de dispositivos
description: Crie ou modifique um conjunto de configurações de atualização de dispositivo.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of Device Update configuration settings
ms:assetid: 3e8ce95f-a8c8-417c-b1f7-0f759a567aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994029(v=OCS.15)
ms:contentKeyID: 51803938
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593a1a0cb0f68254748ee48440cda18c78989780
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389982"
---
# <a name="create-or-modify-a-collection-of-device-update-configuration-settings-in-lync-server-2013"></a>Criar ou modificar um conjunto de definições de configuração de atualização de dispositivos no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-23_

As configurações de atualização de dispositivo podem ser criadas (somente no escopo do site) usando o Windows PowerShell e o cmdlet **New-CsDeviceUpdateConfiguration** e modificados usando o cmdlet **set-CsDeviceUpdateConfiguration** . Esses cmdlets podem ser executados no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.

<div>


> [!NOTE]
> Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


<div>

## <a name="to-create-device-update-configuration-settings-that-use-the-default-values"></a>Para criar definições de configuração de atualização de dispositivo que usam os valores padrão

  - Esse comando cria um novo conjunto de configurações de atualização de dispositivos para o site Redmond:
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond"
    
    Como nenhum parâmetro diferente do parâmetro de identidade obrigatório foi especificado no comando anterior, o novo conjunto de definições de configuração usará os valores padrão para todas as suas propriedades.

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-device-update-configuration-settings"></a>Para alterar um único valor de propriedade ao criar definições de configuração de atualização de dispositivo

  - Para criar configurações que usam valores de propriedade diferentes, basta incluir o parâmetro e valor de parâmetro adequados. Por exemplo, para criar um conjunto de configurações de atualização de dispositivo que, por padrão, exclui arquivos de log antigos a cada 21 dias, use um comando como este:
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00"

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-device-update-configuration-settings"></a>Para alterar vários valores de propriedade ao criar definições de configuração de atualização de dispositivo

  - Vários valores de propriedade podem ser modificados incluindo vários parâmetros. Por exemplo, esse comando define o intervalo de limpeza do log para 21 dias e o intervalo de liberação do log para 30 minutos:
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00" -LogFlushInterval "00:30:00"

</div>

Para obter detalhes sobre como modificar as configurações de configuração de dispositivo existentes, consulte o tópico da ajuda para o cmdlet [set-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg398320(v=OCS.15)) . Para obter detalhes sobre como criar conjuntos de definições de configuração, consulte o tópico da ajuda para o cmdlet [New-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg425761(v=OCS.15)) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

