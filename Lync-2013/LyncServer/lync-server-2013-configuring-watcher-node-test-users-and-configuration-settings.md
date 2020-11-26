---
title: Configurando os usuários do nó do Inspetor e configurações de configuração
description: Configuração de usuários de teste de nó do Inspetor e configurações de configuração.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring watcher node test users and configuration settings
ms:assetid: ab00e9cb-f539-4aa6-bcb4-5533fbe7bc44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205152(v=OCS.15)
ms:contentKeyID: 48185048
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e39a35d3db6ed80c715c706f4b5766e4b684e39e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432328"
---
# <a name="configuring-watcher-node-test-users-and-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="72c06-103">Configurando os usuários de teste de nó do Inspetor e configurações de configuração no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72c06-103">Configuring watcher node test users and configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72c06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72c06-104">

<span> </span></span></span>

<span data-ttu-id="72c06-105">_**Tópico da última modificação:** 2013-07-29_</span><span class="sxs-lookup"><span data-stu-id="72c06-105">_**Topic Last Modified:** 2013-07-29_</span></span>

<span data-ttu-id="72c06-106">Depois de configurar o computador que atuará como um nó do inspetor, você deve:</span><span class="sxs-lookup"><span data-stu-id="72c06-106">After configuring the computer that will act as a watcher node, you must:</span></span>

