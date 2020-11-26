---
title: Configurando a transferência de arquivos e a filtragem de URL para mensagens instantâneas (IM)
description: Configurar a transferência de arquivos e a filtragem de URL para mensagens instantâneas (IM).
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring file transfer and URL filtering for instant messaging (IM)
ms:assetid: 115a1a2c-599f-474c-a063-52f7144b5246
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520952(v=OCS.15)
ms:contentKeyID: 48183440
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92f11c3f3bb924c1d92361c2635bfb37e1f03175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433105"
---
# <a name="configuring-file-transfer-and-url-filtering-for-instant-messaging-im-in-lync-server-2013"></a><span data-ttu-id="d73bf-103">Configurar a transferência de arquivos e a filtragem de URL para mensagens instantâneas (IM) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d73bf-103">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d73bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d73bf-104">

<span> </span></span></span>

<span data-ttu-id="d73bf-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d73bf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d73bf-106">A ferramenta inteligente de filtro de IM ajuda a proteger a implantação do Lync Server 2013 contra a disseminação das formas mais comuns de vírus com uma redução mínima para a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="d73bf-106">The Intelligent IM Filter tool helps protect your Lync Server 2013 deployment against the spread of the most common forms of viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="d73bf-107">Use o filtro de IM inteligente para configurar filtros para bloquear mensagens instantâneas não solicitadas ou perigosas de pontos de extremidade desconhecidos fora do firewall corporativo.</span><span class="sxs-lookup"><span data-stu-id="d73bf-107">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="d73bf-108">Você pode configurar filtros especificando os critérios a serem usados para determinar o que deve ser bloqueado, como mensagens instantâneas contendo hiperlinks com prefixos e arquivos específicos com extensões específicas.</span><span class="sxs-lookup"><span data-stu-id="d73bf-108">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks with specific prefixes and files with specific extensions.</span></span>

<span data-ttu-id="d73bf-109">O filtro de IM inteligente fornece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d73bf-109">Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="d73bf-110">Filtragem de URL aprimorada.</span><span class="sxs-lookup"><span data-stu-id="d73bf-110">Enhanced URL filtering.</span></span>

  - <span data-ttu-id="d73bf-111">Filtragem de transferência de arquivos aprimorada.</span><span class="sxs-lookup"><span data-stu-id="d73bf-111">Enhanced file transfer filtering.</span></span>

<span data-ttu-id="d73bf-112">A configuração do filtro de IM inteligente inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d73bf-112">Configuring Intelligent IM Filter includes the following:</span></span>

  - <span data-ttu-id="d73bf-113">Configurar a filtragem de URL.</span><span class="sxs-lookup"><span data-stu-id="d73bf-113">Configuring URL filtering.</span></span>

  - <span data-ttu-id="d73bf-114">Configurar a filtragem de transferência de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d73bf-114">Configuring file transfer filtering.</span></span>

<div>

## <a name="how-filtering-options-are-applied-to-instant-messages"></a><span data-ttu-id="d73bf-115">Como as opções de filtragem são aplicadas às mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="d73bf-115">How Filtering Options Are Applied to Instant Messages</span></span>

<span data-ttu-id="d73bf-116">Antes de implantar a ferramenta de filtro de mensagem de chat inteligente, você precisa entender como as opções de filtragem são aplicadas à medida que as mensagens são roteadas de um servidor do Lync Server 2013 para outro.</span><span class="sxs-lookup"><span data-stu-id="d73bf-116">Before you deploy the Intelligent IM Message Filter tool, you need to understand how filtering options are applied as messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="d73bf-117">A maneira como essas opções de filtragem são consistentes é consistente, independentemente de os servidores estarem localizados em uma única organização ou entre fronteiras organizacionais.</span><span class="sxs-lookup"><span data-stu-id="d73bf-117">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="d73bf-118">Essa consistência se aplica à maneira como o aviso e o texto de aviso personalizados são inseridos em mensagens e enviados entre servidores.</span><span class="sxs-lookup"><span data-stu-id="d73bf-118">This consistency applies to the way that the customized notice and warning texts are inserted into messages and sent across servers.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="d73bf-119">O filtro de mensagem instantânea aumenta a quantidade de recursos de CPU necessários para processar URLs em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d73bf-119">The instant message filter increases the amount of CPU resources required to process URLs in a message.</span></span> <span data-ttu-id="d73bf-120">Esse aumento na demanda de CPU também afeta o desempenho do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d73bf-120">This increase in CPU demand also affects the performance of Lync Server.</span></span>



