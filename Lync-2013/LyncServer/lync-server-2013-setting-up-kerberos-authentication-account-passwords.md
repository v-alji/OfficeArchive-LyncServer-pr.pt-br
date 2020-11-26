---
title: 'Lync Server 2013: Configurando senhas da conta de autenticação Kerberos'
description: 'Lync Server 2013: configurar senhas da conta de autenticação Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication account passwords
ms:assetid: b435f88e-4a77-4be7-b7e5-c17484303b74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412870(v=OCS.15)
ms:contentKeyID: 48185167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614b1411f9454c39843f4e69cabbfc3b02986e51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423965"
---
# <a name="setting-up-kerberos-authentication-account-passwords-in-lync-server-2013"></a><span data-ttu-id="27a93-103">Configurando senhas da conta de autenticação Kerberos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27a93-103">Setting up Kerberos authentication account passwords in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="27a93-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="27a93-104">

<span> </span></span></span>

<span data-ttu-id="27a93-105">_**Tópico da última modificação:** 2010-11-03_</span><span class="sxs-lookup"><span data-stu-id="27a93-105">_**Topic Last Modified:** 2010-11-03_</span></span>

<span data-ttu-id="27a93-106">Depois de criar o objeto de computador para a conta de autenticação Kerberos, você pode configurar a senha da conta.</span><span class="sxs-lookup"><span data-stu-id="27a93-106">After you create the computer object for the Kerberos authentication account, you can set up the password for the account.</span></span> <span data-ttu-id="27a93-107">Você executa o cmdlet do Windows PowerShell para configurar a senha da conta Kerberos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="27a93-107">You run the Windows PowerShell cmdlet for setting the Kerberos account password on one server.</span></span> <span data-ttu-id="27a93-108">Você pode definir a senha no objeto que você criou para a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="27a93-108">You can set the password on the object that you created for the Kerberos authentication.</span></span> <span data-ttu-id="27a93-109">A senha pode ser definida como um valor conhecido, mas, por padrão, é uma senha aleatória.</span><span class="sxs-lookup"><span data-stu-id="27a93-109">The password can be set to a known value, but by default is a random password.</span></span> <span data-ttu-id="27a93-110">A senha está disponível para todas as fontes de autenticação Kerberos que usam a conta.</span><span class="sxs-lookup"><span data-stu-id="27a93-110">The password is available to all Kerberos authentication sources that use the account.</span></span> <span data-ttu-id="27a93-111">Você usa cmdlets do Windows PowerShell para configurar e gerenciar senhas de conta Kerberos.</span><span class="sxs-lookup"><span data-stu-id="27a93-111">You use Windows PowerShell cmdlets to set up and manage Kerberos account passwords.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="27a93-112">O objeto de conta Kerberos é um objeto de computador, mas usa o parâmetro USERACCOUNT para operações nos cmdlets do Windows PowerShell referenciados.</span><span class="sxs-lookup"><span data-stu-id="27a93-112">The Kerberos account object is a computer object, but uses the UserAccount parameter for operations in the Windows PowerShell cmdlets that are referenced.</span></span> <span data-ttu-id="27a93-113">Observe que isso não é um erro, mas o comportamento pretendido do cmdlet quando usado com a criação e a manutenção da conta Kerberos.</span><span class="sxs-lookup"><span data-stu-id="27a93-113">Note that this is not a mistake, but the intended behavior of the cmdlet when used with the Kerberos account creation and maintenance.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="27a93-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="27a93-114">In This Section</span></span>

  - [<span data-ttu-id="27a93-115">Configurar uma senha da conta de autenticação Kerberos authentication em um servidor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27a93-115">Set a Kerberos authentication account password on a server in Lync Server 2013</span></span>](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)

  - [<span data-ttu-id="27a93-116">Sincronizar uma senha de conta de autenticação Kerberos com o IIS no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="27a93-116">Synchronize a Kerberos authentication account password to IIS in Lync Server 2013</span></span>](lync-server-2013-synchronize-a-kerberos-authentication-account-password-to-iis.md)

<span data-ttu-id="27a93-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="27a93-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

