---
title: (Recomendado) Criar diretórios de conferência
description: Usar Criar diretórios de conferências.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: (Recommended) Create Conference Directories
ms:assetid: 787f4c94-1c96-468a-a74d-e06b7bd4b8a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn832056(v=OCS.15)
ms:contentKeyID: 63146389
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b14982893fbc14a87818875a787d0f776da84ae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443262"
---
# <a name="recommended-create-conference-directories"></a>(Recomendado) Criar diretórios de conferência

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2014-10-03_

As pastas de conferência mantêm um mapeamento entre a ID de reunião alfanumérica que um participante usa para ingressar em uma conferência ao usar o Lync 2013 e a ID de conferência somente numérico que um participante de conferência discada usa para participar da conferência. O formato do ID de conferência é como segue:

    <housekeeping digit (1 digit)><conference directory (usually 1-2 digits)><conference number (variable number of digits><check digit (1 digit)>

Criar vários diretórios de conferência garantirá que os IDs de conferência sejam curtos até que uma quantidade significativa de conferências seja criada. Em uma organização com um número comum de conferências por usuário, recomendamos criar um diretório de conferência para cada 999 usuários no pool. Usando esta diretriz, as IDs de conferência geralmente podem ser mantidas pequenas. No entanto, assim que o número de diretórios de conferência (em todos os pools) ultrapassar 9, o tamanho do ID de conferência aumentará para suportar conferências adicionais.

<div>

## <a name="creating-a-conference-directory"></a>Criando um diretório de conferência

1.  No Shell de gerenciamento do Lync Server, digite o seguinte cmdlet:
    
        New-CsConferenceDirectory -Identity <XdsGlobalRelativeIdentity> -HomePool <String> [-Confirm [<SwitchParameter>]] [-Force <SwitchParameter>] [-WhatIf [<SwitchParameter>]]
    
    Por exemplo, o seguinte cria um diretório de conferência com a identidade 42, hospedada na atl-cs-001.litwareinc.com do pool:
    
        New-CsConferenceDirectory -Identity 42 -HomePool "atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a>Confira também


[Requisitos de conferência discada no Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md)  


[New-CsConferenceDirectory](https://docs.microsoft.com/powershell/module/skype/New-CsConferenceDirectory)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