</div>

<span data-ttu-id="d73bf-121">Usando a página **filtro de URL** no grupo **mensagens instantâneas e presença** no painel de controle do Lync Server, você pode bloquear alguns ou todos os hiperlinks ou configurar um aviso.</span><span class="sxs-lookup"><span data-stu-id="d73bf-121">By using the **URL Filter** page in the **IM and Presence** group in Lync Server Control Panel, you can block some or all hyperlinks or configure a warning.</span></span> <span data-ttu-id="d73bf-122">O aviso é inserido no início de uma mensagem instantânea que contém um hiperlink quando você escolhe a opção de **prefixo de hiperlink** **Enviar mensagem de aviso**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-122">The warning is inserted at the beginning of an instant message that contains a hyperlink when you choose the **Hyperlink prefix** option **Send warning message**.</span></span>

<span data-ttu-id="d73bf-123">Quando uma mensagem instantânea transita de um servidor para outro, as seguintes diretrizes gerais se aplicam:</span><span class="sxs-lookup"><span data-stu-id="d73bf-123">When an instant message travels from one server to another, the following general guidelines apply:</span></span>

  - <span data-ttu-id="d73bf-124">Se um servidor bloquear uma mensagem instantânea (porque você marcou a caixa de seleção **Bloquear URLs com extensão de arquivo** na página **filtro de URL** ou porque você escolheu a opção de **prefixo de hiperlink** **Bloquear hiperlinks**), uma mensagem de erro será retornada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="d73bf-124">If a server blocks an instant message (because you selected the **Block URLs with file extension** check box on the **URL Filter** page or because you chose the **Hyperlink prefix** option **Block hyperlinks**), an error message is returned to the client.</span></span> <span data-ttu-id="d73bf-125">Os servidores subsequentes não recebem esta mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="d73bf-125">Subsequent servers do not receive this instant message.</span></span>

  - <span data-ttu-id="d73bf-126">Se um servidor (Server1) adicionar um aviso a uma mensagem de chat que contém um hiperlink ativo, um servidor subsequente (Server2) que receber essa mensagem instantânea ainda poderá executar uma ação diferente com base nesse hiperlink ativo presente na mensagem instantânea e bloquear a mensagem instantânea ou adicionar um aviso.</span><span class="sxs-lookup"><span data-stu-id="d73bf-126">If a server (Server1) adds a warning to an instant message that contains an active hyperlink, a subsequent server (Server2) that receives this instant message can still take a different action based on this active hyperlink present in the instant message and block the instant message or add a warning.</span></span> <span data-ttu-id="d73bf-127">Se Server2 estiver configurado somente para adicionar um aviso para esta URL, o aviso anterior adicionado pelo Server1 será removido, e o aviso configurado no Server2 será adicionado ao início da mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="d73bf-127">If Server2 is configured only to add a warning for this URL, the earlier warning added by Server1 is removed, and the warning configured on Server2 is added to the beginning of the instant message.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="d73bf-128">Se você estiver executando o Lync Server 2013 em um ambiente misto, o Live Communications Server 2005 com SP1 é a versão mínima necessária para usar o aplicativo filtro inteligente de IM.</span><span class="sxs-lookup"><span data-stu-id="d73bf-128">If you are running Lync Server 2013 in a mixed environment, Live Communications Server 2005 with SP1 is the minimum version required to use the Intelligent IM Filter application.</span></span> <span data-ttu-id="d73bf-129">Não há suporte para o filtro de IM inteligente no Live Communications Server 2005 sem SP1.</span><span class="sxs-lookup"><span data-stu-id="d73bf-129">The Intelligent IM Filter is not supported on Live Communications Server 2005 without SP1.</span></span>



</div>

<div>

## <a name="url-filtering"></a><span data-ttu-id="d73bf-130">Filtragem de URL</span><span class="sxs-lookup"><span data-stu-id="d73bf-130">URL Filtering</span></span>