1.  <span data-ttu-id="72c06-107">Crie as contas de teste a serem usadas por estes nós do Inspetor.</span><span class="sxs-lookup"><span data-stu-id="72c06-107">Create the test accounts to be used by these watcher nodes.</span></span> <span data-ttu-id="72c06-108">Se estiver usando o método de autenticação Negociar, você também deve usar o cmdlet [Set-CsTestUserCredential](https://technet.microsoft.com/library/JJ205341(v=OCS.15)) para permitir o uso dessas contas de teste no nó do inspetor.</span><span class="sxs-lookup"><span data-stu-id="72c06-108">If you are using the Negotiate authentication method, you must also use the [Set-CsTestUserCredential](https://technet.microsoft.com/library/JJ205341(v=OCS.15)) cmdlet to enable these test accounts for use on the watcher node.</span></span>

2.  <span data-ttu-id="72c06-109">Atualizar as definições de configuração do nó do inspetor.</span><span class="sxs-lookup"><span data-stu-id="72c06-109">Update the watcher node configuration settings.</span></span>

<span data-ttu-id="72c06-110">Esta seção aborda:</span><span class="sxs-lookup"><span data-stu-id="72c06-110">This section covers:</span></span>

  - <span data-ttu-id="72c06-111">Configurar contas de usuário de teste</span><span class="sxs-lookup"><span data-stu-id="72c06-111">Configuring Test User Accounts</span></span>

  - <span data-ttu-id="72c06-112">Configurando um nó de Inspetor básico com as transações sintéticas padrão</span><span class="sxs-lookup"><span data-stu-id="72c06-112">Configuring a Basic Watcher Node with the Default Synthetic Transactions</span></span>

  - <span data-ttu-id="72c06-113">Configurando testes estendidos</span><span class="sxs-lookup"><span data-stu-id="72c06-113">Configuring Extended Tests</span></span>

  - <span data-ttu-id="72c06-114">Adicionando e removendo transações sintéticas</span><span class="sxs-lookup"><span data-stu-id="72c06-114">Adding and Removing Synthetic Transactions</span></span>

  - <span data-ttu-id="72c06-115">Exibindo e testando a configuração do nó do inspetor</span><span class="sxs-lookup"><span data-stu-id="72c06-115">Viewing and Testing the Watcher Node Configuration</span></span>

<div>

## <a name="configuring-test-user-accounts"></a><span data-ttu-id="72c06-116">Configurar contas de usuário de teste</span><span class="sxs-lookup"><span data-stu-id="72c06-116">Configuring Test User Accounts</span></span>

<span data-ttu-id="72c06-117">Os usuários de teste não precisam representar pessoas reais, mas devem ser contas válidas dos serviços de domínio Active Directory; Além disso, essas contas devem ser habilitadas para o Lync Server 2013, devem ter endereços SIP válidos e devem ser habilitadas para o Enterprise Voice (para usar a transação sintética Test-CsPstnPeerToPeerCall).</span><span class="sxs-lookup"><span data-stu-id="72c06-117">Test users do not need to represent actual people, but they must be valid Active Directory Domain Services accounts; in addition, these accounts must be enabled for Lync Server 2013, they must have valid SIP addresses, and they should be enabled for Enterprise Voice (to use the Test-CsPstnPeerToPeerCall synthetic transaction).</span></span> <span data-ttu-id="72c06-118">Se você usa o método de autenticação TrustedServer, tudo o que precisa fazer é verificar se essas contas existem e se foram configuradas como especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="72c06-118">If you use the TrustedServer authentication method, then all you need to do is to make sure that these accounts exist and have been configured as specified here.</span></span> <span data-ttu-id="72c06-119">É necessário atribuir pelo menos três usuários de teste a cada pool que deseja testar.</span><span class="sxs-lookup"><span data-stu-id="72c06-119">You should assign at least three test users for each pool that you want to test.</span></span>

<span data-ttu-id="72c06-120">Se você estiver usando o método de autenticação Negotiate, também deverá usar o cmdlet **set-CsTestUserCredential** e o Shell de gerenciamento do Lync Server para permitir que essas contas de teste funcionem com as transações sintéticas.</span><span class="sxs-lookup"><span data-stu-id="72c06-120">If you are using the Negotiate authentication method, you must also use the **Set-CsTestUserCredential** cmdlet and the Lync Server Management Shell to enable these test accounts to work with the synthetic transactions.</span></span> <span data-ttu-id="72c06-121">Você pode fazer isso executando um comando semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="72c06-121">You can do this by running a command similar to the following.</span></span> <span data-ttu-id="72c06-122">(Esses comandos pressupõem que as três contas de usuário do Active Directory já foram criadas e que essas contas foram habilitadas para o Lync Server 2013.):</span><span class="sxs-lookup"><span data-stu-id="72c06-122">(These commands assume that the three Active Directory user accounts have already been created and that those accounts have been enabled for Lync Server 2013.):</span></span>

    Set-CsTestUserCredential -SipAddress "sip:watcher1@litwareinc.com" -UserName "litwareinc\watcher1" -Password "P@ssw0rd"
    Set-CsTestUserCredential -SipAddress "sip:watcher2@litwareinc.com" -UserName "litwareinc\watcher2" -Password "P@ssw0rd"
    Set-CsTestUserCredential -SipAddress "sip:watcher3@litwareinc.com" -UserName "litwareinc\watcher3" -Password "P@ssw0rd"

<span data-ttu-id="72c06-123">Observe que você deve incluir não somente o endereço SIP, mas também o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="72c06-123">Note that you must include not only the SIP address but also the user name and password.</span></span> <span data-ttu-id="72c06-124">Se você não incluir a senha, o Set-CsTestUserCredential solicitará que você insira essas informações.</span><span class="sxs-lookup"><span data-stu-id="72c06-124">If you do not include the password Set-CsTestUserCredential will prompt you to enter that information.</span></span> <span data-ttu-id="72c06-125">O nome de usuário pode ser especificado usando o formato de nome de usuário de nome de domínio \\ mostrado acima ou usando o nome Name@domain usuário do formato; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="72c06-125">The user name can be specified using the domain name\\user name format shown above, or by using the format user name@domain name; for example:</span></span>

    -UserName "watcher3@litwareinc.com"

<span data-ttu-id="72c06-126">Para verificar se as credenciais do usuário de teste foram criadas, execute esses comandos no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="72c06-126">To verify that the test user credentials were created, run these commands from within the Lync Server Management Shell:</span></span>

    Get-CsTestUserCredential -SipAddress "sip:watcher1@litwareinc.com"
    Get-CsTestUserCredential -SipAddress "sip:watcher2@litwareinc.com"
    Get-CsTestUserCredential -SipAddress "sip:watcher3@litwareinc.com"

<span data-ttu-id="72c06-127">Informações semelhantes a isso devem ser retornadas para cada usuário:</span><span class="sxs-lookup"><span data-stu-id="72c06-127">Information similar to this should be returned for each user:</span></span>

    UserName                        Password
    --------                        --------
    Litwareinc\watcher1              System.Security.SecureString

</div>

<div>

## <a name="configuring-a-basic-watcher-node-with-the-default-synthetic-transactions"></a><span data-ttu-id="72c06-128">Configurando um nó de Inspetor básico com as transações sintéticas padrão</span><span class="sxs-lookup"><span data-stu-id="72c06-128">Configuring a Basic Watcher Node with the Default Synthetic Transactions</span></span>

<span data-ttu-id="72c06-129">Após a criação dos usuários de teste, você pode criar um nó de Inspetor usando um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="72c06-129">After the test users have been created you can then create a watcher node by using a command similar to this:</span></span>

    New-CsWatcherNodeConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -PortNumber 5061 -TestUsers @{Add= "sip:watcher1@litwareinc.com","sip:watcher2@litwareinc.com", "sip:watcher3@litwareinc.com"}

<span data-ttu-id="72c06-130">Esse comando cria um novo nó do inspetor que usa as configurações padrão e executa o conjunto padrão de transações sintéticas.</span><span class="sxs-lookup"><span data-stu-id="72c06-130">This command creates a new watcher node that uses the default settings and runs the default set of synthetic transactions.</span></span> <span data-ttu-id="72c06-131">O novo nó do inspetor também usa os usuários de teste watcher1@litwareinc.com, watcher2@litwareinc.com, e watcher3@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="72c06-131">The new watcher node also uses the test users watcher1@litwareinc.com, watcher2@litwareinc.com, and watcher3@litwareinc.com.</span></span> <span data-ttu-id="72c06-132">Se o nó do Inspetor estiver usando a autenticação do TrustedServer, as três contas de teste poderão ser todas as contas de usuário válidas habilitadas para o Active Directory e o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="72c06-132">If the watcher node is using TrustedServer authentication, the three test accounts can be any valid user accounts enabled for Active Directory and Lync Server.</span></span> <span data-ttu-id="72c06-133">Se o nó do Inspetor estiver usando o método de autenticação Negotiate, você também deve habilitar essas contas de usuário para o nó de Inspetor usando o cmdlet **set-CsTestUserCredential** .</span><span class="sxs-lookup"><span data-stu-id="72c06-133">If the watcher node is using the Negotiate authentication method, you must also enable these user accounts for watcher node by using the **Set-CsTestUserCredential** cmdlet.</span></span>

</div>

<div>

## <a name="configuring-extended-tests"></a><span data-ttu-id="72c06-134">Configurando testes estendidos</span><span class="sxs-lookup"><span data-stu-id="72c06-134">Configuring Extended Tests</span></span>

<span data-ttu-id="72c06-135">Se você quiser habilitar a rede telefônica pública comutada (PSTN Test), que verifica a conectividade com a rede telefônica comutada pública, será necessário fazer algumas configurações adicionais ao configurar o nó do Inspetor.</span><span class="sxs-lookup"><span data-stu-id="72c06-135">If you want to enable the public switched telephone network (PSTN test), which verifies connectivity with the public switched telephone network, you will need to do some additional configuration when setting up the watcher node.</span></span> <span data-ttu-id="72c06-136">Primeiro, você precisa associar seus usuários de teste com o tipo de teste PSTN.</span><span class="sxs-lookup"><span data-stu-id="72c06-136">First, you need to associate your test users with the PSTN test type.</span></span> <span data-ttu-id="72c06-137">Para fazer isso, execute um comando semelhante a isso dentro do Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="72c06-137">To do that, run a command similar to this from within the Lync Server Management Shell:</span></span>

    $pstnTest = New-CsExtendedTest -TestUsers "sip:watcher1@litwareinc.com", "sip:watcher2@litwareinc.com", "sip:watcher3@litwareinc.com"  -Name "Contoso Provider Test" -TestType PSTN

<span data-ttu-id="72c06-138">Observe que os resultados desse comando devem ser armazenados em uma variável.</span><span class="sxs-lookup"><span data-stu-id="72c06-138">Note that the results of this command must be stored in a variable.</span></span> <span data-ttu-id="72c06-139">Neste exemplo, isso é uma variável chamada $pstnTest.</span><span class="sxs-lookup"><span data-stu-id="72c06-139">In this example, that's a variable named $pstnTest.</span></span>

<span data-ttu-id="72c06-140">Nesse ponto, você pode usar o cmdlet **New-CsWatcherNodeConfiguration** para associar o tipo de teste (armazenado na variável $pstnTest) a um pool do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="72c06-140">At this point, you can use the **New-CsWatcherNodeConfiguration** cmdlet to associate the test type (stored in the variable $pstnTest) to a Lync Server 2013 pool.</span></span> <span data-ttu-id="72c06-141">Por exemplo, o comando a seguir cria uma nova configuração de nó de inspetor para o pool atl-cs-001.litwareinc.com, adicionando os três usuários de teste que foram criados anteriormente e adicionando também o tipo de teste PSTN:</span><span class="sxs-lookup"><span data-stu-id="72c06-141">For example, the following command creates a new watcher node configuration for the pool atl-cs-001.litwareinc.com, adding the three test users that were created previously, and also adding the PSTN test type:</span></span>

    New-CsWatcherNodeConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -PortNumber 5061 -TestUsers @{Add= "sip:watcher1@litwareinc.com","sip:watcher2@litwareinc.com", "sip:watcher3@litwareinc.com"} -ExtendedTests @{Add=$pstnTest}

<span data-ttu-id="72c06-142">Observe que o comando anterior falhará se você não tiver instalado os arquivos principais do Lync Server e o banco de dados do RTCLocal no computador do nó inspetor.</span><span class="sxs-lookup"><span data-stu-id="72c06-142">Note that the preceding command will fail if you have not installed the Lync Server core files and the RTCLocal database on the watcher node computer.</span></span>

<span data-ttu-id="72c06-143">Para testar várias políticas de voz, você precisa criar um teste estendido para cada política usando o cmdlet **New-CsExtendedTest** .</span><span class="sxs-lookup"><span data-stu-id="72c06-143">To test multiple voice policies, you need to create an extended test for each policy by using the **New-CsExtendedTest** cmdlet.</span></span> <span data-ttu-id="72c06-144">Os usuários atribuídos a esse teste devem ser configurados com as políticas de voz desejadas.</span><span class="sxs-lookup"><span data-stu-id="72c06-144">The users assigned to this test should be configured with the desired voice policies.</span></span> <span data-ttu-id="72c06-145">Os testes estendidos são passados para o cmdlet **New-CsWatcherNodeConfiguration** usando um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="72c06-145">The extended tests are then passed to the **New-CsWatcherNodeConfiguration** cmdlet by using a command similar to the following:</span></span>

    -ExtendedTests @{Add=$pstnTest1,$pstnTest2,$pstnTest3}

<span data-ttu-id="72c06-146">Se New-CsWatcherNodeConfiguration for chamado sem usar o parâmetro testes, isso significa que somente as transações sintéticas padrão (e a transação sintética estendida especificada) serão habilitadas para o novo nó inspetor.</span><span class="sxs-lookup"><span data-stu-id="72c06-146">If New-CsWatcherNodeConfiguration is called without using the Tests parameter, that means that only the Default synthetic transactions (and the specified extended synthetic transaction) will be enabled for the new watcher node.</span></span> <span data-ttu-id="72c06-147">Isso significa que o nó do Inspetor testará os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="72c06-147">This means that the watcher node will test the following components:</span></span>

  - <span data-ttu-id="72c06-148">Registro</span><span class="sxs-lookup"><span data-stu-id="72c06-148">Registration</span></span>

  - <span data-ttu-id="72c06-149">IM</span><span class="sxs-lookup"><span data-stu-id="72c06-149">IM</span></span>

  - <span data-ttu-id="72c06-150">GroupIM (mensagens instantâneas de grupo)</span><span class="sxs-lookup"><span data-stu-id="72c06-150">GroupIM</span></span>

  - <span data-ttu-id="72c06-151">P2PAV (sessões de áudio/vídeo ponto a ponto)</span><span class="sxs-lookup"><span data-stu-id="72c06-151">P2PAV (peer-to-peer audio/video sessions)</span></span>

  - <span data-ttu-id="72c06-152">AvConference (áudio/conferência)</span><span class="sxs-lookup"><span data-stu-id="72c06-152">AvConference (audio/conferencing)</span></span>

  - <span data-ttu-id="72c06-153">Presença</span><span class="sxs-lookup"><span data-stu-id="72c06-153">Presence</span></span>

  - <span data-ttu-id="72c06-154">ABS (serviço do Catálogo de Endereços)</span><span class="sxs-lookup"><span data-stu-id="72c06-154">ABS (Address Book service)</span></span>

  - <span data-ttu-id="72c06-155">ABWQ (serviço Web do Catálogo de Endereços)</span><span class="sxs-lookup"><span data-stu-id="72c06-155">ABWQ (Address Book web service)</span></span>

  - <span data-ttu-id="72c06-156">PSTN (chamadas de gateway PSTN, especificadas como teste estendido.</span><span class="sxs-lookup"><span data-stu-id="72c06-156">PSTN (PSTN gateway calls, specified as an extended test.</span></span> <span data-ttu-id="72c06-157">Por padrão, PSTN está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="72c06-157">By default, PSTN is disabled.</span></span> <span data-ttu-id="72c06-158">O teste está habilitado nesse caso somente porque o comando habilitou PSTN usando o parâmetro ExtendedTests.)</span><span class="sxs-lookup"><span data-stu-id="72c06-158">The test is enabled in this case only because the command enabled PSTN by using the ExtendedTests parameter.)</span></span>

<span data-ttu-id="72c06-159">Isso também significa que os seguintes componentes não serão testados por padrão:</span><span class="sxs-lookup"><span data-stu-id="72c06-159">This also means that the following components will not be tested by default:</span></span>

  - <span data-ttu-id="72c06-160">AVEdgeConnectivity</span><span class="sxs-lookup"><span data-stu-id="72c06-160">AVEdgeConnectivity</span></span>

  - <span data-ttu-id="72c06-161">MCXP2PIM (mensagens instantâneas do dispositivo móvel)</span><span class="sxs-lookup"><span data-stu-id="72c06-161">MCXP2PIM (mobile device instant messaging)</span></span>

  - <span data-ttu-id="72c06-162">ExumConnectivity (Unificação de Mensagens do Exchange)</span><span class="sxs-lookup"><span data-stu-id="72c06-162">ExumConnectivity (Exchange Unified Messaging)</span></span>

  - <span data-ttu-id="72c06-163">JoinLauncher</span><span class="sxs-lookup"><span data-stu-id="72c06-163">JoinLauncher</span></span>

  - <span data-ttu-id="72c06-164">PersistentChatMessage</span><span class="sxs-lookup"><span data-stu-id="72c06-164">PersistentChatMessage</span></span>

  - <span data-ttu-id="72c06-165">DataConference</span><span class="sxs-lookup"><span data-stu-id="72c06-165">DataConference</span></span>

  - <span data-ttu-id="72c06-166">XmppIM</span><span class="sxs-lookup"><span data-stu-id="72c06-166">XmppIM</span></span>

  - <span data-ttu-id="72c06-167">UnifiedContactStore</span><span class="sxs-lookup"><span data-stu-id="72c06-167">UnifiedContactStore</span></span>

</div>

<div>

## <a name="adding-and-removing-synthetic-transactions"></a><span data-ttu-id="72c06-168">Adicionando e removendo transações sintéticas</span><span class="sxs-lookup"><span data-stu-id="72c06-168">Adding and Removing Synthetic Transactions</span></span>

<span data-ttu-id="72c06-169">Após a configuração de um nó de Inspetor, você pode usar o cmdlet **set-CsWatcherNodeConfiguration** para adicionar ou remover transações sintéticas do nó.</span><span class="sxs-lookup"><span data-stu-id="72c06-169">After a watcher node has been configured, you can use the **Set-CsWatcherNodeConfiguration** cmdlet to add or remove synthetic transactions from the node.</span></span> <span data-ttu-id="72c06-170">Por exemplo, para adicionar o teste PersistentChatMessage ao nó do inspetor, use o método Add e um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="72c06-170">For example, to add the PersistentChatMessage test to the watcher node, use the Add method and a command similar to this:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Add="PersistentChatMessage"}

