---
title: Erstellen einer Verteilerliste
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a83090f721d9afa9c1844f8e8aa828bec34e2d35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623775"
---
# <a name="create-a-distribution-list"></a>Erstellen einer Verteilerliste

In diesem Beispiel wird veranschaulicht, wie eine Verteilerliste erstellt und dem Benutzer angezeigt wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Im folgenden Codebeispiel wird von CreateDistributionList eine Verteilerliste erstellt, indem durch Aufrufen der [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\))-Methode ein [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\))-Objekt erstellt wird. Anschließend wird ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt erstellt und die [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\))-Methode aufgerufen, um alle Kontakte im Standardordner für Kontakte zu finden, deren Wert der [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\))-Eigenschaft "Top Customer" lautet und deren Wert der [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\))-Eigenschaft nicht leer ist. Nachdem alle Kontakte identifiziert wurden, wird der **Email1Address**-Name wird als eine Spalte zur **Tabelle** hinzugefügt. Dann erstellt CreateDistributionList ein [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekt mithilfe der [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts. Schließlich zeigt CreateDistributionList dem Benutzer die Verteilerliste "Top Customers" an.

> [!NOTE] 
> Sie müssen ein aufgelöstes **Recipient**-Objekt als Parameter für die [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15))-Methode des [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15))-Objekts übergeben. Zum Auflösen eines **Empfänger**-Objekts verwenden Sie die [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15))-Methode.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a>Siehe auch

- [Exchange-Benutzer](exchange-users.md)

