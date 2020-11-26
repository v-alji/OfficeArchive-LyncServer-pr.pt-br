---
title: 'Lync Server 2013: usando a autenticação de dois fatores com o cliente Lync'
description: 'Lync Server 2013: usando a autenticação de dois fatores com o cliente Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using two-factor authentication with Lync client
ms:assetid: d4136e61-c3ab-4b26-85c8-c1b2c24f5ee3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn338071(v=OCS.15)
ms:contentKeyID: 55115593
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbfde1d04d4e641c8fbe4817ffce214df891b565
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438684"
---
# <a name="using-two-factor-authentication-with-lync-client-and-lync-server-2013"></a><span data-ttu-id="a4371-103">Usando a autenticação de dois fatores com o Lync Client e o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a4371-103">Using two-factor authentication with Lync client and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a4371-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a4371-104">

<span> </span></span></span>

<span data-ttu-id="a4371-105">_**Tópico da última modificação:** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="a4371-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="a4371-106">Este tópico descreveu como tirar proveito da autenticação de dois fatores com o cliente Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a4371-106">This topic described how to take advantage of two-factor authentication with Lync 2013 client.</span></span>

<div>

## <a name="sign-in-to-lync-2013-for-the-first-time"></a><span data-ttu-id="a4371-107">Entrar no Lync 2013 pela primeira vez</span><span class="sxs-lookup"><span data-stu-id="a4371-107">Sign in to Lync 2013 for the first time</span></span>

<span data-ttu-id="a4371-108">Suas informações de entrada do Lync geralmente são configuradas automaticamente quando o Lync 2013 está instalado.</span><span class="sxs-lookup"><span data-stu-id="a4371-108">Your Lync sign-in information is usually configured automatically when Lync 2013 is installed.</span></span> <span data-ttu-id="a4371-109">Mas, na primeira vez que você usar o Lync, talvez seja necessário iniciar manualmente o cliente.</span><span class="sxs-lookup"><span data-stu-id="a4371-109">But the first time you use Lync, you might have to manually start the client.</span></span>

<span data-ttu-id="a4371-110">**Para entrar no Lync pela primeira vez**</span><span class="sxs-lookup"><span data-stu-id="a4371-110">**To sign in to Lync for the first time**</span></span>

1.  <span data-ttu-id="a4371-111">Faça logon na rede da sua organização.</span><span class="sxs-lookup"><span data-stu-id="a4371-111">Log on to your organization’s network.</span></span>

2.  <span data-ttu-id="a4371-112">Selecione **Iniciar** \> **todos os programas** \> **Microsoft Lync \> Lync 2013**.</span><span class="sxs-lookup"><span data-stu-id="a4371-112">Select **Start** \> **All Programs** \> **Microsoft Lync \> Lync 2013**.</span></span>
    
    <span data-ttu-id="a4371-113">Você verá a tela de entrada do Lync.</span><span class="sxs-lookup"><span data-stu-id="a4371-113">You should see the Lync sign-in screen.</span></span>
    
      - <span data-ttu-id="a4371-114">Se a caixa de endereço de entrada já estiver preenchida, confirme se o endereço mostrado está correto.</span><span class="sxs-lookup"><span data-stu-id="a4371-114">If the sign-in address box is already filled in, confirm that the address shown is correct.</span></span>
    
      - <span data-ttu-id="a4371-115">Se não estiver correto ou se a caixa estiver vazia, insira seu endereço de entrada do Lync (geralmente é o mesmo que o seu endereço de email).</span><span class="sxs-lookup"><span data-stu-id="a4371-115">If it’s not correct, or if the box is empty, enter your Lync sign-in address (this is usually the same as your email address).</span></span>
    
      - <span data-ttu-id="a4371-116">Se uma caixa de senha vazia for exibida, adicione sua senha.</span><span class="sxs-lookup"><span data-stu-id="a4371-116">If an empty password box is displayed, add your password.</span></span>

3.  <span data-ttu-id="a4371-117">Selecione **Entrar**.</span><span class="sxs-lookup"><span data-stu-id="a4371-117">Select **Sign-in**.</span></span>

</div>

<div>

## <a name="sign-out-of-lync"></a><span data-ttu-id="a4371-118">Sair do Lync</span><span class="sxs-lookup"><span data-stu-id="a4371-118">Sign out of Lync</span></span>

