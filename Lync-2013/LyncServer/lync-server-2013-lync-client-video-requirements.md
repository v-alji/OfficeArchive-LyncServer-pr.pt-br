---
title: 'Lync Server 2013: requisitos de vídeo do cliente do Lync'
description: 'Lync Server 2013: requisitos de vídeo do cliente do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync client video requirements
ms:assetid: 8f68f4c2-3194-487c-bd2f-fbe71ba8ad70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688132(v=OCS.15)
ms:contentKeyID: 49733731
ms.date: 01/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea1d4a993650ec8102d8b66ea5aa936ad1613f20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426435"
---
# <a name="lync-client-video-requirements-for-lync-server-2013"></a><span data-ttu-id="a0cfa-103">Requisitos de vídeo do cliente do Lync para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0cfa-103">Lync client video requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0cfa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0cfa-104">

<span> </span></span></span>

<span data-ttu-id="a0cfa-105">_**Tópico da última modificação:** 2016-01-29_</span><span class="sxs-lookup"><span data-stu-id="a0cfa-105">_**Topic Last Modified:** 2016-01-29_</span></span>

<span data-ttu-id="a0cfa-106">Esta seção descreve o suporte de hardware de vídeo para chamadas com vídeo do Lync 2013 e descreve como determinar a qualidade de vídeo esperada para várias configurações de computador, Tablet e dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-106">This section describes video hardware support for Lync 2013 video calls and describes how to determine the expected video quality for various computer, tablet, and mobile device configurations.</span></span>

<div>

## <a name="windows-desktop-and-tablet-video-requirements-and-capabilities"></a><span data-ttu-id="a0cfa-107">Recursos e requisitos de vídeo do Windows para área de trabalho e Tablet</span><span class="sxs-lookup"><span data-stu-id="a0cfa-107">Windows Desktop and Tablet Video Requirements and Capabilities</span></span>

<span data-ttu-id="a0cfa-108">O Lync 2013 introduz a aceleração de hardware para codificação e decodificação de vídeo com base no padrão de codificação de vídeo avançado H. 264/MPEG-4 Part 10.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-108">Lync 2013 introduces hardware acceleration for video encoding and decoding based on the H.264/MPEG-4 Part 10 Advanced Video Coding standard.</span></span> <span data-ttu-id="a0cfa-109">Esse recurso permite que computadores com velocidades baixas de clock da CPU codifiquem e decodifiquem vídeo de maior resolução.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-109">This feature allows computers with lower CPU clock speeds to encode and decode higher resolution video.</span></span> <span data-ttu-id="a0cfa-110">Os requisitos de hardware de vídeo variam de acordo com a configuração do computador e a resolução de vídeo desejada.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-110">Video hardware requirements vary depending on the computer configuration and the video resolution wanted.</span></span>

<div>

