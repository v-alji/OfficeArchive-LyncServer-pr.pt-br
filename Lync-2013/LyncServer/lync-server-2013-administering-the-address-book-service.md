---
title: 'Lync Server 2013: administrando o serviço de catálogo de endereços'
description: 'Lync Server 2013: administrando o serviço de catálogo de endereços.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering the Address Book Service
ms:assetid: 801e4243-9670-4477-aa2f-88b61ecf5351
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429711(v=OCS.15)
ms:contentKeyID: 48184649
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86d549b06b5c6ac1c450edf9e7edb0b902ef9adf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440693"
---
# <a name="administering-the-address-book-service-in-lync-server-2013"></a><span data-ttu-id="49656-103">Administrar o serviço de catálogo de endereços no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49656-103">Administering the Address Book Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49656-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49656-104">

<span> </span></span></span>

<span data-ttu-id="49656-105">_**Tópico da última modificação:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="49656-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="49656-106">Como parte da implantação do Lync Server, Enterprise Edition ou do servidor Standard Edition, o serviço de catálogo de endereços é instalado por padrão.</span><span class="sxs-lookup"><span data-stu-id="49656-106">As a part of the deployment of Lync Server, Enterprise Edition or Standard Edition server, the Address Book Service is installed by default.</span></span> <span data-ttu-id="49656-107">O banco de dados usado pelo serviço de catálogo de endereços – RTCab – é criado no SQL Server (para Enterprise Edition, esse é o servidor SQL Server de back-end; para o servidor Standard Edition, o SQL Server posicionado).</span><span class="sxs-lookup"><span data-stu-id="49656-107">The database used by the Address Book Service – RTCab – is created on the SQL Server (for Enterprise Edition, this is the back-end SQL Server; for Standard Edition server, the collocated SQL Server).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49656-108">Para obter informações sobre como usar o <STRONG>ADSI Edit</STRONG> para editar atributos de objeto dos serviços de domínio Active Directory, consulte <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI Edit</A>.</span><span class="sxs-lookup"><span data-stu-id="49656-108">For information about using <STRONG>ADSI Edit</STRONG> to edit Active Directory Domain Services object attributes, see <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI Edit</A>.</span></span> <span data-ttu-id="49656-109">Para obter informações sobre uma ferramenta no kit de recursos especificamente para o serviço de catálogo de endereços, consulte <A href="https://go.microsoft.com/fwlink/?linkid=330429">Ferramentas do Microsoft Lync Server 2013 Resource Kit</A>.</span><span class="sxs-lookup"><span data-stu-id="49656-109">For information about a tool in the Resource Kit specifically for the Address Book service, see <A href="https://go.microsoft.com/fwlink/?linkid=330429">Microsoft Lync Server 2013 Resource Kit Tools</A>.</span></span>



</div>

<div>

## <a name="address-book-server-phone-number-normalization"></a><span data-ttu-id="49656-110">Normalização do número de telefone do servidor do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="49656-110">Address Book Server Phone Number Normalization</span></span>

<span data-ttu-id="49656-111">O Lync Server exige números de telefone padrão RFC 3966/E. 164.</span><span class="sxs-lookup"><span data-stu-id="49656-111">Lync Server requires standardized RFC 3966/E.164 phone numbers.</span></span> <span data-ttu-id="49656-112">Para usar números de telefone não estruturados ou formatados de forma inconsistente, o Lync Server dependerá do servidor do catálogo de endereços para processar os números de telefone antes que eles sejam entregues às regras de normalização.</span><span class="sxs-lookup"><span data-stu-id="49656-112">To use phone numbers that are unstructured or inconsistently formatted, Lync Server relies on the Address Book Server to preprocess phone numbers before they are handed off to the normalization rules.</span></span> <span data-ttu-id="49656-113">Quando um número de telefone é usado no catálogo de endereços e a regra de normalização é aplicada, os clientes, como o Lync Phone Edition e o Lync Mobile, podem usar esses números normalizados.</span><span class="sxs-lookup"><span data-stu-id="49656-113">When a phone number is used from the address book and the normalization rule is applied, clients, such as Lync Phone Edition and Lync Mobile, can use these normalized numbers.</span></span>

<span data-ttu-id="49656-114">As regras de normalização usadas nas versões anteriores podem não funcionar corretamente sem alguns ajustes.</span><span class="sxs-lookup"><span data-stu-id="49656-114">The normalization rules that were used in previous versions may not work properly without some adjustments.</span></span> <span data-ttu-id="49656-115">Como o espaço em branco e os caracteres não obrigatórios são removidos antes das regras de normalização, se a sua expressão Regex estiver procurando por um traço ou outro caractere que tenha sido removido, sua regra de normalidade poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="49656-115">Because the white space and non-mandatory characters are removed prior to the normalization rules, if your regex expression is specifically looking for a dash or other character that was removed, your normalization rule might fail.</span></span> <span data-ttu-id="49656-116">Você deve revisar suas regras de normalização para garantir que elas não estejam procurando por esses caracteres não obrigatórios, ou que a regra possa ser reprovada e continue no caso de o personagem não estar presente onde a regra prevê que ela será.</span><span class="sxs-lookup"><span data-stu-id="49656-116">You should review your normalization rules to ensure that either they are not looking for these non-mandatory characters, or that the rule can fail gracefully and continue in the event that the character is not present where the rule anticipates it will be.</span></span>

</div>

<div>

## <a name="user-replicator-and-address-book-server"></a><span data-ttu-id="49656-117">Duplicador de usuários e servidor de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="49656-117">User Replicator and Address Book Server</span></span>

