---
title: 'Lync Server 2013: Configurar o Lync Server 2013 para trabalhar com a Unificação de Mensagens no Microsoft Exchange Server'
description: 'Lync Server 2013: configurar o Lync Server 2013 para trabalhar com Unificação de mensagens no Microsoft Exchange Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Lync Server 2013 to work with Unified Messaging on Microsoft Exchange Server
ms:assetid: 1098ae4d-f57f-44f3-804e-39889d9fc14e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398193(v=OCS.15)
ms:contentKeyID: 48183430
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 05ef2902ffc03b14e04b378a2ef18e03c8c58372
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433952"
---
# <a name="configure-lync-server-2013-to-work-with-unified-messaging-on-microsoft-exchange-server"></a><span data-ttu-id="c5587-103">Configurar o Lync Server 2013 para trabalhar com a Unificação de Mensagens no Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="c5587-103">Configure Lync Server 2013 to work with Unified Messaging on Microsoft Exchange Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span data-ttu-id="c5587-104">_**Tópico da última modificação:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="c5587-104">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="c5587-105">Esta etapa requer o utilitário de integração do Exchange UM (OcsUmUtil.exe).</span><span class="sxs-lookup"><span data-stu-id="c5587-105">This step requires the Exchange UM Integration Utility (OcsUmUtil.exe).</span></span> <span data-ttu-id="c5587-106">Esta ferramenta está localizada no servidor do Lync Server 2013 em.. \\ Arquivos de programas \\ Arquivos comuns \\ Microsoft Lync Server 2013 \\ support Folder.</span><span class="sxs-lookup"><span data-stu-id="c5587-106">This tool is located on the Lync Server 2013 server in the ..\\Program Files\\Common Files\\Microsoft Lync Server 2013\\Support folder.</span></span>

<div>

## <a name="running-the-exchange-um-integration-utility"></a><span data-ttu-id="c5587-107">Executando o utilitário de integração de UM Exchange</span><span class="sxs-lookup"><span data-stu-id="c5587-107">Running the Exchange UM Integration Utility</span></span>

<span data-ttu-id="c5587-108">O utilitário de integração do Exchange UM deve ser executado a partir de uma conta de usuário com as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="c5587-108">The Exchange UM Integration Utility must be run from a user account with the following characteristics:</span></span>

  - <span data-ttu-id="c5587-109">Associação nos grupos RTCUniversalServerAdmins e RtcUniversalUserAdmins (que inclui a permissão para ler as configurações de mensagens unificadas do Exchange Server).</span><span class="sxs-lookup"><span data-stu-id="c5587-109">Membership in the RTCUniversalServerAdmins and RtcUniversalUserAdmins groups (which includes permission to read Exchange Server Unified Messaging settings).</span></span>

  - <span data-ttu-id="c5587-110">Direitos de usuário no domínio para criar objetos de contato no contêiner de unidade organizacional (OU) especificado.</span><span class="sxs-lookup"><span data-stu-id="c5587-110">User rights within the domain to create contact objects in the specified organizational unit (OU) container.</span></span>

<span data-ttu-id="c5587-111">Quando você executa o utilitário de integração do Exchange UM, ele executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c5587-111">When you run the Exchange UM Integration Utility, it performs the following tasks:</span></span>

  - <span data-ttu-id="c5587-112">Cria objetos de contato para cada número de atendente e acesso do assinante a ser usado por usuários do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="c5587-112">Creates contact objects for each auto-attendant and subscriber access number to be used by Enterprise Voice users.</span></span>

  - <span data-ttu-id="c5587-113">Verifica se o nome de cada plano de discagem de voz empresarial corresponde ao seu próprio contexto de telefone de plano de discagem de mensagens unificadas (UM).</span><span class="sxs-lookup"><span data-stu-id="c5587-113">Verifies that the name of each Enterprise Voice dial plan matches its corresponding unified messaging (UM) dial plan phone context.</span></span> <span data-ttu-id="c5587-114">Essa correspondência só será necessária se o plano de discagem do UM estiver sendo executado em uma versão do Exchange *anterior* ao Exchange 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c5587-114">This matching is necessary only if the UM dial plan is running on a version of Exchange *earlier* than Exchange 2010 Service Pack 1 (SP1).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5587-115">Antes de executar o utilitário de integração do Exchange UM, certifique-se de ter feito o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c5587-115">Before running the Exchange UM Integration Utility, be sure that you have done the following:</span></span>
