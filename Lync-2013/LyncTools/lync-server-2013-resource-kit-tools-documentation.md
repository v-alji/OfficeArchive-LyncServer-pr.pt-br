---
title: Documentação de ferramentas do kit de recursos do Lync Server 2013
description: Documentação de ferramentas do kit de recursos do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Resource Kit Tools Documentation
ms:assetid: b1c341f1-86fa-479d-ba4d-28df5a4c1622
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945604(v=OCS.15)
ms:contentKeyID: 51541429
ms.date: 02/02/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6866e04615014daa7e93f7e7f1081b10325d087d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446642"
---
# <a name="lync-server-2013-resource-kit-tools-documentation"></a><span data-ttu-id="3736e-103">Documentação de ferramentas do kit de recursos do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-103">Lync Server 2013 Resource Kit Tools Documentation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3736e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3736e-104">

<span> </span></span></span>

<span data-ttu-id="3736e-105">_**Tópico da última modificação:** 2014-01-09_</span><span class="sxs-lookup"><span data-stu-id="3736e-105">_**Topic Last Modified:** 2014-01-09_</span></span>

<span data-ttu-id="3736e-106">Este tópico descreve as ferramentas que fazem parte do kit de recursos do Lync Server 2013, incluindo a finalidade de cada ferramenta e exemplos de seu uso. O Lync Server 2013, ferramentas do Resource Kit ajudam a facilitar tarefas de rotina para administradores de ti que implantam e gerenciam o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-106">This topic describes the tools that are part of the Lync Server 2013 Resource Kit, including the purpose of each tool, and examples of its use.The Lync Server 2013, Resource Kit Tools help to make routine tasks easier for IT administrators who deploy and manage Lync Server 2013.</span></span> <span data-ttu-id="3736e-107">Por exemplo, a ferramenta **Web Conf Data** pode ser usada para controlar facilmente os dados carregados pelos usuários durante uma reunião online.</span><span class="sxs-lookup"><span data-stu-id="3736e-107">For example, the **Web Conf Data** tool can be used to easily control data that is uploaded by users during an online meeting.</span></span> <span data-ttu-id="3736e-108">A ferramenta **SEFAUtil** pode ser usada para configurar o encaminhamento e as respostas de chamadas de representantes para os usuários.</span><span class="sxs-lookup"><span data-stu-id="3736e-108">The **SEFAUtil** tool can be used to set up delegate call forwarding and answering for users.</span></span> <span data-ttu-id="3736e-109">Incentivamos os administradores de ti a usar essas ferramentas para gerenciar com mais eficiência o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-109">We encourage IT administrators to use these tools to more effectively manage Lync Server 2013.</span></span>

<div>

## <a name="installation-of-the-resource-kit-tools"></a><span data-ttu-id="3736e-110">Instalação das Ferramentas do Kit de Recursos</span><span class="sxs-lookup"><span data-stu-id="3736e-110">Installation of the Resource Kit Tools</span></span>

