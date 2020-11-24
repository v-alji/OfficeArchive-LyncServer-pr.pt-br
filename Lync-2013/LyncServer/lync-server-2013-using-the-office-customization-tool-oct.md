---
title: 'Lync Server 2013: usando a ferramenta de personalização do Office (OCT)'
description: 'Lync Server 2013: usando a ferramenta de personalização do Office (OCT).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Office Customization Tool (OCT)
ms:assetid: 26647cb6-ba84-4ba7-8b6f-2cf86818e530
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204748(v=OCS.15)
ms:contentKeyID: 48183654
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 602502ba4579ed6c640eee909d4c6b056ce247d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390429"
---
# <a name="using-the-office-customization-tool-oct-in-lync-server-2013"></a><span data-ttu-id="5a3be-103">Usar a ferramenta de personalização do Office (OCT) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a3be-103">Using the Office Customization Tool (OCT) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a3be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a3be-104">

<span> </span></span></span>

<span data-ttu-id="5a3be-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5a3be-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5a3be-106">O Office Customization Tool (OCT) faz parte do programa de Instalação e é a ferramenta recomendada para várias personalizações.</span><span class="sxs-lookup"><span data-stu-id="5a3be-106">The Office Customization Tool (OCT) is part of the Setup program and is the recommended tool for many customizations.</span></span> <span data-ttu-id="5a3be-107">Ao usar o OCT, você personaliza o Office e salva suas personalizações em um arquivo msp de personalização de Instalação.</span><span class="sxs-lookup"><span data-stu-id="5a3be-107">By using the OCT, you customize Office and save your customizations in a Setup customization .msp file.</span></span> <span data-ttu-id="5a3be-108">Você coloca o arquivo na pasta Atualizações no ponto de instalação de rede.</span><span class="sxs-lookup"><span data-stu-id="5a3be-108">You place the file in the Updates folder on the network installation point.</span></span> <span data-ttu-id="5a3be-109">Ao instalar o Office, a Instalação procura por um arquivo de personalização da Instalação na pasta Atualizações e aplica as personalizações.</span><span class="sxs-lookup"><span data-stu-id="5a3be-109">When you install Office, Setup looks for a Setup customization file in the Updates folder and applies the customizations.</span></span> <span data-ttu-id="5a3be-110">A pasta Atualizações pode ser usada somente para implantar atualizações de software durante uma instalação inicial do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="5a3be-110">The Updates folder can be used only to deploy software updates during an initial installation of Office 2013.</span></span>

<span data-ttu-id="5a3be-111">O OCT faz parte da instalação e está incluído em versões de licença de volume do produto.</span><span class="sxs-lookup"><span data-stu-id="5a3be-111">The OCT is part of setup and it is included in volume license versions of the product.</span></span> <span data-ttu-id="5a3be-112">Você executa a OCT digitando `setup.exe /admin` na linha de comando da raiz do ponto de instalação da rede que contém os arquivos de origem do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="5a3be-112">You run the OCT by typing `setup.exe /admin` at the command line from the root of the network installation point that contains the Office 2013 source files.</span></span> <span data-ttu-id="5a3be-113">Por exemplo, use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5a3be-113">For example, use the following:</span></span>

`\\server\share\Office15\setup.exe /admin`

<span data-ttu-id="5a3be-114">Os administradores usam o OCT para criar um arquivo .msp de personalização da instalação.</span><span class="sxs-lookup"><span data-stu-id="5a3be-114">Administrators use the OCT to create a setup customization .msp file.</span></span> <span data-ttu-id="5a3be-115">Como no Microsoft Office 2010 OCT, os administradores podem personalizar as seguintes áreas:</span><span class="sxs-lookup"><span data-stu-id="5a3be-115">As in the Microsoft Office 2010 OCT, administrators can customize the following areas:</span></span>

  - <span data-ttu-id="5a3be-116">**Configurar** Usado para especificar o local de instalação padrão no cliente e o nome da organização padrão, origens adicionais de instalação de rede, chave do produto, contrato de licença de usuário final, nível de exibição, versões anteriores do Office para remover, programas personalizados para executar durante a instalação, configurações de segurança e propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="5a3be-116">**Setup** Used to specify default installation location on the client and default organization name, additional network installation sources, product key, end-user license agreement, display level, earlier versions of Office to remove, custom programs to run during installation, security settings, and Setup properties.</span></span>

  - <span data-ttu-id="5a3be-117">**Recursos** do Usado para definir as configurações do usuário e para personalizar como os recursos do Office são instalados.</span><span class="sxs-lookup"><span data-stu-id="5a3be-117">**Features** Used to configure user settings and to customize how Office features are installed.</span></span> <span data-ttu-id="5a3be-118">Os administradores podem usar o OCT para especificar os valores padrões iniciais das configurações do aplicativo do Office para usuários.</span><span class="sxs-lookup"><span data-stu-id="5a3be-118">Administrators can use the OCT to specify initial default values of Office application settings for users.</span></span> <span data-ttu-id="5a3be-119">Os usuários podem modificar a maioria das configurações após a instalação.</span><span class="sxs-lookup"><span data-stu-id="5a3be-119">Users can modify most of the settings after the installation.</span></span>

  - <span data-ttu-id="5a3be-120">**Conteúdo adicional** Usado para adicionar ou remover arquivos, adicionar ou remover entradas do registro e configurar atalhos.</span><span class="sxs-lookup"><span data-stu-id="5a3be-120">**Additional content** Used to add or remove files, add or remove registry entries, and configure shortcuts.</span></span>

  - <span data-ttu-id="5a3be-121">**Outlook** Usado para personalizar o perfil padrão do Outlook de um usuário, especifique as configurações do Exchange, adicione contas, Remova contas e exporte configurações e especifique os grupos de recebimento de envio \\ .</span><span class="sxs-lookup"><span data-stu-id="5a3be-121">**Outlook** Used to customize a user's default Outlook profile, specify Exchange settings, add accounts, remove accounts and export settings, and specify Send\\Receive groups.</span></span>

<span data-ttu-id="5a3be-122">Para obter informações sobre a OCT, consulte <https://go.microsoft.com/fwlink/p/?linkid=267516> .</span><span class="sxs-lookup"><span data-stu-id="5a3be-122">For information about the OCT, see <https://go.microsoft.com/fwlink/p/?linkid=267516>.</span></span>

<span data-ttu-id="5a3be-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a3be-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

