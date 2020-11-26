---
title: Configurando a qualidade do serviço em dispositivos Microsoft Lync Phone Edition
description: Configurando a qualidade do serviço em dispositivos Microsoft Lync Phone Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service on Microsoft Lync Phone Edition devices
ms:assetid: a6eb2620-a512-4ab6-bdfd-eb76be43bbfe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205137(v=OCS.15)
ms:contentKeyID: 48185004
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0d1e4f10c6b4a550f5da25f8bd2e9fe97606255
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432699"
---
# <a name="configuring-quality-of-service-on-microsoft-lync-phone-edition-devices-in-lync-server-2013"></a><span data-ttu-id="dbadb-103">Configurando a qualidade do serviço em dispositivos Microsoft Lync Phone Edition no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbadb-103">Configuring Quality of Service on Microsoft Lync Phone Edition devices in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dbadb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dbadb-104">

<span> </span></span></span>

<span data-ttu-id="dbadb-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="dbadb-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="dbadb-106">Embora a QoS (qualidade de serviço) não seja habilitada por padrão para dispositivos como iPhones, a QoS é habilitada por padrão para dispositivos que executam o Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="dbadb-106">Although Quality of Service (QoS) is not enabled by default for devices such as iPhones, QoS is enabled by default for devices running Lync Phone Edition.</span></span> <span data-ttu-id="dbadb-107">(Esses dispositivos são comumente referidos como telefones de comunicação unificada ou UC.) Para verificar isso, execute o seguinte comando do Windows PowerShell no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="dbadb-107">(These devices are commonly referred to as UC or Unified Communication phones.) To verify this, run the following Windows PowerShell command from within the Lync Server Management Shell:</span></span>

    Get-CsUCPhoneConfiguration

<span data-ttu-id="dbadb-108">Se você não fez nenhuma alteração nas configurações de seu telefone UC, receberá as informações que se assemelharão a isto:</span><span class="sxs-lookup"><span data-stu-id="dbadb-108">If you have not made any changes to your UC phone configuration settings then you will get back information that looks like this:</span></span>

    Identity             : Global
    CalendarPollInterval : 00:03:00
    EnforcePhoneLock     : True
    PhoneLockTimeout     : 00:10:00
    MinPhonePinLength    : 6
    SIPSecurityMode      : High
    VoiceDiffServTag     : 40
    Voice8021p           : 0
    LoggingLevel         : Off

<span data-ttu-id="dbadb-109">Para fins de qualidade de serviço, apenas uma dessas propriedades é de interesse: VoiceDiffServTag.</span><span class="sxs-lookup"><span data-stu-id="dbadb-109">For Quality of Service purposes, only one of these properties is of interest: VoiceDiffServTag.</span></span> <span data-ttu-id="dbadb-110">O VoiceDiffServTag representa o valor de DSCP atribuído ao tráfego de voz que emana de um dispositivo Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="dbadb-110">The VoiceDiffServTag represents the DSCP value assigned to voice traffic emanating from a Lync Phone Edition device.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="dbadb-111">O parâmetro Voice8021p não é mais compatível com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dbadb-111">The Voice8021p parameter is no longer supported in Lync Server 2013.</span></span> <span data-ttu-id="dbadb-112">O parâmetro ainda é válido para fins de compatibilidade com versões anteriores do Microsoft Lync Server 2010; no entanto, ele não tem efeito em dispositivos usados com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dbadb-112">The parameter is still valid for backward compatibility with Microsoft Lync Server 2010; however, it has no effect on devices used with Lync Server 2013.</span></span>



</div>

<span data-ttu-id="dbadb-113">Na maioria das redes, a marcação de pacotes do Lync Phone Edition com um VoiceDiffServTag de 40 não deve causar problemas.</span><span class="sxs-lookup"><span data-stu-id="dbadb-113">In most networks, marking Lync Phone Edition packets with a VoiceDiffServTag of 40 should not cause any problems.</span></span> <span data-ttu-id="dbadb-114">No entanto, 40 não é o valor normalmente usado para tráfego de áudio; em vez disso, o tráfego de áudio é quase sempre marcado com o código DSCP 46.</span><span class="sxs-lookup"><span data-stu-id="dbadb-114">However, 40 is not the value typically used for audio traffic; instead, audio traffic is almost always marked with the DSCP code 46.</span></span> <span data-ttu-id="dbadb-115">Para manter a consistência em toda a sua rede, talvez você queira alterar a propriedade VoiceDiffServTag de seus telefones UC para o 46.</span><span class="sxs-lookup"><span data-stu-id="dbadb-115">In order to maintain consistency throughout your network, you might want to change the VoiceDiffServTag property of your UC phones to 46.</span></span>