> <ul>
> <li><p><span data-ttu-id="c5587-116">Crie um ou mais planos de discagem de UM do Exchange, conforme descrito na documentação do produto Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5587-116">Create one or more Exchange UM dial plans, as described in the Exchange product documentation.</span></span></p>
> <p><span data-ttu-id="c5587-117">Para o Microsoft Exchange Server 2010, consulte &quot; criar um plano de discagem de um &quot; em <a href="https://go.microsoft.com/fwlink/p/?linkid=186177">https://go.microsoft.com/fwlink/p/?linkId=186177</a> .</span><span class="sxs-lookup"><span data-stu-id="c5587-117">For Microsoft Exchange Server 2010, see &quot;Create a UM Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=186177">https://go.microsoft.com/fwlink/p/?linkId=186177</a>.</span></span></p>
> <p><span data-ttu-id="c5587-118">Para Microsoft Exchange Server 2007 Service Pack 1 (SP1), consulte &quot; como criar um plano de discagem de URI SIP de Unificação de mensagens &quot; em <a href="https://go.microsoft.com/fwlink/p/?linkid=185771">https://go.microsoft.com/fwlink/p/?linkId=185771</a> .</span><span class="sxs-lookup"><span data-stu-id="c5587-118">For Microsoft Exchange Server 2007 Service Pack 1 (SP1), see &quot;How to Create a Unified Messaging SIP URI Dial Plan&quot; at <a href="https://go.microsoft.com/fwlink/p/?linkid=185771">https://go.microsoft.com/fwlink/p/?linkId=185771</a>.</span></span></p></li>
> <li><p><span data-ttu-id="c5587-119">Crie um ou mais planos de discagem do Lync Server correspondentes, conforme descrito em <a href="lync-server-2013-create-a-dial-plan.md">criar um plano de discagem no Lync server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="c5587-119">Create one or more corresponding Lync Server dial plans, as described in <a href="lync-server-2013-create-a-dial-plan.md">Create a dial plan in Lync Server 2013</a>.</span></span></p></li>
> <ul><li><span data-ttu-id="c5587-120">Se estiver usando uma versão do Exchange anterior ao Microsoft Exchange Server 2010 SP1, você deve digitar o nome de domínio totalmente qualificado (FQDN) do plano de discagem SIP do Exchange Unified Messaging (UM) correspondente no campo <STRONG>nome simples</STRONG> do plano de discagem do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c5587-120">If you are using a version of Exchange that is earlier than Microsoft Exchange Server 2010 SP1, you must enter the fully qualified domain name (FQDN) of the corresponding Exchange Unified Messaging (UM) SIP dial plan in the Lync Server 2013 dial plan <STRONG>Simple name</STRONG> field.</span></span> <span data-ttu-id="c5587-121">Se você estiver usando o Microsoft Exchange Server 2010 SP1 ou Service Pack mais recente, o nome do plano de discagem correspondente não será necessário.</span><span class="sxs-lookup"><span data-stu-id="c5587-121">If you are using Microsoft Exchange Server 2010 SP1 or latest service pack, this dial plan name matching is not necessary.</span></span></li></ul>
> <li><span data-ttu-id="c5587-122">Crie um atendedor automático e certifique-se de que o número de acesso do assinante e o número do auto Attendant estejam no formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="c5587-122">Create an auto-attendant and make sure that both the subscriber access number and auto-attendant number are in E.164 format.</span></span></li></ul>


<div>

## <a name="to-run-the-exchange-um-integration-utility"></a><span data-ttu-id="c5587-123">Para executar o utilitário de integração de UM Exchange</span><span class="sxs-lookup"><span data-stu-id="c5587-123">To run the Exchange UM Integration Utility</span></span>

1.  <span data-ttu-id="c5587-124">Em um servidor front-end, abra um prompt de comando e digite **CD% COMMONPROGRAMFILES% \\ Microsoft Lync Server 2013 \\ support** e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="c5587-124">On a Front End Server, open a command prompt and type **cd %CommonProgramFiles%\\Microsoft Lync Server 2013\\Support**, and then press ENTER.</span></span>

2.  <span data-ttu-id="c5587-125">Digite **OcsUmUtil.exe** e, em seguida, pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="c5587-125">Type **OcsUmUtil.exe**, and then press ENTER.</span></span>

3.  <span data-ttu-id="c5587-126">Clique em **carregar dados** para localizar todas as florestas do Exchange confiáveis.</span><span class="sxs-lookup"><span data-stu-id="c5587-126">Click **Load Data** to find all trusted Exchange forests.</span></span>

4.  <span data-ttu-id="c5587-127">Na lista **planos de discagem SIP** , selecione um plano de discagem do um SIP para o qual você deseja criar objetos de contato e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="c5587-127">In the **SIP Dial Plans** list, select a UM SIP dial plan for which you want to create contact objects, and then click **Add**.</span></span>

