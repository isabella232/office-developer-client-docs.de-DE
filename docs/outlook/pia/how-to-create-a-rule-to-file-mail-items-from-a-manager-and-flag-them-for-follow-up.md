---
title: Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2fc6f5fe60b2f643590e8f7545804cf6d8a4c11c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405987"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a>Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung

In diesem Beispiel wird gezeigt, wie eine Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung eingerichtet wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Outlook-Regeln können entweder serverseitig oder clientseitig ausgeführt werden, je nach Typ des Kontos und der Regel. Es gibt viele Möglichkeiten, beim Organisieren von Elementen im Posteingang eigene Organisationsschemas anzuwenden. Beispielsweise können Sie eine Hierarchie von Unterordnern erstellen, in der ungelesene und gelesene Nachrichten nach Thema gruppiert sind. Oder Sie erstellen eine Hierarchie von Unterordnern nach dem Absender der Nachricht. Darüber hinaus können Sie Nachrichten mit Kategorien versehen und dann mithilfe von Suchordnern nach Kategorien zusammenfassen.

Mit dem **Rules**-Objektmodell, das ein [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\))-Objekt umfasst, das eine Regel in Outlook darstellt, können Sie Regeln programmgesteuert so erstellen, dass ein bestimmtes Organisationsschema erzwungen wird, eine bestimmte Regel erstellt wird, die für Ihre Lösung einzigartig ist, oder dass sichergestellt wird, dass bestimmte Regeln für eine Gruppe von Benutzern bereitgestellt wird. Mithilfe des **Rules**-Objektmodells können Sie Regeln programmgesteuert hinzufügen, bearbeiten und löschen. Mithilfe der [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\))-Auflistung und des **Rules**-Objekts können Sie auch auf die für eine Sitzung definierten Regeln zugreifen oder diese hinzufügen und löschen. 

Ein **Rule**-Objekt weist eine [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\))-Eigenschaft auf, die angibt, ob die Regel eine Sende- oder Empfangsregel ist. Wenn eine Regel erstellt wird, wird die **RuleType**-Eigenschaft angegeben ist, und diese kann nicht geändert werden, ohne die Regel mit einer anderen **RuleType**-Eigenschaft zu löschen oder erneut zu erstellen. Das [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\))- und das [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\))-Objekte, deren Auflistungsobjekte und Objekte für abgeleitete Aktionen und Bedingungen werden auch verwendet, um die Bearbeitung von Regelaktionen und Regelbedingungen weiter zu unterstützen.

Das **Rules**-Objektmodell unterstützt zwar nicht alle Regeln, die Sie mithilfe des Assistenten für Regeln und Benachrichtigungen auf der Benutzeroberfläche von Outlook erstellen können, aber die meisten häufig verwendeten Aktionen und Bedingungen für Regeln. Alle mit dem Assistenten für Regeln und Benachrichtigungen erstellten Regeln, die auf Nachrichten angewendet werden - hierzu gehören E-Mail-Elemente, Besprechungsanfragen, Aufgabenanfragen, Dokumente, Übermittlungsbestätigungen, Lesebestätigungen, Abstimmungsresultate und Abwesenheitsmitteilungen -, können auch programmgesteuert erstellt werden.

Eine Regel kann auf dem Exchange-Server oder auf dem Outlook-Client ausgeführt werden, vorausgesetzt, das Postfach des aktuellen Benutzers wird auf einem Exchange-Server gehostet. Die [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\))-Eigenschaft des **Rule**-Objekts gibt **true** zurück, um anzugeben, dass die Regel auf einem Client ausgeführt wird; Outlook muss ausgeführt werden, damit die Regel ausgeführt wird. Bei Ausführung der Regel auf dem Server muss Outlook nicht ausgeführt werden, damit die Regelbedingungen ausgewertet und die Regelaktionen ausgeführt werden.

> [!NOTE]
> Es gibt keine separate Auflistung, die die Bedingungen für die Regelausnahme darstellt. Verwenden Sie die [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) -Eigenschaft des **Rule**-Objekts, um eine [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) -Auflistung abzurufen, die die Bedingungen für die Regelausnahme darstellt.

Führen Sie die folgenden Schritte aus, um Regeln mithilfe des Outlook-Objektmodells zu erstellen:

1.  Rufen Sie die **Rules**-Auflistung aus der [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) -Eigenschaft des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts ab, indem Sie die [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) -Methode für das Standard- [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) -Objekt aufrufen. Verwenden Sie einen **try…catch**-Block, um die Möglichkeit einzubeziehen, dass der Benutzer offline oder vom Exchange-Server getrennt ist. Dadurch verhindern Sie, dass in Outlook ein Fehler ausgelöst wird.

