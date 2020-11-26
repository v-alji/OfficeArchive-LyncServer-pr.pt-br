---
title: 'Lync Server 2013: Preparando o esquema do Active Directory'
description: 'Lync Server 2013: preparando o esquema do Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the Active Directory schema
ms:assetid: 067726ae-fd3f-4133-a32f-26d2603ac674
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398119(v=OCS.15)
ms:contentKeyID: 48183300
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3df7533dcbabe278fd366b441cfd8daa83f54b23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424106"
---
# <a name="preparing-the-active-directory-schema-in-lync-server-2013"></a><span data-ttu-id="f3d6f-103">Preparando o esquema do Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3d6f-103">Preparing the Active Directory schema in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3d6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3d6f-104">

<span> </span></span></span>

<span data-ttu-id="f3d6f-105">_**Tópico da última modificação:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="f3d6f-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="f3d6f-106">Antes de começar a preparar os serviços de domínio do Active Directory, você pode abrir os arquivos de esquema usando um editor de texto, como o bloco de notas do Windows, ou consulte [extensões de esquema, classes e atributos do Active Directory usados pelo Lync server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) para examinar todas as extensões de esquema de serviços de domínio do Active Directory que serão modificadas para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-106">Before you begin preparing Active Directory Domain Services, you can open the schema files by using a text editor, such as Windows Notepad, or see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) to review all the Active Directory Domain Services schema extensions that will be modified for Lync Server 2013.</span></span> <span data-ttu-id="f3d6f-107">O Lync Server usa quatro arquivos de esquema:</span><span class="sxs-lookup"><span data-stu-id="f3d6f-107">Lync Server uses four schema files:</span></span>

  - <span data-ttu-id="f3d6f-108">ExternalSchema. ldf, que é usado para interoperabilidade com o Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="f3d6f-108">ExternalSchema.ldf, which is used for interoperability with Microsoft Exchange Server</span></span>

  - <span data-ttu-id="f3d6f-109">ServerSchema. ldf, que é o arquivo de esquema principal do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3d6f-109">ServerSchema.ldf, which is the primary Lync Server 2013 schema file</span></span>

  - <span data-ttu-id="f3d6f-110">BackCompatSchema. ldf, que é usado para interoperabilidade com qualquer componente de versões anteriores</span><span class="sxs-lookup"><span data-stu-id="f3d6f-110">BackCompatSchema.ldf, which is used for interoperability with any components from prior releases</span></span>

  - <span data-ttu-id="f3d6f-111">VersionSchema. ldf, que é usado para informações sobre a versão do esquema preparado</span><span class="sxs-lookup"><span data-stu-id="f3d6f-111">VersionSchema.ldf, which is used for version information of the prepared schema</span></span>

<span data-ttu-id="f3d6f-112">Todos os arquivos. ldf são instalados durante a preparação do esquema, independentemente de você estar migrando de uma versão anterior ou executando uma instalação limpa.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-112">All .ldf files are installed during schema preparation, regardless of whether you are migrating from a previous release or performing a clean installation.</span></span> <span data-ttu-id="f3d6f-113">Esses arquivos de esquema são instalados na sequência mostrada na lista anterior e estão localizados na \\ pasta de esquema de suporte \\ na mídia de instalação.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-113">These schema files are installed in the sequence shown in the preceding list and are located in the \\Support\\schema folder on the installation media.</span></span>

<span data-ttu-id="f3d6f-114">As extensões de esquema do Lync Server são replicadas em todos os domínios, o que afeta o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-114">The Lync Server schema extensions are replicated across all domains, which impacts network traffic.</span></span> <span data-ttu-id="f3d6f-115">Execute a preparação do esquema de cada vez quando o uso da rede for baixo.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-115">Run schema preparation at a time when network usage is low.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f3d6f-116">Se você precisar adicionar suporte para Microsoft® Office Communicator Mobile 2007 R2 para Java e Microsoft® Office Communicator Mobile para Nokia 1,0 para clientes móveis à implantação do Lync Server 2013, será necessário preparar o esquema do Active Directory para o Microsoft Office Communications Server 2007 R2 durante a instalação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-116">If you need to add support for Microsoft® Office Communicator Mobile 2007 R2 for Java and Microsoft® Office Communicator Mobile for Nokia 1.0 mobile clients to your Lync Server 2013 deployment, you need to prepare the Active Directory schema for Microsoft Office Communications Server 2007 R2 during installation of Lync Server 2013.</span></span> <span data-ttu-id="f3d6f-117">Para obter o software e a documentação necessários, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A> .</span><span class="sxs-lookup"><span data-stu-id="f3d6f-117">For the necessary software and documentation, see <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A>.</span></span>



</div>

