---
title: 'Lync Server 2013: criar políticas de localização'
description: 'Lync Server 2013: criar políticas de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create location policies
ms:assetid: f1878194-c756-4794-8fa1-15dd2118b4b3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413006(v=OCS.15)
ms:contentKeyID: 48185794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 464ea9893890ab6185f180434e2dad13818123d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431929"
---
# <a name="create-location-policies-in-lync-server-2013"></a><span data-ttu-id="ecd2b-103">Criar políticas de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecd2b-103">Create location policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ecd2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ecd2b-104">

<span> </span></span></span>

<span data-ttu-id="ecd2b-105">_**Tópico da última modificação:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="ecd2b-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="ecd2b-106">O Lync Server usa uma política de localização para habilitar os clientes do Lync para E9-1-1 durante o registro do cliente.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-106">Lync Server uses a location policy to enable Lync clients for E9-1-1 during client registration.</span></span> <span data-ttu-id="ecd2b-107">Uma política de local contém as configurações que definem como o serviço E9-1-1 será implementado.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-107">A location policy contains the settings that define how E9-1-1 will be implemented.</span></span>

<span data-ttu-id="ecd2b-p102">É possível editar a política de localização global e criar novas políticas de localização sinalizadas. Um cliente obtém uma política global quando não está localizado dentro de uma sub-rede com uma política de localização associada ou quando o cliente não foi atribuído diretamente com uma política de localização. As políticas sinalizadas são atribuídas à sub-redes ou usuários.  </span><span class="sxs-lookup"><span data-stu-id="ecd2b-p102">You can edit the global location policy and create new tagged location policies. A client obtains a global policy when it is not located within a subnet with an associated location policy, or when the client has not been directly assigned a location policy. Tagged policies are assigned to subnets or users.</span></span>

<span data-ttu-id="ecd2b-111">Para criar uma política de localização, você deve usar uma conta membro do grupo RTCUniversalServerAdmins, membro da função administrativa CsVoiceAdministrator ou com direitos e permissões de administrador equivalentes.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-111">To create a location policy, you must use an account that is a member of the RTCUniversalServerAdmins group, or is a member of the CsVoiceAdministrator administrative role, or has equivalent administrator rights and permissions.</span></span>

