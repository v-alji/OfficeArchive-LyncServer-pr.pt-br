---
title: 'Lync Server 2013: usando o Microsoft SQL Server 2008 R2 como seu banco de dados do System Center Operations Manager'
description: 'Lync Server 2013: usando o Microsoft SQL Server 2008 R2 como seu banco de dados do System Center Operations Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database
ms:assetid: 0efe76da-8854-499e-bdc7-3623244a8e85
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687969(v=OCS.15)
ms:contentKeyID: 49733555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 870c079e7e5e871fc62358e9bdd21653193fad7c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390199"
---
# <a name="using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database-for-lync-server-2013"></a><span data-ttu-id="87135-103">Usar o Microsoft SQL Server 2008 R2 como seu banco de dados do System Center Operations Manager para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87135-103">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87135-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87135-104">

<span> </span></span></span>

<span data-ttu-id="87135-105">_**Tópico da última modificação:** 2013-07-29_</span><span class="sxs-lookup"><span data-stu-id="87135-105">_**Topic Last Modified:** 2013-07-29_</span></span>

<span data-ttu-id="87135-106">Para usar o SQL Server 2008 R2 como seu banco de dados back-end, conclua as etapas detalhadas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="87135-106">To use SQL Server 2008 R2 as your back-end database, complete the steps detailed in this topic.</span></span>

<div>

## <a name="configuring-sql-server-2008-r2-and-sql-server-reporting-services"></a><span data-ttu-id="87135-107">Configuração do SQL Server 2008 R2 e do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="87135-107">Configuring SQL Server 2008 R2 and SQL Server Reporting Services</span></span>

<span data-ttu-id="87135-108">Antes de começar a instalar o System Center Operations Manager, você deve fazer duas alterações no SQL Server 2008 R2 e na configuração do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="87135-108">Before you begin installing System Center Operations Manager you must make two changes to your SQL Server 2008 R2 and your SQL Server Reporting Services configuration.</span></span> <span data-ttu-id="87135-109">(Essas alterações só serão necessárias se você estiver usando o SQL Server 2008 R2 como seu banco de dados do Operations Manager.) Primeiro, faça o seguinte no computador que hospedará seu banco de dados do Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="87135-109">(These changes are required only if you are using SQL Server 2008 R2 as your Operations Manager database.) First, do the following on the computer that will host your Operations Manager database:</span></span>

1.  <span data-ttu-id="87135-110">Clique em **Iniciar** e em **executar**.</span><span class="sxs-lookup"><span data-stu-id="87135-110">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="87135-111">Na caixa de diálogo **executar** , digite **C: \\ Program Files \\ Microsoft SQL Server \\ MSRS10 \_ 50. ARCHINST \\ Reporting Services \\ ReportServer** e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="87135-111">In the **Run** dialog box, type **C:\\Program Files\\Microsoft SQL Server\\ MSRS10\_50.ARCHINST\\Reporting Services\\ReportServer** and then press ENTER.</span></span>

3.  <span data-ttu-id="87135-112">Na pasta **ReportServer** , abra o arquivo **rsreportserver.config** no bloco de notas ou em qualquer outro editor de texto.</span><span class="sxs-lookup"><span data-stu-id="87135-112">In the **ReportServer** folder, open the file **rsreportserver.config** in Notepad or any other text editor.</span></span>

4.  <span data-ttu-id="87135-113">Próximo ao início do arquivo, você verá uma série de nós "Adicionar chave".</span><span class="sxs-lookup"><span data-stu-id="87135-113">Near the beginning of the file you will see a series of "Add Key" nodes.</span></span> <span data-ttu-id="87135-114">Localize a entrada que começa a **\< Adicionar Key = "SecureConnectionLevel"** e defina o valor como **0**:</span><span class="sxs-lookup"><span data-stu-id="87135-114">Find the entry that begins **\<Add Key="SecureConnectionLevel"** and set the value to **0**:</span></span>
    
        <Add Key="SecureConnectionLevel" Value="0"/>

5.  <span data-ttu-id="87135-115">Salve o arquivo **rsreportserver.config** e, em seguida, feche o editor de texto.</span><span class="sxs-lookup"><span data-stu-id="87135-115">Save the file **rsreportserver.config** and then close your text editor.</span></span>