2.  Rufen Sie die [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\))-Methode für das **Rules**-Objekt auf, um eine Instanzvariable oder ein **Rule**-Objekt zu erstellen, wobei Sie einen Namen und einen [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\))-Parameter angeben.

3.  Aktivieren Sie mithilfe der [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) - und der [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) -Auflistung Aktionen, Bedingungen und Ausnahmen für das **Rule**-Objekt. Beachten Sie, dass jede in der **RuleConditions**-Auflistung aktivierte Bedingung, die von der [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) -Eigenschaft zurückgegeben wird, als Bedingung für eine Regelausnahme behandelt wird und Sie der Auflistung keine zusätzlichen integrierten benutzerdefinierten Aktionen oder Bedingungen hinzufügen können.

4.  Legen Sie die [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) -Eigenschaft auf **true** fest, damit jede gegebene Regelaktion, -bedingung oder -ausnahme funktionsfähig ist. Für manche Aktionen oder Bedingungen, z. B. die [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) -Eigenschaft, müssen Sie zusätzliche Eigenschaften festlegen, damit das **Rule**-Objekt fehlerfrei gespeichert wird.

5.  Rufen Sie zum Schluss die [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) -Methode für die **Rules**-Auflistung auf, um die erstellten oder geänderten Regeln zu speichern. Schließen Sie die **Save**-Methode in einen **try…catch**-Block ein, um die Ausnahmebehandlung zu implementieren.

Im folgenden Codebeispiel implementiert CreateManagerRule die oben beschriebenen Schritte. CreateManagerRule überprüft zuerst, ob die [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\))-Eigenschaft ein [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt darstellt, was bedeutet, dass der aktuelle Benutzer ein Exchange-Benutzer ist. Ist dies der Fall, ruft CreateManagerRule durch Aufrufen der [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\))-Methode für das **ExchangeUser**-Objekt der **CurrentUser**-Eigenschaft des **NameSpace**-Objekts den Vorgesetzten des aktuellen Benutzers ab. Danach wird eine Empfangsregel erstellt, um empfangene Nachrichten in einen Unterordner des Postfachs zu verschieben, wenn die folgenden Bedingungen erfüllt sind: 

- Die Nachricht stammt von dem Vorgesetzten des Benutzers.

- Der Empfänger befindet sich in der **An**-Zeile der Nachricht.

- Die Nachricht ist keine Besprechungsanfrage und kein Update.

Zum Schluss wird die Nachricht für die Nachverfolgung am selben Tag gekennzeichnet. CreateManagerRule veranschaulicht auch die ordnungsgemäße Fehlerbehandlung für Bedingungen, die eine Ausnahme auslösen könnten, z. B. wenn der Benutzer offline ist oder die Verbindung im zwischengespeicherten Exchange-Modus getrennt ist. 

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateManagerRule()
{
    Outlook.ExchangeUser manager;
    Outlook.Folder managerFolder;
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        Outlook.Rules rules;
        try
        {
            rules = Application.Session.DefaultStore.GetRules();
        }
        catch
        {
            Debug.WriteLine("Could not obtain rules collection.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            Outlook.Folders folders =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).Folders;
            try
            {
                managerFolder =
                    folders[displayName] as Outlook.Folder;
            }
            catch
            {
                managerFolder =
                    folders.Add(displayName, Type.Missing)
                    as Outlook.Folder;
            }
            Outlook.Rule rule = rules.Create(displayName,
                Outlook.OlRuleType.olRuleReceive);

            // Rule conditions
            // From condition
            rule.Conditions.From.Recipients.Add(
                manager.PrimarySmtpAddress);
            rule.Conditions.From.Recipients.ResolveAll();
            rule.Conditions.From.Enabled = true;

            // Sent only to me
            rule.Conditions.ToMe.Enabled = true;

            // Rule exceptions
            // Meeting invite or update
            rule.Exceptions.MeetingInviteOrUpdate.Enabled = true;

            // Rule actions
            // MarkAsTask action
            rule.Actions.MarkAsTask.MarkInterval =
                Outlook.OlMarkInterval.olMarkToday;
            rule.Actions.MarkAsTask.FlagTo = "Follow-up";
            rule.Actions.MarkAsTask.Enabled = true;

            // MoveToFolder action
            rule.Actions.MoveToFolder.Folder = managerFolder;
            rule.Actions.MoveToFolder.Enabled = true;
            try
            {
                rules.Save(true);
            }
            catch (Exception ex)
            {
                Debug.WriteLine(ex.Message);
            }
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Regeln](rules.md)

