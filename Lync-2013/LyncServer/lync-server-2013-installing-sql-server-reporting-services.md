---
title: 'Lync Server 2013: Instalando o SQL Server Reporting Services'
description: 'Lync Server 2013: Instalando o SQL Server Reporting Services.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing SQL Server Reporting Services
ms:assetid: 638a1d0c-1ac7-4735-83f2-4df3d03c7cf9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204957(v=OCS.15)
ms:contentKeyID: 48184345
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 70da5e3845d18057b3362fa39953dee6cdc3d9f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427009"
---
# <a name="installing-sql-server-reporting-services-in-lync-server-2013"></a><span data-ttu-id="13a79-103">Instalando o SQL Server Reporting Services no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13a79-103">Installing SQL Server Reporting Services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13a79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13a79-104">

<span> </span></span></span>

<span data-ttu-id="13a79-105">_**Tópico da última modificação:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="13a79-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="13a79-106">Se você pretende usar os relatórios de monitoramento do Microsoft Lync Server 2013 (consulte a próxima seção desta documentação para obter mais informações), primeiro é necessário instalar o SQL Server Reporting Services; O Reporting Services pode ser instalado ao mesmo tempo em que você instala o Microsoft SQL Server ou a qualquer momento após a instalação do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="13a79-106">If you intend to use Microsoft Lync Server 2013 Monitoring Reports (see the next section of this documentation for more information) you must first install SQL Server Reporting Services; Reporting Services can be installed at the same time you install Microsoft SQL Server or any time after SQL Server has been installed.</span></span> <span data-ttu-id="13a79-107">Se você não instalou o SQL Server, siga as instruções fornecidas anteriormente nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="13a79-107">If you have not installed SQL Server, then follow the instructions provided earlier in this documentation.</span></span> <span data-ttu-id="13a79-108">Ao instalar o SQL Server, certifique-se de que, na página seleção de recursos, selecione Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="13a79-108">When installing SQL Server, make sure that, on the Feature Selection page, you select Reporting Services.</span></span> <span data-ttu-id="13a79-109">Isso vai instalar o SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="13a79-109">That will install SQL Server Reporting Services.</span></span>

<span data-ttu-id="13a79-110">Se você já instalou o SQL Server, mas não instalou o SQL Server Reporting Services, é possível adicionar esse recurso seguindo o conjunto de instruções apropriado para SQL Server 2008 R2 ou SQL Server 2012, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="13a79-110">If you have already installed SQL Server but did not install SQL Server Reporting Services you can add that feature by following the appropriate set of instructions for SQL Server 2008 R2 or SQL Server 2012, as appropriate.</span></span>

<span data-ttu-id="13a79-111">Para verificar se os serviços de relatório foram instalados com êxito, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="13a79-111">To verify that the reporting Services have been successfully installed, complete the following steps:</span></span>

1.  <span data-ttu-id="13a79-112">Se você estiver executando o Microsoft SQL Server 2008 R2, clique em **Iniciar**, clique em **todos os programas**, clique em **Microsoft SQL Server 2008 R2**, em **ferramentas de configuração** e em Gerenciador de configuração do **Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="13a79-112">If you are running Microsoft SQL Server 2008 R2, then click **Start**, click **All Programs**, click **Microsoft SQL Server 2008 R2**, click **Configuration Tools**, and then click **Reporting Services Configuration Manager**.</span></span>
    
    <span data-ttu-id="13a79-113">Se você estiver executando o Microsoft SQL Server 2012, clique em **Iniciar**, clique em **todos os programas**, clique em **Microsoft SQL Server 2012**, em **ferramentas de configuração** e em Gerenciador de configuração do **Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="13a79-113">If you are running Microsoft SQL Server 2012, then click **Start**, click **All Programs**, click **Microsoft SQL Server 2012**, click **Configuration Tools**, and then click **Reporting Services Configuration Manager**.</span></span>

2.  <span data-ttu-id="13a79-114">Na caixa de diálogo **conexão de configuração do Reporting Services** , verifique se o nome do seu servidor é exibido na caixa **nome do servidor** e se o nome da instância do SQL Server que armazena os dados de monitoramento aparece na caixa de instância do **servidor de relatório** .</span><span class="sxs-lookup"><span data-stu-id="13a79-114">In the **Reporting Services Configuration Connection** dialog box, verify that the name of your server appears in the **Server Name** box and that the name of the SQL Server instance that stores your monitoring data appears in the **Report Server Instance** box.</span></span> <span data-ttu-id="13a79-115">Clique em **conectar**.</span><span class="sxs-lookup"><span data-stu-id="13a79-115">Click **Connect**.</span></span>