<span data-ttu-id="87135-116">Após atualizar o arquivo de configuração do Report Server, você deve atribuir o certificado correto ao SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="87135-116">After updating the Report Server configuration file you must then assign the correct certificate to SQL Server Reporting Services.</span></span> <span data-ttu-id="87135-117">Para fazer isso:</span><span class="sxs-lookup"><span data-stu-id="87135-117">To do that:</span></span>

1.  <span data-ttu-id="87135-118">Clique em **Iniciar**, **em todos os programas**, em **Microsoft SQL Server 2008 R2**, em **ferramentas de configuração** e em Gerenciador de configuração do **Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="87135-118">Click **Start**, click **All Programs**, click **Microsoft SQL Server 2008 R2**, click **Configuration Tools**, and then click **Reporting Services Configuration Manager**.</span></span>

2.  <span data-ttu-id="87135-119">Na caixa de diálogo **conexão de configuração do Reporting Services** , verifique se o nome do seu servidor é exibido na caixa **nome do servidor** .</span><span class="sxs-lookup"><span data-stu-id="87135-119">In the **Reporting Services Configuration Connection** dialog box, make sure that the name of your server appears in the **Server Name** box.</span></span> <span data-ttu-id="87135-120">Selecione a instância do SQL Server que hospedará seu banco de dados do Operations Manager (por exemplo, **ARCHINST**) na lista suspensa de **instâncias do servidor de relatório** e clique em **conectar**.</span><span class="sxs-lookup"><span data-stu-id="87135-120">Select the SQL Server instance that will host your Operations Manager database (for example, **ARCHINST**) from the **Report Server Instance** drop-down list and then click **Connect**.</span></span>

3.  <span data-ttu-id="87135-121">No Gerenciador de configuração do Reporting Services, clique em **URL do serviço Web**.</span><span class="sxs-lookup"><span data-stu-id="87135-121">In Reporting Services Configuration Manager, click **Web Service URL**.</span></span>

4.  <span data-ttu-id="87135-122">Na página **Web Service URL** , selecione o certificado a ser usado para o Reporting Services da lista suspensa **certificado SSL** e clique em **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="87135-122">On the **Web Service URL** page, select the certificate to be used for your Reporting Services from the **SSL Certificate** dropdown list and then click **Apply**.</span></span> <span data-ttu-id="87135-123">Após alguns segundos, você verá um par de URLs listadas nas **URLs do serviço Web do Report Server**.</span><span class="sxs-lookup"><span data-stu-id="87135-123">After a few seconds, you will see a pair of URLs listed under **Report Server Web Service URLs**.</span></span>

5.  <span data-ttu-id="87135-124">Clique em ambas as URLs para verificar se você pode acessar o SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="87135-124">Click both of the URLs to verify that you can access SQL Server Reporting Services.</span></span>

6.  <span data-ttu-id="87135-125">Feche o Gerenciador de configuração do Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="87135-125">Close Reporting Services Configuration Manager.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-database-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="87135-126">Criando um banco de dados do System Center Operations Manager para uso com o SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="87135-126">Creating a System Center Operations Manager database for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="87135-127">Se você quiser configurar o System Center Operations Manager para usar um banco de dados do SQL Server 2008 R2, será necessário "manualmente" criar o banco de dados do Operations Manager no computador que executa o SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="87135-127">If you want to configure System Center Operations Manager to use a SQL Server 2008 R2 database, you will need to "manually" create the Operations Manager database on the computer running SQL Server 2008 R2.</span></span> <span data-ttu-id="87135-128">(Novamente, essas etapas não serão necessárias se você estiver usando o SQL Server 2005 ou o SQL Server 2008 como seu banco de dados back-end.)</span><span class="sxs-lookup"><span data-stu-id="87135-128">(Again, these steps are not required if you are using SQL Server 2005 or SQL Server 2008 as your back-end database.)</span></span>

<span data-ttu-id="87135-129">Para criar manualmente um banco de dados do Operations Manager, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="87135-129">To manually create an Operations Manager database do the following:</span></span>

1.  <span data-ttu-id="87135-130">Na mídia de instalação do System Center Operations Manager 2007 R2, na \\ pasta SupportTools AMD64, clique duas vezes em **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="87135-130">On the System Center Operations Manager 2007 R2 setup media, in the SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="87135-131">No assistente de configuração de banco de dados, na página **Bem-vindo ao assistente de configuração de banco de dados** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-131">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="87135-132">Na página **informações do banco de dados** saia de todas as configurações e clique em **Avançar** .</span><span class="sxs-lookup"><span data-stu-id="87135-132">On the **Database Information** page leave all the settings as-is and then click **Next**</span></span>

