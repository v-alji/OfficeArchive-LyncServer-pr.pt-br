---
title: 'Lync Server 2013: verificando se há atualizações para o analisador de práticas recomendadas'
description: 'Lync Server 2013: verificando se há atualizações para o analisador de práticas recomendadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking for updates to Best Practices Analyzer
ms:assetid: 06f1da8b-99a7-4871-911e-bfb7542baced
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204645(v=OCS.15)
ms:contentKeyID: 48183307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c2662f143be9fc672461715d1c3da867886e686
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434906"
---
# <a name="checking-for-updates-to-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="5abc2-103">Verificando se há atualizações para o analisador de práticas recomendadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5abc2-103">Checking for updates to Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5abc2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5abc2-104">

<span> </span></span></span>

<span data-ttu-id="5abc2-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5abc2-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5abc2-106">Quando você inicia o analisador de práticas recomendadas, a ferramenta oferece uma opção para pesquisar as atualizações mais recentes da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5abc2-106">When you start Best Practices Analyzer, the tool provides you with an option to search for the latest updates to the tool.</span></span> <span data-ttu-id="5abc2-107">Se houver uma atualização disponível, você pode baixar a atualização.</span><span class="sxs-lookup"><span data-stu-id="5abc2-107">If an update is available, you can download the update.</span></span> <span data-ttu-id="5abc2-108">Se você optar por não baixar as atualizações ou se o analisador de práticas recomendadas não conseguir acessar a Internet, você poderá continuar a usar a versão que já está no computador.</span><span class="sxs-lookup"><span data-stu-id="5abc2-108">If you choose not to download updates, or if Best Practices Analyzer cannot access the Internet, you can continue to use the version that is already on the computer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5abc2-109">Se você precisar de autenticação de proxy para acessar a Internet, o analisador de práticas recomendadas não poderá acessar novas atualizações para download.</span><span class="sxs-lookup"><span data-stu-id="5abc2-109">If you need proxy authentication to access the Internet, Best Practices Analyzer cannot access new updates for you to download.</span></span> <span data-ttu-id="5abc2-110">No entanto, você pode baixar manualmente a versão mais recente do RtcBPA.msi a partir do centro de download da Microsoft em <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A> .</span><span class="sxs-lookup"><span data-stu-id="5abc2-110">However, you can manually download the latest version of RtcBPA.msi from the Microsoft Download Center at <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A>.</span></span> <span data-ttu-id="5abc2-111">Depois de baixar o arquivo, você pode copiá-lo para o computador no qual deseja atualizar o analisador de práticas recomendadas e usar o arquivo. msi para instalar a nova versão da ferramenta nesse computador.</span><span class="sxs-lookup"><span data-stu-id="5abc2-111">After downloading the file, you can copy it to the computer on which you want to update Best Practices Analyzer and use the .msi file to install the new version of the tool on that computer.</span></span>



</div>

<span data-ttu-id="5abc2-112">Para atualizar as regras do analisador de práticas recomendadas, você deve executar a ferramenta como administrador no computador local.</span><span class="sxs-lookup"><span data-stu-id="5abc2-112">To update Best Practices Analyzer rules, you must run the tool as an Administrator on the local computer.</span></span> <span data-ttu-id="5abc2-113">Se você não estiver conectado usando uma conta que seja membro do grupo Administradores e atualizações sejam detectadas, feche o analisador de práticas recomendadas e use o procedimento a seguir para iniciar o programa.</span><span class="sxs-lookup"><span data-stu-id="5abc2-113">If you are not logged on using an account that is a member of the Administrators group and updates are detected, close Best Practices Analyzer, and then use the following procedure to start the program.</span></span>

<div>

## <a name="to-open-best-practices-analyzer-as-administrator-to-check-for-updates"></a><span data-ttu-id="5abc2-114">Para abrir o analisador de práticas recomendadas como administrador para verificar se há atualizações</span><span class="sxs-lookup"><span data-stu-id="5abc2-114">To open Best Practices Analyzer as Administrator to check for updates</span></span>

1.  <span data-ttu-id="5abc2-115">Em um computador no qual o Best Practices Analyzer está instalado, clique em **Iniciar**, aponte para **Microsoft Lync Server 2013**, clique com o botão direito do mouse em **analisador de práticas recomendadas** e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="5abc2-115">On a computer on which Best Practices Analyzer is installed, click **Start**, point to **Microsoft Lync Server 2013**, right-click **Best Practices Analyzer**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="5abc2-116">Especifique as credenciais de uma conta que seja membro do grupo Administradores.</span><span class="sxs-lookup"><span data-stu-id="5abc2-116">Specify credentials of an account that is a member of the Administrators group.</span></span>

<span data-ttu-id="5abc2-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5abc2-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

