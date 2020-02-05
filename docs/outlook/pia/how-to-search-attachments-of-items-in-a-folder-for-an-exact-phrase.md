---
title: Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3d14da44731810308d57ba0e70f9651f3105aad0
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773715"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="465c0-102">Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck</span><span class="sxs-lookup"><span data-stu-id="465c0-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="465c0-103">In diesem Beispiel wird nach dem genauen Suchbegriff „office“ in Anlagen von Elementen im Posteingang gesucht.</span><span class="sxs-lookup"><span data-stu-id="465c0-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="465c0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="465c0-104">Example</span></span>

<span data-ttu-id="465c0-105">In diesem Codebeispiel wird eine DASL-Syntax (DAV Searching and Locating) zum Angeben einer Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="465c0-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="465c0-106">Um den Filter zu erstellen, überprüft das Codebeispiel zunächst, ob die Sofortsuche im Standardspeicher aktiviert ist, um festzustellen, ob das **ci\_phrasematch**-Schlüsselwort für eine genaue Übereinstimmung mit „office“ in einer Anlage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="465c0-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="465c0-107">In dem Beispiel wird der Filter dann auf die [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_)-Methode im Posteingang angewendet, und die Ergebnisse werden in einem [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia)-Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="465c0-107">The sample then applies the filter to the [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) method on the Inbox and obtains the results in a [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia) object.</span></span> <span data-ttu-id="465c0-108">Dann wird der Betreff der zurückgegebenen Elemente in der **Tabelle** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="465c0-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="465c0-109">Das Codebeispiel gibt die **Attachments**-Eigenschaft mithilfe der Namespace-Darstellung https://schemas.microsoft.com/mapi/proptag/0x0EA5001E an.</span><span class="sxs-lookup"><span data-stu-id="465c0-109">The code sample specifies the **Attachments** property of an item using the namespace representation, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="465c0-110">Die Syntax für die Verwendung des **ci\_phrasematch**-Schlüsselwortes lautet:</span><span class="sxs-lookup"><span data-stu-id="465c0-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="465c0-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="465c0-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="465c0-112">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="465c0-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="465c0-113">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="465c0-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="465c0-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="465c0-114">See also</span></span>

- [<span data-ttu-id="465c0-115">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="465c0-115">Search and filter</span></span>](search-and-filter.md)

