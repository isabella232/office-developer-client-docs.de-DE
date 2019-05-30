---
title: Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609825(v=office.15)
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 615b90a8423493a9e202e51993eea1c8127a9939
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540896"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="4628b-102">Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck</span><span class="sxs-lookup"><span data-stu-id="4628b-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="4628b-103">In diesem Beispiel wird nach dem genauen Suchbegriff „office“ in Anlagen von Elementen im Posteingang gesucht.</span><span class="sxs-lookup"><span data-stu-id="4628b-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="4628b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4628b-104">Example</span></span>

<span data-ttu-id="4628b-105">In diesem Codebeispiel wird eine DASL-Syntax (DAV Searching and Locating) zum Angeben einer Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="4628b-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="4628b-106">Um den Filter zu erstellen, überprüft das Codebeispiel zunächst, ob die Sofortsuche im Standardspeicher aktiviert ist, um festzustellen, ob das **ci\_phrasematch**-Schlüsselwort für eine genaue Übereinstimmung mit „office“ in einer Anlage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4628b-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="4628b-107">In dem Beispiel wird der Filter dann auf die [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode im Posteingang angewendet, und die Ergebnisse werden in einem [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4628b-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="4628b-108">Dann wird der Betreff der zurückgegebenen Elemente in der **Tabelle** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4628b-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="4628b-109">Das Codebeispiel gibt die **Attachments**-Eigenschaft mithilfe der Namespace-Darstellung http://schemas.microsoft.com/mapi/proptag/0x0EA5001E an.</span><span class="sxs-lookup"><span data-stu-id="4628b-109">The code sample specifies the **Attachments** property of an item using the namespace representation, http://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="4628b-110">Die Syntax für die Verwendung des **ci\_phrasematch**-Schlüsselwortes lautet:</span><span class="sxs-lookup"><span data-stu-id="4628b-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="4628b-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="4628b-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4628b-112">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4628b-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4628b-113">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="4628b-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="4628b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4628b-114">See also</span></span>

- [<span data-ttu-id="4628b-115">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="4628b-115">Search and filter</span></span>](search-and-filter.md)

