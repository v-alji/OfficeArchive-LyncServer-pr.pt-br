---
title: 'Lync Server 2013: gerenciar locais para gateways ELIN'
description: 'Lync Server 2013: gerenciar locais para gateways do ELIN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing locations for ELIN gateways
ms:assetid: ced79c13-4e7e-4034-95cd-6fc913f4f222
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205288(v=OCS.15)
ms:contentKeyID: 48185496
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 94fe7797c0f25adb219512cef4a6c0fb7d84b48d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437396"
---
# <a name="managing-locations-for-elin-gateways-in-lync-server-2013"></a><span data-ttu-id="26250-103">Gerenciando locais para gateways do ELIN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26250-103">Managing locations for ELIN gateways in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26250-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26250-104">

<span> </span></span></span>

<span data-ttu-id="26250-105">_**Tópico da última modificação:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="26250-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="26250-106">Para que o Lync Server forneça automaticamente locais para clientes em uma rede, você precisa executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="26250-106">To have Lync Server automatically provide locations for clients within a network, you need to perform the following tasks:</span></span>

  - <span data-ttu-id="26250-107">Preencha o banco de dados do serviço de informações de localização com uma rede Wiremap e inclua os números de identificação de localização de emergência (ELINs) no campo CompanyName.</span><span class="sxs-lookup"><span data-stu-id="26250-107">Populate the Location Information service database with a network wiremap, and include the Emergency Location Identification Numbers (ELINs) in the CompanyName field.</span></span>

  - <span data-ttu-id="26250-108">Publique os locais para que estejam disponíveis para clientes em sua rede.</span><span class="sxs-lookup"><span data-stu-id="26250-108">Publish the locations so that they are available for clients in your network.</span></span>

  - <span data-ttu-id="26250-109">Carregue os ELINs no banco de dados de Identificação de Localização Automática (ALI) da transportadora PSTN.</span><span class="sxs-lookup"><span data-stu-id="26250-109">Upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span>

