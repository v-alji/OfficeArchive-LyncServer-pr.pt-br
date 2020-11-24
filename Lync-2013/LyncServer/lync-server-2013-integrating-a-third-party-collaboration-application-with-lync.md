---
title: Integrando um aplicativo de colaboração de terceiros com o Lync
description: Integrar um aplicativo de colaboração de terceiros com o Lync.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating a third-party collaboration application with Lync
ms:assetid: 00b9312c-b0c8-4f79-8b76-05b2d820e197
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398068(v=OCS.15)
ms:contentKeyID: 48183224
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adbe1abab83a569f581af034fc46abfef4cf819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390339"
---
# <a name="integrating-a-third-party-collaboration-application-with-lync-server-2013"></a><span data-ttu-id="9c25f-103">Integrando um aplicativo de colaboração de terceiros com o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c25f-103">Integrating a third-party collaboration application with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c25f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c25f-104">

<span> </span></span></span>

<span data-ttu-id="9c25f-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="9c25f-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="9c25f-106">Você pode integrar o Lync 2013 com qualquer aplicativo de colaboração online de terceiros adicionando informações sobre o aplicativo ao registro.</span><span class="sxs-lookup"><span data-stu-id="9c25f-106">You can integrate Lync 2013 with any third-party online collaboration application by adding information about the application to the registry.</span></span> <span data-ttu-id="9c25f-107">Você pode usar o Lync 2013 para iniciar sessões de conferência de dados hospedadas em um servidor interno, um serviço baseado na Internet ou ambos.</span><span class="sxs-lookup"><span data-stu-id="9c25f-107">You can use Lync 2013 to start data conferencing sessions hosted on an in-house server, an Internet-based service, or both.</span></span> <span data-ttu-id="9c25f-108">A sessão de colaboração ou de data conferência pode ser iniciada a partir da lista de contatos ou de uma sessão de mensagens instantâneas, voz ou vídeo existente.</span><span class="sxs-lookup"><span data-stu-id="9c25f-108">The collaboration or data conferencing session can be started from the Contacts list or from an existing instant messaging, voice, or video session.</span></span> <span data-ttu-id="9c25f-109">O Lync 2013 funciona apenas como veículo para iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c25f-109">Lync 2013 acts only as the vehicle for starting the application.</span></span> <span data-ttu-id="9c25f-110">Qualquer conversa existente do Lync 2013 permanecerá ativa após o início da sessão de colaboração online.</span><span class="sxs-lookup"><span data-stu-id="9c25f-110">Any existing Lync 2013 conversations remain active after the online collaboration session has begun.</span></span>

<span data-ttu-id="9c25f-111">As seções a seguir descrevem como integrar o Lync 2013 com aplicativos de colaboração baseados em servidor e baseados na Internet.</span><span class="sxs-lookup"><span data-stu-id="9c25f-111">The following sections describe how to integrate Lync 2013 with Internet-based and server-based collaboration applications.</span></span>

<div>

## <a name="integrating-an-internet-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="9c25f-112">Integrando um aplicativo de colaboração Internet-Based com o Lync 2013</span><span class="sxs-lookup"><span data-stu-id="9c25f-112">Integrating an Internet-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="9c25f-113">Geralmente, as etapas envolvidas na integração de um aplicativo de colaboração de terceiros são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="9c25f-113">Generally, the steps involved in integrating a third-party collaboration application are as follows:</span></span>

1.  <span data-ttu-id="9c25f-114">Informações sobre o aplicativo são adicionadas ao registro.</span><span class="sxs-lookup"><span data-stu-id="9c25f-114">Information about the application is added to the registry.</span></span>

2.  <span data-ttu-id="9c25f-115">O organizador entra no Lync 2013 e seleciona contatos para compartilhamento de dados e colaboração.</span><span class="sxs-lookup"><span data-stu-id="9c25f-115">The organizer signs in to Lync 2013 and selects contacts for data sharing and collaboration.</span></span> <span data-ttu-id="9c25f-116">Ou o organizador pode já estar em uma conversa e decidir adicionar a conferência de dados.</span><span class="sxs-lookup"><span data-stu-id="9c25f-116">Or, the organizer may already be in a conversation and decide to add data conferencing.</span></span>