<span data-ttu-id="49656-118">O servidor de catálogo de endereços usa os dados fornecidos pelo duplicador de usuários para atualizar as informações que ele inicialmente obtém na GAL (lista de endereços global).</span><span class="sxs-lookup"><span data-stu-id="49656-118">The Address Book Server uses data provided by User Replicator to update the information that it initially obtains from the global address list (GAL).</span></span> <span data-ttu-id="49656-119">O Duplicador do usuário grava os atributos dos serviços de domínio Active Directory para cada usuário, contato e grupo na tabela AbUserEntry do banco de dados, e o servidor do catálogo de endereços sincroniza os dados do usuário do banco de dados em arquivos no repositório de arquivos do servidor do catálogo de endereços e no banco de dados do catálogo de endereços do RTCab.</span><span class="sxs-lookup"><span data-stu-id="49656-119">User Replicator writes the Active Directory Domain Services attributes for each user, contact, and group into the AbUserEntry table in the database and the Address Book Server syncs the user data from the database into files in the Address Book Server file store and into the Address Book database RTCab.</span></span> <span data-ttu-id="49656-120">O esquema para a tabela AbUserEntry usa duas colunas, **userguid** e **UserData**.</span><span class="sxs-lookup"><span data-stu-id="49656-120">The schema for the AbUserEntry table uses two columns, **UserGuid** and **UserData**.</span></span> <span data-ttu-id="49656-121">**Userguid** é a coluna de índice e contém o GUID de 16 bytes do objeto do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="49656-121">**UserGuid** is the index column and contains the 16-byte GUID of the Active Directory object.</span></span> <span data-ttu-id="49656-122">**UserData** é uma coluna de imagem que contém todos os atributos dos serviços de domínio do Active Directory mencionados anteriormente para esse contato.</span><span class="sxs-lookup"><span data-stu-id="49656-122">**UserData** is an image column which contains all of the previously mentioned Active Directory Domain Services attributes for that contact.</span></span>

<span data-ttu-id="49656-123">O duplicador de usuários determina quais atributos do Active Directory gravar lendo uma tabela de configuração localizada na mesma instância baseada no SQL Server como a tabela AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="49656-123">User Replicator determines which Active Directory attributes to write by reading a configuration table located in the same SQL Server-based instance as the AbUserEntry table.</span></span> <span data-ttu-id="49656-124">A tabela AbAttribute contém três colunas, **ID**, **nome**, **sinalizadores** e **habilitar**.</span><span class="sxs-lookup"><span data-stu-id="49656-124">The AbAttribute table contains three columns, **ID**, **Name**, **Flags**, and **Enable**.</span></span> <span data-ttu-id="49656-125">A tabela é criada durante a configuração do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49656-125">The table is created during database setup.</span></span> <span data-ttu-id="49656-126">Se a tabela AbAttribute estiver vazia, o usuário duplicador ignorará sua lógica de processamento de tabela AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="49656-126">If the AbAttribute table is empty, User Replicator skips its AbUserEntry table processing logic.</span></span> <span data-ttu-id="49656-127">Os atributos do servidor de catálogo de endereços são dinâmicos e são recuperados da tabela AbAttribute, que é inicialmente escrita pelo servidor de catálogo de endereços quando o servidor do catálogo de endereços é ativado.</span><span class="sxs-lookup"><span data-stu-id="49656-127">Address Book Server attributes are dynamic and are retrieved from the AbAttribute table, which is initially written by the Address Book Server when the Address Book Server is activated.</span></span>

