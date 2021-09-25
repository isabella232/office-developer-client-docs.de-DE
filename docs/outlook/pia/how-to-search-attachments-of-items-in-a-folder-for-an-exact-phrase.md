---
title: Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 09/14/2021
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 932af6a8af1ee6a1f6be93f0aff4f3c7267fc151
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623649"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a>Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck

In diesem Beispiel wird nach dem genauen Suchbegriff „office“ in Anlagen von Elementen im Posteingang gesucht.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird eine DASL-Syntax (DAV Searching and Locating) zum Angeben einer Abfrage verwendet. Um den Filter zu erstellen, überprüft das Codebeispiel zunächst, ob die Sofortsuche im Standardspeicher aktiviert ist, um festzustellen, ob das **ci\_phrasematch**-Schlüsselwort für eine genaue Übereinstimmung mit „office“ in einer Anlage verwendet werden soll. In dem Beispiel wird der Filter dann auf die [GetTable](/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable.md)-Methode im Posteingang angewendet, und die Ergebnisse werden in einem [Table](/dotnet/api/microsoft.office.interop.outlook.table.md)-Objekt abgerufen. Dann wird der Betreff der zurückgegebenen Elemente in der **Tabelle** angezeigt.

Das Codebeispiel gibt die **Attachments**-Eigenschaft mithilfe der Namespace-Darstellung https://schemas.microsoft.com/mapi/proptag/0x0EA5001E an. Die Syntax für die Verwendung des **ci\_phrasematch**-Schlüsselwortes lautet:

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die **Imports**- oder **using**-Anweisung darf nicht direkt vor den Funktionen im Codebeispiel stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```

```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)