3.  <span data-ttu-id="9c25f-117">O Lync 2013 lê o registro, inicia o aplicativo de colaboração e, em seguida, envia uma mensagem SIP personalizada — um appINVITE — para os participantes selecionados.</span><span class="sxs-lookup"><span data-stu-id="9c25f-117">Lync 2013 reads the registry, starts the collaboration application, and then sends a custom SIP message—an appINVITE—to the selected participants.</span></span>

4.  <span data-ttu-id="9c25f-118">Os participantes aceitam o convite e o aplicativo de colaboração é iniciado no computador de cada pessoa.</span><span class="sxs-lookup"><span data-stu-id="9c25f-118">Participants accept the invitation, and the collaboration application is started on each person’s computer.</span></span> <span data-ttu-id="9c25f-119">O Lync 2013 usa o registro para determinar qual aplicativo de colaboração usar e, em seguida, inicia esse aplicativo usando os parâmetros incluídos na mensagem appINVITE.</span><span class="sxs-lookup"><span data-stu-id="9c25f-119">Lync 2013 uses the registry to determine which collaboration application to use, and then starts that application by using the parameters included in the appINVITE message.</span></span>

<span data-ttu-id="9c25f-120">A tabela a seguir descreve as entradas do Registro necessárias para integrar um aplicativo de colaboração baseado na Internet com o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="9c25f-120">The following table describes the registry entries required to integrate an Internet-based collaboration application with Lync 2013.</span></span> <span data-ttu-id="9c25f-121">Essas entradas são colocadas no registro no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="9c25f-121">These entries are placed in the registry in the following location:</span></span>

  - <span data-ttu-id="9c25f-122">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ aplicativos \\ parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c25f-122">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="9c25f-123">Entradas do registro para um aplicativo de colaboração baseado na Internet</span><span class="sxs-lookup"><span data-stu-id="9c25f-123">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c25f-124">Nome</span><span class="sxs-lookup"><span data-stu-id="9c25f-124">Name</span></span></th>
