---
title: 'Lync Server 2013: configurar a telefonia de um usuário'
description: 'Lync Server 2013: configurar a telefonia para um usuário.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure telephony for a user
ms:assetid: 4546432e-c839-4517-a2c5-bc0d4d8c6a03
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520988(v=OCS.15)
ms:contentKeyID: 48183987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b82cecb67ea11928d187bd2a4a00625fbca7b23e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433651"
---
# <a name="configure-telephony-for-a-user-in-lync-server-2013"></a><span data-ttu-id="89b26-103">Configurar a telefonia para um usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89b26-103">Configure telephony for a user in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89b26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89b26-104">

<span> </span></span></span>

<span data-ttu-id="89b26-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="89b26-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="89b26-106">As configurações de telefonia são algumas das configurações individuais de uma conta de usuário que podem ser configuradas no painel de controle do Lync Server para o usuário (ou seja, se o usuário individual tiver sido habilitado para o Lync Server 2013 e a organização oferecer suporte a telefonia).</span><span class="sxs-lookup"><span data-stu-id="89b26-106">Telephony settings are some of the individual settings of a user account that can be configured in Lync Server Control Panel for the user (that is, if the individual user has been enabled for Lync Server 2013 and the organization supports telephony).</span></span>

<span data-ttu-id="89b26-107">As opções de telefonia do usuário do Lync Server incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89b26-107">Lync Server user telephony options include the following:</span></span>

  - <span data-ttu-id="89b26-108">**Áudio/vídeo desabilitado**   O usuário não pode fazer chamadas com áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="89b26-108">**Audio/video disabled**   The user cannot make calls with audio and video.</span></span>

  - <span data-ttu-id="89b26-109">**PC para PC somente**   O usuário pode fazer apenas chamadas de áudio e com vídeo para PC para PC.</span><span class="sxs-lookup"><span data-stu-id="89b26-109">**PC-to-PC only**   The user can make only PC-to-PC audio or video calls.</span></span>

  - <span data-ttu-id="89b26-110">**Enterprise Voice**   O usuário pode usar a infraestrutura do Lync Server 2013 para direcionar todas as chamadas de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="89b26-110">**Enterprise Voice**   The user can use the Lync Server 2013 infrastructure to route all incoming and outgoing calls.</span></span> <span data-ttu-id="89b26-111">O usuário também pode fazer chamadas de PC para PC.</span><span class="sxs-lookup"><span data-stu-id="89b26-111">The user can also make PC-to-PC calls.</span></span>

  - <span data-ttu-id="89b26-112">**Controle de chamada remota**   O usuário pode usar o Lync Server 2013 para controlar o telefone de mesa e também pode fazer chamadas de PC para PC.</span><span class="sxs-lookup"><span data-stu-id="89b26-112">**Remote call control**   The user can use Lync Server 2013 to control the desktop phone, and can also make PC-to-PC calls.</span></span>