## <a name="video-hardware-requirements"></a><span data-ttu-id="a0cfa-111">Requisitos de hardware de vídeo</span><span class="sxs-lookup"><span data-stu-id="a0cfa-111">Video Hardware Requirements</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0cfa-112">Recurso</span><span class="sxs-lookup"><span data-stu-id="a0cfa-112">Feature</span></span></th>
<th><span data-ttu-id="a0cfa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0cfa-113">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-114">Decodificação H.264 acelerada por hardware usando DirectX Video Acceleration (DXVA)</span><span class="sxs-lookup"><span data-stu-id="a0cfa-114">Hardware accelerated H.264 decoding using DirectX Video Acceleration (DXVA)</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a0cfa-115">A placa gráfica deve suportar DirectX 9.0 e expor o modo de decodificação DXVA2_ModeH264_VLD_NoFGT.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-115">Graphics card must support DirectX 9.0 and must expose the DXVA2_ModeH264_VLD_NoFGT decoding mode.</span></span></p></li>
<li><p><span data-ttu-id="a0cfa-116">O driver mais recente da placa gráfica deve estar instalado.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-116">The latest graphics card driver must be installed.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="a0cfa-117">Para obter detalhes sobre os modos de decodificação, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A> .</span><span class="sxs-lookup"><span data-stu-id="a0cfa-117">For details about decoding modes, see <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A>.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-118">Codificação H.264 acelerada por hardware: requisitos de chipset</span><span class="sxs-lookup"><span data-stu-id="a0cfa-118">Hardware accelerated H.264 encoding: Chipset Requirements</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-119">As seguintes soluções de codificação de vídeo acelerada por hardware da Intel têm suporte:</span><span class="sxs-lookup"><span data-stu-id="a0cfa-119">The following Intel hardware accelerated video encoding solutions are supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="a0cfa-120">Os chipsets Intel HD 2000, 2500, 3000 e 4000 de terceira geração são de segunda geração (ou versões posteriores) com codificadores de vídeo de hardware integrados.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-120">Second and third generation Intel HD Graphics 2000, 2500, 3000, and 4000 chipsets (or later versions) with integrated hardware video encoders.</span></span> <span data-ttu-id="a0cfa-121">A instalação do driver Intel HD Graphics 15.28.9.2884 ou driver mais recente contendo os seguintes itens é necessária:</span><span class="sxs-lookup"><span data-stu-id="a0cfa-121">Installation of the Intel HD Graphics driver 15.28.9.2884 or the latest driver containing the following is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="a0cfa-122">Driver de vídeo 9.17.10.2884 ou driver mais recente</span><span class="sxs-lookup"><span data-stu-id="a0cfa-122">Display driver 9.17.10.2884 or the latest driver</span></span></p></li>
<li><p><span data-ttu-id="a0cfa-123">HMFT (Hardware media foundation transform) versão 3.12.10.31 ou HMFT mais recente</span><span class="sxs-lookup"><span data-stu-id="a0cfa-123">Hardware media foundation transform (HMFT) version 3.12.10.31 or the latest HMFT</span></span></p></li>
</ul></li>
</ul>
<p><span data-ttu-id="a0cfa-124">As seguintes soluções de codificação de vídeo aceleradas para hardware AMD são suportadas (requer atualizações do CU1 para o Lync Server 2013):</span><span class="sxs-lookup"><span data-stu-id="a0cfa-124">The following AMD hardware accelerated video encoding solutions are supported (requires CU1 Updates for Lync Server 2013):</span></span></p>
<ul>
<li><p><span data-ttu-id="a0cfa-p103">O Mecanismo de Codec de Vídeo da AMD, que está disponível em diversas placas gráficas e nas unidades de processamento aceleradas integradas de Processadores Acelerados AMD A-Series. O driver do Mecanismo de Codec de Vídeo AMD 9.12.0.0 ou superior deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-p103">AMD Video Codec Engine, which is available in several discrete graphics cards and in integrated accelerated processing units of AMD A-Series Accelerated Processors. The AMD Video Codec Engine driver 9.12.0.0 or higher must be installed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-127">Codificação H.264 acelerada por hardware: requisitos de câmera</span><span class="sxs-lookup"><span data-stu-id="a0cfa-127">Hardware accelerated H.264 encoding: Camera Requirements</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-128">Câmera de vídeo USB com codificador de hardware H.264 integrado em conformidade com a especificação USB Video Class (UVC) versão 1.5.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-128">USB video cameras with integrated H.264 hardware encoder that conforms to the USB Video Class (UVC) specification version 1.5.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="a0cfa-129">O Lync 2013 suporta UVC 1,5 câmeras com Windows 8 ou Windows 8,1, que inclui suporte para UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-129">Lync 2013 supports UVC 1.5 cameras with Windows 8 or Windows 8.1, which includes support for UVC 1.5.</span></span> <span data-ttu-id="a0cfa-130">Como o Windows 7 não inclui suporte para o UVC 1,5, o Lync 2013 trata câmeras UVC 1,5 como câmeras normais sem suporte para codificação de hardware.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-130">Because Windows 7 does not include support for UVC 1.5, Lync 2013 treats UVC 1.5 cameras as regular cameras with no hardware encoding support.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="determining-h264-video-encoding-and-decoding-capabilities"></a><span data-ttu-id="a0cfa-131">Determinação de recursos de codificação e decodificação de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="a0cfa-131">Determining H.264 Video Encoding and Decoding Capabilities</span></span>

