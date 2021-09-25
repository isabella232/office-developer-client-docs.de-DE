---
title: Sicherstellen, dass benutzerdefinierte Elementeigenschaften in Abfragen auf Ordnerebene unterstützt werden
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 44164fcdfca049062c52fdae9e7783bc932c8006
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560577"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a>Sicherstellen, dass benutzerdefinierte Elementeigenschaften in Abfragen auf Ordnerebene unterstützt werden

In diesem Beispiel wird gezeigt, wie Sie sicherstellen, dass beim Hinzufügen einer benutzerdefinierten Eigenschaft zu einem Elementtyp die Eigenschaft auch dem Ordner hinzugefügt wird, sodass Sie auf Ordnerebene eine Abfrage nach dieser benutzerdefinierten Eigenschaft ausführen können.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird veranschaulicht, wie Sie mithilfe des [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) -Objekts und des [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) -Objekts sicherstellen können, dass eine Eigenschaft, die Sie einer benutzerdefinierten Eigenschaft hinzufügen, auch gleichzeitig dem Ordner hinzugefügt wird, sodass Sie auf der Ordnerebene eine Abfrage nach dieser benutzerdefinierten Eigenschaft ausführen können.

Wenn Sie die [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\))-Methode in der [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\))-Auflistung verwenden, um eine benutzerdefinierte Eigenschaft zu einem Element hinzuzufügen, können Sie den *AddToFolderFields*-Parameter auf **true** festlegen, damit die Eigenschaft zu dem Ordner hinzugefügt wird. Die benutzerdefinierte Eigenschaft wird jedoch möglicherweise aufgrund eines Entwicklerfehlers oder einer Benutzeraktion nicht zum gewünschten Ordner hinzugefügt (wenn z. B. die benutzerdefinierte Eigenschaft über die Outlook-Feldauswahl entfernt oder das Element in einen anderen Ordner verschoben wird). Aus diesem Grund tritt bei der [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\))-Methode und bei der [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\))-Methode des [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\))-Objekts, das diese benutzerdefinierte Eigenschaft verwendet, ein Fehler auf. Mithilfe des **UserDefinedProperties**-Objekts können Sie testen, ob Ihre benutzerdefinierten Eigenschaften in dem Ordner vorhanden sind und die benutzerdefinierten Eigenschaften hinzufügen, wenn sie nicht vorhanden sind oder entfernt wurden.

Zum Beibehalten einer durch ein **UserDefinedProperty**-Objekt dargestellten benutzerdefinierten Eigenschaft in einem Ordner müssen Sie die benutzerdefinierte Eigenschaft unter dem gleichen Namen im betreffenden Element speichern. Es hat keinerlei Wirkung, wenn Sie einen Wert im **UserDefinedProperty**-Objekt für den Ordner speichern. Sie müssen die **UserProperties**-Auflistung des Elements so definieren, dass sie auf das festzulegende [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) -Objekt zugreift, und dann den Wert für das **UserProperty**-Objekt festlegen. Achten Sie darauf, dass Sie die **Save**-Methode für das Element aufrufen, damit die Änderungen beibehalten werden.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Folders](folders.md)