<span data-ttu-id="a4371-119">Quando terminar de usar o Lync, você pode fechar a exibição, sair da sessão ou sair do programa, tudo a partir do menu arquivo.</span><span class="sxs-lookup"><span data-stu-id="a4371-119">When you’re finished using Lync, you can close the display, sign out of your session, or exit from the program, all from the File menu.</span></span> <span data-ttu-id="a4371-120">A tabela a seguir explica as diferenças nas opções.</span><span class="sxs-lookup"><span data-stu-id="a4371-120">The following table explains the differences in the options.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4371-121">Opção</span><span class="sxs-lookup"><span data-stu-id="a4371-121">Option</span></span></th>
<th><span data-ttu-id="a4371-122">O que ela faz</span><span class="sxs-lookup"><span data-stu-id="a4371-122">What it does</span></span></th>
<th><span data-ttu-id="a4371-123">Como executar</span><span class="sxs-lookup"><span data-stu-id="a4371-123">How to perform it</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4371-124">Fechar</span><span class="sxs-lookup"><span data-stu-id="a4371-124">Close</span></span></p></td>
<td><p><span data-ttu-id="a4371-125">Fecha a exibição do Lync, mas permite que a sessão do Lync identificada com sua ID de usuário continue sendo executada.</span><span class="sxs-lookup"><span data-stu-id="a4371-125">Closes your Lync display but lets the Lync session identified with your user ID continue to run.</span></span> <span data-ttu-id="a4371-126">Isso acontece para que você possa continuar a obter notificações e a interagir com outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="a4371-126">This is so you can continue to get notifications and interact with others.</span></span></p>
<p><span data-ttu-id="a4371-127">Você pode retomar a exibição a qualquer momento clicando no ícone do Lync na barra de tarefas ou na área de notificação na parte inferior da tela.</span><span class="sxs-lookup"><span data-stu-id="a4371-127">You can get the display back at any time by clicking the Lync icon on the taskbar or the notification area at the bottom of your screen.</span></span></p></td>
<td><p><span data-ttu-id="a4371-128">Na janela principal do Lync, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="a4371-128">On the Lync main window, do one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="a4371-129">Selecione o botão <strong>Opções</strong> e, em seguida, selecione <strong>arquivo</strong> &gt; <strong>fechar</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4371-129">Select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Close</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a4371-130">Clique no botão <strong>Fechar</strong> (X) no canto superior direito da janela.</span><span class="sxs-lookup"><span data-stu-id="a4371-130">Click the <strong>Close</strong> button (X) in the upper-right corner of the window.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4371-131">Sair</span><span class="sxs-lookup"><span data-stu-id="a4371-131">Sign out</span></span></p></td>
<td><p><span data-ttu-id="a4371-132">Finaliza a sessão do Lync associada à sua ID de usuário, mas o Lync continua a ser executado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a4371-132">Ends the Lync session associated with your user ID, but Lync continues to run in the background.</span></span> <span data-ttu-id="a4371-133">Quando você sair, a janela de entrada aparecerá.</span><span class="sxs-lookup"><span data-stu-id="a4371-133">When you sign out, the sign-in window will appear.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="a4371-p105">Selecione <STRONG>Excluir minhas informações de entrada</STRONG> ao sair para remover o registro de sua ID de logon e da senha do computador. Fazer isso torna mais fácil para o pessoal de suporte solucionar problemas de entrada. Também ajuda a garantir que suas informações de entrada fiquem mais seguras ao dificultar que usuários não autorizados façam logon com suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="a4371-p105">Select <STRONG>Delete my sign-in information</STRONG> when you sign out to remove the record of your logon ID and password from the computer. Doing this might make it easier for support people to troubleshoot sign-in issues. It can also help ensure your sign-in information is more secure by making it difficult for unauthorized users to log on with your credentials.</span></span>


</div></td>
<td><p><span data-ttu-id="a4371-137">Na janela principal do Lync, selecione o botão <strong>Opções</strong> e, em seguida, selecione <strong>arquivo</strong> &gt; <strong>sair</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4371-137">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Sign Out</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4371-138">Fechar</span><span class="sxs-lookup"><span data-stu-id="a4371-138">Exit</span></span></p></td>
<td><p><span data-ttu-id="a4371-139">Encerra a sessão do Lync e desliga o Lync em seu computador.</span><span class="sxs-lookup"><span data-stu-id="a4371-139">Ends your Lync session and shuts down Lync on your computer.</span></span> <span data-ttu-id="a4371-140">Depois de sair, se você quiser reiniciar o Lync, selecione <strong>Iniciar</strong> &gt; <strong>todos os programas</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4371-140">After exiting, if you want to restart Lync, select <strong>Start</strong> &gt; <strong>All Programs</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>.</span></span></p></td>
<td><p><span data-ttu-id="a4371-141">Na janela principal do Lync, selecione o botão <strong>Opções</strong> e, em seguida, selecione <strong>arquivo</strong> &gt; <strong>sair</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4371-141">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Exit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sign-in-to-lync-with-a-smart-card"></a><span data-ttu-id="a4371-142">Entrar no Lync com um cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="a4371-142">Sign in to Lync with a Smart Card</span></span>

