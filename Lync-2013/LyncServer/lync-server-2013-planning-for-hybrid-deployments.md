---
title: 'Lync Server 2013: Planejamento para implantações híbridas'
description: 'Lync Server 2013: Planejamento para implantações híbridas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424545"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a>Planejamento para implantações híbridas do Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico Última Modificação:** 2016-05-25_

Você deve considerar os seguintes requisitos para usuários e sua infraestrutura de rede durante o planejamento de uma implantação híbrida.

<div>

## <a name="infrastructure-requirements"></a>Requisitos de infraestrutura

Você deve ter o seguinte configurado em seu ambiente para implementar e implantar uma implantação híbrida.

  - Uma organização do Microsoft 365 ou do Office 365 com o Skype for Business Online habilitado. Observe que você pode usar apenas um único locatário para uma configuração híbrida com sua implantação local.

  - Uma única implantação local (infraestrutura) do Skype for Business Server ou do Lync Server implantado em uma topologia com suporte. Consulte Requisitos de Topologia.
    
    Para obter informações sobre como configurar sua implantação do Lync Server 2013 ou Lync Server 2010 para híbrido, consulte [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).

  - Ferramentas administrativas do Skype for Business Server 2015. Se você estiver usando o Lync Server 2013 ou o Lync Server 2010, poderá usar as ferramentas administrativas do Lync Server 2013.

  - Para dar suporte ao Logon Único com o Microsoft 365 ou o Office 365 para que os usuários possam usar as mesmas credenciais de logon para entrar no Office como fazem no local, você pode usar os recursos de sincronização de senha do Azure Active Directory (AAD) Connect. Você também pode usar os Serviços de Federação do Active Directory (AD FS) para um único login com o Microsoft 365 ou o Office 365.
    
    Para obter mais informações, consulte Integrando suas identidades locais [com o Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).

  - Uma solução de sincronização de diretório único para manter seus objetos Do Active Directory locais e online sincronizados. Para obter detalhes sobre a Sincronização de Diretórios, consulte [Ferramentas de Integração de Diretório.](https://go.microsoft.com/fwlink/p/?linkid=530320)

</div>

<div>

## <a name="lync-client-support"></a>Suporte ao cliente do Lync

Há algumas diferenças nos recursos suportados nos clientes do Lync, bem como nos recursos disponíveis em ambientes locais e online. Antes de decidir onde deseja a casa dos usuários em sua organização, você pode exibir o suporte ao cliente para as várias configurações do Lync Server. Os seguintes clientes têm suporte com o Skype for Business Online em uma implantação híbrida do Lync:

  - Lync 2010

  - Lync 2013

  - Aplicativo Lync Windows Store

  - Lync Web App

  - Lync Mobile

  - Lync para Mac 2011

  - Sistema de Salas do Lync

  - Lync Basic 2013

Para obter detalhes sobre o suporte ao cliente, consulte os seguintes tópicos:

  - [Clientes do Lync Online](https://go.microsoft.com/fwlink/?linkid=281902)

  - [Tabelas de comparação dos clientes para o Lync Server 2013](lync-server-2013-desktop-client-comparison-tables.md)

  - [Tabela de comparação de clientes móveis para o Lync Server 2013](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a>Requisitos de topologia

Para configurar sua implantação híbrida com o Skype for Business Online, você precisa ter uma das seguintes topologias com suporte:

  - Uma implantação do Skype for Business Server 2015 com todos os servidores executando o Skype for Business Server 2015.

  - Uma implantação do Lync Server 2013 com todos os servidores executando o Lync Server 2013.

  - Uma implantação do Lync Server 2010 com todos os servidores executando o Lync Server 2010 com as atualizações cumulativas mais recentes.
    
      - O Servidor de Borda de federação e o servidor de próximo salto do Servidor de Borda de federação devem estar executando o Lync Server 2010 com as atualizações cumulativas mais recentes.
    
      - As Ferramentas Administrativas do Skype for Business Server 2015 ou Lync Server 2013 devem ser instaladas em pelo menos um servidor ou estação de trabalho de gerenciamento.

  - Uma implantação mista do Lync Server 2013 e do Skype for Business Server 2015 com as seguintes funções de servidor em pelo menos um site executando o Skype for Business Server 2015:
    
      - Pelo menos um servidor Pool Enterprise ou Standard Edition. 
    
      - O Pool de Diretores associado à federação SIP, se ela existir.
    
      - O Pool de Borda associado à federação SIP.

  - Uma implantação mista do Lync Server 2010 e do Skype for Business Server 2015 com as seguintes funções de servidores em pelo menos um site executando o Skype for Business Server 2015:
    
      - Pelo menos um servidor Pool Enterprise ou Standard Edition. 
    
      - O Pool de Diretores associado à federação SIP, se ela existir.
    
      - O Pool de Borda associado à federação SIP do site.

  - Uma implantação mista do Lync Server 2010 e do Lync Server 2013 com as seguintes funções de servidor em pelo menos um site executando o Lync Server 2013:
    
      - Pelo menos um servidor Pool Enterprise ou Standard Edition no site.
    
      - O Pool de Diretores associado à federação SIP, se ela existir no site.
    
      - O Pool de Borda associado à federação SIP do site.

<div>


> [!IMPORTANT]  
> Todo o gerenciamento de usuários, incluindo movimentações de usuários entre o local e o UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, precisa ser feito usando a versão mais recente instalada das ferramentas administrativas. As ferramentas administrativas devem ser instaladas em um servidor separado que tenha acesso de conexão à implantação local existente e à Internet. O cmdlet <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> para mover usuários de sua implantação local para UNRESOLVED_TOKEN_VAL(skype16_online) deve ser executado a partir das ferramentas administrativas conectadas à sua implantação local.



</div>

Para obter mais informações sobre topologias com suporte, consulte Topologias com suporte no [Lync Server 2013](lync-server-2013-supported-topologies.md)e topologias de referência do [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)para implantações híbridas corporativas.

Para obter informações de solução de problemas sobre implantações híbridas e conectar o PowerShell ao Lync Online, consulte [Lync Online: Lync PowerShell e Solução de Problemas Híbridos.](https://go.microsoft.com/fwlink/p/?linkid=306718)

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a>Requisitos para listas de federação permitidos/bloqueados

A lista Domínios permitidos contém domínios com um FQDN (nome de domínio totalmente qualificado) de Borda parceiro configurado. Por vezes, eles são chamados de *servidores parceiros permitidos* ou *parceiros de federação diretos*. Você deve estar familiarizado com a diferença entre a federação aberta e a federação fechada, conhecidas respectivamente como *descoberta de parceiros* e *lista de domínios dos parceiros permitidos* nas implantações locais.

Os seguintes requisitos devem ser atendidos para configurar com êxito uma implantação híbrida:

  - A correspondência de domínio deve ser configurada da mesma forma para sua implantação local e sua organização do Microsoft 365 ou office 365. Se a descoberta de parceiros estiver habilitada na implantação local, a federação aberta deverá ser configurada para seu locatário online. Caso contrário, a federação fechada deverá ser configurada para seu locatário online.

  - A lista de domínios bloqueados da implantação local deve corresponder exatamente à do seu locatário online.

  - A lista de domínios permitidos da implantação local deve corresponder exatamente à do seu locatário online.

  - A federação deve estar habilitada para as comunicações externas para o locatário online, que é configurada usando o Painel de Controle do Lync Online.

</div>

<div>

## <a name="dns-settings"></a>Configurações dns

Ao criar registros DNS para implantações híbridas, todos os registros DNS externos do Lync devem apontar para a infraestrutura local. Para obter detalhes sobre registros DNS necessários, consulte Requisitos do Sistema de Nomes de Domínio [(DNS) para o Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).

Além disso será necessário garantir que a resolução DNS descrita na tabela a seguir funciona em sua implantação local:


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Registro DNS</p></td>
<td><p>Pode ser resolvido por</p></td>
<td><p>Requisitos de DNS</p></td>
</tr>
<tr class="even">
<td><p>Registro SRV DNS para _sipfederationtls._tcp. &lt; sipdomain.com para todos os domínios SIP com suporte &gt; que resolvem ip(s) externos do Access Edge</p></td>
<td><p>Servidor(es) de borda</p></td>
<td><p>Habilitar a comunicação federada em uma configuração híbrida. O servidor de borda precisa saber para onde encaminhar o tráfego federado para o domínio SIP que está dividido entre as instalações local e online.</p></td>
</tr>
<tr class="odd">
<td><p>Registro(s) A de DNS para FQDN do serviço de webconferência de borda, como webcon.contoso.com, que resolve IP(s) de borda de webconferência</p></td>
<td><p>Computadores de usuários conectados à rede corporativa interna</p></td>
<td><p>Habilitar usuários online para apresentar ou visualizar conteúdo em reuniões hospedadas localmente. O conteúdo inclui arquivos do PowerPoint, quadros de comunicações, votações e observações compartilhadas. </p></td>
</tr>
</tbody>
</table>


Dependendo de como o DNS está configurado na sua organização, talvez seja necessário adicionar esses registros à zona DNS hospedada interna para os domínios SIP correspondentes para proporcionar resolução de DNS interna para esses registros.

</div>

<div>

## <a name="firewall-considerations"></a>Considerações sobre firewall

Os computadores de sua rede devem ser capazes de realizar pesquisas DNS padrão na Internet. Se esses computadores puderem acessar os sites padrão da Internet, sua rede atenderá a esse requisito.

Dependendo do local do seu data center Microsoft Online Services, você também deve configurar seus dispositivos de firewall de rede para aceitar conexões com base em nomes de domínio curinga (por exemplo, todo o tráfego de \* .outlook.com). Se os firewalls de sua organização não oferecem suporte às configurações de nome com coringa, você deve determinar manualmente o intervalo de endereço IP que deseja permitir e as portas especificadas.

Consulte o tópico Ajuda URLs e intervalos de [endereços IP do Office 365.](https://go.microsoft.com/fwlink/p/?linkid=252942)

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a>Requisitos de porta e protocolo

Além dos requisitos de porta para comunicação interna do Lync Server 2013, você também deve configurar as portas a seguir.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Protocolo/Porta</th>
<th>Aplicativos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TCP 443</p></td>
<td><p>Abrir entrada</p>
<ul>
<li><p>Serviços de Federação do Active Directory (função de servidor de federação)</p>
<p>Para obter mais informações, consulte <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</p></li>
<li><p>Serviços de Federação do Active Directory (função de servidor proxy)</p></li>
<li><p>Microsoft Online Services Portal</p></li>
<li><p>Portal da Minha Empresa</p></li>
<li><p>Outlook Web App</p></li>
<li><p>Cliente Lync (comunicação com o Lync Online a partir do Lync Server local)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>TCP 80 e 443</p></td>
<td><p>Abrir entrada</p>
<ul>
<li><p>Ferramenta de Sincronização de Diretórios do Microsoft Online Services</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>TCP 5061</p></td>
<td><p>Abrir entrada/saída no Servidor de Borda</p></td>
</tr>
<tr class="even">
<td><p>PSOM/TLS 443</p></td>
<td><p>Abrir entrada/saída para sessões de compartilhamento de dados</p></td>
</tr>
<tr class="odd">
<td><p>STUN/TCP 443</p></td>
<td><p>Abrir sessões de entrada/saída para áudio, vídeo, compartilhamento de aplicativos</p></td>
</tr>
<tr class="even">
<td><p>STUN/UDP 3478</p></td>
<td><p>Abrir entrada/saída para sessões de áudio e vídeo</p></td>
</tr>
<tr class="odd">
<td><p>RTP/TCP 50000-59999</p></td>
<td><p>Abrir saída para sessões de áudio e vídeo</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a>Contas de usuário e dados

Em uma implantação híbrida do Lync Server 2013, qualquer usuário que você deseja ter no Lync Online deve primeiro ser criado na implantação local, para que a conta de usuário seja criada nos Serviços de Domínio do Active Directory. Em seguida, você pode mover o usuário para o Skype for Business Online, que move a lista de contatos do usuário.

Ao sincronizar as contas de usuário entre suas implantações do Lync local e do Lync Online com o AD FS e o Dirsync, você precisa sincronizar as contas do AD para todos os usuários do Lync em sua organização entre suas implantações locais e online do Lync, mesmo que os usuários não sejam movidos para o Lync Online. Se você não sincronizar todos os usuários, a comunicação entre os usuários locais e online na sua organização poderá não funcionar conforme o esperado.

<div>


> [!IMPORTANT]  
> Se o usuário for criado usando o portal online para o Centro de administração do Microsoft 365, a conta de usuário não será sincronizada com o Active Directory local e o usuário não existirá no Active Directory local. Se você já criou usuários no Lync Online e deseja configurar híbrido com um Lync Server local, consulte Mover usuários do Lync Online para o Lync local no <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013</A>.



</div>

Você também deve considerar os seguintes problemas relacionados ao usuário ao se planejar para uma implantação híbrida.

  - **Contatos do usuário**   O limite para contatos para usuários do Lync Online é 250. Todos os contatos além desse número serão removidos da lista de contatos do usuário quando a conta for movida para o Lync Online.

  - **Sistema de mensagens instantâneas e presença** As listas de contatos, os grupos e as ACLs (lista de controle de acesso) do usuário são migrados com a conta de usuário.

  - **Dados de conferência, conteúdo de reunião e reuniões agendadas**   Esse conteúdo não é migrado com a conta de usuário. Os usuários devem reagendar as reuniões depois que as contas são migradas para o Lync Online.

</div>

<div>

## <a name="user-policies-and-features"></a>Políticas e recursos do usuário

  - Em um ambiente híbrido do Lync Server 2013, os usuários podem ser habilitados para Mensagens Instantâneas, voz e reuniões no local ou online, mas não simultaneamente.

  - **Cliente Lync**    Alguns usuários podem exigir uma nova versão do cliente quando são movidos para o Lync Online. Para o Office Communications Server 2007 R2, os usuários devem ser movidos para um pool do Lync Server 2013 antes da migração para o Lync Online.
    
    Para obter mais informações sobre o suporte ao cliente, consulte [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).

  - **Configuração e políticas locais (não usuário)**   As políticas online e local exigem configuração separada. Você não pode definir políticas globais que se apliquem a ambas.

</div>

</div>

<span> </span>

</div>

</div>

</div>