<span data-ttu-id="49656-128">A ativação do servidor do catálogo de endereços preenche a tabela AbAttribute com os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="49656-128">Address Book Server activation populates the AbAttribute table with the values shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49656-129">ID</span><span class="sxs-lookup"><span data-stu-id="49656-129">ID</span></span></th>
<th><span data-ttu-id="49656-130">Nome</span><span class="sxs-lookup"><span data-stu-id="49656-130">Name</span></span></th>
<th><span data-ttu-id="49656-131">Informa</span><span class="sxs-lookup"><span data-stu-id="49656-131">Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49656-132">1</span><span class="sxs-lookup"><span data-stu-id="49656-132">1</span></span></p></td>
<td><p><span data-ttu-id="49656-133">especificado</span><span class="sxs-lookup"><span data-stu-id="49656-133">givenName</span></span></p></td>
<td><p><span data-ttu-id="49656-134">0x01400000</span><span class="sxs-lookup"><span data-stu-id="49656-134">0x01400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-135">2</span><span class="sxs-lookup"><span data-stu-id="49656-135">2</span></span></p></td>
<td><p><span data-ttu-id="49656-136">SN</span><span class="sxs-lookup"><span data-stu-id="49656-136">Sn</span></span></p></td>
<td><p><span data-ttu-id="49656-137">0x02400000</span><span class="sxs-lookup"><span data-stu-id="49656-137">0x02400000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-138">3</span><span class="sxs-lookup"><span data-stu-id="49656-138">3</span></span></p></td>
<td><p><span data-ttu-id="49656-139">displayName</span><span class="sxs-lookup"><span data-stu-id="49656-139">displayName</span></span></p></td>
<td><p><span data-ttu-id="49656-140">0x03420000</span><span class="sxs-lookup"><span data-stu-id="49656-140">0x03420000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-141">4</span><span class="sxs-lookup"><span data-stu-id="49656-141">4</span></span></p></td>
<td><p><span data-ttu-id="49656-142">Título</span><span class="sxs-lookup"><span data-stu-id="49656-142">Title</span></span></p></td>
<td><p><span data-ttu-id="49656-143">0x04000000</span><span class="sxs-lookup"><span data-stu-id="49656-143">0x04000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-144">5</span><span class="sxs-lookup"><span data-stu-id="49656-144">5</span></span></p></td>
<td><p><span data-ttu-id="49656-145">mailNickname</span><span class="sxs-lookup"><span data-stu-id="49656-145">mailNickname</span></span></p></td>
<td><p><span data-ttu-id="49656-146">0x05400000</span><span class="sxs-lookup"><span data-stu-id="49656-146">0x05400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-147">6</span><span class="sxs-lookup"><span data-stu-id="49656-147">6</span></span></p></td>
<td><p><span data-ttu-id="49656-148">Empresa</span><span class="sxs-lookup"><span data-stu-id="49656-148">Company</span></span></p></td>
<td><p><span data-ttu-id="49656-149">0x06000000</span><span class="sxs-lookup"><span data-stu-id="49656-149">0x06000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-150">7</span><span class="sxs-lookup"><span data-stu-id="49656-150">7</span></span></p></td>
<td><p><span data-ttu-id="49656-151">physicalDeliveryOfficeName</span><span class="sxs-lookup"><span data-stu-id="49656-151">physicalDeliveryOfficeName</span></span></p></td>
<td><p><span data-ttu-id="49656-152">0x07000000</span><span class="sxs-lookup"><span data-stu-id="49656-152">0x07000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-153">8</span><span class="sxs-lookup"><span data-stu-id="49656-153">8</span></span></p></td>
<td><p><span data-ttu-id="49656-154">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="49656-154">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="49656-155">0x08520C00</span><span class="sxs-lookup"><span data-stu-id="49656-155">0x08520C00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-156">9</span><span class="sxs-lookup"><span data-stu-id="49656-156">9</span></span></p></td>
<td><p><span data-ttu-id="49656-157">telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="49656-157">telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="49656-158">0x09022800</span><span class="sxs-lookup"><span data-stu-id="49656-158">0x09022800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-159">254</span><span class="sxs-lookup"><span data-stu-id="49656-159">10</span></span></p></td>
<td><p><span data-ttu-id="49656-160">homePhone</span><span class="sxs-lookup"><span data-stu-id="49656-160">homePhone</span></span></p></td>
<td><p><span data-ttu-id="49656-161">0x0A302800</span><span class="sxs-lookup"><span data-stu-id="49656-161">0x0A302800</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-162">11:00</span><span class="sxs-lookup"><span data-stu-id="49656-162">11</span></span></p></td>
<td><p><span data-ttu-id="49656-163">Mobile</span><span class="sxs-lookup"><span data-stu-id="49656-163">Mobile</span></span></p></td>
<td><p><span data-ttu-id="49656-164">0x0B622800</span><span class="sxs-lookup"><span data-stu-id="49656-164">0x0B622800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-165">12</span><span class="sxs-lookup"><span data-stu-id="49656-165">12</span></span></p></td>
<td><p><span data-ttu-id="49656-166">otherTelephone</span><span class="sxs-lookup"><span data-stu-id="49656-166">otherTelephone</span></span></p></td>
<td><p><span data-ttu-id="49656-167">0x0C302000</span><span class="sxs-lookup"><span data-stu-id="49656-167">0x0C302000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-168">0,13</span><span class="sxs-lookup"><span data-stu-id="49656-168">13</span></span></p></td>
<td><p><span data-ttu-id="49656-169">ipPhone</span><span class="sxs-lookup"><span data-stu-id="49656-169">ipPhone</span></span></p></td>
<td><p><span data-ttu-id="49656-170">0x0D302000</span><span class="sxs-lookup"><span data-stu-id="49656-170">0x0D302000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-171">14</span><span class="sxs-lookup"><span data-stu-id="49656-171">14</span></span></p></td>
<td><p><span data-ttu-id="49656-172">Mensageiro</span><span class="sxs-lookup"><span data-stu-id="49656-172">Mail</span></span></p></td>
<td><p><span data-ttu-id="49656-173">0x0E500000</span><span class="sxs-lookup"><span data-stu-id="49656-173">0x0E500000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-174">15</span><span class="sxs-lookup"><span data-stu-id="49656-174">15</span></span></p></td>
<td><p><span data-ttu-id="49656-175">GroupType</span><span class="sxs-lookup"><span data-stu-id="49656-175">groupType</span></span></p></td>
<td><p><span data-ttu-id="49656-176">0x0F010800</span><span class="sxs-lookup"><span data-stu-id="49656-176">0x0F010800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-177">16</span><span class="sxs-lookup"><span data-stu-id="49656-177">16</span></span></p></td>
<td><p><span data-ttu-id="49656-178">Partamentais</span><span class="sxs-lookup"><span data-stu-id="49656-178">Department</span></span></p></td>
<td><p><span data-ttu-id="49656-179">0x10000000</span><span class="sxs-lookup"><span data-stu-id="49656-179">0x10000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-180">16</span><span class="sxs-lookup"><span data-stu-id="49656-180">17</span></span></p></td>
<td><p><span data-ttu-id="49656-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="49656-181">Description</span></span></p></td>
<td><p><span data-ttu-id="49656-182">0x11000100</span><span class="sxs-lookup"><span data-stu-id="49656-182">0x11000100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-183">dezoito</span><span class="sxs-lookup"><span data-stu-id="49656-183">18</span></span></p></td>
<td><p><span data-ttu-id="49656-184">Gerente</span><span class="sxs-lookup"><span data-stu-id="49656-184">Manager</span></span></p></td>
<td><p><span data-ttu-id="49656-185">0x12040001</span><span class="sxs-lookup"><span data-stu-id="49656-185">0x12040001</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-186">pol</span><span class="sxs-lookup"><span data-stu-id="49656-186">19</span></span></p></td>
<td><p><span data-ttu-id="49656-187">proxyAddress</span><span class="sxs-lookup"><span data-stu-id="49656-187">proxyAddress</span></span></p></td>
<td><p><span data-ttu-id="49656-188">0x00500105</span><span class="sxs-lookup"><span data-stu-id="49656-188">0x00500105</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-189">cedido</span><span class="sxs-lookup"><span data-stu-id="49656-189">20</span></span></p></td>
<td><p><span data-ttu-id="49656-190">msExchHideFromAddressLists</span><span class="sxs-lookup"><span data-stu-id="49656-190">msExchHideFromAddressLists</span></span></p></td>
<td><p><span data-ttu-id="49656-191">0xFF000003</span><span class="sxs-lookup"><span data-stu-id="49656-191">0xFF000003</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-192">99</span><span class="sxs-lookup"><span data-stu-id="49656-192">99</span></span></p></td>
<td><p><span data-ttu-id="49656-193">EntryID</span><span class="sxs-lookup"><span data-stu-id="49656-193">entryID</span></span></p></td>
<td><p><span data-ttu-id="49656-194">0x99000000</span><span class="sxs-lookup"><span data-stu-id="49656-194">0x99000000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49656-195">Os números na coluna **ID** devem ser exclusivos e nunca devem ser reutilizados.</span><span class="sxs-lookup"><span data-stu-id="49656-195">The numbers in the **ID** column must be unique and should never be reused.</span></span> <span data-ttu-id="49656-196">Além disso, manter os valores de ID em 256 poupa espaço nos arquivos de saída gravados pelo servidor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="49656-196">Also, keeping the ID values under 256 saves space in the output files written by the Address Book Server.</span></span> <span data-ttu-id="49656-197">No entanto, o valor de ID máximo é 65535.</span><span class="sxs-lookup"><span data-stu-id="49656-197">However, the maximum ID value is 65535.</span></span> <span data-ttu-id="49656-198">A coluna **Name** corresponde ao nome de atributo do Active Directory que o replicador do usuário deve colocar na tabela AbUserEntry para cada contato.</span><span class="sxs-lookup"><span data-stu-id="49656-198">The **Name** column corresponds to the Active Directory attribute name that User Replicator should put in the AbUserEntry table for each contact.</span></span> <span data-ttu-id="49656-199">O valor na coluna **sinalizadores** é usado para definir o tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="49656-199">The value in the **Flags** column is used to define the type of attribute.</span></span> <span data-ttu-id="49656-200">Os seguintes tipos de atributos do servidor de catálogo de endereços são reconhecidos pelo replicador do usuário, indicado pelo byte inferior do valor na coluna **sinalizadores** .</span><span class="sxs-lookup"><span data-stu-id="49656-200">The following types of Address Book Server attributes are recognized by User Replicator, indicated by the low byte of the value in the **Flags** column.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49656-201">Atributo</span><span class="sxs-lookup"><span data-stu-id="49656-201">Attribute</span></span></th>
<th><span data-ttu-id="49656-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="49656-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49656-203">0x0</span><span class="sxs-lookup"><span data-stu-id="49656-203">0x0</span></span></p></td>
<td><p><span data-ttu-id="49656-204">Um atributo String.</span><span class="sxs-lookup"><span data-stu-id="49656-204">A string attribute.</span></span> <span data-ttu-id="49656-205">O duplicador de usuários converte esse tipo em UTF-8 antes de armazená-lo na tabela AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="49656-205">User Replicator converts this type to UTF-8 before storing it in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-206">0x1</span><span class="sxs-lookup"><span data-stu-id="49656-206">0x1</span></span></p></td>
<td><p><span data-ttu-id="49656-207">Um atributo binário.</span><span class="sxs-lookup"><span data-stu-id="49656-207">A binary attribute.</span></span> <span data-ttu-id="49656-208">O duplicador de usuários armazena isso no blob sem nenhuma conversão.</span><span class="sxs-lookup"><span data-stu-id="49656-208">User Replicator stores this in the blob without any conversion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-209">0x2</span><span class="sxs-lookup"><span data-stu-id="49656-209">0x2</span></span></p></td>
<td><p><span data-ttu-id="49656-210">Um atributo String, mas está incluído apenas se o valor do atributo começa com &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="49656-210">A string attribute, but is included only if the attribute value begins with &quot;tel:&quot;.</span></span> <span data-ttu-id="49656-211">Isso é principalmente para atributos de cadeia de caracteres de vários valores, especificamente <strong>proxyAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="49656-211">This is primarily for multi-valued string attributes, specifically <strong>proxyAddresses</strong>.</span></span> <span data-ttu-id="49656-212">Nesse caso, o servidor de catálogo de endereços está interessado apenas em entradas <strong>proxyAddresses</strong> que começam com &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="49656-212">In this case, Address Book Server is interested only in <strong>proxyAddresses</strong> entries that begin with &quot;tel:&quot;.</span></span> <span data-ttu-id="49656-213">Portanto, no que se está economizando espaço, o duplicador de usuários armazena apenas as entradas que começam com &quot; Tel: &quot; .</span><span class="sxs-lookup"><span data-stu-id="49656-213">Therefore, in the interest of saving space, User Replicator stores only the entries that begin with &quot;tel:&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-214">0x3</span><span class="sxs-lookup"><span data-stu-id="49656-214">0x3</span></span></p></td>
<td><p><span data-ttu-id="49656-215">Um atributo de cadeia de caracteres booliano, que se verdadeiro faz com que o duplicador de usuários não inclua esse contato na tabela AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="49656-215">A Boolean string attribute, which if TRUE causes User Replicator to not include this contact in the AbUserEntry table.</span></span> <span data-ttu-id="49656-216">Se falso, ele fará com que o duplicador de usuários inclua os atributos para esse contato na tabela AbUserEntry, mas não o atributo específico com esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="49656-216">If FALSE, it causes User Replicator to include the attributes for this contact in the AbUserEntry table, but not the particular attribute with this flag.</span></span> <span data-ttu-id="49656-217">Esse é outro tipo de caso especial que é principalmente para o atributo <strong>msExchHideFromAddressLists</strong> .</span><span class="sxs-lookup"><span data-stu-id="49656-217">This is another special case type that is primarily for the <strong>msExchHideFromAddressLists</strong> attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-218">0x4</span><span class="sxs-lookup"><span data-stu-id="49656-218">0x4</span></span></p></td>
<td><p><span data-ttu-id="49656-219">Um atributo String, mas está incluído apenas se o valor do atributo começa com &quot; SMTP: &quot; e inclui o &quot; @ &quot; símbolo.</span><span class="sxs-lookup"><span data-stu-id="49656-219">A string attribute, but is included only if the attribute value begins with &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-220">0x5</span><span class="sxs-lookup"><span data-stu-id="49656-220">0x5</span></span></p></td>
<td><p><span data-ttu-id="49656-221">Um atributo String, mas está incluído apenas se o valor do atributo começa com &quot; Tel: &quot; ou &quot; SMTP: &quot; e inclui o &quot; @ &quot; símbolo.</span><span class="sxs-lookup"><span data-stu-id="49656-221">A string attribute, but is included only if the attribute value begins with either &quot;tel:&quot; or &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-222">0x100</span><span class="sxs-lookup"><span data-stu-id="49656-222">0x100</span></span></p></td>
<td><p><span data-ttu-id="49656-223">Se definido, é um atributo de valores múltiplos que pode aparecer mais de uma vez para cada contato.</span><span class="sxs-lookup"><span data-stu-id="49656-223">If set, this is a multi-valued attribute that can appear more than once for each contact.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-224">0x400</span><span class="sxs-lookup"><span data-stu-id="49656-224">0x400</span></span></p></td>
<td><p><span data-ttu-id="49656-225">Se definido, identifica o atributo de nome da conta de usuário de email de um contato.</span><span class="sxs-lookup"><span data-stu-id="49656-225">If set, this identifies the email user account name attribute for a contact.</span></span> <span data-ttu-id="49656-226">O servidor de catálogo de endereços usa esse sinalizador para identificar o valor de atributo a ser mostrado na entrada do log de eventos de normalização do telefone.</span><span class="sxs-lookup"><span data-stu-id="49656-226">Address Book Server uses this flag to identify which attribute value to show in the phone normalization event log entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-227">0x800</span><span class="sxs-lookup"><span data-stu-id="49656-227">0x800</span></span></p></td>
<td><p><span data-ttu-id="49656-228">Se definido, identifica um atributo obrigatório para um contato.</span><span class="sxs-lookup"><span data-stu-id="49656-228">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="49656-229">O servidor de catálogo de endereços inclui um usuário na tabela AbUserEntry somente se houver um valor para esse atributo no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="49656-229">Address Book Server includes a user in the AbUserEntry table only if there is a value for this attribute in Active Directory.</span></span> <span data-ttu-id="49656-230">Se houver mais de um atributo obrigatório, apenas um deles será necessário para incluir um valor para incluir o usuário na tabela AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="49656-230">If there is more than one required attribute, only one of them is required to have a value to include the user in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-231">0x1000</span><span class="sxs-lookup"><span data-stu-id="49656-231">0x1000</span></span></p></td>
<td><p><span data-ttu-id="49656-232">Se definido, o servidor do catálogo de endereços sempre normalizará o valor desse atributo.</span><span class="sxs-lookup"><span data-stu-id="49656-232">If set, Address Book Server always normalizes the value of this attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-233">0x2000</span><span class="sxs-lookup"><span data-stu-id="49656-233">0x2000</span></span></p></td>
<td><p><span data-ttu-id="49656-234">Se definido, o servidor do catálogo de endereços usará o número normalizado do <strong>proxyAddresses</strong>, se a configuração de CMS do <strong>UseNormalizationRules</strong> for falsa; caso contrário, ele se comporta como quando o bit do sinalizador é 0x1000.</span><span class="sxs-lookup"><span data-stu-id="49656-234">If set, Address Book Server uses the normalized number from <strong>proxyAddresses</strong>, if the <strong>UseNormalizationRules</strong> CMS setting is FALSE; otherwise it behaves the same as when the flag bit is 0x1000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-235">0x4000</span><span class="sxs-lookup"><span data-stu-id="49656-235">0x4000</span></span></p></td>
<td><p><span data-ttu-id="49656-236">Se definido, o servidor de catálogo de endereços não inclui objetos na tabela AbUserEntry que têm esse valor para o atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="49656-236">If set, Address Book Server does not include objects in the AbUserEntry table that have this value for the specified attribute.</span></span> <span data-ttu-id="49656-237">Por exemplo, se o atributo <strong>msRTCSIP-PrimaryUserAddress</strong> tiver esse conjunto de bits de sinalizador, os contatos que tiverem esse atributo não serão gravados no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49656-237">For example, if the <strong>msRTCSIP-PrimaryUserAddress</strong> attribute has this flag bit set, then contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-238">0x8000</span><span class="sxs-lookup"><span data-stu-id="49656-238">0x8000</span></span></p></td>
<td><p><span data-ttu-id="49656-239">Se definido, o servidor de catálogo de endereços não inclui objetos na tabela AbUserEntry que não têm esse valor para o atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="49656-239">If set, Address Book Server does not include objects in the AbUserEntry table that do not have this value for the specified attribute.</span></span> <span data-ttu-id="49656-240">Se os bits de sinalizador 0x4000 e 0x8000 estiverem definidos em um objeto, o atributo com o valor de bit de sinalizador definido como 0x4000 terá precedência, e o objeto será excluído da tabela AbUserEntry.</span><span class="sxs-lookup"><span data-stu-id="49656-240">If both the 0x4000 and 0x8000 flag bits are set on an object, the attribute with the flag bit value set to 0x4000 takes precedence, and the object is excluded from the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-241">0x10000</span><span class="sxs-lookup"><span data-stu-id="49656-241">0x10000</span></span></p></td>
<td><p><span data-ttu-id="49656-242">Se definido, representa um objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="49656-242">If set, this represents a group object.</span></span> <span data-ttu-id="49656-243">O duplicador de usuários usa esse bit de sinalizador para incluir contatos com o atributo <strong>GroupType</strong> cuja presença indica um grupo (por exemplo, uma lista de distribuição ou um grupo de segurança).</span><span class="sxs-lookup"><span data-stu-id="49656-243">User Replicator uses this flag bit to include contacts with the <strong>groupType</strong> attribute whose presence indicates a group (for example, a distribution list or security group).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-244">0x20000</span><span class="sxs-lookup"><span data-stu-id="49656-244">0x20000</span></span></p></td>
<td><p><span data-ttu-id="49656-245">Se definido, o duplicador de usuários usa esse bit de sinalizador para incluir esse atributo em arquivos de servidor de catálogo de endereços específicos do dispositivo (ou seja, arquivos com extensão. dabs).</span><span class="sxs-lookup"><span data-stu-id="49656-245">If set, User Replicator uses this flag bit to include this attribute in device-specific Address Book Server files (that is, files with a .dabs extension).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49656-246">Em versões anteriores do Lync Server, ao aplicar uma alteração ao Active Directory, o administrador seria obrigado a executar **Update-CSUserDatabase** e **Update-CSAddressBook** cmdlets do Windows PowerShell para persistir a alteração para o banco de dados de usuários do Lync Server e para RTCab o banco de dados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="49656-246">In previous versions of Lync Server, when applying a change to Active Directory, the administrator would be required to run **Update -CSUserDatabase** and **Update –CSAddressBook** Windows PowerShell cmdlets to persist the change to the Lync Server user database and RTCab database immediately.</span></span> <span data-ttu-id="49656-247">No Lync Server 2013, o duplicador de usuários do Lync Server atenderá as alterações do Active Directory e atualizará o banco de dados de usuários do Lync Server com base em um intervalo configurado.</span><span class="sxs-lookup"><span data-stu-id="49656-247">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="49656-248">O duplicador de usuários do Lync Server também propagará as alterações para o banco de dados do RTCab rapidamente, sem que o administrador tenha que executar Update-CSAddressBook.</span><span class="sxs-lookup"><span data-stu-id="49656-248">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="49656-249">Se a consulta da Web do catálogo de endereços estiver habilitada, as alterações serão refletidas nos resultados da pesquisa pelos clientes do Lync.</span><span class="sxs-lookup"><span data-stu-id="49656-249">If Address Book Web query is enabled, then the changes will be reflected in search results by Lync clients.</span></span> <span data-ttu-id="49656-250">Os administradores só precisarão executar Update-CSAddressBook se o download do arquivo do catálogo de endereços estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="49656-250">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49656-251">Por padrão, o duplicador de usuários do Lync Server é executado automaticamente a cada 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="49656-251">By default Lync Server User Replicator runs automatically every 5 minutes.</span></span> <span data-ttu-id="49656-252">Você pode configurar esse intervalo usando Set-CSUserReplicatorConfiguration-ReplicationCycleInterval &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="49656-252">You can configure this interval by using Set -CSUserReplicatorConfiguration -ReplicationCycleInterval &lt;&gt;.</span></span>



