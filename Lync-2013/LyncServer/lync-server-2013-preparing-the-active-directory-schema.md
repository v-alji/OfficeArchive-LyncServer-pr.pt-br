---
title: 'Lync Server 2013: Preparando o esquema do Active Directory'
description: 'Lync Server 2013: preparando o esquema do Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the Active Directory schema
ms:assetid: 067726ae-fd3f-4133-a32f-26d2603ac674
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398119(v=OCS.15)
ms:contentKeyID: 48183300
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3df7533dcbabe278fd366b441cfd8daa83f54b23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424106"
---
# <a name="preparing-the-active-directory-schema-in-lync-server-2013"></a>Preparando o esquema do Active Directory no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2012-08-27_

Antes de começar a preparar os serviços de domínio do Active Directory, você pode abrir os arquivos de esquema usando um editor de texto, como o bloco de notas do Windows, ou consulte [extensões de esquema, classes e atributos do Active Directory usados pelo Lync server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) para examinar todas as extensões de esquema de serviços de domínio do Active Directory que serão modificadas para o Lync Server 2013. O Lync Server usa quatro arquivos de esquema:

  - ExternalSchema. ldf, que é usado para interoperabilidade com o Microsoft Exchange Server

  - ServerSchema. ldf, que é o arquivo de esquema principal do Lync Server 2013

  - BackCompatSchema. ldf, que é usado para interoperabilidade com qualquer componente de versões anteriores

  - VersionSchema. ldf, que é usado para informações sobre a versão do esquema preparado

Todos os arquivos. ldf são instalados durante a preparação do esquema, independentemente de você estar migrando de uma versão anterior ou executando uma instalação limpa. Esses arquivos de esquema são instalados na sequência mostrada na lista anterior e estão localizados na \\ pasta de esquema de suporte \\ na mídia de instalação.

As extensões de esquema do Lync Server são replicadas em todos os domínios, o que afeta o tráfego de rede. Execute a preparação do esquema de cada vez quando o uso da rede for baixo.

<div>


> [!NOTE]  
> Se você precisar adicionar suporte para Microsoft® Office Communicator Mobile 2007 R2 para Java e Microsoft® Office Communicator Mobile para Nokia 1,0 para clientes móveis à implantação do Lync Server 2013, será necessário preparar o esquema do Active Directory para o Microsoft Office Communications Server 2007 R2 durante a instalação do Lync Server 2013. Para obter o software e a documentação necessários, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A> .



</div>

<div>

## <a name="adsi-edit"></a>Editar ADSI

O editor de interfaces de serviço do Active Directory (ADSI Edit) é uma ferramenta de administração do AD DS que você pode usar para verificar a preparação e a replicação do esquema.

O ADSI Edit é instalado por padrão quando você instala a função AD DS para fazer com que um servidor seja um controlador de domínio. Para Windows Server 2008 e Windows Server 2008 R2, o ADSI Edit (Adsiedit. msc) está incluído nas ferramentas de administração de servidor remoto (RSAT). Você também pode instalar o RSAT em servidores membro do domínio ou servidores autônomos. O pacote RSAT é copiado para esses servidores por padrão quando você instala o Windows, mas ele não é instalado por padrão. Você instala ferramentas individuais usando o Gerenciador de servidores. O ADSI Edit está incluído em **ferramentas de administração de funções**, ferramentas de serviços de **domínio Active Directory**, **ferramentas de controlador de domínio do Active Directory**.

Para o Windows Server 2003, o ADSI Edit está incluído nas ferramentas de suporte. As ferramentas de suporte estão disponíveis no CD do Windows Server 2003 na \\ \\ pasta ferramentas de suporte ou você pode baixá-las em "ferramentas de suporte do bit 2003 do windows Server Service Pack 2 32-bit" [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770) . Instruções para instalar as ferramentas de suporte do CD do produto estão disponíveis em "instalar ferramentas de suporte do Windows" em [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771) . O Adsiedit.dll é registrado automaticamente quando você instala as ferramentas de suporte. Se, no entanto, você copiou os arquivos para o seu computador, você deve executar o comando **regsvr32** para registrar o arquivo de adsiedit.dll antes de poder executar a ferramenta.

</div>

<div>

## <a name="in-this-section"></a>Nesta seção

  - [Executando preparação de esquema de Active Directory no Lync Server 2013](lync-server-2013-running-schema-preparation.md)

  - [Verificando a replicação de esquema do Active Directory no Lync Server 2013](lync-server-2013-verifying-schema-replication.md)

</div>

<div>

## <a name="see-also"></a>Confira também


[Preparando a floresta para Lync Server 2013](lync-server-2013-preparing-the-forest.md)  
[Preparando domínios para Server 2013](lync-server-2013-preparing-domains.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

