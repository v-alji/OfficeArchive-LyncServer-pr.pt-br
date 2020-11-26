---
title: 'Lync Server 2013: estabelecendo um plano de backup e restauração'
description: 'Lync Server 2013: estabelecendo um plano de backup e restauração.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Establishing a backup and restoration plan
ms:assetid: 9f562ef1-3804-41e2-b3e4-d45b2e8c63c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202183(v=OCS.15)
ms:contentKeyID: 51541499
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06d93c713364bf6b5f230b255b68a2c1dfe1d04a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428458"
---
# <a name="establishing-a-backup-and-restoration-plan-for-lync-server-2013"></a><span data-ttu-id="39931-103">Como estabelecer um plano de backup e restauração para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39931-103">Establishing a backup and restoration plan for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39931-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39931-104">

<span> </span></span></span>

<span data-ttu-id="39931-105">_**Tópico da última modificação:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="39931-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="39931-106">A criação de um plano de backup e restauração envolve as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="39931-106">Creating a backup and restoration plan involves the following steps:</span></span>

  - <span data-ttu-id="39931-107">Desenvolvendo o plano.</span><span class="sxs-lookup"><span data-stu-id="39931-107">Developing the plan.</span></span>

  - <span data-ttu-id="39931-108">Implementação do plano.</span><span class="sxs-lookup"><span data-stu-id="39931-108">Implementing the plan.</span></span>

  - <span data-ttu-id="39931-109">Manutenção do plano.</span><span class="sxs-lookup"><span data-stu-id="39931-109">Maintaining the plan.</span></span>

<div>

## <a name="developing-a-backup-and-restoration-plan"></a><span data-ttu-id="39931-110">Desenvolvendo um plano de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="39931-110">Developing a Backup and Restoration Plan</span></span>

<span data-ttu-id="39931-111">Depois de desenvolver sua estratégia de backup e restauração para o Lync Server, use-a para documentar um plano detalhado de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="39931-111">After you develop your backup and restoration strategy for Lync Server, use it to document a detailed backup and restoration plan.</span></span> <span data-ttu-id="39931-112">Seu plano deve transmitir claramente as prioridades e os requisitos para fazer backup de dados e configurações.</span><span class="sxs-lookup"><span data-stu-id="39931-112">Your plan should clearly convey the priorities and requirements for backing up data and settings.</span></span> <span data-ttu-id="39931-113">Você pode usar as informações em [estabelecer uma estratégia de backup e restauração para o Lync server 2013](lync-server-2013-establishing-a-backup-and-restoration-strategy.md) e as planilhas nas [planilhas de backup e restauração do Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md) para facilitar a documentação da sua estratégia.</span><span class="sxs-lookup"><span data-stu-id="39931-113">You can use the information in [Establishing a backup and restoration strategy for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-strategy.md) and the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md) to facilitate the documentation of your strategy.</span></span> <span data-ttu-id="39931-114">Seu plano também deve conter critérios para decidir quando e como restaurar o serviço.</span><span class="sxs-lookup"><span data-stu-id="39931-114">Your plan should also contain criteria for deciding when and how to restore service.</span></span>

<span data-ttu-id="39931-115">Ao desenvolver seu plano, você precisa considerar e fazer uma conta do seguinte:</span><span class="sxs-lookup"><span data-stu-id="39931-115">As you develop your plan, you need to consider, and account for, the following:</span></span>

  - <span data-ttu-id="39931-116">Como você vai recuperar os servidores em um novo hardware.</span><span class="sxs-lookup"><span data-stu-id="39931-116">How you will recover servers on new hardware.</span></span>

  - <span data-ttu-id="39931-117">Como você recuperará os serviços que exigem uma ação na parte de várias áreas comerciais ou departamentos.</span><span class="sxs-lookup"><span data-stu-id="39931-117">How you will recover services that require action on the part of multiple business areas or departments.</span></span>

  - <span data-ttu-id="39931-118">Como você pode adquirir servidores sobressalentes rapidamente.</span><span class="sxs-lookup"><span data-stu-id="39931-118">How you can acquire spare servers quickly.</span></span>

  - <span data-ttu-id="39931-119">O tempo que leva para fazer a recuperação usando sua estratégia.</span><span class="sxs-lookup"><span data-stu-id="39931-119">The time it takes to recover by using your strategy.</span></span> <span data-ttu-id="39931-120">Considere os requisitos da sua organização para o objetivo de tempo de recuperação (RTO).</span><span class="sxs-lookup"><span data-stu-id="39931-120">Consider your organization’s requirements for recovery time objective (RTO).</span></span>