</div>

</div>

<div>

## <a name="filtering-the-address-book"></a><span data-ttu-id="49656-253">Filtrando o catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="49656-253">Filtering the Address Book</span></span>

<span data-ttu-id="49656-254">Os usuários preenchidos nos arquivos do servidor do catálogo de endereços podem ser controlados com base em determinados atributos dos serviços de domínio Active Directory listados na tabela AbAttribute.</span><span class="sxs-lookup"><span data-stu-id="49656-254">The users populated in the Address Book Server files can be controlled based on certain Active Directory Domain Services attributes listed in the AbAttribute table.</span></span> <span data-ttu-id="49656-255">Um atributo desse tipo usado para a filtragem é o atributo **msExchangeHideFromAddressBook** .</span><span class="sxs-lookup"><span data-stu-id="49656-255">One such attribute used for filtering is the **msExchangeHideFromAddressBook** attribute.</span></span> <span data-ttu-id="49656-256">Esse é um atributo de usuário adicionado pelo esquema do Exchange.</span><span class="sxs-lookup"><span data-stu-id="49656-256">This is a user attribute added by the Exchange schema.</span></span> <span data-ttu-id="49656-257">Se o valor desse atributo for TRUE, o Exchange Server usará esse atributo para ocultar o contato da GAL (lista de endereços global) do Outlook.</span><span class="sxs-lookup"><span data-stu-id="49656-257">If the value of this attribute is TRUE, Exchange Server uses this attribute to hide the contact from the Outlook Global Address List (GAL).</span></span> <span data-ttu-id="49656-258">Da mesma forma, se o valor desse atributo for TRUE, o Duplicador do usuário não incluirá esse usuário na tabela AbUserEntry e esse usuário não estará nos arquivos do servidor do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="49656-258">Similarly, if the value of this attribute is TRUE, User Replicator does not include that user in the AbUserEntry table and this user will not be in the Address Book Server files.</span></span>