<span data-ttu-id="a4371-143">Algumas organizações agora usam um processo de entrada em várias etapas, chamado de autenticação de dois fatores, para aumentar a segurança dos usuários do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a4371-143">Some organizations now use a multi-step sign-in process, called two-factor authentication, to increase security for their Lync 2013 users.</span></span> <span data-ttu-id="a4371-144">Se você espera usar esta opção, precisará de um "cartão inteligente" para entrar no Lync.</span><span class="sxs-lookup"><span data-stu-id="a4371-144">If you’re expected to use this option, you’ll need a “smart card” to sign in to Lync.</span></span> <span data-ttu-id="a4371-145">Os cartões inteligentes vêm em duas variedades, físicas e virtuais:</span><span class="sxs-lookup"><span data-stu-id="a4371-145">Smart cards come in two varieties, physical and virtual:</span></span>

  - <span data-ttu-id="a4371-146">**Física**   Sobre o tamanho de um cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="a4371-146">**Physical**   About the size of a credit card.</span></span> <span data-ttu-id="a4371-147">Você o insere em um leitor de cartão inteligente ao fazer logon.</span><span class="sxs-lookup"><span data-stu-id="a4371-147">You insert it into a smart card reader when you log in.</span></span>

  - <span data-ttu-id="a4371-148">**Virtual**   Não é um objeto físico, mas um identificador eletrônico que é escrito para um chip especial em seu computador, que, em essência, cria o cartão inteligente no seu computador.</span><span class="sxs-lookup"><span data-stu-id="a4371-148">**Virtual**   Not a physical object, but an electronic identifier that gets written to a special chip on your computer, which in essence builds the smart card into your computer.</span></span> <span data-ttu-id="a4371-149">Disponível somente para uso com computadores com Windows 8 que contenham o chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="a4371-149">Available only for use with Windows 8 computers that contain the TPM (Trusted Platform Module) chip.</span></span>

<div>

## <a name="enroll-your-smart-card"></a><span data-ttu-id="a4371-150">Registrar seu cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="a4371-150">Enroll your smart card</span></span>

<span data-ttu-id="a4371-151">Antes que seja possível entrar com um cartão inteligente, o cartão deverá ser "registrado" — ou seja, suas credenciais devem ser identificadas com o cartão.</span><span class="sxs-lookup"><span data-stu-id="a4371-151">Before you can sign in with a smart card, the card must be “enrolled”—that is, your user credentials have to be identified with the card.</span></span> <span data-ttu-id="a4371-152">Esse será o caso seja o cartão físico ou virtual.</span><span class="sxs-lookup"><span data-stu-id="a4371-152">This is the case whether the card is physical or virtual.</span></span> <span data-ttu-id="a4371-153">Esse processo já pode ser realizado pelo administrador do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a4371-153">This process may already been carried out by your Lync Server administrator.</span></span> <span data-ttu-id="a4371-154">Verifique com ele se não tiver certeza se isso foi feito.</span><span class="sxs-lookup"><span data-stu-id="a4371-154">Check with them if you’re not sure whether that has been done.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a4371-155">Como cada cartão inteligente virtual está associado somente ao dispositivo em que ele está instalado, um cartão separado precisará ser registrado para cada computador com o Windows 8 que você usar.</span><span class="sxs-lookup"><span data-stu-id="a4371-155">Since each virtual smart card is associated only with the device it’s installed on, a separate card will need to be enrolled for each Windows 8 computer you use.</span></span>



</div>

<span data-ttu-id="a4371-156">**Para registrar manualmente seu cartão inteligente**</span><span class="sxs-lookup"><span data-stu-id="a4371-156">**To manually enroll your smart card**</span></span>

1.  <span data-ttu-id="a4371-157">Faça logon no computador em que você está executando o Lync.</span><span class="sxs-lookup"><span data-stu-id="a4371-157">Log on to the computer you’ll be running Lync on.</span></span>

