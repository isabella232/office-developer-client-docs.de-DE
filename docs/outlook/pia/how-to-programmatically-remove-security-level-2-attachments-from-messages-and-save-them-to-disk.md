---
title: Programmgesteuertes Entfernen von Anlagen der Sicherheitsstufe 2 aus Nachrichten und Speichern der Anlagen auf einem Datenträger
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 588d1db8ad222462b2648d4fdb85207fd9bdb782
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539262"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a><span data-ttu-id="1e975-102">Programmgesteuertes Entfernen von Anlagen der Sicherheitsstufe 2 aus Nachrichten und Speichern der Anlagen auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="1e975-102">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>

<span data-ttu-id="1e975-103">Dieses Beispiel zeigt, wie Anlagen der Sicherheitsstufe 2 aus E-Mail-Nachrichten entfernt und auf einem Datenträger gespeichert werden, von wo sie geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="1e975-103">This example shows how to remove security level 2 attachments from email messages and save them to a disk, from where they can be opened.</span></span>

## <a name="example"></a><span data-ttu-id="1e975-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1e975-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1e975-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="1e975-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="1e975-106">In Outlook werden Benutzer vor Malware in E-Mail-Anlagen mit bestimmten Dateierweiterungen, wie EXE oder BAT, geschützt.</span><span class="sxs-lookup"><span data-stu-id="1e975-106">Outlook protects users from malicious code transported via email attachments that have certain file extensions such as .exe or .bat.</span></span> <span data-ttu-id="1e975-107">Diese Anlagen werden standardmäßig blockiert, und als Anlagen der Ebene 1 identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1e975-107">Those particular attachments are blocked by default and identified as Level 1 attachments.</span></span> <span data-ttu-id="1e975-108">Bei Anlagen der Ebene 2 ist die Wahrscheinlichkeit, dass sie schädlichen Code enthalten, geringer, dennoch können Benutzer Anlagen der Ebene 2 nicht direkt aus einer E-Mail-Nachricht heraus öffnen.</span><span class="sxs-lookup"><span data-stu-id="1e975-108">Level 2 attachments have a lesser chance of containing malicious code, but users cannot open a Level 2 attachment directly from an email message.</span></span> <span data-ttu-id="1e975-109">Eine Anlage der Ebene 2 muss zuerst auf einem Datenträger gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1e975-109">A Level 2 attachment must first be saved to a disk.</span></span>

<span data-ttu-id="1e975-110">Mithilfe der [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\))-Methode im [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\))-Objekt können Sie Anlagen auf einem Datenträger speichern.</span><span class="sxs-lookup"><span data-stu-id="1e975-110">By using the [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) method in the [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) object, you can save attachments to a disk.</span></span> <span data-ttu-id="1e975-111">Im folgenden Codebeispiel entfernt RemoveAttachmentsAndSaveToDisk zunächst alle Anlagen der Ebene 2, die eine bestimmte Größe überschreiten, aus E-Mail-Elementen in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="1e975-111">In the following code example, RemoveAttachmentsAndSaveToDisk first removes from mail items in a folder all Level 2 attachments that are greater than a specified size.</span></span> <span data-ttu-id="1e975-112">Dazu wird die [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\))-Eigenschaft jedes **Attachment**-Objekts in der [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\))-Auflistung aufgezählt, und es werden die entfernt, die [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1e975-112">This is done by enumerating the [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) property of each **Attachment** object in the [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) collection and removing the ones that are equal to [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)).</span></span> <span data-ttu-id="1e975-113">Anschließend speichert RemoveAttachmentsAndSaveToDisk die entfernte Anlage mithilfe der **SaveAsFile**-Methode.</span><span class="sxs-lookup"><span data-stu-id="1e975-113">RemoveAttachmentsAndSaveToDisk then saves the removed attachment by using the **SaveAsFile** method.</span></span>

> [!NOTE] 
> <span data-ttu-id="1e975-114">Auflistungen in Outlook sind linear.</span><span class="sxs-lookup"><span data-stu-id="1e975-114">Collections in Outlook are linear.</span></span> <span data-ttu-id="1e975-115">Verwenden Sie den [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia)-Operator, um auf **Attachments**[1] bis **Attachments**[n] zu verweisen, wobei n den Wert der [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia)-Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e975-115">Use the [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) operator to reference **Attachments**[1] to **Attachments**[n], where n represents the value of the [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia) property.</span></span>
> 
> <span data-ttu-id="1e975-p104">Sie können keine **foreach**-Anweisung verwenden, um Elemente aus einer Auflistung zu entfernen. Verwenden Sie stattdessen einen **Index**-Operator, um das erste Element in der Auflistung abzurufen, und löschen Sie es dann. Anschließend können Sie mit einer **while**-Anweisung bestimmen, wann Sie die entsprechende Anzahl von Elementen aus der Auflistung gelöscht haben. Dadurch wird sichergestellt, dass Sie die richtige Anzahl von Elementen in der Auflistung durchlaufen haben.</span><span class="sxs-lookup"><span data-stu-id="1e975-p104">You cannot use a **foreach** statement to remove items in a collection. Instead, use an **Index** operator to obtain the first item in the collection, and then delete the item. Then use a **while** statement to determine when you have deleted the appropriate number of items in the collection. This will ensure that you have iterated over the correct number of items in the collection.</span></span>

<span data-ttu-id="1e975-120">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="1e975-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1e975-121">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1e975-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1e975-122">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1e975-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RemoveAttachmentsAndSaveToDisk(string path,
    Outlook.Folder folder, int size)
{
    Outlook.Items attachItems;
    Outlook.Attachment attachment;
    Outlook.Attachments attachments;
    int byValueCount;
    int removeCount;
    bool saveMessage;
    try
    {
        // The restriction will find all items that
        // have attachments and MessageClass = IPM.Note.
        string filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:hasattachment"
            + "\"" + " = True" + " AND " + "\""
            + "http://schemas.microsoft.com/mapi/proptag/0x001A001E"
            + "\"" + " = 'IPM.Note'";
        attachItems = folder.Items.Restrict(filter);
        foreach (Outlook.MailItem mail in attachItems)
        {
            saveMessage = false;
            byValueCount = 0;
            attachments = mail.Attachments;
            // Obtain the count of ByValue attachments.
            foreach (Outlook.Attachment attach in attachments)
            {
                if (attach.Size > size
                    & attach.Type ==
                    Outlook.OlAttachmentType.olByValue)
                {
                    byValueCount = byValueCount + 1;
                }
            }
            if (byValueCount > 0)
            {
                // removeCount is number of attachments to remove.
                removeCount = attachments.Count - byValueCount;
                while (mail.Attachments.Count != removeCount)
                {
                    // Use indexer to obtain 
                    // first attachment in collection.
                    attachment = mail.Attachments[1];
                    // You can refine this code to save 
                    // separate copies of attachments 
                    // with the same name.
                    attachment.SaveAsFile(path + @"\"
                        + attachment.FileName);
                    attachment.Delete();
                    if (saveMessage != true)
                    {
                        saveMessage = true;
                    }
                }
                if (saveMessage)
                {
                    mail.Save();
                }
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1e975-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e975-123">See also</span></span>

- [<span data-ttu-id="1e975-124">Anlagen</span><span class="sxs-lookup"><span data-stu-id="1e975-124">Attachments</span></span>](attachments.md)