<span data-ttu-id="49656-259">Você pode usar alguns bits de sinalizador para definir um filtro a ser usado nos atributos do servidor do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="49656-259">You can use some flag bits to define a filter to use on Address Book Server attributes.</span></span> <span data-ttu-id="49656-260">Por exemplo, a presença de determinados bits de sinalizador pode identificar um atributo como um atributo Include ou um atributo Exclude.</span><span class="sxs-lookup"><span data-stu-id="49656-260">For example, the presence of certain flag bits can identify an attribute as an include attribute or an exclude attribute.</span></span> <span data-ttu-id="49656-261">O duplicador de usuários filtra os contatos que contêm um atributo de exclusão e filtra os contém que não contêm um atributo include.</span><span class="sxs-lookup"><span data-stu-id="49656-261">User Replicator filters out contacts that contain an exclude attribute and filters out contains that do not contain an include attribute.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="49656-262">Para obter mais informações sobre como filtrar o catálogo de endereços, consulte <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">cmdlets do servidor do catálogo de endereços no Lync Server 2013</A>e <A href="https://go.microsoft.com/fwlink/?linkid=330430">Filtrar catálogo de endereços do Lync 2013</A></span><span class="sxs-lookup"><span data-stu-id="49656-262">For more information about filtering the Address Book, see <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">Address Book Server cmdlets in Lync Server 2013</A>, and <A href="https://go.microsoft.com/fwlink/?linkid=330430">Filter Lync 2013 address book</A></span></span>



