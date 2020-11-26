---
title: 'Lync Server 2013: Validando o roteamento e a normalização do número de voz'
description: 'Lync Server 2013: Validando o roteamento e a normalização do número de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating voice number normalization and routing
ms:assetid: a6a825c7-6928-4e80-b7e9-803b7f7ebd13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720922(v=OCS.15)
ms:contentKeyID: 63969633
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f28f679cbb991bdb90362eb61c9c7b68879791e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438621"
---
# <a name="validating-voice-number-normalization-and-routing-in-lync-server-2013"></a><span data-ttu-id="e230d-103">Validando a normalização de número de voz e encaminhamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e230d-103">Validating voice number normalization and routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e230d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e230d-104">

<span> </span></span></span>

<span data-ttu-id="e230d-105">_**Tópico da última modificação:** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="e230d-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="e230d-106">A normalização e o roteamento do número corretos são muito importantes para o ambiente corporativo de voz funcional.</span><span class="sxs-lookup"><span data-stu-id="e230d-106">Correct number normalization and routing is very important for functional Enterprise Voice environment.</span></span> <span data-ttu-id="e230d-107">Especialmente durante as migrações do PBX (Private Branch Exchange) para o ambiente autônomo do Lync Server, uma das chaves para a migração bem-sucedida é revelar e documentar todas as regras de discagem existentes e criar regras de normalização adequadas, políticas de voz, usos e rotas de telefone.</span><span class="sxs-lookup"><span data-stu-id="e230d-107">Especially during migrations from private branch exchange (PBX) to stand-alone Lync Server environment, one of the keys to successful migration is to reveal and document all existing dialing rules, and create appropriate normalization rules, voice policies, phone usages and routes.</span></span>

<span data-ttu-id="e230d-108">A validação da normalização do número e do roteamento é importante não apenas durante as migrações, mas também durante a operação normal e estável do sistema.</span><span class="sxs-lookup"><span data-stu-id="e230d-108">Validating number normalization and routing is important not only during migrations but also during normal, stable operation of the system.</span></span>

<span data-ttu-id="e230d-109">Recomendamos realizar essa validação diariamente usando o painel de controle do Lync Server, começando com o desenvolvimento de um conjunto robusto de casos de teste em relação ao conjunto atual de regras de normalização que foram publicadas nas configurações globais do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e230d-109">We recommend conducting this validation daily by using the Lync Server Control Panel, starting with developing a robust set of test cases against the current set of normalization rules that were published in the Lync Server global settings.</span></span> <span data-ttu-id="e230d-110">Estes casos de teste devem ser executados diariamente para realçar as alterações indesejadas que foram feitas e confirmadas no plano de discagem.</span><span class="sxs-lookup"><span data-stu-id="e230d-110">These test cases should be run daily to highlight any unwanted changes that were made and committed to the dial plan.</span></span>

<span data-ttu-id="e230d-111">O painel de controle do Lync Server também ajuda você a Visualizar, testar, alterar, arquivar e compartilhar informações de configuração sobre o roteamento de voz e alterar as regras de normalização do número da empresa, planos de discagem, política de voz e rotas.</span><span class="sxs-lookup"><span data-stu-id="e230d-111">Lync Server Control Panel also helps you visualize, test, change, archive, and share configuration information about voice routing and in changing Enterprise Voice number normalization rules, dial plans, voice policy, and routes.</span></span> <span data-ttu-id="e230d-112">Ele tem recursos adicionais para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e230d-112">It has additional features for doing the following:</span></span>

  - <span data-ttu-id="e230d-113">Exportar e importar ou fazer backup de dados de roteamento de voz entre sistemas.</span><span class="sxs-lookup"><span data-stu-id="e230d-113">Exporting and importing or backing up voice routing data between systems.</span></span>

  - <span data-ttu-id="e230d-114">Testar alterações de configuração antes de carregá-las em um sistema dinâmico.</span><span class="sxs-lookup"><span data-stu-id="e230d-114">Testing configuration changes before uploading them to a live system.</span></span>

  - <span data-ttu-id="e230d-115">Criar e executar casos de teste de configuração para ajudar a garantir a usabilidade de dados de roteamento depois de fazer alterações nele, mas antes de confirmá-los as alterações em um sistema implantado.</span><span class="sxs-lookup"><span data-stu-id="e230d-115">Creating and running configuration test cases to help ensure the usability of routing data after you make changes to it, but before committing them the changes to a deployed system.</span></span>

  - <span data-ttu-id="e230d-116">Criar e alterar regras de normalização de número, perfis de localização, política de voz e dados de roteamento sem escrever as expressões regulares necessárias.</span><span class="sxs-lookup"><span data-stu-id="e230d-116">Creating and changing number normalization rules, location profiles, voice policy, and routing data without writing the necessary regular expressions.</span></span>

  - <span data-ttu-id="e230d-117">Analisando um perfil de local para compatibilidade com o Lync Server Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="e230d-117">Analyzing a location profile for compatibility with the Lync Server Phone Edition.</span></span>

  - <span data-ttu-id="e230d-118">Mais informações sobre testes de roteamento de voz podem ser encontradas em [testar roteamento de voz no Lync Server 2013](lync-server-2013-test-voice-routing.md)</span><span class="sxs-lookup"><span data-stu-id="e230d-118">More information about voice routing tests can be found at [Test voice routing in Lync Server 2013](lync-server-2013-test-voice-routing.md)</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="e230d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e230d-119">See Also</span></span>


[<span data-ttu-id="e230d-120">Testar roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e230d-120">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="e230d-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e230d-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