<span data-ttu-id="a0cfa-132">Geralmente, há quatro fatores principais que determinam a capacidade máxima de codificação e decodificação de determinada configuração de computador:</span><span class="sxs-lookup"><span data-stu-id="a0cfa-132">Generally, there are four major factors that determine the maximum encoding and decoding capability of a particular computer configuration:</span></span>

  - <span data-ttu-id="a0cfa-133">Suporte para decodificação acelerada por hardware usando DXVA</span><span class="sxs-lookup"><span data-stu-id="a0cfa-133">Support for hardware accelerated decoding by using DXVA</span></span>

  - <span data-ttu-id="a0cfa-134">Suporte para codificação acelerada por hardware</span><span class="sxs-lookup"><span data-stu-id="a0cfa-134">Support for hardware accelerated encoding</span></span>

  - <span data-ttu-id="a0cfa-135">Número de núcleos físicos</span><span class="sxs-lookup"><span data-stu-id="a0cfa-135">Number of physical cores</span></span>

  - <span data-ttu-id="a0cfa-136">Índice de Experiência do Windows (WEI)</span><span class="sxs-lookup"><span data-stu-id="a0cfa-136">Windows Experience Index (WEI)</span></span>

<span data-ttu-id="a0cfa-137">A Ferramenta de Avaliação de Sistema do Windows (WinSAT) determina o WEI.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-137">The Windows System Assessment Tool (WinSAT) determines the WEI.</span></span> <span data-ttu-id="a0cfa-138">Quando você executa a ferramenta do WinSAT, ele gera um documento XML formal de avaliação no computador no diretório de repositório de documentos do WinSAT do% windir% \\ performance \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="a0cfa-138">When you run the WinSAT tool, it generates a Formal.Assessment XML document on the computer in the %windir%\\Performance\\WinSAT\\DataStore directory.</span></span> <span data-ttu-id="a0cfa-139">Esse arquivo XML contém as duas pontuações a seguir que são particularmente importantes para determinar as capacidades de codificação e decodificação:</span><span class="sxs-lookup"><span data-stu-id="a0cfa-139">This XML file contains the following two scores that are of particular importance for determining encoding and decoding capabilities:</span></span>

  - <span data-ttu-id="a0cfa-140">O VideoEncodeScore indica a capacidade de codificação de vídeo baseada em software do computador.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-140">The VideoEncodeScore indicates the software-based video encoding capability of the computer.</span></span>

  - <span data-ttu-id="a0cfa-141">O valor de GraphicsScore indica a capacidade de codificação acelerada por hardware do computador.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-141">The GraphicsScore value indicates the hardware accelerated encoding capability of the computer.</span></span>

<span data-ttu-id="a0cfa-p106">As três tabelas a seguir explicam a capacidade máxima de codificação e decodificação de diferentes tipos de PC, dependendo da aceleração de hardware que eles suportam. Para resoluções iguais ou maiores que 640x360, a taxa de quadros máxima suportada é de 30 quadros por segundo (fps). Para resoluções menores que 640x360, a taxa de quadros máxima suportada é de 15 fps.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-p106">The following three tables explain the maximum encoding and decoding capability for different PC types depending on what hardware acceleration they support. For resolutions of 640x360 and higher, the maximum supported frame rate is 30 frames per second (fps). For resolutions lower than 640x360, the maximum supported frame rate is 15 fps.</span></span>

