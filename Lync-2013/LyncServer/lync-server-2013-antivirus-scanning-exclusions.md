---
title: 'Lync Server 2013: Exclusões de verificação de antivírus'
description: 'Lync Server 2013: exclusões de verificação antivírus.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440658"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a>Exclusões de verificação de antivírus para Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2015-11-02_

Para garantir que o scanner antivírus não interfira com a operação do Lync Server 2013, você deve excluir processos e pastas específicos para cada função de servidor ou servidor do Lync Server 2013 na qual você executa um verificador de vírus. Os seguintes processos e diretórios devem ser excluídos:

<div>


> [!NOTE]  
> Os locais de pasta e arquivo listados abaixo são os locais padrão do Lync Server 2013. Para quaisquer locais, para os quais você não usa o padrão, exclua os locais que você especificou para a sua organização em vez dos locais padrão especificados neste tópico.



</div>

<div>


> [!IMPORTANT]  
> Observe que alguns programas antivírus podem precisar de caminhos absolutos e não relativos, para a sua lista de exclusão.



</div>

  - Processos do Lync Server 2013:
    
      - ABServer.exe
    
      - AcpMcuSvc.exe
    
      - ASMCUSvc.exe
    
      - AVMCUSvc.exe
    
      - ChannelService.exe
    
      - ClsAgent.exe
    
      - ComplianceService.exe
    
      - DataMCUSvc.exe
    
      - DataProxy.exe
    
      - FileTransferAgent.exe
    
      - IMMCUSvc.exe
    
      - LysSvc.exe
    
      - MasterReplicatorAgent.exe
    
      - MediaRelaySvc.exe
    
      - MediationServerSvc.exe
    
      - MRASSvc.exe
    
      - OcsAppServerHost.exe
    
      - ReplicaReplicatorAgent.exe
    
      - ReplicationApp.exe
    
      - RtcHost.exe
    
      - RTCSrv.exe
    
      - XmppProxy.exe
    
      - XmppTGW.exe

  - Processos de Serviço de Host do Windows Fabric:
    
      - Fabric.exe
    
      - FabricDCA.exe
    
      - FabricHost.exe

  - Processos IIS:
    
      - % SystemRoot% \\ System32 \\ inetsrv \\w3wp.exe
    
      - % SystemRoot% \\ SysWOW64 \\ inetsrv \\w3wp.exe

  - Processos SQL Server Back-End:
    
      - % ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. MSSQLSERVER \\ MSSQL \\ Binn \\SQLServr.exe
    
      - % ProgramFiles% \\ Microsoft SQL Server \\ MSRS11. O \\ Reporting Services \\ ReportServer \\ bin \\ReportingServicesService.exe
    
      - % ProgramFiles% \\ Microsoft SQL Server \\ MSAS11.MSMDSrv.exe da lixeira do MSSQLSERVER \\ OLAP \\ \\

  - Processos SQL Server Front-End:
    
      - % ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. LYNCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe
    
      - % ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. RTCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe

  - Diretórios e arquivos:
    
      - % SystemRoot% \\ System32 \\ LogFiles
    
      - % SystemRoot% \\ SysWOW64 \\ LogFiles
    
      - % SystemRoot% \\ Microsoft.NET \\ assembly \\ GAC \_ MSIL
    
      - % ProgramFiles% \\ Microsoft Lync Server 2013
    
      - % ProgramFiles% \\ Arquivos comuns \\ \\ nó do Inspetor do Microsoft Lync Server 2013
    
      - % ProgramFiles% \\ Arquivos comuns \\ Microsoft Lync Server 2013
    
      - % SystemDrive% \\ RtcReplicaRoot
    
      - Repositório de compartilhamento de arquivo(específico no Construtor de Topologias). Os repositórios de arquivos são especificados no Construtor de Topologias.
    
      - Os arquivos de logs e dados do SQL Server, incluindo aqueles para o banco de dados de back-end, armazenamento de usuário, arquivamento, monitoramento, e repositório de application. Os arquivos da base de dados e os logs podem ser especificados no Construtor de Topologias. Para obter detalhes sobre os dados e arquivos de log para cada banco de dados, incluindo nomes padrão, consulte [dados do SQL Server e posicionamento do arquivo de log para o Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) na documentação de implantação.
    
      - Dados e arquivos de log do SQL Server, incluindo aqueles para o banco de dados front-end, a loja do Lync e a loja do RtcDatabase. Eles estão normalmente em% Unidade_Local% \\ CSData.

</div>

<span> </span>

</div>

</div>

</div>