<span data-ttu-id="ecd2b-112">Para obter uma descrição completa das políticas de localização, consulte [definindo a política de localização do Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="ecd2b-112">For a complete description of Location policies, see [Defining the location policy for Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span></span> <span data-ttu-id="ecd2b-113">Cmdlets neste procedimento usam uma política de localização definida com os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ecd2b-113">Cmdlets in this procedure use a location policy defined using the following values:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ecd2b-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="ecd2b-114">Element</span></span></th>
<th><span data-ttu-id="ecd2b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ecd2b-115">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ecd2b-116">EnhancedEmergencyServicesEnabled</span><span class="sxs-lookup"><span data-stu-id="ecd2b-116">EnhancedEmergencyServicesEnabled</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-117"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-117"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecd2b-118">LocationRequired</span><span class="sxs-lookup"><span data-stu-id="ecd2b-118">LocationRequired</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-119"><strong>Disclaimer</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-119"><strong>Disclaimer</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecd2b-120">EnhancedEmergencyServiceDisclaimer</span><span class="sxs-lookup"><span data-stu-id="ecd2b-120">EnhancedEmergencyServiceDisclaimer</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-p104">Sua empresa exige a definição de uma localização. Se você não a definir, os serviços de emergência não poderão localizá-lo em caso de emergência. Defina uma localização.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-p104">Your company policy requires you to set a location. If you do not set a location, emergency services will not be able to locate you in an emergency. Please set a location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecd2b-124">UseLocationForE911Only</span><span class="sxs-lookup"><span data-stu-id="ecd2b-124">UseLocationForE911Only</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-125"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-125"><strong>False</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecd2b-126">PstnUsage</span><span class="sxs-lookup"><span data-stu-id="ecd2b-126">PstnUsage</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-127"><strong>EmergencyUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-127"><strong>EmergencyUsage</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecd2b-128">EmergencyDialString</span><span class="sxs-lookup"><span data-stu-id="ecd2b-128">EmergencyDialString</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-129"><strong>911</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-129"><strong>911</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecd2b-130">EmergencyDialMask</span><span class="sxs-lookup"><span data-stu-id="ecd2b-130">EmergencyDialMask</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-131"><strong>112</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-131"><strong>112</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecd2b-132">NotificationUri</span><span class="sxs-lookup"><span data-stu-id="ecd2b-132">NotificationUri</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-133"><strong>sip:security@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-133"><strong>sip:security@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecd2b-134">ConferenceUri</span><span class="sxs-lookup"><span data-stu-id="ecd2b-134">ConferenceUri</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-135"><strong>sip:+14255550123@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-135"><strong>sip:+14255550123@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ecd2b-136">ConferenceMode</span><span class="sxs-lookup"><span data-stu-id="ecd2b-136">ConferenceMode</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-137"><strong>twoway</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-137"><strong>twoway</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ecd2b-138">LocationRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="ecd2b-138">LocationRefreshInterval</span></span></p></td>
<td><p><span data-ttu-id="ecd2b-139"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="ecd2b-139"><strong>2</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ecd2b-140">Para obter detalhes sobre como trabalhar com políticas de localização, consulte a documentação do Shell de gerenciamento do Lync Server para os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="ecd2b-140">For details about working with location policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="ecd2b-141">New-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd2b-141">New-CsLocationPolicy</span></span>

  - <span data-ttu-id="ecd2b-142">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd2b-142">Get-CsLocationPolicy</span></span>

  - <span data-ttu-id="ecd2b-143">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd2b-143">Set-CsLocationPolicy</span></span>

  - <span data-ttu-id="ecd2b-144">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd2b-144">Remove-CsLocationPolicy</span></span>

  - <span data-ttu-id="ecd2b-145">Grant-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd2b-145">Grant-CsLocationPolicy</span></span>

<div>

## <a name="to-create-location-policies"></a><span data-ttu-id="ecd2b-146">Para criar políticas de localização</span><span class="sxs-lookup"><span data-stu-id="ecd2b-146">To create location policies</span></span>

1.  <span data-ttu-id="ecd2b-147">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ecd2b-148">O CsLocationPolicy irá falhar se a configuração do <STRONG>PstnUsage</STRONG> ainda não estiver na lista Global de PstnUsages.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-148">CsLocationPolicy will fail if the setting for <STRONG>PstnUsage</STRONG> is not already in the Global list of PstnUsages.</span></span>

    
    </div>

2.  <span data-ttu-id="ecd2b-149">Opcionalmente, execute o seguinte cmdlet para editar a política de localização global:</span><span class="sxs-lookup"><span data-stu-id="ecd2b-149">Optionally, run the following cmdlet to edit the global Location Policy:</span></span>
    
        Set-CsLocationPolicy -Identity Global -EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -PstnUsage "emergencyUsage" -EmergencyDialString "911" -ConferenceMode "twoway" -ConferenceUri "sip:+14255550123@litwareinc.com" -EmergencyDialMask "112" NotificationUri "sip:security@litwareinc.com" -UseLocationForE911Only $true -LocationRefreshInterval 2

3.  <span data-ttu-id="ecd2b-150">Execute o seguinte para criar uma política de localização sinalizada.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-150">Run the following to create a tagged Location Policy.</span></span>
    
        New-CsLocationPolicy -Identity Tag:Redmond - EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -UseLocationForE911Only $false -PstnUsage "EmergencyUsage" -EmergencyDialString "911" -EmergencyDialMask "112" -NotificationUri "sip:security@litwareinc.com" -ConferenceUri "sip:+14255550123@litwareinc.com" -ConferenceMode "twoway" -LocationRefreshInterval 2

4.  <span data-ttu-id="ecd2b-151">Execute o seguinte cmdlet para aplicar a política de localização sinalizada criada na etapa 3 em uma política de usuário.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-151">Run the following cmdlet to apply the tagged Location Policy created in step 3 to a user policy.</span></span>
    
        (Get-CsUser | where { $_.Name -match "UserName" }) | Grant-CsLocationPolicy -PolicyName Redmond

<span data-ttu-id="ecd2b-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ecd2b-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

