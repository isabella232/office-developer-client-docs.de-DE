---
title: Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 074a3eb7b83e4556b41549d18b81c97b96db1e6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407100"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a>Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage

In diesem Beispiel wird ein E-Mail-Element mit der [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\))-Methode erstellt.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird die Vorlagendatei „Ivy.oft“ geöffnet, ein Betreff zugewiesen und die Nachricht dann im Ordner „Entwürfe“ gespeichert.

Die **CreateItemFromTemplate**-Methode ist nützlich, wenn Sie eine auf einem Datenträger gespeicherte Outlook-Vorlagendatei (OFT-Datei) als Nachrichtenvorlage verwenden möchten. Die Vorlagendatei kann vorformatierten Text, Briefpapier oder Bilder enthalten, die Sie in die Nachricht aufnehmen möchten. Enthält die Vorlagendatei jedoch Code hinter dem Formular, wird der Formularcode nicht ausgeführt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateItemFromTemplate()
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderDrafts), Outlook.Folder)
    Dim mail As Outlook.MailItem = _
        CType(Application.CreateItemFromTemplate( _
        "c:\ivy.oft", folder), Outlook.MailItem)
    mail.Subject = "Congratulations"
    mail.Save()
End Sub
```


```csharp
private void CreateItemFromTemplate()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderDrafts) as Outlook.Folder;
    Outlook.MailItem mail =
        Application.CreateItemFromTemplate(
        @"c:\ivy.oft", folder) as Outlook.MailItem;
    mail.Subject = "Congratulations";
    mail.Save();
}
```

## <a name="see-also"></a>Siehe auch

- [Mail](mail.md)

