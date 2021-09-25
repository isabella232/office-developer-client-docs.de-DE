---
title: Erstellen eines Kontaktelements aus einer vCard-Datei und Speichern des Elements in einem Ordner
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7ced53d60b67d75caedccbb87b83947861d25f9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623796"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a>Erstellen eines Kontaktelements aus einer vCard-Datei und Speichern des Elements in einem Ordner

In diesem Beispiel werden alle vCard-Dateien aus einem Dateisystemordner importiert und die Kontakte im durch den *targetFolder*-Parameter angegebenen Ordner gespeichert.

## <a name="example"></a>Beispiel

In dem Beispiel wird die [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\))-Methode verwendet. Die **OpenSharedItem**-Methode öffnet Nachrichten, die als Dateien im Outlook-Nachrichtenformat (MSG), iCalendar-Termindateien (ICS) oder vCard-Dateien (VCF) gespeichert sind. Vergessen Sie nicht, das zurückgegebene Objekt in den entsprechenden Elementtyp umzuwandeln und die entsprechende **Save**-Methode aufzurufen, um das Element dauerhaft zu speichern. Standardmäßig wird das von **OpenSharedItem** zurückgegebene Element im Standardordner für den jeweiligen Elementtyp gespeichert. Sie können das Element mit der entsprechenden **Move**-Methode in einen anderen Ordner verschieben.

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die **Imports**- oder **using**-Anweisung darf nicht direkt vor den Funktionen im Codebeispiel stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ImportContacts( _
    ByVal path As String, ByVal targetFolder As Outlook.Folder)
    Dim contact As Outlook.ContactItem
    Dim moveContact As Outlook.ContactItem
    If (Directory.Exists(path)) Then
        Dim files As String() = Directory.GetFiles(path, "*.vcf")
        For Each file As String In files
            contact = CType(Application.Session.OpenSharedItem(file), _
                Outlook.ContactItem)
            If (targetFolder Is _
                CType(Application.Session.GetDefaultFolder( _
                    Outlook.OlDefaultFolders.olFolderContacts) _
                    , Outlook.Folder)) Then
                contact.Save()
            Else
                moveContact = CType(contact.Move(targetFolder), _
                    Outlook.ContactItem)
                moveContact.Save()
            End If
        Next
    End If
End Sub
```


```csharp
private void ImportContacts(string path, Outlook.Folder targetFolder)
{
    Outlook.ContactItem contact;
    Outlook.ContactItem moveContact;
    if (Directory.Exists(path))
    {
        string[] files = Directory.GetFiles(path, "*.vcf");
        foreach (string file in files)
        {
            contact = Application.Session.OpenSharedItem(file)
                as Outlook.ContactItem;
            if (targetFolder ==
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderContacts)
                as Outlook.Folder)
            {
                contact.Save();
            }
            else
            {
                moveContact = contact.Move(targetFolder)
                    as Outlook.ContactItem;
                moveContact.Save();
            }
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Kontakte](contacts.md)