<span data-ttu-id="d73bf-131">As URLs são filtradas de acordo com o prefixo do hiperlink.</span><span class="sxs-lookup"><span data-stu-id="d73bf-131">URLs are filtered according to their hyperlink prefix.</span></span> <span data-ttu-id="d73bf-132">Os exemplos a seguir são prefixos válidos:</span><span class="sxs-lookup"><span data-stu-id="d73bf-132">The following examples are valid prefixes:</span></span>

  - <span data-ttu-id="d73bf-133">www \* .</span><span class="sxs-lookup"><span data-stu-id="d73bf-133">www\*.</span></span>

  - <span data-ttu-id="d73bf-134">FTP.</span><span class="sxs-lookup"><span data-stu-id="d73bf-134">ftp.</span></span>

  - <span data-ttu-id="d73bf-135">http</span><span class="sxs-lookup"><span data-stu-id="d73bf-135">http:</span></span>

<span data-ttu-id="d73bf-136">Se você não configurar o filtro de mensagem instantânea para executar qualquer filtragem de URL, todas as URLs contidas em mensagens instantâneas serão passadas de forma não modificada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="d73bf-136">If you do not configure the instant message filter to perform any URL filtering, all URLs contained in instant messages are passed unmodified through the server.</span></span> <span data-ttu-id="d73bf-137">Se você configurar o filtro de mensagem instantânea para executar a filtragem de URL, as URLs nas mensagens instantâneas serão filtradas de acordo com as opções que você selecionar na caixa de diálogo **Editar Filtro de URL** ou **novo filtro de URL** .</span><span class="sxs-lookup"><span data-stu-id="d73bf-137">If you configure the instant message filter to perform URL filtering, URLs in instant messages are filtered according to the options that you select in the **Edit URL Filter** or **New URL Filter** dialog box.</span></span>

  - <span data-ttu-id="d73bf-138">**Habilitar o filtro de URL**   Essa opção habilita a filtragem de URL para a implantação global ou para o site que você selecionar.</span><span class="sxs-lookup"><span data-stu-id="d73bf-138">**Enable URL filter**   This option enables URL filtering for the global deployment or for the site that you select.</span></span>

  - <span data-ttu-id="d73bf-139">**Bloquear URLs com extensão de arquivo**   O filtro de mensagem instantânea bloqueia qualquer URL ativa da Internet ou da Internet que contém um arquivo com uma extensão listada em **extensões de tipo de arquivo a serem bloqueadas** na caixa de diálogo **Editar Filtro de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="d73bf-139">**Block URLs with file extension**   The instant message filter blocks any active intranet or Internet URL that contains a file with an extension listed under **File type extensions to block** in the **Edit File Filter** dialog box.</span></span> <span data-ttu-id="d73bf-140">Quando uma URL é bloqueada, uma mensagem de erro é exibida para o remetente.</span><span class="sxs-lookup"><span data-stu-id="d73bf-140">When a URL is blocked, an error message is displayed to the sender.</span></span> <span data-ttu-id="d73bf-141">Quando selecionada, essa opção tem precedência sobre todas as outras opções de filtragem para qualquer extensão de arquivo definida em **extensões de tipo de arquivo a serem bloqueadas**.</span><span class="sxs-lookup"><span data-stu-id="d73bf-141">When selected, this option takes precedence over all other filtering options for any file extensions defined under **File type extensions to block**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="d73bf-142">A filtragem de extensões de arquivo limita-se a nomes de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="d73bf-142">Filtering of file extensions is limited to standard file names.</span></span> <span data-ttu-id="d73bf-143">A filtragem pode não funcionar com extensões de arquivo inseridas em outros nomes.</span><span class="sxs-lookup"><span data-stu-id="d73bf-143">Filtering may not work with file extensions embedded in other names.</span></span>

    
    </div>

