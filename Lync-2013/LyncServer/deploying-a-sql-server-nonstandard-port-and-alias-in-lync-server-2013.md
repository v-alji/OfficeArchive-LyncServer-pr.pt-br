---
title: Implantando porta não padrão e alias do SQL Server no Lync Server 2013
description: Implantação de uma porta e alias não padrão do SQL Server no Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a SQL Server nonstandard port and alias in Lync Server 2013
ms:assetid: 2da92c1f-250e-407a-8651-fb2aec76aeb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn776290(v=OCS.15)
ms:contentKeyID: 62634609
ms.date: 09/17/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da76db2b946a47e13fe3549d7184b0b12894a83a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389810"
---
# <a name="deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="61ed2-103">Implantando porta não padrão e alias do SQL Server no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61ed2-103">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61ed2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61ed2-104">

<span> </span></span></span>

<span data-ttu-id="61ed2-105">_**Tópico da última modificação:** 2015-09-16_</span><span class="sxs-lookup"><span data-stu-id="61ed2-105">_**Topic Last Modified:** 2015-09-16_</span></span>

<span data-ttu-id="61ed2-106">O Microsoft Lync Server 2013 oferece suporte ao uso de uma porta e alias não padrão no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61ed2-106">Microsoft Lync Server 2013 supports using a non-standard port and alias in SQL Server.</span></span> <span data-ttu-id="61ed2-107">Usar uma porta não padrão do SQL Server e um alias aumenta a segurança e cria um ambiente mais flexível para a implantação do Lync.</span><span class="sxs-lookup"><span data-stu-id="61ed2-107">Using a SQL Server non-standard port and an alias increases security and creates a more flexible environment for the Lync deployment.</span></span> <span data-ttu-id="61ed2-108">Estas etapas são apenas uma única etapa para a proteção adequada do ambiente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-108">These steps are only a single step in properly securing your Lync Server 2013 environment.</span></span> <span data-ttu-id="61ed2-109">Etapas adicionais devem ser seguidas para reduzir a superfície de ataque de uma implementação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-109">Additional steps should be taken to reduce the attack surface of a Lync Server 2013 implementation.</span></span>

<span data-ttu-id="61ed2-110">O artigo a seguir descreve as etapas necessárias para configurar uma porta não padrão do SQL Server e alias no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-110">The following article describes the steps required to setup a SQL Server non-standard port and alias in Lync Server 2013.</span></span>

<div>

## <a name="deploying-a-sql-server-non-standard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="61ed2-111">Implantando uma porta e um alias não padrão do SQL Server no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61ed2-111">Deploying a SQL Server Non-Standard Port and Alias in Lync Server 2013</span></span>

<span data-ttu-id="61ed2-112">O construtor de topologias do Lync Server 2013 oferece suporte ao uso de um alias do SQL Server como o FQDN (nome de domínio totalmente qualificado) em vez do FQDN do SQL Server atual ao configurar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-112">Lync Server 2013 Topology Builder supports using a SQL Server alias as the Fully Qualified Domain Name (FQDN) instead of the actual SQL Server FQDN when configuring Lync Server 2013.</span></span> <span data-ttu-id="61ed2-113">Isso permite que o FQDN real do SQL Server fique oculto de qualquer invasor mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="61ed2-113">This allows the actual SQL Server FQDN to be hidden from any malicious attacker.</span></span> <span data-ttu-id="61ed2-114">Além disso, o uso de uma porta não padrão obscurece a porta real de qualquer invasor que esteja tentando atacar o banco de dados na porta padrão 1433, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-114">In addition, using a non-standard port obscures the actual port from any would be attacker attempting to attack the database on the standard port 1433, as shown in the following figure.</span></span>