<span data-ttu-id="3736e-111">Para instalar o Lync Server 2013, ferramentas do Resource Kit, baixe **OCSReskit.msi**.</span><span class="sxs-lookup"><span data-stu-id="3736e-111">To install the Lync Server 2013, Resource Kit Tools, download **OCSReskit.msi**.</span></span> <span data-ttu-id="3736e-112">Você pode baixar o instalador de ferramentas do kit de recursos a partir do centro de download em [https://go.microsoft.com/fwlink/p/?LinkID=330429](https://go.microsoft.com/fwlink/p/?linkid=330429) .</span><span class="sxs-lookup"><span data-stu-id="3736e-112">You can download the Resource Kit Tools installer from the Download Center at [https://go.microsoft.com/fwlink/p/?LinkID=330429](https://go.microsoft.com/fwlink/p/?linkid=330429).</span></span>

<span data-ttu-id="3736e-113">Execute o **OCSResKit.msi** para fazer uma instalação simples.</span><span class="sxs-lookup"><span data-stu-id="3736e-113">Run **OCSResKit.msi** to do a simple installation.</span></span> <span data-ttu-id="3736e-114">O. msi instala todas as ferramentas no seguinte caminho: **% arquivos de programas% \\ Microsoft Lync Server 2013 \\ reskit**.</span><span class="sxs-lookup"><span data-stu-id="3736e-114">The .msi installs all the tools in the following path: **%Program Files%\\Microsoft Lync Server 2013\\ResKit**.</span></span> <span data-ttu-id="3736e-115">As ferramentas que são executáveis autocontidos ficam nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="3736e-115">Tools that are self-contained executables are in this folder.</span></span> <span data-ttu-id="3736e-116">As ferramentas que também têm arquivos estão em suas próprias subpastas.</span><span class="sxs-lookup"><span data-stu-id="3736e-116">Tools that also have files are in their own subfolders.</span></span>

</div>

<div>

## <a name="supported-environments"></a><span data-ttu-id="3736e-117">Ambientes com suporte</span><span class="sxs-lookup"><span data-stu-id="3736e-117">Supported Environments</span></span>

<span data-ttu-id="3736e-118">Para obter o melhor desempenho, as ferramentas do Lync Server 2013, do Resource Kit devem ser instaladas no mesmo ambiente e com as mesmas especificações necessárias para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-118">For optimal performance, the Lync Server 2013, Resource Kit Tools should be installed in the same environment and with the same specifications that are required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="resource-kit-tools-overview"></a><span data-ttu-id="3736e-119">Visão geral das Ferramentas do Kit de Recursos</span><span class="sxs-lookup"><span data-stu-id="3736e-119">Resource Kit Tools Overview</span></span>

<span data-ttu-id="3736e-120">A lista a seguir descreve as ferramentas fornecidas no kit de recursos do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-120">The following list describes the tools that are provided in the Lync Server 2013 Resource Kit.</span></span> <span data-ttu-id="3736e-121">Uma descrição de cada ferramenta, incluindo os requisitos e o uso do exemplo são abordados na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-121">A description of each tool, including the requirements and example usage is covered in the following section.</span></span>

  - <span data-ttu-id="3736e-122">ABSConfig</span><span class="sxs-lookup"><span data-stu-id="3736e-122">ABSConfig</span></span>

  - <span data-ttu-id="3736e-123">Monitor de Serviço da Política de Largura de Banda</span><span class="sxs-lookup"><span data-stu-id="3736e-123">Bandwidth Policy Service Monitor</span></span>

  - <span data-ttu-id="3736e-124">Analisador de Utilização de Largura de Banda</span><span class="sxs-lookup"><span data-stu-id="3736e-124">Bandwidth Utilization Analyzer</span></span>

  - <span data-ttu-id="3736e-125">Estacionador de Chamadas</span><span class="sxs-lookup"><span data-stu-id="3736e-125">Call Parkometer</span></span>

  - <span data-ttu-id="3736e-126">CleanupStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="3736e-126">CleanupStorageServiceData</span></span>

  - <span data-ttu-id="3736e-127">DBAnalyze</span><span class="sxs-lookup"><span data-stu-id="3736e-127">DBAnalyze</span></span>

  - <span data-ttu-id="3736e-128">ImportStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="3736e-128">ImportStorageServiceData</span></span>

  - <span data-ttu-id="3736e-129">LCSSync</span><span class="sxs-lookup"><span data-stu-id="3736e-129">LCSSync</span></span>

  - <span data-ttu-id="3736e-130">LookupUserConsole</span><span class="sxs-lookup"><span data-stu-id="3736e-130">LookupUserConsole</span></span>

  - <span data-ttu-id="3736e-131">MsTurnPing</span><span class="sxs-lookup"><span data-stu-id="3736e-131">MsTurnPing</span></span>

  - <span data-ttu-id="3736e-132">Visualizador da Configuração de Rede</span><span class="sxs-lookup"><span data-stu-id="3736e-132">Network Configuration Viewer</span></span>

  - <span data-ttu-id="3736e-133">Agente do Grupo de Resposta em Tempo Real</span><span class="sxs-lookup"><span data-stu-id="3736e-133">Response Group Agent Live</span></span>

  - <span data-ttu-id="3736e-134">SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="3736e-134">SEFAUtil</span></span>

  - <span data-ttu-id="3736e-135">SYSPrep.ps1</span><span class="sxs-lookup"><span data-stu-id="3736e-135">SYSPrep.ps1</span></span>

  - <span data-ttu-id="3736e-136">Migração de Comunicados de Número não Atribuído</span><span class="sxs-lookup"><span data-stu-id="3736e-136">Unassigned Number Announcements Migration</span></span>

  - <span data-ttu-id="3736e-137">Web Conf Data</span><span class="sxs-lookup"><span data-stu-id="3736e-137">Web Conf Data</span></span>

</div>

<div>

## <a name="absconfig"></a><span data-ttu-id="3736e-138">ABSConfig</span><span class="sxs-lookup"><span data-stu-id="3736e-138">ABSConfig</span></span>

<span data-ttu-id="3736e-139">A ferramenta de configuração de serviço de catálogo de endereços (ABSConfig) é uma ferramenta administrativa que ajuda administradores a personalizar a configuração de serviço de catálogo de endereços no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-139">The Address Book Service Configuration tool (ABSConfig) is an administrative tool that helps administrators customize Address Book Service configuration in Lync Server 2013.</span></span> <span data-ttu-id="3736e-140">Essa ferramenta também habilita os administradores do Lync Server 2013 a restaurar as configurações de serviço de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="3736e-140">This tool also enables Lync Server 2013 administrators to restore the default Address Book Service settings.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-141">Description</span></span>

<span data-ttu-id="3736e-142">O ABSConfig é um aplicativo gráfico de interface do usuário que permite aos administradores configurar os atributos dos serviços de domínio Active Directory relacionados ao serviço de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="3736e-142">ABSConfig is a graphical user interface application that enables administrators to configure Active Directory Domain Services attributes that are related to Address Book Service.</span></span>

<span data-ttu-id="3736e-143">Veja aqui os principais cenários da ferramenta:</span><span class="sxs-lookup"><span data-stu-id="3736e-143">The primary scenarios for the tool are the following:</span></span>

  - <span data-ttu-id="3736e-144">Para permitir que os administradores mapeiem atributos nos serviços de domínio Active Directory para os atributos do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-144">To enable administrators to map attributes in Active Directory Domain Services to the attributes for Lync Server 2013.</span></span>

  - <span data-ttu-id="3736e-145">Permitir que os administradores especifiquem os atributos do Active Directory Domain Services a serem incluídos ou excluídos dos arquivos do Serviço de Catálogo de Endereços.</span><span class="sxs-lookup"><span data-stu-id="3736e-145">To enable administrators to specify the Active Directory Domain Services attribute to be included or excluded in the Address Book Service files.</span></span>

  - <span data-ttu-id="3736e-146">Permitir que os administradores restaurem as configurações padrão do Serviço de Catálogo de Endereços.</span><span class="sxs-lookup"><span data-stu-id="3736e-146">To enable administrators to restore default Address Book Service settings.</span></span>

<span data-ttu-id="3736e-147">A ferramenta ABSConfig pode ser iniciada usando o arquivo absConfig.exe.</span><span class="sxs-lookup"><span data-stu-id="3736e-147">The ABSConfig tool can be started by using the absConfig.exe file.</span></span> <span data-ttu-id="3736e-148">A ferramenta é aberta na guia **Configurar atributos** . Esta tabela tem opções para mapear atributos dos serviços de domínio Active Directory para os campos de atributo do Lync Server 2013 e especificar quais usuários incluir ou excluir nos arquivos do serviço de catálogo de endereços com base em filtros de atributo específicos.</span><span class="sxs-lookup"><span data-stu-id="3736e-148">The tool opens to the **Configure Attributes** tab. This table has options to map Active Directory Domain Services attributes to the attribute fields for Lync Server 2013 and to specify which users to include or exclude in Address Book Service files based on specific attribute filters.</span></span> <span data-ttu-id="3736e-149">Ela também tem opções para personalizar quais números telefônicos serão incluídos no arquivo do Catálogo de Endereços.</span><span class="sxs-lookup"><span data-stu-id="3736e-149">It also has options to customize which value of the phone number to be included in the Address Book file.</span></span> <span data-ttu-id="3736e-150">A opção **Restaurar Padrões** permite aos administradores restaurar os valores padrão das configurações do Serviço de Catálogo de Endereços.</span><span class="sxs-lookup"><span data-stu-id="3736e-150">The **Restore Defaults** option enables administrators to restore Address Book Service settings to default values.</span></span>

</div>

<div>

## <a name="changes-from-lync-server-2010"></a><span data-ttu-id="3736e-151">Alterações do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="3736e-151">Changes from Lync Server 2010</span></span>

<span data-ttu-id="3736e-152">No Lync Server 2013 ferramenta de configuração do ABS, os atributos (linhas) podem ser removidos desmarcando a caixa de seleção "habilitar" para o atributo.</span><span class="sxs-lookup"><span data-stu-id="3736e-152">In Lync Server 2013 ABS Configuration tool, attributes (rows) may be removed by unchecking the “enable” checkbox for the attribute.</span></span> <span data-ttu-id="3736e-153">Isso tem o mesmo efeito que excluir a linha no Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3736e-153">This has the same effect as deleting the row in Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-154">A caixa de seleção Habilitar está na coluna da extrema direita; Talvez seja necessário rolar para a direita para ver a coluna</span><span class="sxs-lookup"><span data-stu-id="3736e-154">The enable checkbox is in the far right column; you may need to scroll right to see the column</span></span>



</div>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-155">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-155">Output</span></span>

<span data-ttu-id="3736e-156">A ABSConfig armazena a configuração do Serviço de Catálogo de Endereços no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3736e-156">ABSConfig stores the Address Book Service configuration in the database.</span></span>

    Path: %ProgramFiles%\Microsoft Lync Server 2013\Reskit

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-157">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-157">Purpose</span></span>

<span data-ttu-id="3736e-158">O ABSConfig oferece uma maneira rápida e fácil de personalizar o serviço de catálogo de endereços do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-158">ABSConfig provides a quick and easy way to customize Lync Server 2013 Address Book Service.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-159">Requirements</span></span>

<div>

## <a name="computer"></a><span data-ttu-id="3736e-160">Computador</span><span class="sxs-lookup"><span data-stu-id="3736e-160">Computer</span></span>

<span data-ttu-id="3736e-161">O ABSConfig pode ser executado apenas em um computador associado a um domínio que tenha o Lync Server 2013 instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-161">ABSConfig can be run only from a domain-joined computer that has Lync Server 2013 installed.</span></span> <span data-ttu-id="3736e-162">No caso do Lync Server 2013, Enterprise Edition, essa ferramenta pode ser executada em qualquer servidor front-end que tenha o serviço de catálogo de endereços habilitado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="3736e-162">In the case of Lync Server 2013, Enterprise Edition, this tool can be run on any Front End servers that have the Address Book Service enabled during setup.</span></span>

</div>

<div>

## <a name="network"></a><span data-ttu-id="3736e-163">Rede</span><span class="sxs-lookup"><span data-stu-id="3736e-163">Network</span></span>

<span data-ttu-id="3736e-164">O computador deve poder se conectar ao pool de front-ends e ao banco de dados back-end.</span><span class="sxs-lookup"><span data-stu-id="3736e-164">The computer should be able to connect to the Front End pool and back-end database.</span></span>

</div>

<div>

## <a name="software"></a><span data-ttu-id="3736e-165">Software</span><span class="sxs-lookup"><span data-stu-id="3736e-165">Software</span></span>

<span data-ttu-id="3736e-166">Os seguintes componentes de software deverão ser instalados antes de executar a ferramenta ABSConfig:</span><span class="sxs-lookup"><span data-stu-id="3736e-166">The following software components must be installed before running the ABSConfig tool:</span></span>

  - <span data-ttu-id="3736e-167">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-167">Microsoft Lync Server 2013</span></span>

</div>

<div>

## <a name="users"></a><span data-ttu-id="3736e-168">Usuários</span><span class="sxs-lookup"><span data-stu-id="3736e-168">Users</span></span>

<span data-ttu-id="3736e-169">Administradores que têm as permissões necessárias para atualizar a implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-169">Administrators who have the permissions required to update the Lync Server 2013 deployment.</span></span>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-170">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-170">Examples</span></span>

<span data-ttu-id="3736e-p109">A ABSConfig pode ser iniciada digitando **ABSConfig.exe** em um prompt de comando. Abaixo é mostrada a interface do usuário da ferramenta ABSConfig.</span><span class="sxs-lookup"><span data-stu-id="3736e-p109">ABSConfig can be started by typing **ABSConfig.exe** at a command prompt. Shown below is the ABSConfig tool user interface.</span></span>

<span data-ttu-id="3736e-173">![A ferramenta ABSConfig.exe.](images/JJ945604.6fb63a70-7b63-4b8b-b7d1-82fe9aa2028f(OCS.15).jpg "A ferramenta ABSConfig.exe.")</span><span class="sxs-lookup"><span data-stu-id="3736e-173">![The ABSConfig.exe tool.](images/JJ945604.6fb63a70-7b63-4b8b-b7d1-82fe9aa2028f(OCS.15).jpg "The ABSConfig.exe tool.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-174">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-174">Summary</span></span>

<span data-ttu-id="3736e-175">A ferramenta ABSConfig fornece aos administradores uma ferramenta rápida e fácil de usar para personalizar o serviço de catálogo de endereços do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-175">The ABSConfig tool provides administrators a quick and easy to use tool to customize Lync Server 2013 Address Book Service.</span></span>

</div>

</div>

<div>

## <a name="bandwidth-policy-service-monitor"></a><span data-ttu-id="3736e-176">Monitor de Serviços da Política de Largura de Banda</span><span class="sxs-lookup"><span data-stu-id="3736e-176">Bandwidth Policy Service Monitor</span></span>

<span data-ttu-id="3736e-177">A ferramenta Monitor de Serviços da Política de Largura de Banda permite que os administradores visualizem uma lista contendo:</span><span class="sxs-lookup"><span data-stu-id="3736e-177">The Bandwidth Policy Service Monitor tool is intended to allow administrators to view a list of the following:</span></span>

1.  <span data-ttu-id="3736e-178">Todos os serviços de política de largura de banda do Lync Server 2013 configurados (autenticação e núcleo) na topologia</span><span class="sxs-lookup"><span data-stu-id="3736e-178">All the configured Lync Server 2013 Bandwidth Policy services (Authentication and Core) in the topology</span></span>

2.  <span data-ttu-id="3736e-179">As conexões de cada um dos serviços com outros serviços da Política de Largura de Banda e servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="3736e-179">The connections that each service makes to other Bandwidth Policy services and to the Edge servers</span></span>

3.  <span data-ttu-id="3736e-180">Todos os links configurados contidos no documento de configuração de rede e uso de largura de banda em tempo real, conforme relatado por cada um dos serviços da Política de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="3736e-180">All the links that are configured in the Network configuration document and real-time bandwidth usage as reported by each of the Bandwidth Policy services</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-181">Description</span></span>

<span data-ttu-id="3736e-p110">A ferramenta Monitor de Serviços da Política de Largura de Banda é implementada como um aplicativo baseado na GUI. Os administradores iniciam a ferramenta executando PDPMonUI.exe.</span><span class="sxs-lookup"><span data-stu-id="3736e-p110">The Bandwidth Policy Service Monitor tool is implemented as a GUI-based application. Administrators start the tool by running PDPMonUI.exe.</span></span>

<span data-ttu-id="3736e-p111">Quando a ferramenta é iniciada, ela tenta descobrir a lista dos serviços da Política de Largura de Banda na topologia. Após a conclusão da atualização inicial, o painel à esquerda da janela é populada com uma lista de serviços agrupados pelos clusters aos quais pertencem.</span><span class="sxs-lookup"><span data-stu-id="3736e-p111">When the tool starts, it attempts to discover the list of Bandwidth Policy services in the topology. After the initial update is done, the pane to the left of the window is populated with a list of services that are grouped by the clusters that they belong to.</span></span>

<span data-ttu-id="3736e-p112">Quando os administradores selecionam determinado Serviço da Política de Largura de Banda, o painel à direita exibe as informações sobre o serviço. O painel também tem duas guias principais que exibem informações.</span><span class="sxs-lookup"><span data-stu-id="3736e-p112">When administrators select a particular Bandwidth Policy Service, the pane on the right displays the information about that particular service. That pane also has two main tabs that display information.</span></span>

<div>

## <a name="machine-info-tab"></a><span data-ttu-id="3736e-188">Guia Informações do Computador</span><span class="sxs-lookup"><span data-stu-id="3736e-188">Machine Info Tab</span></span>

<span data-ttu-id="3736e-189">A guia **Informações do Computador** mostra os detalhes do Serviço da Política de Largura de Banda selecionado, bem como a lista e o estado de todas as conexões realizadas pelo Serviço da Política de Largura de Banda selecionado com outros serviços.</span><span class="sxs-lookup"><span data-stu-id="3736e-189">The **Machine Info** tab shows the details of the Bandwidth Policy Service that is selected and the list and state of all the connections that are made by the selected Bandwidth Policy Service to other services.</span></span>

</div>

<div>

## <a name="topology-info-tab"></a><span data-ttu-id="3736e-190">Guia Informações da Topologia</span><span class="sxs-lookup"><span data-stu-id="3736e-190">Topology Info Tab</span></span>

<span data-ttu-id="3736e-p113">A guia **Informações da Topologia** mostra uma lista de todos os links definidos nas configurações de rede. É exibida a capacidade de largura de banda de vídeo e áudio de cada link. Além disso, a largura de banda utilizada atualmente também é exibida, em Kbps e em um percentual da capacidade. A ferramenta usa codificação por cores para realçar os links cuja utilização esteja próxima do limite de capacidade, permitindo que os administradores isolem rapidamente esses links.</span><span class="sxs-lookup"><span data-stu-id="3736e-p113">The **Topology Info** tab shows a list of all the links that are configured in the Network configuration settings. For each link, the audio and video bandwidth capacity is displayed. Additionally, the currently utilized bandwidth is displayed, both in Kbps and as a percentage of the capacity. The tool uses color-coding to highlight links that have utilization that is close to the capacity—this allows administrators to quickly isolate such links.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-p114"> Se houver uma falha no Monitor de Serviços da Política de Largura de Banda ao se conectar a qualquer um dos serviços da Política de Largura de Banda configurados, as informações nas guias <STRONG>Informações do Computador</STRONG> e <STRONG>Informações da Topologia</STRONG> não serão populadas. No entanto, é possível que a ferramenta se conecte inicialmente, mas depois perca a conexão com o serviço. Nesses casos, os administradores poderão ver informações desatualizadas. Há um carimbo de data/hora <STRONG>Última Atualização</STRONG> em cada uma das guias que permite aos administradores ver quando os dados foram atualizados pela última vez para um determinado Serviço da Política de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="3736e-p114">If the Bandwidth Policy Service Monitor tool experiences failure when it connects to any of the configured Bandwidth Policy services, the information in the <STRONG>Machine Info</STRONG> and the <STRONG>Topology Info</STRONG> tabs won’t be populated. However, it is possible that the tool might connect initially but subsequently lose its connection to the service. In such cases, administrators might see outdated information. There is a <STRONG>Last Updated</STRONG> time stamp on each of the tabs that can allow administrators to see when the data was last updated for a particular Bandwidth Policy Service.</span></span>



</div>

</div>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-199">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-199">Output</span></span>

<span data-ttu-id="3736e-200">Não há nenhum resultado na linha de comando; o resultado do programa está contido dentro da GUI (interface gráfica do usuário) principal.</span><span class="sxs-lookup"><span data-stu-id="3736e-200">There is no command-line output; the program output is contained within the main graphical user interface (GUI).</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-201">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-201">Purpose</span></span>

<span data-ttu-id="3736e-p115">O objetivo da ferramenta Monitor de Serviços da Política de Largura de Banda é proporcionar aos administradores visibilidade do estado de cada um dos serviços da Política de Largura de Banda definidos na topologia. Além disso, os administradores podem ver o uso da largura de banda em tempo real de todos os links definidos no documento de configuração da rede.</span><span class="sxs-lookup"><span data-stu-id="3736e-p115">The purpose of the Bandwidth Policy Service Monitor tool is to allow administrators visibility into the state of each of the Bandwidth Policy services that are defined in the topology. In addition, administrators can see real-time bandwidth usage for all the links that are defined in the Network configuration document.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-204">Requirements</span></span>

<span data-ttu-id="3736e-205">A ferramenta de monitoração do serviço de política de largura de banda precisa ser executada em um computador que faça parte da topologia do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3736e-205">The Bandwidth Policy Service Monitor tool needs to be run on a computer that is part of the Lync Server topology.</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-206">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-206">Summary</span></span>

<span data-ttu-id="3736e-207">A ferramenta Monitor de Serviços da Política de Largura de Banda pode ser um recurso valioso para os administradores, pois com ela é possível inspecionar na topologia o estado de todos os serviços da Política de Largura de Banda e, o mais importante, obter a utilização da largura de banda em tempo real dos links definidos nas configurações da rede.</span><span class="sxs-lookup"><span data-stu-id="3736e-207">The Bandwidth Policy Service Monitor tool can be a valuable resource to administrators so they can inspect the state of all the Bandwidth Policy services in the topology—and more importantly—they can obtain real-time bandwidth utilization for the links that are defined in the Network configuration settings.</span></span>

</div>

</div>

<div>

## <a name="bandwidth-utilization-analyzer"></a><span data-ttu-id="3736e-208">Analisador de Utilização da Largura de Banda</span><span class="sxs-lookup"><span data-stu-id="3736e-208">Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="3736e-p116">O Analisador de Utilização da Largura de Banda é uma ferramenta que cria relatórios sobre diversas exibições do consumo de largura de banda pelos pontos de extremidade de UC nos links WAN da rede corporativa. Esses relatórios podem ser usados para entender o padrão de consumo de largura de banda atual e auxiliar no planejamento de capacidade de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="3736e-p116">Bandwidth Utilization Analyzer is a tool that creates reports about various views of bandwidth consumption by the UC endpoints across WAN links in the enterprise network. These reports can be used to understand the current bandwidth consumption pattern and to aid in bandwidth capacity planning.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-211">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-211">Description</span></span>

<span data-ttu-id="3736e-p117">O Analisador de Utilização da Largura de Banda é implementado como um aplicativo baseado na GUI. Essa ferramenta gera relatórios específicos para utilização de áudio na rede e ajuda no planejamento da capacidade. Também itera na capacidade de largura de banda atribuída a diversos links.</span><span class="sxs-lookup"><span data-stu-id="3736e-p117">Bandwidth Utilization Analyzer is implemented as a GUI-based application. This tool generates reports specifically for audio utilization across the network and helps with capacity planning. It also iterates on the bandwidth capacity that is assigned to various links.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-215">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-215">Output</span></span>

<span data-ttu-id="3736e-216">O Analisador de Utilização da Largura de Banda fornece plotagens gráficas da utilização e da capacidade de largura da banda de áudio de todos os links WAN configurados no sistema.</span><span class="sxs-lookup"><span data-stu-id="3736e-216">Bandwidth Utilization Analyzer provides graphic al plots of bandwidth capacity and utilization for audio for all the WAN links that are configured in the system.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-217">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-217">Purpose</span></span>

<span data-ttu-id="3736e-p118">Em qualquer implantação de vídeo e voz, é fundamental monitorar e entender a tendência da utilização da largura de banda do tráfego de mídia na rede corporativa. A ferramenta Analisador de Utilização da Largura de Banda permite ao administrador realizar justamente isso. Essa ferramenta faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3736e-p118">In any voice and video deployment, it’s critical to monitor and understand the trend of bandwidth utilization of media traffic across the enterprise network. The Bandwidth Utilization Analyzer tool allows an administrator to achieve just that. This tool does the following:</span></span>

  - <span data-ttu-id="3736e-221">Gera relatórios específicos de utilização de áudio na rede.</span><span class="sxs-lookup"><span data-stu-id="3736e-221">Generates specific reports for audio utilization across the network</span></span>

  - <span data-ttu-id="3736e-222">Ajuda com um planejamento de capacidade mais eficaz e com a iteração na capacidade de largura de banda atribuída a vários links.</span><span class="sxs-lookup"><span data-stu-id="3736e-222">Helps with more effective capacity planning and iteration on the bandwidth capacity that is assigned to various links</span></span>

<span data-ttu-id="3736e-223">O Analisador de Utilização da Largura de Banda gera plotagens gráficas dos relatórios de utilização e capacidade de largura de banda; são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="3736e-223">Bandwidth Utilization Analyzer can generate graphical plots of bandwidth capacity and utilization reports; they are as follows:</span></span>

  - <span data-ttu-id="3736e-224">Todos os links WAN na rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="3736e-224">All the WAN links in the enterprise network</span></span>

  - <span data-ttu-id="3736e-225">Filtradas pelos links WAN selecionados que foram escolhidos.</span><span class="sxs-lookup"><span data-stu-id="3736e-225">Filtered by selected WAN links that have been chosen</span></span>

  - <span data-ttu-id="3736e-226">Filtradas pelos links WAN que excederam o limite de capacidade.</span><span class="sxs-lookup"><span data-stu-id="3736e-226">Filtered by WAN links that have exceeded link capacity</span></span>

  - <span data-ttu-id="3736e-227">Filtradas pelos links WAN que têm subutilizado a largura de banda provisionada.</span><span class="sxs-lookup"><span data-stu-id="3736e-227">Filtered by WAN links that have been under-utilizing the provisioned bandwidth</span></span>

  - <span data-ttu-id="3736e-228">Filtradas pelos links WAN que alcançaram níveis críticos (uma utilização de largura de banda superior a 90% da capacidade de largura de banda do link WAN).</span><span class="sxs-lookup"><span data-stu-id="3736e-228">Filter by WAN links that have been reaching critical levels (a bandwidth utilization that is greater than 90% of bandwidth capacity of the WAN link)</span></span>

  - <span data-ttu-id="3736e-229">Filtradas pelo tipo de link WAN : links rede-site, links inter-regionais e links dentro de um site.</span><span class="sxs-lookup"><span data-stu-id="3736e-229">Filtered by WAN link type—network-site links, interregional links, and links within a site</span></span>

  - <span data-ttu-id="3736e-230">Filtradas por região de rede.</span><span class="sxs-lookup"><span data-stu-id="3736e-230">Filtered by network region</span></span>

<div>

## <a name="applications"></a><span data-ttu-id="3736e-231">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="3736e-231">Applications</span></span>

<span data-ttu-id="3736e-232">O Analisador de Utilização da Largura de Banda tem os dois aplicativos (ferramentas) abaixo:</span><span class="sxs-lookup"><span data-stu-id="3736e-232">Bandwidth Utilization Analyzer has the following two applications (tools):</span></span>

  - <span data-ttu-id="3736e-233">**WanLinkLogCollector.exe** Esta ferramenta permite ao usuário inserir as informações necessárias. </span><span class="sxs-lookup"><span data-stu-id="3736e-233">**WanLinkLogCollector.exe**   This tool enables its user to input the required information.</span></span>

  - <span data-ttu-id="3736e-234">**BandwidthUtilizationAnalyzer.xlsm**  Um relatório de software de planilha do Microsoft Excel é iniciado automaticamente pelo WanLinkLogCollector.exe.</span><span class="sxs-lookup"><span data-stu-id="3736e-234">**BandwidthUtilizationAnalyzer.xlsm**  A Microsoft Excel spreadsheet software report is automatically launched by WanLinkLogCollector.exe.</span></span> <span data-ttu-id="3736e-235">Este aplicativo permite ao usuário aplicar filtros ao relatório, como será mostrado posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="3736e-235">This application allows the user to apply filters to the report as shown later in this article.</span></span>

</div>

<div>

## <a name="phases-of-using-bandwidth-utilization-analyzer"></a><span data-ttu-id="3736e-236">Fases de uso do Analisador de Utilização da Largura de Banda</span><span class="sxs-lookup"><span data-stu-id="3736e-236">Phases of Using Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="3736e-237">Há duas fases ao usar o Analisador de Utilização da Largura de Banda:</span><span class="sxs-lookup"><span data-stu-id="3736e-237">There are two phases when using Bandwidth Utilization Analyzer:</span></span>

  - <span data-ttu-id="3736e-238">Coletar logs, o que é realizado ao usar o WanLinkLogCollector.exe.</span><span class="sxs-lookup"><span data-stu-id="3736e-238">Collect logs, which is performed by using WanLinkLogCollector.exe</span></span>

  - <span data-ttu-id="3736e-239">Personalizar relatórios, o que é realizado ao usar o BandwidthUtilizationAnalyzer.xlsm.</span><span class="sxs-lookup"><span data-stu-id="3736e-239">Customize reports, which is performed by using BandwidthUtilizationAnalyzer.xlsm</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3736e-240">Recomendamos que o BandwidthUtilizationAnalyzer.xlsm não seja iniciado manualmente pelos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="3736e-240">We strongly recommend that BandwidthUtilizationAnalyzer.xlsm not be manually launched by end users.</span></span>



</div>

</div>

<div>

## <a name="starting-bandwidth-utilization-analyzer"></a><span data-ttu-id="3736e-241">Iniciando o Analisador de Utilização da Largura de Banda</span><span class="sxs-lookup"><span data-stu-id="3736e-241">Starting Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="3736e-242">Inicie o WanLinkLogCollector.exe no prompt de comando ou no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="3736e-242">Start WanLinkLogCollector.exe at the command prompt or by using Windows Explorer.</span></span>

<span data-ttu-id="3736e-243">**Usando o WanLinkLogCollector.exe**</span><span class="sxs-lookup"><span data-stu-id="3736e-243">**Using WanLinkLogCollector.exe**</span></span>

<span data-ttu-id="3736e-244">Há três etapas para usar o WanLinkLogCollector.exe:</span><span class="sxs-lookup"><span data-stu-id="3736e-244">There are three steps to using WanLinkLogCollector.exe:</span></span>

1.  <span data-ttu-id="3736e-245">**Registrar a linha do tempo** Forneça a linha do tempo para a qual o relatório precisa ser gerado.</span><span class="sxs-lookup"><span data-stu-id="3736e-245">**Log the timeline**   Provide the timeline that the report needs to be generated for</span></span>

2.  <span data-ttu-id="3736e-246">**Especificar os diretórios do arquivo** Forneça as informações de localização do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3736e-246">**Specify the file directories**   Provide file location information</span></span>

3.  <span data-ttu-id="3736e-247">**Coletar os logs e iniciar o Visualizador de relatórios**  Executar o comando para gerar o relatório</span><span class="sxs-lookup"><span data-stu-id="3736e-247">**Collect the logs and launch the report viewer**  Execute the command to generate the report</span></span>

<div>

## <a name="step-1---log-the-timeline"></a><span data-ttu-id="3736e-248">Etapa 1 – Registrar a linha do tempo</span><span class="sxs-lookup"><span data-stu-id="3736e-248">Step 1 - Log the timeline</span></span>

<span data-ttu-id="3736e-249">O registro da linha do tempo permite que o usuário da ferramenta especifique o seguinte, conforme mostra a figura abaixo: </span><span class="sxs-lookup"><span data-stu-id="3736e-249">Logging the timeline allows the tool user to specify the following as shown in the figure below.</span></span>

1.  <span data-ttu-id="3736e-250">**Data de início** Trata-se da data de início da linha do tempo para a qual o relatório deve ser gerado; por exemplo, 1º de agosto de 2010.</span><span class="sxs-lookup"><span data-stu-id="3736e-250">**Start date** This is the start date of the timeline that the report is to be generated for; for example, August 1, 2010.</span></span>

2.  <span data-ttu-id="3736e-251">**Data de término** Trata-se da data de término da linha do tempo para a qual o relatório deve ser gerado; por exemplo, 30 de setembro de 2010.</span><span class="sxs-lookup"><span data-stu-id="3736e-251">**End date** This is the end date of the timeline that the report is to be generated for; for example, September 30, 2010.</span></span>
    
    <span data-ttu-id="3736e-252">![Datas de início e término na utilização da largura de banda A](images/JJ945604.2c597cfc-3372-4d41-816b-26202f607ad8(OCS.15).jpg "Datas de início e término na utilização da largura de banda A")</span><span class="sxs-lookup"><span data-stu-id="3736e-252">![Start and End dates in the Bandwidth Utilization A](images/JJ945604.2c597cfc-3372-4d41-816b-26202f607ad8(OCS.15).jpg "Start and End dates in the Bandwidth Utilization A")</span></span>  

</div>

<div>

## <a name="step-2---specify-the-file-directories"></a><span data-ttu-id="3736e-253">Etapa 2 – Especificar os diretórios do arquivo</span><span class="sxs-lookup"><span data-stu-id="3736e-253">Step 2 - Specify the file directories</span></span>

<span data-ttu-id="3736e-254">Os seguintes diretórios de arquivo devem ser especificados pelo usuário, como a seguir:</span><span class="sxs-lookup"><span data-stu-id="3736e-254">The following file directories can be specified by the user as shown.</span></span>

  - <span data-ttu-id="3736e-255">**Local dos arquivos de log do servidor** O local da pasta onde os logs do servidor de política de largura de banda são armazenados.</span><span class="sxs-lookup"><span data-stu-id="3736e-255">**Server log files location** The folder location where Bandwidth policy server logs are stored.</span></span> <span data-ttu-id="3736e-256">Isso geralmente é no \<fileserver\> \\ \<choice of FE\> \\ \\ PDP AppServerFiles.</span><span class="sxs-lookup"><span data-stu-id="3736e-256">This is typically in \<fileserver\>\\\<choice of FE\>\\AppServerFiles\\PDP.</span></span>

  - <span data-ttu-id="3736e-257">**Local de armazenamento de arquivo temporário** O local do arquivo temporário onde os arquivos intermediários são armazenados enquanto o relatório está sendo gerado.</span><span class="sxs-lookup"><span data-stu-id="3736e-257">**Temporary file storage location** The temporary file location where intermediate files are stored while the report is being generated.</span></span>

<span data-ttu-id="3736e-258">![Diretórios de arquivos no anal de utilização da largura de banda](images/JJ945604.d66daeac-1669-45e3-932d-3f6782840c2a(OCS.15).jpg "Diretórios de arquivos no anal de utilização da largura de banda")</span><span class="sxs-lookup"><span data-stu-id="3736e-258">![File directories in the Bandwidth Utilization Anal](images/JJ945604.d66daeac-1669-45e3-932d-3f6782840c2a(OCS.15).jpg "File directories in the Bandwidth Utilization Anal")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-259">Forneça ao usuário da ferramenta acesso suficiente aos arquivos de logs do servidor e à pasta de repositório de arquivos temporários.</span><span class="sxs-lookup"><span data-stu-id="3736e-259">Ensure that sufficient file access to the server logs and the temporary file store folder is provided to the tool user.</span></span>



</div>

</div>

<div>

## <a name="step-3---collect-the-logs-and-start-the-report-viewer"></a><span data-ttu-id="3736e-260">Etapa 3 – Coletar os logs e iniciar o visualizador de relatórios</span><span class="sxs-lookup"><span data-stu-id="3736e-260">Step 3 - Collect the logs and start the report viewer</span></span>

<span data-ttu-id="3736e-p121">Para coletar os logs e iniciar o visualizador de relatórios, clique em **Executar**, como mostrado abaixo. Esta etapa coleta os dados necessários.</span><span class="sxs-lookup"><span data-stu-id="3736e-p121">To collect the logs and start the report viewer, click **Execute** as shown below. This step collects the required data.</span></span>

<span data-ttu-id="3736e-263">![Coletando dados na Analy de utilização da largura de banda](images/JJ945604.0019cb2c-7c01-4dc9-ac90-ac47c47d1bfd(OCS.15).jpg "Coletando dados na Analy de utilização da largura de banda")</span><span class="sxs-lookup"><span data-stu-id="3736e-263">![Collecting data in the Bandwidth Utilization Analy](images/JJ945604.0019cb2c-7c01-4dc9-ac90-ac47c47d1bfd(OCS.15).jpg "Collecting data in the Bandwidth Utilization Analy")</span></span>

<span data-ttu-id="3736e-264">Se a validação da entrada for bem-sucedida, a mensagem abaixo será exibida.</span><span class="sxs-lookup"><span data-stu-id="3736e-264">When the input validation is successful, the message shown below is displayed.</span></span>

<span data-ttu-id="3736e-265">![Registra a notificação coletada no utilitário de largura de banda](images/JJ945604.eda91da8-3285-4eab-8ccb-c6d89c8cc221(OCS.15).jpg "Registra a notificação coletada no utilitário de largura de banda")</span><span class="sxs-lookup"><span data-stu-id="3736e-265">![Logs collected notification in the Bandwidth Utili](images/JJ945604.eda91da8-3285-4eab-8ccb-c6d89c8cc221(OCS.15).jpg "Logs collected notification in the Bandwidth Utili")</span></span>

<span data-ttu-id="3736e-p122">Clique em **OK**. BandwidthUtilizationAnalyzer.xlsm será iniciado automaticamente. Siga as instrução na caixa de mensagens. Para obter mais detalhes, consulte **Uso do BandwidthUtilizationAnalyzer.xlsm** na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="3736e-p122">Click **OK**. BandwidthUtilizationAnalyzer.xlsm is automatically started. Follow the instructions in the message box. For details, see **Using BandwidthUtilizationAnalyzer.xlsm** in the next section.</span></span>

</div>

<div>


<span data-ttu-id="3736e-270">**Uso do BandwidthUtilizationAnalyzer.xlsm**</span><span class="sxs-lookup"><span data-stu-id="3736e-270">**Using BandwidthUtilizationAnalyzer.xlsm**</span></span>

1.  <span data-ttu-id="3736e-271">Se o BandwidthUtilizationAnalyzer.xlsm tiver sido iniciado automaticamente, clique em **Atualizar**, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-271">When BandwidthUtilizationAnalyzer.xlsm is automatically started, click **Refresh** as shown below.</span></span>
    
    <span data-ttu-id="3736e-272">![BandwidthUtilizationAnalyzer.xlsm](images/JJ945604.c4e675b9-1671-400e-a712-6db82d731b39(OCS.15).jpg "BandwidthUtilizationAnalyzer.xlsm")</span><span class="sxs-lookup"><span data-stu-id="3736e-272">![BandwidthUtilizationAnalyzer.xlsm](images/JJ945604.c4e675b9-1671-400e-a712-6db82d731b39(OCS.15).jpg "BandwidthUtilizationAnalyzer.xlsm")</span></span>

2.  <span data-ttu-id="3736e-273">Quando uma pasta de arquivos for aberta, selecione consolidated.csv na localização especificada na caixa de mensagens, como a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-273">When a file folder is opened, select consolidated.csv from the location that is specified in the message box as shown below.</span></span> <span data-ttu-id="3736e-274">Ele também mostra o local como **C: \\ Temp**.</span><span class="sxs-lookup"><span data-stu-id="3736e-274">It also shows the location as **C:\\Temp**.</span></span>
    
    <span data-ttu-id="3736e-275">![Abrir uma pasta no BandwidthUtilizationAnalyzer.](images/JJ945604.601cc572-cee9-45fb-9ed1-c4b96a2fa21e(OCS.15).jpg "Abrir uma pasta no BandwidthUtilizationAnalyzer.")</span><span class="sxs-lookup"><span data-stu-id="3736e-275">![Opening a folder in BandwidthUtilizationAnalyzer.](images/JJ945604.601cc572-cee9-45fb-9ed1-c4b96a2fa21e(OCS.15).jpg "Opening a folder in BandwidthUtilizationAnalyzer.")</span></span>

3.  <span data-ttu-id="3736e-276">Clique em **Importar**.</span><span class="sxs-lookup"><span data-stu-id="3736e-276">Click **Import**.</span></span>

4.  <span data-ttu-id="3736e-p124">A plotagem gráfica é gerada automaticamente. Ela será disponibilizada assim que o ponteiro de trabalho em segundo plano desaparecer.</span><span class="sxs-lookup"><span data-stu-id="3736e-p124">The graphical plot is automatically generated. It is available when the working-in-the-background pointer disappears.</span></span>
    
    <span data-ttu-id="3736e-279">![Aplicação de filtros no modo de exibição relatório.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Aplicação de filtros no modo de exibição relatório.")</span><span class="sxs-lookup"><span data-stu-id="3736e-279">![Applying filters in Report View.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Applying filters in Report View.")</span></span>

</div>

<div>

## <a name="applying-filters-to-the-report-view"></a><span data-ttu-id="3736e-280">Aplicando filtros ao visualizador de relatórios</span><span class="sxs-lookup"><span data-stu-id="3736e-280">Applying Filters to the Report View</span></span>

<span data-ttu-id="3736e-281">Os filtros que podem ser aplicados ao visualizador de relatórios, conforme mostrado abaixo, são descritos da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="3736e-281">The filters that can be applied to the report view as shown below are described as follows:</span></span>

<span data-ttu-id="3736e-282">![Aplicação de filtros no modo de exibição relatório.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Aplicação de filtros no modo de exibição relatório.")</span><span class="sxs-lookup"><span data-stu-id="3736e-282">![Applying filters in Report View.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Applying filters in Report View.")</span></span>

1.  <span data-ttu-id="3736e-283">**Nome** Filtrar por links WAN (o filtro se situa no lado direito do gráfico). O prefixo denota os tipos de links a seguir; consulte a caixa (azul) vertical:</span><span class="sxs-lookup"><span data-stu-id="3736e-283">**Name** Filter by WAN links (the filter is on the right side of the graph).The prefix denotes the following link types; see the vertical (blue) box:</span></span>
    
      - <span data-ttu-id="3736e-284">**S Site** O link WAN de um site da rede a uma região da rede</span><span class="sxs-lookup"><span data-stu-id="3736e-284">**S Site** The WAN link from a network site to a network region</span></span>
    
      - <span data-ttu-id="3736e-285">**IS Entre sites** O link WAN entre dois sites da rede</span><span class="sxs-lookup"><span data-stu-id="3736e-285">**IS Inter-Site** The WAN link between two network sites</span></span>
    
      - <span data-ttu-id="3736e-286">**R Inter-regional** O link WAN entre duas regiões da rede</span><span class="sxs-lookup"><span data-stu-id="3736e-286">**R Inter-Region** The WAN link between two network region</span></span>

2.  <span data-ttu-id="3736e-287">**Limite excedido** Filtrar por links WAN cuja utilização de largura de banda seja superior à capacidade da largura de banda</span><span class="sxs-lookup"><span data-stu-id="3736e-287">**Exceeded limit** Filter by WAN links whose bandwidth utilization is more than the bandwidth capacity</span></span>

3.  <span data-ttu-id="3736e-288">**Níveis críticos** Filtrar por links WAN cuja utilização da largura de banda tenha alcançado 90% ou mais da capacidade da largura de banda</span><span class="sxs-lookup"><span data-stu-id="3736e-288">**Critical levels** Filter by WAN links whose bandwidth utilization has reached 90% or more than the bandwidth capacity</span></span>

4.  <span data-ttu-id="3736e-289">**Subutilizado** Filtrar por links WAN cuja utilização da largura de banda seja inferior a 25% da capacidade da largura de banda</span><span class="sxs-lookup"><span data-stu-id="3736e-289">**Under-utilized** Filter by WAN links whose bandwidth utilization has been less than 25% of the bandwidth capacity</span></span>

5.  <span data-ttu-id="3736e-290">**Tipo de link** Filtrar pelos seguintes tipos de links WAN:</span><span class="sxs-lookup"><span data-stu-id="3736e-290">**Link type** Filter by the following WAN links types:</span></span>
    
      - <span data-ttu-id="3736e-291">
            Tipo **Site da rede**</span><span class="sxs-lookup"><span data-stu-id="3736e-291">**Network site** type</span></span>
    
      - <span data-ttu-id="3736e-292">
            Tipo **Entre sites**</span><span class="sxs-lookup"><span data-stu-id="3736e-292">**Inter-site** type</span></span>
    
      - <span data-ttu-id="3736e-293">
            Tipo \*\*Link inter-regional**</span><span class="sxs-lookup"><span data-stu-id="3736e-293">**Inter-Region link** type</span></span>

6.  <span data-ttu-id="3736e-294">**Região** Filtrar pela região da rede</span><span class="sxs-lookup"><span data-stu-id="3736e-294">**Region** Filter by network region</span></span>

<span data-ttu-id="3736e-295">As imagens abaixo mostram os filtros descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3736e-295">The following figures show the previously described filters.</span></span>

<span data-ttu-id="3736e-p125">Filtrar por **Nome**. Selecione a lista de links que precisam ser exibidos no gráfico.</span><span class="sxs-lookup"><span data-stu-id="3736e-p125">Filter by **Name**. Select the list of links that need to be displayed in the graph.</span></span>

<span data-ttu-id="3736e-298">![Filtragem por nome no BandwidthUtilizationAnalyzer.](images/JJ945604.002b7c8e-f0da-48ce-9e1a-5c34d2cab063(OCS.15).jpg "Filtragem por nome no BandwidthUtilizationAnalyzer.")</span><span class="sxs-lookup"><span data-stu-id="3736e-298">![Filtering by Name in BandwidthUtilizationAnalyzer.](images/JJ945604.002b7c8e-f0da-48ce-9e1a-5c34d2cab063(OCS.15).jpg "Filtering by Name in BandwidthUtilizationAnalyzer.")</span></span>

<span data-ttu-id="3736e-299">Filtrar por **Limite excedido**.</span><span class="sxs-lookup"><span data-stu-id="3736e-299">Filter by **Exceeded limit**.</span></span> <span data-ttu-id="3736e-300">Selecione **True** para impor o filtro.</span><span class="sxs-lookup"><span data-stu-id="3736e-300">Select **True** to enforce the filter.</span></span>

<span data-ttu-id="3736e-301">![A filtragem excedeu o limite.](images/JJ945604.5946c95e-76ce-46ca-8f3e-a79be1e5c527(OCS.15).jpg "A filtragem excedeu o limite.")</span><span class="sxs-lookup"><span data-stu-id="3736e-301">![Filtering by Exceeded Limit.](images/JJ945604.5946c95e-76ce-46ca-8f3e-a79be1e5c527(OCS.15).jpg "Filtering by Exceeded Limit.")</span></span>

<span data-ttu-id="3736e-302">Filtrar por **Níveis críticos**.</span><span class="sxs-lookup"><span data-stu-id="3736e-302">Filter by **Critical levels**.</span></span> <span data-ttu-id="3736e-303">Selecione **True** para impor o filtro.</span><span class="sxs-lookup"><span data-stu-id="3736e-303">Select **True** to enforce the filter.</span></span>

<span data-ttu-id="3736e-304">![Filtragem por níveis críticos.](images/JJ945604.60771a52-d8ba-4cb9-a02d-d6c888cb5505(OCS.15).jpg "Filtragem por níveis críticos.")</span><span class="sxs-lookup"><span data-stu-id="3736e-304">![Filtering by Critical Levels.](images/JJ945604.60771a52-d8ba-4cb9-a02d-d6c888cb5505(OCS.15).jpg "Filtering by Critical Levels.")</span></span>

<span data-ttu-id="3736e-305">Filtrar por **Subutilizado**.</span><span class="sxs-lookup"><span data-stu-id="3736e-305">Filter by **Under utilized**.</span></span> <span data-ttu-id="3736e-306">Selecione **True** para impor o filtro.</span><span class="sxs-lookup"><span data-stu-id="3736e-306">Select **True** to enforce the filter.</span></span>

<span data-ttu-id="3736e-307">![Filtragem por subutilizado.](images/JJ945604.95a2bf01-5aba-4927-af47-1ad3c459d791(OCS.15).jpg "Filtragem por subutilizado.")</span><span class="sxs-lookup"><span data-stu-id="3736e-307">![Filtering by Under Utilized.](images/JJ945604.95a2bf01-5aba-4927-af47-1ad3c459d791(OCS.15).jpg "Filtering by Under Utilized.")</span></span>

<span data-ttu-id="3736e-308">Filtrar por **Tipo de Link**.</span><span class="sxs-lookup"><span data-stu-id="3736e-308">Filter by **Link Type**.</span></span> <span data-ttu-id="3736e-309">Selecione um ou mais tipos que precisam ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="3736e-309">Select the type or types that need to be displayed.</span></span>

<span data-ttu-id="3736e-310">![Filtragem por tipo de link.](images/JJ945604.08757949-06bd-4cf3-809f-d81fd23a6639(OCS.15).jpg "Filtragem por tipo de link.")</span><span class="sxs-lookup"><span data-stu-id="3736e-310">![Filtering by Link Type.](images/JJ945604.08757949-06bd-4cf3-809f-d81fd23a6639(OCS.15).jpg "Filtering by Link Type.")</span></span>

<span data-ttu-id="3736e-311">Filtrar por **Região**.</span><span class="sxs-lookup"><span data-stu-id="3736e-311">Filter by **Region**.</span></span> <span data-ttu-id="3736e-312">Selecione uma lista de regiões cujos links precisam ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="3736e-312">Select a list of regions whose links need to be displayed.</span></span>

<span data-ttu-id="3736e-313">![Filtragem por região.](images/JJ945604.5de4cec4-6c09-48bb-98c7-b56f7bdb3d5a(OCS.15).jpg "Filtragem por região.")</span><span class="sxs-lookup"><span data-stu-id="3736e-313">![Filtering by Region.](images/JJ945604.5de4cec4-6c09-48bb-98c7-b56f7bdb3d5a(OCS.15).jpg "Filtering by Region.")</span></span>

</div>

</div>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-314">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-314">Requirements</span></span>

  - <span data-ttu-id="3736e-315">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="3736e-315">The .NET Framework 3.5</span></span>

  - <span data-ttu-id="3736e-316">Microsoft Excel 2010 ou Excel 2007</span><span class="sxs-lookup"><span data-stu-id="3736e-316">Microsoft Excel 2010 or Excel 2007</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-317">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-317">Summary</span></span>

<span data-ttu-id="3736e-p131">O Analisador de Utilização da Largura de Banda é usado para plotar a utilização da largura de banda de áudio do tráfego de UC na rede. Esta ferramenta pode ser usada também para relatar a utilização da largura de banda de vídeo na rede.</span><span class="sxs-lookup"><span data-stu-id="3736e-p131">Bandwidth Utilization Analyzer is used to plot the audio bandwidth utilization for UC traffic across the network. This tool can be used to report the utilization of video bandwidth on the network as well.</span></span>

</div>

</div>

<div>

## <a name="call-parkometer"></a><span data-ttu-id="3736e-320">Parquímetro de Chamada</span><span class="sxs-lookup"><span data-stu-id="3736e-320">Call Parkometer</span></span>

<span data-ttu-id="3736e-321">O Parquímetro de Chamada é um aplicativo de linha de comando que proporciona fácil acesso ao banco de dados da Órbita do Call Park.</span><span class="sxs-lookup"><span data-stu-id="3736e-321">Call Parkometer is a command-line application that provides easy access to the Call Park orbit database.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-322">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-322">Description</span></span>

<span data-ttu-id="3736e-323">O Parquímetro de Chamada é uma ferramenta que rastreia as chamadas estacionadas atualmente.</span><span class="sxs-lookup"><span data-stu-id="3736e-323">Call Parkometer is a tool to track currently parked calls.</span></span> <span data-ttu-id="3736e-324">Ele também coleta estatísticas sobre as órbitas e o uso do CPS (Servidor de Estacionamento de Chamada).</span><span class="sxs-lookup"><span data-stu-id="3736e-324">It also collects statistics about orbits and Call Park Server (CPS) usage.</span></span> <span data-ttu-id="3736e-325">Essa ferramenta de linha de comando fornece acesso de leitura e gravação ao banco de dados do SQL Server do CPS órbita a partir de um computador local ou remotamente conectado.</span><span class="sxs-lookup"><span data-stu-id="3736e-325">This command-line tool provides both read and write-access to the CPS orbit SQL Server database from a local or remotely connected computer.</span></span>

<span data-ttu-id="3736e-p133">Todas as opções são mutuamente exclusivas. A sintaxe da linha de comando é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="3736e-p133">All options are mutually exclusive. Command-line syntax is as follows:</span></span>

  - <span data-ttu-id="3736e-328">
            Parâmetro \*\*–o\*\* – lista todos os intervalos de órbitas configurados para este pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-328">**–o** parameter—lists all orbit ranges configured for this pool.</span></span>

  - <span data-ttu-id="3736e-p134">
            Parâmetro \*\*–n\*\* – lista todas as órbitas usadas atualmente neste pool. As informações são exibidas da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="3736e-p134">**–n** parameter—lists all currently used orbits in this pool. The information displayed is as follows:</span></span>
    
      - <span data-ttu-id="3736e-331">URI (Uniform Resource Identifier) do SIP da chamada estacionada e do estacionador.</span><span class="sxs-lookup"><span data-stu-id="3736e-331">SIP Uniform Resource Identifier (URI) of the parkee and parker.</span></span>
    
      - <span data-ttu-id="3736e-332">Nome do host do CPS onde a chamada está estacionada.</span><span class="sxs-lookup"><span data-stu-id="3736e-332">Host name of the CPS where the call is parked.</span></span>
    
      - <span data-ttu-id="3736e-333">Carimbo de data/hora de quando a chamada foi estacionada.</span><span class="sxs-lookup"><span data-stu-id="3736e-333">Time stamp of when the call was parked.</span></span>

  - <span data-ttu-id="3736e-334">
            Parâmetro \*\*–f\*\* – lista o número de órbitas atualmente livres no pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-334">**–f** parameter—lists the number of currently free orbits in the pool.</span></span>

  - <span data-ttu-id="3736e-335">**– r \<n\>** parâmetro — lista as \<n\> últimas chamadas estacionadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-335">**–r \<n\>** parameter—lists the \<n\> last parked calls.</span></span> <span data-ttu-id="3736e-336">As informações são exibidas da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="3736e-336">The information displayed is as follows:</span></span>
    
      - <span data-ttu-id="3736e-337">URI do SIP da chamada estacionada.</span><span class="sxs-lookup"><span data-stu-id="3736e-337">Parkee SIP URI.</span></span>
    
      - <span data-ttu-id="3736e-338">URI do SIP do estacionador da chamada.</span><span class="sxs-lookup"><span data-stu-id="3736e-338">Parker SIP URI.</span></span>
    
      - <span data-ttu-id="3736e-339">Nome do host do CPS onde a chamada foi estacionada.</span><span class="sxs-lookup"><span data-stu-id="3736e-339">Host name of the CPS where the call was parked.</span></span>
    
      - <span data-ttu-id="3736e-340">Carimbo de data/hora de quando a chamada foi recuperada ou ignorada.</span><span class="sxs-lookup"><span data-stu-id="3736e-340">Time stamp of when the call was retrieved or dropped.</span></span>

  - <span data-ttu-id="3736e-341">**-t \<n\>** testes de parâmetro reservando uma órbita no banco de dados para mostrar a aleatoriedade dos números de órbita atribuídos.</span><span class="sxs-lookup"><span data-stu-id="3736e-341">**-t\<n\>** parameter - tests reserving an orbit in the database to show the randomness of the assigned orbit numbers.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-342">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-342">Output</span></span>

<span data-ttu-id="3736e-343">Dependendo dos parâmetros de entrada especificados em um prompt de comando, o Parquímetro de Chamada exibirá o seguinte resultado:</span><span class="sxs-lookup"><span data-stu-id="3736e-343">Depending on the input parameters that are specified at a command prompt, Call Parkometer displays the following output:</span></span>

  - <span data-ttu-id="3736e-344">Todos os intervalos de órbita configurados para este pool</span><span class="sxs-lookup"><span data-stu-id="3736e-344">All orbit ranges that are configured for this pool</span></span>

  - <span data-ttu-id="3736e-345">Chamadas estacionadas atualmente</span><span class="sxs-lookup"><span data-stu-id="3736e-345">Currently parked calls</span></span>

  - <span data-ttu-id="3736e-346">Número de órbitas livres (disponíveis)</span><span class="sxs-lookup"><span data-stu-id="3736e-346">Number of free (available) orbits</span></span>

  - <span data-ttu-id="3736e-347">Chamadas estacionadas recentemente</span><span class="sxs-lookup"><span data-stu-id="3736e-347">Recently parked calls</span></span>

  - <span data-ttu-id="3736e-348">Órbitas reservadas para testes uniformes e valores de órbita aleatórios</span><span class="sxs-lookup"><span data-stu-id="3736e-348">Reserved orbits for testing uniform and random orbit values</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-349">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-349">Purpose</span></span>

<span data-ttu-id="3736e-p136">O objetivo da ferramenta CPS é fornecer acesso de linha de comando ao banco de dados do CPS. O administrador pode visualizar o CPS usado e determinar o números de órbitas atribuídas a um pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-p136">The purpose of the CPS tool is to provide command-line access to the CPS database. The administrator can view the CPS usage and determine the number of orbits assigned to a pool.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-352">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-352">Requirements</span></span>

<span data-ttu-id="3736e-353">Não haverá nenhum requisito se esta ferramenta for executada no mesmo computador que estiver executando o CPS.</span><span class="sxs-lookup"><span data-stu-id="3736e-353">There are no requirements if this tool is run on the same computer that is running CPS.</span></span> <span data-ttu-id="3736e-354">Se essa ferramenta for executada em um computador remoto, o banco de dados do SQL Server usado pelo Lync Server 2013 deve ser configurado para permitir acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="3736e-354">If this tool is run on a remote computer, the SQL Server database used by Lync Server 2013 must be configured to allow remote access.</span></span> <span data-ttu-id="3736e-355">Chame Parkometer deve ser configurado com uma cadeia de conexão de banco de dados SQL Server para se conectar ao SQL Server do pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-355">Call Parkometer must be configured with a SQL Server database connection string to connect to the pool’s SQL Server.</span></span> <span data-ttu-id="3736e-356">Esta cadeia de conexão de banco de dados do SQL Server é definida no arquivo de configuração, **parkometer.exe.config**. Ele deve ser colocado no mesmo diretório em que parkometer.exe está localizado.</span><span class="sxs-lookup"><span data-stu-id="3736e-356">This SQL Server database connection string is defined in the configuration file, **parkometer.exe.config**. It must be placed in the same directory where parkometer.exe is located.</span></span> <span data-ttu-id="3736e-357">O arquivo XML a seguir é um exemplo de um parkometer.exe.config. Os parâmetros que devem ser configurados são o nome de usuário (por exemplo, administrador de mydomain \\ ), senha (por exemplo, mypassword) e nome do host (por exemplo, meuservidor).</span><span class="sxs-lookup"><span data-stu-id="3736e-357">The following XML file is an example of a parkometer.exe.config. The parameters that must be configured are user name (for example, mydomain\\Administrator), password (for example, mypassword), and host name (for example, myserver).</span></span>

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <appSettings>
       <add key="SQL" value="server=myserver\RTC;
    database=cpsdyn;
    User Id=mydomain\Administrator;
    Password=mypassword.;
    Integrated Security=false;"/>
      </appSettings>
    </configuration>
```

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-358">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-358">Examples</span></span>

<span data-ttu-id="3736e-359">Intervalos de órbitas implantados: o parâmetro –o lista todos os intervalos de órbita configurados para este pool, como a seguir:</span><span class="sxs-lookup"><span data-stu-id="3736e-359">Deployed orbit ranges: the –o parameter lists all orbit ranges that are configured for this pool as shown</span></span>

<span data-ttu-id="3736e-360">![As faixas órbitas no Call Parkometer.](images/JJ945604.9ede64cb-29d9-4782-a34b-b76c42fbdcad(OCS.15).jpg "As faixas órbitas no Call Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="3736e-360">![Orbit ranges in Call Parkometer.](images/JJ945604.9ede64cb-29d9-4782-a34b-b76c42fbdcad(OCS.15).jpg "Orbit ranges in Call Parkometer.")</span></span>

<span data-ttu-id="3736e-361">Chamadas estacionadas atualmente: o parâmetro –n lista todas as órbitas usadas atualmente neste pool, como a seguir:</span><span class="sxs-lookup"><span data-stu-id="3736e-361">Currently parked calls: the –n parameter lists all currently used orbits on this pool as shown</span></span>

<span data-ttu-id="3736e-362">![Chamadas estacionadas no momento no Call Parkometer.](images/JJ945604.07a7eec4-7999-4c92-93f0-95525b244b4c(OCS.15).jpg "Chamadas estacionadas no momento no Call Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="3736e-362">![Currently-parked calls in Call Parkometer.](images/JJ945604.07a7eec4-7999-4c92-93f0-95525b244b4c(OCS.15).jpg "Currently-parked calls in Call Parkometer.")</span></span>

<span data-ttu-id="3736e-363">Número de órbitas livres: o parâmetro –f lista o número de órbitas livres atualmente neste pool, como a seguir:</span><span class="sxs-lookup"><span data-stu-id="3736e-363">Number of free orbits: the –f parameter lists the number of currently free orbits in the pool as shown</span></span>

<span data-ttu-id="3736e-364">![Órbitas grátis no Call Parkometer.](images/JJ945604.ecc1d621-0ca0-4ecf-a579-08b41c6f08ed(OCS.15).jpg "Órbitas grátis no Call Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="3736e-364">![Free orbits in Call Parkometer.](images/JJ945604.ecc1d621-0ca0-4ecf-a579-08b41c6f08ed(OCS.15).jpg "Free orbits in Call Parkometer.")</span></span>

<span data-ttu-id="3736e-365">Chamadas estacionadas recentemente: o parâmetro – r \<n\> lista as \<n\> últimas chamadas estacionadas conforme mostrado</span><span class="sxs-lookup"><span data-stu-id="3736e-365">Recently parked calls: the –r \<n\> parameter lists the \<n\> last parked calls as shown</span></span>

<span data-ttu-id="3736e-366">![Chamadas estacionadas recentemente no Call Parkometer.](images/JJ945604.1c5eb27d-faa1-491b-b4aa-b484255c3353(OCS.15).jpg "Chamadas estacionadas recentemente no Call Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="3736e-366">![Recently-parked calls in Call Parkometer.](images/JJ945604.1c5eb27d-faa1-491b-b4aa-b484255c3353(OCS.15).jpg "Recently-parked calls in Call Parkometer.")</span></span>

<span data-ttu-id="3736e-367">Testar reserva órbita: os testes de \<n\> parâmetro – t que reservam uma órbita no banco de dados conforme mostrado</span><span class="sxs-lookup"><span data-stu-id="3736e-367">Test orbit reservation: the –t \<n\> parameter tests reserving an orbit in the database as shown</span></span>

<span data-ttu-id="3736e-368">![Teste as reservas em órbita na Call Parkometer.](images/JJ945604.84c9b69e-7af0-4224-8711-a43a28f08691(OCS.15).jpg "Teste as reservas em órbita na Call Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="3736e-368">![Test orbit reservations in Call Parkometer.](images/JJ945604.84c9b69e-7af0-4224-8711-a43a28f08691(OCS.15).jpg "Test orbit reservations in Call Parkometer.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-369">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-369">Summary</span></span>

<span data-ttu-id="3736e-370">O Parquímetro de Chamada é uma ferramenta de linha de comando que fornece informações detalhadas sobre o Servidor de Estacionamento de Chamada.</span><span class="sxs-lookup"><span data-stu-id="3736e-370">Call Parkometer is a command-line tool that provides detailed information about the Call Park Server.</span></span>

</div>

</div>

<div>

## <a name="cleanupstorageservicedata"></a><span data-ttu-id="3736e-371">CleanupStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="3736e-371">CleanupStorageServiceData</span></span>

<span data-ttu-id="3736e-372">A ferramenta CleanupStorageServiceData Resource Kit permite excluir dados órfãos do banco de dados usado pelo serviço de armazenamento do Lync Server (LYSS).</span><span class="sxs-lookup"><span data-stu-id="3736e-372">The CleanupStorageServiceData resource kit tool allows for deleting of orphaned data from the database used by the Lync Server Storage Service (LYSS).</span></span> <span data-ttu-id="3736e-373">Uma função do serviço de armazenamento é armazenar em buffer a comunicação entre o Lync Server e vários pontos de extremidade de armazenamento de dados back-end, como o SQL Server e o Exchange.</span><span class="sxs-lookup"><span data-stu-id="3736e-373">One function of the storage service is to buffer communication between Lync Server and various back-end data storage endpoints, like SQL Server and Exchange.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-374">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-374">Description</span></span>

<span data-ttu-id="3736e-375">Para dar suporte à alta disponibilidade, o LYSS aceita e salva cópias dos dados em vários servidores front-end no pool temporariamente, e remove esses dados após serem entregues ao seu local de armazenamento final de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="3736e-375">To support high availability, LYSS accepts and saves copies of the data on multiple front end servers in the pool temporarily, and removes that data once it has been delivered to its final long-term storage location.</span></span> <span data-ttu-id="3736e-376">Há situações anormais que podem ocorrer durante a operação normal, quando um servidor pode falhar ou enfrentar um problema de processamento, e alguns dados podem não ser limpos corretamente.</span><span class="sxs-lookup"><span data-stu-id="3736e-376">There are unusual situations which may occur during otherwise normal operation, when a server might crash or experience a processing issue, and some data might not get cleaned up properly.</span></span> <span data-ttu-id="3736e-377">Esses dados são inofensivos, mas não consomem recursos de processamento limitados.</span><span class="sxs-lookup"><span data-stu-id="3736e-377">This data is harmless, but it does consume limited processing resources.</span></span> <span data-ttu-id="3736e-378">Grande parte da manutenção de dados necessária normal é automatizada, mas essa ferramenta permite que a identificação e a remoção sejam excluídas desses dados órfãos quando a remoção automatizada não é possível.</span><span class="sxs-lookup"><span data-stu-id="3736e-378">Much of the normal required data maintenance is automated, but this tool allows for the safe identification and removal of such orphaned data when automated removal is not possible.</span></span> <span data-ttu-id="3736e-379">O uso dessa ferramenta é indicado quando um alerta do Gerenciador de operações do sistema de monitoramento de integridade (SCOM) é gerado, solicitando que o administrador remova os dados desnecessários dos bancos de dados do LYSS locais do pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-379">Usage of this tool is indicated when a health monitoring System Center Operations Manager (SCOM) alert is raised which asks the administrator to remove the unneeded data from the local LYSS databases in the pool.</span></span> <span data-ttu-id="3736e-380">Haverá um evento correspondente no log de eventos do front-end que disparou o alerta.</span><span class="sxs-lookup"><span data-stu-id="3736e-380">There will be a corresponding event in the event log on the front end which triggered the alert.</span></span> <span data-ttu-id="3736e-381">Os detalhes do evento contêm informações sobre a quantidade de dados órfãos contidos no front-end e são acionados quando esses dados excedem certos limites predefinidos</span><span class="sxs-lookup"><span data-stu-id="3736e-381">The event details will contain information about the amount of orphaned data contained on the front end, and is raised when that data exceeds certain pre-determine thresholds</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-382">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-382">Requirements</span></span>

<span data-ttu-id="3736e-383">Instale as ferramentas do Lync Server 2013, Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="3736e-383">Install the Lync Server 2013, Resource Kit Tools.</span></span> <span data-ttu-id="3736e-384">A ferramenta é executada em máquinas Unidas a domínios nas quais o Shell de gerenciamento do Lync Server e do Lync Server 2013 está instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-384">The tool runs on domain-joined machines where Lync Server and Lync Server 2013 Management Shell are installed.</span></span> <span data-ttu-id="3736e-385">A ferramenta usa um cmdlet do Shell de gerenciamento para identificar todos os servidores de front-end do pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-385">The tool uses a cmdlet from the management shell to identify all Front End servers in the pool.</span></span> <span data-ttu-id="3736e-386">Em segundo lugar, a ferramenta deve ser executada em um computador no pool em que o banco de dados do **RtcLocal** está instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-386">Secondly, the tool must be executed from a machine in the pool which has the **RtcLocal** database installed.</span></span> <span data-ttu-id="3736e-387">Este banco de dados é usado pela ferramenta CleanupStorageServiceData para obter os detalhes de conexão necessários para se comunicar com o serviço de roteamento do Lync Server. por fim, a conta ou a credencial que invocar a ferramenta deve ter permissão de leitura/gravação para o compartilhamento de arquivos no qual deseja gravar o log de saída. Além disso, essa ferramenta depende do pool estar em um estado estável.</span><span class="sxs-lookup"><span data-stu-id="3736e-387">This database is used by the CleanupStorageServiceData tool to get the connection details needed to communicate with the Lync Server Routing Service.Finally, the account or credential invoking the tool must have read/write permission to the file share to which they want to write the output log.Also, this tool depends on the pool being in a stable state.</span></span> <span data-ttu-id="3736e-388">Em essência, isso significa que cada servidor front-end deve estar em funcionamento, a instância LYNCLOCAL do SQL Server e o banco de dados do LYSS devem estar conectados, e cada grupo de roteamento deve ter um conjunto completo de 1 servidor front-end primário e dois servidores front-end secundários.</span><span class="sxs-lookup"><span data-stu-id="3736e-388">In essence this means that every Front End server is expected to be up and running, the SQL Server LYNCLOCAL instance and LYSS database must be able to be connected to, and each routing group must have a complete set of 1 primary Front End servers and 2 secondary Front End servers.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-389">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-389">Examples</span></span>

<span data-ttu-id="3736e-390">C: \\ arquivos de programas \\ Microsoft Lync Server 2013 \\ reskit \\ StorageService \> ImportStorageServiceData.exe</span><span class="sxs-lookup"><span data-stu-id="3736e-390">C:\\Program Files\\Microsoft Lync Server 2013\\ResKit\\StorageService\> ImportStorageServiceData.exe</span></span>

    Description:
    This tool will remove orphaned data from the Storage Service database
    for a pool. You are required to run this tool on a machine inside the
    pool which has the Lync Server Management Shell installed and has RtcLocal database installed.
    Usage: Default behavior is to clean up orphaned data from the all the 
           Storage Service databases in the current pool.
    Additional Options:
    -Verbose    : Turn verbose output on.
    -LogPath    : The UNC path to which to write the log.
    ------------------------------------------------------------------------------
    Please wait while we initialize...
    Found 4 front end servers
    Replica Instances for LYSS Service
    Address: server2.vdomain.com - Primaries: 7 Secondaries: 14
    Address: server.vdomain.com - Primaries: 7 Secondaries: 14
    Address: server1.vdomain.com - Primaries: 7 Secondaries: 14
    Address: server3.vdomain.com - Primaries: 7 Secondaries: 14
    Primary Total Count = 28, Secondary Total Count = 56
    Finding and removing orphaned data for 28 routing groups
    Removing 1 stale groups from FE server.vdomain.com
    No stale routing groups detected on FE server2.vdomain.com
    No stale routing groups detected on FE server1.vdomain.com
    No stale routing groups detected on FE server3.vdomain.com
    Searching for stale queue items
    Removed 20 stale queue items for routing group 17D5435AE40259F7BBDF1866776386E4
    No stale queue items found for routing group 1975349662315F90B119DACB4F2AE3AD
    No stale queue items found for routing group 1A23E3D58BDB5A458A0B73F34AB7ACBE
    No stale queue items found for routing group 1AC91E3A1029535A80123121989CEADC
    No stale queue items found for routing group 3313935458E35B9B9759E08A15D251E6
    No stale queue items found for routing group 39BB0035B06B5427873FC6099720462A
    No stale queue items found for routing group 40721948E7B55CE893A53E911F76D185
    No stale queue items found for routing group 4501E04EAE4856059346949FF817C220
    No stale queue items found for routing group 4D833C98801F546F8E45E417EE028E2E
    No stale queue items found for routing group 5AD77443AD955A22A876749BE66D5317
    No stale queue items found for routing group 69844A271E6C5633A1F2B46A42287DD6
    No stale queue items found for routing group 69DA3BE407A95C7284EB4B1337718C93
    No stale queue items found for routing group 8437358AB34A5CC8967D5EF39494AB8D
    No stale queue items found for routing group 8ED455B1789655359816E1C5BF4C430F
    No stale queue items found for routing group 904F6C9B8AC951AE8B3C86684D3832E4
    No stale queue items found for routing group 90AAB3AE9A1950E0ADE7809A27021D63
    No stale queue items found for routing group 944F5724C65C5F93900DC1C8C898B102
    No stale queue items found for routing group 9E8A2630250C51769E39F63F0FB552BA
    No stale queue items found for routing group A11E27AE439A582288D4657EDA86B565
    No stale queue items found for routing group A9B10C76E764556FAEA3E47301EDF518
    No stale queue items found for routing group AEA2699E74ED59848ACEA7896699430D
    No stale queue items found for routing group B269961603E75065AFDA4F4F006DA5E4
    No stale queue items found for routing group BB873D9A3DA959DAB2FD743E5AA619F7
    No stale queue items found for routing group BCC6A48FBA2454B79B9EDB276657A404
    No stale queue items found for routing group C8EF4805722B5F6C876EBC0440B420FD
    No stale queue items found for routing group CA38EBDAC4845489ACE208C2240E4056
    No stale queue items found for routing group F5921887DB025C5F908CE42DB7F1AEE8
    No stale queue items found for routing group F9E606A825395422B3BF7A01ECBB7B1F
    Writing log: M:\Dev\Server\ResKit\StorageService\CleanupStorageServiceData.Log_20121009_151040
    Tool has finished execution.  Errors encountered: 0
    C:\Program Files\Microsoft Lync Server 2013\ResKit\StorageService>

</div>

</div>

<div>

## <a name="dbanalyze"></a><span data-ttu-id="3736e-391">DBAnalyze</span><span class="sxs-lookup"><span data-stu-id="3736e-391">DBAnalyze</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-392">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-392">Description</span></span>

<span data-ttu-id="3736e-393">DBAnalyze é uma ferramenta de linha de comando que ajuda os administradores a reunir relatórios de análise sobre os bancos de dados do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-393">DBAnalyze is a command-line tool that helps administrators to gather analysis reports about the Lync Server 2013 databases.</span></span> <span data-ttu-id="3736e-394">O DBAnalyze tem os seguintes modos: diagnóstico, dados do usuário, conferência, MCUs e fragmentação de disco:</span><span class="sxs-lookup"><span data-stu-id="3736e-394">DBAnalyze has the following modes: diagnostic, user data, conference, MCUs, and disk fragmentation:</span></span>

  - <span data-ttu-id="3736e-395">**Modo de diagnóstico** Cria um relatório com informações sobre tabelas (número de registros, fragmentação, tamanho dos dados e tamanho do índice), tamanho do arquivo de log e dos dados, a hora do último backup, a distribuição de contatos entre os servidores que estiverem executando o Microsoft Office Communications Server, o número médio de permissões, contatos, contêineres, assinaturas, publicações, pontos de extremidade por usuário, usuários hospedados inadequadamente, usuários que não podem ser roteados, o número médio de conferências organizadas por usuários, conferências agendadas, conferências ativas e a versão do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3736e-395">**Diagnostic mode**   Creates a report that includes information about tables (number of records, fragmentation, data size, and index size), data and log file sizes, the last back-up time, contact distribution among servers that are running Microsoft Office Communications Server, the average number of permissions, contacts, containers, subscriptions, publications, endpoints per user, any improperly homed users, users that can’t be routed, the average number of conferences organized per user, scheduled conferences, active conferences, and the database version.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3736e-396">A execução do modo de diagnóstico pode afetar o desempenho do servidor.</span><span class="sxs-lookup"><span data-stu-id="3736e-396">Running diagnostic mode can affect server performance.</span></span>

    
    </div>

  - <span data-ttu-id="3736e-397">**Modo de dados do usuário**  Relata os dados de contato, contêiner, assinatura, publicação, permissão e grupo de contatos para um usuário especificado ou para usuários que tenham esse usuário em suas listas de contatos e permissões.</span><span class="sxs-lookup"><span data-stu-id="3736e-397">**User data mode**  Reports contact, container, subscription, publication, permission, and contact-group data for a specified user or for users who have that user in their contact and permission lists.</span></span> <span data-ttu-id="3736e-398">Este modo também relata dados resumidos de conferências que um usuário organizou ou para as quais foi convidado.</span><span class="sxs-lookup"><span data-stu-id="3736e-398">This mode also reports summary data for conferences that a user organizes or is invited to.</span></span>

  - <span data-ttu-id="3736e-399">**Modo de conferência** Relata dados detalhados de uma conferência específica, incluindo os detalhes da hora agendada da conferência, a lista de convidados, a lista de tipos de mídia permitidos para a conferência, as MCUs (Unidades de Controle de Multipontos) ativas, a lista de participantes ativos e o estado de sinalização de cada participante.</span><span class="sxs-lookup"><span data-stu-id="3736e-399">**Conference mode**   Reports detailed data for a specific conference, including all schedule-time details for the conference, the invitee list, the list of media types allowed for the conference, active MCUs (multipoint control units), the active participant list, and each participant’s signaling state.</span></span>

  - <span data-ttu-id="3736e-400">**Decodificar ID de Reunião** Decodifica a ID de uma reunião PSTN (Rede Telefônica Pública Comutada) especificada pela opção **/pstnid**, mas não se conecta ao back-end para obter informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-400">**Decode Meeting ID**  Decodes a public switched telephone network (PSTN) meeting ID that is specified by the **/pstnid** switch but does not connect to the back end for detailed information.</span></span>

  - <span data-ttu-id="3736e-401">**Resolver conferência**  Decodifica uma ID de reunião PSTN especificada pela opção **/pstnid** e exibe informações sobre a conferência indicada pela ID.</span><span class="sxs-lookup"><span data-stu-id="3736e-401">**Resolve conference**   Decodes a PSTN meeting ID that is specified by the **/pstnid** switch and displays information about the conference indicated by the ID.</span></span>

  - <span data-ttu-id="3736e-402">**Modo de MCUs** Relata a ID, o tipo de mídia, a URL, o status de pulsação, a carga de conferência e a carga de participante de cada MCU no pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-402">**MCUs mode**  Reports the ID, media type, URL, heartbeat status, conference load, and participant load for each MCU in the pool.</span></span>

  - <span data-ttu-id="3736e-403">**Modo de fragmentação de disco** Exibe o status de fragmentação de todos os discos.</span><span class="sxs-lookup"><span data-stu-id="3736e-403">**Disk fragmentation mode**  Displays the fragmentation status of all disks.</span></span>

<span data-ttu-id="3736e-p143">Esta ferramenta pode ser usada para diagnosticar diversos problemas ou para ajudar os administradores no planejamento da capacidade. Por exemplo, se a maioria dos usuários hospedados no servidor A escolher como contatos usuários hospedados no servidor B, o administrador poderá mover os usuários do servidor A para o servidor B para reduzir o tráfego entre servidores.</span><span class="sxs-lookup"><span data-stu-id="3736e-p143">This tool can be used to diagnose various problems or to assist administrators with capacity planning. For example, if most of the users homed on server A choose users homed on server B as their contacts, the administrator can move the users on server A to server B to reduce cross-server traffic.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-406">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-406">Output</span></span>

<span data-ttu-id="3736e-407">Esta ferramenta emite relatórios predefinidos sobre o banco de dados do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-407">This tool outputs predefined reports about the Lync Server 2013 database.</span></span> <span data-ttu-id="3736e-408">**Caminho:** % ProgramFiles% \\ Microsoft Lync Server 2013 \\ reskit</span><span class="sxs-lookup"><span data-stu-id="3736e-408">**Path:** %ProgramFiles%\\Microsoft Lync Server 2013\\Reskit</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-409">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-409">Purpose</span></span>

<span data-ttu-id="3736e-410">Para instalar o Dbanalyze.exe, copie-o para uma pasta local e execute a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="3736e-410">To install Dbanalyze.exe, copy it to a local folder and then run the tool.</span></span> <span data-ttu-id="3736e-411">Para usar a ferramenta, execute o seguinte comando a partir da linha de comando.`dbanalyze.exe [/v] [/report:value] [/sqlserver:value] [/user:user@domain.com] [/conf:value][/pstnid:Value] [/maxcontacts:value]`</span><span class="sxs-lookup"><span data-stu-id="3736e-411">To use the tool, run the following command from the command line.`dbanalyze.exe [/v] [/report:value] [/sqlserver:value] [/user:user@domain.com] [/conf:value][/pstnid:Value] [/maxcontacts:value]`</span></span> <span data-ttu-id="3736e-412">As descrições das opções de linha de comando são mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="3736e-412">The descriptions for the command-line options are shown below.</span></span>

<span data-ttu-id="3736e-413">![Opções de linha de comando para Dbanalyze.exe.](images/JJ945604.22bf3432-af6d-495b-8f48-d94c5d259523(OCS.15).jpg "Opções de linha de comando para Dbanalyze.exe.")</span><span class="sxs-lookup"><span data-stu-id="3736e-413">![Command line options for Dbanalyze.exe.](images/JJ945604.22bf3432-af6d-495b-8f48-d94c5d259523(OCS.15).jpg "Command line options for Dbanalyze.exe.")</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-414">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-414">Requirements</span></span>

<span data-ttu-id="3736e-415">**Computador** O DBAnalyze pode ser executado apenas em um computador associado a um domínio que tenha o Lync Server 2013 instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-415">**Computer** DBAnalyze can be run only from a domain-joined computer that has Lync Server 2013 installed.</span></span>

<span data-ttu-id="3736e-416">**Rede** O computador deve poder se conectar ao banco de dados back-end.</span><span class="sxs-lookup"><span data-stu-id="3736e-416">**Network** The computer should be able to connect to the back-end database.</span></span>

<span data-ttu-id="3736e-417">**Software** Os componentes do software do Lync Server 2013 devem ser instalados antes de executar o DBAnalyze.</span><span class="sxs-lookup"><span data-stu-id="3736e-417">**Software** Lync Server 2013 software components must be installed before running DBAnalyze.</span></span>

<span data-ttu-id="3736e-418">**Usuários** do A tabela a seguir mostra os administradores que têm as permissões necessárias para acessar bancos de dados do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-418">**Users** The table below shows the administrators who have the necessary permissions to access Lync Server 2013 databases.</span></span>

<span data-ttu-id="3736e-419">![Tabela de permissões para Dbanalyze.exe.](images/JJ945604.b8931e9e-834e-4dec-8a84-2fc47d1613e9(OCS.15).jpg "Tabela de permissões para Dbanalyze.exe.")</span><span class="sxs-lookup"><span data-stu-id="3736e-419">![Permissions table for Dbanalyze.exe.](images/JJ945604.b8931e9e-834e-4dec-8a84-2fc47d1613e9(OCS.15).jpg "Permissions table for Dbanalyze.exe.")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-420">Uma conta de administrador local é necessária para o modo <STRONG>/report:disk</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3736e-420">A local administrator account is required for <STRONG>/report:disk</STRONG> mode.</span></span>



</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-421">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-421">Examples</span></span>

<span data-ttu-id="3736e-422">Veja abaixo exemplos de comandos válidos do Dbanalyze.exe:</span><span class="sxs-lookup"><span data-stu-id="3736e-422">The following are examples of valid Dbanalyze.exe commands:</span></span>

    dbanalyze.exe /report:diag
    dbanalyze.exe /report:user /user:usera@domainb.com
    dbanalyze.exe /report:conf /user:bob@example.com /conf:1W9J71SKSX2X
    dbanalyze.exe /report:resolve /pstnid:12345
    dbanalyze.exe /report:mcus
    dbanalyze.exe /report:disk

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-423">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-423">Summary</span></span>

<span data-ttu-id="3736e-424">O DBAnalyzer fornece aos administradores um rápido e fácil de analisar bancos de dados do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-424">DBAnalyzer provides administrators a quick and easy to analyze Lync Server 2013 databases.</span></span>

</div>

</div>

<div>

## <a name="importstorageservicedata"></a><span data-ttu-id="3736e-425">ImportStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="3736e-425">ImportStorageServiceData</span></span>

<span data-ttu-id="3736e-426">A ferramenta ImportStorageServiceData do kit de recursos permite reimportar os dados da fila e do ponto de extremidade que foram exportados do Serviço de Armazenamento (LYSS) para o Serviço de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3736e-426">The ImportStorageServiceData resource kit tool allows for re-importing Queue and Endpoint data that was flushed out of the Storage Service (LYSS) back into the Storage Service.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-427">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-427">Description</span></span>

<span data-ttu-id="3736e-428">A exportação dos dados do Serviço de Armazenamento pode ter sido automática (periodicamente) com base no status do item da fila ou no tamanho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3736e-428">The data flushed out of the Storage Service could have been automatic (periodic) based on Queue Item status or database size.</span></span> <span data-ttu-id="3736e-429">Ela pode ter ocorrido devido à invocação manual do cmdlet de failover do pool ou do cmdlet StorageServiceFullFlush (invocado pelo cmdlet de failover do pool).</span><span class="sxs-lookup"><span data-stu-id="3736e-429">It could have happened due to the manual invocation of the pool failover cmdlet, or the StorageServiceFullFlush cmdlet (which the pool failover cmdlet invokes).</span></span> <span data-ttu-id="3736e-430">Lembre-se de que os dados não devem ser importados novamente se qualquer um dos tamanhos de banco de dados do serviço de armazenamento (LYSS) no front-ends estiver acima do nível normal, porque isso provavelmente apenas fará com que mais dados sejam exportados. Além disso, quaisquer problemas que possam ter contribuído com erros que fizeram com que a fila do serviço de armazenamento cresça devem primeiro ser resolvidos (por exemplo, erros de ponto de extremidade do Exchange, problemas de rede ou outros problemas).</span><span class="sxs-lookup"><span data-stu-id="3736e-430">Note that data should ideally not be re-imported if any of the Storage Service (LYSS ) database size on the front ends is above the normal level, because doing so will likely just cause more data to be exported back out. Furthermore, any problems which could have contributed to errors that caused the Storage Service Queue to grow should first be resolved (for example Exchange endpoint errors, network issues, or other problems).</span></span>

<span data-ttu-id="3736e-431">**Cenário 1:** durante o failover do pool, os arquivos poderão ser liberados do serviço de armazenamento de cada front-end.</span><span class="sxs-lookup"><span data-stu-id="3736e-431">**Scenario 1:** during pool failover, files may be flushed out from storage service for each front end.</span></span> <span data-ttu-id="3736e-432">Após a conclusão do failover, a ferramenta deverá ser executada para reimportar os dados.</span><span class="sxs-lookup"><span data-stu-id="3736e-432">After failover is completed, the tool should be run to re-import the data.</span></span>

<span data-ttu-id="3736e-433">**Cenário 2:** os dados estão sendo exportados de maneira automática diariamente ou em resposta ao banco de dados de Serviço de Armazenamento ter excedido determinados limites de tamanho (por exemplo, 60%, 80%, 90%, capacidade total).</span><span class="sxs-lookup"><span data-stu-id="3736e-433">**Scenario 2:** data is being flushed automatically each day or in response to Storage Service database exceeding certain size thresholds ( for example 60%, 80%, 90% full ).</span></span> <span data-ttu-id="3736e-434">Esses dados exportados automaticamente devem ser reimportados regularmente pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="3736e-434">This automatically flushed data should be re-imported routinely by the administrator.</span></span> <span data-ttu-id="3736e-435">Na situação acima, se o pacote do SCOM que está sendo monitorado não for implantado, há eventos para o serviço de armazenamento do Lync Server relacionados a dados que estão sendo liberados do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3736e-435">In the above situation, if the monitoring SCOM pack is not deployed, there are events for Lync Server Storage Service relating to data being flushed from the Storage Service.</span></span> <span data-ttu-id="3736e-436">As IDs de evento são: 32075 (operação de exportação completa iniciada), 32076 (exportação completa concluída), 32082 (exportação de nível de manutenção iniciada), 32083 (exportação de nível de manutenção concluída), 32089 (exportação ocorrida devido ao preenchimento do banco de dados).</span><span class="sxs-lookup"><span data-stu-id="3736e-436">Event IDs of 32075 (full flush operation is started), 32076 (full flush has completed), 32082 (maintenance level flush started), 32083 (maintenance level flush complete), 32089 (flush occurred due to filling up of database).</span></span> <span data-ttu-id="3736e-437">Observe que essas IDs de evento correspondem à versão do RTM.</span><span class="sxs-lookup"><span data-stu-id="3736e-437">Note these event Ids correspond to the RTM release.</span></span> <span data-ttu-id="3736e-438">Quando um administrador vê esses eventos, isso significa que há arquivos que foram liberados. Esses dados devem ser importados rotineiramente usando essa ferramenta, por exemplo, uma vez por semana.</span><span class="sxs-lookup"><span data-stu-id="3736e-438">When an administrator sees these events, it means that there are files that have been flushed out. This data should routinely be imported back using this tool, for example once per week.</span></span>

<span data-ttu-id="3736e-439">Para o lançamento do serviço online, se o pacote do SCOM Pack para Lync Server for implantado, há novos alertas que podem ser gerados, que pede ao administrador para reimportar os dados liberados de volta para o serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3736e-439">For the Online Service release, if health monitoring SCOM pack for Lync Server is deployed, there are new alerts which may be raised which ask the administrator to re-import the flushed data back into Storage Service.</span></span> <span data-ttu-id="3736e-440">Haverá um evento correspondente no log de eventos no servidor front-end que disparou o alerta.</span><span class="sxs-lookup"><span data-stu-id="3736e-440">There will be a corresponding event in the event log on the Front End server which triggered the alert.</span></span> <span data-ttu-id="3736e-441">O evento dará uma descrição do caminho pai sob o qual se encontram os arquivos de dados exportados, bem como a quantidade de arquivos existentes que cumpre os critérios do alerta.</span><span class="sxs-lookup"><span data-stu-id="3736e-441">The event will give a description of the Parent path under which the flushed data files are located, as well as how many files there are which meet the alert criteria.</span></span> <span data-ttu-id="3736e-442">O critério de alerta é de que há X ou mais arquivos sob o caminho pai específico que tem pelo menos Y dias (em que X e Y são predefinidos dentro do StorageService, mas podem ser substituídos, alterando o arquivo APPCONFIG).</span><span class="sxs-lookup"><span data-stu-id="3736e-442">The alert criteria is that there are X or more files under the particular parent path which are at least Y days old ( where X and Y are preset within the StorageService but can be overridden by changing the APPCONFIG file.)Two examples of events which can trigger the health alert are shown below, with the difference being their parent path.</span></span> <span data-ttu-id="3736e-443">Dois exemplos de eventos que podem disparar o alerta de integridade são mostrados abaixo, com a diferença sendo seu respectivo caminho pai.</span><span class="sxs-lookup"><span data-stu-id="3736e-443">One possibility is under Web service file share, while the other possibility is the local Application Data directory of each front end.</span></span> <span data-ttu-id="3736e-444">(por exemplo c: \\ ProgramData \\ Microsoft \\ Lync Server \\ StorageService).</span><span class="sxs-lookup"><span data-stu-id="3736e-444">( for example c:\\ProgramData\\Microsoft\\Lync Server\\StorageService ).</span></span> <span data-ttu-id="3736e-445">O administrador executará essa ferramenta do reskit.</span><span class="sxs-lookup"><span data-stu-id="3736e-445">The administrator will then run this reskit tool.</span></span>

<span data-ttu-id="3736e-446">Essa ferramenta aumentará a carga de CPU e de E/S no front-end em que estiver sendo executada e também em outros front-ends se os dados não pertencerem ao front-end no qual a ferramenta estiver sendo executada.</span><span class="sxs-lookup"><span data-stu-id="3736e-446">This tool will increase CPU and IO load on the front end it is running on, as well as other front ends, in the situation that the data is not owned by the front end that the tool is executed on.</span></span> <span data-ttu-id="3736e-447">Recomendamos executar essa ferramenta quando os front-ends não estiverem sob uma carga de E/S e CPU pesada, por exemplo, fora dos horários de pico.</span><span class="sxs-lookup"><span data-stu-id="3736e-447">We recommend runng this tool when front ends are not under heavy CPU and IO load, for example outside of peak hours.</span></span> <span data-ttu-id="3736e-448">Em segundo lugar, essa ferramenta leva de 2 a 3 minutos para importar um arquivo de dados.</span><span class="sxs-lookup"><span data-stu-id="3736e-448">Secondly, this tool can 2 to 3 minutes to import one data file.</span></span> <span data-ttu-id="3736e-449">Lembre-se disso ao estimar por quanto tempo a ferramenta estará em execução. O arquivo de log detalhado gerado pela ferramenta, por padrão, será exibido no repositório de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3736e-449">Keep this in mind when estimating how long tool will be running.The verbose log file generated by the tool will by default appear on the File Store.</span></span> <span data-ttu-id="3736e-450">Exclua-o se não houver nenhum erro relatado, pois o arquivo de log pode ter muitos megabytes.</span><span class="sxs-lookup"><span data-stu-id="3736e-450">Delete it if there are no errors reported, because the log file can be tens of MB or more.</span></span>

<span data-ttu-id="3736e-451">![Exemplos de eventos do log de eventos do servidor de armazenamento.](images/JJ945604.3a903ef7-ea8a-4606-8229-a3e32f13af3a(OCS.15).jpg "Exemplos de eventos do log de eventos do servidor de armazenamento.")</span><span class="sxs-lookup"><span data-stu-id="3736e-451">![Sample Storage Server event log events.](images/JJ945604.3a903ef7-ea8a-4606-8229-a3e32f13af3a(OCS.15).jpg "Sample Storage Server event log events.")</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-452">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-452">Requirements</span></span>

<span data-ttu-id="3736e-453">Instale as ferramentas do Lync Server 2013, Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="3736e-453">Install the Lync Server 2013, Resource Kit Tools.</span></span> <span data-ttu-id="3736e-454">A ferramenta é executada em máquinas Unidas a domínios nas quais o Lync Server e o Shell de gerenciamento do Lync Server são instalados.</span><span class="sxs-lookup"><span data-stu-id="3736e-454">The tool runs on domain-joined machines where Lync Server and Lync Server Management Shell are installed.</span></span> <span data-ttu-id="3736e-455">A ferramenta usa um cmdlet do Shell de gerenciamento para identificar todos os servidores de front-end do pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-455">The tool uses a cmdlet from the management shell to identify all the Front End servers in the pool.</span></span> <span data-ttu-id="3736e-456">Em segundo lugar, a ferramenta deve ser executada em um computador no pool em que o banco de dados do **RtcLocal** está instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-456">Secondly, the tool must be executed from a machine in the pool which has the **RtcLocal** database installed.</span></span> <span data-ttu-id="3736e-457">Esse banco de dados é usado pela ferramenta para recuperar a localização do compartilhamento de arquivo WEBSERVICE para o pool. Além disso, antes de usar a ferramenta, cada servidor front-end deve primeiro habilitar a comunicação remota do Windows PowerShell usando **Enable-PSRemoting** em cada servidor front-end, bem como a máquina na qual a ferramenta é executada.</span><span class="sxs-lookup"><span data-stu-id="3736e-457">This database is used by the tool to retrieve the location of the WEBSERVICE file share for the pool.Additionally, before using the tool, each Front End server must first enable Windows PowerShell Remoting using **Enable-PSRemoting** on each Front End server, as well as the machine that the tool is executed from.</span></span> <span data-ttu-id="3736e-458">Caso contrário, os comandos remotos do Windows PowerShell dessa ferramenta falharão.</span><span class="sxs-lookup"><span data-stu-id="3736e-458">Otherwise, remote Windows PowerShell commands from this tool will fail.</span></span> <span data-ttu-id="3736e-459">A comunicação remota do Windows PowerShell pode ser desativada em todos os servidores de front-end do pool após o término.</span><span class="sxs-lookup"><span data-stu-id="3736e-459">Windows PowerShell Remoting can be turned off on all Front End servers in the pool after it is finished.</span></span> <span data-ttu-id="3736e-460">Por fim, a conta ou a credencial que invocar a ferramenta deve ter permissão de leitura/gravação para o compartilhamento de arquivo WebService para o pool em que ele está executando essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="3736e-460">Finally, the account or credential invoking the tool must have read/write permission to the webservice file share for the pool they are executing this tool on.</span></span> <span data-ttu-id="3736e-461">Caso contrário, a ferramenta irá falhar com erros de permissão de e/s.</span><span class="sxs-lookup"><span data-stu-id="3736e-461">Otherwise the tool will fail with IO Permission errors.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-462">No Windows Server 2012, a comunicação remota do Windows PowerShell está habilitada por padrão, mas não no sistema operacional Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3736e-462">On Windows Server 2012, Windows PowerShell Remoting is enabled by default, but not on the Windows Server 2008 operating system.</span></span>



</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-463">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-463">Examples</span></span>

    >  C:\StorageService>ImportStorageServiceData.exe
    Description:
    This tool will re-import Storage Service (LYSS) flushed queue data back in.  For a pool: you are required to run this tool on a machine inside the pool which has the Lync Server Management Shell installed.  Additionally, all front end machines need to have Windows Powershell Remoting enabled before executing this tool by executing Enable-PSRemoting.  Also, please ensure that all Storage Service instance DB Size are at the 'Normal' level (verify this by viewing Eventlog events). Otherwise re-importing may cause data to be flushed out again if any Storage Service instance DB size level goes above 'Normal'.
    Usage: Default behavior is to Import data from web service file share as well as any files on all Front End machines in pool.
    Additional Options:
    -Verbose                    : Turn verbose output on.
    
    -StorageServiceHostName     : Host Name of Storage Service WCF endpoint.  ( Default=localhost netnamedpipe binding. )
                                        
    -FileSharePath              : Import only all data from just under the UNC path specified.
    
    ActivityID: cc3b62ff-bb66-4e61-a6e2-96cb3626315c. <-- Use this to correlate with StorageService trace logs if troubleshooting.
    Type Server name (TCP binding) or press <enter> for localhost (NamePipe binding):
    Using NetNamedPipeBinding...
    OnTopologyChanged Event received
    Web Service File Share: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService
    
    Front Ends:
    server.vdomain.com
    server2.vdomain.com
    server1.vdomain.com
    server3.vdomain.com
    Looking under directory: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService for exported data.
    # Files found: 8
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml
    Items deserialized: 20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml
    Items deserialized: 20
    
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server1.vdomain.com, queueItems=20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\904f6c9b8ac951ae8b3c86684d3832e4__0.xml
    
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server1.vdomain.com, queueItems=20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\904f6c9b8ac951ae8b3c86684d
    3832e4__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\904f6c9b8ac951ae8b3c
    86684d3832e4__0.xml
    
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER1.vdomain.com\904f6c9b8ac951ae8b3c86684d3832e4__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER2.vdomain.com\69844a271e6c5633a1f2b46a42287dd6__0.xml
    
    Items deserialized: 20
    
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server2.vdom
    ain.com, queueItems=20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER2.vdomain.com\69844a271e6c5633a1f2b46a42
    287dd6__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER2.vdomain.com\69844a271e6c5633a1f2
    b46a42287dd6__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER2.vdomain.com\69844a271e6c5633a1f2b46a42287dd6__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\3313935458e35b9b9759e08a15d251e6__0.xml
    
    Items deserialized: 20
    
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=1
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\3313935458e35b9b9759e08a15
    d251e6__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\3313935458e35b9b9759
    e08a15d251e6__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\3313935458e35b9b9759e08a15d251e6__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\4501e04eae4856059346949ff817c220__0.xml
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=1
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\4501e04eae4856059346949ff8
    17c220__0.xml
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\4501e04eae4856059346
    949ff817c220__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\4501e04eae4856059346949ff817c220__0.xml: succeeded: 20, failed: 0
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\5ad77443ad955a22a876749be66d5317__0.xml
    
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=20
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\5ad77443ad955a22a876749be6
    6d5317__0.xml
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\5ad77443ad955a22a876
    749be66d5317__0.xml
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\5ad77443ad955a22a876749be66d5317__0.xml: succeeded: 20, failed: 0
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\a11e27ae439a582288d4657eda86b565__0.xml
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=20
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\a11e27ae439a582288d4657eda
    86b565__0.xml
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\a11e27ae439a582288d4
    657eda86b565__0.xml
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\a11e27ae439a582288d4657eda86b565__0.xml: succeeded: 20, failed: 0
    All files have been imported into Storage Service for path: \\dc.vdomain.com\OcsFileStore\co1-WebSer
    vices-1\StorageService
    Importing files for: server.vdomain.com
    No files founds.
    Importing files for: server2.vdomain.com
    No files founds.
    Importing files for: server1.vdomain.com
    No files founds.
    Importing files for: server3.vdomain.com
    No files founds.
    Writing log: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\ImportStorageServiceData
    Log20120910_1609SS
    Tool has finished execution.
    >  C:\StorageService>

</div>

</div>

<div>

## <a name="lcssync"></a><span data-ttu-id="3736e-464">LCSSync</span><span class="sxs-lookup"><span data-stu-id="3736e-464">LCSSync</span></span>

<span data-ttu-id="3736e-465">A ferramenta LCSSync ajuda a implantar o software de comunicação do Lync Server 2013 em um ambiente de várias florestas.</span><span class="sxs-lookup"><span data-stu-id="3736e-465">The LCSSync tool helps to deploy Lync Server 2013 communications software in a multi-forest environment.</span></span> <span data-ttu-id="3736e-466">Essa ferramenta é usada para sincronizar usuários e grupos de florestas de usuários diferentes como um objeto de contato dos serviços de domínio Active Directory para uma floresta central na qual o Lync Server 2013 está instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-466">This tool is used to synchronize users and groups from different user forests as an Active Directory Domain Services contact object to a central forest where Lync Server 2013 is installed.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-467">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-467">Description</span></span>

<span data-ttu-id="3736e-468">O LCSSync usa os objetos de contato sincronizados dos serviços de domínio Active Directory na floresta central para permitir que os usuários do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3736e-468">LCSSync uses the synchronized Active Directory Domain Services contact objects in the central forest to enable users for Lync Server.</span></span> <span data-ttu-id="3736e-469">Para fornecer logon único, a conta de usuário principal deve ser mapeada para o objeto de contato dos serviços de domínio Active Directory na floresta central do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-469">To provide single sign-in, the primary user account must be mapped to the Active Directory Domain Services contact object in the central forest for Lync Server 2013.</span></span> <span data-ttu-id="3736e-470">Essa ferramenta ajuda a realizar esse mapeamento.</span><span class="sxs-lookup"><span data-stu-id="3736e-470">This tool helps perform that mapping.</span></span> <span data-ttu-id="3736e-471">Ela também fornece modelos para a criação de Agentes de Gerenciamento no Microsoft Identity Integration Server.</span><span class="sxs-lookup"><span data-stu-id="3736e-471">This tool provides templates for creating Management Agents in the Microsoft Identity Integration Server.</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-472">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-472">Summary</span></span>

<span data-ttu-id="3736e-473">A ferramenta LCSSync ajuda a implantar o Lync Server em um ambiente de várias florestas.</span><span class="sxs-lookup"><span data-stu-id="3736e-473">The LCSSync tool helps to deploy Lync Server in a multi-forest environment.</span></span>

</div>

</div>

<div>

## <a name="lookupuserconsole"></a><span data-ttu-id="3736e-474">LookupUserConsole</span><span class="sxs-lookup"><span data-stu-id="3736e-474">LookupUserConsole</span></span>

<span data-ttu-id="3736e-475">A ferramenta LookupUserConsole exibe informações de roteamento internas do Lync Server sobre usuários específicos.</span><span class="sxs-lookup"><span data-stu-id="3736e-475">The LookupUserConsole tool displays internal Lync Server routing information about specific users.</span></span> <span data-ttu-id="3736e-476">Essas informações poderão ser úteis para o suporte pessoal da Microsoft no diagnóstico de problemas de implantação e roteamento.</span><span class="sxs-lookup"><span data-stu-id="3736e-476">This information may be useful to Microsoft support personal in diagnosing deployment and routing problems.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-477">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-477">Description</span></span>

<span data-ttu-id="3736e-478">Executar LookupUserConsole.exe abrirá um prompt de comando que aceite endereços SIP e tentará exibir as informações internas de roteamento do Lync Server relacionadas a eles.</span><span class="sxs-lookup"><span data-stu-id="3736e-478">Executing LookupUserConsole.exe will open a command prompt that accepts SIP addresses and attempts to display internal Lync Server routing information relating them.</span></span> <span data-ttu-id="3736e-479">Digite **exit** para sair da ferramenta LookupUserConsole.</span><span class="sxs-lookup"><span data-stu-id="3736e-479">Type **exit** to quit the LookupUserConsole tool.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-480">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-480">Requirements</span></span>

<span data-ttu-id="3736e-481">Instale as ferramentas do Lync Server 2013, Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="3736e-481">Install the Lync Server 2013, Resource Kit Tools.</span></span> <span data-ttu-id="3736e-482">A ferramenta é executada em máquinas Unidas pelo domínio onde o Lync Server está instalado</span><span class="sxs-lookup"><span data-stu-id="3736e-482">The tool runs on domain-joined machines where Lync Server is installed</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-483">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-483">Examples</span></span>

<span data-ttu-id="3736e-484">C: \\ arquivos de programas \\ Microsoft Lync Server 2013 \\ reskit \>LookupUserConsole.exe</span><span class="sxs-lookup"><span data-stu-id="3736e-484">C:\\Program Files\\Microsoft Lync Server 2013\\ResKit\>LookupUserConsole.exe</span></span>

    > sip:john.doe@vdomain.com
    
      Execution time (ms):                            171.094
      Exeuction result:                               Success
      SIP URI:                                        sip:john.doe@vdomain.com
      User info:
        SID:                                          S-1-5-21-2831376166-29632525...    Display name:                                     John Doe
        Grouping ID:                                  00000000-0000-0000-0000-...
        Line URI:                                     <null>
        Policy assignment:                            TenantId={00000000--0000-000....
        SIP enabled:                                  True
        UC enabled:                                   False
        Tenant ID:                                    00000000-0000-0000-0000-...  Cluster info:
        Active cluster:                               pool0.vdomain.com
        Backup registrar cluster:                     <null>
        Deployment location:                          <null>
        Home Front-End FQDN:                          SERVER.vdomain.com
        Primary Registrar cluster:                    pool0.vdomain.com
        Remote Director external SIP FQDN:            <null>
        Remote Director internal SIP FQDN:            <null>
        Remote Director Web FQDN:                     <null>
        Routing group ID:                             4501e04e-ae48-5605-9346...
        Service tag ID:                               1266953005
        User Front-End resolved:                      True
        User in local forest:                         True
        User in remote forest:                        False
        User in split domain:                         False
        User-Services cluster:                        pool0.vdomain.com
    
    > sip:nouser@vdomain.com
    
      Execution time (ms):                            948.7574
      Exeuction result:                               UserDoesNotExist
    
    > exit

</div>

</div>

<div>

## <a name="msturnping"></a><span data-ttu-id="3736e-485">MsTurnPing</span><span class="sxs-lookup"><span data-stu-id="3736e-485">MsTurnPing</span></span>

<span data-ttu-id="3736e-486">A ferramenta MSTurnPing permite que um administrador do software de comunicação do Microsoft Lync Server 2013 Verifique o status dos servidores que estão executando a borda de áudio/vídeo e os serviços de autenticação de áudio/vídeo, bem como os servidores que estão executando os serviços de política de largura de banda na topologia.</span><span class="sxs-lookup"><span data-stu-id="3736e-486">The MSTurnPing tool allows an administrator of Microsoft Lync Server 2013 communications software to check the status of the servers running the Audio/Video Edge and Audio/Video Authentication services as well as the servers that are running Bandwidth Policy Services in the topology.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-487">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-487">Description</span></span>

<span data-ttu-id="3736e-488">A ferramenta MSTurnPing permite que um administrador do software de comunicação do Lync Server 2013 Verifique o status dos servidores que executam a borda de áudio/vídeo e os serviços de autenticação de áudio/vídeo, bem como os servidores que estão executando os serviços de política de largura de banda na topologia.</span><span class="sxs-lookup"><span data-stu-id="3736e-488">The MSTurnPing tool allows an administrator of Lync Server 2013 communications software to check the status of the servers running the Audio/Video Edge and Audio/Video Authentication services as well as the servers that are running Bandwidth Policy Services in the topology.</span></span>

<span data-ttu-id="3736e-489">A ferramenta permite ao administrador realizar os seguintes testes:</span><span class="sxs-lookup"><span data-stu-id="3736e-489">The tool allows the administrator to perform the following tests:</span></span>

1.  <span data-ttu-id="3736e-490">Teste do Servidor de Borda A/V: a ferramenta realiza testes em todos os Servidores de Borda A/V na topologia fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3736e-490">A/V Edge Server test: The tool performs tests against all A/V Edge Servers in the topology by doing the following:</span></span>
    
      - <span data-ttu-id="3736e-491">Verificar se o serviço de autenticação de áudio/vídeo do Lync Server foi iniciado e pode emitir credenciais adequadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-491">Verifying that the Lync Server Audio/Video Authentication service is started and can issue proper credentials.</span></span>
    
      - <span data-ttu-id="3736e-492">Verificando se o serviço de borda de áudio/vídeo do Lync Server foi iniciado e pode alocar os recursos na borda externa com êxito.</span><span class="sxs-lookup"><span data-stu-id="3736e-492">Verifying that the Lync Server Audio/Video Edge service is started and can allocate the resources on the external edge successfully.</span></span>

2.  <span data-ttu-id="3736e-493">Teste do Serviço da Política de Largura de Banda: a ferramenta realiza testes em todos os servidores que estejam executando os Serviços da Política de Largura de Banda na topologia fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3736e-493">Bandwidth Policy Service test: The tool performs tests against all the servers that are running the Bandwidth Policy Services in the topology by doing the following:</span></span>
    
      - <span data-ttu-id="3736e-494">Verificar se o serviço de política de largura de banda (autenticação) do Lync Server foi iniciado e pode emitir credenciais adequadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-494">Verifying that the Lync Server Bandwidth Policy Service (Authentication) is started and can issue proper credentials.</span></span>
    
      - <span data-ttu-id="3736e-495">Verificando se o serviço de política de largura de banda do Lync Server (básico) foi iniciado e pode executar a verificação de largura de banda com êxito.</span><span class="sxs-lookup"><span data-stu-id="3736e-495">Verifying that the Lync Server Bandwidth Policy Service (Core) is started and can perform the bandwidth check successfully.</span></span>

<span data-ttu-id="3736e-496">Essa ferramenta deve ser executada em um computador que faça parte da topologia e tenha o repositório local instalado. </span><span class="sxs-lookup"><span data-stu-id="3736e-496">This tool must be run from a computer that is part of the topology and has the local store installed.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-497">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-497">Output</span></span>

<span data-ttu-id="3736e-498">Essa ferramenta gera os resultados de cada uma das operações.</span><span class="sxs-lookup"><span data-stu-id="3736e-498">The tool outputs the results of each of the operations.</span></span>

  - <span data-ttu-id="3736e-499">Quando o teste **AudioVideoEdgeServer** é realizado, a ferramenta gera o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3736e-499">If the **AudioVideoEdgeServer** test is performed, the tool outputs are the following:</span></span>
    
      - <span data-ttu-id="3736e-500">Os resultados do teste dos computadores que fornecem o serviço de autenticação de áudio/vídeo do Lync Server na topologia</span><span class="sxs-lookup"><span data-stu-id="3736e-500">The test results of the computers that provide the Lync Server Audio/Video Authentication service in the topology</span></span>
    
      - <span data-ttu-id="3736e-501">Os resultados do teste dos computadores que fornecem o serviço de borda de áudio/vídeo do Lync Server na topologia</span><span class="sxs-lookup"><span data-stu-id="3736e-501">The test results of the computers that provide the Lync Server Audio/Video Edge service in the topology</span></span>

  - <span data-ttu-id="3736e-502">Quando o teste **BandwidthPolicyServer** é realizado, a ferramenta gera o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3736e-502">If the **BandwidthPolicyServer** test is performed, the tool outputs are the following:</span></span>
    
      - <span data-ttu-id="3736e-503">Os resultados do teste dos computadores que fornecem o serviço de política de largura de banda (autenticação) do Lync Server na topologia</span><span class="sxs-lookup"><span data-stu-id="3736e-503">The test results of the computers that provide the Lync Server Bandwidth Policy Service (Authentication) in the topology</span></span>
    
      - <span data-ttu-id="3736e-504">Os resultados do teste dos computadores que fornecem o serviço de política de largura de banda do Lync Server (básico) na topologia</span><span class="sxs-lookup"><span data-stu-id="3736e-504">The test results of the computers that provide the Lync Server Bandwidth Policy Service (Core) in the topology</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-505">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-505">Requirements</span></span>

  - <span data-ttu-id="3736e-506">Essa ferramenta deve ser executada em um computador que faça parte da topologia e tenha o repositório local instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-506">This tool must be run from a computer that is in the topology and that has the local store.</span></span>

  - <span data-ttu-id="3736e-507">A ferramenta deve ser executada por um administrador que tenha acesso ao repositório local.</span><span class="sxs-lookup"><span data-stu-id="3736e-507">The tool must be run as an administrator who has access to the local store.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-508">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-508">Examples</span></span>

<span data-ttu-id="3736e-509">Veja a seguir um exemplo de entrada de dados da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="3736e-509">The following is an example of the tool input.</span></span>

    MsTurnPing -ServerRole AudioVideoEdgeServer
    
    MsTurnPing -ServerRole BandwidthPolicyServer

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-510">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-510">Summary</span></span>

<span data-ttu-id="3736e-511">Essa ferramenta pode ser um recurso valioso para os administradores do Lync Server 2013 que desejam verificar o status dos servidores que estão executando os serviços de política de áudio/vídeo e largura de banda.</span><span class="sxs-lookup"><span data-stu-id="3736e-511">This tool can be a valuable resource to Lync Server 2013 administrators who want to check the status of the servers that are running audio/video and bandwidth policy services.</span></span>

</div>

</div>

<div>

## <a name="network-configuration-viewer"></a><span data-ttu-id="3736e-512">Visualizador da Configuração de Rede</span><span class="sxs-lookup"><span data-stu-id="3736e-512">Network Configuration Viewer</span></span>

<span data-ttu-id="3736e-513">O Visualizador de configuração de rede pode ser usado pelos administradores do software de comunicações do Microsoft Lync Server 2013 para exibir a topologia de rede do controle de admissão de chamadas (CAC) para uma empresa que é provisionada para permitir sessões de comunicação em tempo real, como chamadas de voz ou com vídeo com base na capacidade de largura de banda especificada.</span><span class="sxs-lookup"><span data-stu-id="3736e-513">Network Configuration Viewer can be used by Microsoft Lync Server 2013 communications software administrators to view call admission control (CAC) network topology for an enterprise that is provisioned to allow real-time communication sessions, such as voice or video calls based on specified bandwidth capacity.</span></span> <span data-ttu-id="3736e-514">Os administradores do Lync Server 2013 definem políticas do CAC, que são impostas pelos serviços de política de largura de banda que são instalados com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-514">Lync Server 2013 administrators define CAC policies, which are enforced by the Bandwidth Policy services that are installed with Lync Server 2013.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-515">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-515">Description</span></span>

<span data-ttu-id="3736e-516">O Visualizador da Configuração de Rede (NetworkConfigurationViewer.exe) permite aos administradores executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="3736e-516">Network Configuration Viewer (NetworkConfigurationViewer.exe) allows administrators to perform the following tasks:</span></span>

  - <span data-ttu-id="3736e-517">Carregar e exibir a topologia de rede do CAC a partir de uma implantação do Lync Server 2013 em um formato gráfico.</span><span class="sxs-lookup"><span data-stu-id="3736e-517">Load and view CAC network topology from a Lync Server 2013 deployment in a graphical format.</span></span>

  - <span data-ttu-id="3736e-518">Carregar e exibir a topologia de rede do CAC de um arquivo de log do Servidor da Política de Largura de Banda em um formato gráfico.</span><span class="sxs-lookup"><span data-stu-id="3736e-518">Load and view CAC network topology from a Bandwidth Policy Server log file in a graphical format.</span></span>

  - <span data-ttu-id="3736e-519">Salvar e armazenar no disco a topologia de rede do CAC no formato XML.</span><span class="sxs-lookup"><span data-stu-id="3736e-519">Save and store CAC network topology in an XML format on the disk.</span></span>

  - <span data-ttu-id="3736e-520">Salvar e armazenar o diagrama da topologia de rede do CAC no formato JPG ou BMP.</span><span class="sxs-lookup"><span data-stu-id="3736e-520">Save and store CAC network topology diagram in JPG or BMP format.</span></span>

  - <span data-ttu-id="3736e-521">Exibir os dados de configuração da topologia de rede do CAC.</span><span class="sxs-lookup"><span data-stu-id="3736e-521">View CAC network topology configuration data.</span></span>

  - <span data-ttu-id="3736e-522">Exibir a topologia de rede do CAC em modo de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="3736e-522">View CAC network topology in a tree-view style.</span></span>

  - <span data-ttu-id="3736e-523">Definir conectores personalizados para os links da topologia de rede do CAC (por exemplo, links de site para região, região para região e site para site).</span><span class="sxs-lookup"><span data-stu-id="3736e-523">Define custom connectors for CAC network topology links (for example, site-to-region, region-to-region, and site-to-site links).</span></span>

  - <span data-ttu-id="3736e-524">Exibir as informações do site de topologia de rede do CAC, informações da região e links de rede e políticas de largura de banda provisionadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-524">View CAC network topology site information, region Information, and provisioned bandwidth policies and network links.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-525">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-525">Purpose</span></span>

<span data-ttu-id="3736e-526">Exibir os links de topologia de rede do CAC da empresa em uma interface gráfica.</span><span class="sxs-lookup"><span data-stu-id="3736e-526">View enterprise CAC network topology links in a graphical interface.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-527">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-527">Examples</span></span>

<span data-ttu-id="3736e-528">**Carregar e exibir a topologia de rede do CAC a partir de uma implantação do Lync Server 2013 em um formato gráfico:** Os administradores do Lync Server 2013 podem carregar e exibir a configuração de topologia de rede do CAC em qualquer computador com o Lync Server 2013 usando a opção **baixar a configuração de rede** , conforme mostrado na figura abaixo.</span><span class="sxs-lookup"><span data-stu-id="3736e-528">**Load and view CAC network topology from a Lync Server 2013 deployment in a graphical format:** Lync Server 2013 administrators can load and view CAC network topology configuration on any Lync Server 2013 computer by using the **Download Network Configuration** option as shown in the figure below.</span></span> <span data-ttu-id="3736e-529">A ferramenta não fará o download ou exibirá essa configuração quando implantada em um computador que não tenha conectividade com o repositório de configuração do Lync.</span><span class="sxs-lookup"><span data-stu-id="3736e-529">The tool will fail to download or view such a configuration when deployed on a computer that does not have connectivity to the Lync configuration store.</span></span>

<span data-ttu-id="3736e-530">![Baixando a configuração de rede.](images/JJ945604.8d126d3f-2545-4f13-a244-974f09614982(OCS.15).jpg "Baixando a configuração de rede.")</span><span class="sxs-lookup"><span data-stu-id="3736e-530">![Downloading the network configuration.](images/JJ945604.8d126d3f-2545-4f13-a244-974f09614982(OCS.15).jpg "Downloading the network configuration.")</span></span>

<span data-ttu-id="3736e-531">**Carregar e exibir a topologia de rede do CAC de um arquivo de log do servidor de políticas de largura de banda em um formato gráfico:** Servidores de política de largura de banda do Lync Server 2013 salve a topologia de rede do CAC como parte do mecanismo de log no local de compartilhamento de arquivos do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-531">**Load and View CAC network topology from a Bandwidth Policy server log file in a graphical format:** Lync Server 2013 Bandwidth Policy servers save the CAC network topology as a part of the logging mechanism under the Lync Server 2013 file share location.</span></span> <span data-ttu-id="3736e-532">Os administradores do Lync Server podem exibir esse arquivo em um formato gráfico usando a opção **abrir a configuração de rede** , como mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-532">Lync Server administrators can view such a file in a graphical format by using the **Open Network Configuration** option as shown below.</span></span>

<span data-ttu-id="3736e-533">![Abrir um arquivo de log do servidor de políticas de largura de banda.](images/JJ945604.3e503e92-aacb-4921-a8d2-23f860fe2df6(OCS.15).jpg "Abrir um arquivo de log do servidor de políticas de largura de banda.")</span><span class="sxs-lookup"><span data-stu-id="3736e-533">![Opening a Bandwidth Policy Server log file.](images/JJ945604.3e503e92-aacb-4921-a8d2-23f860fe2df6(OCS.15).jpg "Opening a Bandwidth Policy Server log file.")</span></span>

<span data-ttu-id="3736e-534">Salvar e armazenar a topologia de rede do CAC em um formato XML no disco: os administradores do Lync Server 2013 podem salvar o arquivo de configuração de topologia de rede do CAC em um formato XML usando a opção **salvar uma cópia da configuração de rede** , conforme mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-534">Save and store CAC network topology in an XML format on the disk: Lync Server 2013 administrators can save the CAC network topology configuration file in an XML format by using the **Save a copy of Network Configuration** option as shown below.</span></span> <span data-ttu-id="3736e-535">O arquivo de configuração salvo pode ser usado offline para fins de exibição gráfica.</span><span class="sxs-lookup"><span data-stu-id="3736e-535">The saved configuration file can then be used offline for graphical viewing purposes.</span></span>

<span data-ttu-id="3736e-536">![Salvando a configuração de rede como um arquivo XML.](images/JJ945604.6eeef3b0-78b5-4ee6-8d94-1a4ddf3d8676(OCS.15).jpg "Salvando a configuração de rede como um arquivo XML.")</span><span class="sxs-lookup"><span data-stu-id="3736e-536">![Saving the network configuration as an XML file.](images/JJ945604.6eeef3b0-78b5-4ee6-8d94-1a4ddf3d8676(OCS.15).jpg "Saving the network configuration as an XML file.")</span></span>

<span data-ttu-id="3736e-537">Salvar e armazenar o diagrama de topologia de rede do CAC no formato JPG ou BMP: os administradores do Lync Server 2013 podem salvar a configuração de topologia de rede do CAC em um formato gráfico (formatos de arquivo JPG e BMP) usando a opção **salvar diagrama de configuração de rede como imagem** , conforme mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-537">Save and Store CAC network topology diagram in JPG or BMP format: Lync Server 2013 administrators can save the CAC network topology configuration in a graphical format (JPG and BMP file formats) by using the **Save Network Configuration diagram as picture** option as shown below.</span></span>

<span data-ttu-id="3736e-538">![Salvando a configuração de rede como uma imagem.](images/JJ945604.145a6fb9-58b1-46b1-bbd5-a661ceba07b4(OCS.15).jpg "Salvando a configuração de rede como uma imagem.")</span><span class="sxs-lookup"><span data-stu-id="3736e-538">![Saving the network configuration as a picture.](images/JJ945604.145a6fb9-58b1-46b1-bbd5-a661ceba07b4(OCS.15).jpg "Saving the network configuration as a picture.")</span></span>

<span data-ttu-id="3736e-539">**Exibir dados de configuração de topologia de rede do CAC:** Os administradores do Lync Server 2013 podem exibir dados de configuração de rede relacionados, como regiões de rede, sites de rede, perfis de largura de banda e endereços IP de sub-rede de sites em um formato de texto usando a opção Exibir dados de configuração de rede, conforme mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-539">**View CAC network topology configuration data:** Lync Server 2013 administrators can view related network configuration data such as network regions, network sites, bandwidth profiles, and site subnet IP addresses in a textual format by using the View Network Configuration data option as shown below.</span></span>

<span data-ttu-id="3736e-540">![Exibir dados de configuração de rede.](images/JJ945604.b72a4c21-a042-4d91-bf96-fcb396af0679(OCS.15).jpg "Exibir dados de configuração de rede.")</span><span class="sxs-lookup"><span data-stu-id="3736e-540">![Viewing network configuration data.](images/JJ945604.b72a4c21-a042-4d91-bf96-fcb396af0679(OCS.15).jpg "Viewing network configuration data.")</span></span>

<span data-ttu-id="3736e-541">**Exiba a topologia de rede do CAC em um estilo de exibição de árvore:** Os administradores do Lync Server 2013 podem exibir dados de configuração de rede relacionados em um estilo de exibição de árvore gráfica usando o painel de controle no lado esquerdo da janela da ferramenta, como mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="3736e-541">**View CAC network topology in a tree-view style:** Lync Server 2013 administrators can view related network configuration data in a graphical tree view style by using the control panel on the left side of the tool window as shown below.</span></span>

<span data-ttu-id="3736e-542">![Exibir dados de configuração de rede em um modo de exibição de árvore.](images/JJ945604.4d924ac9-fd96-430f-b211-ee35b7ef9a23(OCS.15).jpg "Exibir dados de configuração de rede em um modo de exibição de árvore.")</span><span class="sxs-lookup"><span data-stu-id="3736e-542">![Viewing network configuration data in a tree-view.](images/JJ945604.4d924ac9-fd96-430f-b211-ee35b7ef9a23(OCS.15).jpg "Viewing network configuration data in a tree-view.")</span></span>

<span data-ttu-id="3736e-543">**Definir conectores personalizados para links de topologia de rede do CAC (como links de site para região, região para região e links entre sites):** Os administradores do Lync Server 2013 podem definir conectores gráficos personalizados para o WAN links de configuração de rede do CAC usando a opção configurações, conforme mostrado a seguir.</span><span class="sxs-lookup"><span data-stu-id="3736e-543">**Define custom connectors for CAC network topology links (such as site-to-region, region-to-region, and site-to-site links):** Lync Server 2013 administrators can define custom graphical connectors for CAC network configuration WAN links by using the Settings option as shown below.</span></span> <span data-ttu-id="3736e-544">Isso ajuda a diferenciar entre os vários tipos de links de rede provisionados na configuração da rede.</span><span class="sxs-lookup"><span data-stu-id="3736e-544">This helps differentiate between various types of network links that are provisioned in the network configuration.</span></span>

<span data-ttu-id="3736e-545">![Definir conectores personalizados para a topologia de rede do CAC](images/JJ945604.b20bea67-c8e1-453e-b1dd-e2aa17b62566(OCS.15).jpg "Definir conectores personalizados para a topologia de rede do CAC")</span><span class="sxs-lookup"><span data-stu-id="3736e-545">![Define custom connectors for CAC network topology](images/JJ945604.b20bea67-c8e1-453e-b1dd-e2aa17b62566(OCS.15).jpg "Define custom connectors for CAC network topology")</span></span>

<span data-ttu-id="3736e-546">**Exibir informações do site de topologia de rede do CAC, informações de região e políticas de largura de banda provisionadas:** Os administradores do Lync Server 2013 podem exibir informações de região de rede do CAC, informações do site e informações de provisionamento de largura de banda do CAC relacionadas usando as opções mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="3736e-546">**View CAC network topology site information, region information, and provisioned bandwidth policies:** Lync Server 2013 administrators can view related CAC network region information, site information, and CAC bandwidth provisioning information by using options shown below.</span></span> <span data-ttu-id="3736e-547">Por exemplo, clique em **Informações** em uma região da rede ou objeto do site da rede.</span><span class="sxs-lookup"><span data-stu-id="3736e-547">(For example, click **Info** in a network region or network site object.)</span></span>

<span data-ttu-id="3736e-548">![Definir conectores personalizados para a sua rede.](images/JJ945604.26262c75-4342-41c3-bc98-1793aa6a7713(OCS.15).jpg "Definir conectores personalizados para a sua rede.")</span><span class="sxs-lookup"><span data-stu-id="3736e-548">![Defining custom connectors for your network.](images/JJ945604.26262c75-4342-41c3-bc98-1793aa6a7713(OCS.15).jpg "Defining custom connectors for your network.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-549">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-549">Summary</span></span>

<span data-ttu-id="3736e-550">Essa ferramenta pode ser um recurso valioso para os administradores do Lync Server 2013 que desejam exibir a topologia de rede do CAC para a implantação em um formato gráfico.</span><span class="sxs-lookup"><span data-stu-id="3736e-550">This tool can be a valuable resource to Lync Server 2013 administrators who would like to view CAC network topology for their deployment in a graphical format.</span></span>

</div>

</div>

<div>

## <a name="response-group-agent-live"></a><span data-ttu-id="3736e-551">Agente do Grupo de Resposta em Tempo Real</span><span class="sxs-lookup"><span data-stu-id="3736e-551">Response Group Agent Live</span></span>

<span data-ttu-id="3736e-552">O aplicativo Grupo de Resposta proporciona aos agentes a capacidade de acessar informações úteis em tempo real usando o serviço Web interno.</span><span class="sxs-lookup"><span data-stu-id="3736e-552">The Response Group application gives agents the ability to access useful real-time information using its built-in Web service.</span></span> <span data-ttu-id="3736e-553">Infelizmente, nenhuma exibição gráfica desses dados está disponível fora do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3736e-553">Unfortunately, no graphical view of this data is available outside the application.</span></span> <span data-ttu-id="3736e-554">A ferramenta agente do grupo de resposta do Live Resource Kit resolve esse problema fornecendo uma maneira simples e gráfica de acessar essas informações, aprimoradas com informações de software de comunicação do Microsoft Lync 2013, como a presença de outros agentes.</span><span class="sxs-lookup"><span data-stu-id="3736e-554">The Response Group Agent Live Resource Kit tool solves this issue by providing a simple and graphical way to access this information, enhanced with real-time Microsoft Lync 2013 communications software information such as the presence of other agents.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-555">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-555">Description</span></span>

<span data-ttu-id="3736e-556">O Agente do Grupo de Resposta em Tempo Real é um aplicativo do Windows que fornece a funcionalidade de entrar e sair e algumas informações em tempo real (como membros do grupo e número atual de chamadas) a agentes do Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="3736e-556">Response Group Agent Live is a Windows application that provides sign-in and sign-out functionality and some real-time information (such as group membership and current number of calls) to Response Group agents.</span></span> <span data-ttu-id="3736e-557">Ele deve ser uma versão aprimorada da página de grupos de agente (acessível do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-557">It is meant to be an enhanced version of the Agent Groups page (accessible from Lync 2013.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-558">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-558">Purpose</span></span>

<span data-ttu-id="3736e-p165">O aplicativo Grupo de Resposta enfileira as chamadas recebidas e, em seguida, as encaminha para os grupos de agentes. Para tomar decisões conscientes sobre quais chamadas devem ser atendidas, os agentes podem acessar informações em tempo real sobre os grupos de agentes, como quais outros agentes estão disponíveis e quantas chamadas estão em espera em cada fila. Essas informações, inicialmente acessíveis somente por meio do serviço de Grupo de Resposta, são disponibilizadas de forma intuitiva pelo Agente do Grupo de Resposta em Tempo Real.</span><span class="sxs-lookup"><span data-stu-id="3736e-p165">The Response Group application queues incoming calls, and then routes them to agent groups. To make informed decisions about which calls to service, agents can access real-time information about their agent groups, such as what other agents are available and how many calls are waiting in each queue. This information, initially accessible only through the Response Group service, is made available in an intuitive way by Response Group Agent Live.</span></span>

<div>

## <a name="features"></a><span data-ttu-id="3736e-562">Recursos</span><span class="sxs-lookup"><span data-stu-id="3736e-562">Features</span></span>

<span data-ttu-id="3736e-563">A ferramenta de tempo de agente de grupo de resposta é criada no serviço de grupo de resposta e no SDK do Microsoft Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-563">The Response Group Agent Live tool is built on the Response Group service and the Microsoft Lync 2013 SDK.</span></span> <span data-ttu-id="3736e-564">Ela fornece aos agentes do Grupo de Resposta as informações e os recursos disponíveis no serviço de Grupo de Resposta (como membros do grupo, presença de outros agentes e número de chamadas em espera).</span><span class="sxs-lookup"><span data-stu-id="3736e-564">It provides Response Group agents the information and capabilities that are available from the Response Group service (such as group membership, presence of other agents, and number of waiting calls).</span></span>

<span data-ttu-id="3736e-565">A figura abaixo ilustra a interface principal do Agente do Grupo de Resposta em Tempo Real.</span><span class="sxs-lookup"><span data-stu-id="3736e-565">The figure below illustrates the main interface of Response Group Agent Live.</span></span>

<span data-ttu-id="3736e-566">![A ferramenta de tempo de agente do grupo de resposta.](images/JJ945604.63cb0374-a6ef-4a59-b60e-bec86a880d09(OCS.15).jpg "A ferramenta de tempo de agente do grupo de resposta.")</span><span class="sxs-lookup"><span data-stu-id="3736e-566">![The Response Group Agent Live tool.](images/JJ945604.63cb0374-a6ef-4a59-b60e-bec86a880d09(OCS.15).jpg "The Response Group Agent Live tool.")</span></span>

<span data-ttu-id="3736e-567">Os seguintes três recursos principais estão disponíveis para os agentes do Agente do Grupo de Resposta em Tempo Real:</span><span class="sxs-lookup"><span data-stu-id="3736e-567">The following three main features are available for agents in Response Group Agent Live:</span></span>

  - <span data-ttu-id="3736e-568">**Entrada/saída:** Ao contrário da página grupos de agente (acessível do Lync 2013), o agente de resposta em tempo real permite que somente os agentes entrem em todos os grupos de agente ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="3736e-568">**Sign-in/out:** Contrary to the Agent Groups page (accessible from Lync 2013), Response Group Agent Live allows only agents to sign-in or out of all agent groups at once.</span></span> <span data-ttu-id="3736e-569">Este aplicativo fornece três maneiras rápidas para os agentes entrarem ou sairem:</span><span class="sxs-lookup"><span data-stu-id="3736e-569">This application provides three quick ways for agents to sign in or out:</span></span>
    
      - <span data-ttu-id="3736e-570">Clicar nos botões Entrar/sair (verde e vermelho) no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3736e-570">Click the Sign-in/out (green and red) buttons within the application.</span></span>
    
      - <span data-ttu-id="3736e-571">Clicar com o botão direito do mouse no ícone de bandeja do sistema e selecionar entrar ou sair.</span><span class="sxs-lookup"><span data-stu-id="3736e-571">Right-click the system tray icon, and select sign in or sign out.</span></span>
    
      - <span data-ttu-id="3736e-572">Usar os atalhos do teclado configuráveis.</span><span class="sxs-lookup"><span data-stu-id="3736e-572">Using configurable keyboard shortcuts.</span></span>

  - <span data-ttu-id="3736e-573">**Associação a um grupo:** Quando um grupo de agente é selecionado, o agente do grupo de resposta Live exibe a lista de agentes neste grupo no painel direito.</span><span class="sxs-lookup"><span data-stu-id="3736e-573">**Group membership:** When an agent group is selected, Response Group Agent Live displays the list of agents in this group in the right pane.</span></span> <span data-ttu-id="3736e-574">Se o Lync 2013 estiver em execução no mesmo computador que este aplicativo, as informações de presença e o cartão de visita serão exibidos no agente do grupo de resposta ao vivo.</span><span class="sxs-lookup"><span data-stu-id="3736e-574">If Lync 2013 is running on the same computer as this application, presence information and the contact card are displayed in the Response Group Agent Live.</span></span> <span data-ttu-id="3736e-575">Os agentes podem enviar uma mensagem instantânea ou ligar para outros agentes diretamente.</span><span class="sxs-lookup"><span data-stu-id="3736e-575">Agents can send an IM or call other agents directly from there.</span></span>

  - <span data-ttu-id="3736e-p169">**Estatísticas em tempo real:** o Agente do Grupo de Resposta em Tempo Real fornece estatísticas em tempo real de todos os grupos de agentes. A frequência de atualização é de um minuto. Quando uma chamada é atendida por um Grupo de Resposta, um indicador visual é adicionado ao lado do nome do grupo com o número atual de chamadas em fila. Pausar o ponteiro sobre um grupo também exibe o tempo de espera mais longo.</span><span class="sxs-lookup"><span data-stu-id="3736e-p169">**Real-time statistics:** Response Group Agent Live provides real-time statistics for all agent groups. The update frequency is one minute. When a call is answered by a Response Group, a visual indicator is added next to the group name with the current number of queued calls. Pausing the pointer over a group also displays the longest waiting time.</span></span>

</div>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-580">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-580">Requirements</span></span>

<span data-ttu-id="3736e-581">O Agente do Grupo de Resposta em Tempo Real requer o .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="3736e-581">Response Group Agent Live requires the .NET Framework 4.0.</span></span> <span data-ttu-id="3736e-582">Além disso, para tirar proveito dos recursos de presença e cartão de contato, o Lync 2013 deve ser instalado localmente (e estar em execução).</span><span class="sxs-lookup"><span data-stu-id="3736e-582">In addition, to take advantage of the presence and contact card features, Lync 2013 must be installed locally (and be running).</span></span>

<div>

## <a name="configuration"></a><span data-ttu-id="3736e-583">Configuração</span><span class="sxs-lookup"><span data-stu-id="3736e-583">Configuration</span></span>

<span data-ttu-id="3736e-p171">O Agente do Grupo de Resposta em Tempo Real pode ser personalizado de acordo com as preferências individuais usando a caixa de diálogo Opções no aplicativo. Além disso, o administrador pode definir o endereço de host padrão editando diretamente a propriedade defaultHostAddress do arquivo RGAgentLive.exe.config.</span><span class="sxs-lookup"><span data-stu-id="3736e-p171">Response Group Agent Live can be customized to individual preferences by using the Options dialog box in the application. In addition, the administrator can define the default host address by editing directly the defaultHostAddress property of the RGAgentLive.exe.config file.</span></span>

<span data-ttu-id="3736e-p172">A figura abaixo ilustra a caixa de diálogo Opções que os agentes podem usar para configurar as teclas de atalho e o endereço de host. Essa caixa de diálogo é acessada clicando no botão Opções no canto superior direito da interface principal.</span><span class="sxs-lookup"><span data-stu-id="3736e-p172">The figure below illustrates the Options dialog box that agents can use to configure the host address and shortcut keys. This dialog is accessed by clicking the Options button on the top right of the main interface.</span></span>

<span data-ttu-id="3736e-588">![A caixa de diálogo opções de agente do grupo de resposta em tempo real.](images/JJ945604.3cc15e29-8699-45ab-90c3-e1565fa6ebf6(OCS.15).jpg "A caixa de diálogo opções de agente do grupo de resposta em tempo real.")</span><span class="sxs-lookup"><span data-stu-id="3736e-588">![The Response Group Agent Live Options dialog box.](images/JJ945604.3cc15e29-8699-45ab-90c3-e1565fa6ebf6(OCS.15).jpg "The Response Group Agent Live Options dialog box.")</span></span>

<span data-ttu-id="3736e-589">As três configurações diferentes a seguir podem ser personalizadas na configuração do Agente do Grupo de Resposta em Tempo Real:</span><span class="sxs-lookup"><span data-stu-id="3736e-589">The following three different settings can be customized in the Response Group Agent Live configuration:</span></span>

  - <span data-ttu-id="3736e-p173">Endereço do host: normalmente este é o FQDN do pool da Web que pertence ao pool da página inicial do agente. O endereço de serviço exato do Grupo de Resposta é automaticamente derivado em segundo plano dessa informação (anexado no caminho à direita depois do host).</span><span class="sxs-lookup"><span data-stu-id="3736e-p173">Host address: This is typically the web pool FQDN belonging to the agent’s home pool. The exact Response Group service address is automatically derived in the background from this information (by appending the right path after the host).</span></span>

  - <span data-ttu-id="3736e-p174">Atalhos: os atalhos exatos para entrar/sair podem ser personalizados. A única limitação é que ambos os atalhos devem conter a tecla do logotipo do Windows (além de pelo menos outra tecla).</span><span class="sxs-lookup"><span data-stu-id="3736e-p174">Shortcuts: The exact shortcuts to sign-in/out can be customized. The only limitation is that both shortcuts must contain the “Windows Logo” key (in addition to at least another key).</span></span>

  - <span data-ttu-id="3736e-594">Iniciar com o Windows: o aplicativo pode ser configurado para ser iniciado automaticamente com o Windows.</span><span class="sxs-lookup"><span data-stu-id="3736e-594">Start with Windows: The application can be configured to start automatically with Windows.</span></span>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-595">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-595">Examples</span></span>

<span data-ttu-id="3736e-596">A figura abaixo ilustra como chamar ou enviar uma mensagem instantânea para outro agente clicando com o botão direito do mouse no contato no painel à direita.</span><span class="sxs-lookup"><span data-stu-id="3736e-596">The figure below illustrates how to call or send an IM to another agent by right-clicking the contact in the right pane.</span></span>

<span data-ttu-id="3736e-597">![Fazer uma chamada ou enviar uma mensagem instantânea.](images/JJ945604.009cebe0-5a93-4745-89c3-8a16c7c13009(OCS.15).jpg "Fazer uma chamada ou enviar uma mensagem instantânea.")</span><span class="sxs-lookup"><span data-stu-id="3736e-597">![Making a call or sending an IM.](images/JJ945604.009cebe0-5a93-4745-89c3-8a16c7c13009(OCS.15).jpg "Making a call or sending an IM.")</span></span>

<span data-ttu-id="3736e-598">A figura abaixo ilustra como o Agente do Grupo de Resposta em Tempo Real exibe o número atual de chamadas na fila e o tempo de espera mais longo entre todas as chamadas de entrada.</span><span class="sxs-lookup"><span data-stu-id="3736e-598">The figure below illustrates how Response Group Agent Live displays the current number of calls in the queue and the longest waiting time among all these incoming calls.</span></span>

<span data-ttu-id="3736e-599">![Exibir informações da fila.](images/JJ945604.131d7f79-b7ed-41f5-a9da-ffc556e31037(OCS.15).jpg "Exibir informações da fila.")</span><span class="sxs-lookup"><span data-stu-id="3736e-599">![Viewing queue information.](images/JJ945604.131d7f79-b7ed-41f5-a9da-ffc556e31037(OCS.15).jpg "Viewing queue information.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-600">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-600">Summary</span></span>

<span data-ttu-id="3736e-601">Ações rápidas de entrada e saída, associação a um grupo e estatísticas básicas em tempo real são recursos interessantes do Agente do Grupo de Resposta que estão disponíveis apenas fora do aplicativo do serviço de Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="3736e-601">Fast sign-in and sign-out, group membership, and basic real-time statistics are interesting Response Group agent features that are only available outside the application from the Response Group service.</span></span> <span data-ttu-id="3736e-602">Com a ferramenta de agente de resposta do Live Resource Kit, os administradores do Lync podem fornecer seus agentes com um aplicativo do Windows que permita executar tarefas de forma mais rápida e gráfica.</span><span class="sxs-lookup"><span data-stu-id="3736e-602">With the Response Group Agent Live Resource Kit tool, Lync administrators can provide their agents with a Windows application that allows them to perform tasks in a faster and graphical way.</span></span>

</div>

</div>

<div>

## <a name="sefautil"></a><span data-ttu-id="3736e-603">SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="3736e-603">SEFAUtil</span></span>

<span data-ttu-id="3736e-604">SEFAUtil (ativação de recurso de extensão secundária) é uma ferramenta de linha de comando que permite aos administradores do software de comunicações do Microsoft Lync Server 2013 e dos agentes de helpdesk configurar o recurso de direcionamento de chamada, o encaminhamento de chamadas, o toque simultâneo, as configurações de chamada de equipe e o recebimento de chamadas em grupo em nome de um usuário do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-604">SEFAUtil (secondary extension feature activation) is a command-line tool that enables Microsoft Lync Server 2013 communications software administrators and helpdesk agents to configure delegate-ringing, call-forwarding, simultaneous ringing, team-call settings and group call pickup on behalf of a Lync Server 2013 user.</span></span> <span data-ttu-id="3736e-605">A ferramenta também permite que os administradores consultem as configurações de direcionamento de chamadas publicadas para um usuário específico. A ferramenta SEFAUtil permite que o administrador habilite/desabilite/modifique o encaminhamento de chamadas ou toque simultaneamente em nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-605">The tool also allows administrators to query the call-routing settings that are published for a particular user.The SEFAUtil tool allows the administrator to enable/disable/modify call forwarding or simultaneously ringing on behalf of the user.</span></span> <span data-ttu-id="3736e-606">O administrador pode especificar o destino (na forma de um URI SIP) ou usar um destino que já foi publicado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-606">The administrator can specify the target (in the form of a SIP URI) or use a target that has already been published by the user.</span></span> <span data-ttu-id="3736e-607">Essa ferramenta também permite que os administradores adicionem ou removam representantes ou membros do grupo de chamada de equipe em nome do usuário. Essa ferramenta foi criada com o Microsoft Unified Communications Managed API (UCMA) 3,0 e requer que os administradores criem um aplicativo confiável no repositório de gerenciamento central para SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="3736e-607">This tool also allows administrators to add or remove delegates or team-call group members on behalf of the user.This tool is built on Microsoft Unified Communications Managed API (UCMA) 3.0 and requires that administrators create a trusted application in the Central Management store for SEFAUtil</span></span>

<span data-ttu-id="3736e-608">SEFAUtil (ativação de recurso de extensão secundária) permite que os administradores do Lync Server 2013 e do helpdesk configurem o recurso de toque, o encaminhamento de chamadas, o toque simultâneo, as configurações de chamada de equipe e a retirada de chamadas em grupo em nome de um usuário do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-608">SEFAUtil (secondary extension feature activation) enables Lync Server 2013 administrators and helpdesk agents to configure delegate-ringing, call-forwarding, simultaneous ringing, team-call settings and group call pickup on behalf of a Lync Server 2013 user.</span></span> <span data-ttu-id="3736e-609">Essa ferramenta também permite aos administradores consultar as configurações de roteamento de chamadas publicadas para determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-609">This tool also allows administrators to query the call-routing settings that are published for a particular user.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-610">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-610">Description</span></span>

<span data-ttu-id="3736e-611">A versão atual de SEFAUtil é apenas uma ferramenta de linha de comando; não há nenhum suporte para interface gráfica do usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-611">The current version of SEFAUtil is only a command-line tool; there is no supporting graphical user interface.</span></span> <span data-ttu-id="3736e-612">Esta ferramenta se baseia na API gerenciada de comunicação unificada da Microsoft (UCMA) 3,0.</span><span class="sxs-lookup"><span data-stu-id="3736e-612">This tool is based on Microsoft Unified Communications Managed API (UCMA) 3.0.</span></span> <span data-ttu-id="3736e-613">Os recursos dessa ferramenta permitem a administradores e agentes de assistência técnica realizar as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="3736e-613">The features in this tool allow administrators and helpdesk agents to do the following:</span></span>

  - <span data-ttu-id="3736e-614">Exibir todas as configurações de roteamento de chamadas de um usuário (inclui encaminhamento de chamadas, delegação, toque simultâneo, chamada de equipe e recebimento de chamada em grupo).</span><span class="sxs-lookup"><span data-stu-id="3736e-614">View all call routing settings for a user (includes call-forwarding, delegation, simultaneous ringing, team-call and group call pickup)</span></span>

  - <span data-ttu-id="3736e-615">Habilitar/desabilitar/modificar a configuração de encaminhamento de chamadas (inclui temporizador sem resposta e de destino).</span><span class="sxs-lookup"><span data-stu-id="3736e-615">Enable/disable/modify call-forwarding setting (includes destination and no-answer timer)</span></span>

  - <span data-ttu-id="3736e-616">Habilitar/desabilitar/modificar configurações imediatas de encaminhamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-616">Enable/disable/modify call-forwarding immediate configurations</span></span>

  - <span data-ttu-id="3736e-617">Habilitar/desabilitar/modificar configurações de delegação.</span><span class="sxs-lookup"><span data-stu-id="3736e-617">Enable/disable/modify delegation settings</span></span>

  - <span data-ttu-id="3736e-618">Habilitar/desabilitar/modificar configurações do grupo de chamada de equipe.</span><span class="sxs-lookup"><span data-stu-id="3736e-618">Enable/disable/modify team-call group settings</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3736e-619">Novo na ferramenta SEFAUtil do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-619">New in Lync Server 2013 SEFAUtil tool</span></span>

    
    </div>

  - <span data-ttu-id="3736e-620">Habilitar/desabilitar/modificar configurações de toque simultâneo (inclui destino).</span><span class="sxs-lookup"><span data-stu-id="3736e-620">Enable/disable/modify simultaneous ringing settings (includes destination)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3736e-621">Novo na ferramenta SEFAUtil do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-621">New in Lync Server 2013 SEFAUtil tool</span></span>

    
    </div>

  - <span data-ttu-id="3736e-622">Habilitar/desabilitar/modificar configurações de recebimento de chamada em grupo.</span><span class="sxs-lookup"><span data-stu-id="3736e-622">Enable/disable/modify group call pickup settings</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="3736e-623">Novo na ferramenta SEFAUtil do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-623">New in Lync Server 2013 SEFAUtil tool</span></span>

    
    </div>

<span data-ttu-id="3736e-624">Esta ferramenta apresenta as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="3736e-624">This tool has the following limitations:</span></span>

  - <span data-ttu-id="3736e-625">Com suporte somente para usuários hospedados em um pool do Lync Server</span><span class="sxs-lookup"><span data-stu-id="3736e-625">Supported only for users homed in a Lync Server pool</span></span>

  - <span data-ttu-id="3736e-626">Não há suporte para edição em massa de configurações de roteamento de chamadas para diversos usuários.</span><span class="sxs-lookup"><span data-stu-id="3736e-626">Bulk-edit of call routing settings for several users is not supported</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-627">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-627">Output</span></span>

<span data-ttu-id="3736e-p179">A versão atual desta ferramenta fornece resultados apenas na janela Prompt de Comando. Para ver detalhes, consulte a seção Exemplos mais adiante neste documento.</span><span class="sxs-lookup"><span data-stu-id="3736e-p179">The current version of this tool provides output only in the Command Prompt window. For details, see the Examples section later in this document.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-630">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-630">Purpose</span></span>

<span data-ttu-id="3736e-631">Veja a seguir alguns dos principais cenários onde esta ferramenta pode ser usada:</span><span class="sxs-lookup"><span data-stu-id="3736e-631">Following are some of the key scenarios where this tool may be used:</span></span>

  - <span data-ttu-id="3736e-632">Bob é um executivo e foi movido para a telefonia do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3736e-632">Bob is an executive and has been moved to Lync Server telephony.</span></span> <span data-ttu-id="3736e-633">Ele já tem delegação em seu sistema PBX existente.</span><span class="sxs-lookup"><span data-stu-id="3736e-633">He has delegation on his existing PBX system.</span></span> <span data-ttu-id="3736e-634">Como parte da mudança para o Lync, o administrador é capaz de configurar o roteamento de Bob para refletir sua configuração de delegação já existente.</span><span class="sxs-lookup"><span data-stu-id="3736e-634">As part of the move to Lync, the administrator is able to configure Bob’s routing to reflect his pre-existing delegation configuration.</span></span>

  - <span data-ttu-id="3736e-p181">Brenda está viajando e aguarda uma chamada importante de um de seus clientes. No entanto, ela está em hotel e não tem acesso a computador. Ela liga para a assistência técnica e solicita que encaminhem para seu número de celular todas as chamadas feitas para seu número comercial. O pessoal da assistência técnica pode fazer a configuração em seu nome.</span><span class="sxs-lookup"><span data-stu-id="3736e-p181">Alice is travelling and realizes that she is expecting an important call from one of her customers. However, she is in a hotel and has no access to a computer. She calls the helpdesk and requests that they forward to her mobile number all the calls made to her work number. The helpdesk personnel are able to do the configuration on her behalf.</span></span>

  - <span data-ttu-id="3736e-p182">As chamadas de Vinícius para seu número comercial vão para a caixa postal de seu celular sempre que ele está no trabalho; no entanto, as coisas parecem estar funcionando corretamente na maioria dos outros locais. O técnico da assistência técnica consegue visualizar a configuração de roteamento de Vinícius e descobre que ele está com toque simultâneo configurado em seu celular. O técnico pergunta a Vinícius sobre a cobertura móvel em seu escritório e consegue determinar que a regra de toque simultâneo é o que está fazendo as chamadas irem para a caixa postal do celular de Vinícius quando sua cobertura de rede está fraca.</span><span class="sxs-lookup"><span data-stu-id="3736e-p182">Joe’s calls to his work number are going to his mobile voicemail whenever he is at work; however, things appear to be working correctly in most other locations. The helpdesk technician is able to view Joe’s routing configuration and discovers that Joe has simultaneous ringing configured to his mobile phone. The technician asks Joe about the mobile coverage at his office and is able to determine that the simultaneous ringing rule is what is causing the calls to go to Joe’s mobile voicemail when his network coverage is poor.</span></span>

  - <span data-ttu-id="3736e-642">Mike é um novo funcionário da Contoso e ele está participando de uma nova equipe na qual todos os membros são configurados para chamada de equipe, quando habilitados para o Microsoft Lync, o administrador pode definir as configurações do grupo de chamada de equipe para incluir todos os membros de sua equipe, além disso, o administrador adiciona Mike como um membro do grupo de chamada de equipe para cada um dos membros</span><span class="sxs-lookup"><span data-stu-id="3736e-642">Mike is a new employee at Contoso and he’s joining a new team on which all members are configured for team-call, when being enabled for Microsoft Lync, the administrator is able to set his team-call group settings to include all his new team members, additionally, the administrator adds Mike as a team-call group member for each of the members in his team.</span></span>

  - <span data-ttu-id="3736e-643">Uma prática de atendimento ao cliente no departamento de recursos humanos da Contoso é fornecer um atendimento pessoal a todos os chamadores desde a primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="3736e-643">A customer service practice in the human resources department at Contoso is to provide personal service for all callers since the first call.</span></span> <span data-ttu-id="3736e-644">Como todos os membros do departamento sentam-se muito próximos uns dos outros, ter todos os telefones tocando ao mesmo tempo com a chamada de equipe é desconfortável para a equipe.</span><span class="sxs-lookup"><span data-stu-id="3736e-644">Given that all members of the department sit very close to each other, having all phones ringing at the same time with team-call is very disruptive for the team.</span></span> <span data-ttu-id="3736e-645">Para fornecer o melhor serviço sem interromper os membros da equipe, o administrador do Lync aproveita o recurso de retirada de chamadas em grupo.</span><span class="sxs-lookup"><span data-stu-id="3736e-645">To provide the best service without disrupting the team members, the Lync administrator takes advantage of the Group Call Pickup capability.</span></span> <span data-ttu-id="3736e-646">O administrador adiciona todos os membros do departamento a um grupo de recebimento e informa o número do grupo de recebimento ao departamento.</span><span class="sxs-lookup"><span data-stu-id="3736e-646">The administrator adds all department members to a pickup group and communicates to the department the pickup group number.</span></span> <span data-ttu-id="3736e-647">Quando Clara está fora de sua mesa, Vinícius percebe que o telefone dela está tocando e atende à chamada em sua própria mesa.</span><span class="sxs-lookup"><span data-stu-id="3736e-647">When Samantha is absent from her desk, Joe notices her phone ringing and he proceeds to answer the call from his desk.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-648">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-648">Requirements</span></span>

<span data-ttu-id="3736e-p184">A ferramenta SEFAUtil pode ser executada apenas em um computador que faça parte de um pool de aplicativos confiáveis. O UCMA 3.0 deve ser instalado nesse computador. Para executar a ferramenta, um novo aplicativo confiável com a ID do aplicativo SEFAUtil deve ser criado nesse pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-p184">The SEFAUtil tool can be run only on a computer that is a part of a Trusted Application Pool. UCMA 3.0 must be installed on that computer. To run the tool, a new Trusted Application with the SEFAUtil application ID must be created on that pool.</span></span>

<span data-ttu-id="3736e-652">**Criando um novo aplicativo confiável para a ferramenta SEFAUtil**</span><span class="sxs-lookup"><span data-stu-id="3736e-652">**Creating a new Trusted Application for the SEFAUtil tool**</span></span>

1.  <span data-ttu-id="3736e-653">A ferramenta SEFAUTil pode ser executada apenas em um computador que faça parte de um pool de aplicativos confiáveis.</span><span class="sxs-lookup"><span data-stu-id="3736e-653">The SEFAUTil tool can be run only on a computer that is part of a trusted application pool.</span></span> <span data-ttu-id="3736e-654">Se necessário, adicionar um pool como um novo pool de aplicativos confiável pode ser feito por meio do Shell de gerenciamento do Lync Server com o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3736e-654">If needed, adding a pool as a new trusted application pool can be done via the Lync Server Management Shell with the following cmdlet:</span></span>
    
        New-CsTrustedApplicationPool -id <Pool FQDN> -Registrar <Pool Registrar FQDN> -site Site:<Pool Site>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3736e-655">O UCMA 3.0 deve ser instalado em qualquer computador que será usado para executar a ferramenta SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="3736e-655">UCMA 3.0 must be installed on any computer that will be used to run the SEFAUtil tool.</span></span>

    
    </div>

2.  <span data-ttu-id="3736e-656">Um aplicativo confiável precisa ser definido na topologia para a ferramenta SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="3736e-656">A trusted application needs to be defined in the topology for the SEFAUtil tool.</span></span> <span data-ttu-id="3736e-657">Para definir SEFAUtil como um novo aplicativo confiável, use o Shell de gerenciamento do Lync Server e execute o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3736e-657">To define SEFAUtil as a new trusted application, use the Lync Server Management Shell and execute the following cmdlet:</span></span>
    
        New-CsTrustedApplication -ApplicationId sefautil -TrustedApplicationPoolFqdn <Pool FQDN>  -Port 7489
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3736e-658">Uma porta diferente pode ser usada, se necessário.</span><span class="sxs-lookup"><span data-stu-id="3736e-658">A different port can be used if needed.</span></span>

    
    </div>

3.  <span data-ttu-id="3736e-659">As alterações de topologia precisam ser habilitadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-659">The topology changes need to be enabled.</span></span> <span data-ttu-id="3736e-660">Habilitar as alterações de topologia pode ser feito por meio do Shell de gerenciamento do Lync Server executando o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3736e-660">Enabling the topology changes can be done via the Lync Server Management Shell by executing the following cmdlet:</span></span>
    
        Enable-CsToplogy

4.  <span data-ttu-id="3736e-661">Se necessário, instale as ferramentas do Lync Server 2013 Resource Kit no servidor que serão usadas para executar a ferramenta SEFAUtil (o servidor deve fazer parte de um pool de aplicativos confiável).</span><span class="sxs-lookup"><span data-stu-id="3736e-661">If needed, install the Lync Server 2013 Resource Kit Tools in the server that will be used to run the SEFAUtil tool (the server must be part of a trusted application pool).</span></span>

5.  <span data-ttu-id="3736e-662">Verifique se o SEFAUtil está sendo executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="3736e-662">Verify the SEFAUtil is running correctly.</span></span> <span data-ttu-id="3736e-663">Para fazer isso, execute a ferramenta em um prompt de comando do Windows com privilégios de administrador para exibir as configurações de encaminhamento de chamadas de um usuário na implantação.</span><span class="sxs-lookup"><span data-stu-id="3736e-663">To do this, run the tool from a windows command prompt with administrator privileges to display the call forwarding settings of a user in the deployment.</span></span> <span data-ttu-id="3736e-664">Por padrão, a ferramenta estará localizada em: "... \\ Arquivos de programa \\ Microsoft Lync Server 2013 \\ reskit ".</span><span class="sxs-lookup"><span data-stu-id="3736e-664">By default the tool will be located in: “…\\Program Files\\Microsoft Lync Server 2013\\Reskit”.</span></span> <span data-ttu-id="3736e-665">Para exibir as configurações de encaminhamento de chamadas de um usuário, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="3736e-665">To display the call forwarding settings of a user, use the following command:</span></span>
    
        SEFAUtil.exe <user SIP address> /server:<Lync Server/Pool FQDN>
    
    <span data-ttu-id="3736e-666">As configurações de encaminhamento de chamadas do usuário devem ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="3736e-666">The call forwarding settings of the user should be displayed.</span></span>

<div>

## <a name="group-call-pickup"></a><span data-ttu-id="3736e-667">Recebimento de Chamadas em Grupo</span><span class="sxs-lookup"><span data-stu-id="3736e-667">Group Call Pickup</span></span>

<span data-ttu-id="3736e-668">A retirada de chamadas em grupo requer configuração adicional no Lync Server para que a funcionalidade seja totalmente habilitada.</span><span class="sxs-lookup"><span data-stu-id="3736e-668">Group Call Pickup requires additional configuration in Lync Server for the capability to be fully enabled.</span></span> <span data-ttu-id="3736e-669">Antes de atribuir grupos de atendimento aos usuários, consulte a documentação do produto de Recebimento de Chamadas em Grupo para ver as etapas de planejamento e implantação desse recurso.</span><span class="sxs-lookup"><span data-stu-id="3736e-669">Before assigning pickup groups to users, refer to the Group Call Pickup product documentation for the planning and deployment steps of this capability.</span></span>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-670">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-670">Examples</span></span>

<div>

## <a name="display-current-call-handling-settings"></a><span data-ttu-id="3736e-671">Exibir configurações atuais de administração de chamadas</span><span class="sxs-lookup"><span data-stu-id="3736e-671">Display Current Call Handling Settings</span></span>

<span data-ttu-id="3736e-672">O comando a seguir exibe a administração de chamadas do usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-672">The following command displays the call handling for the user.</span></span> `SEFAUtil.exe /server:lyncserver.contoso.com katarina@contoso.com`

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-673">Este exemplo usa a opção <STRONG>/Server</STRONG> para especificar o servidor do Lync para se conectar.</span><span class="sxs-lookup"><span data-stu-id="3736e-673">This example uses the <STRONG>/server</STRONG> switch to specify the Lync Server to connect to.</span></span>



</div>

<span data-ttu-id="3736e-674">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-674">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:20
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="set-the-call-forwardno-answer-destination"></a><span data-ttu-id="3736e-675">Definir destino de encaminhamento de chamadas/destino sem resposta</span><span class="sxs-lookup"><span data-stu-id="3736e-675">Set the Call Forward/No Answer Destination</span></span>

<span data-ttu-id="3736e-676">Este exemplo define o encaminhamento de chamadas/destino sem resposta e o atraso de toque.</span><span class="sxs-lookup"><span data-stu-id="3736e-676">This example sets the call forward/no answer destination and the ring delay.</span></span> <span data-ttu-id="3736e-677">Aqui, a opção/Server não é fornecida; O SEFAUtil tenta descobrir o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3736e-677">Here, the /server switch is not provided; SEFAUtil attempts to autodiscover the Lync Server.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /enablefwdnoanswer /callanswerwaittime:30 /setfwddestination:+1425555 0126@contoso.com;user=phone

<span data-ttu-id="3736e-678">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-678">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: sip:+14255550126@contoso.com;user=phone

</div>

<div>

## <a name="enable-call-forwarding-immediately"></a><span data-ttu-id="3736e-679">Habilitar o encaminhamento de chamadas imediatamente</span><span class="sxs-lookup"><span data-stu-id="3736e-679">Enable Call Forwarding Immediately</span></span>

<span data-ttu-id="3736e-680">Este exemplo habilita imediatamente o encaminhamento de chamadas para outro usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-680">This example immediately enables call-forwarding to another user.</span></span>

    SEFAUtil.exe sip:katarina@contoso.com /enablefwdimmediate /setfwddestination:anders@contoso.com

<span data-ttu-id="3736e-681">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-681">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    Forward immediate to: sip:anders@contoso.com

</div>

<div>

## <a name="disable-call-forwarding-immediately"></a><span data-ttu-id="3736e-682">Desabilitar o encaminhamento de chamadas imediatamente</span><span class="sxs-lookup"><span data-stu-id="3736e-682">Disable Call Forwarding Immediately</span></span>

<span data-ttu-id="3736e-683">Este exemplo desabilita imediatamente o encaminhamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="3736e-683">This example immediately disables call forwarding.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com katarina@contoso.com  /disablefwdimmediate

<span data-ttu-id="3736e-684">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="3736e-684">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="add-a-user-as-a-delegate-and-set-up-simultaneous-ringing-of-delegates"></a><span data-ttu-id="3736e-685">Adicionar um usuário como um representante e configurar o toque simultâneo dos representantes</span><span class="sxs-lookup"><span data-stu-id="3736e-685">Add a User as a Delegate and Set Up Simultaneous Ringing of Delegates</span></span>

<span data-ttu-id="3736e-686">Este exemplo adiciona um usuário como um representante e configura o toque simultâneo dos representantes:</span><span class="sxs-lookup"><span data-stu-id="3736e-686">This example adds a user as a delegate and sets up simultaneous ringing of delegates.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /adddelegate:joe@contoso.com /simulringdelegates

<span data-ttu-id="3736e-687">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="3736e-687">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simultaneously Ringing Delegates: sip:joe@contoso.com

</div>

<div>

## <a name="change-simultaneous-ringing-rule-of-delegates"></a><span data-ttu-id="3736e-688">Alterar regra de toque simultâneo dos representantes</span><span class="sxs-lookup"><span data-stu-id="3736e-688">Change Simultaneous Ringing Rule of Delegates</span></span>

<span data-ttu-id="3736e-689">Este exemplo altera a regra de toque simultâneo que foi definida no exemplo anterior à regra de toque atrasado.</span><span class="sxs-lookup"><span data-stu-id="3736e-689">This example changes the simultaneous ringing rule that was set in the previous example to the delayed ringing rule.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /delayringdelegates:10

<span data-ttu-id="3736e-690">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="3736e-690">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    Delay Ringing Delegates (delay:10 seconds): sip:joe@contoso.com

</div>

<div>

## <a name="remove-the-delegate"></a><span data-ttu-id="3736e-691">Remover o representante</span><span class="sxs-lookup"><span data-stu-id="3736e-691">Remove the Delegate</span></span>

<span data-ttu-id="3736e-692">Este exemplo remove o representante.</span><span class="sxs-lookup"><span data-stu-id="3736e-692">This example removes the delegate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-693">Quando o ultimo representante é removido, o toque delegado é desabilitado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3736e-693">When the last delegate is removed, delegate ringing is automatically disabled.</span></span>



</div>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /removedelegate:joe@contoso.com

<span data-ttu-id="3736e-694">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-694">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="add-a-delegate-and-set-up-the-call-forward-to-delegates-rule"></a><span data-ttu-id="3736e-695">Adicionar um representante e configurar a regra de encaminhamento de chamadas para representantes</span><span class="sxs-lookup"><span data-stu-id="3736e-695">Add a Delegate and Set Up the Call-Forward to Delegates Rule</span></span>

<span data-ttu-id="3736e-696">Este exemplo adiciona um representante e configura a regra de encaminhamento de chamadas para representantes.</span><span class="sxs-lookup"><span data-stu-id="3736e-696">This example adds a delegate and sets up the call-forward to delegates rule.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /adddelegate:anders@contoso.com /fwdtodelegates

<span data-ttu-id="3736e-697">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-697">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Forwarding calls to Delegates: sip:anders@contoso.com

</div>

<div>

## <a name="enable-simultaneous-ringing-and-set-a-destination-number"></a><span data-ttu-id="3736e-698">Habilitar toque simultâneo e definir um número de destino</span><span class="sxs-lookup"><span data-stu-id="3736e-698">Enable Simultaneous Ringing and Set a Destination Number</span></span>

<span data-ttu-id="3736e-699">Este exemplo habilita o toque simultâneo e define o número de destino do toque simultâneo.</span><span class="sxs-lookup"><span data-stu-id="3736e-699">This example enables simultaneous ringing and sets a simultaneous ringing destination number.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /setsimulringdestination:+14255550126 /enablesimulring

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-700">Para alterar o número de destino do toque simultâneo de um usuário cujo toque simultâneo já está habilitado, mantenha o comando com a opção /enablesimulring; caso contrário, o número de destino não será alterado.</span><span class="sxs-lookup"><span data-stu-id="3736e-700">To change the simultaneous ringing destination number of a user that has already simultaneous ringing enabled, keep the command with the /enablesimulring switch, otherwise the destination number will not be changed.</span></span>



</div>

<span data-ttu-id="3736e-701">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-701">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: True
    Simul_Ringing to: sip:+14255550126@contoso.com;user=phone

</div>

<div>

## <a name="disable-simultaneous-ringing"></a><span data-ttu-id="3736e-702">Desabilitar toque simultâneo</span><span class="sxs-lookup"><span data-stu-id="3736e-702">Disable Simultaneous Ringing</span></span>

<span data-ttu-id="3736e-703">Este exemplo desabilita o toque simultâneo.</span><span class="sxs-lookup"><span data-stu-id="3736e-703">This example disables simultaneous ringing.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /disablesimulring

<span data-ttu-id="3736e-704">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-704">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="add-a-team-member-for-team-call-and-set-up-simultaneous-ringing-to-the-team-call-members-group"></a><span data-ttu-id="3736e-705">Adicionar um membro da equipe para chamada de equipe e configurar toque simultâneo para o grupo de membros da chamada de equipe</span><span class="sxs-lookup"><span data-stu-id="3736e-705">Add a Team Member for Team-Call and Set up Simultaneous Ringing to the Team-Call Members Group</span></span>

<span data-ttu-id="3736e-706">Este exemplo adiciona um membro ao grupo de chamada de equipe de um usuário e habilita o toque simultâneo para o grupo de chamada de equipe.</span><span class="sxs-lookup"><span data-stu-id="3736e-706">This example adds a team member to the team-call group of a user and enables simultaneous ringing to the team-call group.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /addteammember:anders@contoso.com /simulringteam

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-707">Adicionar um membro ao grupo de chamada de equipe de um usuário mudará automaticamente as configurações de toque simultâneo dos usuários para o toque simultâneo do grupo de chamada de equipe desse membro.</span><span class="sxs-lookup"><span data-stu-id="3736e-707">Adding a member to the team-call group of a user will automatically switch the simultaneous ringing settigs of the users to simulring his team-call group.</span></span>



</div>

<span data-ttu-id="3736e-708">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-708">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Team ringing enabled. Team: sip:anders@contoso.com

</div>

<div>

## <a name="remove-a-member-from-the-team-call-group"></a><span data-ttu-id="3736e-709">Remover um membro do grupo de chamada de equipe</span><span class="sxs-lookup"><span data-stu-id="3736e-709">Remove a Member from the Team-Call Group</span></span>

<span data-ttu-id="3736e-710">Este exemplo remove um membro da equipe do grupo de chamada de equipe de um usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-710">This example removes a team member of the team-call group of a user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /removeteammember:anders@contoso.com

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-711">Se o membro a ser removido for o único membro do grupo de chamada de equipe, o toque simultâneo para o grupo de chamada de equipe será automaticamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3736e-711">If the member being removed is the only member of the team-call group, simultaneously ringing to the team-call group will be automatically disabled.</span></span>



</div>

<span data-ttu-id="3736e-712">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-712">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="set-the-delayed-ring-to-the-team-call-group"></a><span data-ttu-id="3736e-713">Definir toque atrasado para o grupo de chamada de equipe</span><span class="sxs-lookup"><span data-stu-id="3736e-713">Set the Delayed Ring to the Team-Call Group</span></span>

<span data-ttu-id="3736e-714">Este exemplo altera o toque atrasado para a configuração de hora do grupo de chamada de equipe.</span><span class="sxs-lookup"><span data-stu-id="3736e-714">This example changes the delayed ring to the team-call group time setting.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /delayringteam:5

<span data-ttu-id="3736e-715">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-715">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Delay Ringing Team (delay:5 seconds). Team: sip:anders@contoso.com

</div>

<div>

## <a name="enable-team-call"></a><span data-ttu-id="3736e-716">Habilitar chamada de equipe</span><span class="sxs-lookup"><span data-stu-id="3736e-716">Enable Team-Call</span></span>

<span data-ttu-id="3736e-717">Isso habilita a chamada de equipe de determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-717">This example enables team-call for a given user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /simulringteam

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-718">Se o grupo de chamada de equipe do usuário não tiver membros, a chamada de equipe não será habilitada.</span><span class="sxs-lookup"><span data-stu-id="3736e-718">If the team-call group of the user has no members, team-call won’t be enabled.</span></span>



</div>

<span data-ttu-id="3736e-719">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-719">**Output**</span></span>

</div>

<div>

## <a name="disable-team-call"></a><span data-ttu-id="3736e-720">Desabilitar chamada de equipe</span><span class="sxs-lookup"><span data-stu-id="3736e-720">Disable Team-Call</span></span>

<span data-ttu-id="3736e-721">Este exemplo desabilita a chamada de equipe de um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-721">This example disables team-call for a given user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /disableteamcall

<span data-ttu-id="3736e-722">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-722">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="enable-group-call-pickup-and-assign-a-pickup-group-to-a-user"></a><span data-ttu-id="3736e-723">Habilitar recebimento de chamadas em grupo e atribuir um grupo de recebimento a um usuário</span><span class="sxs-lookup"><span data-stu-id="3736e-723">Enable Group Call Pickup and Assign a Pickup Group to a User</span></span>

<span data-ttu-id="3736e-724">Este exemplo atribui um grupo de recebimento a um usuário e habilita o Recebimento de Chamadas em Grupo.</span><span class="sxs-lookup"><span data-stu-id="3736e-724">This example assigns a pickup group to a user and enables Group Call Pickup.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /enablegrouppickup:199

<span data-ttu-id="3736e-725">**Saída**</span><span class="sxs-lookup"><span data-stu-id="3736e-725">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Group Pickup Orbit: sip:199;phone-context=user-default@ contoso.com;user=phone

</div>

<div>

## <a name="disable-group-call-pickup"></a><span data-ttu-id="3736e-726">Desabilitar recebimento de chamadas em grupo</span><span class="sxs-lookup"><span data-stu-id="3736e-726">Disable Group Call Pickup</span></span>

<span data-ttu-id="3736e-727">Este exemplo desabilita o Recebimento de Chamadas em Grupo de determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-727">This example disables Group Call Pickup for a given user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /disablegrouppickup

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-p191">Ao desabilitar o Recebimento de Chamadas em Grupo de determinado usuário, o número do grupo que foi atribuído ao usuário não é retido. Se desejar habilitar novamente o Recebimento de Chamadas em Grupo para esse usuário, será necessário atribuir o numero do grupo novamente com a opção /enablegrouppickup.</span><span class="sxs-lookup"><span data-stu-id="3736e-p191">When you disable Group Call Pickup for a user, the group number that was assigned to the user is not retained. If you subsequently want to re-enable Group Call Pickup for that user, you must assign the group number again with the /enablegrouppickup switch.</span></span>



</div>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True

</div>

</div>

</div>

<div>

## <a name="sysprepps1"></a><span data-ttu-id="3736e-730">SYSPrep.ps1</span><span class="sxs-lookup"><span data-stu-id="3736e-730">SYSPrep.ps1</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-731">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-731">Description</span></span>

<span data-ttu-id="3736e-732">SYSPrep.ps1 é um script do Windows PowerShell que instalará os seguintes pré-requisitos do Lync Server 2013 em seu computador do sistema operacional Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3736e-732">SYSPrep.ps1 is a Windows PowerShell script that will install the following Lync Server 2013 prerequisites on your Windows Server 2008 operating system machine.</span></span>

  - <span data-ttu-id="3736e-733">Microsoft .Net Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="3736e-733">Microsoft .Net Framework 4.5</span></span>

  - <span data-ttu-id="3736e-734">Microsoft SQL Server Express</span><span class="sxs-lookup"><span data-stu-id="3736e-734">Microsoft SQL Server Express</span></span>

  - <span data-ttu-id="3736e-735">Windows PowerShell versão 3.0</span><span class="sxs-lookup"><span data-stu-id="3736e-735">Windows Powershell version 3.0</span></span>

  - <span data-ttu-id="3736e-736">Pacotes Redistribuíveis do Visual C++ 2010</span><span class="sxs-lookup"><span data-stu-id="3736e-736">Visual C++ 2010 Redistributable</span></span>

  - <span data-ttu-id="3736e-737">Atualizações do Servidor de Informações da Internet</span><span class="sxs-lookup"><span data-stu-id="3736e-737">Internet Information Server Updates</span></span>

  - <span data-ttu-id="3736e-738">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="3736e-738">Windows Identity Foundation</span></span>

  - <span data-ttu-id="3736e-739">Arquivos principais do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-739">Lync Server 2013 Core files</span></span>

<span data-ttu-id="3736e-740">Embora o nome do script seja semelhante à Ferramenta de Preparação do Sistema para os sistemas operacionais Microsoft Windows, eles são diferentes.</span><span class="sxs-lookup"><span data-stu-id="3736e-740">While the script name is similar to the System Preparation Tool for the Microsoft Windows operating systems, they are different.</span></span> <span data-ttu-id="3736e-741">Este script instalará somente os pré-requisitos obrigatórios do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-741">This script will only install the required prerequisites for Lync Server 2013.</span></span> <span data-ttu-id="3736e-742">Depois que esses requisitos estiverem instalados, a ferramenta SYSPrep do Windows poderá então ser usada para criar uma imagem do servidor.</span><span class="sxs-lookup"><span data-stu-id="3736e-742">Once those prerequisites are installed, the Windows SYSPrep tool can then be used to create an image of the server.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-743">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-743">Requirements</span></span>

<span data-ttu-id="3736e-744">Antes de executar o script SYSPrep.ps1, você deve copiar os arquivos de pré-requisito para uma pasta local no computador do sistema operacional Windows Server 2008 (por exemplo, **D: \\ configuração)**.</span><span class="sxs-lookup"><span data-stu-id="3736e-744">Prior to running the SYSPrep.ps1 script, you must copy the prerequisite files to a local folder on the Windows Server 2008 operating system machine (for example **D:\\Setup)**.</span></span> <span data-ttu-id="3736e-745">Essa pasta também deve incluir uma cópia dos arquivos do Lync Server 2013, especificamente **Setup.exe.**</span><span class="sxs-lookup"><span data-stu-id="3736e-745">This folder must also include a copy of the Lync Server 2013 files, specifically **Setup.exe.**</span></span> <span data-ttu-id="3736e-746">Os arquivos de pré-requisitos podem ser baixados dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="3736e-746">The prerequisite files can be downloaded from the following locations:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3736e-747">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="3736e-747">Prerequisite</span></span></th>
<th><span data-ttu-id="3736e-748">Local</span><span class="sxs-lookup"><span data-stu-id="3736e-748">Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3736e-749">Microsoft .Net Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="3736e-749">Microsoft .Net Framework 4.5</span></span></p></td>
<td><p>https://go.microsoft.com/?linkid=9816306</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3736e-750">Microsoft SQL Server Express 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3736e-750">Microsoft SQL Server Express 2008 R2</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=23650</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3736e-751">Windows PowerShell versão 3.0</span><span class="sxs-lookup"><span data-stu-id="3736e-751">Windows Powershell version 3.0</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=34595</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3736e-752">Pacotes Redistribuíveis do Visual C++ 2010</span><span class="sxs-lookup"><span data-stu-id="3736e-752">Visual C++ 2010 Redistributable</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=5555</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3736e-753">Atualizações do Servidor de Informações da Internet</span><span class="sxs-lookup"><span data-stu-id="3736e-753">Internet Information Server Updates</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=34869</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3736e-754">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="3736e-754">Windows Identity Foundation</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=17331</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3736e-755">Setup.exe do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-755">Lync Server 2013 Setup.exe</span></span></p></td>
<td><p><span data-ttu-id="3736e-756">Copiar da mídia do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-756">Copy from Lync Server 2013 media</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="parameter"></a><span data-ttu-id="3736e-757">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="3736e-757">Parameter</span></span>

<span data-ttu-id="3736e-758">O parâmetro **–SetupFolder** toma como argumento o local do diretório dos arquivos de pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="3736e-758">The **–SetupFolder** parameter takes as an argument the directory location of the prerequisite files</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-759">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-759">Examples</span></span>

<span data-ttu-id="3736e-760">Para executar o script SYSPrep.ps1 e instalar os pré-requisitos do Lync Server 2013, execute o seguinte comando em um prompt de comando elevado:</span><span class="sxs-lookup"><span data-stu-id="3736e-760">To run the SYSPrep.ps1 script and install the Lync Server 2013 prerequisites, run the following command from an elevated command prompt:</span></span>

    ./SysPrep.PS1 -SetupFolder D:\Setup

</div>

</div>

<div>

## <a name="unassigned-number-announcements-migration"></a><span data-ttu-id="3736e-761">Migração de Comunicados de Número Não Atribuído</span><span class="sxs-lookup"><span data-stu-id="3736e-761">Unassigned Number Announcements Migration</span></span>

<span data-ttu-id="3736e-762">A ferramenta de migração de anúncios de número não atribuído permite que um administrador do Lync mova a configuração de números não atribuídos que é atendida pelo aplicativo de anúncio de um servidor ou de um servidor Lync de origem para um servidor ou grupo Lync de destino.</span><span class="sxs-lookup"><span data-stu-id="3736e-762">The Unassigned Number Announcements Migration tool enables a Lync administrator to move the unassigned numbers configuration that is serviced by the announcement application from a source Lync Server or Pool to a destination Lync Server or Pool.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-763">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-763">Description</span></span>

<span data-ttu-id="3736e-764">A ferramenta de Migração de Comunicados de Número Não Atribuído é um script do Windows PowerShell que move a configuração de números não atribuídos atendidos pelo aplicativo de comunicados de um servidor ou pool de origem para outro servidor ou pool.</span><span class="sxs-lookup"><span data-stu-id="3736e-764">The Unassigned Number Announcements Migration tool is a Windows PowerShell script that moves the unassigned numbers configuration serviced by the announcement application of a source server or pool to a different server or pool.</span></span>

<span data-ttu-id="3736e-765">Quando executado, o script da Migração de Comunicados de Número não Atribuído realizará as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="3736e-765">When executed, the Unassigned Number Announcements Migration script will perform the following operations:</span></span>

1.  <span data-ttu-id="3736e-766">Mover todos os arquivos de áudio usados pelos comunicados de números não atribuídos do aplicativo de comunicado hospedado no servidor ou pool de origem para o repositório de arquivos do servidor ou pool de destino.</span><span class="sxs-lookup"><span data-stu-id="3736e-766">Move all the audio files used by the unassigned number announcements of the announcement application hosted in the source server or pool to the file store of the destination server or pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3736e-767">os arquivos de áudio são removidos do pool de origem quando são copiados para o pool de destino.</span><span class="sxs-lookup"><span data-stu-id="3736e-767">the audio files are removed from the source pool once they’re copied to the destination pool.</span></span>

    
    </div>

2.  <span data-ttu-id="3736e-768">Mover todos os comunicados de números não atribuídos configurados do aplicativo de comunicados hospedado no servidor ou pool de origem para o servidor ou pool de destino.</span><span class="sxs-lookup"><span data-stu-id="3736e-768">Move all unassigned number announcements configured for the announcement application hosted in the source server or pool to the destination server or pool.</span></span>

3.  <span data-ttu-id="3736e-769">Atribuir novamente todos os intervalos de números não atribuídos que são atendidos pelo aplicativo de comunicados hospedado no servidor ou pool de origem ao servidor ou pool de destino.</span><span class="sxs-lookup"><span data-stu-id="3736e-769">Reassign all the unassigned number ranges that are serviced by the announcement application hosted in the source server or pool to the destination server or pool.</span></span>

<span data-ttu-id="3736e-770">Depois de executar o script com êxito, todos os intervalos de números não atribuídos que eram atendidos pelo aplicativo de comunicados hospedado no servidor ou pool de origem agora serão atendidos com a mesma configuração pelo servidor ou pool de destino.</span><span class="sxs-lookup"><span data-stu-id="3736e-770">After successfully running the script, all the unassigned number ranges that were serviced by the announcement application hosted in the source server or pool will now be serviced with the same configuration by the destination server or pool.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-771">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-771">Output</span></span>

<span data-ttu-id="3736e-772">O script **move-CsAnnouncementConfiguration** indica na janela do Shell de gerenciamento do Lync a partir de onde ele é executado o êxito ou falha da operação de migração.</span><span class="sxs-lookup"><span data-stu-id="3736e-772">The **Move-CsAnnouncementConfiguration** script indicates in the Lync Management Shell window from where it’s executed the success or failure of the migration operation.</span></span>

<span data-ttu-id="3736e-p194">Se a execução da operação for interrompida por qualquer erro, os intervalos de números não atribuídos que foram movidos com êxito para o destino permanecerão no destino de uma forma operacional, e o restante dos intervalos de números não atribuídos a serem migrados permanecerá na origem também em uma forma operacional. Para migrar totalmente o restante da configuração, execute novamente o script depois de resolver o erro.</span><span class="sxs-lookup"><span data-stu-id="3736e-p194">If the execution of the operation is interrupted by any error, the unassigned number ranges that were successfully moved to the destination will remain in the destination in an operational form and the rest of the unassigned number ranges to be migrated will remain in the source as well in an operational form. To fully migrate the rest of the configuration, rerun the script after addressing the error.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="3736e-775">Objetivo</span><span class="sxs-lookup"><span data-stu-id="3736e-775">Purpose</span></span>

<span data-ttu-id="3736e-776">O script de Migração de Comunicados de Número Não Atribuído pode ser usado nos três cenários a seguir:</span><span class="sxs-lookup"><span data-stu-id="3736e-776">The Unassigned Number Announcements Migration script can be used in the following three scenarios:</span></span>

  - <span data-ttu-id="3736e-777">**Migrando definições de configuração para uma nova versão do Lync Server:** A Contoso está em processo de migração para o Lync Server 2013 e, como parte do processo de migração, o administrador do Lync Server gostaria de mover a configuração de números não atribuídas atendida pelo aplicativo de anúncio da implantação do Lync Server 2010 para a nova implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-777">**Migrating configuration settings to a new version of Lync Server:** Contoso is in the process of migrating to Lync Server 2013 and as part of the migration process the Lync Server administrator would like to move the unassigned numbers configuration serviced by the announcement application from the Lync Server 2010 deployment to the new Lync Server 2013 deployment.</span></span> <span data-ttu-id="3736e-778">Para mover as definições de configuração, o administrador do Lync Server usa a ferramenta de migração de anúncios de número não atribuído.</span><span class="sxs-lookup"><span data-stu-id="3736e-778">To move the configuration settings, the Lync Server administrator uses the Unassigned Number Announcements Migration tool.</span></span>

  - <span data-ttu-id="3736e-779">Reverter **uma implantação do Lync server 2013 para o Lync server 2010:** Devido a fatores inesperados, a contoso tem que reverter a migração para a nova implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3736e-779">**Rolling back a deployment from Lync Server 2013 to Lync Server 2010:** Due unexpected factors, Contoso has to roll back the migration to the new Lync Server 2013 deployment.</span></span> <span data-ttu-id="3736e-780">Para minimizar as interrupções do serviço, o administrador do Lync Server usa a ferramenta de migração de anúncios de número não atribuído para reverter a configuração da implantação do Lync Server 2013 para a implantação do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3736e-780">To minimize disruptions to the service, the Lync Server administrator uses the Unassigned Number Announcements Migration tool to roll back the configuration from the Lync Server 2013 deployment to the Lync Server 2010 deployment.</span></span>

  - <span data-ttu-id="3736e-781">**Mover dados entre implantações do Lync:** A Contoso está em processo de substituição de todos os servidores de um pool por servidores mais recentes.</span><span class="sxs-lookup"><span data-stu-id="3736e-781">**Moving data between Lync deployments:** Contoso is in the process of replacing all the servers of one pool with newer servers.</span></span> <span data-ttu-id="3736e-782">Sua estratégia é implantar um novo pool do Lync Server 2013, mover todos os dados do antigo para o novo pool e, em seguida, substituir o pool antigo.</span><span class="sxs-lookup"><span data-stu-id="3736e-782">Their strategy is to deploy a new Lync Server 2013 pool, move all the data from the old to the new pool, and then deprecate the old pool.</span></span> <span data-ttu-id="3736e-783">Depois que o novo pool é implantado, a ferramenta de migração anúncios de número não atribuído é usada para mover a configuração do pool antigo para o novo.</span><span class="sxs-lookup"><span data-stu-id="3736e-783">Once the new pool is deployed, the Unassigned Number Announcements Migration tool is used to move the configuration from the old pool to the new one.</span></span>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-784">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-784">Requirements</span></span>

<span data-ttu-id="3736e-785">Os principais requisitos necessários para executar a ferramenta com êxito são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="3736e-785">The following are the main requirements needed to successfully run the tool:</span></span>

1.  <span data-ttu-id="3736e-786">O script deve ser executado em um computador com o Shell de gerenciamento do Lync Server 2013 instalado.</span><span class="sxs-lookup"><span data-stu-id="3736e-786">The script must be run from a computer that has Lync Server 2013 Management Shell installed.</span></span>

2.  <span data-ttu-id="3736e-787">O aplicativo de anúncio precisa ser implantado com êxito nos servidores ou pools de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="3736e-787">The announcement application has to be successfully deployed in the source and destination Lync Servers or Pools.</span></span>

<div>

## <a name="move-csannouncementconfiguration-script"></a><span data-ttu-id="3736e-788">Script Move-CsAnnouncementConfiguration</span><span class="sxs-lookup"><span data-stu-id="3736e-788">Move-CsAnnouncementConfiguration script</span></span>

<span data-ttu-id="3736e-789">O script Move-CsAnnouncementConfiguration exige os dois parâmetros descritos na tabela abaixo. </span><span class="sxs-lookup"><span data-stu-id="3736e-789">The Move-CsAnnouncementConfiguration script requires the two parameters that are described in the table below.</span></span>

<span data-ttu-id="3736e-790">![Parâmetros move-CsAnnouncementConfiguration.](images/JJ945604.7ab66ad3-d0db-4d77-8b93-ebccf0cb0663(OCS.15).jpg "Parâmetros de Move-CsAnnouncementConfiguration.")</span><span class="sxs-lookup"><span data-stu-id="3736e-790">![Move-CsAnnouncementConfiguration parameters.](images/JJ945604.7ab66ad3-d0db-4d77-8b93-ebccf0cb0663(OCS.15).jpg "Move-CsAnnouncementConfiguration parameters.")</span></span>

</div>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-791">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-791">Examples</span></span>

<div>

## <a name="moving-the-unassigned-number-announcements-configuration-from-a-lync-server-2010-pool-to-a-lync-server-2013-pool"></a><span data-ttu-id="3736e-792">Mover a configuração de anúncios de número não atribuído de um pool do Lync Server 2010 para um pool do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3736e-792">Moving the Unassigned Number Announcements Configuration from a Lync Server 2010 Pool to a Lync Server 2013 Pool</span></span>

<span data-ttu-id="3736e-793">Este exemplo move os anúncios de número não atribuído do pool de origem (Lync Server 2010) para o pool de destino (Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="3736e-793">This example moves the unassigned number announcements from the source pool (Lync Server 2010) to the destination pool (Lync Server 2013).</span></span>

    Move-CsAnnouncementConfiguration.ps1 -Source LS2010Pool.contoso.com -Destination LS2013Pool.contoso.com

</div>

<div>

## <a name="moving-the-unassigned-number-announcements-configuration-from-a-lync-server-2013-pool-to-a-lync-server-2010-pool"></a><span data-ttu-id="3736e-794">Mover a configuração de anúncios de número não atribuído de um pool do Lync Server 2013 para um pool do Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="3736e-794">Moving the Unassigned Number Announcements Configuration from a Lync Server 2013 Pool to a Lync Server 2010 Pool</span></span>

<span data-ttu-id="3736e-795">Este exemplo move os anúncios de número não atribuído do pool de origem (Lync Server 2013) para o pool de destino (Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="3736e-795">This example moves the unassigned number announcements from the source pool (Lync Server 2013) to the destination pool (Lync Server 2010).</span></span>

    Move-CsAnnouncementConfiguration.ps1 -Source LS2013Pool.contoso.com -Destination LS2010Pool.contoso.com

</div>

</div>

</div>

<div>

## <a name="web-conf-data"></a><span data-ttu-id="3736e-796">Web Conf Data</span><span class="sxs-lookup"><span data-stu-id="3736e-796">Web Conf Data</span></span>

<span data-ttu-id="3736e-797">A ferramenta Web conf data permite que um administrador do software de comunicação do Lync Server 2013 tenha mais controle sobre os dados associados às conferências da Web do organizador.</span><span class="sxs-lookup"><span data-stu-id="3736e-797">The Web Conf Data Tool allows an administrator of Lync Server 2013 communications software to have more control over the data associated with an organizer’s Web conferences.</span></span> <span data-ttu-id="3736e-798">Os cenários incluem a capacidade de excluir os dados da reunião de um usuário específico com base em um critério de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="3736e-798">Scenarios include the ability to delete a specific user’s meeting data based on a time stamp criteria.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="3736e-799">Descrição</span><span class="sxs-lookup"><span data-stu-id="3736e-799">Description</span></span>

<span data-ttu-id="3736e-800">Esta ferramenta permite ao administrador executar as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="3736e-800">This tool allows the administrator to perform the following operations:</span></span>

1.  <span data-ttu-id="3736e-801">Encontrar todos os dados de webconferência associados a um único usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-801">Find all Web conferencing data associated with a single user.</span></span>

2.  <span data-ttu-id="3736e-802">Excluir todos os dados de webconferência associados a um único usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-802">Delete all Web conferencing data associated with a single user.</span></span>

3.  <span data-ttu-id="3736e-803">Excluir todos os dados de webconferência associados a um único usuário que sejam anteriores à determinada data.</span><span class="sxs-lookup"><span data-stu-id="3736e-803">Delete all Web conferencing data associated with a single user that is older than a certain date.</span></span>

4.  <span data-ttu-id="3736e-804">Mover todos os dados de webconferência associados a um único usuário quando o usuário for movido de um pool para outro.</span><span class="sxs-lookup"><span data-stu-id="3736e-804">Move all Web conferencing data associated with a single user when that user is moved from one pool to another.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3736e-805">As ferramentas do kit de recursos para Lync Server 2010 têm suporte para mover todos os dados de Webconferência associados a um único usuário quando esse usuário é movido de um pool para outro.</span><span class="sxs-lookup"><span data-stu-id="3736e-805">The Resource Kit Tools for Lync Server 2010 supported moving all Web conferencing data associated with a single user when that user is moved from one pool to another.</span></span> <span data-ttu-id="3736e-806">Essa funcionalidade agora foi preterida nesta ferramenta em favor do parâmetro <STRONG>MoveConferenceData</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3736e-806">That functionality is now deprecated from this tool in favor of the <STRONG>MoveConferenceData</STRONG> parameter.</span></span> <span data-ttu-id="3736e-807">Para obter detalhes sobre esse parâmetro, consulte o cmdlet <A href="https://technet.microsoft.com/library/gg398528(v=ocs.15)">move-CsUser</A> .</span><span class="sxs-lookup"><span data-stu-id="3736e-807">For details about this parameter, see the <A href="https://technet.microsoft.com/library/gg398528(v=ocs.15)">Move-CsUser</A> cmdlet.</span></span>



</div>

<span data-ttu-id="3736e-p200">A ferramenta exclui dados apenas de reuniões que estejam inativas. As reuniões ativas (ou reuniões em sessões) não podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="3736e-p200">The tool deletes meeting data only for meetings that are inactive. Active meetings (or meetings in sessions) cannot be deleted.</span></span>

<span data-ttu-id="3736e-p201">Essa ferramenta deve ser executada em um computador que esteja no mesmo pool do usuário de destino. O usuário cujos dados de conteúdo de reuniões estiverem sendo gerenciados por essa ferramenta deverá ser hospedado no mesmo pool de usuários.</span><span class="sxs-lookup"><span data-stu-id="3736e-p201">This tool must be run from a computer that is in the same pool as the target user. The user whose meeting content data is being managed by this tool must be homed in the same user pool.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="3736e-812">Resultado</span><span class="sxs-lookup"><span data-stu-id="3736e-812">Output</span></span>

<span data-ttu-id="3736e-813">Essa ferramenta gera os resultados de cada uma das operações:</span><span class="sxs-lookup"><span data-stu-id="3736e-813">This tool outputs the results of each of the operations:</span></span>

  - <span data-ttu-id="3736e-814">Se uma consulta é executada, a ferramenta gera a lista de todas as pastas de dados de reuniões inativas que tenham esse usuário como organizador.</span><span class="sxs-lookup"><span data-stu-id="3736e-814">If a query is performed, the tool outputs the list of all inactive meeting data folders that have that user as an organizer.</span></span>

  - <span data-ttu-id="3736e-815">Se uma exclusão é realizada, a ferramenta gera a lista de todas as pastas de dados de reuniões cujos dados serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="3736e-815">If a delete is performed, the tool outputs the list of all meeting data folders whose data will be deleted.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="3736e-816">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3736e-816">Requirements</span></span>

<span data-ttu-id="3736e-817">A ferramenta deve ser executada no mesmo pool onde o organizador está hospedado.</span><span class="sxs-lookup"><span data-stu-id="3736e-817">The tool needs to be run in the same pool where the organizer is currently homed.</span></span>

<span data-ttu-id="3736e-818">A ferramenta deve ser executada com privilégios de administrador com acesso ao repositório de arquivos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3736e-818">The tool must be run using administrator privileges with access to the Content File Store.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="3736e-819">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3736e-819">Examples</span></span>

<span data-ttu-id="3736e-820">A tabela a seguir descreve os parâmetros, alguns dos quais são usados nos exemplos.</span><span class="sxs-lookup"><span data-stu-id="3736e-820">The following table describes the parameters, some of which are used in the examples.</span></span>

<span data-ttu-id="3736e-821">![Parâmetros da ferramenta de dados Web conf.](images/JJ945604.a733c1c6-5dfc-4874-a74f-bfdee81c1401(OCS.15).jpg "Parâmetros da ferramenta de dados Web conf.")</span><span class="sxs-lookup"><span data-stu-id="3736e-821">![Web Conf Data Tool parameters.](images/JJ945604.a733c1c6-5dfc-4874-a74f-bfdee81c1401(OCS.15).jpg "Web Conf Data Tool parameters.")</span></span>

    WebConfDataTool.exe /User:user0@contoso.com /Action:query ""/ExpirationDate:08/09/2010 12:00:00""

<span data-ttu-id="3736e-p202">O exemplo anterior mostra como um comando de consulta funcionaria. O resultado desse comando seria uma lista de todas as pastas de conteúdo de reuniões que seriam afetadas por essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="3736e-p202">The preceding example shows how a query command would work. The output of such a command would be a list of all meeting content folders that would be affected by this tool.</span></span>

    WebConfDataTool.exe /User:user0@contoso.com /Action:delete

<span data-ttu-id="3736e-p203">O exemplo anterior mostra um comando de exclusão (delete), que removerá todas as pastas de reuniões inativas deste usuário.</span><span class="sxs-lookup"><span data-stu-id="3736e-p203">The preceding is an example of a delete command. The delete command will remove all inactive meeting folders from this user.</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="3736e-826">Resumo</span><span class="sxs-lookup"><span data-stu-id="3736e-826">Summary</span></span>

<span data-ttu-id="3736e-827">Essa ferramenta pode ser um recurso valioso para os administradores que precisam de um controle mais preciso sobre os dados de reuniões realizadas em chamadas em conferência.</span><span class="sxs-lookup"><span data-stu-id="3736e-827">This tool can be a valuable resource to administrators who need more precise control over conference meeting data.</span></span>

<span data-ttu-id="3736e-828"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3736e-828"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