4.  <span data-ttu-id="87135-133">Na página **configuração do grupo de gerenciamento** digite um nome para o seu grupo de gerenciamento (por exemplo, **monitoração do Lync Server**) na caixa **nome do grupo de gerenciamento** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-133">On the **Management Group Configuration** page type a name for your Management Group (for example, **Lync Server Monitoring**) in the **Management Group name** box and then click **Next**.</span></span>

5.  <span data-ttu-id="87135-134">Na página **relatórios de erros do Operations Manager** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-134">On the **Operations Manager Error Reports** page click **Next**.</span></span>

6.  <span data-ttu-id="87135-135">Na página **Resumo** , clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="87135-135">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-data-warehouse-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="87135-136">Criando um data warehouse do System Center Operations Manager para uso com o SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="87135-136">Creating a System Center Operations Manager data warehouse for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="87135-137">O Microsoft Lync Server 2013 vem com três novos relatórios do System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="87135-137">Microsoft Lync Server 2013 ships with three new System Center Operations Manager reports:</span></span>

  - <span data-ttu-id="87135-138">**Relatório de disponibilidade de cenário de ponta a ponta**   Esse relatório detalha a disponibilidade/tempo de atividade para os principais serviços do Lync Server, como registro ou presença.</span><span class="sxs-lookup"><span data-stu-id="87135-138">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="87135-139">**Relatório de capacidade**   Usando informações de contador de desempenho, esse relatório mostra tendências para componentes do sistema, como disponibilidade da memória e uso do processador.</span><span class="sxs-lookup"><span data-stu-id="87135-139">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="87135-140">**Relatório de componente**   Esse relatório lista os principais geradores de alertas agrupados pelo componente do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="87135-140">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="87135-141">Para usar esses novos relatórios, você deve instalar um data warehouse do System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="87135-141">In order to use these new reports you must install a System Center Operations Manager data warehouse.</span></span> <span data-ttu-id="87135-142">(Um depósito de dados permite armazenamento de longo prazo de dados de operações.) Para usar um data warehouse com o SQL Server 2008 R2, você deve executar as seguintes etapas no computador que hospeda seu banco de dados do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="87135-142">(A data warehouse provides for long-term storage of operations data.) To use a data warehouse with SQL Server 2008 R2 you must carry out the following steps on the computer that hosts your SQL Server database:</span></span>

1.  <span data-ttu-id="87135-143">Na mídia de instalação do System Center Operations Manager, na \\ pasta Setup SupportTools \\ AMD64, clique duas vezes em **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="87135-143">On the System Center Operations Manager setup media, in the Setup\\SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="87135-144">No assistente de configuração de banco de dados, na página **Bem-vindo ao assistente de configuração de banco de dados** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-144">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="87135-145">Na página **informações do banco** de dados, selecione o **banco de dados de data warehouse do Operations Manager** na lista suspensa **tipo de banco** de dados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-145">On the **Database Information** page, select **Operations Manager Data Warehouse Database** from the **Database Type** dropdown list and then click **Next**.</span></span>

4.  <span data-ttu-id="87135-146">Na página **Resumo** , clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="87135-146">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="installing-the-system-center-operations-manager-console"></a><span data-ttu-id="87135-147">Instalando o console do System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="87135-147">Installing the System Center Operations Manager console</span></span>

<span data-ttu-id="87135-148">O console do Operations Manager é a principal ferramenta usada para gerenciar o System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="87135-148">The Operations Manager console is the primary tool used to manage System Center Operations Manager.</span></span> <span data-ttu-id="87135-149">Antes de instalar o console do Operations Manager, verifique se você instalou uma versão com suporte do SQL Server, juntamente com o serviço relatórios do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87135-149">Before you install the Operations Manager console, make sure that you have installed a supported version of SQL Server along with the SQL Server Reporting Service.</span></span> <span data-ttu-id="87135-150">Também é recomendável que você execute o Gerenciador de configuração do Reporting Services do SQL Server para verificar se o serviço de relatório foi instalado e configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="87135-150">It is also recommended that you run SQL Server's Reporting Services Configuration Manager to verify that the Reporting Service has been correctly installed and configured.</span></span>