</div>

<span data-ttu-id="49656-263">Atualmente, há três filtros diferentes.</span><span class="sxs-lookup"><span data-stu-id="49656-263">Currently, there are three different filters.</span></span> <span data-ttu-id="49656-264">A tabela a seguir lista esses filtros.</span><span class="sxs-lookup"><span data-stu-id="49656-264">The following table lists these filters.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49656-265">Atributo</span><span class="sxs-lookup"><span data-stu-id="49656-265">Attribute</span></span></th>
<th><span data-ttu-id="49656-266">Descrição</span><span class="sxs-lookup"><span data-stu-id="49656-266">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49656-267">0x800</span><span class="sxs-lookup"><span data-stu-id="49656-267">0x800</span></span></p></td>
<td><p><span data-ttu-id="49656-268">Se definido, identifica um atributo obrigatório para um contato.</span><span class="sxs-lookup"><span data-stu-id="49656-268">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="49656-269">O duplicador de usuários usa este bit de sinalizador para filtrar os contatos que não contêm pelo menos um atributo obrigatório.</span><span class="sxs-lookup"><span data-stu-id="49656-269">User Replicator uses this flag bit to filter out contacts that do not contain at least one required attribute.</span></span> <span data-ttu-id="49656-270">O OuPathId é um atributo obrigatório, que é sempre definido.</span><span class="sxs-lookup"><span data-stu-id="49656-270">The OuPathId is a required attribute, which is always set.</span></span> <span data-ttu-id="49656-271">Portanto, pelo menos um dos outros atributos obrigatórios deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="49656-271">So at least one of other required attributes should be set.</span></span> <span data-ttu-id="49656-272">Caso contrário, o contato (ou seja, com o valor do atributo obrigatório OuPathId) ainda não será gravado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49656-272">Otherwise, contact (that is, with value of required attribute OuPathId) will still not be written to database.</span></span> <span data-ttu-id="49656-273">Por exemplo, se <strong>telephoneNumber</strong> e <strong>homePhone</strong> forem definidos como atributos obrigatórios, somente os contatos que tiverem pelo menos um desses atributos serão gravados no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49656-273">For example, if <strong>telephoneNumber</strong> and <strong>homePhone</strong> are defined as required attributes, only the contacts that have at least one of these attributes are written to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49656-274">0x4000</span><span class="sxs-lookup"><span data-stu-id="49656-274">0x4000</span></span></p></td>
<td><p><span data-ttu-id="49656-275">Se definido, identifica um atributo de exclusão.</span><span class="sxs-lookup"><span data-stu-id="49656-275">If set, this identifies an exclude attribute.</span></span> <span data-ttu-id="49656-276">O duplicador de usuários usa esse sinal bit para filtrar os contatos que contêm esse atributo.</span><span class="sxs-lookup"><span data-stu-id="49656-276">User Replicator uses this flag bit to filter out contacts that contain this attribute.</span></span> <span data-ttu-id="49656-277">Por exemplo, se <strong>msRTCSIP-PrimaryUserAddress</strong> for definido como um atributo Exclude, os contatos que tiverem esse atributo não serão gravados no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49656-277">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an exclude attribute, contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49656-278">0x8000</span><span class="sxs-lookup"><span data-stu-id="49656-278">0x8000</span></span></p></td>
<td><p><span data-ttu-id="49656-279">Se definido, isso identifica um atributo include.</span><span class="sxs-lookup"><span data-stu-id="49656-279">If set, this identifies an include attribute.</span></span> <span data-ttu-id="49656-280">O duplicador de usuários usa este bit de sinalizador para filtrar os contatos que não contêm esse atributo.</span><span class="sxs-lookup"><span data-stu-id="49656-280">User Replicator uses this flag bit to filter out contacts that do not contain this attribute.</span></span> <span data-ttu-id="49656-281">Por exemplo, se <strong>msRTCSIP-PrimaryUserAddress</strong> for definido como um atributo Include, somente os contatos que tiverem esse atributo serão gravados no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49656-281">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an include attribute, only the contacts that have this attribute are written to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="49656-282">Se os bits de sinalizador 0x4000 (Exclude Attribute) e 0x8000 (include Attribute) estiverem definidos, o bit 0x4000 substituirá o bit 0x8000 e o contato será excluído.</span><span class="sxs-lookup"><span data-stu-id="49656-282">If both the 0x4000 (exclude attribute) and 0x8000 (include attribute) flag bits are set, the 0x4000 bit overrides the 0x8000 bit and the contact is excluded.</span></span>