<th><span data-ttu-id="9c25f-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c25f-125">Type</span></span></th>
<th><span data-ttu-id="9c25f-126">Dados</span><span class="sxs-lookup"><span data-stu-id="9c25f-126">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-127">Nome</span><span class="sxs-lookup"><span data-stu-id="9c25f-127">Name</span></span></p></td>
<td><p><span data-ttu-id="9c25f-128">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-128">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-129">O nome do aplicativo para os menus do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="9c25f-129">The application name for Lync 2013 menus.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25f-130">SmallIcon</span><span class="sxs-lookup"><span data-stu-id="9c25f-130">SmallIcon</span></span></p></td>
<td><p><span data-ttu-id="9c25f-131">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-131">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-132">Caminho para o ícone de 16 pixels x 16 pixels, BMP ou PNG.</span><span class="sxs-lookup"><span data-stu-id="9c25f-132">Path to 16-pixel x 16-pixel icon, BMP or PNG.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-133">Path</span><span class="sxs-lookup"><span data-stu-id="9c25f-133">Path</span></span></p></td>
<td><p><span data-ttu-id="9c25f-134">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-134">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-135">Caminho do participante para iniciar o aplicativo de colaboração online.</span><span class="sxs-lookup"><span data-stu-id="9c25f-135">Participant path for starting the online collaboration application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25f-136">OriginatorPath</span><span class="sxs-lookup"><span data-stu-id="9c25f-136">OriginatorPath</span></span></p></td>
<td><p><span data-ttu-id="9c25f-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-138">Caminho do organizador para iniciar o aplicativo de colaboração online.</span><span class="sxs-lookup"><span data-stu-id="9c25f-138">Organizer path for starting the online collaboration application.</span></span> <span data-ttu-id="9c25f-139">Esse caminho pode conter um ou mais parâmetros personalizados, conforme definido na subchave Parameters.</span><span class="sxs-lookup"><span data-stu-id="9c25f-139">This path can contain one or more custom parameters as defined in the Parameters subkey.</span></span> <span data-ttu-id="9c25f-140">Por exemplo, <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span><span class="sxs-lookup"><span data-stu-id="9c25f-140">For example, <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-141">SessionType</span><span class="sxs-lookup"><span data-stu-id="9c25f-141">SessionType</span></span></p></td>
<td><p><span data-ttu-id="9c25f-142">DUPLA</span><span class="sxs-lookup"><span data-stu-id="9c25f-142">DWORD</span></span></p></td>
<td><p><span data-ttu-id="9c25f-143">0 = sessão local.</span><span class="sxs-lookup"><span data-stu-id="9c25f-143">0 = Local session.</span></span> <span data-ttu-id="9c25f-144">O aplicativo é iniciado no computador local.</span><span class="sxs-lookup"><span data-stu-id="9c25f-144">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="9c25f-145">1 = sessão de dois participantes (padrão).</span><span class="sxs-lookup"><span data-stu-id="9c25f-145">1 = Two-party session (default).</span></span> <span data-ttu-id="9c25f-146">O Lync 2013 inicia o aplicativo localmente e, em seguida, envia uma notificação do sistema para o outro usuário.</span><span class="sxs-lookup"><span data-stu-id="9c25f-146">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="9c25f-147">O outro usuário clica na notificação e inicia o aplicativo especificado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="9c25f-147">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="9c25f-148">2 = sessão com vários participantes.</span><span class="sxs-lookup"><span data-stu-id="9c25f-148">2 = Multiparty session.</span></span> <span data-ttu-id="9c25f-149">O Lync 2013 inicia o aplicativo localmente e, em seguida, envia notificações do sistema para os outros usuários, solicitando que eles iniciem o aplicativo especificado em seu próprio computador.</span><span class="sxs-lookup"><span data-stu-id="9c25f-149">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their own computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25f-150">ExensibleMenu</span><span class="sxs-lookup"><span data-stu-id="9c25f-150">ExensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="9c25f-151">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-151">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-152">Uma lista dos menus em que esse comando será exibido, separados por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="9c25f-152">A list of the menus where this command will appear, separated by semi-colons.</span></span> <span data-ttu-id="9c25f-153">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="9c25f-153">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9c25f-154">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="9c25f-154">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="9c25f-155">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="9c25f-155">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="9c25f-156">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="9c25f-156">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="9c25f-157">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="9c25f-157">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="9c25f-158">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="9c25f-158">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="9c25f-159">Se ExtensibleMenu não for definido, os valores padrão de MainWindowRightClick e ConversationWindowActions serão usados.</span><span class="sxs-lookup"><span data-stu-id="9c25f-159">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c25f-160">A tabela a seguir descreve as entradas do registro para parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9c25f-160">The following table describes the registry entries for parameters.</span></span> <span data-ttu-id="9c25f-161">Essas entradas são locais em HKEY \_ \_ software user \\ atual \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ apps \\ Parameters.</span><span class="sxs-lookup"><span data-stu-id="9c25f-161">These entries are place at HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters.</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="9c25f-162">Entradas do registro para um aplicativo de colaboração baseado na Internet</span><span class="sxs-lookup"><span data-stu-id="9c25f-162">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c25f-163">Nome</span><span class="sxs-lookup"><span data-stu-id="9c25f-163">Name</span></span></th>
<th><span data-ttu-id="9c25f-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c25f-164">Type</span></span></th>
<th><span data-ttu-id="9c25f-165">Dados</span><span class="sxs-lookup"><span data-stu-id="9c25f-165">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-166">Param1</span><span class="sxs-lookup"><span data-stu-id="9c25f-166">Param1</span></span></p></td>
<td><p><span data-ttu-id="9c25f-167">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-167">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-168">Usado em formato de token ( <code>%Parm1%</code> ) para adicionar valores específicos do usuário para a chave do Registro OriginatorPath.</span><span class="sxs-lookup"><span data-stu-id="9c25f-168">Used in tokenized format (<code>%Parm1%</code>) to add user-specific values to the OriginatorPath registry key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25f-169">Param2</span><span class="sxs-lookup"><span data-stu-id="9c25f-169">Param2</span></span></p></td>
<td><p><span data-ttu-id="9c25f-170">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-170">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-171">Consulte param1.</span><span class="sxs-lookup"><span data-stu-id="9c25f-171">See Param1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-172">Param3</span><span class="sxs-lookup"><span data-stu-id="9c25f-172">Param3</span></span></p></td>
<td><p><span data-ttu-id="9c25f-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-174">Consulte param1.</span><span class="sxs-lookup"><span data-stu-id="9c25f-174">See Param1.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c25f-175">As configurações de registro de exemplo a seguir integram o cliente de colaboração do ADatum com o Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="9c25f-175">The following example registry settings integrate ADatum Collaboration Client with Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Path"="https://meetingservice.adatum.com/cc/%param1%/meet/%param2%"
    "OriginatorPath"="https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&role=present&pw=%param3%"
    "SessionType"=dword:00000002
    "ApplicationType"=dword:00000001
    "LiveServerIntegration"=dword:00000000
    "Name"="ADatum Online Collaboration Service"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"
    
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Param1"="meetserv"
    "Param2"="admin"
    "Param3"="abcdefg123"