<span data-ttu-id="87135-151">Para instalar o console do System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="87135-151">To install the System Center Operations Manager console:</span></span>

1.  <span data-ttu-id="87135-152">Na mídia de instalação do System Center Operations Manager, clique duas vezes em **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="87135-152">On the System Center Operations Manager setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="87135-153">Na configuração do System Center Operations Manager 2007 R2, clique em **verificar pré-requisitos**.</span><span class="sxs-lookup"><span data-stu-id="87135-153">In System Center Operations Manager 2007 R2 Setup, click **Check Prerequisites**.</span></span>

3.  <span data-ttu-id="87135-154">No Visualizador de pré-requisitos do System Center Operations Manager, selecione os componentes do System Center a serem instalados: (**servidor**; **Console**; e do **PowerShell**) e clique em **verificar**.</span><span class="sxs-lookup"><span data-stu-id="87135-154">In the System Center Operations Manager Prerequisite Viewer, select the System Center components to be installed: (**Server**; **Console**; and **PowerShell**) and then click **Check**.</span></span> <span data-ttu-id="87135-155">Verifique se não foram relatados problemas de bloqueio e clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="87135-155">Verify that no blocking issues have been reported and then click **Close**.</span></span> <span data-ttu-id="87135-156">Se um problema de bloqueio tiver sido reportado, corrija o problema e clique em **verificar** para executar novamente o teste de pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="87135-156">If a blocking issue has been reported, correct the problem and then click **Check** to re-run the prerequisite testing.</span></span>

4.  <span data-ttu-id="87135-157">Na instalação do System Center Operations Manager, clique em **instalar Gerenciador de operações**.</span><span class="sxs-lookup"><span data-stu-id="87135-157">In System Center Operations Manager Setup, click **Install Operations Manager**.</span></span>

5.  <span data-ttu-id="87135-158">No assistente de configuração do System Center Operations Manager, na página **Bem-vindo ao assistente de configuração do System Center Operations Manager** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-158">In the System Center Operations Manager Setup wizard, on the **Welcome to the System Center Operations Manager Setup Wizard** page, click **Next**.</span></span>

6.  <span data-ttu-id="87135-159">Na página de **contrato de licença de usuário final** , selecione **aceito os termos do contrato de licença** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-159">On the **End-User License Agreement** page, select **I accept the terms in the license agreement** and then click **Next**.</span></span>

7.  <span data-ttu-id="87135-160">Na página **registro de produto** , digite seu nome na caixa **nome de usuário** e o nome da sua organização na caixa **organização** .</span><span class="sxs-lookup"><span data-stu-id="87135-160">On the **Product Registration** page, type your name in the **User Name** box and name of your organization in the **Organization** box.</span></span> <span data-ttu-id="87135-161">Digite a chave do produto (Product Key) do System Center Operations Manager na caixa **digite a chave do CD de 25 dígitos** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-161">Type your System Center Operations Manager product key in the **Enter your 25 digit CD Key** box and then click **Next**.</span></span>

8.  <span data-ttu-id="87135-162">Na página **configuração personalizada** , selecione as opções do System Center a serem instaladas e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-162">On the **Custom Setup** page select the System Center options to be installed and then click **Next**.</span></span> <span data-ttu-id="87135-163">Você deve selecionar **servidor de gerenciamento**, **interfaces do usuário** e **console Web** para ser instalado.</span><span class="sxs-lookup"><span data-stu-id="87135-163">You should select **Management Server**, **User Interfaces**, and **Web Console** to be installed.</span></span> <span data-ttu-id="87135-164">O **banco de dados** não deve ser selecionado e não deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="87135-164">**Database** should not be selected and should not be installed.</span></span>

9.  <span data-ttu-id="87135-165">Na página **instância do servidor de banco de dados SC** , verifique se o nome do computador em que os bancos de dados do Operations Manager estão instalados aparece na caixa **servidor de banco de dados do System Center** .</span><span class="sxs-lookup"><span data-stu-id="87135-165">On the **SC Database Server Instance** page, verify that the name of the computer where the Operations Manager databases are installed appears in the **System Center Database Server** box.</span></span> <span data-ttu-id="87135-166">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="87135-166">Click **Next**.</span></span>

