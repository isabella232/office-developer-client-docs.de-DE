---
title: Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4e69d1a4bda4d4bab1b84a9c29214ca31549b82f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629410"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a>Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage

In diesem Beispiel wird ein E-Mail-Element mit der [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\))-Methode erstellt.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird die Vorlagendatei „Ivy.oft“ geöffnet, ein Betreff zugewiesen und die Nachricht dann im Ordner „Entwürfe“ gespeichert.

Die **CreateItemFromTemplate**-Methode ist nützlich, wenn Sie eine auf einem Datenträger gespeicherte Outlook-Vorlagendatei (OFT-Datei) als Nachrichtenvorlage verwenden möchten. Die Vorlagendatei kann vorformatierten Text, Briefpapier oder Bilder enthalten, die Sie in die Nachricht aufnehmen möchten. Enthält die Vorlagendatei jedoch Code hinter dem Formular, wird der Formularcode nicht ausgeführt.

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die **Imports**- oder **using**-Anweisung darf nicht direkt vor den Funktionen im Codebeispiel stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

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

