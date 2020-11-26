---
title: 'Lync Server 2013: Configurando o Windows 8 para cartões inteligentes virtuais'
description: 'Lync Server 2013: Configurando o Windows 8 para cartões inteligentes virtuais.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Windows 8 for Virtual Smart Cards
ms:assetid: 4916c167-4ee3-4f3e-b65c-33e588595112
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308564(v=OCS.15)
ms:contentKeyID: 54973684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 112047f91a20dd552c628fb33eba7bb9ad3d0f01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432314"
---
# <a name="configuring-windows-8-for-using-virtual-smart-cards-with-lync-server-2013"></a><span data-ttu-id="b3317-103">Configurar o Windows 8 para usar cartões inteligentes virtuais com o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3317-103">Configuring Windows 8 for using Virtual Smart Cards with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3317-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3317-104">

<span> </span></span></span>

<span data-ttu-id="b3317-105">_**Tópico da última modificação:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="b3317-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="b3317-106">Um fator que deve ser levado em consideração na implantação da autenticação de dois fatores e na tecnologia de cartão inteligente é o custo da implementação.</span><span class="sxs-lookup"><span data-stu-id="b3317-106">One factor to consider when deploying two-factor authentication and smart card technology is the cost of implementation.</span></span> <span data-ttu-id="b3317-107">O Windows 8 fornece vários recursos de segurança novos, e um dos novos recursos mais interessantes é o suporte para cartões inteligentes virtuais.</span><span class="sxs-lookup"><span data-stu-id="b3317-107">Windows 8 provides a number of new security capabilities, and one of the most interesting new features is support for virtual smart cards.</span></span>

<span data-ttu-id="b3317-108">Para computadores que contam com um chip Trusted Platform Module (TPM) compatível com a especificação da versão 1.2, as organizações podem agora se beneficiar do logon com cartões inteligentes sem fazer mais nenhum investimento em hardware.</span><span class="sxs-lookup"><span data-stu-id="b3317-108">For computers equipped with a Trusted Platform Module (TPM) chip that meets specification version 1.2, organizations can now get the benefits of smart card logon without making any additional investments in hardware.</span></span> <span data-ttu-id="b3317-109">Para obter mais informações, consulte usando cartões inteligentes virtuais com o Windows 8 em [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365) .</span><span class="sxs-lookup"><span data-stu-id="b3317-109">For more information, see Using Virtual Smart Cards with Windows 8 at [https://go.microsoft.com/fwlink/p/?LinkId=313365](https://go.microsoft.com/fwlink/p/?linkid=313365).</span></span>

<div>

## <a name="to-configure-windows-8-for-virtual-smart-cards"></a><span data-ttu-id="b3317-110">Para configurar o Windows 8 para cartões inteligentes virtuais</span><span class="sxs-lookup"><span data-stu-id="b3317-110">To Configure Windows 8 for Virtual Smart Cards</span></span>

1.  <span data-ttu-id="b3317-111">Faça logon no computador com o Windows 8 usando as credenciais de um usuário compatível com o Lync.</span><span class="sxs-lookup"><span data-stu-id="b3317-111">Log in to the Windows 8 computer using the credentials of a Lync-enabled user.</span></span>

2.  <span data-ttu-id="b3317-112">Na tela Iniciar do Windows 8, mova seu cursor para o canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="b3317-112">At the Windows 8 Start screen, move your cursor to the bottom right corner of the screen.</span></span>

3.  <span data-ttu-id="b3317-113">Selecione a opção **Pesquisar** e pesquise **Command Prompt**.</span><span class="sxs-lookup"><span data-stu-id="b3317-113">Select the **Search** option, and then search for **Command Prompt**.</span></span>

4.  <span data-ttu-id="b3317-114">Clique com o botão direito do mouse em **Prompt de comando** e selecione **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="b3317-114">Right click on **Command Prompt**, and then select **Run as Administrator**.</span></span>

5.  <span data-ttu-id="b3317-115">Abra o Console de Gerenciamento do Trusted Platform Module (TPM) executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b3317-115">Open the Trusted Platform Module (TPM) Management console by running the following command:</span></span>
    
        Tpm.msc

6.  <span data-ttu-id="b3317-116">No Console de Gerenciamento do TPM, confira se a versão do seu TPM é 1.2 ou superior.</span><span class="sxs-lookup"><span data-stu-id="b3317-116">From the TPM management console, verify that your TPM specification version is at least 1.2</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b3317-117">Caso surja uma caixa de diálogo com a mensagem de que não foi possível encontrar o Trust Platform Module (TPM) compatível, verifique se o computador tem um módulo TPM compatível e se ele está habilitado na BIOS do sistema.</span><span class="sxs-lookup"><span data-stu-id="b3317-117">If you receive a dialog stating that a Compatible Trust Platform Module (TPM) cannot be found, verify that the computer has a compatible TPM module and that it is enabled in the system BIOS.</span></span>

    
    </div>

7.  <span data-ttu-id="b3317-118">Feche o Console de Gerenciamento do TPM</span><span class="sxs-lookup"><span data-stu-id="b3317-118">Close the TPM management console</span></span>

8.  <span data-ttu-id="b3317-119">No prompt de comando, crie um novo cartão inteligente virtual usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b3317-119">From the command prompt, create a new virtual smart card using the following command:</span></span>
    
        TpmVscMgr create /name MyVSC /pin default /adminkey random /generate
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b3317-120">Para personalizar o valor do PIN ao criar o cartão inteligente virtual, use o prompt /pin.</span><span class="sxs-lookup"><span data-stu-id="b3317-120">To provide a custom PIN value when creating the virtual smart card, use /pin prompt instead.</span></span>

    
    </div>

9.  <span data-ttu-id="b3317-121">No prompt de comando, abre o Console de Gerenciamento do computador executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b3317-121">From the command prompt, open the Computer Management console by running the following command:</span></span>
    
        CompMgmt.msc

10. <span data-ttu-id="b3317-122">No Console de Gerenciamento do computador, selecione **Gerenciamento de Dispositivos**.</span><span class="sxs-lookup"><span data-stu-id="b3317-122">In the Computer Management console, select **Device Management**.</span></span>

11. <span data-ttu-id="b3317-123">Expanda **Leitores de cartão inteligente**.</span><span class="sxs-lookup"><span data-stu-id="b3317-123">Expand **Smart card readers**.</span></span>

12. <span data-ttu-id="b3317-124">Verifique se o novo leitor de cartão inteligente virtual foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b3317-124">Verify that the new virtual smart card reader has been created successfully.</span></span>

<span data-ttu-id="b3317-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3317-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