<span data-ttu-id="72c06-171">É possível adicionar vários testes separando os nomes de teste com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="72c06-171">Multiple tests can be added by separating the test names by using commas.</span></span> <span data-ttu-id="72c06-172">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="72c06-172">For example:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Add="PersistentChatMessage","DataConference","UnifiedContactStore"}

<span data-ttu-id="72c06-173">Observe que um erro ocorrerá se um ou mais desses testes (por exemplo, dataconferência) já tiver sido habilitado no nó inspetor.</span><span class="sxs-lookup"><span data-stu-id="72c06-173">Note that an error will occur if one or more of these tests (for example, DataConference) has already been enabled on the watcher node.</span></span> <span data-ttu-id="72c06-174">Nesse caso, você receberá uma mensagem de erro semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="72c06-174">In this case, you will receive an error message similar to the following:</span></span>

    Set-CsWatcherNodeConfiguration : There is a duplicate key sequence 'DataConference' for the 'urn:schema:Microsoft.Rtc.Management.Settings.WatcherNode.2010:TestName' key or unique identity constraint.

<span data-ttu-id="72c06-175">Quando esse erro ocorre, nenhuma alteração será aplicada.</span><span class="sxs-lookup"><span data-stu-id="72c06-175">When this error occurs, no changes will be applied.</span></span> <span data-ttu-id="72c06-176">O comando deve ser executado novamente com o teste duplicado removido.</span><span class="sxs-lookup"><span data-stu-id="72c06-176">The command should be rerun with the duplicate test removed.</span></span>