10. <span data-ttu-id="87135-167">Na página da **conta de ação do servidor de gerenciamento** , selecione conta de **domínio ou computador local** e, em seguida, insira os valores apropriados nas caixas conta de **usuário**, **senha** e **domínio ou computador local** .</span><span class="sxs-lookup"><span data-stu-id="87135-167">On the **Management Server Action Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="87135-168">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="87135-168">Click **Next**.</span></span>

11. <span data-ttu-id="87135-169">Na página **da conta do serviço SDK e config** , selecione **conta de domínio ou computador local** e, em seguida, insira os valores apropriados nas caixas **conta de usuário**, **senha** e **domínio ou computador local** .</span><span class="sxs-lookup"><span data-stu-id="87135-169">On the **SDK and Config Service Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="87135-170">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="87135-170">Click **Next**.</span></span>

12. <span data-ttu-id="87135-171">Na página **relatórios de erros do Operations Manager** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-171">On the **Operations Manager Error Reports** page click **Next**.</span></span>

13. <span data-ttu-id="87135-172">Na página do **programa de aperfeiçoamento da experiência do usuário** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-172">On the **Customer Experience Improvement Program** page click **Next**.</span></span>

14. <span data-ttu-id="87135-173">Na página **pronto para instalar o programa** , clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="87135-173">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="87135-174">Na página **concluindo a configuração do Gerenciador de operações do System Center** , desmarque a **chave de criptografia de backup** e **inicie as caixas de seleção do console** e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="87135-174">On the **Completing the System Center Operations Manager Setup** page, clear the **Backup Encryption Key** and **Start the console checkboxes** and then click **Finish**.</span></span>

16. <span data-ttu-id="87135-175">Na configuração do System Center Operations Manager, clique em **sair**.</span><span class="sxs-lookup"><span data-stu-id="87135-175">In System Center Operations Manager Setup click **Exit**.</span></span>

</div>

<div>

## <a name="installing-system-center-reporting-services"></a><span data-ttu-id="87135-176">Instalar o System Center Reporting Services</span><span class="sxs-lookup"><span data-stu-id="87135-176">Installing System Center Reporting Services</span></span>

<span data-ttu-id="87135-177">Depois de instalar e configurar o console System Center Operations Manager, você deve instalar o System Center Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="87135-177">After installing and configuring the System Center Operations Manager console you must then install System Center Reporting Services.</span></span> <span data-ttu-id="87135-178">Se você estiver usando o SQL Server 2008 R2 como o banco de dados back-end do Operations Manager, isso significa que você deve primeiro fazer uma alteração temporária no grupo de segurança associado ao SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="87135-178">If you are using SQL Server 2008 R2 as your Operations Manager back-end database, that means that you must first make a temporary change to the security group associated with SQL Server Reporting Services.</span></span> <span data-ttu-id="87135-179">Se estiver usando o SQL Server 2008 R2, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="87135-179">If you are using SQL Server 2008 R2, you must do the following:</span></span>

1.  <span data-ttu-id="87135-180">Clique em **Iniciar**, aponte para **Ferramentas administrativas** e clique em **Gerenciador de servidores**.</span><span class="sxs-lookup"><span data-stu-id="87135-180">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="87135-181">No Gerenciador de servidores, expanda **configuração**, expanda **usuários e grupos locais** e clique em **grupos**.</span><span class="sxs-lookup"><span data-stu-id="87135-181">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="87135-182">Localize o seguinte grupo, em que ATL-SC-001 representa o nome do seu computador e ARCHINST representa a instância do SQL Server para o banco de dados do System Center: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="87135-182">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the System Center database: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

4.  <span data-ttu-id="87135-183">Clique com o botão direito do mouse no grupo e clique em **renomear**.</span><span class="sxs-lookup"><span data-stu-id="87135-183">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="87135-184">Renomeie o grupo excluindo **\_ 50** do nome do grupo.</span><span class="sxs-lookup"><span data-stu-id="87135-184">Rename the group by deleting **\_50** from the group name.</span></span> <span data-ttu-id="87135-185">Por exemplo: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="87135-185">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

5.  <span data-ttu-id="87135-186">Feche o Gerenciador de servidores.</span><span class="sxs-lookup"><span data-stu-id="87135-186">Close Server Manager.</span></span>

<span data-ttu-id="87135-187">Nesse ponto, você está pronto para instalar o System Center Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="87135-187">At this point you are ready to install System Center Reporting Services.</span></span> <span data-ttu-id="87135-188">Para fazer isso:</span><span class="sxs-lookup"><span data-stu-id="87135-188">To do this:</span></span>

