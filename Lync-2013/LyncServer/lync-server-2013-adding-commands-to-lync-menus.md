---
title: 'Lync Server 2013: adicionar comandos aos menus do Lync'
description: 'Lync Server 2013: adicionar comandos aos menus do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding commands to Lync menus
ms:assetid: a8443bc2-e234-4022-870a-00700f38b1ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412788(v=OCS.15)
ms:contentKeyID: 48185091
ms.date: 04/11/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed4d62d085eaf115d107244ae50a7cc69e0aacd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439237"
---
# <a name="adding-commands-to-lync-menus-in-lync-server-2013"></a><span data-ttu-id="f6625-103">Adicionar comandos aos menus do Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6625-103">Adding commands to Lync menus in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6625-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6625-104">

<span> </span></span></span>

<span data-ttu-id="f6625-105">_**Tópico da última modificação:** 2016-04-11_</span><span class="sxs-lookup"><span data-stu-id="f6625-105">_**Topic Last Modified:** 2016-04-11_</span></span>

<span data-ttu-id="f6625-106">Você pode adicionar comandos personalizados aos menus do Lync 2013 e passar o URI (Uniform Resource Identifier) do SIP do usuário atual e os contatos selecionados para o aplicativo que o comando personalizado inicia.</span><span class="sxs-lookup"><span data-stu-id="f6625-106">You can add custom commands to Lync 2013 menus and pass the SIP Uniform Resource Identifier (URI) of the current user and selected contacts to the application that the custom command starts.</span></span>

<span data-ttu-id="f6625-107">Os comandos personalizados que você adiciona podem aparecer em um ou mais dos seguintes menus:</span><span class="sxs-lookup"><span data-stu-id="f6625-107">The custom commands that you add can appear on one or more of the following menus:</span></span>

  - <span data-ttu-id="f6625-108">O menu ferramentas, na barra de menus da janela principal do Lync</span><span class="sxs-lookup"><span data-stu-id="f6625-108">The Tools menu, on the menu bar in the Lync main window</span></span>

  - <span data-ttu-id="f6625-109">O menu de atalho para contatos na lista de contatos</span><span class="sxs-lookup"><span data-stu-id="f6625-109">The shortcut menu for contacts in the Contacts list</span></span>

  - <span data-ttu-id="f6625-110">O menu mais opções, na janela de conversa</span><span class="sxs-lookup"><span data-stu-id="f6625-110">The More Options menu, in the Conversation window</span></span>

  - <span data-ttu-id="f6625-111">O menu de atalho para as pessoas listadas na lista de participantes da janela de conversa</span><span class="sxs-lookup"><span data-stu-id="f6625-111">The shortcut menu for people listed in the Conversation window participant list</span></span>

  - <span data-ttu-id="f6625-112">O menu opções em um cartão de visita</span><span class="sxs-lookup"><span data-stu-id="f6625-112">The options menu in a contact card</span></span>

<span data-ttu-id="f6625-113">Você pode definir comandos personalizados para dois tipos de aplicativos — aplicativos que executam um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="f6625-113">You can define custom commands for two types of applications—applications that do either of the following:</span></span>

  - <span data-ttu-id="f6625-114">Aplicar somente ao usuário atual e são iniciados no computador local.</span><span class="sxs-lookup"><span data-stu-id="f6625-114">Apply only to the current user and are started on the local computer.</span></span>

  - <span data-ttu-id="f6625-115">Envolver usuários adicionais, como um programa de colaboração online, e deve ser iniciado no computador de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="f6625-115">Involve additional users, such as an online collaboration program, and must be started on each user's computer.</span></span>

<span data-ttu-id="f6625-116">O comando personalizado pode ser invocado das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="f6625-116">The custom command can be invoked in the following ways:</span></span>

  - <span data-ttu-id="f6625-117">Selecione um ou mais usuários e, em seguida, escolha o comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="f6625-117">Select one or more users, and then choose the custom command.</span></span>

  - <span data-ttu-id="f6625-118">Inicie uma conversa entre duas pessoas ou vários participantes e, em seguida, escolha o comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="f6625-118">Start a two-party or multiparty conversation, and then choose the custom command.</span></span>

<div>

## <a name="to-add-a-custom-command"></a><span data-ttu-id="f6625-119">Para adicionar um comando personalizado</span><span class="sxs-lookup"><span data-stu-id="f6625-119">To add a custom command</span></span>

