---
title: Verificar as definições da configuração
description: Verifique as configurações de configuração.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify configuration settings
ms:assetid: 51c2d1d9-63f7-43ab-88ca-b8913da7cede
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204885(v=OCS.15)
ms:contentKeyID: 48184111
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7bb1135e95dafe51e906768fe0f4f0d57bf2d6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423341"
---
# <a name="verify-configuration-settings"></a><span data-ttu-id="93582-103">Verificar as definições da configuração</span><span class="sxs-lookup"><span data-stu-id="93582-103">Verify configuration settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93582-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93582-104">

<span> </span></span></span>

<span data-ttu-id="93582-105">_**Tópico da última modificação:** 2012-09-06_</span><span class="sxs-lookup"><span data-stu-id="93582-105">_**Topic Last Modified:** 2012-09-06_</span></span>

<span data-ttu-id="93582-106">Você pode validar a replicação de informações de configuração para o servidor de borda executando o cmdlet **Get-CsManagementStoreReplicationStatus** do Lync Server 2013 no computador interno no qual o repositório de gerenciamento central está localizado ou em qualquer computador associado a um domínio no qual o Lync Server 2013 Core Components (OcsCore.msi) esteja instalado.</span><span class="sxs-lookup"><span data-stu-id="93582-106">You can validate the replication of configuration information to the Edge server by running the Lync Server 2013 **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located, or on any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span>

<span data-ttu-id="93582-107">Os resultados iniciais podem indicar o status como "falso" em vez de "verdadeiro" para replicação.</span><span class="sxs-lookup"><span data-stu-id="93582-107">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="93582-108">Em caso afirmativo, execute o cmdlet **Invoke-CsManagementStoreReplication** e aguarde o tempo de conclusão da replicação antes de executar o **Get-CsManagementStoreReplicationStatus** novamente.</span><span class="sxs-lookup"><span data-stu-id="93582-108">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="93582-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93582-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

