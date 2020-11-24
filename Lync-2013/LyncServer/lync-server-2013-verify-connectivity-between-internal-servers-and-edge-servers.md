---
title: Verificar conectividade entre servidores internos e Servidores de Borda
description: Verifique a conectividade entre servidores internos e servidores de borda.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity between internal servers and Edge Servers
ms:assetid: 219f706e-2b8a-46c5-b394-c384240eef50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398292(v=OCS.15)
ms:contentKeyID: 48183602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f86f87428d7eaf91b8f70422cfee712584252fad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390322"
---
# <a name="verify-connectivity-between-internal-servers-and-edge-servers-in-lync-server-2013"></a><span data-ttu-id="f3ba3-103">Verificar conectividade entre servidores internos e Servidores de Borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3ba3-103">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3ba3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3ba3-104">

<span> </span></span></span>

<span data-ttu-id="f3ba3-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="f3ba3-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="f3ba3-106">No Lync Server 2013, um assistente de validação separado estava disponível para ajudar a validar a conectividade entre servidores de borda e servidores internos.</span><span class="sxs-lookup"><span data-stu-id="f3ba3-106">In Lync Server 2013, a separate validation wizard was available to help validate connectivity between Edge Servers and internal servers.</span></span> <span data-ttu-id="f3ba3-107">Na validação do Lync Server 2013 de conectividade, é feito automaticamente quando você instala seus servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="f3ba3-107">In Lync Server 2013 validation of connectivity is done automatically when you install your Edge Servers.</span></span>

<span data-ttu-id="f3ba3-108">Você pode validar a replicação de informações de configuração para a borda executando o cmdlet **Get-CsManagementStoreReplicationStatus** do Windows PowerShell no computador interno no qual o repositório de gerenciamento central está localizado (ou qualquer computador associado a domínio no qual o Lync Server 2013 Core Components (OcsCore.msi) está instalado.</span><span class="sxs-lookup"><span data-stu-id="f3ba3-108">You can validate the replication of configuration information to the edge by running the Windows PowerShell **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located (or any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span> <span data-ttu-id="f3ba3-109">Os resultados iniciais podem indicar o status como "falso" em vez de "verdadeiro" para replicação.</span><span class="sxs-lookup"><span data-stu-id="f3ba3-109">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="f3ba3-110">Em caso afirmativo, execute o cmdlet **Invoke-CsManagementStoreReplication** e aguarde o tempo de conclusão da replicação antes de executar o **Get-CsManagementStoreReplicationStatus** novamente.</span><span class="sxs-lookup"><span data-stu-id="f3ba3-110">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="f3ba3-111">Você pode verificar a conectividade do usuário externo separadamente, incluindo o uso do analisador de conectividade remota do Office Communications Server para verificar a conectividade do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="f3ba3-111">You can verify external user connectivity separately, including using the Office Communications Server Remote Connectivity Analyzer to verify remote user connectivity.</span></span> <span data-ttu-id="f3ba3-112">Para obter detalhes, consulte [verificar a conectividade para usuários externos no Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span><span class="sxs-lookup"><span data-stu-id="f3ba3-112">For details, see [Verify connectivity for external users in Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span></span>

<span data-ttu-id="f3ba3-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3ba3-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