<span data-ttu-id="f6625-120">Use as configurações do registro na tabela a seguir para adicionar um comando aos menus.</span><span class="sxs-lookup"><span data-stu-id="f6625-120">Use the registry settings in the following table to add a command to the menus.</span></span> <span data-ttu-id="f6625-121">Essas entradas são colocadas no registro em um dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="f6625-121">These entries are placed in the registry at one of the following locations:</span></span>

  - <span data-ttu-id="f6625-122">Para o sistema operacional de 32 bits: HKEY \_ local \_ Machine \\ SOFTWARE \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ apps</span><span class="sxs-lookup"><span data-stu-id="f6625-122">For 32bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

  - <span data-ttu-id="f6625-123">Para OS sistemas operacionais de 64 bits: HKEY \_ local \_ Machine \\ software \\ Wow6432Node \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ SessionManager \\ apps</span><span class="sxs-lookup"><span data-stu-id="f6625-123">For 64bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

### <a name="custom-command-registry-entries"></a><span data-ttu-id="f6625-124">Entradas de registro de comando personalizado</span><span class="sxs-lookup"><span data-stu-id="f6625-124">Custom Command Registry Entries</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6625-125">Nome</span><span class="sxs-lookup"><span data-stu-id="f6625-125">Name</span></span></th>
<th><span data-ttu-id="f6625-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6625-126">Type</span></span></th>
<th><span data-ttu-id="f6625-127">Dados</span><span class="sxs-lookup"><span data-stu-id="f6625-127">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6625-128">Nome</span><span class="sxs-lookup"><span data-stu-id="f6625-128">Name</span></span></p></td>
<td><p><span data-ttu-id="f6625-129">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f6625-129">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f6625-130">Nome do aplicativo exibido no menu.</span><span class="sxs-lookup"><span data-stu-id="f6625-130">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6625-131">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="f6625-131">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="f6625-132">DUPLA</span><span class="sxs-lookup"><span data-stu-id="f6625-132">DWORD</span></span></p></td>
<td><p><span data-ttu-id="f6625-133">0 = executável (padrão)</span><span class="sxs-lookup"><span data-stu-id="f6625-133">0 = Executable (default)</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="f6625-134">Requer ApplicationInstallPath.</span><span class="sxs-lookup"><span data-stu-id="f6625-134">Requires ApplicationInstallPath.</span></span>


