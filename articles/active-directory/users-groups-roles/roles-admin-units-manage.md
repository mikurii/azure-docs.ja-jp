---
title: 管理単位を追加および削除する (プレビュー) - Azure Active Directory | Microsoft Docs
description: Azure Active Directory で管理単位を使用してロールのアクセス許可のスコープを制限します。
services: active-directory
documentationcenter: ''
author: curtand
manager: daveba
ms.service: active-directory
ms.topic: article
ms.subservice: users-groups-roles
ms.workload: identity
ms.date: 04/16/2020
ms.author: curtand
ms.reviewer: anandy
ms.custom: oldportal;it-pro;
ms.collection: M365-identity-device-management
ms.openlocfilehash: 7a4a0dfaeda18b3f68ddc3c7cc7333b8c994d174
ms.sourcegitcommit: 849bb1729b89d075eed579aa36395bf4d29f3bd9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2020
ms.locfileid: "81684911"
---
# <a name="manage-administrative-units-in-azure-active-directory"></a>Azure Active Directory で管理単位を管理する

Azure Active Directory (Azure AD) では、きめ細かい管理制御を行うために、1 つ以上の管理単位 (AU) に制限されたスコープでユーザーを Azure AD ロールに割り当てることができます。

## <a name="get-started"></a>はじめに

1. [Graph Explorer](https://aka.ms/ge) を使用して以降の手順からクエリを実行するには、以下を実行してください。

    a. Azure Portal で、Azure AD に移動します。 アプリケーションの一覧で **[Graph Explorer]** を選択して、 **[Grant admin consent to Graph Explorer]\(Graph Explorer に管理者の同意を付与する\)** を指定します。

    !["管理者の同意を付与する" へのリンクを示すスクリーンショット](./media/roles-admin-units-manage/select-graph-explorer.png)

    b. Graph Explorer で、 **[ベータ]** バージョンを選択します。

    ![ベータ版が選択されていることを示すスクリーンショット](./media/roles-admin-units-manage/select-beta-version.png)

1. Azure AD PowerShell のプレビュー版を使用します。

## <a name="add-an-administrative-unit"></a>管理単位を追加する

### <a name="use-the-azure-portal"></a>Azure ポータルの使用

1. Azure portal で、Azure AD に移動し、左側のペインで **[管理単位]** を選択します。

    ![Azure AD の [管理単位] (プレビュー) リンクのスクリーンショット](./media/roles-admin-units-manage/nav-to-admin-units.png)

1. **[追加]** を選択してから、管理単位の名前を入力します。 必要に応じて、管理単位の説明を追加します。

    ![[追加] ボタンと、管理単位の名前を入力するためのテキスト ボックスのスクリーンショット](./media/roles-admin-units-manage/add-new-admin-unit.png)

1. **[追加]** を選択して管理単位を最終処理します。

### <a name="use-powershell"></a>PowerShell の使用

次のコマンドを実行する前に Azure AD PowerShell (プレビュー) をインストールします。

    Connect-AzureAD
    New-AzureADAdministrativeUnit -Description "West Coast region" -DisplayName "West Coast"

必要に応じて、引用符で囲まれた値を変更できます。

### <a name="use-microsoft-graph"></a>Microsoft Graph の使用

    Http Request
    POST /administrativeUnits
    Request body
    {
        "displayName": "North America Operations",
        "description": "North America Operations administration"
    }

## <a name="remove-an-administrative-unit"></a>管理単位を削除する

Azure AD では、管理ロールのスコープの単位として不要になった管理単位を削除できます。

### <a name="use-the-azure-portal"></a>Azure ポータルの使用

1. Azure portal で、 **[Azure AD]**  >  **[管理単位]** にアクセスします。 
1. 削除する管理単位を選択してから、 **[削除]** を選択します。 
1. 管理単位の削除を確認するには、 **[はい]** を選択します。 管理単位が削除されます。

![管理単位の [削除] ボタンと確認ウィンドウのスクリーンショット](./media/roles-admin-units-manage/select-admin-unit-to-delete.png)

### <a name="use-powershell"></a>PowerShell の使用

    $delau = Get-AzureADAdministrativeUnit -Filter "displayname eq 'DeleteMe Admin Unit'"
    Remove-AzureADAdministrativeUnit -ObjectId $delau.ObjectId

特定の環境で必要に応じて、引用符で囲まれた値を変更できます。

### <a name="use-the-graph-api"></a>Graph API の使用

    HTTP request
    DELETE /administrativeUnits/{Admin id}
    Request body
    {}

## <a name="next-steps"></a>次のステップ

* [管理単位のユーザーを管理する](roles-admin-units-add-manage-users.md)
* [管理単位のグループを管理する](roles-admin-units-add-manage-groups.md)
