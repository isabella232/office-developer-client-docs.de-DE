---
title: Synchronisieren von Outlook mit einem SharePoint-Ordner
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 000743f394db3eeaf6d6b9d1d3eb98506d0d348b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583086"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a>Synchronisieren von Outlook mit einem SharePoint-Ordner

In diesem Beispiel wird veranschaulicht, wie programmgesteuert eine Verbindung zwischen Outlook und einem SharePoint-Ordner hergestellt und die Ordnerinhalte synchronisiert werden können.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

In Outlook können Sie Kalender, Kontaktlisten, Aufgabenlisten, Diskussionsrunden und Dokumentbibliotheken mit SharePoint-Ordnern synchronisieren. Based on the URL provided upon synchronization, Outlook will create a new folder of the same base type as the SharePoint folder. Beim Synchronisieren mit einem SharePoint-Kalenderordner zum Beispiel wird eine neuer Kalenderordner in Outlook erstellt. SharePoint-Synchronisierungsordner werden in eigenen persönlichen Outlook-Ordnern (PST-Datei) außerhalb des Benutzerpostfachs gespeichert. Sie können eine Verbindung mit einem SharePoint-Ordner mit der [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts herstellen. Note that you must use a stssync:// URL that provides details about the SharePoint server, folder path, and other information that Outlook needs to open a SharePoint folder.

When connecting to a SharePoint folder programmatically, you must determine the proper URL to use to create the sharing relationship. Da die stssync://-URL für den Ordner nicht auf der SharePoint-Benutzeroberfläche bereitgestellt wird, müssen Sie den Zielordner in Outlook manuell verknüpfen. Verwenden Sie dann das erste Verfahren, DisplaySharePointUrl, im folgenden Codebeispiel, um die richtige URL abzurufen. DisplaySharePointUrl verwendet das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt, um nach Freigabebindungsinformationen im aktuellen Ordner für das aktive Explorer-Fenster zu suchen. Wenn eine oder mehrere Bindungskontexte gefunden werden, werden die URLs für alle verfügbaren Freigabekontexte angezeigt.

Jetzt haben Sie die richtige URL zum Erstellen der Freigabebeziehung. Um den neuen SharePoint-Ordner in Outlook zu synchronisieren, kopieren Sie die URL und fügen Sie sie in die Zuweisung der Zeichenfolgenvariable „CalendarUrl“ in dem zweiten Verfahren „AddSpsFolder“. AddSpsFolder automatisiert die Synchronisierung des neuen SharePoint-Ordners in Outlook, indem die **NameSpace.OpenSharedFolder**-Methode mit einer `stssync://`-URL (in diesem Fall die URL, die im DisplaySharePointUrl-Verfahren generiert wurde) verwendet wird. AddSpsFolder bietet auch einen benutzerdefinierten Ordnernamen „Example SPS Calendar“ und weist Outlook an, die standardmäßige Gültigkeitsdauer (Time to Live, TTL) für den Ordner zu verwenden. SharePoint-Ordner laden immer Elementanlagen herunter, daher müssen Sie dies hier nicht angeben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySharePointUrl()
{
    const string PROP_SYNC_URL = 
        "http://schemas.microsoft.com/mapi/id/{00062040-0000-0000-C000-000000000046}/8A24001E";

    Outlook.Folder folder = Application.ActiveExplorer().CurrentFolder as Outlook.Folder;
    Outlook.Table table = folder.GetTable(Type.Missing, Outlook.OlTableContents.olHiddenItems);
    table.Columns.RemoveAll();
    table.Columns.Add("MessageClass");
    table.Columns.Add(PROP_SYNC_URL);

    StringBuilder sb = new StringBuilder();
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        string msgClass, spsUrl;
        msgClass = row["MessageClass"] as string;
        spsUrl = row[PROP_SYNC_URL] as string;

        if (msgClass == "IPM.Sharing.Binding.In")
        {
            sb.Append(spsUrl);
            sb.Append("\r\n");
        }
    }
    if (sb.Length > 0)
    {
        System.Windows.Forms.MessageBox.Show(
            "The following SharePoint Folder URLs were found:\r\n" + sb.ToString());
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("No SharePoint URLs were found in this folder.");
    }
}

private void AddSpsFolder()
{
    string calendarUrl = "stssync://sts/?ver=1.1&type=calendar&cmd=add-folder&base-url=
        https://example.org/calendar&list-url=/Lists/Calendar/calendar.aspx&guid=&site-name=
        Example%20Site&list-name=Calendar";
    string folderName = "Example SPS Calendar";
    bool useDefaultTTL = true;
    Outlook.Folder calendarFolder =
        Application.Session.OpenSharedFolder(calendarUrl, folderName, Type.Missing, useDefaultTTL) 
        as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(calendarFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a>Siehe auch

- [Gruppenfreigabe](group-sharing.md)

