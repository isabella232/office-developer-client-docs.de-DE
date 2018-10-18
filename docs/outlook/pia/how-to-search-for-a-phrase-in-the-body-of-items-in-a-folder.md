---
title: Suchen nach einem Ausdruck im Textkörper von Elementen in einem Ordner
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2792e5bd96547975d878f89a7e186c24c4983d8f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406932"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a><span data-ttu-id="e90d0-102">Suchen nach einem Ausdruck im Textkörper von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="e90d0-102">Search for a phrase in the body of items in a folder</span></span>

<span data-ttu-id="e90d0-103">In diesem Beispiel wird nach der Zeichenfolge „Office“ im Textkörper der Elemente im Posteingang gesucht.</span><span class="sxs-lookup"><span data-stu-id="e90d0-103">This example searches for the string "office" in the Body of items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="e90d0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e90d0-104">Example</span></span>

<span data-ttu-id="e90d0-105">In diesem Codebeispiel wird eine DASL-Syntax (DAV Searching and Locating) zum Angeben einer Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="e90d0-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="e90d0-106">Um den Filter zu erstellen, überprüft das Codebeispiel zunächst, ob die Sofortsuche im Standardspeicher aktiviert ist, um zu ermitteln, ob das **ci\_phrasematch**-Schlüsselwort für eine genaue Übereinstimmung mit „office“ im Textkörper oder das **like**-Schlüsselwort für eine Übereinstimmung mit einem beliebigen Vorkommen von „Office“ als genaue Zeichenfolge oder eine Teilzeichenfolge im Textkörper verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e90d0-106">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query. To construct the filter, the code sample first checks if Instant Search is enabled in the default store to determine whether to use the ci_phrasematch keyword for an exact phrase match of "office" in the item body, or the like keyword to match any occurrence of "office" as an exact string or a substring in the item body. The sample then applies the filter to the GetTable method on the Inbox and obtains the results in a Table object. The code sample then displays the subject of each of the returned items in the Table.</span></span> <span data-ttu-id="e90d0-107">In dem Beispiel wird der Filter dann auf die [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode im Posteingang angewendet, und die Ergebnisse werden in einem [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e90d0-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="e90d0-108">Dann wird der Betreff der zurückgegebenen Elemente in **Tabelle** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e90d0-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="e90d0-109">Das Codebeispiel gibt die **Body**-Eigenschaft mithilfe der Namespace-Darstellung urn:schemas:httpmail:textdescription an. </span><span class="sxs-lookup"><span data-stu-id="e90d0-109">The code sample specifies the Body property by using the namespace representation urn:schemas:httpmail:textdescription.</span></span>

<span data-ttu-id="e90d0-110">Die Syntax für die Verwendung des **ci\_phrasematch**-Schlüsselwortes lautet:</span><span class="sxs-lookup"><span data-stu-id="e90d0-110">The syntax for using the ci_phrasematch keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="e90d0-111">Die Syntax für die Verwendung des **like**-Schlüsselworts für die Präfixübereinstimmung lautet:</span><span class="sxs-lookup"><span data-stu-id="e90d0-111">The syntax for using the **like** keyword for prefix matching is:</span></span>

`<PropertySchemaName> like <Token>%`

<span data-ttu-id="e90d0-112">Die Syntax für die Verwendung des **like**-Schlüsselworts für die Übereinstimmung mit einer beliebigen Teilzeichenfolge lautet:</span><span class="sxs-lookup"><span data-stu-id="e90d0-112">The syntax for using the **like** keyword for any substring matching is:</span></span>

`<PropertySchemaName> like %<Token>%`

<span data-ttu-id="e90d0-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="e90d0-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="e90d0-114">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e90d0-114">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="e90d0-115">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e90d0-115">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e90d0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e90d0-116">See also</span></span>

- [<span data-ttu-id="e90d0-117">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="e90d0-117">Search and Filter</span></span>](search-and-filter.md)

