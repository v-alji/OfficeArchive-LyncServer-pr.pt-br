---
title: 'Lync Server 2013: regras de atualização de dispositivos'
description: 'Lync Server 2013: regras de atualização de dispositivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update rules
ms:assetid: a2f7e293-3342-4566-9605-410cb95f3b3b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994062(v=OCS.15)
ms:contentKeyID: 51803973
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd6d34c290f4a08f67143294fcc5dd18e1acf9d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429371"
---
# <a name="device-update-rules-in-lync-server-2013"></a><span data-ttu-id="9b24e-103">Regras de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b24e-103">Device Update rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9b24e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9b24e-104">

<span> </span></span></span>

<span data-ttu-id="9b24e-105">_**Tópico da última modificação:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="9b24e-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="9b24e-106">Periodicamente, a Microsoft lança um novo conjunto de atualizações de firmware de dispositivo para o Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="9b24e-106">Periodically, Microsoft releases a new set of device firmware updates for Lync Phone Edition.</span></span> <span data-ttu-id="9b24e-107">*As regras de atualização de dispositivo* associam atualizações de firmware com dispositivos de hardware — telefones e outros dispositivos que executam o Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="9b24e-107">*Device update rules* associate firmware updates with hardware devices—phones and other devices running Lync Phone Edition.</span></span>

<span data-ttu-id="9b24e-108">Para obter o conjunto mais recente de regras de atualização de dispositivos, acesse a página de ajuda e suporte no website da Microsoft e procure por "Phone Edition".</span><span class="sxs-lookup"><span data-stu-id="9b24e-108">To get the latest set of device update rules, go to the Help and Support page on the Microsoft website, and search for "Phone Edition."</span></span> <span data-ttu-id="9b24e-109">Baixe o pacote de atualização e extraia os arquivos para uma pasta no computador onde as atualizações serão carregadas.</span><span class="sxs-lookup"><span data-stu-id="9b24e-109">Download the update package, and extract the files to a folder on the computer where the updates are to be uploaded.</span></span> <span data-ttu-id="9b24e-110">Depois que os arquivos forem extraídos, importe as regras de atualização de dispositivo encontradas no arquivo extraído. Arquivo CAB (que tem o nome UCUpdates.cab).</span><span class="sxs-lookup"><span data-stu-id="9b24e-110">After the files have been extracted, import the device update rules found in the extracted .CAB file (which have the name UCUpdates.cab).</span></span> <span data-ttu-id="9b24e-111">Em seguida, use o painel de controle do Lync Server ou cmdlets do Windows PowerShell para exibir e gerenciar essas regras para os dispositivos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="9b24e-111">Then, use the Lync Server Control Panel or Windows PowerShell cmdlets to view and manage these rules for your organization’s devices.</span></span>

<span data-ttu-id="9b24e-112">Os tópicos a seguir explicam como importar, exibir e gerenciar as regras de atualização de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9b24e-112">The following topics tell you how to import, view, and manage device update rules.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9b24e-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9b24e-113">In This Section</span></span>

  - [<span data-ttu-id="9b24e-114">Exibir informações sobre as regras de atualização de dispositivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b24e-114">View information about Device Update rules in Lync Server 2013</span></span>](lync-server-2013-view-information-about-device-update-rules.md)

  - [<span data-ttu-id="9b24e-115">Importar regras de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b24e-115">Import Device Update rules in Lync Server 2013</span></span>](lync-server-2013-import-device-update-rules.md)

  - [<span data-ttu-id="9b24e-116">Aprovar uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b24e-116">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)

  - [<span data-ttu-id="9b24e-117">Remover uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b24e-117">Remove a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-remove-a-device-update-rule.md)

  - [<span data-ttu-id="9b24e-118">Redefinir uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b24e-118">Reset a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-reset-a-device-update-rule.md)

  - [<span data-ttu-id="9b24e-119">Restaurar uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9b24e-119">Restore a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-restore-a-device-update-rule.md)

<span data-ttu-id="9b24e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9b24e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