1.  <span data-ttu-id="87135-189">Na mídia de instalação do System Center Operations Manager 2007 R2, clique duas vezes em **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="87135-189">On the System Center Operations Manager 2007 R2 Setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="87135-190">Na instalação do System Center Operations Manager 2007 R2, clique em **instalar relatório do Operations Manager**.</span><span class="sxs-lookup"><span data-stu-id="87135-190">In System Center Operations Manager 2007 R2 Setup, click **Install Operations Manager Reporting**.</span></span>

3.  <span data-ttu-id="87135-191">No assistente de configuração de relatórios do System Center Operations Manager 2007 R2, na página **Bem-vindo à configuração de relatórios do Operations Manager** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-191">In the System Center Operations Manager 2007 R2 Reporting Setup wizard, on the **Welcome to Operations Manager Reporting Setup** page, click **Next**.</span></span>

4.  <span data-ttu-id="87135-192">Na página de **contrato de licença de usuário final** , selecione **aceito os termos do contrato de licença** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-192">On the **End-user License Agreement** page select **I accept the terms of the license agreement** and then click **Next**.</span></span>

5.  <span data-ttu-id="87135-193">Na página **registro de produtos** , certifique-se de que seu nome e o nome de sua organização sejam exibidos nas caixas **nome de usuário** e **organização** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-193">On the **Product Registration** page, ensure that your name and the name of your organization appear in the **User Name** and **Organization** boxes and then click **Next**.</span></span>

6.  <span data-ttu-id="87135-194">Na página **configuração personalizada** , clique em **servidor de relatório** e selecione **esse componente, e todos os componentes dependentes serão instalados na unidade de disco local**.</span><span class="sxs-lookup"><span data-stu-id="87135-194">On the **Custom Setup** page, click **Reporting Server** and select **This component, and all dependent components, will be installed on local disk drive**.</span></span> <span data-ttu-id="87135-195">Clique em **data warehouse** e selecione **este componente não estará disponível** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-195">Click **Data Warehouse** and select **This component will not be available**, and then click **Next**.</span></span>

7.  <span data-ttu-id="87135-196">Na página **conectar-se ao servidor de gerenciamento raiz** , digite o nome do servidor de gerenciamento raiz do Operations Manager na caixa **servidor de gerenciamento raiz** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-196">On the **Connect to the Root Management Server** page, type the name of your Operations Manager root management server in the **Root Management Server** box and then click **Next**.</span></span>

8.  <span data-ttu-id="87135-197">Na página **conectar-se ao data warehouse do Operations Manager** , digite a instância do SQL Server na qual o data warehouse está localizado na caixa **instância do SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="87135-197">On the **Connect to the Operations Manager Data Warehouse** page, type the SQL Server instance where your data warehouse is located in the **SQL Server Instance** box.</span></span> <span data-ttu-id="87135-198">(Se o seu data warehouse estiver localizado na instância padrão, basta digitar o nome do servidor; por exemplo: ATL-SQL-001.) Verifique se o nome do banco de dados **OperationsManagerDW** aparece na caixa de **nome** e se a porta **1433** é exibida na caixa de **porta do SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="87135-198">(If your data warehouse is located in the Default instance then simply type the server name; for example: atl-sql-001.) Verify that the database name **OperationsManagerDW** appears in the **Name** box, and that port **1433** appears in the **SQL Server port** box.</span></span> <span data-ttu-id="87135-199">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="87135-199">Click **Next**.</span></span>

9.  <span data-ttu-id="87135-200">Na página **instância de relatórios do SQL Server** , selecione o servidor de relatórios do SQL Server na lista suspensa **digite o servidor do SQL Server Reporting Services** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-200">On the **SQL Server Reporting Instance** page, select your SQL Server reporting server from the **Enter the SQL Server Reporting Services Server** dropdown list and then click **Next**.</span></span>

10. <span data-ttu-id="87135-201">Na página de **gravação da conta de data warehouse** , insira o nome e a senha do usuário para receber as permissões de gravação inicialmente atribuídas ao depósito de dados nas caixas **conta de usuário** e **senha** .</span><span class="sxs-lookup"><span data-stu-id="87135-201">On the **Data Warehouse Write Account** page, enter the name and password of the user to be initially assigned write permissions to the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="87135-202">Selecione o domínio do usuário na lista suspensa **domínio** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-202">Select the user's domain from the **Domain** dropdown list and then click **Next**.</span></span>

