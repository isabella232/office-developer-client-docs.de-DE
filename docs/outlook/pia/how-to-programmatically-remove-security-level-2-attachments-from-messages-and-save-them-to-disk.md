---
title: Programmgesteuertes Entfernen von Anlagen der Sicherheitsstufe 2 aus Nachrichten und Speichern der Anlagen auf einem Datenträger
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 135f07f4bd3bdc36cee8547106b955b967150df8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320146"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a>Programmgesteuertes Entfernen von Anlagen der Sicherheitsstufe 2 aus Nachrichten und Speichern der Anlagen auf einem Datenträger

Dieses Beispiel zeigt, wie Anlagen der Sicherheitsstufe 2 aus E-Mail-Nachrichten entfernt und auf einem Datenträger gespeichert werden, von wo sie geöffnet werden können.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

In Outlook werden Benutzer vor Malware in E-Mail-Anlagen mit bestimmten Dateierweiterungen, wie EXE oder BAT, geschützt. Diese Anlagen werden standardmäßig blockiert, und als Anlagen der Ebene 1 identifiziert. Bei Anlagen der Ebene 2 ist die Wahrscheinlichkeit, dass sie schädlichen Code enthalten, geringer, dennoch können Benutzer Anlagen der Ebene 2 nicht direkt aus einer E-Mail-Nachricht heraus öffnen. Eine Anlage der Ebene 2 muss zuerst auf einem Datenträger gespeichert werden.

Mithilfe der [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\))-Methode im [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\))-Objekt können Sie Anlagen auf einem Datenträger speichern. Im folgenden Codebeispiel entfernt RemoveAttachmentsAndSaveToDisk zunächst alle Anlagen der Ebene 2, die eine bestimmte Größe überschreiten, aus E-Mail-Elementen in einem Ordner. Dazu wird die [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\))-Eigenschaft jedes **Attachment**-Objekts in der [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\))-Auflistung aufgezählt, und es werden die entfernt, die [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) entsprechen. Anschließend speichert RemoveAttachmentsAndSaveToDisk die entfernte Anlage mithilfe der **SaveAsFile**-Methode.

> [!NOTE] 
> Auflistungen in Outlook sind linear. Verwenden Sie den [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia)-Operator, um auf **Attachments**[1] bis **Attachments**[n] zu verweisen, wobei n den Wert der [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia)-Eigenschaft darstellt.
> 
> Sie können keine **foreach**-Anweisung verwenden, um Elemente aus einer Auflistung zu entfernen. Verwenden Sie stattdessen einen **Index**-Operator, um das erste Element in der Auflistung abzurufen, und löschen Sie es dann. Anschließend können Sie mit einer **while**-Anweisung bestimmen, wann Sie die entsprechende Anzahl von Elementen aus der Auflistung gelöscht haben. Dadurch wird sichergestellt, dass Sie die richtige Anzahl von Elementen in der Auflistung durchlaufen haben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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
            + "https://schemas.microsoft.com/mapi/proptag/0x001A001E"
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

## <a name="see-also"></a>Siehe auch

- [Anlagen](attachments.md)