<span data-ttu-id="39931-121">Modifique os procedimentos de backup e restauração neste tópico, adicionando e excluindo procedimentos conforme apropriado, para refletir os servidores e componentes na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="39931-121">Modify the backup and restoration procedures in this topic, adding and deleting procedures as appropriate, to reflect the servers and components in your deployment.</span></span> <span data-ttu-id="39931-122">Você também pode adicionar os detalhes apropriados, como o agendamento de backup, aos procedimentos apropriados para garantir que as informações não sejam ignoradas.</span><span class="sxs-lookup"><span data-stu-id="39931-122">You can also add appropriate details, such as the backup schedule, to the appropriate procedures to make sure that the information is not overlooked.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39931-123">É uma prática recomendada criar scripts para o maior número possível de etapas, para ajudar a garantir a qualidade e a Reproducibility de procedimentos.</span><span class="sxs-lookup"><span data-stu-id="39931-123">It is good practice to create scripts for as many steps as possible, to help ensure the quality and reproducibility of procedures.</span></span>



</div>

<span data-ttu-id="39931-124">Em seu plano, especifique quem é o responsável por revisar o plano, quem é responsável por testar e validar quaisquer novos procedimentos ou ferramentas e quem deve aprovar qualquer alteração no plano e nos procedimentos relacionados.</span><span class="sxs-lookup"><span data-stu-id="39931-124">In your plan, specify who is responsible for reviewing the plan, who is responsible for testing and validating any new procedures or tools, and who must approve any changes to the plan and related procedures.</span></span>

<span data-ttu-id="39931-125">Para garantir que seu plano de backup e restauração atenda totalmente a todas as metas e prioridades estabelecidas, obtenha a aprovação dos tomadores de decisões de negócios e tomadores de decisões técnicas adequados em sua organização antes de implementar o plano.</span><span class="sxs-lookup"><span data-stu-id="39931-125">To make sure that your backup and restoration plan fully meets all established goals and priorities, get the approval of the appropriate business decision makers and technical decision makers in your organization before you implement the plan.</span></span>

</div>

<div>

## <a name="implementing-the-backup-and-restoration-plan"></a><span data-ttu-id="39931-126">Implementando o plano de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="39931-126">Implementing the Backup and Restoration Plan</span></span>

<span data-ttu-id="39931-127">A implementação de um plano de backup e restauração requer as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="39931-127">Implementing a backup and restoration plan requires the following steps:</span></span>

  - <span data-ttu-id="39931-128">Testar e validar o plano.</span><span class="sxs-lookup"><span data-stu-id="39931-128">Testing and validating the plan.</span></span>

  - <span data-ttu-id="39931-129">Comunicar o plano.</span><span class="sxs-lookup"><span data-stu-id="39931-129">Communicating the plan.</span></span>

  - <span data-ttu-id="39931-130">Validando operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="39931-130">Validating backup and restoration operations.</span></span>

<div>

## <a name="testing-and-validating-the-plan"></a><span data-ttu-id="39931-131">Testando e validando o plano</span><span class="sxs-lookup"><span data-stu-id="39931-131">Testing and Validating the Plan</span></span>

<span data-ttu-id="39931-132">Os procedimentos descritos aqui foram testados e validados em um ambiente de laboratório.</span><span class="sxs-lookup"><span data-stu-id="39931-132">The procedures described here have been tested and validated in a lab environment.</span></span> <span data-ttu-id="39931-133">Para garantir que esses ou outros procedimentos funcionem em seu ambiente, você deve testar e validar cada procedimento que pretende implementar.</span><span class="sxs-lookup"><span data-stu-id="39931-133">To make sure that these or any other procedures work in your environment, you should test and validate each procedure you intend to implement.</span></span> <span data-ttu-id="39931-134">Conclua o teste e a validação antes de enviar seu plano para aprovação final.</span><span class="sxs-lookup"><span data-stu-id="39931-134">Complete the testing and the validation before you submit your plan for final approval.</span></span>

</div>

<div>

## <a name="communicating-the-plan"></a><span data-ttu-id="39931-135">Comunicando o plano</span><span class="sxs-lookup"><span data-stu-id="39931-135">Communicating the Plan</span></span>

