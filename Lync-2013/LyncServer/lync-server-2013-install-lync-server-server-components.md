---
title: 'Lync Server 2013: Instalar componentes de servidor do Lync Server'
description: 'Lync Server 2013: instalar componentes do servidor do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server server components
ms:assetid: 186aed6e-7adf-4a92-9f2e-f9a4de5ff202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398239(v=OCS.15)
ms:contentKeyID: 48183528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1930926f3a46be868d838abf646eb8702c9713a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427163"
---
# <a name="install-server-components-for-lync-server-2013"></a><span data-ttu-id="e9db4-103">Instalar componentes de servidor para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9db4-103">Install server components for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9db4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9db4-104">

<span> </span></span></span>

<span data-ttu-id="e9db4-105">_**Tópico da última modificação:** 2014-05-05_</span><span class="sxs-lookup"><span data-stu-id="e9db4-105">_**Topic Last Modified:** 2014-05-05_</span></span>

<span data-ttu-id="e9db4-106">Antes de seguir essas etapas, verifique se você está conectado ao servidor com uma conta de usuário de domínio que seja um administrador local e um membro do grupo RTCUniversalReadOnlyAdmins no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9db4-106">Before following these steps, make sure you’re logged onto the server with a domain user account that’s both a local administrator and a member of the RTCUniversalReadOnlyAdmins group in Active Directory.</span></span>

<span data-ttu-id="e9db4-107">O assistente de implantação do Lync Server é usado para instalar os componentes necessários para cada função do Lync Server e ativar o servidor.</span><span class="sxs-lookup"><span data-stu-id="e9db4-107">The Lync Server Deployment Wizard is used to install the needed components for each Lync server role and to activate the server.</span></span> <span data-ttu-id="e9db4-108">Este artigo orienta você pelas etapas de implantação de um servidor Standard Edition ou de um servidor front-end na sua infraestrutura do Lync.</span><span class="sxs-lookup"><span data-stu-id="e9db4-108">This article walks you through the steps of deploying a Standard Edition server or a Front End Server in your Lync infrastructure.</span></span>

<div>

## <a name="to-install-lync-server-components"></a><span data-ttu-id="e9db4-109">Para instalar os componentes do Lync Server</span><span class="sxs-lookup"><span data-stu-id="e9db4-109">To install Lync Server components</span></span>

1.  <span data-ttu-id="e9db4-110">Se o assistente de implantação do Lync Server não estiver em execução, inicie-o no servidor em que você deseja instalar o Lync.</span><span class="sxs-lookup"><span data-stu-id="e9db4-110">If the Lync Server Deployment Wizard isn’t running, start it on the server you want to install Lync onto.</span></span>

2.  <span data-ttu-id="e9db4-111">Clique em **instalar ou atualizar o sistema do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e9db4-111">Click **Install or Update Lync Server System**.</span></span>

3.  <span data-ttu-id="e9db4-112">No assistente de implantação, confirme se a **etapa 1: instalar o repositório de configuração local** tem uma marca de seleção verde, o que significa que o servidor tem uma cópia local da loja instalada com êxito.</span><span class="sxs-lookup"><span data-stu-id="e9db4-112">In the Deployment Wizard, confirm that **Step 1: Install Local Configuration Store** has a green check mark, which means that this server has a local copy of the store installed successfully.</span></span> <span data-ttu-id="e9db4-113">Se não estiver marcada, você precisará instalar o repositório de configuração local no servidor.</span><span class="sxs-lookup"><span data-stu-id="e9db4-113">If it’s not checked, you need to install the Local Configuration store on the server.</span></span> <span data-ttu-id="e9db4-114">Siga as etapas em [instalar o repositório de configuração local no Lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) e, em seguida, volte aqui.</span><span class="sxs-lookup"><span data-stu-id="e9db4-114">Follow the steps at [Install the Local Configuration store in Lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) and then come back here.</span></span>

4.  <span data-ttu-id="e9db4-115">Quando estiver pronto para instalar os componentes do Lync Server 2013 em seu servidor, clique em **executar** ao lado da **etapa 2: configurar ou remover componentes do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e9db4-115">When you’re ready to install the Lync Server 2013 components on your server, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

5.  <span data-ttu-id="e9db4-116">Na página **configurar componentes do Lync Server** , clique em **Avançar** para configurar componentes conforme definido na sua topologia publicada.</span><span class="sxs-lookup"><span data-stu-id="e9db4-116">On the **Set Up Lync Server Components** page, click **Next** to set up components as defined in your published topology.</span></span>

6.  <span data-ttu-id="e9db4-117">A página **comandos em execução** exibirá um resumo dos comandos e informações de instalação à medida que a configuração ocorre.</span><span class="sxs-lookup"><span data-stu-id="e9db4-117">The **Executing Commands** page will display a summary of commands and installation information as the set up takes place.</span></span> <span data-ttu-id="e9db4-118">Quando terminar, use a lista para selecionar um log para exibição e clique em **Exibir Log**.</span><span class="sxs-lookup"><span data-stu-id="e9db4-118">When it’s done, you can use the list to select a log to view, and then click **View Log**.</span></span>

7.  <span data-ttu-id="e9db4-119">Quando a instalação dos componentes do Lync Server 2013 for concluída e você tiver revisado os logs conforme necessário, clique em **concluir** para concluir esta etapa na instalação.</span><span class="sxs-lookup"><span data-stu-id="e9db4-119">When Lync Server 2013 components setup is done, and you’ve reviewed the logs as needed, click **Finish** to complete this step in the installation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9db4-120">Se você for solicitado a reiniciar o servidor (o que pode acontecer se a experiência da área de trabalho do Windows precisar ser instalada), definitivamente faça isso.</span><span class="sxs-lookup"><span data-stu-id="e9db4-120">If you’re prompted to restart the server (which might happen if Windows Desktop Experience needed to be installed), definitely do that.</span></span> <span data-ttu-id="e9db4-121">Quando o computador estiver em operação de backup e em execução, você precisará executar essas etapas novamente, começando da etapa três listadas acima (basicamente, execute a etapa 2 no assistente de implantação mais uma vez).</span><span class="sxs-lookup"><span data-stu-id="e9db4-121">When the computer is back up and running, you need to do these steps over again, starting from step three listed above (basically run Step 2 in the Deployment Wizard one more time).</span></span>

    
    <span data-ttu-id="e9db4-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9db4-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

