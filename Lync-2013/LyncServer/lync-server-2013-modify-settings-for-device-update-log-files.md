---
title: 'Lync Server 2013: modificar as configurações dos arquivos de log de atualização do dispositivo'
description: 'Lync Server 2013: modifique as configurações dos arquivos de log de atualização do dispositivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify settings for Device Update log files
ms:assetid: 9b57f126-1853-43b3-bbd4-06401e6498bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182554(v=OCS.15)
ms:contentKeyID: 48184975
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c2086e11a67207a00ca99773cc818106b16d05c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445726"
---
# <a name="modify-settings-for-device-update-log-files-in-lync-server-2013"></a><span data-ttu-id="6bb2a-103">Modificar as configurações dos arquivos de log de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6bb2a-103">Modify settings for Device Update log files in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bb2a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bb2a-104">

<span> </span></span></span>

<span data-ttu-id="6bb2a-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="6bb2a-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="6bb2a-106">Você pode alterar as configurações de como as informações de atualização do dispositivo são registradas em sua organização usando o painel de controle do Lync Server ou o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-106">You can change settings for how device update information is logged in your organization by using Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="6bb2a-107">A tabela a seguir mostra quais configurações podem ser modificadas e quais ferramentas você usa para modificar as configurações.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-107">The following table shows which settings are modifiable, and which tool(s) you use to modify the settings.</span></span>

<span data-ttu-id="6bb2a-108">As configurações de log podem ser alteradas e aplicadas globalmente ou por site.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-108">Log settings can be changed and applied globally, or per site.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6bb2a-109">Para alterar</span><span class="sxs-lookup"><span data-stu-id="6bb2a-109">To change</span></span></th>
<th><span data-ttu-id="6bb2a-110">Usar</span><span class="sxs-lookup"><span data-stu-id="6bb2a-110">Use</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6bb2a-111">O tamanho máximo (em bytes) de um arquivo de log</span><span class="sxs-lookup"><span data-stu-id="6bb2a-111">The maximum size (in bytes) for a log file</span></span></p></td>
<td><p><span data-ttu-id="6bb2a-112">Painel de Controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-112">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="6bb2a-113">or</span><span class="sxs-lookup"><span data-stu-id="6bb2a-113">-or-</span></span></p>
<p><span data-ttu-id="6bb2a-114">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-114">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bb2a-115">A quantidade máxima de informações (em bytes) que podem ser mantidas no cache</span><span class="sxs-lookup"><span data-stu-id="6bb2a-115">The maximum amount of information (in bytes) that can be held in the cache</span></span></p></td>
<td><p><span data-ttu-id="6bb2a-116">Painel de Controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-116">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="6bb2a-117">or</span><span class="sxs-lookup"><span data-stu-id="6bb2a-117">-or-</span></span></p>
<p><span data-ttu-id="6bb2a-118">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-118">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bb2a-119">Com que frequência (em minutos) gravar informações armazenadas em cache no arquivo de log</span><span class="sxs-lookup"><span data-stu-id="6bb2a-119">How often (in minutes) to write cached information to the log file</span></span></p></td>
<td><p><span data-ttu-id="6bb2a-120">Painel de Controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-120">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="6bb2a-121">or</span><span class="sxs-lookup"><span data-stu-id="6bb2a-121">-or-</span></span></p>
<p><span data-ttu-id="6bb2a-122">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-122">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bb2a-123">Quanto tempo (em dias) para manter os arquivos de log</span><span class="sxs-lookup"><span data-stu-id="6bb2a-123">How long (in days) to keep log files</span></span></p></td>
<td><p><span data-ttu-id="6bb2a-124">Painel de Controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-124">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="6bb2a-125">or</span><span class="sxs-lookup"><span data-stu-id="6bb2a-125">-or-</span></span></p>
<p><span data-ttu-id="6bb2a-126">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-126">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bb2a-127">Quando (hora do dia) verificar se há arquivos expirados que devem ser excluídos</span><span class="sxs-lookup"><span data-stu-id="6bb2a-127">When (time of day) to check for expired files that should be deleted</span></span></p></td>
<td><p><span data-ttu-id="6bb2a-128">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-128">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6bb2a-129">Quais extensões de arquivo de log permitir</span><span class="sxs-lookup"><span data-stu-id="6bb2a-129">What log file extensions to permit</span></span></p></td>
<td><p><span data-ttu-id="6bb2a-130">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-130">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6bb2a-131">Quais tipos de arquivo de log manter</span><span class="sxs-lookup"><span data-stu-id="6bb2a-131">Which log file types to retain</span></span></p></td>
<td><p><span data-ttu-id="6bb2a-132">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-132">Lync Server Management Shell</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-change-logging-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="6bb2a-133">Para alterar as configurações de registro em log usando o painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="6bb2a-133">To change logging settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="6bb2a-134">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-134">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6bb2a-135">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6bb2a-135">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="6bb2a-136">Na barra de navegação à esquerda, clique em **clientes** e, em seguida, clique em **configuração do log do dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-136">In the left navigation bar, click **Clients**, and then click **Device Log Configuration**.</span></span>

3.  <span data-ttu-id="6bb2a-137">Na página **configuração de log do dispositivo** , clique duas vezes na configuração que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-137">On the **Device Log Configuration** page, double-click the configuration that you want to change.</span></span>