<span data-ttu-id="72c06-177">Para remover uma transação sintética de um nó de Inspetor, use o método Remove em vez do método Add.</span><span class="sxs-lookup"><span data-stu-id="72c06-177">To remove a synthetic transaction from a watcher node, use the Remove method instead of the Add method.</span></span> <span data-ttu-id="72c06-178">Por exemplo, esse comando remove o teste ABWQ do nó do inspetor:</span><span class="sxs-lookup"><span data-stu-id="72c06-178">For example, this command removes the ABWQ test from a watcher node:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Remove="ABWQ"}

<span data-ttu-id="72c06-179">Você também pode usar o método Replace para substituir todos os testes habilitados no momento por um ou mais testes novos.</span><span class="sxs-lookup"><span data-stu-id="72c06-179">You can also use the Replace method to replace all the currently-enabled tests with one or more new tests.</span></span> <span data-ttu-id="72c06-180">Por exemplo, se você quiser apenas um nó de inspetor para executar o teste de mensagem instantânea, poderá configurá-lo usando este comando:</span><span class="sxs-lookup"><span data-stu-id="72c06-180">For example, if you only want a watcher node to run the IM test, you can configure that by using this command:</span></span>

    Set-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" -Tests @{Replace="IM"}

<span data-ttu-id="72c06-181">Quando você executa o comando anterior, todas as transações sintéticas do nó de Inspetor especificado serão desabilitadas, exceto para mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="72c06-181">When you run the preceding command, all synthetic transactions on the specified watcher node will be disabled except for IM.</span></span>