<div>

## <a name="adsi-edit"></a><span data-ttu-id="f3d6f-118">Editar ADSI</span><span class="sxs-lookup"><span data-stu-id="f3d6f-118">ADSI Edit</span></span>

<span data-ttu-id="f3d6f-119">O editor de interfaces de serviço do Active Directory (ADSI Edit) é uma ferramenta de administração do AD DS que você pode usar para verificar a preparação e a replicação do esquema.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-119">Active Directory Service Interfaces Editor (ADSI Edit) is an AD DS administration tool that you can use to verify schema preparation and replication.</span></span>

<span data-ttu-id="f3d6f-120">O ADSI Edit é instalado por padrão quando você instala a função AD DS para fazer com que um servidor seja um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-120">ADSI Edit is installed by default when you install the AD DS role to make a server a domain controller.</span></span> <span data-ttu-id="f3d6f-121">Para Windows Server 2008 e Windows Server 2008 R2, o ADSI Edit (Adsiedit. msc) está incluído nas ferramentas de administração de servidor remoto (RSAT).</span><span class="sxs-lookup"><span data-stu-id="f3d6f-121">For Windows Server 2008 and Windows Server 2008 R2, ADSI Edit (adsiedit.msc) is included with the Remote Server Administration Tools (RSAT).</span></span> <span data-ttu-id="f3d6f-122">Você também pode instalar o RSAT em servidores membro do domínio ou servidores autônomos.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-122">You can also install RSAT on domain member servers or stand-alone servers.</span></span> <span data-ttu-id="f3d6f-123">O pacote RSAT é copiado para esses servidores por padrão quando você instala o Windows, mas ele não é instalado por padrão.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-123">The RSAT package is copied to these servers by default when you install Windows, but it is not installed by default.</span></span> <span data-ttu-id="f3d6f-124">Você instala ferramentas individuais usando o Gerenciador de servidores.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-124">You install individual tools by using Server Manager.</span></span> <span data-ttu-id="f3d6f-125">O ADSI Edit está incluído em **ferramentas de administração de funções**, ferramentas de serviços de **domínio Active Directory**, **ferramentas de controlador de domínio do Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-125">ADSI Edit is included under **Role Administration Tools**, **Active Directory Domain Services Tools**, **Active Directory Domain Controller Tools**.</span></span>

<span data-ttu-id="f3d6f-126">Para o Windows Server 2003, o ADSI Edit está incluído nas ferramentas de suporte.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-126">For Windows Server 2003, ADSI Edit is included with the Support Tools.</span></span> <span data-ttu-id="f3d6f-127">As ferramentas de suporte estão disponíveis no CD do Windows Server 2003 na \\ \\ pasta ferramentas de suporte ou você pode baixá-las em "ferramentas de suporte do bit 2003 do windows Server Service Pack 2 32-bit" [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770) .</span><span class="sxs-lookup"><span data-stu-id="f3d6f-127">The Support Tools are available from the Windows Server 2003 CD in the \\SUPPORT\\TOOLS folder, or you can download them from “Windows Server 2003 Service Pack 2 32-bit Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770).</span></span> <span data-ttu-id="f3d6f-128">Instruções para instalar as ferramentas de suporte do CD do produto estão disponíveis em "instalar ferramentas de suporte do Windows" em [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771) .</span><span class="sxs-lookup"><span data-stu-id="f3d6f-128">Instructions for installing the Support Tools from the product CD are available from “Install Windows Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771).</span></span> <span data-ttu-id="f3d6f-129">O Adsiedit.dll é registrado automaticamente quando você instala as ferramentas de suporte.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-129">Adsiedit.dll is automatically registered when you install the support tools.</span></span> <span data-ttu-id="f3d6f-130">Se, no entanto, você copiou os arquivos para o seu computador, você deve executar o comando **regsvr32** para registrar o arquivo de adsiedit.dll antes de poder executar a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-130">If, however, you copied the files to your computer, you must run the **regsvr32** command to register the adsiedit.dll file before you can run the tool.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f3d6f-131">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f3d6f-131">In This Section</span></span>

  - [<span data-ttu-id="f3d6f-132">Executando preparação de esquema de Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3d6f-132">Running Active Directory schema preparation in Lync Server 2013</span></span>](lync-server-2013-running-schema-preparation.md)

  - [<span data-ttu-id="f3d6f-133">Verificando a replicação de esquema do Active Directory no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3d6f-133">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f3d6f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3d6f-134">See Also</span></span>


[<span data-ttu-id="f3d6f-135">Preparando a floresta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3d6f-135">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
[<span data-ttu-id="f3d6f-136">Preparando domínios para Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3d6f-136">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="f3d6f-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3d6f-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

