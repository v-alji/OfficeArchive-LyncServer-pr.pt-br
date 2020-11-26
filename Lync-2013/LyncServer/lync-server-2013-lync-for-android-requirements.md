---
title: 'Lync Server 2013: requisitos do Lync para Android'
description: 'Lync Server 2013: requisitos do Lync para Android.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync for Android requirements
ms:assetid: 4ff53e03-0c1f-4a2b-9cec-1131c2a48563
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690980(v=OCS.15)
ms:contentKeyID: 53312965
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d3d3aa6e428c3a73f1b9263fe9cf13e5aa9fff0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426414"
---
# <a name="lync-for-android-requirements-in-lync-server-2013"></a><span data-ttu-id="1eb5d-103">Requisitos do Lync para Android no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1eb5d-103">Lync for Android requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1eb5d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1eb5d-104">

<span> </span></span></span>

<span data-ttu-id="1eb5d-105">_**Tópico da última modificação:** 2014-04-24_</span><span class="sxs-lookup"><span data-stu-id="1eb5d-105">_**Topic Last Modified:** 2014-04-24_</span></span>

<span data-ttu-id="1eb5d-106">Microsoft Lync 2013 o Microsoft Lync 2013 para Android fornece mensagens instantâneas (IM), presença aprimorada e recursos de junção de reunião do Lync para usuários em sua organização que estão se conectando de um dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-106">Microsoft Lync 2013 Microsoft Lync 2013 for Android provides instant messaging (IM), enhanced presence, and Lync meeting join capabilities for users in your organization who are connecting from an Android device.</span></span> <span data-ttu-id="1eb5d-107">Este tópico descreve as considerações sobre o Lync 2013 para Android, incluindo pré-requisitos, requisitos técnicos e componentes obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-107">This topic describes considerations for Lync 2013 for Android, including prerequisites, technical requirements, and required components.</span></span>

<div>

## <a name="lync-for-android-prerequisite"></a><span data-ttu-id="1eb5d-108">Pré-requisito do Lync para Android</span><span class="sxs-lookup"><span data-stu-id="1eb5d-108">Lync for Android Prerequisite</span></span>

<span data-ttu-id="1eb5d-109">Para dar suporte ao Lync 2013 para Android, o dispositivo Android deve atender aos seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="1eb5d-109">To support Lync 2013 for Android, the Android device must meet the following requirements:</span></span>

  - <span data-ttu-id="1eb5d-110">O dispositivo Android deve estar executando o Android 4,0 ou um sistema operacional mais recente orientado por telefone ou Tablet, incluindo tablets, exceto aqueles com o chip Tegra2.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-110">The Android device must be running Android 4.0 or a later phone- or tablet-oriented operating system, including tablets, except those with the Tegra2 chip.</span></span>

  - <span data-ttu-id="1eb5d-111">O dispositivo deve ter uma CPU dual core de 1,2 GHz ou superior.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-111">The device must have a 1.2 GHz dual core or higher CPU.</span></span>

  - <span data-ttu-id="1eb5d-112">A resolução da câmera (frontal/traseira) do dispositivo deve ser VGA ou superior.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-112">The device camera (front/rear) resolution should be VGA or higher.</span></span>

  - <span data-ttu-id="1eb5d-113">Outros requisitos de hardware devem ser alinhados ao documento de definição de compatibilidade do Android 4,0.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-113">Other hardware requirements should be aligned with Android 4.0 Compatibility Definition Document.</span></span>

</div>

<div>

## <a name="other-technical-considerations"></a><span data-ttu-id="1eb5d-114">Outras considerações técnicas</span><span class="sxs-lookup"><span data-stu-id="1eb5d-114">Other Technical Considerations</span></span>

<span data-ttu-id="1eb5d-115">Na plataforma de dispositivo Android, o aplicativo Lync pode ser executado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-115">On the Android device platform, the Lync application can run in the background.</span></span> <span data-ttu-id="1eb5d-116">Portanto, ao contrário de outras plataformas de dispositivos móveis, as notificações por push não são necessárias para dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-116">Therefore, unlike other mobile device platforms, push notifications are not required for Android devices.</span></span> <span data-ttu-id="1eb5d-117">A única maneira de sair do aplicativo do Lync em um dispositivo Android é explicitamente desconectar-se do Lync.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-117">The only way to exit the Lync application on an Android device is to explicitly sign out of Lync.</span></span> <span data-ttu-id="1eb5d-118">Não há suporte para esta versão do aplicativo do Lync em dispositivos com chipsets Tegra 2.</span><span class="sxs-lookup"><span data-stu-id="1eb5d-118">This version of the Lync application is not supported on devices with Tegra 2 chipsets.</span></span>

<span data-ttu-id="1eb5d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1eb5d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

