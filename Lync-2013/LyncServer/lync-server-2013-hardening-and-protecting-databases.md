---
title: 'Lync Server 2013: Protegendo os bancos de dados'
description: 'Lync Server 2013: proteção e proteção de bancos de dados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hardening and protecting the databases of Lync Server 2013
ms:assetid: 6953e721-3511-4235-b848-51bab093dc89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518330(v=OCS.15)
ms:contentKeyID: 62625490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af1ed8f54384e8ecac3b1e4ce6a4253a10bcc2c6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427758"
---
# <a name="hardening-and-protecting-the-databases-of-lync-server-2013"></a>Protegendo os bancos de dados do Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2013-12-05_

O Microsoft Lync Server 2013 também depende dos bancos de dados do SQL Server para armazenar informações do usuário, o estado da conferência, os dados de arquivamento e os registros de detalhes da chamada (CDRs). Você pode maximizar a disponibilidade dos dados do Lync Server 2013 em bancos de dados back-end do Lync Server, Particionando os dados do aplicativo de forma a melhorar a tolerância a falhas e simplificar a solução de problemas. Para alcançar essas metas, Particione os dados do aplicativo:

  - **Usando as práticas recomendadas de particionamento do servidor**   Separe o sistema operacional, o aplicativo e os arquivos de programas dos seus arquivos de dados.

  - **Armazenando arquivos de log de transações e arquivos de banco de dados**   Armazene esses arquivos separadamente para aumentar a tolerância a falhas e otimizar a recuperação e armazená-los em um disco ou volume criptografado.

  - **Usar o agrupamento do servidor**   Cluster os servidores back-end para otimizar a disponibilidade do sistema do Lync Server 2013.

  - **Garantir que todos os backups de dados sejam criptografados e devidamente manipulados**   Uma mídia de backup perdida, descartada ou mal colocada pode representar uma ameaça significativa à segurança de dados para implantações do Lync Server 2013

Em qualquer servidor do Lync Server 2013, exceto o Standard Edition Server, a instância do SQL Server Express (instância RTCLOCAL) não é acessível remotamente, e nenhuma exceção de firewall local é criada, exceto para o SQL Server Express em um servidor Standard Edition. Em um servidor Standard Edition, o banco de dados back-end e o repositório de gerenciamento central (CMS) estão configurados para serem acessíveis remotamente. Para proteger bancos de dados do SQL Server, você pode fazer o seguinte:

  - Personalize o Firewall do SQL Server Express nos servidores do Standard Edition, limitando o escopo de servidores que podem acessar o banco de dados remotamente. Por padrão, qualquer endereço IP pode acessar remotamente o banco de dados.

  - Use o Gerenciador de configuração do SQL Server para especificar os protocolos, endereços IP e portas para o acesso remoto do SQL Server:
    
      - O Lync Server 2013 usa o protocolo TCP/IP. Ele dá suporte a IP versão 4 (IPv4), mas não IP versão 6 (IPv6).
        
        <div>
        

        > [!NOTE]  
        > O Lync Server 2013 pode funcionar em uma rede com a pilha de IP duplo habilitada.

        
        </div>
    
      - O Lync Server 2013 dá suporte a vários endereços IP (cartões de endereço de rede de hospedagem múltipla). Você pode especificar que o SQL Server escuta apenas em endereços IP específicos (endereço individual ou sub-rede) e usar somente protocolos específicos.
    
      - O Lync Server 2013 dá suporte a portas estáticas e dinâmicas do SQL Server.

  - Execute o SQL Server em uma porta estática (não padrão) e não execute o navegador do SQL Server (para que ele não possa relatar a porta de escuta para o cliente). Isso requer uma configuração personalizada em cada cliente do SQL Server, incluindo servidores de front-end, Monitoring Server, servidor de arquivamento e consoles administrativos (executando o Shell de gerenciamento do Lync Server, o painel de controle do Lync Server ou o construtor de topologias) e todos os outros servidores que executam bancos de dados do Lync Server).

<div>


> [!NOTE]  
> O acesso a bancos de dados deve estar limitado a administradores de banco de dados confiáveis. Um administrador de banco de dados mal-intencionado pode inserir ou modificar dados em bancos de dados para obter privilégios nos servidores do Lync Server 2013 ou obter informações confidenciais dos serviços, mesmo se o administrador do banco de dados não tiver sido concedido acesso direto ou controle dos servidores do Lync Server 2013.



</div>

Para obter detalhes sobre configurações personalizadas e proteção de bancos de dados do SQL Server, consulte o artigo sobre o blog NextHop, "usando o Lync Server 2010 com uma configuração de rede personalizada do SQL Server" em [https://go.microsoft.com/fwlink/p/?LinkId=214008](https://go.microsoft.com/fwlink/p/?linkid=214008) .

<div>


> [!NOTE]  
> Você também pode proteger sistemas operacionais e servidores de aplicativos, e pode usar a política de grupo para implementar bloqueios de segurança na implantação do Lync Server. Para obter detalhes, consulte <A href="lync-server-2013-hardening-and-protecting-servers-and-applications.md">protegendo e protegendo servidores e aplicativos para o Lync Server 2013</A>.



</div>

</div>

<span> </span>

</div>

</div>

</div>