<span data-ttu-id="d73bf-144">Para configurar como os hiperlinks são manipulados nas conversas de mensagens instantâneas, selecione uma das seguintes opções em **prefixo do hiperlink**:</span><span class="sxs-lookup"><span data-stu-id="d73bf-144">To configure how hyperlinks are handled in instant message conversations, select one of the following options under **Hyperlink prefix**:</span></span>

  - <span data-ttu-id="d73bf-145">Não **Filtrar**   As URLs nas mensagens são enviadas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="d73bf-145">**Do not filter**   URLs in messages are sent through the server.</span></span> <span data-ttu-id="d73bf-146">Quando você escolhe essa opção, a caixa de **mensagem permitir** é exibida.</span><span class="sxs-lookup"><span data-stu-id="d73bf-146">When you choose this option, the **Allow message** box appears.</span></span> <span data-ttu-id="d73bf-147">Na caixa de **mensagem permitir** , especifique o aviso que você deseja inserir no início de cada mensagem instantânea contendo hiperlinks.</span><span class="sxs-lookup"><span data-stu-id="d73bf-147">In the **Allow message** box, specify the notice that you want to insert at the beginning of each instant message containing hyperlinks.</span></span> <span data-ttu-id="d73bf-148">Este aviso pode consistir em no máximo 65535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d73bf-148">This notice can consist of no more than 65535 characters.</span></span>

  - <span data-ttu-id="d73bf-149">**Bloquear hiperlinks**   A entrega de mensagens instantâneas com hiperlinks ativos é bloqueada pelo Lync Server, e uma mensagem de erro é exibida para o remetente.</span><span class="sxs-lookup"><span data-stu-id="d73bf-149">**Block hyperlinks**   Delivery of instant messages containing active hyperlinks is blocked by Lync Server, and an error message is displayed to the sender.</span></span>

  - <span data-ttu-id="d73bf-150">**Enviar mensagem de aviso**   O Lync Server permite hiperlinks ativos em mensagens instantâneas, mas inclui um aviso.</span><span class="sxs-lookup"><span data-stu-id="d73bf-150">**Send warning message**   Lync Server permits active hyperlinks in instant messages, but it includes a warning.</span></span> <span data-ttu-id="d73bf-151">Quando você escolhe essa opção, a caixa de **mensagem de aviso** é exibida.</span><span class="sxs-lookup"><span data-stu-id="d73bf-151">When you choose this option, the **Warning message** box appears.</span></span> <span data-ttu-id="d73bf-152">Na caixa de **mensagem de aviso** , você deve digitar o aviso que deseja incluir com mensagens instantâneas que contenham hiperlinks válidos.</span><span class="sxs-lookup"><span data-stu-id="d73bf-152">In the **Warning message** box, you must type the warning that you want to include with instant messages containing valid hyperlinks.</span></span> <span data-ttu-id="d73bf-153">Por exemplo, este aviso pode declarar os possíveis perigos de clicar em um link desconhecido, ou pode se referir às políticas e requisitos relevantes da sua organização.</span><span class="sxs-lookup"><span data-stu-id="d73bf-153">For example, this warning might state the potential dangers of clicking an unknown link, or it might refer to your organization’s relevant policies and requirements.</span></span> <span data-ttu-id="d73bf-154">O aviso não pode ter mais de 65535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d73bf-154">The warning can be no more than 65535 characters.</span></span>

