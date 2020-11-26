---
title: 'Lync Server 2013: Preparando domínios'
description: 'Lync Server 2013: preparando domínios.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing domains
ms:assetid: 8eea541c-5f9d-4afc-92a8-a31d6f742544
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398721(v=OCS.15)
ms:contentKeyID: 48184816
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7700bbdd10a96949f892858ae03da8de60d86a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424160"
---
# <a name="preparing-domains-for-lync-server-2013"></a><span data-ttu-id="b43d3-103">Preparando domínios para Server 2013</span><span class="sxs-lookup"><span data-stu-id="b43d3-103">Preparing domains for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b43d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b43d3-104">

<span> </span></span></span>

<span data-ttu-id="b43d3-105">_**Tópico da última modificação:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="b43d3-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="b43d3-106">Preparação do domínio é a etapa final na preparação dos serviços de domínio Active Directory para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b43d3-106">Domain preparation is the final step in preparing Active Directory Domain Services for Lync Server 2013.</span></span> <span data-ttu-id="b43d3-107">A etapa de preparação do domínio adiciona entradas de controle de acesso (ACEs) necessárias aos grupos universais que concedem permissões para hospedar e gerenciar usuários no domínio.</span><span class="sxs-lookup"><span data-stu-id="b43d3-107">The domain preparation step adds the necessary access control entries (ACEs) to universal groups that grant permissions to host and manage users within the domain.</span></span> <span data-ttu-id="b43d3-108">A preparação do domínio cria ACEs no domínio raiz e três contêiners integrados: Usuário, Computadores e Controladores de Domínio.</span><span class="sxs-lookup"><span data-stu-id="b43d3-108">Domain preparation creates ACEs on the domain root and three built-in containers: User, Computers, and Domain Controllers.</span></span>

<span data-ttu-id="b43d3-109">Você pode executar a preparação do domínio em qualquer computador do domínio no qual você está implantando o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b43d3-109">You can run domain preparation on any computer in the domain where you are deploying Lync Server.</span></span> <span data-ttu-id="b43d3-110">Você deve preparar cada domínio que hospedará o Lync Server ou os usuários.</span><span class="sxs-lookup"><span data-stu-id="b43d3-110">You must prepare every domain that will host Lync Server or users.</span></span>

<span data-ttu-id="b43d3-111">Se a herança de permissões estiver desabilitada ou as permissões de usuário autenticadas estiverem desabilitadas em sua organização, você deverá executar etapas adicionais durante a preparação do domínio.</span><span class="sxs-lookup"><span data-stu-id="b43d3-111">If permissions inheritance is disabled or authenticated user permissions are disabled in your organization, you must perform additional steps during domain preparation.</span></span> <span data-ttu-id="b43d3-112">Para obter detalhes, consulte [preparando um serviço de domínio do Active Directory bloqueado no Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="b43d3-112">For details, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md).</span></span>

<span data-ttu-id="b43d3-113">Se sua organização usa unidades organizacionais (OU) em vez de três recipientes internos (ou seja, usuários, computadores e controladores de domínio), você deve conceder acesso de leitura às UOs do grupo usuários autenticados.</span><span class="sxs-lookup"><span data-stu-id="b43d3-113">If your organization uses organizational units (OU) instead of the three built-in containers (that is, Users, Computers, and Domain Controllers), you must grant read access to the OUs for the Authenticated Users group.</span></span> <span data-ttu-id="b43d3-114">O acesso de leitura aos recipientes é necessário para a preparação do domínio.</span><span class="sxs-lookup"><span data-stu-id="b43d3-114">Read access to the containers is required for domain preparation.</span></span> <span data-ttu-id="b43d3-115">Se o grupo usuários autenticados não tiver acesso de leitura à OU, execute o cmdlet **Grant-CsOuPermission** conforme ilustrado nos exemplos de código a seguir para conceder permissões de leitura para cada UO.</span><span class="sxs-lookup"><span data-stu-id="b43d3-115">If the Authenticated Users group does not have read access to the OU, run the **Grant-CsOuPermission** cmdlet as illustrated in the following code examples to grant read permissions for each OU.</span></span>

   ```PowerShell
    Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU > 
   ```

   ```PowerShell
    Grant-CsOuPermission -ObjectType "user","contact",inetOrgPerson" -OU "ou=Redmond,dc=contoso,dc=net"
   ```

<span data-ttu-id="b43d3-116">Para obter detalhes sobre o cmdlet **Grant-CsOuPermission** , consulte a documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b43d3-116">For details about the **Grant-CsOuPermission** cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div class="">


> [!TIP]  
> <span data-ttu-id="b43d3-117">Para obter detalhes sobre os ases criados na raiz do domínio e nos contêineres usuários, computadores e controladores de domínio, consulte <A href="lync-server-2013-changes-made-by-domain-preparation.md">alterações feitas pela preparação do domínio no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="b43d3-117">For details about the ACEs created on the domain root and in the Users, Computers, and Domain Controllers containers, see <A href="lync-server-2013-changes-made-by-domain-preparation.md">Changes made by domain preparation in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b43d3-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b43d3-118">In This Section</span></span>

  - [<span data-ttu-id="b43d3-119">Executando preparação de domínio para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b43d3-119">Running domain preparation for Lync Server 2013</span></span>](lync-server-2013-running-domain-preparation.md)

  - [<span data-ttu-id="b43d3-120">Usando cmdlets para reverter a preparação do domínio para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b43d3-120">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)

<span data-ttu-id="b43d3-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b43d3-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

