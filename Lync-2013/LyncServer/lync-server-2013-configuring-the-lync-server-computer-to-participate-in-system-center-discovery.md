---
title: Configurando o computador do Lync Server para participar da descoberta do System Center
description: Configuração do computador do Lync Server para participar da descoberta do System Center.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computer to participate in System Center discovery
ms:assetid: 2f9c9cb0-3120-4571-9cd2-657c2123fe21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204776(v=OCS.15)
ms:contentKeyID: 48183731
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d25ba3de673084b2e64e17790a2776cbe57f07
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432559"
---
# <a name="configuring-the-lync-server-2013-computer-to-participate-in-system-center-discovery"></a><span data-ttu-id="ea494-103">Configurando o computador do Lync Server 2013 para participar da descoberta do System Center</span><span class="sxs-lookup"><span data-stu-id="ea494-103">Configuring the Lync Server 2013 computer to participate in System Center discovery</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea494-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea494-104">

<span> </span></span></span>

<span data-ttu-id="ea494-105">_**Tópico da última modificação:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="ea494-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="ea494-106">Para garantir que seu novo agente do Lync Server participe do processo de descoberta do System Center Operations Manager, você deve concluir o procedimento a seguir em cada computador em que o console do System Center Operations Manager foi instalado:</span><span class="sxs-lookup"><span data-stu-id="ea494-106">To make sure that your new Lync Server agent participates in discovery process for System Center Operations Manager, you must complete the following procedure on each computer where the System Center Operations Manager console has been installed:</span></span>

1.  <span data-ttu-id="ea494-107">Na guia **Administração** , clique em **agente gerenciado**.</span><span class="sxs-lookup"><span data-stu-id="ea494-107">On the **Administration** tab, click **Agent Managed**.</span></span>

2.  <span data-ttu-id="ea494-108">Clique com o botão direito no nome do computador e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="ea494-108">Right-click the name of the computer, and then click **Properties**.</span></span> <span data-ttu-id="ea494-109">Na caixa de diálogo **Propriedades** , na guia **segurança** , selecione **permitir que esse agente atue como um proxy e descubra objetos gerenciados em outros computadores** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea494-109">In the **Properties** dialog box, on the **Security** tab, select **Allow this agent to act as a proxy and discover managed objects on other computers**, and then click **OK**.</span></span>

<span data-ttu-id="ea494-110">Depois de concluir a etapa 2, reinicie o serviço de agente de integridade.</span><span class="sxs-lookup"><span data-stu-id="ea494-110">After completing step 2, reboot the Health Agent service.</span></span> <span data-ttu-id="ea494-111">(A reinicialização do serviço irá "forçar" a descoberta da nova máquina.</span><span class="sxs-lookup"><span data-stu-id="ea494-111">(Rebooting the service will “force” discovery of the new machine.</span></span> <span data-ttu-id="ea494-112">Se você não reinicializar o serviço, pode levar até 4 horas para que o novo computador seja descoberto pelo System Center Operations Manager.).</span><span class="sxs-lookup"><span data-stu-id="ea494-112">If you do not reboot the service, it could take as long as 4 hours before the new machine is discovered by System Center Operations Manager.).</span></span> <span data-ttu-id="ea494-113">Após a reinicialização do serviço, verifique se nenhum evento de erro está sendo gravado no log de eventos do Operations Manager nesse computador.</span><span class="sxs-lookup"><span data-stu-id="ea494-113">After the service has rebooted, verify that no error events are being recorded in the Operations Manager event log on that computer.</span></span>

<span data-ttu-id="ea494-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea494-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

