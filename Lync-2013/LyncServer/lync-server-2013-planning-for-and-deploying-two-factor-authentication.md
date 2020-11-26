---
title: 'Lync Server 2013: planejando e implantando a autenticação de dois fatores'
description: 'Lync Server 2013: planejando e implantando a autenticação de dois fatores.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for and deploying two-factor authentication
ms:assetid: 442a88df-ebc2-4335-9c59-0ce1adc1471e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308563(v=OCS.15)
ms:contentKeyID: 54973686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1e04fa7a0c1184152328882a7c7b4bea8e42ec0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437116"
---
# <a name="two-factor-authentication-in-lync-server-2013"></a><span data-ttu-id="e93a7-103">Autenticação de dois fatores no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e93a7-103">Two-factor authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e93a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e93a7-104">

<span> </span></span></span>

<span data-ttu-id="e93a7-105">_**Tópico da última modificação:** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="e93a7-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="e93a7-106">A autenticação de dois fatores oferece segurança aprimorada exigindo que os usuários conheçam dois critérios de autenticação: uma combinação de nome de usuário/senha e token ou certificado.</span><span class="sxs-lookup"><span data-stu-id="e93a7-106">Two-factor authentication provides improved security by requiring users to meet two authentication criteria: a user name/password combination and a token or certificate.</span></span> <span data-ttu-id="e93a7-107">Isso também é conhecido como "algo que você tem, algo que você sabe".</span><span class="sxs-lookup"><span data-stu-id="e93a7-107">This is also known as “something you have, something you know.”</span></span> <span data-ttu-id="e93a7-108">Um exemplo típico da autenticação de dois fatores com um certificado é o uso de cartões inteligentes.</span><span class="sxs-lookup"><span data-stu-id="e93a7-108">A typical example of two-factor authentication with a certificate is the use of smart cards.</span></span> <span data-ttu-id="e93a7-109">Um cartão inteligente contém um certificado associado à conta do usuário e pode ser validado com as informações e certificado e usuário que estão armazenadas em um servidor.</span><span class="sxs-lookup"><span data-stu-id="e93a7-109">A smart card contains a certificate associated with the user account, and can be validated against user and certificate information stored on a server.</span></span> <span data-ttu-id="e93a7-110">Ao comparar as informações do usuário (nome do usuário e senha) ao certificado fornecido, o servidor valida as credenciais e autentica o usuário.</span><span class="sxs-lookup"><span data-stu-id="e93a7-110">By comparing the user information (user name and password) to the certificate provided, the server validates the credentials and authenticates the user.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e93a7-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e93a7-111">In This Section</span></span>

[<span data-ttu-id="e93a7-112">Planejando a autenticação de dois fatores no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e93a7-112">Planning for two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-planning-for-two-factor-authentication.md)

[<span data-ttu-id="e93a7-113">Configurando a autenticação de dois fatores no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e93a7-113">Configuring two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-configuring-two-factor-authentication.md)

[<span data-ttu-id="e93a7-114">Usando a autenticação de dois fatores com o Lync Client e o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e93a7-114">Using two-factor authentication with Lync client and Lync Server 2013</span></span>](lync-server-2013-using-two-factor-authentication-with-lync-client.md)

<span data-ttu-id="e93a7-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e93a7-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

