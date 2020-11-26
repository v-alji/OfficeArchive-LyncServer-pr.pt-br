---
title: 'Lync Server 2013: Configurando o AD FS 2,0 para dar suporte à autenticação de cliente'
description: 'Lync Server 2013: Configurando o AD FS 2,0 para dar suporte à autenticação de cliente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring AD FS 2.0 to support client authentication
ms:assetid: 4d93d400-ccaa-4da8-a71b-d05d7ba79d93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308565(v=OCS.15)
ms:contentKeyID: 54973687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 156eb6d7e8af85dec04601ab8f88c55181db20d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433392"
---
# <a name="configuring-ad-fs-20-to-support-client-authentication-in-lync-server-2013"></a><span data-ttu-id="d8a69-103">Configurando o AD FS 2,0 para dar suporte à autenticação de cliente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8a69-103">Configuring AD FS 2.0 to support client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8a69-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8a69-104">

<span> </span></span></span>

<span data-ttu-id="d8a69-105">_**Tópico da última modificação:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="d8a69-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="d8a69-106">Há dois tipos possíveis de autenticação que podem ser configurados para permitir que o AD FS 2.0 suporte autenticações utilizando cartões inteligentes:</span><span class="sxs-lookup"><span data-stu-id="d8a69-106">There are two possible authentication types that can be configured to allow AD FS 2.0 to support authentication using smart cards:</span></span>

  - <span data-ttu-id="d8a69-107">Autenticação baseada em formulário (FBA)</span><span class="sxs-lookup"><span data-stu-id="d8a69-107">Forms-based authentication (FBA)</span></span>

  - <span data-ttu-id="d8a69-108">Autenticação de Cliente de Segurança na Camada de Transporte</span><span class="sxs-lookup"><span data-stu-id="d8a69-108">Transport Layer Security Client Authentication</span></span>

<span data-ttu-id="d8a69-109">Utilizando a autenticação baseada em formulários, você pode desenvolver uma página da Web que permite que os usuários autentiquem usando seus nomes de usuário/senhas ou usando o cartão inteligente e o PIN.</span><span class="sxs-lookup"><span data-stu-id="d8a69-109">Using forms-based authentication, you can develop a web page that allows users to authenticate either by using their username/password or by using their smart card and PIN.</span></span> <span data-ttu-id="d8a69-110">Este tópico tem como foco como implementar a Autenticação de Cliente de Segurança na Camada de Transporte com o AD FS 2.0.</span><span class="sxs-lookup"><span data-stu-id="d8a69-110">This topic focuses on how to implement Transport Layer Security Client Authentication with AD FS 2.0.</span></span> <span data-ttu-id="d8a69-111">Para obter mais informações sobre os tipos de autenticação do AD FS 2,0, consulte AD FS 2,0: como alterar o tipo de autenticação local em [https://go.microsoft.com/fwlink/p/?LinkId=313384](https://go.microsoft.com/fwlink/p/?linkid=313384) .</span><span class="sxs-lookup"><span data-stu-id="d8a69-111">For more information about AD FS 2.0 authentication types, see AD FS 2.0: How to Change the Local Authentication Type at [https://go.microsoft.com/fwlink/p/?LinkId=313384](https://go.microsoft.com/fwlink/p/?linkid=313384).</span></span>

<div>


<span data-ttu-id="d8a69-112">**Para configurar o AD FS 2.0 para suportar a autenticação de cliente**</span><span class="sxs-lookup"><span data-stu-id="d8a69-112">**To Configure AD FS 2.0 to Support Client Authentication**</span></span>

1.  <span data-ttu-id="d8a69-113">Faça logon no computador do AD FS 2.0 utilizando uma conta de Administrador de Domínio.</span><span class="sxs-lookup"><span data-stu-id="d8a69-113">Log in to the AD FS 2.0 computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="d8a69-114">Inicie o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="d8a69-114">Launch Windows Explorer.</span></span>

3.  <span data-ttu-id="d8a69-115">Navegue até C: \\ Inetpub \\ ADFS \\ ls</span><span class="sxs-lookup"><span data-stu-id="d8a69-115">Browse to C:\\inetpub\\adfs\\ls</span></span>

4.  <span data-ttu-id="d8a69-116">Faça uma cópia de backup do arquivo web.config existente.</span><span class="sxs-lookup"><span data-stu-id="d8a69-116">Make a backup copy of the existing web.config file.</span></span>

5.  <span data-ttu-id="d8a69-117">Abra o arquivo web.config existente utilizando o Bloco de Notas.</span><span class="sxs-lookup"><span data-stu-id="d8a69-117">Open the existing web.config file using Notepad.</span></span>

6.  <span data-ttu-id="d8a69-118">Na barra de Menu, selecione **Editar** e, em seguida, selecione **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="d8a69-118">From the Menu bar, select **Edit** and then select **Find**.</span></span>

7.  <span data-ttu-id="d8a69-119">Pesquisar **\<localAuthenticationTypes\>** .</span><span class="sxs-lookup"><span data-stu-id="d8a69-119">Search for **\<localAuthenticationTypes\>**.</span></span>
    
    <span data-ttu-id="d8a69-120">Observe que há quatro tipos de autenticação listados, um por linha.</span><span class="sxs-lookup"><span data-stu-id="d8a69-120">Note that there are four authentication types listed, one per line.</span></span>

8.  <span data-ttu-id="d8a69-121">Mova para a linha que contém o tipo de autenticação TLSClient para o topo da lista na seção.</span><span class="sxs-lookup"><span data-stu-id="d8a69-121">Move the line containing the TLSClient authentication type to the top of the list in the section.</span></span>

9.  <span data-ttu-id="d8a69-122">Salve e Feche o arquivo web.config.</span><span class="sxs-lookup"><span data-stu-id="d8a69-122">Save and Close the web.config file.</span></span>

10. <span data-ttu-id="d8a69-123">Inicie um Prompt de Comando com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="d8a69-123">Launch a Command Prompt with elevated privileges.</span></span>

11. <span data-ttu-id="d8a69-124">Reinicie o IIS executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d8a69-124">Restart IIS by running the following command:</span></span>
    
        IISReset /Restart /NoForce

<span data-ttu-id="d8a69-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8a69-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

