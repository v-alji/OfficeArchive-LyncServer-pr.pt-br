---
title: 'Lync Server 2013: Configuração de federação do Lync'
description: 'Lync Server 2013: Configurando a federação do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390326"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a>Configuração de federação do Lync no Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico Última Modificação:** 2014-03-27_

Se você já tiver implantado servidores ou servidores de Borda, a adição dos recursos de cenários federados será direta. Se você não tiver configurar Servidores de Borda, deverá fazer isso primeiro. Para obter detalhes, consulte: Planning for external [user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.

<div>


> [!NOTE]  
> Se você pretende configurar qualquer combinação de federação XMPP, Federação do Lync ou conectividade de mensagens instantâneas públicas, poderá implantá-las simultaneamente ou uma de cada vez. Se você configurar as opções por meio do Construtor de Topologias e do shell de Gerenciamento do Lync Server, execute o Assistente de Implantação no servidor de Borda depois de configurar as opções para um, dois ou todos os três tipos de federação, você poderá reduzir o número de etapas necessárias.



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>Configurando a Federação do Lync no Construtor de Topologias e no Assistente de Implantação

1.  Em um servidor Front-End, abra o Construtor de Topologias. Expanda pools de borda e clique com o botão direito do mouse em seu servidor de Borda ou pool de servidores de Borda. Selecione Editar propriedades.

2.  Em Editar Propriedades em Geral, selecione Habilitar federação para este pool de Borda (Porta 5061). Clique em OK.

3.  Clique em Ação, selecione Topologia, selecione Publicar. Quando solicitado em Publicar a topologia, clique em Next. Quando a Publicação for concluída, clique em Concluir.

4.  No servidor de Borda, abra o assistente de Implantação do Lync Server. Clique em Instalar ou Atualizar o Sistema do Lync Server e clique em Configurar ou Remover Componentes do Lync Server. Clique em Executar Novamente.

5.  Em Configurar componentes do Lync Server, clique em Próximo. A tela de resumo mostrará as ações à medida que elas são executadas. Depois que a implantação for feita, clique em Exibir Log para exibir arquivos de log disponíveis. Clique em Concluir para concluir a implantação.
    
    <div>
    

    > [!IMPORTANT]  
    > Você pode selecionar essa opção, mas apenas um pool de Borda ou Servidor de Borda em sua organização pode ser publicado externamente para federação. Todos os acessos por usuários federados, incluindo usuários de mensagens instantâneas públicas (IM), passam pelo mesmo pool de Borda ou servidor de borda único. Por exemplo, se sua implantação incluir um pool de Borda ou um único Servidor de Borda implantado em Nova York e um implantado em Londres e você habilitar o suporte de federação no pool de Borda de Nova York ou servidor de borda único, o tráfego de sinal para usuários federados passará pelo pool de Borda de Nova York ou pelo servidor de borda único. Isso se aplica inclusive para comunicações com usuários de Londres, embora um usuário interno de Londres chamando um usuário federado de Londres use o pool de Londres ou Servidor de Borda para tráfego de A/V.

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>Configurando Federação com Parceiros

1.  Para configurar uma federação bem-sucedida com outro Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 ou Office Communicator 2007, selecione o tipo de federação na tabela a seguir e defina registros SRV DNS, host DNS (A ou AAAA para IPv6) e configure políticas aplicáveis ao tipo de federação:
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Tipo de federação</th>
    <th>Registros DNS</th>
    <th>Definição de Política</th>
    <th>Observações</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Domínio do Parceiro Descoberto</p></td>
    <td><p>Configure o registro SRV do formato _sipfederationtls._tcp. &lt; nome de domínio externo Onde o valor da porta para o registro SRV é &gt; TCP 5061 e o <strong>Host que</strong> oferece esse serviço é definido como sip. &lt;nome de domínio &gt; externo – o FQDN do seu serviço de Borda de Acesso. Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> para obter detalhes sobre como criar o registro SRV</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Habilitar ou desabilitar descoberta de parceiros de federação no Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>As versões anteriores se referiam a esse tipo de federação como <strong>Federação Aprimorada Aberta.</strong> A criação do registro SRV é necessária para esse tipo de federação e é permitir que outros parceiros descubram sua federação.</p></td>
    </tr>
    <tr class="even">
    <td><p>Domínio de parceiro permitido</p></td>
    <td><p>Configure o registro SRV do formato _sipfederationtls._tcp. &lt; nome de domínio externo Onde o valor da porta para o registro SRV é &gt; TCP 5061 e o <strong>Host que</strong> oferece esse serviço é definido como sip. &lt;nome de domínio &gt; externo – o FQDN do seu serviço de Borda de Acesso. Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> para obter detalhes sobre como criar o registro SRV</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>As versões anteriores se referiam a esse tipo de federação como <strong>Federação Aprimorada.</strong> A criação do registro SRV é opcional para esse tipo de federação e é permitir que outros parceiros descubram sua federação. É claro que, em seguida, isso é <strong>uma Federação Aprimorada Aberta</strong>ou Domínio do Parceiro <strong>Descoberto</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>Servidor parceiro permitido</p></td>
    <td><p>Configurar o nome de domínio SIP e o FQDN do servidor de borda parceiro como um parceiro de federação em Políticas</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configurar suprote para domínios externos permitidos no Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configurar suporte para domínios externos bloqueados no Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Esse tipo de federação é a definição de um para um relacionamento e não permite a descoberta de outros parceiros de federação. Cada parceiro de federação é configurado explicitamente. Nas versões anteriores, isso era conhecido como <strong>Federação Direta</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>Provedor de Hospedagem e Provedor público de IM</p></td>
    <td><p>Nenhum requisito DNS específico é definido para esse tipo de federação</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Criar ou editar fornecedores SIP públicos federados no Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Criar ou editar provedores hospedados federados SIP no Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Esse tipo de federação define serviços e provedores de hospedagem que você deseja configurar para seus usuários. Os usos típicos incluem configuração para provedores públicos de IM, como Windows Live Messenger, Yahoo! e AOL, bem como provedores de hospedagem como o Lync Online e o Microsoft 365</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>A partir de 1º de setembro de 2012, a Licença de Assinatura do Usuário de Conectividade pública de IM do Microsoft Lync ("PIC USL") não está mais disponível para compra para contratos novos ou renovadores. Os clientes com licenças ativas poderão continuar federados com o Yahoo! Messenger até a data de encerrar o serviço. Uma data de fim de vida de junho de 2014 para AOL e Yahoo! foi anunciado. Para obter detalhes, <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">consulte Support for public instant messenger connectivity in Lync Server 2013</A>.</P>
    > <LI>
    > <P>A USL pic é uma licença de assinatura por usuário por mês que é necessária para o Lync Server ou o Office Communications Server federar com o Yahoo! Messenger. A capacidade da Microsoft de fornecer esse serviço foi contingente com o suporte do Yahoo!, o contrato subjacente para o qual está se esvaindo.</P>
    > <LI>
    > <P>Mais do que nunca, o Lync é uma ferramenta poderosa para se conectar entre organizações e com indivíduos em todo o mundo. A federação Windows Live Messenger requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync. A federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync alcancem centenas de milhões de pessoas com mensagens de IM e voz.</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  Definir e configurar qualquer host DNS necessário (A ou AAAA para IPv6) e registros SRV DNS

3.  Defina e configure todas as políticas usando o Painel de Controle do Lync Server ou usando o Shell de Gerenciamento do Lync Server e os cmdlets apropriados. Para obter detalhes sobre os cmdlets do Shell de Gerenciamento do Lync Server, consulte [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)
    
    <div>
    

    > [!NOTE]  
    > O Lync Room System (LRS) não mostra o botão de junção para reuniões enviadas pelos organizadores em parceiros federados do Lync. Para que um link de junção de reunião apareça no LRS, a organização de envio deve habilitar o TNEF usando o seguinte cmdlet:<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>Observe que isso não é específico do LRS. O Outlook e o Lync também não mostrariam Links de junção neste caso, pois as propriedades MAPI não são transportadas, mas, no caso do Outlook, o usuário pode abrir o convite da reunião e clicar na URL da reunião. Quando O TNEFEnabled é definido como verdadeiro, o Exchange 2013 não tira propriedades MAPI, incluindo OnlineMeetingExternalLink e o botão Ingressar será mostrado no lembrete.

    
    </div>

</div>

<div>

## <a name="see-also"></a>Confira também


[Planejamento para SIP, federação XMPP e mensagens instantâneas públicas no Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[Gerenciamento de federação e acesso externo ao Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