<span data-ttu-id="dbadb-116">Para fazer isso, você pode usar o Windows PowerShell ou o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dbadb-116">To do that, you can use either Windows PowerShell or the Lync Server Control Panel.</span></span> <span data-ttu-id="dbadb-117">Para modificar o valor VoiceDiffServTag usando o Windows PowerShell, execute o seguinte comando no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="dbadb-117">To modify the VoiceDiffServTag value by using Windows PowerShell, run the following command from within the Lync Server Management Shell:</span></span>

    Set-CsUCPhoneConfiguration -VoiceDiffServTag 46

<span data-ttu-id="dbadb-118">O comando anterior modifica o conjunto global de configurações de configuração de telefone de comunicação unificada.</span><span class="sxs-lookup"><span data-stu-id="dbadb-118">The preceding command modifies the global collection of UC phone configuration settings.</span></span> <span data-ttu-id="dbadb-119">No entanto, observe que as configurações de telefone UC também podem ser atribuídas ao escopo do site.</span><span class="sxs-lookup"><span data-stu-id="dbadb-119">Note, however, that UC phone settings can also be assigned to the site scope.</span></span> <span data-ttu-id="dbadb-120">Para modificar as configurações de telefone UC no escopo do site, você deve especificar a identidade do site.</span><span class="sxs-lookup"><span data-stu-id="dbadb-120">To modify UC phone configuration settings at the site scope, you must specify the site Identity.</span></span> <span data-ttu-id="dbadb-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dbadb-121">For example:</span></span>

    Set-CsUCPhoneConfiguration -Identity "site:Redmond" -VoiceDiffServTag 46

<span data-ttu-id="dbadb-122">Você também pode usar o comando a seguir para modificar simultaneamente todas as suas configurações de telefone UC:</span><span class="sxs-lookup"><span data-stu-id="dbadb-122">You can also use the following command to simultaneously modify all your UC phone configuration settings:</span></span>

    Get-CsUCPhoneConfiguration | Set-CsUCPhoneConfiguration -VoiceDiffServTag 46

<span data-ttu-id="dbadb-123">Se você preferir fazer essa alteração usando o painel de controle do Lync Server, inicie o painel de controle e, em seguida, conclua o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="dbadb-123">If you prefer to make this change using Lync Server Control Panel, then start the Control Panel and then complete the following procedure:</span></span>

1.  <span data-ttu-id="dbadb-124">Clique em **clientes** e em **configuração de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="dbadb-124">Click **Clients** and then click **Device Configuration**.</span></span>

2.  <span data-ttu-id="dbadb-125">Na guia **configuração de dispositivo** , clique duas vezes na coleção de configurações que você deseja modificar (por exemplo, **global**).</span><span class="sxs-lookup"><span data-stu-id="dbadb-125">On the **Device Configuration** tab, double-click the collection of settings you want to modify (for example, **Global**).</span></span>

3.  <span data-ttu-id="dbadb-126">Na caixa de diálogo **Editar configuração de dispositivo** , defina o valor da **caixa QoS (qualidade de serviço) de voz** como **46** e clique em **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="dbadb-126">In the **Edit Device Configuration** dialog box, set the value of the **Voice Quality of Service (QoS)** box to **46** and then click **Commit**.</span></span>

<span data-ttu-id="dbadb-127">Se você tiver várias coleções, será necessário repetir esse processo para cada conjunto de configurações de telefone UC.</span><span class="sxs-lookup"><span data-stu-id="dbadb-127">If you have multiple collections you will need to repeat this process for each collection of UC phone settings.</span></span> <span data-ttu-id="dbadb-128">O painel de controle do Lync Server não permitirá que você modifique simultaneamente várias coleções de configurações.</span><span class="sxs-lookup"><span data-stu-id="dbadb-128">Lync Server Control Panel will not allow you to simultaneously modify multiple setting collections.</span></span>

<span data-ttu-id="dbadb-129">Se você tiver dispositivos que não são baseados no sistema operacional Windows (por exemplo, iPhones) em sua organização, esses dispositivos não serão afetados alterando a configuração VoiceDiffServTag.</span><span class="sxs-lookup"><span data-stu-id="dbadb-129">If you have devices that are not based on the Windows operating system (such as iPhones) in your organization these devices will not be affected by changing the VoiceDiffServTag setting.</span></span> <span data-ttu-id="dbadb-130">Se você quiser alterar os valores de DSCP nesses dispositivos, será necessário consultar o manual de administração para cada um dos seus tipos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbadb-130">If you want to change DSCP values on those devices you will need to refer to the administration manual for each of your device types.</span></span>

<span data-ttu-id="dbadb-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dbadb-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

