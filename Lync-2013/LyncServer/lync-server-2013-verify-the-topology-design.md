---
title: 'Lync Server 2013: Verificar o design de topologia'
description: 'Lync Server 2013: verificar o design da topologia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438908"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a><span data-ttu-id="91784-103">Verificar o design de topologia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91784-103">Verify the topology design in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91784-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91784-104">

<span> </span></span></span>

<span data-ttu-id="91784-105">_**Tópico da última modificação:** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="91784-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="91784-106">O construtor de topologias verifica automaticamente a topologia.</span><span class="sxs-lookup"><span data-stu-id="91784-106">Topology Builder automatically verifies the topology.</span></span> <span data-ttu-id="91784-107">Qualquer erro de topologia é identificado como um erro de validação, indicado pelo ícone de erro de validação ao lado da função do servidor.</span><span class="sxs-lookup"><span data-stu-id="91784-107">Any topology error is identified as a validation error, indicated by the validation error icon next to the server role.</span></span> <span data-ttu-id="91784-108">Também é importante verificar se a topologia representa corretamente a topologia para a implantação.</span><span class="sxs-lookup"><span data-stu-id="91784-108">It is important to also verify that the topology correctly represents the topology for your deployment.</span></span>

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a><span data-ttu-id="91784-109">Para verificar a topologia antes da publicação</span><span class="sxs-lookup"><span data-stu-id="91784-109">To verify the topology prior to publication</span></span>

1.  <span data-ttu-id="91784-110">Verifique se todas as URLs simples estão configuradas corretamente.</span><span class="sxs-lookup"><span data-stu-id="91784-110">Check that all simple URLs are configured correctly.</span></span>

2.  <span data-ttu-id="91784-111">Verifique se o servidor baseado em SQL Server está online e disponível para o computador no qual o Construtor de Topologias está instalado, incluindo quaisquer regras de firewall necessárias.</span><span class="sxs-lookup"><span data-stu-id="91784-111">Confirm that the SQL Server-based server is online and available to the computer where Topology Builder is installed, including any necessary firewall rules.</span></span>

3.  <span data-ttu-id="91784-112">Confirme se o compartilhamento de arquivos está disponível e se tem as permissões adequadas definidas.</span><span class="sxs-lookup"><span data-stu-id="91784-112">Confirm that the file share is available and has the proper permissions defined.</span></span>

4.  <span data-ttu-id="91784-113">Verifique se as funções de servidor corretas que atendem aos requisitos de implantação estão definidas na topologia.</span><span class="sxs-lookup"><span data-stu-id="91784-113">Confirm that the correct server roles that meet the deployment requirements are defined in the topology.</span></span>

5.  <span data-ttu-id="91784-114">Verifique se os servidores existem nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="91784-114">Verify that the servers exist in Active Directory Domain Services.</span></span> <span data-ttu-id="91784-115">Isso ocorrerá automaticamente se você tiver ingressado nos servidores do domínio.</span><span class="sxs-lookup"><span data-stu-id="91784-115">This will happen automatically if you have joined the servers to the domain.</span></span>

<span data-ttu-id="91784-116">Após a verificação da topologia, se não houver erros de validação, você estará pronto para publicar a topologia.</span><span class="sxs-lookup"><span data-stu-id="91784-116">When you have verified the topology and there are no validation errors, you should be ready to publish the topology.</span></span> <span data-ttu-id="91784-117">Se houver erros de validação, você deve corrigi-los para poder publicar a topologia.</span><span class="sxs-lookup"><span data-stu-id="91784-117">If there are validation errors, you must correct these before you can publish the topology.</span></span> <span data-ttu-id="91784-118">Para obter detalhes sobre como publicar sua topologia, consulte [publicar a topologia no Lync Server 2013](lync-server-2013-publish-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="91784-118">For details about publishing your topology, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md).</span></span>

<span data-ttu-id="91784-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91784-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