2.  <span data-ttu-id="a4371-158">Usando o Internet Explorer, navegue até a página de Registro da Autoridade de Certificação da sua organização.</span><span class="sxs-lookup"><span data-stu-id="a4371-158">Using Internet Explorer, browse to your organization’s Certificate Authority Web Enrollment page.</span></span>
    
    <span data-ttu-id="a4371-159">Pergunte ao administrador do Lync Server o endereço Web desse recurso, se ainda não o tiver.</span><span class="sxs-lookup"><span data-stu-id="a4371-159">Ask your Lync Server administrator for the web address of this resource if you don’t already have it.</span></span> <span data-ttu-id="a4371-160">A URL terá a seguinte aparência: https://MyCA.\ [nomedesuaempresa \] . com/certsrv.</span><span class="sxs-lookup"><span data-stu-id="a4371-160">The URL will look something like this: https://MyCA.\[yourcompanyname\].com/certsrv.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a4371-161">Se você estiver usando o Internet Explorer 10, talvez precise exibir o site em Modo de Compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="a4371-161">If you’re using Internet Explorer 10, you may need to view this website in Compatibility Mode.</span></span>

    
    </div>

3.  <span data-ttu-id="a4371-162">Quando solicitado a fazer logon na página de certificação, faça logon usando sua conta de domínio (em vez do administrador do seu computador).</span><span class="sxs-lookup"><span data-stu-id="a4371-162">When you’re prompted to log on to the certification page, log on using your domain account (rather than as administrator of your computer).</span></span>

4.  <span data-ttu-id="a4371-163">Na página de Boas-vindas do site, selecione **Solicitar um certificado**.</span><span class="sxs-lookup"><span data-stu-id="a4371-163">On the website Welcome Page, select **Request a certificate**.</span></span>

5.  <span data-ttu-id="a4371-164">Selecione **Solicitação Avançada**.</span><span class="sxs-lookup"><span data-stu-id="a4371-164">Select **Advanced Request**.</span></span>

6.  <span data-ttu-id="a4371-165">Selecione **Criar e enviar uma solicitação para esta CA** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a4371-165">Select **Create and submit a request to this CA**, then click **Next**.</span></span>

7.  <span data-ttu-id="a4371-166">Agora você verá uma página chamada Estação de Registro de Cartão Inteligente.</span><span class="sxs-lookup"><span data-stu-id="a4371-166">Now you’ll see a page called Smart Card Enrollment Station.</span></span> <span data-ttu-id="a4371-167">Aprove a solicitação para instalar o controle ActiveX e então preencha o formulário Solicitação de Certificado Avançado desta forma:</span><span class="sxs-lookup"><span data-stu-id="a4371-167">Approve the request to install the ActiveX control, and then complete the Advanced Certificate Request form as follows:</span></span>
    
    1.  <span data-ttu-id="a4371-168">Selecione **Usuário de cartão inteligente** na lista suspensa **Modelo de Certificado**.</span><span class="sxs-lookup"><span data-stu-id="a4371-168">Select **Smartcard user** from the **Certificate Template** dropdown list.</span></span>
    
    2.  <span data-ttu-id="a4371-169">Selecione **Criar novo conjunto de chaves**.</span><span class="sxs-lookup"><span data-stu-id="a4371-169">Select **Create new key set**.</span></span>
    
    3.  <span data-ttu-id="a4371-170">Localize as informações do fabricante no rótulo do seu cartão inteligente e selecione esse fabricante na lista suspensa **CSP**.</span><span class="sxs-lookup"><span data-stu-id="a4371-170">Find the manufacturer information on the label of your smart card and select that manufacturer from the **CSP** dropdown list.</span></span>
    
    4.  <span data-ttu-id="a4371-171">Selecione **CSP** como o Formato de Solicitação, caso ainda não esteja selecionado.</span><span class="sxs-lookup"><span data-stu-id="a4371-171">Select **CSP** as the Request Format, if it’s not already selected.</span></span>
    
    5.  <span data-ttu-id="a4371-172">Selecione **sha1** na lista suspensa Algoritmo de Hash, caso ainda não tenha sido selecionado.</span><span class="sxs-lookup"><span data-stu-id="a4371-172">Select **sha1** from the Hash Algorithm dropdown list, if it’s not already selected.</span></span>
    
    6.  <span data-ttu-id="a4371-173">Dê um nome ao seu certificado que seja fácil de reconhecer e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="a4371-173">Give your certificate a name you’ll recognize, and click **Submit**.</span></span>

8.  <span data-ttu-id="a4371-174">Agora insira seu cartão inteligente em branco no leitor de cartão conectado à estação de registro e clique em **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="a4371-174">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

9.  <span data-ttu-id="a4371-175">Quando solicitado, insira seu número de identificação pessoal (PIN) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4371-175">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a4371-176">Se o encarregado do suporte técnico não tiver dado um PIN para você registrar seu cartão inteligente, use o valor padrão de PIN de cartão inteligente, 12345678.</span><span class="sxs-lookup"><span data-stu-id="a4371-176">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