11. <span data-ttu-id="87135-203">Na página **conta do leitor de dados** , insira o nome e a senha da conta de usuário a ser usada quando o SQL Reporting Services consulta o armazém de dados nas caixas **conta do usuário** e **senha** .</span><span class="sxs-lookup"><span data-stu-id="87135-203">On the **Data Reader Account** page, enter the name and password of the user account to be used when SQL Reporting Services queries the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="87135-204">Selecione o domínio de conta na lista suspensa **domínio** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-204">Select the account domain from the **Domain** dropdown list and then click **Next**.</span></span>

12. <span data-ttu-id="87135-205">Na página **relatórios de dados operacionais** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-205">On the **Operational Data Reports** page, click **Next**.</span></span>

13. <span data-ttu-id="87135-206">Na página **Microsoft Update** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="87135-206">On the **Microsoft Update** page, click **Next**.</span></span>

14. <span data-ttu-id="87135-207">Na página **pronto para instalar o programa** , clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="87135-207">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="87135-208">Na página **concluindo o assistente de configuração dos componentes de relatório do Operations Manager** , clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="87135-208">On the **Completing the Operations Manager Reporting Components Setup Wizard** page, click **Finish**.</span></span>

16. <span data-ttu-id="87135-209">Na instalação do System Center Operations Manager 2007 R2, clique em **sair**.</span><span class="sxs-lookup"><span data-stu-id="87135-209">In System Center Operations Manager 2007 R2 Setup, click **Exit**.</span></span>

<span data-ttu-id="87135-210">Após a instalação do relatório do System Center, use o procedimento a seguir para redefinir o nome do grupo de segurança associado ao relatório do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87135-210">After System Center reporting has been installed you then use the following procedure to reset the name of the security group associated with SQL Server reporting.</span></span> <span data-ttu-id="87135-211">Novamente, esse procedimento só será necessário se você estiver usando o SQL Server:</span><span class="sxs-lookup"><span data-stu-id="87135-211">Again, this procedure is only required if you are using SQL Server:</span></span>

1.  <span data-ttu-id="87135-212">Clique em **Iniciar**, aponte para **Ferramentas administrativas** e clique em **Gerenciador de servidores**.</span><span class="sxs-lookup"><span data-stu-id="87135-212">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="87135-213">No Gerenciador de servidores, expanda **configuração**, expanda **usuários e grupos locais** e clique em **grupos**.</span><span class="sxs-lookup"><span data-stu-id="87135-213">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="87135-214">Localize o seguinte grupo, em que ATL-SC-001 representa o nome do seu computador e ARCHINST representa a instância do SQL Server para os bancos de dados de arquivamento e monitoramento: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="87135-214">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the archiving and monitoring databases: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

4.  <span data-ttu-id="87135-215">Clique com o botão direito do mouse no grupo e clique em **renomear**.</span><span class="sxs-lookup"><span data-stu-id="87135-215">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="87135-216">Renomeie o grupo adicionando **\_ 50** ao final do nome do grupo, logo antes do nome da instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87135-216">Rename the group by adding **\_50** to the end of the group name, right before the SQL Server instance name.</span></span> <span data-ttu-id="87135-217">Por exemplo: **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="87135-217">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

5.  <span data-ttu-id="87135-218">Feche o Gerenciador de servidores.</span><span class="sxs-lookup"><span data-stu-id="87135-218">Close Server Manager.</span></span>

<span data-ttu-id="87135-219">Se o console de operações do System Center estiver aberto, será necessário fechar o aplicativo e reiniciá-lo; Se você não fizer isso, a guia **relatório** não será exibida na interface do usuário do console de operações.</span><span class="sxs-lookup"><span data-stu-id="87135-219">If the System Center Operations Console is open you will need to close the application and then restart it; if you do not do this the **Reporting** tab will not appear in the Operations Console user interface.</span></span> <span data-ttu-id="87135-220">Observe que depois de reiniciar o console de operações pela primeira vez, pode demorar vários minutos antes de todos os relatórios de monitoramento serem exibidos na guia **relatório** .</span><span class="sxs-lookup"><span data-stu-id="87135-220">Note that, after restarting the Operations Console the first time, it could take several minutes before all the Monitoring Reports appear on the **Reporting** tab.</span></span>

<span data-ttu-id="87135-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87135-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

