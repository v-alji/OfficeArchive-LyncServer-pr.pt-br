---
title: 'Lync Server 2013: Segurança de dados de emparelhamento do pool Front End'
description: 'Lync Server 2013: o pool de front-ends está emparelhando a segurança de dados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Front End pool pairing data security
ms:assetid: edb852b8-ea86-4948-b756-60fe6ee876d2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721930(v=OCS.15)
ms:contentKeyID: 49733865
ms.date: 10/07/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 32a2ce72752819392429c8407649e663494f1daf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428045"
---
# <a name="front-end-pool-pairing-data-security-in-lync-server-2013"></a><span data-ttu-id="7058a-103">Segurança de dados de emparelhamento do pool Front End no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7058a-103">Front End pool pairing data security in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7058a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7058a-104">

<span> </span></span></span>

<span data-ttu-id="7058a-105">_**Tópico da última modificação:** 2014-10-07_</span><span class="sxs-lookup"><span data-stu-id="7058a-105">_**Topic Last Modified:** 2014-10-07_</span></span>

<span data-ttu-id="7058a-106">O serviço de backup é um mecanismo de replicação de dados introduzido no Lync Server 2013 que transfere dados de usuários e conteúdo de conferência entre dois pools front-ends em dois data centers para fins de recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="7058a-106">The Backup Service is a data replication mechanism introduced in Lync Server 2013 that transfers user data and conference content between two paired Front End pools continuously across two data centers for disaster recovery purposes.</span></span> <span data-ttu-id="7058a-107">Os dados do usuário contêm URIs SIP do usuário, bem como as listas de contatos e as configurações.</span><span class="sxs-lookup"><span data-stu-id="7058a-107">The user data contains user SIP URIs as well as contact lists and settings.</span></span> <span data-ttu-id="7058a-108">O conteúdo da conferência inclui carregamentos do Microsoft PowerPoint 2010, bem como quadros de comunicações usados em conferências.</span><span class="sxs-lookup"><span data-stu-id="7058a-108">Conference content includes Microsoft PowerPoint 2010 uploads, as well as whiteboards used in conferences.</span></span> <span data-ttu-id="7058a-109">Do pool de origem, os dados do usuário e o conteúdo da conferência são exportados do armazenamento local, zipados, transferidos para o pool de destino, onde eles são descompactados e importados para armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="7058a-109">From the source pool, user data and conference content are exported from the local storage, zipped, transferred to the target Pool, where it is unzipped and imported to local storage.</span></span> <span data-ttu-id="7058a-110">O Serviço de Backup pressupõe que o link de comunicações entre os dois data centers está dentro da rede corporativa que está protegida a partir da Internet.</span><span class="sxs-lookup"><span data-stu-id="7058a-110">The Backup Service assumes that the communications link between the two data centers is within the corporate network that is protected from the Internet.</span></span> <span data-ttu-id="7058a-111">Ele não criptografa os dados transferidos entre os dois data centers, nem é encapsulado nativamente em um protocolo seguro, como HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7058a-111">It does not encrypt the transferred data between the two data centers, nor is it natively encapsulated within a secure protocol, such as HTTPS.</span></span> <span data-ttu-id="7058a-112">Portanto, é possível que o ataque pelo meio Man do pessoal interno na rede da empresa seja possível.</span><span class="sxs-lookup"><span data-stu-id="7058a-112">Therefore, man-in-the-middle attack from internal personnel within the corporate network is possible.</span></span>

<div>

## <a name="evaluating-security-risks"></a><span data-ttu-id="7058a-113">Avaliando riscos de segurança</span><span class="sxs-lookup"><span data-stu-id="7058a-113">Evaluating Security Risks</span></span>