</div>

<div>

## <a name="viewing-and-testing-the-watcher-node-configuration"></a><span data-ttu-id="72c06-182">Exibindo e testando a configuração do nó do inspetor</span><span class="sxs-lookup"><span data-stu-id="72c06-182">Viewing and Testing the Watcher Node Configuration</span></span>

<span data-ttu-id="72c06-183">Se quiser exibir os testes que foram atribuídos ao nó do inspetor, use um comando semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="72c06-183">If you want to view the tests that have been assigned to a watcher node, use a command similar to this:</span></span>

    Get-CsWatcherNodeConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object -ExpandProperty Tests

<span data-ttu-id="72c06-184">O comando anterior retornará informações parecidas com isso, dependendo das transações sintéticas que foram atribuídas ao nó:</span><span class="sxs-lookup"><span data-stu-id="72c06-184">The preceding command will return information similar to this, depending on the synthetic transactions that have been assigned to the node:</span></span>

    Registration
    IM
    GroupIM
    P2PAV
    AvConference
    Presence
    PersistentChatMessage
    DataConference

<div>


> [!TIP]
> <span data-ttu-id="72c06-185">Para exibir as transações sintéticas em ordem alfabética, use este comando:</span><span class="sxs-lookup"><span data-stu-id="72c06-185">To view the synthetic transactions in alphabetical order, use this command instead:</span></span><BR><span data-ttu-id="72c06-186">Get-CsWatcherNodeConfiguration – identidade "atl-cs-001.litwareinc.com" | Select-Object – ExpandProperty Tests | Sort-Object</span><span class="sxs-lookup"><span data-stu-id="72c06-186">Get-CsWatcherNodeConfiguration –Identity "atl-cs-001.litwareinc.com" | Select-Object –ExpandProperty Tests | Sort-Object</span></span>



