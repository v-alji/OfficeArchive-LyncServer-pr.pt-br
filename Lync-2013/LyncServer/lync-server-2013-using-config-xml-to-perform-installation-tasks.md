---
title: 'Lync Server 2013: usando o Config.xml para executar tarefas de instalação'
description: 'Lync Server 2013: usando o Config.xml para executar tarefas de instalação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Config.xml to perform installation tasks
ms:assetid: 0813184a-ab40-417c-b3a3-c2090766b831
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204651(v=OCS.15)
ms:contentKeyID: 48183332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22fff14e21a120c3a0ee2cd6432fd1eba2bbee5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438950"
---
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a><span data-ttu-id="c3181-103">Usar o Config.xml para executar tarefas de instalação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c3181-103">Using Config.xml to perform installation tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3181-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3181-104">

<span> </span></span></span>

<span data-ttu-id="c3181-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="c3181-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="c3181-p101">Embora a Ferramenta de Personalização do Office (OCT) seja a ferramenta principal para instalação com personalização, os administradores podem usar o arquivo Config.xml para especificar instruções de instalação adicionais que não estão disponíveis na OCT. As personalizações a seguir só podem ser feitas usando o arquivo Config.xml:</span><span class="sxs-lookup"><span data-stu-id="c3181-p101">Although the Office Customization Tool (OCT) is the primary tool for customization installation, administrators can use the Config.xml file to specify additional installation instructions that are not available in the OCT. The following customizations can only be made by using the Config.xml file:</span></span>

  - <span data-ttu-id="c3181-108">Especificar o caminho do ponto de instalação de rede.</span><span class="sxs-lookup"><span data-stu-id="c3181-108">Specify the path of the network installation point.</span></span>

  - <span data-ttu-id="c3181-109">Selecionar os produtos a serem instalados.</span><span class="sxs-lookup"><span data-stu-id="c3181-109">Select the products to install.</span></span>

  - <span data-ttu-id="c3181-110">Configure o registro em log e o local do arquivo de personalização da Instalação e atualizações de software.</span><span class="sxs-lookup"><span data-stu-id="c3181-110">Configure logging and the location of the Setup customization file and software updates.</span></span>

  - <span data-ttu-id="c3181-111">Especifique as opções de instalação, como nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="c3181-111">Specify installation options, such as user name.</span></span>

  - <span data-ttu-id="c3181-112">Copiar a LIS (origem de instalação local) no computador do usuário, mas sem instalar o Office.</span><span class="sxs-lookup"><span data-stu-id="c3181-112">Copy the local installation source (LIS) to the user's computer without installing Office.</span></span>

  - <span data-ttu-id="c3181-113">Adicionar ou remover idiomas da instalação.</span><span class="sxs-lookup"><span data-stu-id="c3181-113">Add or remove languages from the installation.</span></span>

<span data-ttu-id="c3181-114">Recomendamos que você use o arquivo Config.xml para configurar a instalação silenciosa do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="c3181-114">We recommend that you use the Config.xml file to configure Lync 2013 silent installation.</span></span>

<span data-ttu-id="c3181-115">Por padrão, o arquivo Config.xml armazenado na pasta do produto principal (por exemplo, \\ produto. WW) instrui a instalação a instalar esse produto.</span><span class="sxs-lookup"><span data-stu-id="c3181-115">By default, the Config.xml file that is stored in the core product folder (for example, \\product.WW) directs Setup to install that product.</span></span> <span data-ttu-id="c3181-116">Por exemplo, o arquivo Config.xml na seguinte pasta instala o Lync 2013:</span><span class="sxs-lookup"><span data-stu-id="c3181-116">For example, the Config.xml file in the following folder installs Lync 2013:</span></span>

  - <span data-ttu-id="c3181-117">\\\\Server \\ share \\ Lync15 \\ Lync. WW \\Config.xml</span><span class="sxs-lookup"><span data-stu-id="c3181-117">\\\\server\\share\\Lync15\\Lync.WW \\Config.xml</span></span>

<span data-ttu-id="c3181-118">Os elementos Config.xml mais comumente usados para a instalação do Lync 2013 estão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3181-118">The Config.xml elements most commonly used for Lync 2013 installation are listed in the following table.</span></span>