<span data-ttu-id="7058a-114">Qualquer empresa que implante o Lync Server 2013 em vários data centers e use o recurso de recuperação de desastres deve garantir que o tráfego entre o Data Center seja protegido pela intranet corporativa.</span><span class="sxs-lookup"><span data-stu-id="7058a-114">Any enterprise which deploys Lync Server 2013 across multiple data centers and uses the disaster recovery feature must ensure that cross-data center traffic is protected by their corporate Intranet.</span></span> <span data-ttu-id="7058a-115">As empresas que se preocupam com a proteção interna contra ataques devem proteger os links de comunicação entre os data centers.</span><span class="sxs-lookup"><span data-stu-id="7058a-115">Enterprises which care about internal attack protection must secure the communication links among the data centers.</span></span>

<span data-ttu-id="7058a-116">A pressuposição de que os dados centrais de uma empresa são protegidos por trás da intranet corporativa é padrão.</span><span class="sxs-lookup"><span data-stu-id="7058a-116">The assumption that data centers of an enterprise are protected behind the corporate Intranet is standard.</span></span> <span data-ttu-id="7058a-117">Há muitos outros tipos de dados confidenciais corporativos transferidos entre esses data centers.</span><span class="sxs-lookup"><span data-stu-id="7058a-117">There are many other types of corporate sensitive data transferred among these data centers.</span></span> <span data-ttu-id="7058a-118">A infraestrutura de ti da empresa está a perigo risco se esses links de Data Center não estiverem protegidos.</span><span class="sxs-lookup"><span data-stu-id="7058a-118">The enterprise’s IT infrastructure is at dire risk if these cross-data center links are not protected.</span></span>

<span data-ttu-id="7058a-119">Embora exista o risco de ataques de "intrusos" na rede corporativa, ele é relativamente limitado em comparação a expor o tráfego à Internet.</span><span class="sxs-lookup"><span data-stu-id="7058a-119">While the risk of man-in-the-middle attacks within the corporate network exists, it is relatively contained as compared to exposing the traffic to the Internet.</span></span> <span data-ttu-id="7058a-120">Especificamente, os dados do usuário expostos pelo serviço de backup (como URIs SIP) estão disponíveis geralmente para todos os funcionários da empresa por meio de outros meios como o catálogo de endereços global pelo Exchange ou outro software de diretório.</span><span class="sxs-lookup"><span data-stu-id="7058a-120">Specifically, the user data exposed by Backup Service (such as SIP URIs) are generally available to all employees within the company via other means such as the Global Address Book by Exchange or other directory software.</span></span> <span data-ttu-id="7058a-121">Portanto, o foco deve estar na proteção da WAN entre os dois data centers quando o serviço de backup é usado para copiar dados entre os dois pools emparelhados.</span><span class="sxs-lookup"><span data-stu-id="7058a-121">Hence, the focus should be on securing the WAN between the two data centers when the Backup Service is used to copy data between the two paired Pools.</span></span>

</div>

<div>

## <a name="mitigating-security-risks"></a><span data-ttu-id="7058a-122">Redução de riscos de segurança</span><span class="sxs-lookup"><span data-stu-id="7058a-122">Mitigating Security Risks</span></span>

