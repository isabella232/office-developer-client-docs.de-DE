---
title: Abrufen der Standardnachrichtenklasse eines Ordners
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 78646e5ef2263d7478eb3caf54c83d41e4eff890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583142"
---
# <a name="get-the-default-message-class-of-a-folder"></a>Abrufen der Standardnachrichtenklasse eines Ordners

In diesem Beispiel wird gezeigt, wie die [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\))-Eigenschaft verwendet wird, um die Standardnachrichtenklasse eines Ordners abzurufen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Verwenden Sie die **DefaultMessageClass**-Eigenschaft des [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\))-Objekts, um die Standardnachrichtenklasse eines Ordners abzurufen. Ein [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt mit der **DefaultMessageClass** „IPM.Contact“ bedeutet beispielsweise, dass es einen Ordner „Kontakte“ darstellt. Wenn der Ordner jedoch ein benutzerdefiniertes Formular aufweist oder ein Ersatzformular ein Standardformular aufweist, müssen Sie das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt verwenden, um die Nachrichtenklasse des Standardformulars zu ermitteln. Die **DefaultMessageClass**-Eigenschaft gibt nicht die Nachrichtenklasse des Standardformulars für den Ordner zurück.

Im folgenden Codebeispiel ermittelt die GetDefaultMessageClass-Prozedur anhand der **PropertyAccessor**-Klasse das Standardformular für einen Ordner. Wenn die Ordnereigenschaft **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) nicht gefunden wird und in Outlook ein Fehler ausgelöst wird, gibt der **try…catch**-Block die **DefaultMessageClass**-Eigenschaft für das **Folder**-Objekt zurück.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"http://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Folders](folders.md)

