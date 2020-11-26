---
title: 'Lync Server 2013: Verificar acesso por meio de seu proxy reverso'
description: 'Lync Server 2013: Verifique o acesso por meio do proxy reverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify access through your reverse proxy
ms:assetid: 3076a786-e022-4d41-91ec-1bf252b2a468
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429697(v=OCS.15)
ms:contentKeyID: 48183753
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593aac5574f0dcf683351f12a6392f6116480ac5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443472"
---
# <a name="verify-access-through-your-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="aacc5-103">Verificar acesso por meio de seu proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aacc5-103">Verify access through your reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aacc5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aacc5-104">

<span> </span></span></span>

<span data-ttu-id="aacc5-105">_**Tópico da última modificação:** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="aacc5-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="aacc5-106">Use o procedimento a seguir para verificar se os usuários podem acessar informações no proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="aacc5-106">Use the following procedure to verify that your users can access information on the reverse proxy.</span></span> <span data-ttu-id="aacc5-107">Talvez seja necessário concluir a configuração do firewall e a configuração do sistema de nome de domínio (DNS) antes de o Access funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="aacc5-107">You might need to complete the firewall configuration and Domain Name System (DNS) configuration before access will work correctly.</span></span>

<div>

## <a name="to-verify-that-you-can-access-the-website-through-the-internet"></a><span data-ttu-id="aacc5-108">Para verificar se você pode acessar o site pela Internet</span><span class="sxs-lookup"><span data-stu-id="aacc5-108">To verify that you can access the website through the Internet</span></span>

  - <span data-ttu-id="aacc5-109">Abra um navegador da Web, digite as URLs na barra de **endereços** que os clientes usam para acessar os arquivos do catálogo de endereços e o site para conferência da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="aacc5-109">Open a web browser, type the URLs in the **Address** bar that clients use to access the Address Book files and the website for conferencing as follows:</span></span>
    
      - <span data-ttu-id="aacc5-110">Para o servidor do catálogo de endereços, digite uma URL semelhante à seguinte: **https://externalwebfarmFQDN/abs** onde externalwebfarmFQDN é o FQDN externo dos serviços Web externos que hospeda os serviços de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="aacc5-110">For Address Book Server, type a URL similar to the following: **https://externalwebfarmFQDN/abs** where externalwebfarmFQDN is the external FQDN of the external web services that hosts Address Book services.</span></span> <span data-ttu-id="aacc5-111">O usuário deve receber um desafio HTTP porque a segurança do diretório na pasta do servidor do catálogo de endereços está configurada como autenticação do Windows por padrão.</span><span class="sxs-lookup"><span data-stu-id="aacc5-111">The user should receive an HTTP challenge, because directory security on the Address Book Server folder is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="aacc5-112">Em conferência, digite uma URL semelhante à seguinte: **https://externalwebfarmFQDN/meet** onde externalwebfarmFQDN é o FQDN externo do Web farm que hospeda o conteúdo da reunião.</span><span class="sxs-lookup"><span data-stu-id="aacc5-112">For conferencing, type a URL similar to the following: **https://externalwebfarmFQDN/meet** where externalwebfarmFQDN is the external FQDN of the web farm that hosts meeting content.</span></span> <span data-ttu-id="aacc5-113">Esta URL deve exibir a página de solução de problemas para conferência.</span><span class="sxs-lookup"><span data-stu-id="aacc5-113">This URL should display the troubleshooting page for conferencing.</span></span> <span data-ttu-id="aacc5-114">Se preferir, confirme se sua URL simples para a conferência funciona corretamente.</span><span class="sxs-lookup"><span data-stu-id="aacc5-114">Alternatively, confirm that your Simple URL for conferencing functions correctly.</span></span> <span data-ttu-id="aacc5-115">Um exemplo de URL simples para a junção em conferência pode ser https://meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="aacc5-115">An example Simple URL for the conference join might be https://meet.contoso.com</span></span>
    
      - <span data-ttu-id="aacc5-116">Para expansão do grupo de distribuição, digite uma URL semelhante à seguinte: **https://externalwebfarmFQDN/GroupExpansion/service.svc** .</span><span class="sxs-lookup"><span data-stu-id="aacc5-116">For distribution group expansion, type a URL similar to the following: **https://externalwebfarmFQDN/GroupExpansion/service.svc**.</span></span> <span data-ttu-id="aacc5-117">O usuário deve receber um desafio HTTP porque a segurança de diretório no serviço de expansão do grupo de distribuição é configurada como autenticação do Windows por padrão.</span><span class="sxs-lookup"><span data-stu-id="aacc5-117">The user should receive an HTTP challenge, because directory security on the distribution group expansion service is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="aacc5-118">Para discagem, digite a URL simples semelhante à seguinte **https://externalwebfarmFQDN/dialin** em que externalwebfarmFQDN é o FQDN externo do Web farm que hospeda a página de discagem para conferência discada.</span><span class="sxs-lookup"><span data-stu-id="aacc5-118">For dial-in, type the simple URL similar to the following **https://externalwebfarmFQDN/dialin** where externalwebfarmFQDN is the external FQDN of the web farm that hosts the dial-in page for dial-in conferencing.</span></span> <span data-ttu-id="aacc5-119">O usuário deve ser direcionado para a página de discagem.</span><span class="sxs-lookup"><span data-stu-id="aacc5-119">The user should be directed to the dial-in page.</span></span> <span data-ttu-id="aacc5-120">Como alternativa, confirme se a sua URL simples de discagem funciona corretamente.</span><span class="sxs-lookup"><span data-stu-id="aacc5-120">Alternatively, confirm that your Simple URL dial-in functions correctly.</span></span> <span data-ttu-id="aacc5-121">Um exemplo de URL simples para discagem pode ser https://dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="aacc5-121">An example Simple URL for dial-in might be https://dialin.contoso.com</span></span>
    
      - <span data-ttu-id="aacc5-122">Para confirmar se a URL da descoberta automática está funcionando, digite https://lyncdiscover .</span><span class="sxs-lookup"><span data-stu-id="aacc5-122">To confirm that the autodiscover URL is working, type https://lyncdiscover.</span></span> <span data-ttu-id="aacc5-123">externaldomainFQDN.</span><span class="sxs-lookup"><span data-stu-id="aacc5-123">externaldomainFQDN.</span></span> <span data-ttu-id="aacc5-124">O navegador deve solicitar a abertura de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="aacc5-124">The browser should prompt you to open a file.</span></span> <span data-ttu-id="aacc5-125">Selecione bloco de notas para abri-lo.</span><span class="sxs-lookup"><span data-stu-id="aacc5-125">Select Notepad to open it.</span></span> <span data-ttu-id="aacc5-126">Uma resposta típica seria semelhante a:</span><span class="sxs-lookup"><span data-stu-id="aacc5-126">A typical response would be similar to:</span></span>
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

<span data-ttu-id="aacc5-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aacc5-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