<span data-ttu-id="7058a-123">Há muitas maneiras de melhorar a proteção de segurança para o tráfego do serviço de backup, desde a restrição do acesso a centros de dados até a proteção do transporte de WAN entre os dois data centers.</span><span class="sxs-lookup"><span data-stu-id="7058a-123">There are many ways to enhance security protection for the Backup Service traffic, ranging from restricting access to the data centers to securing the WAN transport between the two data centers.</span></span> <span data-ttu-id="7058a-124">Na maioria dos casos, as empresas que implantam o Lync Server 2013 podem já ter a infraestrutura de segurança necessária implementada.</span><span class="sxs-lookup"><span data-stu-id="7058a-124">In most cases, enterprises deploying Lync Server 2013 might already have the required security infrastructure in place.</span></span> <span data-ttu-id="7058a-125">Para as empresas que buscam orientação, a Microsoft oferece uma solução como um exemplo de como criar uma infraestrutura de ti segura.</span><span class="sxs-lookup"><span data-stu-id="7058a-125">For enterprises looking for guidance, Microsoft provides solution as an example of how to build a secure IT infrastructure.</span></span> <span data-ttu-id="7058a-126">No entanto, isso não significa que essa é a única solução, nem significa que ela é a solução preferida para o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7058a-126">However, this does not imply that it is the only solution, nor does it imply that it is the preferred solution for Lync Server.</span></span> <span data-ttu-id="7058a-127">Recomendamos que os clientes corporativos escolham a solução adequada às suas necessidades específicas, com base em sua infraestrutura de segurança de ti e seus requisitos. O exemplo de solução da Microsoft emprega IPSec e a política de grupo para o isolamento de servidor e domínio.</span><span class="sxs-lookup"><span data-stu-id="7058a-127">We recommend that enterprise customers choose the solution suits their specific needs, based on their IT security infrastructure and requirements.The example Microsoft solution employs IPSec and Group Policy for Server and Domain Isolation.</span></span> <span data-ttu-id="7058a-128">Para obter detalhes, consulte [https://go.microsoft.com/fwlink/p/?LinkId=268544](https://go.microsoft.com/fwlink/p/?linkid=268544) .</span><span class="sxs-lookup"><span data-stu-id="7058a-128">For details, see [https://go.microsoft.com/fwlink/p/?LinkId=268544](https://go.microsoft.com/fwlink/p/?linkid=268544).</span></span> <span data-ttu-id="7058a-129">Para perguntas e comentários, entre em contato com a secwish@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="7058a-129">For questions and comments, contact secwish@microsoft.com.</span></span>

<span data-ttu-id="7058a-130">Outra solução possível é usar o IPSec apenas para ajudar a proteger os dados enviados pelo próprio Serviço de Backup.</span><span class="sxs-lookup"><span data-stu-id="7058a-130">Another possible solution is to use IPSec just to help secure the data sent by the Backup Service itself.</span></span> <span data-ttu-id="7058a-131">Se você escolher este método, deverá configurar as regras do IPSec para o protocolo SMB nos seguintes servidores, onde Pool A e Pool B são dois Pools de Front-Ends emparelhados.</span><span class="sxs-lookup"><span data-stu-id="7058a-131">If you choose this method, you should configure the IPSec rules for the SMB protocol for the following servers, where Pool A and Pool B are two paired Front End pools.</span></span>

  - <span data-ttu-id="7058a-132">O Serviço SMB (TCP/445) de cada Servidor Front-End no Pool A para o Repositório de Arquivos usado pelo Pool B.</span><span class="sxs-lookup"><span data-stu-id="7058a-132">The SMB Service (TCP/445) from each Front End Server in Pool A to the File Store used by Pool B.</span></span>

  - <span data-ttu-id="7058a-133">O Serviço SMB (TCP/445) de cada Servidor Front-End no Pool B para o Repositório de Arquivos usado pelo Pool A.</span><span class="sxs-lookup"><span data-stu-id="7058a-133">The SMB Service (TCP/445) from each Front End Server in Pool B to the File Store used by Pool A.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="7058a-134">O IPsec não deve ser usado para substituir a segurança no nível de aplicativo, como SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="7058a-134">IPsec is not intended as a replacement for application-level security, such as SSL/TLS.</span></span> <span data-ttu-id="7058a-135">Uma vantagem de usar o IPsec é que ele pode fornecer segurança ao tráfego da rede para os aplicativos existentes sem ter de alterá-los.</span><span class="sxs-lookup"><span data-stu-id="7058a-135">One advantage of using IPsec is that it can provide network traffic security for existing applications without having to change them.</span></span> <span data-ttu-id="7058a-136">As empresas que desejam proteger o transporte entre os dois data centers devem consultar seus respectivos fornecedores de hardware de rede em relação à maneira de configurar conexões WAN seguras usando o equipamento do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="7058a-136">Enterprises that want to just secure the transport between the two data centers should consult their respective networking hardware vendors about ways to set up secure WAN connections by using the vendor’s equipment.</span></span>



<span data-ttu-id="7058a-137"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7058a-137"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

