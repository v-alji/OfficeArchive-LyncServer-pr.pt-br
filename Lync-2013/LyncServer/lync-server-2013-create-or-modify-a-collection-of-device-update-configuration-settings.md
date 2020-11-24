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
# <a name="create-or-modify-a-collection-of-device-update-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="a7c95-103">Criar ou modificar um conjunto de definições de configuração de atualização de dispositivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a7c95-103">Create or modify a collection of Device Update configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a7c95-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a7c95-104">

<span> </span></span></span>

<span data-ttu-id="a7c95-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="a7c95-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="a7c95-106">As configurações de atualização de dispositivo podem ser criadas (somente no escopo do site) usando o Windows PowerShell e o cmdlet **New-CsDeviceUpdateConfiguration** e modificados usando o cmdlet **set-CsDeviceUpdateConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a7c95-106">Device update configuration settings can be created (at the site scope only) by using Windows PowerShell and the **New-CsDeviceUpdateConfiguration** cmdlet and modified by using the **Set-CsDeviceUpdateConfiguration** cmdlet.</span></span> <span data-ttu-id="a7c95-107">Esses cmdlets podem ser executados no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7c95-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="a7c95-108">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="a7c95-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="to-create-device-update-configuration-settings-that-use-the-default-values"></a><span data-ttu-id="a7c95-109">Para criar definições de configuração de atualização de dispositivo que usam os valores padrão</span><span class="sxs-lookup"><span data-stu-id="a7c95-109">To create device update configuration settings that use the default values</span></span>

  - <span data-ttu-id="a7c95-110">Esse comando cria um novo conjunto de configurações de atualização de dispositivos para o site Redmond:</span><span class="sxs-lookup"><span data-stu-id="a7c95-110">This command creates a new set of device update configuration settings for the Redmond site:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond"
    
    <span data-ttu-id="a7c95-111">Como nenhum parâmetro diferente do parâmetro de identidade obrigatório foi especificado no comando anterior, o novo conjunto de definições de configuração usará os valores padrão para todas as suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a7c95-111">Because no parameters other than the mandatory Identity parameter were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span>

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-device-update-configuration-settings"></a><span data-ttu-id="a7c95-112">Para alterar um único valor de propriedade ao criar definições de configuração de atualização de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a7c95-112">To change a single property value when creating device update configuration settings</span></span>

  - <span data-ttu-id="a7c95-113">Para criar configurações que usam valores de propriedade diferentes, basta incluir o parâmetro e valor de parâmetro adequados.</span><span class="sxs-lookup"><span data-stu-id="a7c95-113">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="a7c95-114">Por exemplo, para criar um conjunto de configurações de atualização de dispositivo que, por padrão, exclui arquivos de log antigos a cada 21 dias, use um comando como este:</span><span class="sxs-lookup"><span data-stu-id="a7c95-114">For example, to create a collection of device update configuration settings that, by default, deletes old log files every 21 days, use a command like this one:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00"

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-device-update-configuration-settings"></a><span data-ttu-id="a7c95-115">Para alterar vários valores de propriedade ao criar definições de configuração de atualização de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a7c95-115">To change multiple property values when creating device update configuration settings</span></span>

  - <span data-ttu-id="a7c95-116">Vários valores de propriedade podem ser modificados incluindo vários parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a7c95-116">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="a7c95-117">Por exemplo, esse comando define o intervalo de limpeza do log para 21 dias e o intervalo de liberação do log para 30 minutos:</span><span class="sxs-lookup"><span data-stu-id="a7c95-117">For example, this command sets the log cleanup interval to 21 days and the log flush interval to 30 minutes:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00" -LogFlushInterval "00:30:00"

</div>

<span data-ttu-id="a7c95-118">Para obter detalhes sobre como modificar as configurações de configuração de dispositivo existentes, consulte o tópico da ajuda para o cmdlet [set-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg398320(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="a7c95-118">For details about modifying existing device configuration settings, see the Help topic for the [Set-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg398320(v=OCS.15)) cmdlet.</span></span> <span data-ttu-id="a7c95-119">Para obter detalhes sobre como criar conjuntos de definições de configuração, consulte o tópico da ajuda para o cmdlet [New-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg425761(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="a7c95-119">For details about creating collections of configuration settings, see the Help topic for the [New-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg425761(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="a7c95-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a7c95-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