### <a name="computer-without-dxva-and-without-hardware-accelerated-encoder"></a><span data-ttu-id="a0cfa-145">Computador sem DXVA e sem codificador acelerado por hardware</span><span class="sxs-lookup"><span data-stu-id="a0cfa-145">Computer Without DXVA And Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0cfa-146">Capacidade de resolução do codificador</span><span class="sxs-lookup"><span data-stu-id="a0cfa-146">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="a0cfa-147">Capacidade de resolução do decodificador</span><span class="sxs-lookup"><span data-stu-id="a0cfa-147">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="a0cfa-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0cfa-148">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-149">424x240</span><span class="sxs-lookup"><span data-stu-id="a0cfa-149">424x240</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-150">424x240 (640x360 a 15fps para cenários apenas de recepção)</span><span class="sxs-lookup"><span data-stu-id="a0cfa-150">424x240 (640x360 at 15fps for receive only scenarios)</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-151">1 Núcleo e VideoEncodeScore ≥ 4,0</span><span class="sxs-lookup"><span data-stu-id="a0cfa-151">1 Core and VideoEncodeScore ≥ 4.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-152">640x360</span><span class="sxs-lookup"><span data-stu-id="a0cfa-152">640x360</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-153">640x360</span><span class="sxs-lookup"><span data-stu-id="a0cfa-153">640x360</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-154">2 Núcleos e VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="a0cfa-154">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-155">640x360</span><span class="sxs-lookup"><span data-stu-id="a0cfa-155">640x360</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-156">1280x720</span><span class="sxs-lookup"><span data-stu-id="a0cfa-156">1280x720</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-157">2 Núcleos e VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="a0cfa-157">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-158">640x360</span><span class="sxs-lookup"><span data-stu-id="a0cfa-158">640x360</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-159">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-159">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-160">4 Núcleos e VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="a0cfa-160">4 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-161">1280x720</span><span class="sxs-lookup"><span data-stu-id="a0cfa-161">1280x720</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-162">1280x720</span><span class="sxs-lookup"><span data-stu-id="a0cfa-162">1280x720</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-163">4 Núcleos e VideoEncodeScore ≥ 7.3</span><span class="sxs-lookup"><span data-stu-id="a0cfa-163">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-164">1280x720</span><span class="sxs-lookup"><span data-stu-id="a0cfa-164">1280x720</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-165">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-165">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-166">4 Núcleos e VideoEncodeScore ≥ 7.3</span><span class="sxs-lookup"><span data-stu-id="a0cfa-166">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-167">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-167">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-168">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-168">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-169">N/D</span><span class="sxs-lookup"><span data-stu-id="a0cfa-169">N/A</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="computer-with-dxva-but-without-hardware-accelerated-encoder"></a><span data-ttu-id="a0cfa-170">Computador com DXVA, mas sem codificador acelerado por hardware</span><span class="sxs-lookup"><span data-stu-id="a0cfa-170">Computer With DXVA But Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0cfa-171">Capacidade de resolução do codificador</span><span class="sxs-lookup"><span data-stu-id="a0cfa-171">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="a0cfa-172">Capacidade de resolução do decodificador</span><span class="sxs-lookup"><span data-stu-id="a0cfa-172">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="a0cfa-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0cfa-173">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-174">424x240</span><span class="sxs-lookup"><span data-stu-id="a0cfa-174">424x240</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-175">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-175">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-176">1 Núcleo e VideoEncodeScore ≥ 3,0</span><span class="sxs-lookup"><span data-stu-id="a0cfa-176">1 Core and VideoEncodeScore ≥ 3.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-177">640x360</span><span class="sxs-lookup"><span data-stu-id="a0cfa-177">640x360</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-178">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-178">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-179">2 Núcleos e VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="a0cfa-179">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-180">960x540</span><span class="sxs-lookup"><span data-stu-id="a0cfa-180">960x540</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-181">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-181">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-182">2 Núcleos e VideoEncodeScore ≥ 6,0</span><span class="sxs-lookup"><span data-stu-id="a0cfa-182">2 Cores and VideoEncodeScore ≥ 6.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-183">1280x720</span><span class="sxs-lookup"><span data-stu-id="a0cfa-183">1280x720</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-184">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-184">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-185">4 Núcleos e VideoEncodeScore ≥ 6,7</span><span class="sxs-lookup"><span data-stu-id="a0cfa-185">4 Cores and VideoEncodeScore ≥ 6.7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-186">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-186">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-187">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-187">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-188">4 Núcleos e VideoEncodeScore ≥ 8,2</span><span class="sxs-lookup"><span data-stu-id="a0cfa-188">4 Cores and VideoEncodeScore ≥ 8.2</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a0cfa-p107">A pontuação WinSAT no Windows 7 está limitada ao máximo de 7,9. Dessa forma, a capacidade de codificação de um computador sem um codificador acelerado por hardware pode ser atingida somente no Windows 8 ou no Windows 8.1, onde a pontuação WinSAT máxima é 9,9.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-p107">The WinSAT score on Windows 7 is limited to a maximum of 7.9. Therefore, the encoding capability for a computer without a hardware accelerated encoder can only be achieved on Windows 8 or Windows 8.1, where the maximum WinSAT score is 9.9.</span></span>



</div>