<span data-ttu-id="39931-136">Seu plano de backup e restauração deve descrever claramente quem implementa procedimentos e instruções passo a passo para executar os procedimentos.</span><span class="sxs-lookup"><span data-stu-id="39931-136">Your backup and restoration plan should clearly describe who implements procedures and step-by-step instructions for carrying out the procedures.</span></span> <span data-ttu-id="39931-137">Você deve certificar-se de que todos responsáveis por qualquer aspecto de backup e restauração compreendam o plano, como ele deve ser implementado e qual é a função deles.</span><span class="sxs-lookup"><span data-stu-id="39931-137">You should make sure that everyone responsible for any aspect of backup and restoration understands the plan, how it is to be implemented, and what their role is.</span></span> <span data-ttu-id="39931-138">Isso inclui todos os requisitos de implementação para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39931-138">This includes all implementation requirements for the following:</span></span>

  - <span data-ttu-id="39931-139">Backup do pool e do servidor.</span><span class="sxs-lookup"><span data-stu-id="39931-139">Pool and server backup.</span></span>

  - <span data-ttu-id="39931-140">Restauração do serviço.</span><span class="sxs-lookup"><span data-stu-id="39931-140">Restoration of service.</span></span>

<span data-ttu-id="39931-141">**Backup do pool e do servidor**</span><span class="sxs-lookup"><span data-stu-id="39931-141">**Pool and server backup**</span></span>