10. <span data-ttu-id="a4371-177">Selecione a opção para forçar o usuário (você) a alterar o PIN na primeira vez em que o cartão inteligente for usado.</span><span class="sxs-lookup"><span data-stu-id="a4371-177">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

11. <span data-ttu-id="a4371-178">Agora insira seu cartão inteligente em branco no leitor de cartão conectado à estação de registro e clique em **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="a4371-178">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

12. <span data-ttu-id="a4371-179">Quando solicitado, insira seu número de identificação pessoal (PIN) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4371-179">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a4371-180">Se o encarregado do suporte técnico não tiver dado um PIN para você registrar seu cartão inteligente, use o valor padrão de PIN de cartão inteligente, 12345678.</span><span class="sxs-lookup"><span data-stu-id="a4371-180">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

13. <span data-ttu-id="a4371-181">Selecione a opção para forçar o usuário (você) a alterar o PIN na primeira vez em que o cartão inteligente for usado.</span><span class="sxs-lookup"><span data-stu-id="a4371-181">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

14. <span data-ttu-id="a4371-182">Clique em **OK** para confirmar se o certificado exibido tem suas informações neles.</span><span class="sxs-lookup"><span data-stu-id="a4371-182">Click **OK** to confirm that the certificate displayed has your information on it.</span></span>

15. <span data-ttu-id="a4371-183">Assim que for exibido o aviso de que o certificado foi emitido, clique em **Instalar este certificado** para concluir o processo de registro.</span><span class="sxs-lookup"><span data-stu-id="a4371-183">Once you see the notice that the certificate has been issued, click **Install this certificate** to complete the enrollment process.</span></span>

</div>

<div>

## <a name="sign-in-to-lync-with-your-smart-card-credentials"></a><span data-ttu-id="a4371-184">Entre no Lync com as credenciais do seu cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="a4371-184">Sign in to Lync with your smart card credentials</span></span>

<span data-ttu-id="a4371-185">Antes de usar o cartão inteligente pela primeira vez, é recomendável clicar em **excluir minhas informações de entrada** na página de entrada do Lync.</span><span class="sxs-lookup"><span data-stu-id="a4371-185">Before you use your smart card for the first time, it’s recommended that you click **Delete my sign-in info** on the Lync sign-in page.</span></span> <span data-ttu-id="a4371-186">Fazer isso limpará qualquer credencial de entrada armazenada no computador e eliminará uma possível origem de erros.</span><span class="sxs-lookup"><span data-stu-id="a4371-186">Doing this clears any sign-in credentials stored on your computer, and eliminates a possible source of error.</span></span>

<span data-ttu-id="a4371-187">**Para entrar no Lync com as credenciais do seu cartão inteligente**</span><span class="sxs-lookup"><span data-stu-id="a4371-187">**To sign in to Lync with your smart card credentials**</span></span>

1.  <span data-ttu-id="a4371-188">Inicie o cliente do Lync.</span><span class="sxs-lookup"><span data-stu-id="a4371-188">Start the Lync client.</span></span>

2.  <span data-ttu-id="a4371-189">Na tela Entrar, digite seu nome de conta de usuário na caixa **Endereço de entrada** e clique em **Entrar**.</span><span class="sxs-lookup"><span data-stu-id="a4371-189">On the Sign in screen, type your sign in user account name in the **Sign-in address** box, and then click **Sign In**.</span></span>

3.  <span data-ttu-id="a4371-190">Se você estiver usando um cartão inteligente virtual, ignore esta etapa.</span><span class="sxs-lookup"><span data-stu-id="a4371-190">If you are using a virtual smart card, skip this step.</span></span>
    
    <span data-ttu-id="a4371-191">Se estiver usando um cartão inteligente físico, insira o cartão inteligente no leitor de cartão inteligente quando solicitado e então clique em **OK** quando o cartão for detectado.</span><span class="sxs-lookup"><span data-stu-id="a4371-191">If you are using a physical smart card, insert the smart card into your smart card reader and prompted to do so, and then click **OK** when the card is detected.</span></span>

4.  <span data-ttu-id="a4371-192">Digite o número PIN do seu cartão inteligente e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4371-192">Type in the PIN number you for your smart card and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a4371-193">Se você não tiver recebido um número PIN de cartão inteligente do pessoal de suporte, use o valor padrão, que é 12345678.</span><span class="sxs-lookup"><span data-stu-id="a4371-193">If you were not assigned a smart card PIN number by your support person, use the default value, which is 12345678.</span></span>

    
    <span data-ttu-id="a4371-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a4371-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

