---
title: 'Lync Server 2013: Pré-requisitos do plug-in Lync VDI'
description: 'Lync Server 2013: pré-requisitos de plug-in VDI do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync VDI plug-in prerequisites
ms:assetid: da25a976-7624-4dfc-b332-9c4db4ee78da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205304(v=OCS.15)
ms:contentKeyID: 48185552
ms.date: 03/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4389f776747426d07442e29418ab97e9609de7ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426239"
---
# <a name="lync-vdi-plug-in-prerequisites-in-lync-server-2013"></a>Pré-requisitos do plug-in Lync VDI no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2017-03-07_

Em um ambiente da Virtual Desktop Infrastructure (VDI), as máquinas virtuais e o computador local do usuário devem atender aos requisitos descritos nesta seção.

<div>


> [!NOTE]  
> Consulte seu provedor de soluções de virtualização para obter detalhes sobre como instalar e implantar o ambiente virtualizado. Para obter informações sobre como implantar um ambiente virtualizado com base no Hyper-V e nos serviços de área de trabalho remota, consulte os seguintes artigos na biblioteca do Microsoft TechNet: 
> <UL>
> <LI>
> <P>Hyper-V em <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247514">https://go.microsoft.com/fwlink/p/?linkid=247514</A></P>
> <LI>
> <P>Serviços de área de trabalho remota no Windows Server &nbsp; 2008 &nbsp; R2 em <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247513">https://go.microsoft.com/fwlink/p/?linkid=247513</A></P></LI></UL>



</div>

Veja a seguir os requisitos para as máquinas virtuais em execução no computador do Data Center:

  - Máquinas virtuais devem ser configuradas com o Windows 10, o Windows 8,1, o Windows 8, o Windows 7 ou o Windows Server 2008 R2 com os service packs mais recentes.

Veja a seguir os requisitos para o usuário e o computador local do usuário:

  - O usuário deve ser hospedado no Lync Server 2013.

  - O computador local deve estar executando o Windows Embedded Standard 7 com SP1, o Windows 7 com SP1, o Windows 8, o Windows 8,1 Embedded ou o Windows 8,1 (não incorporado).

  - Se você estiver usando os serviços de área de trabalho remota, o bit de bits de plug-in do Lync da VDI (ou seja, se o aplicativo for 32 bits ou 64 bits) deve corresponder ao sistema operacional do sistema operacional do computador local. A bits do sistema operacional no computador local e o sistema operacional na máquina virtual não precisam ser correspondentes. Se você estiver usando outra solução ou plataforma de virtualização, consulte a orientação de seu provedor de soluções de virtualização sobre requisitos de bits.

  - O computador local deve estar executando a versão mais recente do cliente da área de trabalho remota. Instale as últimas atualizações do cliente de Serviços de Área de Trabalho Remota da Microsoft ou o software cliente de área de trabalho remota mais recente do seu provedor de soluções de virtualização. Para obter as atualizações mais recentes dos serviços de área de trabalho remota, consulte [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .

  - No computador local, as configurações do cliente de área de trabalho remota devem ser definidas para que o áudio seja reproduzido no computador local e a gravação remota seja desabilitada. Para definir essas configurações para a conexão de área de trabalho remota no Windows, consulte a próxima seção, "para definir as configurações de conexão de área de trabalho remota".

<div>

## <a name="to-configure-remote-desktop-connection-settings"></a>Para definir as configurações da conexão de área de trabalho remota

Para preparar a conexão de área de trabalho remota no Windows para o plug-in VDI do Lync, siga estas etapas.

1.  Se o computador local estiver executando o Windows 8, pule esta etapa. Se o computador local estiver executando o Windows 7 com SP1, instale a versão mais recente do Windows 8 do cliente dos serviços de área de trabalho remota, disponível em [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .

2.  Inicie o cliente de Serviços de Área de Trabalho Remota clicando em **Iniciar** e em **Conexão de Área de Trabalho Remota**.

3.  Clique em **Opções**.

4.  Clique na guia **Recursos Locais**. Em **Áudio remoto**, clique em **Configurações** e faça o seguinte:
    
      - Em **Reprodução de áudio remoto**, selecione **Reproduzir neste computador**.
    
      - Em **Gravação de áudio remoto**, selecione **Não gravar**.
    
      - Clique em **OK**.

5.  Clique na guia **Experiência**. Em **Desempenho**, desmarque a caixa de seleção **Armazenamento persistente de bitmaps em cache**.

6.  Clique na guia **geral** . Em **computador**, digite o nome da máquina virtual e, em seguida, clique em **conectar**.

</div>

</div>

<span> </span>

</div>

</div>

</div>