<span data-ttu-id="61ed2-115">![Um hacker não sabe o número da porta a ser atacado.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "Um hacker não sabe o número da porta a ser atacado.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-115">![A hacker doesn't know the port number to attack.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "A hacker doesn't know the port number to attack.")</span></span>

<span data-ttu-id="61ed2-116">Para ter êxito ao determinar que a porta do Lync Server 2013 está usando para se comunicar com o SQL Server, o invasor precisaria verificar todas as portas para obter as informações de porta.</span><span class="sxs-lookup"><span data-stu-id="61ed2-116">In order to be successful in determining the port Lync Server 2013 is using to communicate with SQL Server, the attacker would need to scan all ports to obtain the port information.</span></span> <span data-ttu-id="61ed2-117">Uma verificação de porta por um invasor aumenta a probabilidade de que a segurança possa detectar e interromper a instrução.</span><span class="sxs-lookup"><span data-stu-id="61ed2-117">A port scan by an attacker increases the chances that security can detect and stop the instruction.</span></span> <span data-ttu-id="61ed2-118">Além de adicionar maior segurança com uma porta não padrão, você também pode usar um alias do SQL Server para fornecer flexibilidade para a implantação.</span><span class="sxs-lookup"><span data-stu-id="61ed2-118">In addition to adding increased security with a non-standard port, you can also use a SQL Server alias to provide flexibility for the deployment.</span></span> <span data-ttu-id="61ed2-119">Isso é útil para reduzir as alterações de configuração em situações em que uma alteração de nome do SQL Server é necessária.</span><span class="sxs-lookup"><span data-stu-id="61ed2-119">This is valuable in order to reduce configuration changes in situations where a SQL Server name change is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="61ed2-120">O SQL Server oferece dois métodos de tolerância a falhas (clustering de failover e espelhamento).</span><span class="sxs-lookup"><span data-stu-id="61ed2-120">SQL Server provides two fault tolerance methods (Failover Clustering and Mirroring).</span></span> <span data-ttu-id="61ed2-121">Os dois métodos de tolerância a falhas do SQL Server têm suporte usando uma porta não padrão do SQL Server e alias com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-121">Both SQL Server fault tolerance methods are supported using a SQL Server non-standard port and alias with Lync Server 2013.</span></span> <span data-ttu-id="61ed2-122">Se o back-end do SQL Server usado pelo pool estiver em uma configuração espelhada, então o serviço do SQL browser nos servidores back-end do SQL Server deverá estar em execução para servidores front-end para se conectar ao banco de dados espelhado quando os bancos de dados tiverem failover para o SQL Server espelhado.</span><span class="sxs-lookup"><span data-stu-id="61ed2-122">If the SQL Server backend used by the pool is in a mirrored configuration, then the SQL browser service on the SQL Server backend servers should be running for Front End servers to connect to the mirrored database when the databases are failed over to the mirrored SQL Server.</span></span>



</div>

<span data-ttu-id="61ed2-123">Ao configurar a conectividade de banco de dados do SQL Server no construtor de topologias, ou ao usar o cmdlet Install-CsDatabase, não é possível definir explicitamente um número de porta não padrão do SQL Server e associá-lo a uma instância SQL.</span><span class="sxs-lookup"><span data-stu-id="61ed2-123">When configuring SQL Server database connectivity from within Topology Builder, or when using the Install-CsDatabase cmdlet, it’s not possible to explicitly define a SQL Server non-standard port number and associate it with a SQL instance.</span></span> <span data-ttu-id="61ed2-124">Para definir uma porta não padrão, você precisará usar os utilitários do SQL Server e do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="61ed2-124">To set a non-standard port, you’ll need to use SQL Server and Windows Server utilities.</span></span>

<span data-ttu-id="61ed2-125">Para configurar uma porta e um alias não padrão do SQL Server para uso com o Lync Server 2013, será necessário concluir três etapas principais.</span><span class="sxs-lookup"><span data-stu-id="61ed2-125">To set up a SQL Server non-standard port and alias for use with Lync Server 2013, you will need to complete three primary steps.</span></span> <span data-ttu-id="61ed2-126">Estas etapas são:</span><span class="sxs-lookup"><span data-stu-id="61ed2-126">These steps are:</span></span>

  - <span data-ttu-id="61ed2-127">Confirme se o Lync Server 2013 tem as atualizações mais recentes aplicadas.</span><span class="sxs-lookup"><span data-stu-id="61ed2-127">Confirm that Lync Server 2013 has the Latest Updates Applied.</span></span>

  - <span data-ttu-id="61ed2-128">Configurar a porta e o alias não padrão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61ed2-128">Setup the SQL Server Non-Standard Port and Alias.</span></span>

  - <span data-ttu-id="61ed2-129">Configure o Lync Server 2013 com o alias do SQL Server usando o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="61ed2-129">Configure Lync Server 2013 with the SQL Server alias using Topology Builder.</span></span>

  - <span data-ttu-id="61ed2-130">Publique a topologia e verifique o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="61ed2-130">Publish the Topology, and Verify the Database.</span></span>

<div>

## <a name="confirm-that-lync-server-2013-has-the-latest-updates-applied"></a><span data-ttu-id="61ed2-131">Confirme se o Lync Server 2013 tem as atualizações mais recentes aplicadas</span><span class="sxs-lookup"><span data-stu-id="61ed2-131">Confirm that Lync Server 2013 has the Latest Updates Applied</span></span>

<span data-ttu-id="61ed2-132">É importante manter atualizado o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-132">It is important to keep Lync Server 2013 up to date.</span></span> <span data-ttu-id="61ed2-133">Para verificar as atualizações e informações mais recentes sobre como aplicá-las, confira [atualizações para o Lync Server 2013](https://support.microsoft.com/kb/2809243).</span><span class="sxs-lookup"><span data-stu-id="61ed2-133">To check for the most recent updates and information on how to apply them, see [Updates for Lync Server 2013](https://support.microsoft.com/kb/2809243).</span></span>

</div>

<div>

## <a name="setup-the-sql-server-non-standard-port-and-alias"></a><span data-ttu-id="61ed2-134">Configurar a porta e o alias não padrão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="61ed2-134">Setup the SQL Server Non-Standard Port and Alias</span></span>

<span data-ttu-id="61ed2-135">A porta e o alias não padrão do SQL Server devem ser configurados na instância do banco de dados para que ele possa ser referenciado do construtor de topologias do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-135">The SQL Server non-standard port and alias must be set up on the database instance before it can be referenced from Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="61ed2-136">Para configurar uma porta e um alias não padrão do SQL Server, será necessário concluir três etapas principais.</span><span class="sxs-lookup"><span data-stu-id="61ed2-136">To set up a SQL Server non-standard port and alias, you will have to complete three primary steps.</span></span> <span data-ttu-id="61ed2-137">Estas etapas são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="61ed2-137">These steps are as follows:</span></span>

  - <span data-ttu-id="61ed2-138">Altere os valores de protocolo TCP/IP padrão.</span><span class="sxs-lookup"><span data-stu-id="61ed2-138">Change the Default TCP/IP Protocol Values.</span></span>

  - <span data-ttu-id="61ed2-139">Criar e configurar um alias do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61ed2-139">Create and Configure a SQL Server Alias.</span></span>

  - <span data-ttu-id="61ed2-140">Criar um registro de recurso de nome canônico (CNAME) do sistema de nome de domínio (DNS).</span><span class="sxs-lookup"><span data-stu-id="61ed2-140">Create a Domain Name System (DNS) Canonical Name (CNAME) Resource Record.</span></span>

<span data-ttu-id="61ed2-141">**Modificar os valores de protocolo TCP/IP padrão**</span><span class="sxs-lookup"><span data-stu-id="61ed2-141">**Modify the Default TCP/IP Protocol Values**</span></span>

1.  <span data-ttu-id="61ed2-142">Selecione **Iniciar** e escolha **Gerenciador de configuração do SQL Server**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-142">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-143">![O ícone do SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "O ícone do SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="61ed2-143">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="61ed2-144">No painel de navegação, escolha expandir a **instância do SQL Server**, escolha expandir a **configuração de rede do SQL Server** e escolha **protocolos \<instance name\> para**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-144">In the navigation pane, choose to expand the **SQL Server instance**, choose to expand **SQL Server Network Configuration**, and choose **Protocols for \<instance name\>**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-145">![Navegar para as propriedades de TCP/IP](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navegar para as propriedades de TCP/IP")</span><span class="sxs-lookup"><span data-stu-id="61ed2-145">![Navigate to TCP/IP Properties](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navigate to TCP/IP Properties")</span></span>

3.  <span data-ttu-id="61ed2-146">No painel direito, clique com o botão direito do mouse em **TCP/IP** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="61ed2-146">In the right pane, right-click **TCP/IP**, and select **Properties**.</span></span> <span data-ttu-id="61ed2-147">A caixa de diálogo Propriedades de TCP/IP é exibida.</span><span class="sxs-lookup"><span data-stu-id="61ed2-147">The TCP/IP Properties dialog box is displayed.</span></span>

4.  <span data-ttu-id="61ed2-148">Selecione a guia **endereços IP** . A guia endereços IP mostra todos os endereços IP ativos no servidor.</span><span class="sxs-lookup"><span data-stu-id="61ed2-148">Select the **IP Addresses** tab. The IP Addresses tab shows all of the active IP addresses on the server.</span></span> <span data-ttu-id="61ed2-149">Elas estão no formato IP1, IP2, até IPAll, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-149">These are in the format IP1, IP2, up to IPAll, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-150">![Abra as propriedades de TCP/IP.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Abra as propriedades de TCP/IP.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-150">![Open TCP/IP properties.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Open TCP/IP properties.")</span></span>

5.  <span data-ttu-id="61ed2-151">Desmarque o campo **portas TCP dinâmicas** para todos os endereços IP.</span><span class="sxs-lookup"><span data-stu-id="61ed2-151">Clear the **TCP Dynamic Ports** field for all IP addresses.</span></span> <span data-ttu-id="61ed2-152">Se o campo contiver um caractere zero, significará que o SQL Server está ouvindo portas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="61ed2-152">If the field contains a zero character, then it means SQL Server is listening on dynamic ports.</span></span> <span data-ttu-id="61ed2-153">Certifique-se de que esses campos estejam limpos e não contenham zero.</span><span class="sxs-lookup"><span data-stu-id="61ed2-153">Make sure these fields are cleared and do not contain a zero.</span></span>

6.  <span data-ttu-id="61ed2-154">Para o endereço IP que o Lync Server usará para se conectar ao banco de dados, verifique se **habilitado** está definido como **Sim**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-154">For the IP address that Lync Server will be using to connect to the database, make sure that **Enabled** is set to **Yes**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-155">![Defina Enabled como Yes para o IP correto.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Defina Enabled como Yes para o IP correto.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-155">![Set enabled as Yes for the correct IP.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Set enabled as Yes for the correct IP.")</span></span>

7.  <span data-ttu-id="61ed2-156">Na seção **IPAll** na parte inferior da caixa de diálogo, insira a porta desejada no campo **porta TCP** , conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-156">In the **IPAll** section at the bottom of the dialog, enter the desired port in the **TCP Port** field, as shown in the following figure.</span></span> <span data-ttu-id="61ed2-157">Neste exemplo, usamos a porta 50062, mas você pode usar qualquer porta entre o 49152 e o 65535.</span><span class="sxs-lookup"><span data-stu-id="61ed2-157">In this example, we use port 50062, but you can use any port between 49152 and 65535.</span></span> <span data-ttu-id="61ed2-158">Estas são as portas atribuídas ao uso dinâmico e privado, e isso garante que você não entre em conflito com outras portas usadas na implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61ed2-158">These are the ports assigned to dynamic and private use, and this ensures you won’t conflict with other ports being used in the Lync Server 2013 deployment.</span></span>
    
    <span data-ttu-id="61ed2-159">![Defina a porta na seção IPAll.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Defina a porta na seção IPAll.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-159">![Set port in IPAll section.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Set port in IPAll section.")</span></span>

8.  <span data-ttu-id="61ed2-160">Escolha **OK** para sair da caixa de diálogo Propriedades de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="61ed2-160">Choose **OK** to exit the TCP/IP Properties dialog.</span></span>

9.  <span data-ttu-id="61ed2-161">Reinicie a instância do SQL Server selecionando **Serviços do SQL Server** no painel esquerdo do Gerenciador de configuração do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61ed2-161">Restart the SQL Server instance by selecting **SQL Server Services** in the left pane of SQL Server Configuration Manager.</span></span> <span data-ttu-id="61ed2-162">Em seguida, clique com o botão direito do mouse em **SQL Server \<instance name\>** no painel direito e selecione **reiniciar**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-162">Then right-click **SQL Server \<instance name\>** in the right pane, and select **Restart**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-163">![Redefina o serviço do SQL Server por exemplo.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Redefina o serviço do SQL Server por exemplo.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-163">![Reset the SQL Server service for instance.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Reset the SQL Server service for instance.")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="61ed2-164">Certifique-se de atualizar as configurações do seu firewall para acomodar a nova porta do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61ed2-164">Make sure you update your firewall settings to accommodate the new SQL Server port.</span></span>



</div>

<span data-ttu-id="61ed2-165">**Criar e configurar um alias do SQL Server**</span><span class="sxs-lookup"><span data-stu-id="61ed2-165">**Create and Configure a SQL Server Alias**</span></span>

1.  <span data-ttu-id="61ed2-166">Selecione **Iniciar** e escolha **Gerenciador de configuração do SQL Server**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-166">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-167">![O ícone do SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "O ícone do SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="61ed2-167">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="61ed2-168">No painel esquerdo, escolha para expandir a **instância do SQL Server**, escolha expandir a **\<version\> configuração do SQL Native Client** e, em seguida, escolha **aliases**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-168">In the left pane, choose to expand **SQL Server instance**, choose to expand **SQL Native Client \<version\> Configuration**, and then choose **Aliases**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-169">![Aliases no Gerenciador de configuração do SQL Server.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliases no Gerenciador de configuração do SQL Server.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-169">![Aliases in SQL Server Configuration Manager.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliases in SQL Server Configuration Manager.")</span></span>

3.  <span data-ttu-id="61ed2-170">Clique com o botão direito do mouse em **alias** e selecione **novo alias..**..</span><span class="sxs-lookup"><span data-stu-id="61ed2-170">Right-click **Aliases**, and select **New Alias…**.</span></span>

4.  <span data-ttu-id="61ed2-171">Digite o **nome do alias**, o **número da porta**, o **protocolo** e o **servidor**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-171">Enter the **Alias Name**, **Port Number**, **Protocol**, and **Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-172">![Criando um novo alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Criando um novo alias")</span><span class="sxs-lookup"><span data-stu-id="61ed2-172">![Creating a new alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Creating a new alias")</span></span>
    
    <div>
    

    > [!CAUTION]  
    > <span data-ttu-id="61ed2-173">Certifique-se de digitar a mesma porta não padrão que você usou na etapa anterior, pois a porta do SQL Server estará ouvindo.</span><span class="sxs-lookup"><span data-stu-id="61ed2-173">Make sure to enter the same non-standard port you used in the previous step since that is the port SQL Server will be listening on.</span></span> <span data-ttu-id="61ed2-174">Se um alias configurado estiver se conectando ao FQDN ou à instância errada do SQL Server, desabilite e habilite novamente o protocolo de rede associado.</span><span class="sxs-lookup"><span data-stu-id="61ed2-174">If a configured alias is connecting to the wrong SQL Server FQDN or Instance, disable and then re-enable the associated network protocol.</span></span> <span data-ttu-id="61ed2-175">Isso limpa todas as informações de conexão armazenadas em cache e permite que o cliente se conecte corretamente.</span><span class="sxs-lookup"><span data-stu-id="61ed2-175">Doing this clears any cached connection information and allows the client to connect correctly.</span></span>

    
    </div>

<span data-ttu-id="61ed2-176">**Criar um registro de recurso CNAME de DNS**</span><span class="sxs-lookup"><span data-stu-id="61ed2-176">**Create a DNS CNAME Resource Record**</span></span>

1.  <span data-ttu-id="61ed2-177">Entre no computador Gerenciando o DNS.</span><span class="sxs-lookup"><span data-stu-id="61ed2-177">Sign into the computer managing DNS.</span></span>

2.  <span data-ttu-id="61ed2-178">Selecione **Iniciar** e escolha **Gerenciador de servidores**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-178">Select **Start**, and choose **Server Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-179">![Abrindo o Gerenciador de servidores](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Abrindo o Gerenciador de servidores")</span><span class="sxs-lookup"><span data-stu-id="61ed2-179">![Opening Server Manager](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Opening Server Manager")</span></span>

3.  <span data-ttu-id="61ed2-180">Escolha a lista suspensa **ferramentas** e selecione **DNS**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-180">Choose the **Tools** drop-down, and select **DNS**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-181">![Abrindo o DNS do Gerenciador de servidores.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Abrindo o DNS do Gerenciador de servidores.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-181">![Opening DNS from Server Manager.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Opening DNS from Server Manager.")</span></span>

4.  <span data-ttu-id="61ed2-182">No painel esquerdo, expanda o nó nome do servidor, expanda o nó de zonas de pesquisa direta e escolha o domínio relevante.</span><span class="sxs-lookup"><span data-stu-id="61ed2-182">In the left pane, expand the server name node, expand the Forward Lookup Zones node, and choose the relevant domain.</span></span>

5.  <span data-ttu-id="61ed2-183">Clique com o botão direito do mouse no domínio e selecione **novo alias (CNAME)...**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-183">Right-click the domain, and select **New Alias (CNAME)…**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-184">![Selecionando a opção para criar um novo alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selecionando a opção para criar um novo alias CNAME")</span><span class="sxs-lookup"><span data-stu-id="61ed2-184">![Selecting option to create a new alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selecting option to create a new alias CNAME")</span></span>

6.  <span data-ttu-id="61ed2-185">Digite o **nome do alias** e o **FQDN do SQL Server**, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-185">Enter the **Alias Name** and the **FQDN for SQL Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-186">![Preenchendo a caixa de diálogo novo alias CNAME.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Preenchendo a caixa de diálogo novo alias CNAME.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-186">![Filling in the new alias CNAME dialog.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Filling in the new alias CNAME dialog.")</span></span>

7.  <span data-ttu-id="61ed2-187">Escolha **OK** para salvar o CNAME e exibi-lo no Gerenciador de DNS.</span><span class="sxs-lookup"><span data-stu-id="61ed2-187">Choose **OK** to save the CNAME and view it in DNS Manager.</span></span>

</div>

<div>

## <a name="validate-database-connectivity"></a><span data-ttu-id="61ed2-188">Validar a conectividade do banco de dados</span><span class="sxs-lookup"><span data-stu-id="61ed2-188">Validate Database Connectivity</span></span>

<span data-ttu-id="61ed2-189">Há muitas maneiras diferentes de verificar se ele está funcionando.</span><span class="sxs-lookup"><span data-stu-id="61ed2-189">There are many different ways to make sure it is working.</span></span> <span data-ttu-id="61ed2-190">Você deseja certificar-se de que o banco de dados do SQL Server está ouvindo na porta especificada usando o alias.</span><span class="sxs-lookup"><span data-stu-id="61ed2-190">You want to make sure that the SQL Server database is listening on the specified port using the alias.</span></span> <span data-ttu-id="61ed2-191">Uma verificação rápida pode ser completada usando os comandos **netstat** e **Telnet** .</span><span class="sxs-lookup"><span data-stu-id="61ed2-191">A quick check can be completed using the **netstat** and **telnet** commands.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="61ed2-192">O cliente Telnet é um recurso que vem com o Windows Server, mas que deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="61ed2-192">Telnet Client is a Feature that comes with Windows Server but that must be installed.</span></span> <span data-ttu-id="61ed2-193">Um recurso do Windows Server pode ser instalado abrindo o Gerenciador do servidor e selecionando Adicionar funções e recursos no menu gerenciar.</span><span class="sxs-lookup"><span data-stu-id="61ed2-193">A Windows Server Feature can be installed by opening Server Manager and selecting Add Roles and Features from the Manage menu.</span></span>



</div>

<span data-ttu-id="61ed2-194">**Usar netstat e Telnet para verificar a conectividade do banco de dados**</span><span class="sxs-lookup"><span data-stu-id="61ed2-194">**Use netstat and telnet to verify database connectivity**</span></span>

1.  <span data-ttu-id="61ed2-195">Selecione **Iniciar** e digite **cmd** para abrir um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="61ed2-195">Select **Start**, and type **cmd** to open a command prompt.</span></span>

2.  <span data-ttu-id="61ed2-196">Digite **netstat-a-f** e confirme se o SQL Server está em execução com a porta correta, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="61ed2-196">Type **netstat -a -f**, and confirm that SQL Server is running with the correct port, as shown in the following figure.</span></span>
    
    <span data-ttu-id="61ed2-197">![Usando netstat para verificar a porta.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Usando netstat para verificar a porta.")</span><span class="sxs-lookup"><span data-stu-id="61ed2-197">![Using netstat to verify port.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Using netstat to verify port.")</span></span>

3.  <span data-ttu-id="61ed2-198">Digite **Telnet \<alias name\> \<port \#\>** para confirmar a conexão com a instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61ed2-198">Type **telnet \<alias name\> \<port \#\>** to confirm the connection to the SQL Server instance.</span></span> <span data-ttu-id="61ed2-199">Se a conexão for bem-sucedida, o telnet será conectado e você não verá um erro.</span><span class="sxs-lookup"><span data-stu-id="61ed2-199">If the connection is successful, telnet will connect and you shouldn’t see an error.</span></span> <span data-ttu-id="61ed2-200">Isso mostra que a instância do SQL Server está ouvindo na porta correta com o alias correto.</span><span class="sxs-lookup"><span data-stu-id="61ed2-200">This shows that the SQL Server instance is listening on the correct port with the correct alias.</span></span> <span data-ttu-id="61ed2-201">Se houver problemas para se conectar ao banco de dados do SQL Server, o Telnet mostrará um erro informando que a conexão não pode ser feita.</span><span class="sxs-lookup"><span data-stu-id="61ed2-201">If there’s a problem connecting to the SQL Server database, then telnet shows an error that the connection cannot be made.</span></span> <span data-ttu-id="61ed2-202">Agora que você verificou a conectividade do banco de dados no servidor de banco de dados, é possível fazer a mesma coisa no Lync Server (na rede) e verificar se não há firewalls bloqueando o acesso ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="61ed2-202">Now that you have checked database connectivity on the database server, you can do the same thing from Lync Server (over the network) and make sure there aren’t any firewalls blocking access along the way.</span></span>

</div>

<div>

## <a name="conclusion"></a><span data-ttu-id="61ed2-203">Conclusão</span><span class="sxs-lookup"><span data-stu-id="61ed2-203">Conclusion</span></span>

<span data-ttu-id="61ed2-204">Após a configuração do alias do SQL Server, você pode usá-lo para criar uma topologia do Lync Server 2013 na ferramenta Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="61ed2-204">Once the SQL Server alias has been configured, you can use it to create a Lync Server 2013 topology in the Topology Builder tool.</span></span> <span data-ttu-id="61ed2-205">Para obter mais informações sobre topologias, consulte [definindo e configurando a topologia no Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="61ed2-205">For more information about topologies, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="61ed2-206">Confira também</span><span class="sxs-lookup"><span data-stu-id="61ed2-206">See Also</span></span>


<span data-ttu-id="61ed2-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md)  
 [Planejando a segurança no Lync Server 2013](lync-server-2013-planning-for-security.md)</span><span class="sxs-lookup"><span data-stu-id="61ed2-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md) 
[Planning for security in Lync Server 2013](lync-server-2013-planning-for-security.md)</span></span>  
[<span data-ttu-id="61ed2-208">Definindo e configurando a topologia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61ed2-208">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)  
[<span data-ttu-id="61ed2-209">Implantando o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61ed2-209">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="61ed2-210"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61ed2-210"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