</div>
<p><span data-ttu-id="f6625-135">1 = protocolo</span><span class="sxs-lookup"><span data-stu-id="f6625-135">1 = Protocol</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6625-136">ApplicationInstallPath</span><span class="sxs-lookup"><span data-stu-id="f6625-136">ApplicationInstallPath</span></span></p></td>
<td><p><span data-ttu-id="f6625-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f6625-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f6625-138">Caminho completo do executável.</span><span class="sxs-lookup"><span data-stu-id="f6625-138">Full path of the executable.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="f6625-139">Deve ser especificado se ApplicationType for 0 (executável).</span><span class="sxs-lookup"><span data-stu-id="f6625-139">Must be specified if ApplicationType is 0 (Executable).</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6625-140">Path</span><span class="sxs-lookup"><span data-stu-id="f6625-140">Path</span></span></p></td>
<td><p><span data-ttu-id="f6625-141">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f6625-141">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f6625-142">Caminho completo para ser iniciado juntamente com qualquer parâmetro, incluindo os parâmetros padrão <em>% User-ID%</em> e <em>% Contact-ID%</em>.</span><span class="sxs-lookup"><span data-stu-id="f6625-142">Full path to be started along with any parameters, including the default parameters <em>%user-id%</em> and <em>%contact-id%</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6625-143">SessionType</span><span class="sxs-lookup"><span data-stu-id="f6625-143">SessionType</span></span></p></td>
<td><p><span data-ttu-id="f6625-144">DUPLA</span><span class="sxs-lookup"><span data-stu-id="f6625-144">DWORD</span></span></p></td>
<td><p><span data-ttu-id="f6625-145">0 = sessão local.</span><span class="sxs-lookup"><span data-stu-id="f6625-145">0 = Local session.</span></span> <span data-ttu-id="f6625-146">O aplicativo é iniciado no computador local.</span><span class="sxs-lookup"><span data-stu-id="f6625-146">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="f6625-147">1 = sessão de dois participantes (padrão).</span><span class="sxs-lookup"><span data-stu-id="f6625-147">1 = Two-party session (default).</span></span> <span data-ttu-id="f6625-148">O Lync 2013 inicia o aplicativo localmente e, em seguida, envia uma notificação da área de trabalho para o outro usuário.</span><span class="sxs-lookup"><span data-stu-id="f6625-148">Lync 2013 starts the application locally and then sends a desktop notification to the other user.</span></span> <span data-ttu-id="f6625-149">O outro usuário clica na notificação para iniciar o aplicativo em seu computador.</span><span class="sxs-lookup"><span data-stu-id="f6625-149">The other user clicks the notification to start the application on their computer.</span></span></p>
<p><span data-ttu-id="f6625-150">2 = sessão com vários participantes.</span><span class="sxs-lookup"><span data-stu-id="f6625-150">2 = Multiparty session.</span></span> <span data-ttu-id="f6625-151">O Lync 2013 inicia o aplicativo localmente e, em seguida, envia notificações da área de trabalho para os outros usuários.</span><span class="sxs-lookup"><span data-stu-id="f6625-151">Lync 2013 starts the application locally and then sends desktop notifications to the other users.</span></span> <span data-ttu-id="f6625-152">O outro usuário clica na notificação para iniciar o aplicativo especificado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="f6625-152">The other user clicks the notification to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6625-153">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="f6625-153">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="f6625-154">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f6625-154">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f6625-155">Uma lista dos menus em que esse comando será exibido, separados por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="f6625-155">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="f6625-156">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="f6625-156">Possible values are:</span></span></p>
<p><span data-ttu-id="f6625-157">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="f6625-157">MainWindowActions</span></span></p>
<p><span data-ttu-id="f6625-158">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="f6625-158">MainWindowRightClick</span></span></p>
<p><span data-ttu-id="f6625-159">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="f6625-159">ConversationWindowActions</span></span></p>
<p><span data-ttu-id="f6625-160">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="f6625-160">ConversationWindowRightClick</span></span></p>
<p><span data-ttu-id="f6625-161">ContactCardMenu</span><span class="sxs-lookup"><span data-stu-id="f6625-161">ContactCardMenu</span></span></p>
<p><span data-ttu-id="f6625-162">Se ExtensibleMenu não for definido, os valores padrão de MainWindowRightClick e ConversationWindowActions serão usados.</span><span class="sxs-lookup"><span data-stu-id="f6625-162">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f6625-163">Por exemplo, o seguinte editor de registro (. REG) mostra os resultados da adição de um item de menu do Gerenciador de contatos de vendas da Contoso ao menu ações na janela de conversa:</span><span class="sxs-lookup"><span data-stu-id="f6625-163">For example, the following Registry Editor (.REG) file shows the results of adding a Contoso Sales Contact Manager menu item to Actions menu in the Conversation window:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Lync\SessionManager\Apps\{1F9F07C6-7E0B-462B-AAD7-98C6DBEA8F69}]
    "Name"="Contoso Sales Contact Manager"
    "HelpMessage"="The Contoso Sales Contact Manager is not installed. Contact the Help Desk for more information."
    "ApplicationType"=dword:00000000
    "ApplicationInstallPath"="C:\\cscm.exe"
    "Path"="C:\\cscm.exe %user-id% %contact-id%"
    "SessionType"=dword:00000001
    "ExtensibleMenu"="ConversationWindowActions;MainWindowRightClick"

</div>

<div>

## <a name="to-access-a-custom-command"></a><span data-ttu-id="f6625-164">Para acessar um comando personalizado</span><span class="sxs-lookup"><span data-stu-id="f6625-164">To access a custom command</span></span>

<span data-ttu-id="f6625-165">Para acessar um comando personalizado após ele ser adicionado, siga um destes procedimentos, dependendo dos valores de ExtensibleMenu que você definir:</span><span class="sxs-lookup"><span data-stu-id="f6625-165">To access a custom command after it is added, do one of the following, depending on the ExtensibleMenu values that you define:</span></span>

  - <span data-ttu-id="f6625-166">**MainWindowActions**   Na janela principal do Lync, clique em **ferramentas** e, em seguida, clique em seu comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="f6625-166">**MainWindowActions**   In the Lync main window, click **Tools**, and then click your custom command.</span></span>

  - <span data-ttu-id="f6625-167">**MainWindowRightClick**   Na janela principal do Lync, clique com o botão direito do mouse em um contato e clique no comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="f6625-167">**MainWindowRightClick**   In the Lync main window, right-click a contact, and then click your custom command.</span></span>

  - <span data-ttu-id="f6625-168">**ConversationWindowActions**   Na janela de conversa, clique no ícone **mais opções** e, em seguida, clique em seu comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="f6625-168">**ConversationWindowActions**   In the Conversation window, click the **More Options** icon, and then click your custom command.</span></span>

  - <span data-ttu-id="f6625-169">**ConversationWindowRightClick**   Na janela de conversa, clique com o botão direito do mouse no nome de um contato e, em seguida, clique em seu comando personalizado.</span><span class="sxs-lookup"><span data-stu-id="f6625-169">**ConversationWindowRightClick**   In the Conversation window, right-click a contact name, and then click your custom command.</span></span>

<span data-ttu-id="f6625-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6625-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

