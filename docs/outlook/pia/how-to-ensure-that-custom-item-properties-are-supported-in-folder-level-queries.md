---
title: Sicherstellen, dass benutzerdefinierte Elementeigenschaften in Abfragen auf Ordnerebene unterstützt werden
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcba2648988d2de3c208079d2845e2cb4c2f549
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319089"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a><span data-ttu-id="91db4-102">Sicherstellen, dass benutzerdefinierte Elementeigenschaften in Abfragen auf Ordnerebene unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="91db4-102">Ensure that custom item properties are supported in folder-level queries</span></span>

<span data-ttu-id="91db4-103">In diesem Beispiel wird gezeigt, wie Sie sicherstellen, dass beim Hinzufügen einer benutzerdefinierten Eigenschaft zu einem Elementtyp die Eigenschaft auch dem Ordner hinzugefügt wird, sodass Sie auf Ordnerebene eine Abfrage nach dieser benutzerdefinierten Eigenschaft ausführen können.</span><span class="sxs-lookup"><span data-stu-id="91db4-103">This example shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

## <a name="example"></a><span data-ttu-id="91db4-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91db4-104">Example</span></span>

<span data-ttu-id="91db4-105">In diesem Codebeispiel wird veranschaulicht, wie Sie mithilfe des [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) -Objekts und des [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) -Objekts sicherstellen können, dass eine Eigenschaft, die Sie einer benutzerdefinierten Eigenschaft hinzufügen, auch gleichzeitig dem Ordner hinzugefügt wird, sodass Sie auf der Ordnerebene eine Abfrage nach dieser benutzerdefinierten Eigenschaft ausführen können.</span><span class="sxs-lookup"><span data-stu-id="91db4-105">This code sample shows how to use the [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) object and the [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) object to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

<span data-ttu-id="91db4-106">Wenn Sie die [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\))-Methode in der [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\))-Auflistung verwenden, um eine benutzerdefinierte Eigenschaft zu einem Element hinzuzufügen, können Sie den *AddToFolderFields*-Parameter auf **true** festlegen, damit die Eigenschaft zu dem Ordner hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="91db4-106">When you use the [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) method on the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection to add a custom property to an item, you can specify the *AddToFolderFields* parameter as **true** to add the property to the folder.</span></span> <span data-ttu-id="91db4-107">Die benutzerdefinierte Eigenschaft wird jedoch möglicherweise aufgrund eines Entwicklerfehlers oder einer Benutzeraktion nicht zum gewünschten Ordner hinzugefügt (wenn z. B. die benutzerdefinierte Eigenschaft über die Outlook-Feldauswahl entfernt oder das Element in einen anderen Ordner verschoben wird).</span><span class="sxs-lookup"><span data-stu-id="91db4-107">However, the custom property might not get added to the desired folderbecause of developer error or a user action, such as removing the custom property through the Outlook Field Chooser or moving the item to another folder.</span></span> <span data-ttu-id="91db4-108">Aus diesem Grund tritt bei der [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\))-Methode und bei der [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\))-Methode des [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\))-Objekts, das diese benutzerdefinierte Eigenschaft verwendet, ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="91db4-108">Consequently, the [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) method and the [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) object that uses that custom property will fail.</span></span> <span data-ttu-id="91db4-109">Mithilfe des **UserDefinedProperties**-Objekts können Sie testen, ob Ihre benutzerdefinierten Eigenschaften in dem Ordner vorhanden sind und die benutzerdefinierten Eigenschaften hinzufügen, wenn sie nicht vorhanden sind oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="91db4-109">By using the **UserDefinedProperties** object, you can test whether your custom properties exist in the folder, and add the custom properties if they do not exist or if they have been removed.</span></span>

<span data-ttu-id="91db4-p102">Zum Beibehalten einer durch ein **UserDefinedProperty**-Objekt dargestellten benutzerdefinierten Eigenschaft in einem Ordner müssen Sie die benutzerdefinierte Eigenschaft unter dem gleichen Namen im betreffenden Element speichern. Es hat keinerlei Wirkung, wenn Sie einen Wert im **UserDefinedProperty**-Objekt für den Ordner speichern. Sie müssen die **UserProperties**-Auflistung des Elements so definieren, dass sie auf das festzulegende [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) -Objekt zugreift, und dann den Wert für das **UserProperty**-Objekt festlegen. Achten Sie darauf, dass Sie die **Save**-Methode für das Element aufrufen, damit die Änderungen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="91db4-p102">To persist a custom property represented by a **UserDefinedProperty** object in a folder, you must save the custom property with the same name in the item. Storing a value in the **UserDefinedProperty** object for the folder has no effect. You must se the item's **UserProperties** collection to access the [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) object that you want to set, and then set the value on the **UserProperty** object. Be sure to call the **Save** method on the item to persist your changes.</span></span>

<span data-ttu-id="91db4-114">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="91db4-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="91db4-115">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="91db4-115">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="91db4-116">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="91db4-116">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoUserDefinedProperty()
    Dim folder As Outlook.Folder = _
        CType(Application.ActiveExplorer().CurrentFolder(), _
        Outlook.Folder)
    Dim post As Outlook.PostItem = CType( _
        folder.Items.Add("IPM.Post"), Outlook.PostItem)
    ' Add UserProperty to PostItem
    post.UserProperties.Add("ColorID", _
        Outlook.OlUserPropertyType.olText, False)
    post.UserProperties("ColorID").Value = "Green"
    post.Subject = "UserProperty Example"
    post.Save()
    Dim findPost As Outlook.PostItem
    Try
        ' Items.Find will fail unless custom property
        ' is defined in the folder
        findPost = _
            CType(folder.Items.Find("[ColorID] = 'Green'"), _
            Outlook.PostItem)
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
        ' Add ColorID field to the folder
        folder.UserDefinedProperties.Add("ColorID", _
            Outlook.OlUserPropertyType.olText)
        ' Now the find works ok
        Dim findPostOK As Outlook.PostItem
        Try
            findPostOK = _
                CType(folder.Items.Find("[ColorID] = 'Green'"), _
                Outlook.PostItem)
            If Not (findPostOK Is Nothing) Then
                Debug.WriteLine("Found PostItem")
            End If
            ' Cleanup by deleting PostItem and ColorID
            findPostOK.Delete()
            Dim userProperty As Outlook.UserDefinedProperty = _
                folder.UserDefinedProperties("ColorID")
            userProperty.Delete()
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
End Sub
```


```csharp
private void DemoUserDefinedProperty()
{
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.PostItem post = folder.Items.Add("IPM.Post")
        as Outlook.PostItem;
    // Add UserProperty to PostItem
    post.UserProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        false, Type.Missing);
    post.UserProperties["ColorID"].Value = "Green";
    post.Subject = "UserProperty Example";
    post.Save();
    Outlook.PostItem findPost;
    try
    {
        // Items.Find will fail unless custom property
        // is defined in the folder
        findPost =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
     // Add ColorID field to the folder
    folder.UserDefinedProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        Type.Missing, Type.Missing);
    // Now the find works ok
    Outlook.PostItem findPostOK;
    try
    {
        findPostOK =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
        if (findPostOK != null)
        {
            Debug.WriteLine("Found PostItem");
        }
        // Cleanup by deleting PostItem and ColorID
        findPostOK.Delete();
        Outlook.UserDefinedProperty userProperty =
            folder.UserDefinedProperties["ColorID"];
        userProperty.Delete();
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="91db4-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91db4-117">See also</span></span>

- [<span data-ttu-id="91db4-118">Folders</span><span class="sxs-lookup"><span data-stu-id="91db4-118">Folders</span></span>](folders.md)