5.  <span data-ttu-id="c5587-128">Na caixa de **contato** , aceite a unidade organizacional padrão ou clique em **procurar** para iniciar o **seletor de ou**.</span><span class="sxs-lookup"><span data-stu-id="c5587-128">In the **Contact** box, accept the default organizational unit, or click **Browse** to start the **OU Picker**.</span></span> <span data-ttu-id="c5587-129">Na caixa do **seletor de ou** , você pode selecionar uma UO e clicar em **OK**, ou pode clicar em **fazer nova UO** para criar uma nova unidade organizacional na raiz ou em qualquer outra UO do domínio (por exemplo, "ou = contas especiais do RTC, DC = fourthcoffee, DC = com") e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5587-129">In the **OU Picker** box, you can select an OU and click **OK**, or you can click **Make New OU** to create a new organizational unit under the root or any other OU in the domain (for example, "OU=RTC Special Accounts,DC=fourthcoffee,DC=com"), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5587-130">O nome diferenciado (DN) da OU que você selecionou ou criou agora é exibido na caixa <STRONG>unidade organizacional</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c5587-130">The distinguished name (DN) of the OU that you have selected or created is now displayed in the <STRONG>Organizational Unit</STRONG> box.</span></span>

    
    </div>

6.  <span data-ttu-id="c5587-131">Na caixa **nome** , aceite o nome do plano de discagem padrão ou digite um novo nome para exibição para o objeto de contato que você está criando.</span><span class="sxs-lookup"><span data-stu-id="c5587-131">In the **Name** box, either accept the default dial plan name or type a new display name for the contact object that you are creating.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5587-132">Por exemplo, se você estiver criando um objeto de contato do acesso ao Assinante, você pode simplesmente nomeá-lo como assinante.</span><span class="sxs-lookup"><span data-stu-id="c5587-132">For example, if you are creating a subscriber access contact object, you might simply name it Subscriber Access.</span></span>

    
    </div>

7.  <span data-ttu-id="c5587-133">Na caixa **endereço SIP** , aceite o endereço SIP padrão ou digite um novo endereço SIP.</span><span class="sxs-lookup"><span data-stu-id="c5587-133">In the **SIP Address** box, either accept the default SIP address or type a new SIP address.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5587-134">Se você digitar um novo endereço SIP, ele deve começar com <STRONG>SIP:</STRONG> (isto é, "SIP:" incluindo os dois-pontos).</span><span class="sxs-lookup"><span data-stu-id="c5587-134">If you type a new SIP address, it must begin with <STRONG>SIP:</STRONG> (that is, "SIP:" including the colon).</span></span>

    
    </div>

8.  <span data-ttu-id="c5587-135">Na lista **servidor ou pool** , selecione o servidor Standard Edition ou o pool de front-end no qual o objeto de contato deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="c5587-135">In the **Server or Pool** list, select the Standard Edition server or Front End pool in which the contact object is to be enabled.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5587-136">Preferencialmente, o pool selecionado é o mesmo pool em que os usuários habilitados para o Enterprise Voice e o Exchange UM são implantados.</span><span class="sxs-lookup"><span data-stu-id="c5587-136">Preferably, the pool you select is the same one pool where users enabled for Enterprise Voice and Exchange UM are deployed.</span></span>

    
    </div>

9.  <span data-ttu-id="c5587-137">Na lista **número de telefone** , selecione **Inserir número de telefone** ou **Use este número piloto no Exchange um** e, em seguida, digite um número de telefone.</span><span class="sxs-lookup"><span data-stu-id="c5587-137">In the **Phone Number** list, select either **Enter phone number** or **Use this pilot number from Exchange UM** and then enter a phone number.</span></span>

10. <span data-ttu-id="c5587-138">Na lista **tipo de contato** , selecione o tipo de contato que você deseja criar e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5587-138">In the **Contact Type** list, select the contact type that you want to create, and then click **OK**.</span></span>

11. <span data-ttu-id="c5587-139">Repita as etapas de 1 a 10 para objetos de contato adicionais que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="c5587-139">Repeat steps 1 through 10 for additional contact objects that you want to create.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5587-140">Você deve criar pelo menos um contato para cada atendedor automático.</span><span class="sxs-lookup"><span data-stu-id="c5587-140">You should create at least one contact for each auto attendant.</span></span> <span data-ttu-id="c5587-141">Se você quiser acesso externo, também precisará de um contato do acesso do assinante e especificar números do Direct Inward Dial (DID).</span><span class="sxs-lookup"><span data-stu-id="c5587-141">If you want external access, you also need a Subscriber Access contact and to specify Direct Inward Dial (DID) numbers.</span></span>

    
    </div>

</div>

<span data-ttu-id="c5587-142">Para verificar se os objetos de contato foram criados, abra usuários e computadores do Active Directory e selecione a OU em que os objetos foram criados.</span><span class="sxs-lookup"><span data-stu-id="c5587-142">To verify that the contact objects have been created, open Active Directory Users and Computers and select the OU in which the objects were created.</span></span> <span data-ttu-id="c5587-143">Os objetos de contato devem aparecer no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="c5587-143">The contact objects should appear in the details pane.</span></span>

<span data-ttu-id="c5587-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5587-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