</div>

<div>

## <a name="integrating-a-server-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="9c25f-176">Integrando um aplicativo de colaboração Server-Based com o Lync 2013</span><span class="sxs-lookup"><span data-stu-id="9c25f-176">Integrating a Server-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="9c25f-177">As configurações para adicionar comandos para iniciar um aplicativo de colaboração baseado em servidor no Lync 2013 são semelhantes às descritas na seção anterior, integrando um aplicativo de colaboração Internet-Based com o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="9c25f-177">The settings to add commands for starting a server-based collaboration application from within Lync 2013 are similar to those described in the previous section, Integrating an Internet-Based Collaboration Application with Lync 2013.</span></span> <span data-ttu-id="9c25f-178">No entanto, o OriginatorPath não é necessário e alguns valores são alterados.</span><span class="sxs-lookup"><span data-stu-id="9c25f-178">However, the OriginatorPath is not required, and some values are changed.</span></span> <span data-ttu-id="9c25f-179">As entradas do registro são colocadas no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="9c25f-179">Registry entries are placed in the following location:</span></span>

  - <span data-ttu-id="9c25f-180">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ aplicativos \\ parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c25f-180">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-a-server-based-collaboration-application"></a><span data-ttu-id="9c25f-181">Entradas do registro para um aplicativo de colaboração baseado em servidor</span><span class="sxs-lookup"><span data-stu-id="9c25f-181">Registry Entries for a Server-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c25f-182">Nome</span><span class="sxs-lookup"><span data-stu-id="9c25f-182">Name</span></span></th>