</div>

<span data-ttu-id="72c06-187">Para verificar se um nó de inspetor foi criado, digite o seguinte comando no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="72c06-187">To verify that a watcher node has been created, type the following command from within the Lync Server Management Shell:</span></span>

    Get-CsWatcherNodeConfiguration

<span data-ttu-id="72c06-188">Você receberá informações semelhantes a esta:</span><span class="sxs-lookup"><span data-stu-id="72c06-188">You will receive information similar to this:</span></span>

    Identity      : atl-cs-001.litwareinc.com
    TestUsers     : {sip:watcher1@litwareinc.com, sip:watcher2@litwareinc.com ...}
    ExtendedTests : {TestUsers=IList<System.String>;Name=PSTN Test; Te...}
    TargetFqdn    : atl-cs-001.litwareinc.com
    PortNumber    : 5061

<span data-ttu-id="72c06-189">Para verificar se o nó do inspetor foi configurado corretamente, digite o seguinte comando no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="72c06-189">To verify that the watcher node has been configured correctly, type the following command from within the Lync Server Management Shell:</span></span>

    Test-CsWatcherNodeConfiguration

<span data-ttu-id="72c06-190">O comando anterior testará cada nó de Inspetor em sua implantação e informará a você as informações, como se:</span><span class="sxs-lookup"><span data-stu-id="72c06-190">The preceding command will test each watcher node in your deployment and tell you information, such as whether:</span></span>

  - <span data-ttu-id="72c06-191">A função registrador necessária foi instalada.</span><span class="sxs-lookup"><span data-stu-id="72c06-191">The required Registrar role been installed.</span></span>

  - <span data-ttu-id="72c06-192">A chave do Registro necessária foi criada para você quando você executou Set-CsWatcherNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="72c06-192">The required registry key was created for you when you ran Set-CsWatcherNodeConfiguration.</span></span>

  - <span data-ttu-id="72c06-193">Seus servidores estão executando a versão correta do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="72c06-193">Your servers are running the correct version of Lync Server.</span></span>

  - <span data-ttu-id="72c06-194">Suas portas foram configuradas corretamente.</span><span class="sxs-lookup"><span data-stu-id="72c06-194">Your ports been configured correctly.</span></span>

  - <span data-ttu-id="72c06-195">Seus usuários de teste atribuídos têm as credenciais necessárias.</span><span class="sxs-lookup"><span data-stu-id="72c06-195">Your assigned test users have the required credentials.</span></span>

<span data-ttu-id="72c06-196"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72c06-196"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