<span data-ttu-id="13a79-116">No Gerenciador de configuração do Reporting Services, o painel de status do servidor de relatório deve mostrar que o SQL Server Reporting Services foi instalado e que o Reporting Services está em execução: o status do servidor de relatório deve ser mostrado como **iniciado** e o botão **Iniciar** deve estar esmaecido e indisponível.</span><span class="sxs-lookup"><span data-stu-id="13a79-116">In the Reporting Service Configuration Manager, the Report Server Status pane should show that SQL Server Reporting Services has been installed and that the Reporting Services are currently running: the Report Server Status should be shown as **Started** and the **Start** button should be grayed-out and unavailable.</span></span> <span data-ttu-id="13a79-117">Se o serviço de relatório não estiver em execução, clique em **Iniciar** para iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="13a79-117">If the Reporting Service is not running, click **Start** in order to start the service.</span></span>

<span data-ttu-id="13a79-118">Se nenhum banco de dados estiver listado ao lado do rótulo de nome do banco de dados do servidor de relatório, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="13a79-118">If no database is listed next to the Report Server Database Name label then do the following:</span></span>

1.  <span data-ttu-id="13a79-119">No Gerenciador de configuração do Reporting Services, clique em **banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="13a79-119">In the Reporting Services Configuration Manager click **Database**.</span></span>

2.  <span data-ttu-id="13a79-120">No painel banco de dados do servidor de relatório, clique em **alterar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="13a79-120">In the Report Server Database pane click **Change Database**.</span></span>

3.  <span data-ttu-id="13a79-121">No assistente de configuração do Report Server Database, no painel Ação, selecione **criar um novo banco de dados do servidor de relatório** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a79-121">In the Report Server Database Configuration wizard, in the Action pane, select **Create a new report server database** and then click **Next**.</span></span>

4.  <span data-ttu-id="13a79-122">No assistente de configuração do Report Server Database, no painel servidor de banco de dados, verifique se as informações listadas nas caixas **nome do servidor**, **tipo de autenticação** e nome de **usuário** estão corretas.</span><span class="sxs-lookup"><span data-stu-id="13a79-122">In the Report Server Database Configuration wizard, in the Database Server pane, verify that the information listed in the **Server Name**, **Authentication Type**, and **Username** boxes is correct.</span></span> <span data-ttu-id="13a79-123">Clique em **testar conexão** para verificar se uma conexão pode ser feita com o servidor de banco de dados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a79-123">Click **Test Connection** to verify that a connection can be made to the database server and then click **Next**.</span></span>

5.  <span data-ttu-id="13a79-124">No assistente de configuração do Report Server Database, no painel banco de dados, aceite os valores padrão para o **nome do banco de dados**, o **idioma** e o **modo servidor de relatório** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a79-124">In the Report Server Database Configuration wizard, in the Database pane, accept the default values for **Database Name**, **Language**, and **Report Server Mode** and then click **Next**.</span></span>

6.  <span data-ttu-id="13a79-125">No assistente de configuração do Report Server Database, no painel credenciais, verifique se as informações corretas estão listadas na lista suspensa **tipo de autenticação** e as caixas **nome de usuário** e **senha** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a79-125">In the Report Server Database Configuration wizard, in the Credentials pane, verify that the correct information is listed in the **Authentication Type** dropdown list and the **User name** and **Password** boxes, and then click **Next**.</span></span>

7.  <span data-ttu-id="13a79-126">No assistente de configuração do Report Server Database, no painel Resumo, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="13a79-126">In the Report Server Database Configuration wizard, in the Summary pane, click **Next**.</span></span>

8.  <span data-ttu-id="13a79-127">No assistente de configuração do Report Server Database, no painel progresso e concluir, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="13a79-127">In the Report Server Database Configuration wizard, in the Progress and Finish pane, click **Finish**.</span></span>

<span data-ttu-id="13a79-128">Para verificar se as URLs do serviço de relatório foram configuradas, clique em **URL do serviço Web**.</span><span class="sxs-lookup"><span data-stu-id="13a79-128">To verify that the Reporting Service URLs have been configured, click **Web Service URL**.</span></span> <span data-ttu-id="13a79-129">Você deve ver uma ou mais URLs listadas nas **URLs do serviço Web servidor do relatório** de título.</span><span class="sxs-lookup"><span data-stu-id="13a79-129">You should see one or more URLs listed under the heading **Report Server Web Service URLs**.</span></span> <span data-ttu-id="13a79-130">Clique em cada uma dessas URLs para verificar se você pode acessar a Home Page para a instalação local do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="13a79-130">Click each of these URLs to verify that you can reach the home page for the local installation of SQL Server Reporting Services.</span></span>

<span data-ttu-id="13a79-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13a79-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