<th><span data-ttu-id="9c25f-183">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c25f-183">Type</span></span></th>
<th><span data-ttu-id="9c25f-184">Dados</span><span class="sxs-lookup"><span data-stu-id="9c25f-184">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-185">Nome</span><span class="sxs-lookup"><span data-stu-id="9c25f-185">Name</span></span></p></td>
<td><p><span data-ttu-id="9c25f-186">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-186">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-187">Nome do aplicativo exibido no menu.</span><span class="sxs-lookup"><span data-stu-id="9c25f-187">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25f-188">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="9c25f-188">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="9c25f-189">DUPLA</span><span class="sxs-lookup"><span data-stu-id="9c25f-189">DWORD</span></span></p></td>
<td><p><span data-ttu-id="9c25f-190">Valor = 1.</span><span class="sxs-lookup"><span data-stu-id="9c25f-190">Value = 1.</span></span> <span data-ttu-id="9c25f-191">Define o tipo de aplicativo como protocolo.</span><span class="sxs-lookup"><span data-stu-id="9c25f-191">Sets the application type to protocol.</span></span> <span data-ttu-id="9c25f-192">Os outros valores possíveis não se aplicam nesse caso.</span><span class="sxs-lookup"><span data-stu-id="9c25f-192">The other possible values do not apply in this case.</span></span> <span data-ttu-id="9c25f-193">Se não estiver presente, ApplicationType será definido como 0 (executável).</span><span class="sxs-lookup"><span data-stu-id="9c25f-193">If not present, ApplicationType is set to 0 (executable).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-194">Path</span><span class="sxs-lookup"><span data-stu-id="9c25f-194">Path</span></span></p></td>
<td><p><span data-ttu-id="9c25f-195">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-195">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-196">Protocolo usado para iniciar o aplicativo de colaboração.</span><span class="sxs-lookup"><span data-stu-id="9c25f-196">Protocol used to start the collaboration application.</span></span> <span data-ttu-id="9c25f-197">Para o Live Meeting 2007, o valor de Path é definido como <code>meet:%conf-uri%</code> .</span><span class="sxs-lookup"><span data-stu-id="9c25f-197">For Live Meeting 2007, the value of Path is set to <code>meet:%conf-uri%</code>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25f-198">SessionType</span><span class="sxs-lookup"><span data-stu-id="9c25f-198">SessionType</span></span></p></td>
<td><p><span data-ttu-id="9c25f-199">DUPLA</span><span class="sxs-lookup"><span data-stu-id="9c25f-199">DWORD</span></span></p></td>
<td><p><span data-ttu-id="9c25f-200">0 = sessão local.</span><span class="sxs-lookup"><span data-stu-id="9c25f-200">0 = Local session.</span></span> <span data-ttu-id="9c25f-201">O aplicativo é iniciado no computador local.</span><span class="sxs-lookup"><span data-stu-id="9c25f-201">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="9c25f-202">1 = sessão de dois participantes (padrão).</span><span class="sxs-lookup"><span data-stu-id="9c25f-202">1 = Two-party session (default).</span></span> <span data-ttu-id="9c25f-203">O Lync 2013 inicia o aplicativo localmente e, em seguida, envia uma notificação do sistema para o outro usuário.</span><span class="sxs-lookup"><span data-stu-id="9c25f-203">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="9c25f-204">O outro usuário clica na notificação e inicia o aplicativo especificado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="9c25f-204">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="9c25f-205">2 = sessão com vários participantes.</span><span class="sxs-lookup"><span data-stu-id="9c25f-205">2 = Multiparty session.</span></span> <span data-ttu-id="9c25f-206">O Lync 2013 inicia o aplicativo localmente e, em seguida, envia notificações do sistema para os outros usuários, solicitando que eles iniciem o aplicativo especificado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="9c25f-206">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c25f-207">MCUType</span><span class="sxs-lookup"><span data-stu-id="9c25f-207">MCUType</span></span></p></td>
<td><p><span data-ttu-id="9c25f-208">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-208">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-209">DATA = o tipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="9c25f-209">DATA = The type of server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25f-210">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="9c25f-210">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="9c25f-211">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9c25f-211">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9c25f-212">Uma lista dos menus em que esse comando será exibido, separados por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="9c25f-212">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="9c25f-213">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="9c25f-213">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="9c25f-214">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="9c25f-214">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="9c25f-215">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="9c25f-215">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="9c25f-216">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="9c25f-216">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="9c25f-217">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="9c25f-217">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="9c25f-218">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="9c25f-218">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="9c25f-219">Se ExtensibleMenu não for definido, os valores padrão de MainWindowRightClick e ConversationWindowActions serão usados.</span><span class="sxs-lookup"><span data-stu-id="9c25f-219">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c25f-220">O exemplo a seguir adiciona comandos para iniciar o ADatum de colaboração do cliente no Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="9c25f-220">The following example adds commands to start ADatum Collaboration Client from within Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{27877e66-615c-4582-ab88-0cb2ca05d951}]
    "Path"="meet:%conf-uri%"
    "SessionType"=dword:00000002
    "LiveServerIntegration"=dword:00000001
    "ApplicationType"=dword:00000001
    "Name"="ADatum Collaboration Client"
    "MCUType"="Data"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"

<span data-ttu-id="9c25f-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c25f-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