<span data-ttu-id="89b26-113">Para obter detalhes sobre como configurar a telefonia de uma organização, consulte [Configurar a telefonia de um usuário no Lync server 2013](lync-server-2013-configure-telephony-for-a-user.md) e [implantação do Enterprise Voice no Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="89b26-113">For details about configuring telephony for an organization, see [Configure telephony for a user in Lync Server 2013](lync-server-2013-configure-telephony-for-a-user.md) and [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span>

<div>

## <a name="to-configure-telephony-for-a-specific-user-account"></a><span data-ttu-id="89b26-114">Para configurar a telefonia para uma conta de usuário específica</span><span class="sxs-lookup"><span data-stu-id="89b26-114">To configure telephony for a specific user account</span></span>

1.  <span data-ttu-id="89b26-115">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="89b26-115">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="89b26-116">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="89b26-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="89b26-117">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="89b26-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="89b26-118">Na barra de navegação esquerda, clique em **Usuários**.</span><span class="sxs-lookup"><span data-stu-id="89b26-118">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="89b26-119">Na caixa **Pesquisar usuários** , digite toda ou a primeira parte do nome para exibição, nome, sobrenome, nome da conta do Gerenciador de contas de segurança (Sam), endereço SIP ou URI (Uniform Resource Identifier) da conta de usuário que você deseja e, em seguida, clique em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="89b26-119">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want, and then click **Find**.</span></span>

5.  <span data-ttu-id="89b26-120">Na tabela, clique na conta de usuário que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="89b26-120">In the table, click the user account that you want to modify.</span></span>

6.  <span data-ttu-id="89b26-121">No menu **Editar** , clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="89b26-121">On the **Edit** menu, click **Modify**.</span></span>

7.  <span data-ttu-id="89b26-122">Em **telefonia**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89b26-122">In **Telephony**, do the following:</span></span>
    
      - <span data-ttu-id="89b26-123">Para desativar as chamadas de áudio e vídeo para o usuário, clique em **áudio/vídeo desabilitado**.</span><span class="sxs-lookup"><span data-stu-id="89b26-123">To disable audio and video calls for the user, click **Audio/video disabled**.</span></span>
    
      - <span data-ttu-id="89b26-124">Para habilitar as comunicações de áudio PC para PC para o usuário, mas não o controle de chamada remota ou o Enterprise Voice, clique em **PC para PC somente**.</span><span class="sxs-lookup"><span data-stu-id="89b26-124">To enable PC-to-PC audio communications for the user, but not remote call control or Enterprise Voice, click **PC-to-PC only**.</span></span> <span data-ttu-id="89b26-125">Especifique um valor para o **URI da linha** para o telefone que o usuário usa para comunicações de áudio PC para PC.</span><span class="sxs-lookup"><span data-stu-id="89b26-125">Specify a value for **Line URI** for the telephone that the user uses for PC-to-PC audio communications.</span></span>
    
      - <span data-ttu-id="89b26-126">Para encaminhar as chamadas telefônicas do usuário usando a infraestrutura do Lync Server 2010 de acordo com a classe de política de serviço, incluindo comunicação de áudio PC para PC, clique em **Enterprise Voice**.</span><span class="sxs-lookup"><span data-stu-id="89b26-126">To route the user's phone calls by using the Lync Server 2010 infrastructure in accordance with the class of service policy, including PC-to-PC audio communication, click **Enterprise Voice**.</span></span> <span data-ttu-id="89b26-127">Em **URI da linha**, especifique o número de telefone do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="89b26-127">In **Line URI**, specify the telephone number for Enterprise Voice.</span></span> <span data-ttu-id="89b26-128">Em **política de plano de discagem** e **política de voz**, especifique as políticas adequadas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="89b26-128">In **Dial plan policy** and **Voice policy**, specify the appropriate policies for the user.</span></span> <span data-ttu-id="89b26-129">Para especificar as regras de normalização para a tradução de números de telefone discados pelo usuário para o formato E. 164, selecione o perfil de localização apropriado na **política de localização**.</span><span class="sxs-lookup"><span data-stu-id="89b26-129">To specify the normalization rules for translating phone numbers dialed by the user to the E.164 format, select the appropriate location profile in **Location policy**.</span></span>
    
      - <span data-ttu-id="89b26-130">Para habilitar o controle de chamada remota, que permite que os usuários controlem a linha de telefone da área de trabalho do Lync Server 2013 para fazer chamadas de PC para PC e chamadas de PC para telefone, clique em **controle de chamada remota**.</span><span class="sxs-lookup"><span data-stu-id="89b26-130">To enable remote call control, which enables users to control their desktop phone line from Lync Server 2013 to make PC-to-PC calls and PC-to-phone calls, click **Remote call control**.</span></span> <span data-ttu-id="89b26-131">Em **URI de linha**, especifique o número de telefone para o controle de chamada remota.</span><span class="sxs-lookup"><span data-stu-id="89b26-131">In **Line URI**, specify the telephone number for remote call control.</span></span> <span data-ttu-id="89b26-132">O usuário deve ter uma conexão de telefone de mesa e PBX (Private Branch Exchange) para roteamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="89b26-132">The user must have a desktop phone and private branch exchange (PBX) connection for call routing.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="89b26-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="89b26-133">See Also</span></span>


[<span data-ttu-id="89b26-134">Modificando Propriedades de conta de usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89b26-134">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)  
  

<span data-ttu-id="89b26-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89b26-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

