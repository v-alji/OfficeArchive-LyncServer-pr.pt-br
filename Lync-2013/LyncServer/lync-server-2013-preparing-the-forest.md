---
title: 'Lync Server 2013: Preparando a floresta'
description: 'Lync Server 2013: preparando a floresta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the forest
ms:assetid: 3d188fcb-c64e-46cf-a3a7-9e3ebefed7fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425898(v=OCS.15)
ms:contentKeyID: 48183926
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 275d861ebfe7e0350e7baf120b6e6f2bae6a26ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424104"
---
# <a name="preparing-the-forest-for-lync-server-2013"></a><span data-ttu-id="5ba6b-103">Preparando a floresta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ba6b-103">Preparing the forest for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ba6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ba6b-104">

<span> </span></span></span>

<span data-ttu-id="5ba6b-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5ba6b-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5ba6b-106">A preparação da floresta cria configurações e objetos globais do Active Directory e grupos universais do Active Directory para uso pelo Lync Server 2013 e concede permissões de acesso adequadas nos objetos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5ba6b-106">Forest preparation creates Active Directory global settings and objects and Active Directory universal groups for use by Lync Server 2013, and grants suitable access permissions on the Active Directory objects.</span></span> <span data-ttu-id="5ba6b-107">Para obter uma descrição dos grupos universais e das configurações globais e dos objetos criados pela preparação da floresta, consulte [as alterações feitas pela preparação da floresta no Lync Server 2013](lync-server-2013-changes-made-by-forest-preparation.md).</span><span class="sxs-lookup"><span data-stu-id="5ba6b-107">For a description of the universal groups and the global settings and objects created by forest preparation, see [Changes made by forest preparation in Lync Server 2013](lync-server-2013-changes-made-by-forest-preparation.md).</span></span>

<span data-ttu-id="5ba6b-108">A preparação da floresta também cria objetos que contêm conjuntos de propriedades e especificadores de exibição que são usados pelo Lync Server 2013 e os armazena no contêiner de configuração.</span><span class="sxs-lookup"><span data-stu-id="5ba6b-108">Forest preparation also creates objects that contain property sets and display specifiers that are used by Lync Server 2013, and stores them in the Configuration container.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5ba6b-109">Verifique se as alterações de preparação do esquema foram duplicadas para todos os controladores de domínio antes de executar o procedimento de preparação da floresta.</span><span class="sxs-lookup"><span data-stu-id="5ba6b-109">Make sure that schema preparation changes have replicated to all domain controllers before performing the forest preparation procedure.</span></span> <span data-ttu-id="5ba6b-110">Se a duplicação não for completada, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="5ba6b-110">If replication is not completed, an error occurs.</span></span>



</div>

<span data-ttu-id="5ba6b-111">Se você estiver executando uma nova implantação do Lync Server, deverá armazenar as configurações globais no contêiner de configuração.</span><span class="sxs-lookup"><span data-stu-id="5ba6b-111">If you are performing a new Lync Server deployment, you must store global settings in the Configuration container.</span></span> <span data-ttu-id="5ba6b-112">Se você estiver atualizando de uma versão anterior e ainda armazenar configurações globais no contêiner do sistema, poderá continuar a usar o contêiner do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ba6b-112">If you are upgrading from an earlier version and you still store global settings in the System container, you can continue to use the System container.</span></span>

<span data-ttu-id="5ba6b-113">Você deve ser membro do grupo Administradores da empresa ou administradores de domínio do domínio raiz da floresta para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="5ba6b-113">You must be a member of the Enterprise Admins or Domain Admins group for the forest root domain to perform this procedure.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5ba6b-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5ba6b-114">In This Section</span></span>

  - [<span data-ttu-id="5ba6b-115">Executando preparação de floresta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ba6b-115">Running forest preparation for Lync Server 2013</span></span>](lync-server-2013-running-forest-preparation.md)

  - [<span data-ttu-id="5ba6b-116">Usando cmdlets para reverter preparação da floresta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ba6b-116">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)

<span data-ttu-id="5ba6b-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ba6b-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

