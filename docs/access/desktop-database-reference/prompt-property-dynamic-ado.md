---
title: Refrom Dynamic Property (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 261ac5640b5239f27ad91e01d1cb23794f88740a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301323"
---
# <a name="prompt-dynamic-property-ado"></a><span data-ttu-id="a1d74-102">Refrom Dynamic Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="a1d74-102">Prompt dynamic property (ADO)</span></span>

<span data-ttu-id="a1d74-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1d74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1d74-104">Es wird angegeben, ob der OLE DB-Anbieter den Benutzer zur Angabe von Initialisierungsinformationen auffordern sollte.</span><span class="sxs-lookup"><span data-stu-id="a1d74-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a1d74-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a1d74-105">Settings and return values</span></span>

<span data-ttu-id="a1d74-106">Mit dieser Eigenschaft wird ein [ConnectPromptEnum](connectpromptenum.md)-Wert festgelegt und zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1d74-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d74-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1d74-107">Remarks</span></span>

<span data-ttu-id="a1d74-p101">**Prompt** ist eine dynamische Eigenschaft, die vom OLE DB-Anbieter an die [Properties](connection-object-ado.md)-Auflistung des [Connection](properties-collection-ado.md)-Objekts angefügt werden kann. Für die Aufforderung zur Eingabe von Initialisierungsinformationen zeigen OLE DB-Anbieter dem Benutzer normalerweise ein Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="a1d74-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="a1d74-p102">Dynamische Eigenschaften eines [Connection](connection-object-ado.md)-Objekts gehen beim Schließen des **Connection** -Objekts verloren. Die **Prompt** -Eigenschaft muss vor dem erneuten Öffnen des **Connection** -Objekts zurückgesetzt werden, um einen anderen als den Standardwert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1d74-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>

> [!NOTE]
> <span data-ttu-id="a1d74-p103">[!HINWEIS] In Fällen, in denen der Benutzer nicht auf das Dialogfeld reagieren kann, sollten Sie nicht festlegen, dass der Anbieter den Benutzer zur Eingabe auffordern soll. Beispielsweise kann der Benutzer nicht reagieren, wenn die Anwendung nicht auf dem Client des Benutzers, sondern auf einem Serversystem ausgeführt wird, oder wenn die Anwendung auf einem System ohne angemeldeten Benutzer ausgeführt wird. In diesen Fällen wartet die Anwendung unbegrenzt auf eine Antwort und ist scheinbar abgestürzt.</span><span class="sxs-lookup"><span data-stu-id="a1d74-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span>

<span data-ttu-id="a1d74-115">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="a1d74-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