4.  <span data-ttu-id="6bb2a-138">Na caixa de diálogo **Editar configuração do log** , altere qualquer uma das seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="6bb2a-138">In the **Edit Log Setting** dialog box, change any of the following settings:</span></span>
    
      - <span data-ttu-id="6bb2a-139">**Tamanho máximo de arquivo (bytes)**   Especifica o tamanho máximo que um arquivo de log pode ficar antes de ser limpo.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-139">**Maximum file size (bytes)**   Specifies the maximum size a log file can become before it is purged.</span></span> <span data-ttu-id="6bb2a-140">O padrão é 1.024.000 bytes (1 MB).</span><span class="sxs-lookup"><span data-stu-id="6bb2a-140">The default is 1,024,000 bytes (1 MB).</span></span>
    
      - <span data-ttu-id="6bb2a-141">**Tamanho máximo do cache (bytes)**   Especifica a quantidade máxima de informações (em bytes) que podem ser mantidas no cache de arquivos de log antes que o cache deva ser limpo e os dados sejam gravados em um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-141">**Maximum cache size (bytes)**   Specifies the maximum amount of information (in bytes) that can be held in the log file cache before that cache must be cleared and the data is written to a log file.</span></span> <span data-ttu-id="6bb2a-142">O padrão é 512.000 bytes (0,5 MB).</span><span class="sxs-lookup"><span data-stu-id="6bb2a-142">The default is 512,000 bytes (0.5 MB).</span></span>
    
      - <span data-ttu-id="6bb2a-143">**Número de minutos para liberar o cache (1-60)**   Indica com que frequência as informações armazenadas no cache do arquivo de log são gravadas no arquivo de log real.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-143">**Number of minutes to flush cache (1-60)**   Indicates how often information stored in the log file cache is written to the actual log file.</span></span> <span data-ttu-id="6bb2a-144">Depois que os dados são registrados, o cache é limpo.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-144">After the data is logged, the cache is cleared.</span></span> <span data-ttu-id="6bb2a-145">O padrão é cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-145">The default is five minutes.</span></span>
    
      - <span data-ttu-id="6bb2a-146">**Número de dias para manter os arquivos de log (1-365)**   Especifica o número de dias durante os quais os arquivos de log são mantidos antes de serem limpos.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-146">**Number of days to keep log files (1-365)**   Specifies the number of days the log files are kept before they are purged.</span></span> <span data-ttu-id="6bb2a-147">O padrão é 10 dias.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-147">The default is 10 days.</span></span>

5.  <span data-ttu-id="6bb2a-148">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-148">Click **Commit**.</span></span>

</div>

<div>

## <a name="changing-logging-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="6bb2a-149">Alterando as configurações de log usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6bb2a-149">Changing Logging Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="6bb2a-150">As configurações de arquivo de log de atualização de dispositivo podem ser modificadas usando o Windows PowerShell e o cmdlet **set-CsDeviceUpdateConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="6bb2a-150">Device update log file settings can be modified by using Windows PowerShell and the **Set-CsDeviceUpdateConfiguration** cmdlet.</span></span> <span data-ttu-id="6bb2a-151">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-151">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6bb2a-152">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="6bb2a-152">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<span data-ttu-id="6bb2a-153">Os exemplos a seguir mostram algumas maneiras pelas quais você pode usar **set-CsDeviceUpdateConfiguration** para modificar as configurações.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-153">The following examples show a couple of the ways that you can use **Set-CsDeviceUpdateConfiguration** to modify settings.</span></span>

<div>

## <a name="to-modify-the-maximum-log-file-size-and-the-log-cleanup-interval"></a><span data-ttu-id="6bb2a-154">Para modificar o tamanho máximo do arquivo de log e o intervalo de limpeza do log</span><span class="sxs-lookup"><span data-stu-id="6bb2a-154">To modify the maximum log file size and the log cleanup interval</span></span>

  - <span data-ttu-id="6bb2a-155">O comando a seguir modifica as configurações do log de atualização de dispositivo aplicadas ao site Redmond.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-155">The following command modifies the device update log settings applied to the Redmond site.</span></span> <span data-ttu-id="6bb2a-156">Neste exemplo, o tamanho máximo do arquivo de log é definido como 204800 bytes, e o intervalo de limpeza do log é definido como 14 dias.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-156">In this example, the maximum log file size is set to 204800 bytes and the log cleanup interval is set to 14 days.</span></span>
    
        Set-CsDeviceUpdateConfiguration -Identity "site:Redmond" -MaxLogFileSize 204800 -LogCleanUpInterval 14.00:00:00

</div>

<div>

## <a name="to-modify-the-log-cleanup-time-of-day"></a><span data-ttu-id="6bb2a-157">Para modificar a hora de limpeza do log do dia</span><span class="sxs-lookup"><span data-stu-id="6bb2a-157">To modify the log cleanup time of day</span></span>

  - <span data-ttu-id="6bb2a-158">Esse comando define o tempo de limpeza do log para o site Redmond para 3:00 AM.</span><span class="sxs-lookup"><span data-stu-id="6bb2a-158">This command sets the log cleanup time for the Redmond site to 3:00 AM.</span></span>
    
        Set-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupTimeOfDay 03:00

</div>

<span data-ttu-id="6bb2a-159">Para obter detalhes, consulte o tópico da ajuda para o cmdlet [set-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsDeviceUpdateConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="6bb2a-159">For details, see the Help topic for the [Set-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsDeviceUpdateConfiguration) cmdlet.</span></span>

<span data-ttu-id="6bb2a-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bb2a-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