### <a name="computer-with-dxva-and-with-intel-hd-graphics-hardware-accelerated-encoder"></a><span data-ttu-id="a0cfa-191">Computador com DXVA e codificador acelerado por hardware Intel HD Graphics</span><span class="sxs-lookup"><span data-stu-id="a0cfa-191">Computer With DXVA And With Intel HD Graphics Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0cfa-192">Capacidade de resolução do codificador</span><span class="sxs-lookup"><span data-stu-id="a0cfa-192">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="a0cfa-193">Capacidade de resolução do decodificador</span><span class="sxs-lookup"><span data-stu-id="a0cfa-193">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="a0cfa-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0cfa-194">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-195">1280x720</span><span class="sxs-lookup"><span data-stu-id="a0cfa-195">1280x720</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-196">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-196">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-197">Toda a segunda e a terceira geração Intel HD Graphics</span><span class="sxs-lookup"><span data-stu-id="a0cfa-197">All 2nd and 3rd generation Intel HD Graphics</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-198">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-198">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-199">1920x1080</span><span class="sxs-lookup"><span data-stu-id="a0cfa-199">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-200">Segunda e terceira geração Intel HD Graphics e GraphicsScore ≥ 5,0</span><span class="sxs-lookup"><span data-stu-id="a0cfa-200">2nd and 3rd generation Intel HD Graphics and GraphicsScore ≥ 5.0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="mobile-device-video-capabilities"></a><span data-ttu-id="a0cfa-201">Recursos de vídeo do dispositivo móvel</span><span class="sxs-lookup"><span data-stu-id="a0cfa-201">Mobile Device Video Capabilities</span></span>

<span data-ttu-id="a0cfa-202">A tabela a seguir descreve a capacidade máxima de vídeo para dispositivos móveis compatíveis.</span><span class="sxs-lookup"><span data-stu-id="a0cfa-202">The following table describes the maximum video capabilities for supported mobile devices.</span></span> <span data-ttu-id="a0cfa-203">Para obter mais informações sobre o suporte a dispositivos móveis, consulte [planejando para clientes móveis no Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span><span class="sxs-lookup"><span data-stu-id="a0cfa-203">For more information about mobile device support, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0cfa-204">Recurso</span><span class="sxs-lookup"><span data-stu-id="a0cfa-204">Feature</span></span></th>
<th><span data-ttu-id="a0cfa-205">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="a0cfa-205">Windows Phone</span></span></th>
<th><span data-ttu-id="a0cfa-206">iPhone</span><span class="sxs-lookup"><span data-stu-id="a0cfa-206">iPhone</span></span></th>
<th><span data-ttu-id="a0cfa-207">iPad</span><span class="sxs-lookup"><span data-stu-id="a0cfa-207">iPad</span></span></th>
<th><span data-ttu-id="a0cfa-208">Android</span><span class="sxs-lookup"><span data-stu-id="a0cfa-208">Android</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0cfa-209">Resolução máxima de codificação H.264</span><span class="sxs-lookup"><span data-stu-id="a0cfa-209">H.264 encoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-210">VGA</span><span class="sxs-lookup"><span data-stu-id="a0cfa-210">VGA</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-211">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="a0cfa-211">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="a0cfa-212">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="a0cfa-212">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="a0cfa-213">720p: iPhone 5S e posterior</span><span class="sxs-lookup"><span data-stu-id="a0cfa-213">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-214">VGA: iPad 2 e posterior/iPad mini 1 e posterior</span><span class="sxs-lookup"><span data-stu-id="a0cfa-214">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="a0cfa-215">720P: iPad Air/iPad mini 2/iPad Pro e posterior</span><span class="sxs-lookup"><span data-stu-id="a0cfa-215">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-216">Até VGA, dependendo do modelo do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a0cfa-216">Up to VGA depending on device model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0cfa-217">Resolução máxima de decodificação H.264</span><span class="sxs-lookup"><span data-stu-id="a0cfa-217">H.264 decoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-218">VGA</span><span class="sxs-lookup"><span data-stu-id="a0cfa-218">VGA</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-219">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="a0cfa-219">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="a0cfa-220">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="a0cfa-220">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="a0cfa-221">720p: iPhone 5S e posterior</span><span class="sxs-lookup"><span data-stu-id="a0cfa-221">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-222">VGA: iPad 2 e posterior/iPad mini 1 e posterior</span><span class="sxs-lookup"><span data-stu-id="a0cfa-222">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="a0cfa-223">720P: iPad Air/iPad mini 2/iPad Pro e posterior</span><span class="sxs-lookup"><span data-stu-id="a0cfa-223">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="a0cfa-224">Até VGA, dependendo do modelo do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a0cfa-224">Up to VGA depending on device model</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a0cfa-225">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0cfa-225">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