<span data-ttu-id="26250-110">Para obter detalhes sobre como executar essas tarefas, consulte [Configurar o banco de dados de localização no Lync Server 2013](lync-server-2013-configure-the-location-database.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="26250-110">For details about how to perform these tasks, see [Configure the location database in Lync Server 2013](lync-server-2013-configure-the-location-database.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="26250-111">Os locais adicionados ao banco de dados do local central não estarão disponíveis para o cliente até serem publicados usando um comando shell do Shell de gerenciamento do Lync Server e serão duplicados para os armazenamentos locais do pool.</span><span class="sxs-lookup"><span data-stu-id="26250-111">Locations added to the central location database are not available to the client until they have been published by using a Lync Server Management Shell command and are replicated to the pool's local stores.</span></span> <span data-ttu-id="26250-112">Para obter detalhes, consulte <A href="lync-server-2013-publish-the-location-database.md">publicar o banco de dados de local do Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="26250-112">For details, see <A href="lync-server-2013-publish-the-location-database.md">Publish the location database from Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="26250-113">Esta seção descreve coisas a considerar conforme você planeja atualizar e manter o banco de dados de localização.</span><span class="sxs-lookup"><span data-stu-id="26250-113">This section describes things to consider as you plan to update and maintain the location database.</span></span>

<div>

## <a name="planning-emergency-locations"></a><span data-ttu-id="26250-114">Planejamento de locais de emergência</span><span class="sxs-lookup"><span data-stu-id="26250-114">Planning Emergency Locations</span></span>

<span data-ttu-id="26250-115">Ao usar gateways do ELIN, você preenche o banco de dados do serviço de informações de localização com o endereço cívico, um local específico dentro de um edifício e pelo menos um ELIN para cada local.</span><span class="sxs-lookup"><span data-stu-id="26250-115">When you use ELIN gateways, you populate the Location Information service database with the civic address, a specific location within a building, and at least one ELIN for each location .</span></span> <span data-ttu-id="26250-116">Durante a fase de planejamento, é uma boa ideia decidir como deseja nomear os locais e como você deseja atribuir os ELINs.</span><span class="sxs-lookup"><span data-stu-id="26250-116">During the planning phase, it is a good idea to decide how you want to name the locations and how you want to assign ELINs.</span></span>

<div>

## <a name="planning-location-names"></a><span data-ttu-id="26250-117">Planejamento dos nomes de local</span><span class="sxs-lookup"><span data-stu-id="26250-117">Planning Location Names</span></span>

<span data-ttu-id="26250-118">O campo **local** do serviço de informações de localização, que contém o local específico dentro de um edifício, tem um comprimento máximo de 20 caracteres (incluindo espaços).</span><span class="sxs-lookup"><span data-stu-id="26250-118">The Location Information service **Location** field, which holds the specific location within a building, has a maximum length of 20 characters (including spaces).</span></span> <span data-ttu-id="26250-119">Dentro deste comprimento limitado, tente incluir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="26250-119">Within that limited length, try to include the following:</span></span>

  - <span data-ttu-id="26250-p104">Um nome fácil de compreender que identifica o local do chamador 911 para ajudar a garantir que os respondedores da emergência encontrem o local específico rapidamente quando chegarem ao endereço civil. Este nome de local pode incluir um número de construção, número do piso, designador de asa, número da sala e assim por diante. Evite apelidos que são conhecidos apenas pelos funcionários, que pode fazer com que os respondedores de emergência vão para o local incorreto.</span><span class="sxs-lookup"><span data-stu-id="26250-p104">An easy-to-understand name that identifies the location of the 911 caller to help ensure that emergency responders find the specific location promptly when they arrive at the civic address. This location name may include a building number, floor number, wing designator, room number, and so on. Avoid nicknames that are known only to employees, which might cause emergency responders to go to the wrong location.</span></span>

  - <span data-ttu-id="26250-123">Um identificador de localização que ajuda os usuários a ver facilmente que o cliente do Lync selecionou o local correto.</span><span class="sxs-lookup"><span data-stu-id="26250-123">A location identifier that helps users to easily see that their Lync client picked up the correct location.</span></span> <span data-ttu-id="26250-124">O cliente Lync concatena e exibe automaticamente os campos **local** e **cidade** descobertos no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="26250-124">The Lync client automatically concatenates and displays the discovered **Location** and **City** fields in its header.</span></span> <span data-ttu-id="26250-125">Uma prática recomendada é adicionar o endereço do edifício a cada identificador de localização (por exemplo, "primeiro andar \<street number\> ").</span><span class="sxs-lookup"><span data-stu-id="26250-125">A good practice is to add the street address of the building to each location identifier (for example, "1st Floor \<street number\>").</span></span> <span data-ttu-id="26250-126">Sem o endereço físico, um identificador de local genérico como "1° andar" pode ser aplicado a qualquer edifício na cidade.</span><span class="sxs-lookup"><span data-stu-id="26250-126">Without the street address, a generic location identifier such as "1st Floor" could apply to any building in the city.</span></span>

  - <span data-ttu-id="26250-127">Se o local for aproximado por ser determinado por um ponto de acesso sem fio, convém adicionar a palavra  Near (por exemplo, próximo ao 1º andar, 1234).</span><span class="sxs-lookup"><span data-stu-id="26250-127">If the location is approximate because it’s determined by a wireless access point, you may want to add the word Near (for example, "Near 1st Floor 1234").</span></span>

</div>

<div>

## <a name="planning-elins"></a><span data-ttu-id="26250-128">Planejamento de ELINs</span><span class="sxs-lookup"><span data-stu-id="26250-128">Planning ELINs</span></span>

<span data-ttu-id="26250-p106">Após decidir como você deseja dividir o espaço da construção em locais, é necessário decidir quantos ELINs atribuir em cada local. Por exemplo, em uma construção de vários locais ou pisos, diferentes áreas na construção podem ser atribuídas com zonas de emergência diferentes. Geralmente, cada piso na construção é designado como um local. Cada local é atribuído com um ou mais ELINs, que são usados como números de chamada durante uma chamada de emergência. Entre em contato com sua transportadora PSTN para obter os números de telefone que você pode usar para ELINs. A tabela a seguir oferece um exemplo de locais para um endereço específico.</span><span class="sxs-lookup"><span data-stu-id="26250-p106">After you decide how you want to divide your building space into locations, you need to decide how many ELINs to assign to each location. For example, in a multifloor or multitenant building, different areas in the building can be assigned different emergency zones. Typically, each floor in a building is designated as a location. Each location is then assigned one or more ELINs, which are used as the calling number(s) during an emergency call. Contact your PSTN carrier for phone numbers that you can use for ELINs. The following table provides an example of locations for a specific street address.</span></span>

### <a name="sample-location-and-elin-assignments"></a><span data-ttu-id="26250-135">Local de amostra e Atribuições de ELIN</span><span class="sxs-lookup"><span data-stu-id="26250-135">Sample Location and ELIN Assignments</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26250-136">Área de construção</span><span class="sxs-lookup"><span data-stu-id="26250-136">Building Area</span></span></th>
<th><span data-ttu-id="26250-137">Local</span><span class="sxs-lookup"><span data-stu-id="26250-137">Location</span></span></th>
<th><span data-ttu-id="26250-138">ELIN</span><span class="sxs-lookup"><span data-stu-id="26250-138">ELIN</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26250-139">Primeiro andar</span><span class="sxs-lookup"><span data-stu-id="26250-139">First floor</span></span></p></td>
<td><p><span data-ttu-id="26250-140">1</span><span class="sxs-lookup"><span data-stu-id="26250-140">1</span></span></p></td>
<td><p><span data-ttu-id="26250-141">425-555-0100</span><span class="sxs-lookup"><span data-stu-id="26250-141">425-555-0100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26250-142">Segundo andar</span><span class="sxs-lookup"><span data-stu-id="26250-142">Second floor</span></span></p></td>
<td><p><span data-ttu-id="26250-143">2</span><span class="sxs-lookup"><span data-stu-id="26250-143">2</span></span></p></td>
<td><p><span data-ttu-id="26250-144">425-555-0111</span><span class="sxs-lookup"><span data-stu-id="26250-144">425-555-0111</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26250-145">Terceiro andar</span><span class="sxs-lookup"><span data-stu-id="26250-145">Third floor</span></span></p></td>
<td><p><span data-ttu-id="26250-146">3</span><span class="sxs-lookup"><span data-stu-id="26250-146">3</span></span></p></td>
<td><p><span data-ttu-id="26250-147">425-555-0123</span><span class="sxs-lookup"><span data-stu-id="26250-147">425-555-0123</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26250-148">Os locais definidos devem atender os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="26250-148">The locations you define should meet the following requirements:</span></span>

  - <span data-ttu-id="26250-149">Cumpre os regulamentos locais e nacionais/regionais em termos de área máxima por local e número de locais por endereço.</span><span class="sxs-lookup"><span data-stu-id="26250-149">Comply with local and national/regional regulations in terms of maximum area per location and number of locations per street address.</span></span>

  - <span data-ttu-id="26250-150">São específicos o suficiente para tornar fácil localizar o chamador de emergência.</span><span class="sxs-lookup"><span data-stu-id="26250-150">Are specific enough to make it easy to locate the emergency caller.</span></span>

</div>

</div>

<div>

## <a name="populating-the-location-database"></a><span data-ttu-id="26250-151">Preenchendo o banco de dados Local</span><span class="sxs-lookup"><span data-stu-id="26250-151">Populating the Location Database</span></span>

<span data-ttu-id="26250-152">As seguintes perguntas ajudarão a determinar como preencher o banco de dados de local.</span><span class="sxs-lookup"><span data-stu-id="26250-152">The following questions will help you determine how to will populate the location database.</span></span>

  - <span data-ttu-id="26250-153">**Qual processo você usará para preencher o banco de dados de local?**</span><span class="sxs-lookup"><span data-stu-id="26250-153">**What process will you use to populate the location database?**</span></span>  
    <span data-ttu-id="26250-p107">Onde estão os dados e quais etapas você precisa executar para convertê-los para o formato necessário pelo banco de dados de local? Você adicionará locais individualmente ou em lote usando um arquivo CSV?</span><span class="sxs-lookup"><span data-stu-id="26250-p107">Where does the data exist, and what steps do you need to take to convert the data into the format required by the location database? Will you add locations individually, or in bulk, by using a CSV file?</span></span>

<!-- end list -->

  - <span data-ttu-id="26250-156">**Você tem um banco de dados de terceiro que já contém um mapeamento de locais?**</span><span class="sxs-lookup"><span data-stu-id="26250-156">**Do you have a third party database that already contains a mapping of locations?**</span></span>  
    <span data-ttu-id="26250-157">Ao usar a opção do serviço de informações de localização secundária do Lync Server para se conectar a um banco de dados de terceiros, você pode agrupar e gerenciar locais usando uma plataforma offline.</span><span class="sxs-lookup"><span data-stu-id="26250-157">By using Lync Server's Secondary Location Information service option to connect to a third-party database, you can group and manage locations by using an offline platform.</span></span> <span data-ttu-id="26250-158">Um benefício dessa abordagem é que além de associar locais aos identificadores de rede, é possível associar locais a um usuário.</span><span class="sxs-lookup"><span data-stu-id="26250-158">A benefit to this approach is that in addition to associating locations to network identifiers, you can associate locations to a user.</span></span> <span data-ttu-id="26250-159">Isso significa que o serviço de informações de localização pode retornar vários endereços, originários do serviço de informações de localização secundário, para um cliente do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="26250-159">This means that the Location Information service can return multiple addresses, originating from the Secondary Location Information service, to a Lync Server client.</span></span> <span data-ttu-id="26250-160">Em seguida, o usuário pode escolher o local mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="26250-160">The user can then choose the most appropriate location.</span></span>
    
    <span data-ttu-id="26250-161">Para integrar-se com o serviço informações de localização, o banco de dados de terceiros deve seguir o esquema de solicitação/resposta de localização do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="26250-161">To integrate with the Location Information service, the third-party database must follow the Lync Server Location Request/Response schema.</span></span> <span data-ttu-id="26250-162">Para obter detalhes, consulte <https://go.microsoft.com/fwlink/p/?linkid=213819> .</span><span class="sxs-lookup"><span data-stu-id="26250-162">For details, see <https://go.microsoft.com/fwlink/p/?linkid=213819>.</span></span> <span data-ttu-id="26250-163">Para obter detalhes sobre a implantação de um serviço de informações de localização secundário, consulte [configurar um serviço de informações de localização secundário no Lync Server 2013](lync-server-2013-configure-a-secondary-location-information-service.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="26250-163">For details about deploying a Secondary Location Information service, see [Configure a secondary Location Information service in Lync Server 2013](lync-server-2013-configure-a-secondary-location-information-service.md) in the Deployment documentation.</span></span>

<span data-ttu-id="26250-164">Para obter detalhes sobre como preencher o banco de dados de localização, consulte [Configurar o banco de dados de localização no Lync Server 2013](lync-server-2013-configure-the-location-database.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="26250-164">For details about populating the location database, see [Configure the location database in Lync Server 2013](lync-server-2013-configure-the-location-database.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="maintaining-the-location-database"></a><span data-ttu-id="26250-165">Manutenção do banco de dados de local</span><span class="sxs-lookup"><span data-stu-id="26250-165">Maintaining the Location Database</span></span>

<span data-ttu-id="26250-p110">Depois de preencher o banco de dados de local, é necessário desenvolver uma estratégia para atualização do banco de dados à medida que a configuração de rede mudar. As seguintes perguntas ajudarão a determinar como você manterá o banco de dados de local.</span><span class="sxs-lookup"><span data-stu-id="26250-p110">After you populate the location database, you need to develop a strategy for updating the database as the network configuration changes. The following questions will help you determine how to maintain the location database.</span></span>

  - <span data-ttu-id="26250-168">**Como você atualizará o banco de dados de local?**</span><span class="sxs-lookup"><span data-stu-id="26250-168">**How will you update the location database?**</span></span>  
    <span data-ttu-id="26250-p111">Há diversos cenários que exigem uma atualização para o banco de dados de local, incluindo a adição de WAPs (pontos de acesso sem fio), recabeamento do escritório (resultando em atribuições de comutação diferentes) e expansão da subrede. Você atualizará diretamente cada local individual ou realizará uma atualização em massa de todos os locais usando um arquivo CSV?</span><span class="sxs-lookup"><span data-stu-id="26250-p111">There are several scenarios that require an update to the location database, including adding wireless access points (WAPs), office recabling (resulting in different switch assignments), and subnet expansion. Will you directly update each individual location, or will you perform a bulk update of all the locations by using a CSV file?</span></span>

<!-- end list -->

  - <span data-ttu-id="26250-171">**Você usará um aplicativo SNMP para que os endereços do MAC do cliente do Skype sejam compatíveis aos identificadores de porta e de comutador?**</span><span class="sxs-lookup"><span data-stu-id="26250-171">**Will you use an SNMP application to match Lync client MAC addresses to port and switch identifiers?**</span></span>  
    <span data-ttu-id="26250-172">Se você usar um aplicativo SNMP, precisará desenvolver um processo manual para manter as informações de porta e chassis de comutador consistentes entre o aplicativo SNMP e o banco de dados de local.</span><span class="sxs-lookup"><span data-stu-id="26250-172">If you use an SNMP application, you need to develop a manual process for keeping the switch chassis and port information consistent between the SNMP application and the location database.</span></span> <span data-ttu-id="26250-173">Se o aplicativo SNMP retornar um endereço IP de chassi ou uma ID de porta que não está incluída no banco de dados, o serviço de informações de localização não poderá retornar um local ao cliente.</span><span class="sxs-lookup"><span data-stu-id="26250-173">If the SNMP application returns a chassis IP address or port ID that is not included in the database, the Location Information service will not be able to return a location to the client.</span></span>

<span data-ttu-id="26250-174"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26250-174"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

