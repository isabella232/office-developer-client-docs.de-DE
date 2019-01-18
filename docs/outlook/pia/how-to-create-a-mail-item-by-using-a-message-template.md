---
title: Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cdd9654187685ceab1062fb4ae1882b2d48c68d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711574"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a><span data-ttu-id="7e1a7-102">Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage</span><span class="sxs-lookup"><span data-stu-id="7e1a7-102">Create a mail item by using a message template</span></span>

<span data-ttu-id="7e1a7-103">In diesem Beispiel wird ein E-Mail-Element mit der [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\))-Methode erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e1a7-103">This example creates a mail item by using the [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="7e1a7-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7e1a7-104">Example</span></span>

<span data-ttu-id="7e1a7-105">In diesem Codebeispiel wird die Vorlagendatei „Ivy.oft“ geöffnet, ein Betreff zugewiesen und die Nachricht dann im Ordner „Entwürfe“ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7e1a7-105">This code sample opens the Ivy.oft template file, assigns a subject, and then saves the message to the Drafts folder.</span></span>

<span data-ttu-id="7e1a7-p101">Die **CreateItemFromTemplate**-Methode ist nützlich, wenn Sie eine auf einem Datenträger gespeicherte Outlook-Vorlagendatei (OFT-Datei) als Nachrichtenvorlage verwenden möchten. Die Vorlagendatei kann vorformatierten Text, Briefpapier oder Bilder enthalten, die Sie in die Nachricht aufnehmen möchten. Enthält die Vorlagendatei jedoch Code hinter dem Formular, wird der Formularcode nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e1a7-p101">The **CreateItemFromTemplate** method is useful if you have an Outlook form template file (.oft) stored on disk that you want to use as a message template. The template file can contain preformatted text, stationery, or images that you want to include in the message. However, if the template file contains code behind the form, the form code will not run.</span></span>

<span data-ttu-id="7e1a7-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="7e1a7-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7e1a7-110">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7e1a7-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7e1a7-111">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7e1a7-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateItemFromTemplate()
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderDrafts), Outlook.Folder)
    Dim mail As Outlook.MailItem = _
        CType(Application.CreateItemFromTemplate( _
        "c:\ivy.oft", folder), Outlook.MailItem)
    mail.Subject = "Congratulations"
    mail.Save()
End Sub
```


```csharp
private void CreateItemFromTemplate()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderDrafts) as Outlook.Folder;
    Outlook.MailItem mail =
        Application.CreateItemFromTemplate(
        @"c:\ivy.oft", folder) as Outlook.MailItem;
    mail.Subject = "Congratulations";
    mail.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="7e1a7-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e1a7-112">See also</span></span>

- [<span data-ttu-id="7e1a7-113">Mail</span><span class="sxs-lookup"><span data-stu-id="7e1a7-113">Mail</span></span>](mail.md)

