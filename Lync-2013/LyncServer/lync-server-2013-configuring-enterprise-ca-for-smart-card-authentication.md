---
title: 'Lync Server 2013: Configurando a CA empresarial para autenticação de cartão inteligente'
description: 'Lync Server 2013: Configurando a CA empresarial para autenticação de cartão inteligente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise CA for smart card authentication
ms:assetid: c24e0891-e108-4cb6-9902-c6a4c8e68455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308571(v=OCS.15)
ms:contentKeyID: 54973692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98044c96dd04d02fd87609918f309cf65227b133
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433147"
---
# <a name="configuring-enterprise-ca-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="09fe0-103">Configurando a CA corporativa para autenticação de cartão inteligente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09fe0-103">Configuring Enterprise CA for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09fe0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09fe0-104">

<span> </span></span></span>

<span data-ttu-id="09fe0-105">_**Tópico da última modificação:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="09fe0-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="09fe0-106">A seção a seguir descreve como configurar uma CA (autoridade de certificação) raiz corporativa para dar suporte à autenticação de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="09fe0-106">The following section describes how to configure an Enterprise Root Certification Authority (CA) to support smart card authentication.</span></span> <span data-ttu-id="09fe0-107">Para obter informações sobre como instalar uma autoridade de certificação raiz corporativa, consulte instalar uma autoridade de certificação raiz corporativa em [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364) .</span><span class="sxs-lookup"><span data-stu-id="09fe0-107">For information on how to install an Enterprise Root CA, see Install an Enterprise Root Certification Authority at [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364).</span></span>

<div>

## <a name="configuring-an-enterprise-root-certificate-authority-to-support-smart-card-authentication"></a><span data-ttu-id="09fe0-108">Configurando uma autoridade de certificação raiz corporativa para dar suporte à autenticação de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="09fe0-108">Configuring an Enterprise Root Certificate Authority to Support Smart Card Authentication</span></span>

<span data-ttu-id="09fe0-109">As seguintes etapas descrevem como configurar uma CA Raiz Corporativa para dar suporte à Autenticação de Cartão Inteligente:</span><span class="sxs-lookup"><span data-stu-id="09fe0-109">The following steps describe how to configure an Enterprise Root CA to support Smart Card Authentication:</span></span>

1.  <span data-ttu-id="09fe0-110">Faça o login no computador da AC corporativa utilizando uma conta de Administrador de Domínio.</span><span class="sxs-lookup"><span data-stu-id="09fe0-110">Log in to the Enterprise CA computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="09fe0-111">Inicie o Gerenciador de Sistema e verifique se a função de Registro da Web da Autoridade de Certificação está instalada.</span><span class="sxs-lookup"><span data-stu-id="09fe0-111">Launch System Manager, and verify that the Certificate Authority Web Enrollment role is installed.</span></span>

3.  <span data-ttu-id="09fe0-112">No menu **Ferramentas Administrativas**, abra o console de gerenciamento da **Autoridade de Certificação**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-112">From the **Administrative Tools** menu, open the **Certification Authority** management console.</span></span>

4.  <span data-ttu-id="09fe0-113">No painel de Navegação, expanda **Autoridade de Certificação**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-113">In the Navigation pane, expand **Certification Authority**.</span></span>

5.  <span data-ttu-id="09fe0-114">Clique com o botão direito do mouse em **Modelos de Certificado**, selecione **Novo** e, em seguida, selecione **Modelo de Certificação para Emissão**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-114">Right click on **Certificate Templates**, select **New**, then select **Certificate Template to Issue**.</span></span>

6.  <span data-ttu-id="09fe0-115">Selecione **Agente de Registro**, **Usuário do Cartão Inteligente** e **Logon do Cartão Inteligente**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-115">Select **Enrollment Agent**, **Smartcard User**, and **Smartcard Logon**.</span></span>

7.  <span data-ttu-id="09fe0-116">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-116">Click **OK**.</span></span>

8.  <span data-ttu-id="09fe0-117">Clique com o botão direito em **Modelos de Certificado**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-117">Right click on **Certificate Templates**.</span></span>

9.  <span data-ttu-id="09fe0-118">Selecione **Gerenciar**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-118">Select **Manage**.</span></span>

10. <span data-ttu-id="09fe0-119">Abra as propriedades do modelo do Usuário do Cartão Inteligente.</span><span class="sxs-lookup"><span data-stu-id="09fe0-119">Open the properties of the Smartcard User template.</span></span>

11. <span data-ttu-id="09fe0-120">Clique na guia **Segurança**.</span><span class="sxs-lookup"><span data-stu-id="09fe0-120">Click on the **Security** tab.</span></span>

12. <span data-ttu-id="09fe0-121">Altere as permissões da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="09fe0-121">Change the permissions as follows:</span></span>
    
      - <span data-ttu-id="09fe0-122">Adicione contas de AD de usuários individuais com permissões para Ler/Registrar (Permitir) ou</span><span class="sxs-lookup"><span data-stu-id="09fe0-122">Add individual user AD accounts with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="09fe0-123">Adicione um grupo de segurança contendo usuários do cartão inteligente com permissões para Ler/Registrar (Permitir), ou</span><span class="sxs-lookup"><span data-stu-id="09fe0-123">Add a security group containing smart card users with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="09fe0-124">Adicione o grupo do Usuário de Domínio com as permissões para Ler/Registrar (Permitir)</span><span class="sxs-lookup"><span data-stu-id="09fe0-124">Add the Domain Users group with Read/Enroll (Allow) permissions</span></span>

<span data-ttu-id="09fe0-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09fe0-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

