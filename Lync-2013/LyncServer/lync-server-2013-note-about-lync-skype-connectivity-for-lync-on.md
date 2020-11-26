---
title: 'Lync Server 2013: observação sobre a conectividade do Lync-Skype para o Lync em'
description: 'Lync Server 2013: observação sobre a conectividade do Lync-Skype para o Lync em.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Note about Lync-Skype connectivity for Lync On
ms:assetid: 1d0f5c1a-74c6-468f-9877-ad2b1ddf355f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440169(v=OCS.15)
ms:contentKeyID: 57793359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f7d9758f277f2f987677c2c0ffa0a4447ba31d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424972"
---
# <a name="note-about-lync-skype-connectivity-in-lync-server-2013-for-lync-online-customers"></a><span data-ttu-id="9dc99-103">Observação sobre a conectividade do Lync-Skype no Lync Server 2013 para clientes do Lync Online</span><span class="sxs-lookup"><span data-stu-id="9dc99-103">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9dc99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9dc99-104">

<span> </span></span></span>

<span data-ttu-id="9dc99-105">_**Tópico da última modificação:** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="9dc99-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="9dc99-106">Este documento foi escrito para ajudar os administradores locais do Lync Server a configurar a conectividade do Lync-Skype.</span><span class="sxs-lookup"><span data-stu-id="9dc99-106">This document was written to help Lync Server on-premise administrators set up Lync-Skype connectivity.</span></span>  <span data-ttu-id="9dc99-107">Lync-Skype conectividade também é um recurso do Lync Online, que faz parte do Office 365 e do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9dc99-107">Lync-Skype connectivity is also a feature of Lync Online, which is part of Office 365 and Microsoft 365.</span></span> <span data-ttu-id="9dc99-108">Você pode habilitar o recurso de conectividade do Lync-Skype a partir do centro de administração do Lync no centro de administração.</span><span class="sxs-lookup"><span data-stu-id="9dc99-108">You can enable the Lync-Skype connectivity feature from the Lync Administration Center within the admin center.</span></span>

<span data-ttu-id="9dc99-109">Para Microsoft 365 Midsize Business, Office 365 Enterprise, Microsoft 365 Education e Office 365 para governo: entre no portal do Office 365 ou no centro de administração do Microsoft 365 e navegue até o **centro de administração do Lync**.</span><span class="sxs-lookup"><span data-stu-id="9dc99-109">For Microsoft 365 Midsize Business, Office 365 Enterprise, Microsoft 365 Education, and Office 365 for Government: Sign in to the Office 365 portal or Microsoft 365 admin center and navigate to the **Lync Administration Center**.</span></span> <span data-ttu-id="9dc99-110">Vá para **comunicações externas**.</span><span class="sxs-lookup"><span data-stu-id="9dc99-110">Go to **External Communications**.</span></span> <span data-ttu-id="9dc99-111">Em **provedores de serviços públicos de mensagens instantâneas**, clique em **habilitar**.</span><span class="sxs-lookup"><span data-stu-id="9dc99-111">Under **Public IM Service Providers**, click **Enable**.</span></span> <span data-ttu-id="9dc99-112">Se você quiser controlar o acesso de um usuário individual à conectividade do Lync-Skype, poderá fazer isso editando as configurações de comunicações externas de usuários individuais.</span><span class="sxs-lookup"><span data-stu-id="9dc99-112">If you want to control individual user access to Lync-Skype Connectivity, you can do so by editing individual users’ External Communications settings.</span></span>

<span data-ttu-id="9dc99-113">Para o Microsoft 365 Small Business Premium: entrar no Microsoft 365 e vá para **configurações do serviço de administração \> \> , reuniões e conferências**.</span><span class="sxs-lookup"><span data-stu-id="9dc99-113">For Microsoft 365 Small Business Premium: Sign in to Microsoft 365, and go to **Admin \> Service Settings \> Instant messaging, meetings and conferencing**.</span></span> <span data-ttu-id="9dc99-114">Ative as comunicações internas.</span><span class="sxs-lookup"><span data-stu-id="9dc99-114">Turn on External communications.</span></span> <span data-ttu-id="9dc99-115">O interruptor de comunicações externas liga Lync-Skype conectividade e comunicações com outras organizações que usam o Lync.</span><span class="sxs-lookup"><span data-stu-id="9dc99-115">The External communications switch turns on both Lync-Skype connectivity and communications with other organizations that use Lync.</span></span> <span data-ttu-id="9dc99-116">Dependendo de quando você começou a usar o Lync Online, a opção de comunicação externa em um estado "ativado" pode indicar que somente as comunicações com outras organizações do Lync são ativadas.</span><span class="sxs-lookup"><span data-stu-id="9dc99-116">Depending on when you started using Lync Online, the External communications switch in an "on" state may initially indicate only that communications with other Lync organizations is activated.</span></span> <span data-ttu-id="9dc99-117">Para ativar a conectividade do Lync-Skype, basta desativar a opção e, em seguida, ligá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="9dc99-117">To turn on Lync-Skype Connectivity, simply toggle the switch off and then back on again.</span></span>

<span data-ttu-id="9dc99-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9dc99-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