</div>

<span data-ttu-id="49656-283">Embora você possa filtrar o catálogo de endereços para incluir apenas determinados usuários, limitar as entradas não limita a capacidade dos outros usuários de entrar em contato com os usuários filtrados ou ver o status de presença deles.</span><span class="sxs-lookup"><span data-stu-id="49656-283">Although you can filter the Address Book to include only certain users, limiting entries does not limit other users' ability to contact the filtered users or to see their presence status.</span></span> <span data-ttu-id="49656-284">Os usuários sempre podem localizar, enviar manualmente mensagens de chat ou iniciar manualmente chamadas para usuários que não estão no catálogo de endereços inserindo um nome de entrada completo do usuário.</span><span class="sxs-lookup"><span data-stu-id="49656-284">Users can always find, manually send instant messages, or manually initiate calls to users not in the Address Book by entering a user's complete sign-in name.</span></span> <span data-ttu-id="49656-285">Além disso, as informações de contato para um usuário também podem ser encontradas no Outlook.</span><span class="sxs-lookup"><span data-stu-id="49656-285">Also, contact information for a user could also be found in Outlook.</span></span>

<span data-ttu-id="49656-286">Embora tenha registros de contatos completos nos arquivos do catálogo de endereços, você pode usar o Lync Server para iniciar chamadas de email, de telefone ou de voz empresarial (ou seja, se o Enterprise Voice estiver habilitado no servidor) com usuários que não estão configurados para o protocolo SIP, algumas organizações preferem incluir somente usuários habilitados para SIP nas entradas do servidor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="49656-286">While having full contact records in the Address Book files enables you to use Lync Server to initiate email, telephone, or Enterprise Voice calls (that is, if Enterprise Voice is enabled on the server) with users that are not configured for Session Initiation Protocol (SIP), some organizations prefer to include only SIP-enabled users in their Address Book Server entries.</span></span> <span data-ttu-id="49656-287">Você pode filtrar o catálogo de endereços para incluir somente usuários habilitados para SIP, desmarcando o bit 0x800 na coluna **sinalizadores** dos seguintes atributos obrigatórios: **mailNickname**, **telephoneNumber**, **homePhone** e **celular**.</span><span class="sxs-lookup"><span data-stu-id="49656-287">You can filter the Address Book to include only SIP-enabled users by clearing the 0x800 bit in the **Flags** column of the following required attributes: **mailNickname**, **telephoneNumber**, **homePhone**, and **mobile**.</span></span> <span data-ttu-id="49656-288">Você também pode filtrar o catálogo de endereços para incluir somente usuários habilitados para SIP definindo o 0x8000 (include Attribute) na coluna **flags** do atributo **msRTCSIP-PrimaryUserAddress** .</span><span class="sxs-lookup"><span data-stu-id="49656-288">You can also filter the Address Book to include only SIP-enabled users by setting the 0x8000 (include attribute) in the **Flags** column of the **msRTCSIP-PrimaryUserAddress** attribute.</span></span> <span data-ttu-id="49656-289">Isso também ajuda a excluir contas de serviço dos arquivos do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="49656-289">This also helps to exclude service accounts from the Address Book files.</span></span>

