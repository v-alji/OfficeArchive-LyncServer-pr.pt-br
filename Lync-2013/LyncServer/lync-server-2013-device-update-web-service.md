---
title: 'Lync Server 2013: Serviço Web de Atualização de Dispositivo'
description: 'Lync Server 2013: serviço Web de atualização de dispositivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update Web service
ms:assetid: 036f473d-a131-431f-8051-76ccadc5cfba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994015(v=OCS.15)
ms:contentKeyID: 51803921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45511d34ab99f295481472f2a3c14bf21da32ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429364"
---
# <a name="device-update-web-service-in-lync-server-2013"></a><span data-ttu-id="d8bf3-103">Serviço Web de Atualização de Dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8bf3-103">Device Update Web service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8bf3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8bf3-104">

<span> </span></span></span>

<span data-ttu-id="d8bf3-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="d8bf3-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="d8bf3-106">O Lync Server inclui o serviço Web de atualização de dispositivo, que é instalado automaticamente como parte da função de serviços Web.</span><span class="sxs-lookup"><span data-stu-id="d8bf3-106">Lync Server includes the Device Update Web service, which is automatically installed as part of the Web Services role.</span></span> <span data-ttu-id="d8bf3-107">Esse serviço permite baixar atualizações da Microsoft, testá-las e, em seguida, implantar as atualizações em telefones IP em sua organização.</span><span class="sxs-lookup"><span data-stu-id="d8bf3-107">This service lets you download updates from Microsoft, test them, and then deploy the updates to IP phones in your organization.</span></span> <span data-ttu-id="d8bf3-108">Você também pode usar o serviço Web de atualização de dispositivo para reverter dispositivos para versões anteriores do software.</span><span class="sxs-lookup"><span data-stu-id="d8bf3-108">You can also use Device Update Web service to roll back devices to previous software versions.</span></span>

<span data-ttu-id="d8bf3-109">Esta seção fornece detalhes sobre como gerenciar o serviço Web de atualização de dispositivo e atualizações implantadas usando logs de atualização de dispositivo, regras (o Lync Phone Edition usa *regras* para associar atualizações de versão de firmware a dispositivos de hardware) e configurações.</span><span class="sxs-lookup"><span data-stu-id="d8bf3-109">This section provides details about how to manage the Device Update Web service and deployed updates by using device update logs, rules (Lync Phone Edition uses *rules* to associate firmware version updates with hardware devices), and configuration settings.</span></span>

<span data-ttu-id="d8bf3-110">Para obter detalhes sobre o processo e os recursos do serviço Web de atualização de dispositivo, consulte [atualizando dispositivos](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) na biblioteca do TechNet do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d8bf3-110">For details about the Device Update Web service process and features, see [Updating Devices](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="d8bf3-111">(Observe que o serviço Web de atualização de dispositivo, como todos os componentes do Lync Phone Edition, funciona da mesma maneira com o Lync Server 2013 como no Lync Server 2010.)</span><span class="sxs-lookup"><span data-stu-id="d8bf3-111">(Note that the Device Update Web service, like all Lync Phone Edition components, works the same way with Lync Server 2013 as it does with Lync Server 2010.)</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d8bf3-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d8bf3-112">In This Section</span></span>

  - [<span data-ttu-id="d8bf3-113">Logs e arquivos de atualização de dispositivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8bf3-113">Device Update logs and files in Lync Server 2013</span></span>](lync-server-2013-device-update-logs-and-files.md)

  - [<span data-ttu-id="d8bf3-114">Regras de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8bf3-114">Device Update rules in Lync Server 2013</span></span>](lync-server-2013-device-update-rules.md)

  - [<span data-ttu-id="d8bf3-115">Opções de configuração de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8bf3-115">Device Update configuration settings in Lync Server 2013</span></span>](lync-server-2013-device-update-configuration-settings.md)

  - [<span data-ttu-id="d8bf3-116">Exibir atualizações de software para dispositivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8bf3-116">View software updates for devices in Lync Server 2013</span></span>](lync-server-2013-view-software-updates-for-devices-in-your-organization.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d8bf3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8bf3-117">See Also</span></span>


<span data-ttu-id="d8bf3-118">[Ferramentas e serviços para gerenciar e solucionar problemas de dispositivos](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span><span class="sxs-lookup"><span data-stu-id="d8bf3-118">[Tools and Services for Managing and Troubleshooting Devices](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span></span>  
  

<span data-ttu-id="d8bf3-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8bf3-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