<span data-ttu-id="39931-142">O plano de backup e restauração deve incluir todas as informações necessárias para concluir os procedimentos de backup continuamente.</span><span class="sxs-lookup"><span data-stu-id="39931-142">The backup and restoration plan should include all information required to complete backup procedures on an ongoing basis.</span></span> <span data-ttu-id="39931-143">As informações principais a serem comunicadas aos membros da equipe responsável incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39931-143">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="39931-144">Equipe ou pessoa (especificada como uma pessoa ou função) responsável por fazer backup de cada servidor.</span><span class="sxs-lookup"><span data-stu-id="39931-144">Team or person (specified as an individual or role) responsible for backing up each server.</span></span>

  - <span data-ttu-id="39931-145">Agendas específicas para fazer backup de cada servidor.</span><span class="sxs-lookup"><span data-stu-id="39931-145">Specific schedules for backing up each server.</span></span>

  - <span data-ttu-id="39931-146">Locais de backup para cada tipo de dados (configurações, banco de dados e compartilhamentos de arquivos).</span><span class="sxs-lookup"><span data-stu-id="39931-146">Backup locations for each type of data (settings, database, and file shares).</span></span>

  - <span data-ttu-id="39931-147">Procedimentos de backup a serem usados, incluindo as ferramentas necessárias para concluir cada procedimento.</span><span class="sxs-lookup"><span data-stu-id="39931-147">Backup procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="39931-148">Informações necessárias para concluir backups, conforme abordado nas [planilhas de backup e restauração do Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="39931-148">Information required to complete backups, as covered in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="39931-149">Métodos de validação a serem usados para ajudar a garantir que os dados e configurações sejam backups adequadamente e disponíveis para restauração, que podem incluir auditorias periódicas e restaurações de teste.</span><span class="sxs-lookup"><span data-stu-id="39931-149">Validation methods to be used to help ensure that data and settings are appropriately backed up and available for restoration, which can include periodic audits and test restorations.</span></span>

<span data-ttu-id="39931-150">**Restauração do serviço**</span><span class="sxs-lookup"><span data-stu-id="39931-150">**Restoration of service**</span></span>

<span data-ttu-id="39931-151">O plano de backup e restauração deve incluir todas as informações necessárias para restaurar o serviço, caso um ou mais servidores tenham uma perda que torna o serviço indisponível.</span><span class="sxs-lookup"><span data-stu-id="39931-151">The backup and restoration plan should include all information required to restore service, in case one or more servers experience a loss that makes service unavailable.</span></span> <span data-ttu-id="39931-152">As informações principais a serem comunicadas aos membros da equipe responsável incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39931-152">The primary information to be communicated to responsible team members includes the following:</span></span>

  - <span data-ttu-id="39931-153">Equipe ou pessoa (especificada como uma pessoa ou uma função) que é responsável por determinar quando a restauração do serviço é necessária e os procedimentos a serem usados para restaurar o serviço e também a equipe ou pessoa responsável pela implementação de procedimentos para cada cenário de restauração.</span><span class="sxs-lookup"><span data-stu-id="39931-153">Team or person (specified as an individual or a role) that is responsible for determining when restoration of service is required and the procedures to be used to restore service, and also the team or person responsible for implementing procedures for each restoration scenario.</span></span>

  - <span data-ttu-id="39931-154">Os critérios para determinar quais procedimentos de restauração são mais apropriados para uma situação específica.</span><span class="sxs-lookup"><span data-stu-id="39931-154">Criteria for determining which restoration procedures are most appropriate for a specific situation.</span></span>

  - <span data-ttu-id="39931-155">Estimativas de tempo para restauração do RTO (objetivo de tempo de recuperação) e de serviço (RTO) em cada cenário de restauração.</span><span class="sxs-lookup"><span data-stu-id="39931-155">Time estimates for restoration of service and recovery time objective (RTO) in each restoration scenario.</span></span>

  - <span data-ttu-id="39931-156">Procedimentos de restauração a serem usados, incluindo as ferramentas necessárias para concluir cada procedimento.</span><span class="sxs-lookup"><span data-stu-id="39931-156">Restoration procedures to be used, including the tools required to complete each procedure.</span></span>

  - <span data-ttu-id="39931-157">Informações necessárias para restaurar dados e configurações.</span><span class="sxs-lookup"><span data-stu-id="39931-157">Information required to restore data and settings.</span></span> <span data-ttu-id="39931-158">As planilhas são fornecidas em [planilhas de backup e restauração para o Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="39931-158">Worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

</div>

<div>

## <a name="validating-backup-and-restoration-operations"></a><span data-ttu-id="39931-159">Validando operações de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="39931-159">Validating Backup and Restoration Operations</span></span>

<span data-ttu-id="39931-160">Depois de concluir os esforços iniciais de backup em seu ambiente de produção e em intervalos específicos (conforme abordado em seu plano de backup e restauração), você deve verificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39931-160">After completing initial backup efforts in your production environment and at specified intervals (as covered in your backup and restoration plan), you should verify the following:</span></span>

  - <span data-ttu-id="39931-161">Os backups ocorrem conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="39931-161">Backups are occurring as required.</span></span>

  - <span data-ttu-id="39931-162">Dados de backup e configurações são acessíveis.</span><span class="sxs-lookup"><span data-stu-id="39931-162">Backed-up data and settings are accessible.</span></span>

  - <span data-ttu-id="39931-163">Os procedimentos de restauração podem ser executados dentro dos tempos de objetivo de tempo de recuperação especificados no plano de backup e restauração, e os resultados atendem a todas as necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="39931-163">Restoration procedures can be performed within the recovery time objective (RTO) times specified in the backup and restoration plan, and the results meet all business requirements.</span></span>

  - <span data-ttu-id="39931-164">As planilhas de backup foram concluídas e verificadas e são armazenadas em um local seguro.</span><span class="sxs-lookup"><span data-stu-id="39931-164">Backup worksheets have been completed and verified, and they are stored in a secure location.</span></span> <span data-ttu-id="39931-165">Essas planilhas são fornecidas em [planilhas de backup e restauração para o Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span><span class="sxs-lookup"><span data-stu-id="39931-165">These worksheets are provided in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md).</span></span>

  - <span data-ttu-id="39931-166">Procedimentos de restauração foram testados e verificados para funcionar como esperado, conforme especificado no seu plano de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="39931-166">Restoration procedures have been tested and verified to work as expected, as specified in your backup and restoration plan.</span></span>

</div>

</div>

<div>

## <a name="maintaining-the-backup-and-restoration-plan"></a><span data-ttu-id="39931-167">Manutenção do plano de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="39931-167">Maintaining the Backup and Restoration Plan</span></span>

<span data-ttu-id="39931-168">Uma topologia do Lync Server é um ambiente dinâmico que muda para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="39931-168">A Lync Server topology is a dynamic environment that changes with your organization.</span></span> <span data-ttu-id="39931-169">Reavalie seu plano de backup e restauração à medida que sua organização muda e revise-a periodicamente para garantir que ela continue atendendo às necessidades da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="39931-169">Reassess your backup and restoration plan as your organization changes, and review it periodically to make sure that it continues to meet the needs of your business.</span></span>

<span data-ttu-id="39931-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39931-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

