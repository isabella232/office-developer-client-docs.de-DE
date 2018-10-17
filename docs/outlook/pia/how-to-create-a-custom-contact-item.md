---
title: Erstellen eines benutzerdefinierten Kontaktelements
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 189be01e6e690ad1db3d58d58837ab418b4c2e74
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407345"
---
# <a name="create-a-custom-contact-item"></a>Erstellen eines benutzerdefinierten Kontaktelements

In diesem Beispiel wird gezeigt, wie ein benutzerdefiniertes Kontaktelement erstellt wird und sowohl vordefinierte als auch benutzerdefinierte Eigenschaften festgelegt werden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Ein [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Objekt stellt einen Kontakt im Ordner „Kontakte“ dar und verfügt über mehr als 100 integrierte Eigenschaften, wie z. B. [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) und [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)). Manchmal sind die integrierten Eigenschaften nicht ausreichend, und Sie müssen benutzerdefinierte Eigenschaften hinzufügen, wozu Sie die [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\))-Sammlung verwenden können.

Im folgenden Codebeispiel erstellt CreateCustomItem erstellt ein benutzerdefiniertes **ContactItem**-Objekt, gibt ihm den Namen „Shoe Store“ und ruft die [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\))-Methode auf, um es einem Ordner mit dem Namen „Shoe Store“ hinzuzufügen. CreateCustomItem ruft zunächst den Ordner „Shoe Store“ mithilfe der [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\))-Methode ab. Der Ordner „Shoe Store“ ist ein Unterordner des Standardordners für Kontakte. CreateCustomItem legt dann die Eigenschaften **FirstName** und **LastName** fest und erstellt eine benutzerdefinierte Eigenschaft („Shoe Size“) mithilfe der **UserProperties**-Sammlung.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a>Siehe auch

- [Kontakte](contacts.md)

