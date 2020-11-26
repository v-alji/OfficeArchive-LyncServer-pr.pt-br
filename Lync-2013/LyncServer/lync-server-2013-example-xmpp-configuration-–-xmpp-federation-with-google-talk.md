---
title: Exemplo de configuração de XMPP – federação XMPP com Google Talk
description: Exemplo de configuração do XMPP – Federação do XMPP com o Google Talk.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428445"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a>Exemplo de configuração de XMPP no Lync Server 2013 – federação XMPP com Google Talk

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Tópico da última modificação:** 2014-04-22_

Um exemplo de configuração para a implantação do proxy XMPP define uma federação com o Google Talk.

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a>Exemplo de configuração de XMPP – federação XMPP com Google Talk

1.  No servidor front-end, abra o assistente de implantação do Lync Server. Clique em **instalar** ou **atualizar o Lync Server System** e, em seguida, clique em **Configurar** ou **remover componentes do Lync Server**. Clique em **executar novamente**.

2.  Em **configurar componentes do Lync Server**, clique em **Avançar**. A tela Resumo mostrará as ações conforme elas são executadas. Após a conclusão da implantação, clique em **Exibir log** para exibir os arquivos de log disponíveis. Clique em **concluir** para concluir a implantação.

3.  No servidor de borda, abra o assistente de implantação do Lync Server. Clique em **instalar** ou **atualizar o Lync Server System** e, em seguida, clique em **Configurar** ou **remover componentes do Lync Server**. Clique em **executar novamente**.

4.  Adicione o Google Talk como parceiro autorizado da XMPP. No momento, o Google Talk só dá suporte a conexões TCP não criptografadas para a Federação do XMPP Server-to-Server e só dá suporte à verificação de identidades do servidor. (Consulte <http://xmpp.org/extensions/xep-0220.html> ).
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  Para habilitar a Federação de borda, digite o seguinte:
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  Em **configurar componentes do Lync Server**, clique em **Avançar**. A tela Resumo mostrará as ações conforme elas são executadas. Depois que a implantação for concluída, clique em **Exibir log** para exibir os arquivos de log disponíveis. Clique em **concluir** para concluir a implantação.

7.  No servidor de borda, no assistente de implantação do Lync Server, ao lado da **etapa 3: solicitar, instalar ou atribuir certificados**, clique **novamente em executar**.
    
    <div>
    

    > [!TIP]
    > Se você estiver implantando o servidor de borda pela primeira vez, você verá executar novamente em vez de executar novamente.

    
    </div>

8.  Na página **Tarefas de Certificado Disponíveis**, clique em  **Criar uma nova solicitação de certificado**.

9.  Na página **solicitação de certificado** , clique em **certificado de borda externa**.

10. Na página **solicitação atrasada ou imediata** , marque a caixa de seleção **preparar a solicitação agora, mas enviá-la mais tarde** .

11. Na página **arquivo de solicitação de certificado** , digite o caminho completo e o nome do arquivo para o qual a solicitação deve ser salva (por exemplo, c: \\ CERT \_ guia \_ Edge. cer).

12. Na página **especificar modelo de certificado alternativo** , para usar um modelo diferente do modelo padrão do webserver, marque a caixa de seleção **usar modelo de certificado alternativo para a autoridade de certificação selecionada** .

13. Na página **configurações de nome e segurança** , faça o seguinte:
    
    1.  Em **nome amigável**, digite um nome de exibição para o certificado
    
    2.  Em **comprimento de bit**, especifique o comprimento do bit (geralmente, o padrão de **2048**)
    
    3.  Verifique se a caixa de seleção **Marcar chave privada de certificado como exportável** está marcada

14. Na página **informações da organização** , digite o nome da organização e da unidade organizacional (por exemplo, uma divisão ou um departamento)

15. Na página **informações geográficas** , especifique as informações de localização

16. Na página **nome do assunto/nomes alternativos de assunto** , as informações a serem automaticamente preenchidas pelo assistente serão exibidas. Se forem necessários nomes alternativos de entidades adicionais, você os especificará nas duas próximas etapas

17. Na **configuração de domínio SIP na página de nomes alternativos de entidades (SANs)** , marque a caixa de seleção domínio para adicionar um SIP. \<sipdomain\> entrada para a lista nomes alternativos da entidade.

18. Na página **configurar nomes alternativos de entidades adicionais** , especifique os nomes alternativos de entidades adicionais necessários.
    
    <div>
    

    > [!TIP]
    > Se o proxy XMPP estiver instalado, por padrão, o nome de domínio (como contoso.com) será preenchido nas entradas de SAN. Se você precisar de mais entradas, adicione-as nesta etapa.

    
    </div>

19. Na página **Resumo da solicitação** , examine as informações do certificado a serem usadas para gerar a solicitação.

20. Após a conclusão da execução dos comandos, você pode **Exibir o log** ou clicar em **Avançar** para continuar.

21. Na página **arquivo de solicitação de certificado** , você pode exibir o arquivo de solicitação de assinatura de certificado (CSR) gerado clicando em **Exibir** ou em sair do assistente de certificado clicando em **concluir**.

22. Copie o arquivo de solicitação e envie para sua autoridade de certificação pública.

23. Depois de receber, importar e atribuir o certificado público, você deve parar e reiniciar os serviços do servidor de borda. Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**... No Shell de gerenciamento do Lync Server, digite:
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. Para configurar o DNS para a Federação do XMPP, adicione o seguinte registro SRV para DNS externo: \_ XMPP-Server. \_ Protocol.\<domain name\> O registro SRV será resolvido para o FQDN de borda de acesso do servidor de borda, com um valor de porta de 5269

25. Configure uma nova política de acesso externo para permitir que todos os usuários abram o Shell de gerenciamento do Lync Server em um servidor front-end e digitem:
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

</div>

</div>

<span> </span>

</div>

</div>

</div>

