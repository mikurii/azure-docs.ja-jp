---
title: アカウントの 2 要素認証に関する一般的な問題 - Azure AD
description: 2 要素認証と職場または学校アカウントの一般的な問題のソリューション。
services: active-directory
author: curtand
manager: daveba
ms.assetid: 8f3aef42-7f66-4656-a7cd-d25a971cb9eb
ms.workload: identity
ms.service: active-directory
ms.subservice: user-help
ms.topic: conceptual
ms.date: 04/02/2020
ms.author: curtand
ms.reviewer: kexia
ms.openlocfilehash: 3df79fb1e103ddfaafeb348641e675cd250f5858
ms.sourcegitcommit: 530e2d56fc3b91c520d3714a7fe4e8e0b75480c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "81271694"
---
# <a name="common-problems-with-two-factor-verification-and-your-work-or-school-account"></a>2 要素認証と職場または学校アカウントの一般的な問題

Azure Active Directory (Azure AD) 組織が 2 要素認証を有効にすると、職場または学校アカウントのサインインには、ユーザー名、パスワード、モバイルデバイスまたはスマートフォンの組み合わせが必要になります。 ユーザーが知っているものとユーザーが所有するものの 2 つの形式の認証に依存するため、パスワードだけよりも安全性が高くなります。 2 要素認証は、悪意のあるハッカーによるなりすましを防ぐのに役立ちます。なぜなら、悪意のあるハッカーがあなたのパスワードを知っていたとしても、あなたのデバイスを持っていない可能性も高いためです。

<center>

![認証方法の概念画像](../authentication/media/concept-mfa-howitworks/methods.png)</center>

2 要素認証では、誰もがそうあってほしいと思うより頻繁に、一般的な問題が発生します。 このアーティクルでは、最も一般的な問題と、考えられる修正方法について説明します。

