---
title: Anzeigen Sie des Adressbuchs, das einem Ordner „Kontakte“ entspricht, im Dialogfeld „Namen auswählen“
TOCTitle: Display in the Select Names dialog box the address book corresponding to a Contacts folder
ms:assetid: 6cbfc843-51b5-4841-bbb1-14b93a35ba78
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610437(v=office.15)
ms:contentKeyID: 55119799
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 8aa7093b26366f5aa47ce054b27eff04d48889b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405791"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a>Anzeigen Sie des Adressbuchs, das einem Ordner „Kontakte“ entspricht, im Dialogfeld „Namen auswählen“

In diesem Beispiel wird gezeigt, wie ein Adressbuch, das dem standardmäßigen Kontaktordner entspricht, abgerufen wird und wie dieses Adressbuch im Dialogfeld **Namen auswählen** angezeigt wird.

## <a name="example"></a>Beispiel

Jedes Adressbuch in Outlook wird von der [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) -Eigenschaft des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts als Sammlung dargestellt. Das Codebeispiel verwendet die [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) -Methode des [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) -Objekts zum Auffinden der Kontaktordner, die den Adresslisten entsprechen. Jeder Outlook-Ordner verfügt über eine Eintrags-ID. Vergleichen Sie die Eintrags-ID des standardmäßigen Kontaktordners mit der Eintrags-ID anderer Kontaktordner, um das AddressList-Element zu erzeugen, das dem standardmäßigen Kontaktordner entspricht.

Bevor die dem standardmäßigen Kontaktordner entsprechende Adressliste im Dialogfeld **Namen auswählen** angezeigt wird, legt das Codebeispiel den Wert auf den der [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) -Eigenschaft des [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) -Objekts fest.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ShowContactsFolderAsInitialAddressList()
    Dim addrLists As Outlook.AddressLists
    Dim contactsFolder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts), _
        Outlook.Folder)
    addrLists = Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        Dim testFolder As Outlook.Folder = _
        CType(addrList.GetContactsFolder(), Outlook.Folder)
        If Not (testFolder Is Nothing) Then
            ' Test to determine if Folder returned
            ' by GetContactsFolder has same EntryID
            ' as default Contacts folder.
            If (Application.Session.CompareEntryIDs( _
                contactsFolder.EntryID, testFolder.EntryID)) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.InitialAddressList = addrList
                snd.Display()
            End If
        End If
    Next
End Sub
```


```csharp
private void ShowContactsFolderAsInitialAddressList()
{
    Outlook.AddressLists addrLists;
    Outlook.Folder contactsFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    addrLists = Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        Outlook.Folder testFolder =
            addrList.GetContactsFolder() as Outlook.Folder;
        if (testFolder != null)
        {
            // Test to determine if Folder returned
            // by GetContactsFolder has same EntryID
            // as default Contacts folder.
            if (Application.Session.CompareEntryIDs(
                contactsFolder.EntryID, testFolder.EntryID))
            {
                Outlook.SelectNamesDialog snd =
                    Application.
                    Session.GetSelectNamesDialog();
                snd.InitialAddressList = addrList;
                snd.Display();
             }
         }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Adressbuch](address-book.md)