<span data-ttu-id="49656-290">Depois de modificar a tabela AbAttribute, você pode atualizar os dados na tabela AbUserEntry executando o comando **Update-CsUserDatabase** do cmdlet Update.</span><span class="sxs-lookup"><span data-stu-id="49656-290">After you modify the AbAttribute table, you can refresh the data in the AbUserEntry table by running the cmdlet **Update-CsUserDatabase** command.</span></span> <span data-ttu-id="49656-291">Após a conclusão da replicação UR, você pode atualizar o arquivo no repositório de arquivos do servidor do catálogo de endereços executando manualmente o comando cmdlet **UpdateCsAddressBook** .</span><span class="sxs-lookup"><span data-stu-id="49656-291">After UR replication completes, you can update the file in the Address Book Server file store by manually running the cmdlet **UpdateCsAddressBook** command.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49656-292">O servidor front-end no qual o servidor do catálogo de endereços não é configurado administrativamente.</span><span class="sxs-lookup"><span data-stu-id="49656-292">The Front End Server that the Address Book Server is placed is not administratively configurable.</span></span> <span data-ttu-id="49656-293">Um é escolhido durante a implantação — geralmente, o primeiro servidor de front-end implantado.</span><span class="sxs-lookup"><span data-stu-id="49656-293">One is chosen during deployment—typically, the first Front End Server deployed.</span></span> <span data-ttu-id="49656-294">Em caso de falha, o serviço de catálogo de endereços passará para outro servidor front-end e não exigirá atenção administrativa.</span><span class="sxs-lookup"><span data-stu-id="49656-294">In the event of failure, the Address Book Service will move to another Front End Server, and requires no administrative attention.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="49656-295">Se você consolidou ou modificou sua infraestrutura de uma implantação de várias florestas ou de uma implantação pai/filho (como consolidar sua infraestrutura antes de migrar para o Lync Server), talvez descubra que o download do serviço de catálogo de endereços e a consulta à Web do catálogo de endereços falham para alguns usuários.</span><span class="sxs-lookup"><span data-stu-id="49656-295">If you have consolidated or otherwise modified your infrastructure from a multi-forest deployment or a parent/child deployment (such as consolidating your infrastructure before moving to Lync Server), you may find that the Address Book service download and the Address Book Web Query fails for some users.</span></span> <span data-ttu-id="49656-296">Quando em uma implantação que tinha vários domínios ou florestas, o atributo <STRONG>MsRTCSIP-OriginatorSid</STRONG> é preenchido nos objetos de usuário que estão apresentando o problema.</span><span class="sxs-lookup"><span data-stu-id="49656-296">When in a deployment that had multiple domains or forests, the attribute <STRONG>MsRTCSIP-OriginatorSid</STRONG> is populated on the user objects that are exhibiting the issue.</span></span> <span data-ttu-id="49656-297">O atributo <STRONG>MsRTCSIP-OriginatorSid</STRONG> deve ser definido como NULL nesses objetos para resolver o problema.</span><span class="sxs-lookup"><span data-stu-id="49656-297">The <STRONG>MsRTCSIP-OriginatorSid</STRONG> attribute must be set to NULL on these objects to resolve the issue.</span></span>



<span data-ttu-id="49656-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49656-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

