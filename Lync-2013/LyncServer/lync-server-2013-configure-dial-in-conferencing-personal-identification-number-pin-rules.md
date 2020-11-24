---
title: Configurar regras de PIN (número de identificação pessoal) da conferência discada
description: Configurar regras de PIN (número de identificação pessoal) de conferência discada.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing personal identification number (PIN) rules
ms:assetid: 27b79fb1-e2dc-4f71-bc82-b6eb61be2b16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520967(v=OCS.15)
ms:contentKeyID: 48183668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 799092ba57e9a85cd196840fc81c1f46b96e9900
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390360"
---
# <a name="configure-dial-in-conferencing-personal-identification-number-pin-rules-in-lync-server-2013"></a><span data-ttu-id="7643d-103">Configurar regras de PIN (número de identificação pessoal) da conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7643d-103">Configure dial-in conferencing personal identification number (PIN) rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7643d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7643d-104">

<span> </span></span></span>

<span data-ttu-id="7643d-105">_**Tópico da última modificação:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="7643d-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="7643d-106">Os usuários do Lync Server 2013 que têm credenciais do AD DS (serviços de domínio Active Directory) em sua organização podem ingressar em conferências discadas como usuários autenticados usando um PIN (número de identificação pessoal).</span><span class="sxs-lookup"><span data-stu-id="7643d-106">Lync Server 2013 users who have Active Directory Domain Services (AD DS) credentials in your organization can join dial-in conferences as authenticated users by using a personal identification number (PIN).</span></span> <span data-ttu-id="7643d-107">A política de PIN define as regras de funcionamento dos PINs de conferências de discagem.</span><span class="sxs-lookup"><span data-stu-id="7643d-107">PIN policy defines the rules for how dial-in conferencing PINs work.</span></span>

<span data-ttu-id="7643d-108">É possível criar uma nova política de PIN se você quiser que uma política específica seja aplicada a um site ou a determinado grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="7643d-108">You can create a new PIN policy if you want a specific policy to apply to a site or to a certain group of users.</span></span> <span data-ttu-id="7643d-109">Se você quiser usar a mesma política de PIN para toda a organização, utilize a política de PIN global e modifique-a conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7643d-109">If you want to use the same PIN policy for your entire organization, you can use the global PIN policy and modify it as needed.</span></span> <span data-ttu-id="7643d-110">As políticas de PIN se aplicam aos usuários do escopo mais estreito para o mais amplo.</span><span class="sxs-lookup"><span data-stu-id="7643d-110">PIN policies apply to users from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="7643d-111">Se você atribuir uma política de PIN no nível de usuário a um usuário, essas configurações terão precedência.</span><span class="sxs-lookup"><span data-stu-id="7643d-111">If you assign a user-level PIN policy to a user, those settings take precedence.</span></span> <span data-ttu-id="7643d-112">Se você não atribuir uma política de usuário, a política de PIN no nível de site será aplicada, se existir.</span><span class="sxs-lookup"><span data-stu-id="7643d-112">If you do not assign a user policy, the site-level PIN policy applies, if it exists.</span></span> <span data-ttu-id="7643d-113">Se nenhuma política de usuário ou site se aplicar, a política de PIN global fornecerá as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="7643d-113">If no user or site policies apply, global PIN policy provides the default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7643d-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7643d-114">In This Section</span></span>

  - [<span data-ttu-id="7643d-115">Modificar as configurações de PIN de conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7643d-115">Modify the default dial-in conferencing PIN settings in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-dial-in-conferencing-pin-settings.md)

  - [<span data-ttu-id="7643d-116">Criar ou modificar as configurações de PIN de conferência discada no Lync Server 2013 para um site ou grupo de usuários</span><span class="sxs-lookup"><span data-stu-id="7643d-116">Create or modify dial-in conferencing PIN settings in Lync Server 2013 for a site or group of users</span></span>](lync-server-2013-create-or-modify-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

  - [<span data-ttu-id="7643d-117">Excluir configurações de PIN de conferência discada de um site ou grupo de usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7643d-117">Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013</span></span>](lync-server-2013-delete-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

<span data-ttu-id="7643d-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7643d-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

