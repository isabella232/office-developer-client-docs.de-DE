---
title: Suchen nach einem Ausdruck im Textkörper von Elementen in einem Ordner
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c083e11034324f0be80d56a714635ee265914a2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608949"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a>Suchen nach einem Ausdruck im Textkörper von Elementen in einem Ordner

In diesem Beispiel wird nach der Zeichenfolge „Office“ im Textkörper der Elemente im Posteingang gesucht.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird eine DASL-Syntax (DAV Searching and Locating) zum Angeben einer Abfrage verwendet. Um den Filter zu erstellen, überprüft das Codebeispiel zunächst, ob die Sofortsuche im Standardspeicher aktiviert ist, um zu ermitteln, ob das **ci\_phrasematch**-Schlüsselwort für eine genaue Übereinstimmung mit „office“ im Textkörper oder das **like**-Schlüsselwort für eine Übereinstimmung mit einem beliebigen Vorkommen von „Office“ als genaue Zeichenfolge oder eine Teilzeichenfolge im Textkörper verwendet werden soll. In dem Beispiel wird der Filter dann auf die [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode im Posteingang angewendet, und die Ergebnisse werden in einem [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt abgerufen. Dann wird der Betreff der zurückgegebenen Elemente in **Tabelle** angezeigt.

Das Codebeispiel gibt die **Body**-Eigenschaft mithilfe der Namespace-Darstellung urn:schemas:httpmail:textdescription an. 

Die Syntax für die Verwendung des **ci\_phrasematch**-Schlüsselwortes lautet:

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

Die Syntax für die Verwendung des **like**-Schlüsselworts für die Präfixübereinstimmung lautet:

`<PropertySchemaName> like <Token>%`

Die Syntax für die Verwendung des **like**-Schlüsselworts für die Übereinstimmung mit einer beliebigen Teilzeichenfolge lautet:

`<PropertySchemaName> like %<Token>%`

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die **Imports**- oder **using**-Anweisung darf nicht direkt vor den Funktionen im Codebeispiel stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchBody()
    Dim filter As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " ci_phrasematch 'office'"
    Else
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " like '%office%'"
    End If
    Dim table As Outlook.Table = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
        filter, Outlook.OlTableContents.olUserItems)
    While Not (table.EndOfTable)
        Dim row As Outlook.Row = table.GetNextRow()
        Debug.WriteLine(row("Subject"))
    End While
End Sub
```


```csharp
private void DemoSearchBody()
{
    string filter;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " ci_phrasematch 'office'";
    }
    else
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " like '%office%'";
    }
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