### <a name="configxml-elements"></a><span data-ttu-id="c3181-119">Elementos de Config.xml</span><span class="sxs-lookup"><span data-stu-id="c3181-119">Config.xml elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3181-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="c3181-120">Element</span></span></th>
<th><span data-ttu-id="c3181-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3181-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3181-122">Configuração</span><span class="sxs-lookup"><span data-stu-id="c3181-122">Configuration</span></span></p></td>
<td><p><span data-ttu-id="c3181-123">Elemento de nível superior (obrigatório).</span><span class="sxs-lookup"><span data-stu-id="c3181-123">Top-level element (required).</span></span> <span data-ttu-id="c3181-124">Contém o atributo Product, por exemplo: Product = Lync</span><span class="sxs-lookup"><span data-stu-id="c3181-124">Contains the Product attribute, for example: Product=Lync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3181-125">OptionState</span><span class="sxs-lookup"><span data-stu-id="c3181-125">OptionState</span></span></p></td>
<td><p><span data-ttu-id="c3181-126">Especifica como os recursos específicos de produto são manipulados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c3181-126">Specifies how specific product features are handled during installation.</span></span> <span data-ttu-id="c3181-127">Use os atributos a seguir para impedir a instalação de serviços corporativos de conectividade, que incluem componentes compartilhados que interferem com o Outlook 2010:</span><span class="sxs-lookup"><span data-stu-id="c3181-127">Use the following attributes to prevent installation of Business Connectivity Services, which includes shared components that interfere with Outlook 2010:</span></span></p>
<ul>
<li><p><span data-ttu-id="c3181-128">ID = &quot; LOBiMain&quot;</span><span class="sxs-lookup"><span data-stu-id="c3181-128">Id=&quot;LOBiMain&quot;</span></span></p></li>
<li><p><span data-ttu-id="c3181-129">Estado = &quot; ausente&quot;</span><span class="sxs-lookup"><span data-stu-id="c3181-129">State=&quot;Absent&quot;</span></span></p></li>
<li><p><span data-ttu-id="c3181-130">Filhos = &quot; força&quot;</span><span class="sxs-lookup"><span data-stu-id="c3181-130">Children=&quot;Force&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3181-131">Exibir</span><span class="sxs-lookup"><span data-stu-id="c3181-131">Display</span></span></p></td>
<td><p><span data-ttu-id="c3181-p105">O nível deUI que a Instalação exibe para o usuário. Entre os atributos comuns estão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c3181-p105">The level of UI that Setup displays to the user. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c3181-134">CompletionNotice = &quot; Sim &quot;  |  &quot; não &quot; (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3181-134">CompletionNotice=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
<li><p><span data-ttu-id="c3181-135">AcceptEula = &quot; Sim &quot;  |  &quot; não &quot; (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3181-135">AcceptEula=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3181-136">Registro em log</span><span class="sxs-lookup"><span data-stu-id="c3181-136">Logging</span></span></p></td>
<td><p><span data-ttu-id="c3181-p106">Opções para o tipo de registro em log executado pela Instalação. Entre os atributos comuns estão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c3181-p106">Options for the kind of logging that Setup performs. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c3181-139">Digite = &quot; &quot;  |  &quot; padrão &quot; (padrão) | &quot; Detalha&quot;</span><span class="sxs-lookup"><span data-stu-id="c3181-139">Type =&quot;Off&quot; | &quot;Standard&quot;(default) | &quot;Verbose&quot;</span></span></p></li>
<li><p><span data-ttu-id="c3181-140">Template=” filename.txt” (o nome do arquivo de log)</span><span class="sxs-lookup"><span data-stu-id="c3181-140">Template=”filename.txt” (the name of the log file)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3181-141">Configuração</span><span class="sxs-lookup"><span data-stu-id="c3181-141">Setting</span></span></p></td>
<td><p><span data-ttu-id="c3181-p107">Especifica valores para as propriedades do Windows Installer. Entre os atributos comuns estão os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c3181-p107">Specifies values for Windows Installer properties. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c3181-144">Setting ID = &quot; name &quot; (o nome da Propriedade do Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="c3181-144">Setting Id=&quot;name&quot; (the name of the Windows Installer property)</span></span></p></li>
<li><p><span data-ttu-id="c3181-145">Valor = &quot; valor &quot; (o valor a ser atribuído à propriedade)</span><span class="sxs-lookup"><span data-stu-id="c3181-145">Value=&quot;value&quot; (the value to assign to the property)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3181-146">DistributionPoint</span><span class="sxs-lookup"><span data-stu-id="c3181-146">DistributionPoint</span></span></p></td>
<td><p><span data-ttu-id="c3181-p108">O caminho totalmente qualificado do ponto de instalação de rede do qual a instalação deve ser executada. Inclui o atributo Location:</span><span class="sxs-lookup"><span data-stu-id="c3181-p108">The fully qualified path of the network installation point from which the installation is to run. Includes the Location attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="c3181-149">Local=”path”</span><span class="sxs-lookup"><span data-stu-id="c3181-149">Location=”path”</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c3181-150">O exemplo a seguir mostra um arquivo Config.xml para uma instalação silenciosa típica do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="c3181-150">The following example shows a Config.xml file for a typical silent installation of Lync 2013.</span></span>

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

<span data-ttu-id="c3181-151">Informações detalhadas sobre como usar o arquivo Config.xml para executar tarefas de instalação e manutenção do Office estão disponíveis em <https://go.microsoft.com/fwlink/p/?linkid=267514> .</span><span class="sxs-lookup"><span data-stu-id="c3181-151">Detailed information about using the Config.xml file to perform Office installation and maintenance tasks is available at <https://go.microsoft.com/fwlink/p/?linkid=267514>.</span></span>

<div>

## <a name="to-customize-the-configxml-file"></a><span data-ttu-id="c3181-152">Para personalizar o arquivo Config.xml</span><span class="sxs-lookup"><span data-stu-id="c3181-152">To customize the Config.xml file</span></span>

1.  <span data-ttu-id="c3181-153">Abra o arquivo Config.xml usando uma ferramenta editora de texto, como o Bloco de Notas.</span><span class="sxs-lookup"><span data-stu-id="c3181-153">Open the Config.xml file by using a text editor tool, such as Notepad.</span></span>

2.  <span data-ttu-id="c3181-154">Localize as linhas que contêm os elementos que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="c3181-154">Locate the lines that contain the elements you want to change.</span></span>

3.  <span data-ttu-id="c3181-155">Modifique a entrada do elemento com as opções silenciosas que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="c3181-155">Modify the element entry with the silent options that you want to use.</span></span> <span data-ttu-id="c3181-156">Certifique-se de remover os delimitadores de comentário " \<\!--" and "--\> ".</span><span class="sxs-lookup"><span data-stu-id="c3181-156">Make sure that you remove the comment delimiters, "\<\!--" and "--\>".</span></span> <span data-ttu-id="c3181-157">Por exemplo, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="c3181-157">For example, use the following syntax:</span></span>
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  <span data-ttu-id="c3181-158">Salve o arquivo Config.xml.</span><span class="sxs-lookup"><span data-stu-id="c3181-158">Save the Config.xml file.</span></span>

<span data-ttu-id="c3181-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3181-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