>[!Important]
>管理者の方は、 Azure AD 環境の設定と管理方法の詳細については、「[Azure AD のドキュメント](https://docs.microsoft.com/azure/active-directory)」をご参照ください。
>
>また、このコンテンツの対象は、職場または学校アカウント、つまり勤務先から支給されるアカウント (alain@contoso.com など) での使用のみです。 ご自身のために自分で設定するアカウント (danielle@outlook.com など) である個人用 Microsoft アカウントと 2 要素認証に関して問題がある場合は、[Microsoft アカウントの 2 要素認証を有効または無効にする方法](https://support.microsoft.com/help/4028586/microsoft-account-turning-two-step-verification-on-or-off)に関するページをご参照ください。

## <a name="i-dont-have-my-mobile-device-with-me"></a>自分のモバイル デバイスを持っていません

よくあることです。 自宅にモバイル デバイスを置いてきたため、電話を使って自分の身元を確認できません。 会社の電話などの別の方法を自分のアカウントへのサインイン用に以前に追加している場合は、ここでその方法を使用できます。 追加の検証方法を追加していない場合は、自分の組織のヘルプ デスクに連絡して、アカウントに戻るのを手伝ってもらう必要があります。

### <a name="to-sign-in-to-your-work-or-school-account-using-another-verification-method"></a>別の検証方法を使用して職場または学校アカウントにサインインするには

1. アカウントにサインインし、**2 要素認証**ページで **[別の方法でサインイン]** リンクを選択します。

    ![サインインの検証方法を変更する](./media/multi-factor-authentication-end-user-troubleshoot/two-factor-auth-signin-another-way.png)

    **[Sign in another way]\(別の方法でサインイン\)** リンクが表示されない場合は、他の検証方法を設定していないことを意味します。 アカウントにサインインするには、管理者に連絡してサポートを受ける必要があります。

2. 他の認証方法を選択し、2 要素認証を続行します。

## <a name="i-lost-my-mobile-device-or-it-was-stolen"></a>モバイル デバイスを紛失したか、または盗難にあいました

モバイル デバイスを紛失した場合、またはモバイル デバイスを盗まれた場合は、別の方法を使用してサインインするか、設定をクリアするように自分の組織のヘルプ デスクに依頼することができます。 アカウントを適切に更新できるように、携帯電話を紛失したこと、または携帯電話が盗難にあったことを、自分の組織のヘルプ デスクに知らせることを強くお勧めします。 設定が消去されると、次回のサインイン時に [2 要素認証の登録](multi-factor-authentication-end-user-first-time.md)を求めるメッセージが表示されます。

## <a name="im-not-getting-the-verification-code-sent-to-my-mobile-device"></a>モバイル デバイスに送信された確認コードを受け取っていません

確認コードを受け取れないのはよくある問題であり、通常はモバイル デバイスとその設定に関連しています。 いくつかのことを試してみてください。

これを試します | ガイダンス情報
--------- | ------------
モバイル デバイスを再起動します | 場合によっては、デバイスの更新だけで済むことがあります。 デバイスを再起動すると、現在実行されていて問題の原因になっている可能性があるバックグラウンド プロセスやサービスが終了すると共に、デバイスのコア コンポーネントが更新され、どこかでクラッシュしていた場合は再起動されます。
セキュリティ情報が正しいことを確認します | セキュリティ検証方法の情報が正確であること (特に電話番号) を確認します。 間違った電話番号を入力すると、すべてのアラートがその正しくない番号に送られます。 幸い、そのユーザーはアラートに対して何もできませんが、アカウントへのサインインにも役立ちません。 情報が正しいことを確認するには、「[2 要素認証方法の設定を管理する](multi-factor-authentication-end-user-manage-settings.md)」の記事の手順を参照してください。
通知が有効になっていることを確認します | モバイル デバイスで通知が有効になっていること、および電話、認証アプリ、およびメッセージング アプリ (テキスト メッセージの場合) を使用してモバイル デバイスに表示されるアラート通知を送信できる通知方法を選択していることを確認します。
デバイス信号とインターネット接続があることを確認します | 通話とテキスト メッセージがモバイル デバイスに送信されていることを確認します。 友人に頼んで、電話での呼び出しとテキスト メッセージの送信を行ってもらい、両方とも受信することを確認するします。 そうでない場合は、最初にモバイル デバイスの電源が入っていることを確認します。 デバイスの電源がオンになっているのに、通話やテキストを受け取れない場合は、ネットワークに問題がある可能性が高いため、プロバイダーに問い合わせる必要があります。 信号関連の問題が頻繁に発生する場合は、モバイル デバイスに [Microsoft Authenticator アプリ](user-help-auth-app-download-install.md)をインストールして使用することをお勧めします。 Authenticator アプリを使用すると、電波またはインターネット接続を必要とせずに、サインイン用のランダムなセキュリティ コードを生成できます。
応答不可をオフにします | モバイル デバイスの**応答不可**機能が有効になっていないことを確認します。 この機能が有効になっていると、モバイル デバイスで通知を受け取ることができません。 この機能を無効にする方法については、モバイル デバイスのマニュアルを参照してください。
電話番号をブロック解除します | 米国の場合、Microsoft からの音声通話は、+1 (866) 539 4191、+1 (855) 330 8653、+1 (877) 668 6536 から発信されます。
バッテリに関連する設定を確認します | これは少し奇妙に思えますが、バッテリの最適化を設定し、使用頻度の低いアプリがバックグラウンドでアクティブのままにならないようになっている場合、通知システムは影響を受ける可能性が最も高くなります。 この問題を解決するには、認証アプリとメッセージング アプリのバッテリ最適化を無効にしてから、もう一度アカウントにサインインしてみてください。
サードパーティ製のセキュリティ アプリを無効にします | 不明な発信者を最小限に抑えるためにテキスト メッセージや電話の呼び出しを保護するアプリがある場合、確認コードを受信できなくなる可能性があります。 お使いの電話でサードパーティ製のセキュリティ アプリを無効にしてから、確認コードをもう一度送信するように依頼してください。

## <a name="im-not-getting-prompted-for-my-second-verification-information"></a>2 番目の検証情報を求めるメッセージが表示されません

ユーザー名とパスワードを使用して職場または学校アカウントにサインインしていても、追加のセキュリティ確認情報の入力を求められない場合は、デバイスをまだセットアップしていない可能性があります。 特定の追加のセキュリティ検証方法を使用するように、モバイル デバイスを設定する必要があります。 モバイル デバイスが有効になっていること、および検証方法で使用できるようになっていることを確認するには、「[2 要素認証方法の設定を管理する](multi-factor-authentication-end-user-manage-settings.md)」の記事を参照してください。 デバイスまたはアカウントを設定していないことがわかっている場合は、[2 段階認証のアカウントの設定](multi-factor-authentication-end-user-first-time.md)に関する記事の手順に従って、これを行うことができます。

## <a name="i-got-a-new-phone-number-and-i-want-to-add-it"></a>新しい電話番号にしたので追加したい

電話番号が新しくなった場合は、検証プロンプトが適切な場所に送られるように、セキュリティ検証方法の詳細を更新する必要があります。 検証方法を更新するには、「[2 要素認証方法の設定を管理する](multi-factor-authentication-end-user-manage-settings.md#add-or-change-your-phone-number)」記事の「**電話番号を追加または変更する**」の手順に従います。

## <a name="i-got-a-new-mobile-device-and-i-want-to-add-it"></a>新しいモバイル デバイスを入手したので追加したい

新しいモバイル デバイスを入手した場合は、2 要素認証で動作するように設定する必要があります。 これはマルチステップのソリューションです。

1. [2 段階認証のアカウントの設定](multi-factor-authentication-end-user-first-time.md)に関する記事の手順に従って、職場または学校アカウントで動作するようにデバイスを設定します。

1. **[追加のセキュリティ確認]** ページでアカウントとデバイスの情報を更新し、古いデバイスを削除して新しいデバイスを追加します。 詳しくは、「[2 要素認証方法の設定を管理する](multi-factor-authentication-end-user-manage-settings.md)」を参照してください。

省略可能な手順:

- 「[Microsoft Authenticator アプリのダウンロードとインストール](user-help-auth-app-download-install.md)」の手順に従って、モバイル デバイスに Microsoft Authenticator アプリをダウンロードしてインストールし、セットアップします。

- 信頼されたデバイスの 2 要素認証を有効にするには、「[2 要素認証方法の設定を管理する](multi-factor-authentication-end-user-manage-settings.md#turn-on-two-factor-verification-prompts-on-a-trusted-device)」の「**信頼されたデバイスで 2 要素認証のプロンプトを有効にする**」に関する手順に従います。

## <a name="im-having-problems-signing-in-on-my-mobile-device-while-traveling"></a>旅行中にモバイル デバイスにサインインするときに問題が発生します

外国にいるときは、テキスト メッセージングなどのモバイル デバイス関連の検証方法を使用するのが難しい場合があります。 また、モバイル デバイスでローミング料金が発生する可能性もあります。 このような状況では、Wi-Fi ホットスポット接続オプションを有効にして Microsoft Authenticator アプリを使用することをお勧めします。 モバイル デバイスに Microsoft Authenticator アプリをダウンロードしてインストールし、セットアップする方法について詳しくは、「[Microsoft Authenticator アプリのダウンロードとインストール](user-help-auth-app-download-install.md)」をご覧ください。

## <a name="i-cant-get-my-app-passwords-to-work"></a>アプリ パスワードを動作させることができません

2 要素認証がサポートされていない古いバージョンのデスクトップ アプリケーションでは、アプリ パスワードによって通常のパスワードが置き換えられます。 まず、パスワードを正しく入力したことを確認してください。 それでも問題が解決しない場合は、「[2 段階認証のアプリ パスワードを管理する](multi-factor-authentication-end-user-app-passwords.md#create-and-delete-app-passwords-from-the-additional-security-verification-page)」の「**MyApps ポータルを使用してアプリ パスワードを作成および削除する**」の手順に従って、アプリの新しいアプリ パスワードを作成してみてください。

## <a name="i-cant-turn-two-factor-verification-off"></a>2 要素認証を無効にできません

職場または学校のアカウント (alain@contoso.com など) で 2 要素認証を使用している場合、追加したこのセキュリティ機能を使用しなければならないと組織が決定している可能性があります。 この機能を使用しなければならないことは組織の決定であるため、個人でこれを無効にすることはできません。 ただし、alain@outlook.com のような個人アカウントで 2 要素認証を使用している場合は、この機能の有効/無効を切り替えることができます。 個人のアカウントに対する 2 要素認証を制御する方法については、[Microsoft アカウントの 2 段階認証を有効または無効にする](https://support.microsoft.com/help/4028586/microsoft-account-turning-two-step-verification-on-or-off)に関するページをご覧ください。

2 要素認証を無効にできない場合は、組織レベルで適用されているセキュリティの既定値群が原因である可能性もあります。 セキュリティの既定値群の詳細については、「[セキュリティ デフォルトとは](../fundamentals/concept-fundamentals-security-defaults.md)」を参照してください。

## <a name="i-didnt-find-an-answer-to-my-problem"></a>問題に対する回答が見つからなかった場合

これらの手順を試してもまだ問題が発生する場合は、自分の組織のヘルプ デスクに連絡してサポートを受けてください。

## <a name="related-articles"></a>関連記事

- [2 要素認証方法の設定を管理する](multi-factor-authentication-end-user-manage-settings.md)

- [アカウントへの 2 段階認証の設定](multi-factor-authentication-end-user-first-time.md)

- [Microsoft Authenticator アプリに関する FAQ](user-help-auth-app-faq.md)
