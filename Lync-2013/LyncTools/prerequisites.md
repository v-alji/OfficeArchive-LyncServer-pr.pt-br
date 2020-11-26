---
title: Pré-requisitos
description: Pré-requisitos.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prerequisites
ms:assetid: 48016bea-be3b-4ba5-8df8-d8ad4d9243d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945592(v=OCS.15)
ms:contentKeyID: 51541417
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 936e52961539ed57fe1b610d42fb1c9cf35589b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446401"
---
# <a name="prerequisites"></a>Pré-requisitos

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-02-19_

Há vários requisitos de configuração de hardware, software e sistema que você precisará para executar a ferramenta de stress e desempenho do Lync Server 2013.

<div>

## <a name="client-hardware-requirements"></a>Requisitos de hardware do cliente

Para executar a ferramenta de stress e desempenho do Lync Server 2013 na sua implantação do Lync Server 2013 para cada usuário do 4.500 cuja carga você deseja simular, é preciso ter pelo menos um computador dedicado que atenda aos seguintes requisitos mínimos de hardware:

  - Adaptador rede de 1 gigabit

  - 8 GB de RAM

  - 2 unidades de processamento central de Dual-Core (CPUs)

</div>

<div>

## <a name="client-software-requirements"></a>Requisitos de software do cliente

Para executar a ferramenta de stress e desempenho do Lync Server 2013 em sua implantação do Lync Server 2013, os sistemas operacionais com suporte são:

  - Sistema operacional Windows Server 2012

  - Sistema operacional Windows Server 2008 (edição de 64 bits)

O computador cliente deve atender aos seguintes requisitos de software:

  - Você deve ter o [Microsoft .NET Framework 4,5](https://go.microsoft.com/fwlink/?linkid=143212) Runtime instalado.

  - No Windows Server 2008/Windows Server 2012, o recurso experiência da área de trabalho deve ser habilitado.

  - Você deve ter instalado o [pacote redistribuível do Microsoft Visual C++ 2012](https://go.microsoft.com/fwlink/?linkid=143216) (x64).

  - Uma implantação totalmente configurada do Lync Server 2013.

<div>


> [!IMPORTANT]  
> As bibliotecas da API gerenciada de comunicação unificada da Microsoft (UCMA) 4,0 estão incluídas no pacote de instalação, portanto, o UCMA não é necessário e não deve ser instalado em computadores cliente.



</div>

</div>

<div>

## <a name="configuration-requirements"></a>Requisitos de configuração

Os computadores que executarão a ferramenta de stress e desempenho do Lync Server 2013 devem ser configurados de acordo com os seguintes requisitos:

1.  Você deve estar conectado como um membro do grupo domínio ou administradores locais.

2.  A ferramenta de stress e desempenho do Lync Server 2013 (LyncPerfTool.exe) não pode ser executada em um computador que também esteja executando os componentes do Lync Server 2013.

3.  Você deve executar a ferramenta de criação de usuários do Lync Server 2013 (UserProvisioningTool.exe) no servidor front-end ou no servidor Standard Edition, onde as contas de usuário residem. Quando a ferramenta é executada várias vezes, cada usuário habilitado para a comunicação unificada da Microsoft deve ter um número de telefone exclusivo.

4.  O tamanho do arquivo da página deve ser gerenciado pelo sistema ou deve ter pelo menos 1,5 vezes a quantidade de RAM no sistema.

</div>

</div>

<span> </span>

</div>

</div>

</div>

