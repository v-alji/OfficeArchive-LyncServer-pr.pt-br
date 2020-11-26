---
title: 'Lync Server 2013: Testar roteamento de voz'
description: 'Lync Server 2013: testar roteamento de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice routing
ms:assetid: d3aae909-fef6-440f-b144-0b62dc82bf5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398915(v=OCS.15)
ms:contentKeyID: 48185444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e641e68ccecfe7d1d0e64dc9eb1b1f5016e68e22
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441148"
---
# <a name="test-voice-routing-in-lync-server-2013"></a><span data-ttu-id="b26be-103">Testar roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b26be-103">Test voice routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b26be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b26be-104">

<span> </span></span></span>

<span data-ttu-id="b26be-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="b26be-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="b26be-106">Você pode usar a guia de roteamento de **voz** do painel de controle do Lync Server para configurar cenários de casos de teste.</span><span class="sxs-lookup"><span data-stu-id="b26be-106">You can use the Lync Server Control Panel **Test Voice Routing** tab to configure test case scenarios.</span></span> <span data-ttu-id="b26be-107">Para definir um caso de teste, especifique o plano de discagem, a política de voz, o uso da PSTN e a rota de voz em que deseja testar um número de telefone especificado.</span><span class="sxs-lookup"><span data-stu-id="b26be-107">To define a test case, you specify the dial plan, voice policy, PSTN usage, and voice route against which to test a specified phone number.</span></span>

<span data-ttu-id="b26be-108">Antes de realmente implantar sua configuração de roteamento de voz, recomendamos testá-la em vários números de telefone para ter certeza de que os resultados são o que você está esperando.</span><span class="sxs-lookup"><span data-stu-id="b26be-108">Before you actually deploy your voice routing configuration, we recommend that you test it on various phone numbers to make sure that the results are what you're expecting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="b26be-109">Você pode usar os comandos <STRONG>Exportar casos de teste</STRONG> e <STRONG>importar casos de teste</STRONG> para salvar os casos de teste de roteamento de voz e importá-los para uso em outro computador.</span><span class="sxs-lookup"><span data-stu-id="b26be-109">You can use the <STRONG>Export test cases</STRONG> and <STRONG>Import test cases</STRONG> commands to save voice routing test cases and import them for use on another computer.</span></span>



</div>

<div>


> [!WARNING]  
> <span data-ttu-id="b26be-110">Se você excluir qualquer parte de sua configuração de roteamento de voz, como um plano de discagem, política de voz, rota de voz ou uso do telefone, você deve revisar e atualizar seus casos de teste de roteamento de voz.</span><span class="sxs-lookup"><span data-stu-id="b26be-110">If you delete any part of your voice routing configuration, such as a dial plan, voice policy, voice route, or phone usage, you should review and update your voice routing test cases.</span></span> <span data-ttu-id="b26be-111">O painel de controle do Lync Server não irá alertá-lo para testar casos que não sejam mais válidos devido às configurações alteradas.</span><span class="sxs-lookup"><span data-stu-id="b26be-111">The Lync Server Control Panel will not alert you to test cases that are no longer valid due to changed configurations.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b26be-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b26be-112">In This Section</span></span>

  - [<span data-ttu-id="b26be-113">Criar um caso de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b26be-113">Create a voice routing test case in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-routing-test-case.md)

  - [<span data-ttu-id="b26be-114">Exportar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b26be-114">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)

  - [<span data-ttu-id="b26be-115">Importar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b26be-115">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)

  - [<span data-ttu-id="b26be-116">Executando testes de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b26be-116">Running voice routing tests in Lync Server 2013</span></span>](lync-server-2013-running-voice-routing-tests.md)

<span data-ttu-id="b26be-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b26be-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