<span data-ttu-id="d73bf-155">Se você selecionar **Bloquear hiperlinks** ou **Enviar uma mensagem de aviso**, as seguintes opções estarão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="d73bf-155">If you select **Block hyperlinks** or **Send warning message**, the following options are available:</span></span>

  - <span data-ttu-id="d73bf-156">**Excluir hiperlinks da intranet local**   O filtro de mensagem instantânea bloqueia somente URLs da Internet.</span><span class="sxs-lookup"><span data-stu-id="d73bf-156">**Exclude local intranet hyperlinks**   The instant message filter blocks only Internet URLs.</span></span> <span data-ttu-id="d73bf-157">As URLs para locais na sua intranet são passadas de forma não modificada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="d73bf-157">URLs for locations within your intranet are passed unmodified through the server.</span></span> <span data-ttu-id="d73bf-158">No entanto, as URLs de intranet que os servidores individuais que executam o Lync Server passam dependem de quais tipos de sites locais são considerados parte da zona da intranet deles.</span><span class="sxs-lookup"><span data-stu-id="d73bf-158">However, the intranet URLs that individual servers running Lync Server pass depend on which types of local websites are considered part of their intranet zone.</span></span> <span data-ttu-id="d73bf-159">Para verificar as configurações de zona da intranet de um servidor, consulte o procedimento "para configurar suas configurações de intranet no Internet Explorer" em [Modificar o filtro de URL padrão no Lync server 2013](lync-server-2013-modify-the-default-url-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d73bf-159">To check a server’s intranet zone settings, see the “To configure your intranet settings in Internet Explorer” procedure in [Modify the default URL filter in Lync Server 2013](lync-server-2013-modify-the-default-url-filter.md).</span></span>

  - <span data-ttu-id="d73bf-160">**Filtrar esses prefixos de hiperlink**   Para escolher quais prefixos deseja bloquear, clique em **selecionar** e, em seguida, no **prefixo selecionar Hiperlink**, adicione os prefixos à lista **prefixos de hiperlink** .</span><span class="sxs-lookup"><span data-stu-id="d73bf-160">**Filter these hyperlink prefixes**   To choose which prefixes you want to block, click **Select**, and then, in **Select Hyperlink Prefix**, add the prefixes to the **Hyperlink prefixes** list.</span></span>
    
    <span data-ttu-id="d73bf-161">Todos os prefixos exceto **href** devem terminar com um ponto ou dois-pontos, ou um asterisco seguido por um ponto.</span><span class="sxs-lookup"><span data-stu-id="d73bf-161">All prefixes except **href** must end with a period or a colon, or an asterisk followed by a period.</span></span> <span data-ttu-id="d73bf-162">Prefixos válidos podem conter qualquer caractere no conjunto de caracteres de URL válidos, exceto o asterisco ( \* ).</span><span class="sxs-lookup"><span data-stu-id="d73bf-162">Valid prefixes can contain any characters in the set of valid URL characters except the asterisk (\*).</span></span> <span data-ttu-id="d73bf-163">O conjunto de caracteres válidos para URL é: \# \* +/0123456789 = @ABCDEFGHIJKLMNOPQRSTUVWXYZ ^ \_ \` abcdefghijklmnopqrstuvwxyz | ~</span><span class="sxs-lookup"><span data-stu-id="d73bf-163">The set of valid URL characters is: \#\*+/0123456789=@ABCDEFGHIJKLMNOPQRSTUVWXYZ^\_\` abcdefghijklmnopqrstuvwxyz|~</span></span>

</div>

<div>

## <a name="file-transfer-filtering"></a><span data-ttu-id="d73bf-164">Filtragem de transferência de arquivo</span><span class="sxs-lookup"><span data-stu-id="d73bf-164">File Transfer Filtering</span></span>

<span data-ttu-id="d73bf-165">A filtragem de transferência de filtro afeta mensagens instantâneas e conferências.</span><span class="sxs-lookup"><span data-stu-id="d73bf-165">Filter transfer filtering affects both instant messages and conferences.</span></span> <span data-ttu-id="d73bf-166">Em conferências, essas configurações afetam o recurso folheto no cliente do Office Live Meeting 2007 e os recursos de reprodução de multimídia.</span><span class="sxs-lookup"><span data-stu-id="d73bf-166">For conferences, these settings affect the handout feature in the Office Live Meeting 2007 client and multimedia playback features.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="d73bf-167">O Lync Server também oferece opções de configuração de transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d73bf-167">Lync Server also offers file transfer setting options.</span></span> <span data-ttu-id="d73bf-168">Essa opção do lado do servidor é oferecida além dos controles do lado do cliente disponíveis no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d73bf-168">This server-side option is offered in addition to the client-side controls available in Lync Server.</span></span>



</div>

<span data-ttu-id="d73bf-169">Você pode filtrar transferências de arquivos durante conversas de mensagem instantânea, quando estiver usando o recurso folheto no cliente do Office Live Meeting 2007 e para recursos de reprodução de multimídia para todos os tipos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d73bf-169">You can filter file transfers during instant message conversations, when you are using the handout feature in the Office Live Meeting 2007 client, and for multimedia playback features for all file types.</span></span> <span data-ttu-id="d73bf-170">Você pode definir as seguintes opções para controlar as transferências de arquivos:</span><span class="sxs-lookup"><span data-stu-id="d73bf-170">You can set the following options to control file transfers:</span></span>

  - <span data-ttu-id="d73bf-171">**Habilitar filtro de arquivo**   Essa opção habilita a filtragem de arquivo para a implantação global ou para o site que você selecionar.</span><span class="sxs-lookup"><span data-stu-id="d73bf-171">**Enable file filter**   This option enables file filtering for the global deployment or for the site that you select.</span></span>
    
    <span data-ttu-id="d73bf-172">Ao habilitar o filtro de arquivo, você pode escolher uma das seguintes opções na **transferência de arquivos**:</span><span class="sxs-lookup"><span data-stu-id="d73bf-172">When you enable the file filter, you can choose one of the following options in **File transfer**:</span></span>
    
      - <span data-ttu-id="d73bf-173">**Bloquear tipos de arquivo específicos**   Você especifica quais solicitações de transferência de arquivo são filtradas pelo servidor especificando uma lista de extensões de arquivo a serem bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="d73bf-173">**Block specific file types**   You specify which file transfer requests are filtered by the server by specifying a list of file extensions to block.</span></span> <span data-ttu-id="d73bf-174">As entradas na lista podem conter todos os caracteres padrão, mas não o caractere curinga ( \* ).</span><span class="sxs-lookup"><span data-stu-id="d73bf-174">Entries in the list can contain all standard characters, but not the wildcard character (\*).</span></span> <span data-ttu-id="d73bf-175">No cliente do Office Live Meeting 2007, o recurso folheto está habilitado, mas qualquer arquivo com essa extensão não pode ser carregado ou baixado.</span><span class="sxs-lookup"><span data-stu-id="d73bf-175">In the Office Live Meeting 2007 client the handout feature is enabled, but any file with this extension cannot be uploaded or downloaded.</span></span> <span data-ttu-id="d73bf-176">Se você marcar a caixa de seleção **Bloquear URLs com extensão de arquivo** nas configurações de um filtro de URL listado na guia **filtro de URL** , o filtro de URL usará essa mesma lista para bloquear hiperlinks ativos que contenham qualquer uma dessas extensões de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d73bf-176">If you select the **Block URLs with file extension** check box on the settings for a URL filter listed on the **URL Filter** tab, the URL filter uses this same list to block active hyperlinks that contain any of these file extensions.</span></span> <span data-ttu-id="d73bf-177">Para escolher quais tipos de arquivo você deseja bloquear, clique em **selecionar** e, em seguida, em **Selecionar tipo de arquivo**, adicione as extensões de tipo de arquivo à lista de extensões de tipo de **arquivo selecionadas** .</span><span class="sxs-lookup"><span data-stu-id="d73bf-177">To choose which file types you want to block, click **Select**, and then, in **Select File Type**, add the file type extensions to the **Selected file type extensions** list.</span></span>
    
      - <span data-ttu-id="d73bf-178">**Bloquear tudo**   O servidor descarta todas as mensagens instantâneas que contêm solicitações de transferência de arquivo e retorna uma mensagem de erro para o remetente da solicitação.</span><span class="sxs-lookup"><span data-stu-id="d73bf-178">**Block All**   The server drops all instant messages that contain file transfer requests and returns an error message to the sender of the request.</span></span> <span data-ttu-id="d73bf-179">O recurso folheto no cliente do Office Live Meeting 2007 está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d73bf-179">The handout feature in the Office Live Meeting 2007 client is disabled.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="d73bf-180">A filtragem de extensões de arquivo limita-se a nomes de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="d73bf-180">Filtering of file extensions is limited to standard file names.</span></span> <span data-ttu-id="d73bf-181">A filtragem pode não funcionar com extensões de arquivo inseridas em outros nomes.</span><span class="sxs-lookup"><span data-stu-id="d73bf-181">Filtering may not work with file extensions embedded in other names.</span></span>



</div>

</div>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d73bf-182">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d73bf-182">In This Section</span></span>

  - [<span data-ttu-id="d73bf-183">Modificar o filtro de transferência de arquivo padrão no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d73bf-183">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)

  - [<span data-ttu-id="d73bf-184">Criar um novo filtro de transferência de arquivo no Lync Server 2013 para um site específico</span><span class="sxs-lookup"><span data-stu-id="d73bf-184">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)

  - [<span data-ttu-id="d73bf-185">Modificar o filtro de URL padrão no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d73bf-185">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)

  - [<span data-ttu-id="d73bf-186">Criar um novo filtro de URL no Lync Server 2013 para manipular hiperlinks em conversas de mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="d73bf-186">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d73bf-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="d73bf-187">See Also</span></span>


[<span data-ttu-id="d73bf-188">Gerenciando configurações de IM e de presença no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d73bf-188">Managing IM and presence settings in Lync Server 2013</span></span>](lync-server-2013-managing-im-and-presence-settings.md)  
  

<span data-ttu-id="d73bf-189"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d73bf-189"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

