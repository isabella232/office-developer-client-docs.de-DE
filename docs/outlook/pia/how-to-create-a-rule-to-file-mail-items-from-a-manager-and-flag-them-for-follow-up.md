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
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a><span data-ttu-id="d1446-102">Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="d1446-102">Create a rule to file mail items from a manager and flag them for follow-up</span></span>

<span data-ttu-id="d1446-103">In diesem Beispiel wird gezeigt, wie eine Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="d1446-103">This example shows how to set up a rule to file mail items from the user’s manager and flag them for follow up.</span></span>

## <a name="example"></a><span data-ttu-id="d1446-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d1446-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d1446-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d1446-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="d1446-p101">Outlook-Regeln können entweder serverseitig oder clientseitig ausgeführt werden, je nach Typ des Kontos und der Regel. Es gibt viele Möglichkeiten, beim Organisieren von Elementen im Posteingang eigene Organisationsschemas anzuwenden. Beispielsweise können Sie eine Hierarchie von Unterordnern erstellen, in der ungelesene und gelesene Nachrichten nach Thema gruppiert sind. Oder Sie erstellen eine Hierarchie von Unterordnern nach dem Absender der Nachricht. Darüber hinaus können Sie Nachrichten mit Kategorien versehen und dann mithilfe von Suchordnern nach Kategorien zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="d1446-p101">Outlook rules can operate either server-side or client-side, depending on the type of account and rule. There are many ways you can implement rules to enforce your own organizational schemes when you organize items in your mailbox. For example, you can create a subfolder hierarchy that organizes unread mail and read mail by subject area. Or, you can create a subfolder hierarchy that corresponds to the sender of the message. You can also categorize your mail and then use search folders to aggregate the mail by category.</span></span>

<span data-ttu-id="d1446-111">Mit dem **Rules**-Objektmodell, das ein [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\))-Objekt umfasst, das eine Regel in Outlook darstellt, können Sie Regeln programmgesteuert so erstellen, dass ein bestimmtes Organisationsschema erzwungen wird, eine bestimmte Regel erstellt wird, die für Ihre Lösung einzigartig ist, oder dass sichergestellt wird, dass bestimmte Regeln für eine Gruppe von Benutzern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d1446-111">The **Rules** object model, which includes a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object that represents a rule in Outlook, allows you to create rules programmatically to enforce a certain organizational scheme, create a specific rule that is unique to your solution, or ensure that certain rules are deployed to a group of users.</span></span> <span data-ttu-id="d1446-112">Mithilfe des **Rules**-Objektmodells können Sie Regeln programmgesteuert hinzufügen, bearbeiten und löschen.</span><span class="sxs-lookup"><span data-stu-id="d1446-112">By using the **Rules** object model, you can programmatically add, edit, and delete rules.</span></span> <span data-ttu-id="d1446-113">Mithilfe der [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\))-Auflistung und des **Rules**-Objekts können Sie auch auf die für eine Sitzung definierten Regeln zugreifen oder diese hinzufügen und löschen.</span><span class="sxs-lookup"><span data-stu-id="d1446-113">By using the [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) collection and the **Rule** object, you can also access, add, and delete rules defined for a session.</span></span> 

<span data-ttu-id="d1446-114">Ein **Rule**-Objekt weist eine [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\))-Eigenschaft auf, die angibt, ob die Regel eine Sende- oder Empfangsregel ist.</span><span class="sxs-lookup"><span data-stu-id="d1446-114">A **Rule** object has a [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) property that indicates whether the rule is a send or receive rule.</span></span> <span data-ttu-id="d1446-115">Wenn eine Regel erstellt wird, wird die **RuleType**-Eigenschaft angegeben ist, und diese kann nicht geändert werden, ohne die Regel mit einer anderen **RuleType**-Eigenschaft zu löschen oder erneut zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1446-115">When a rule is created, the **RuleType** property is specified, and cannot be changed without deleting and re-creating the rule with a different **RuleType** property.</span></span> <span data-ttu-id="d1446-116">Das [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\))- und das [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\))-Objekte, deren Auflistungsobjekte und Objekte für abgeleitete Aktionen und Bedingungen werden auch verwendet, um die Bearbeitung von Regelaktionen und Regelbedingungen weiter zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d1446-116">The [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) and [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) objects, their collection objects, and derived action and condition objects are also used to further support editing rule actions and rule conditions.</span></span>

<span data-ttu-id="d1446-p104">Das **Rules**-Objektmodell unterstützt zwar nicht alle Regeln, die Sie mithilfe des Assistenten für Regeln und Benachrichtigungen auf der Benutzeroberfläche von Outlook erstellen können, aber die meisten häufig verwendeten Aktionen und Bedingungen für Regeln. Alle mit dem Assistenten für Regeln und Benachrichtigungen erstellten Regeln, die auf Nachrichten angewendet werden - hierzu gehören E-Mail-Elemente, Besprechungsanfragen, Aufgabenanfragen, Dokumente, Übermittlungsbestätigungen, Lesebestätigungen, Abstimmungsresultate und Abwesenheitsmitteilungen -, können auch programmgesteuert erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d1446-p104">The **Rules** object model does not support all rules that you can create by using the Rules and Alert Wizard in the Outlook user interface, but it supports the most commonly used rule actions and conditions. Any rules created by using the Rules and Alerts Wizard that are applied to messages, which include mail items, meeting requests, task requests, documents, delivery receipts, read receipts, voting responses, and out-of-office notices, can also be created programmatically.</span></span>

<span data-ttu-id="d1446-119">Eine Regel kann auf dem Exchange-Server oder auf dem Outlook-Client ausgeführt werden, vorausgesetzt, das Postfach des aktuellen Benutzers wird auf einem Exchange-Server gehostet.</span><span class="sxs-lookup"><span data-stu-id="d1446-119">A rule can execute on the Exchange server or on the Outlook client, provided that the current user’s mailbox is hosted on an Exchange server.</span></span> <span data-ttu-id="d1446-120">Die [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\))-Eigenschaft des **Rule**-Objekts gibt **true** zurück, um anzugeben, dass die Regel auf einem Client ausgeführt wird; Outlook muss ausgeführt werden, damit die Regel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1446-120">The [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the **Rule** object returns **true** to indicate that the rule executes on a client, and Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="d1446-121">Bei Ausführung der Regel auf dem Server muss Outlook nicht ausgeführt werden, damit die Regelbedingungen ausgewertet und die Regelaktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d1446-121">If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span>

> [!NOTE]
> <span data-ttu-id="d1446-p106">Es gibt keine separate Auflistung, die die Bedingungen für die Regelausnahme darstellt. Verwenden Sie die [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) -Eigenschaft des **Rule**-Objekts, um eine [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) -Auflistung abzurufen, die die Bedingungen für die Regelausnahme darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1446-p106">There is no separate collection that represents rule exception conditions. Use the [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) property of the **Rule** object to get a [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) collection that represents rule exception conditions.</span></span>

<span data-ttu-id="d1446-124">Führen Sie die folgenden Schritte aus, um Regeln mithilfe des Outlook-Objektmodells zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d1446-124">To create rules through the Outlook object model, follow these steps:</span></span>

1.  <span data-ttu-id="d1446-p107">Rufen Sie die **Rules**-Auflistung aus der [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) -Eigenschaft des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts ab, indem Sie die [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) -Methode für das Standard- [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) -Objekt aufrufen. Verwenden Sie einen **try…catch**-Block, um die Möglichkeit einzubeziehen, dass der Benutzer offline oder vom Exchange-Server getrennt ist. Dadurch verhindern Sie, dass in Outlook ein Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="d1446-p107">Get the **Rules** collection from the [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object by calling the [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) method on the default [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object. Use a **try…catch** block to account for the user being offline or disconnected from the Exchange server. This prevents Outlook from raising an error.</span></span>

2.  <span data-ttu-id="d1446-128">Rufen Sie die [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\))-Methode für das **Rules**-Objekt auf, um eine Instanzvariable oder ein **Rule**-Objekt zu erstellen, wobei Sie einen Namen und einen [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\))-Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d1446-128">Call the [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) method on the **Rules** object to create an instance variable or a **Rule** object, specifying a  Name and a [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) parameter.</span></span>

3.  <span data-ttu-id="d1446-p108">Aktivieren Sie mithilfe der [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) - und der [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) -Auflistung Aktionen, Bedingungen und Ausnahmen für das **Rule**-Objekt. Beachten Sie, dass jede in der **RuleConditions**-Auflistung aktivierte Bedingung, die von der [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) -Eigenschaft zurückgegeben wird, als Bedingung für eine Regelausnahme behandelt wird und Sie der Auflistung keine zusätzlichen integrierten benutzerdefinierten Aktionen oder Bedingungen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="d1446-p108">Use the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) and [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collections to enable actions, conditions, and exceptions on the **Rule** object. Note that any condition enabled in the **RuleConditions** collection, returned by the [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) property, is treated as a rule exception condition, and additional built-in custom actions or conditions cannot be added to the collection.</span></span>

4.  <span data-ttu-id="d1446-p109">Legen Sie die [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) -Eigenschaft auf **true** fest, damit jede gegebene Regelaktion, -bedingung oder -ausnahme funktionsfähig ist. Für manche Aktionen oder Bedingungen, z. B. die [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) -Eigenschaft, müssen Sie zusätzliche Eigenschaften festlegen, damit das **Rule**-Objekt fehlerfrei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d1446-p109">Set the [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) property to **true** for any given rule action, condition, or exception to be operational. Some actions or conditions, such as the [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) property, require that you set additional properties on the action or condition to save the **Rule** object without an error.</span></span>

5.  <span data-ttu-id="d1446-p110">Rufen Sie zum Schluss die [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) -Methode für die **Rules**-Auflistung auf, um die erstellten oder geänderten Regeln zu speichern. Schließen Sie die **Save**-Methode in einen **try…catch**-Block ein, um die Ausnahmebehandlung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d1446-p110">Finally, call the [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) method on the **Rules** collection to save the created or modified rules. Enclose the **Save** method in a **try…catch** block to handle exceptions.</span></span>

<span data-ttu-id="d1446-135">Im folgenden Codebeispiel implementiert CreateManagerRule die oben beschriebenen Schritte.</span><span class="sxs-lookup"><span data-stu-id="d1446-135">In the following code example,   implements the steps previously described.</span></span> <span data-ttu-id="d1446-136">CreateManagerRule überprüft zuerst, ob die [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\))-Eigenschaft ein [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt darstellt, was bedeutet, dass der aktuelle Benutzer ein Exchange-Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="d1446-136"> first verifies whether the CurrentUser property represents an ExchangeUser object, indicating that the current user is an Exchange user.</span></span> <span data-ttu-id="d1446-137">Ist dies der Fall, ruft CreateManagerRule durch Aufrufen der [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\))-Methode für das **ExchangeUser**-Objekt der **CurrentUser**-Eigenschaft des **NameSpace**-Objekts den Vorgesetzten des aktuellen Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="d1446-137">If the current user is an Exchange user,   gets the current user's manager by calling the GetExchangeUserManager() method on the ExchangeUser object of the CurrentUser property of the NameSpace object.</span></span> <span data-ttu-id="d1446-138">Danach wird eine Empfangsregel erstellt, um empfangene Nachrichten in einen Unterordner des Postfachs zu verschieben, wenn die folgenden Bedingungen erfüllt sind: </span><span class="sxs-lookup"><span data-stu-id="d1446-138">A receive rule is then created to move received messages to a subfolder of the Inbox for the following conditions:</span></span>

- <span data-ttu-id="d1446-139">Die Nachricht stammt von dem Vorgesetzten des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d1446-139">The message is from the user’s manager.</span></span>

- <span data-ttu-id="d1446-140">Der Empfänger befindet sich in der **An**-Zeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d1446-140">The recipient is on the **To:** line of the message.</span></span>

- <span data-ttu-id="d1446-141">Die Nachricht ist keine Besprechungsanfrage und kein Update.</span><span class="sxs-lookup"><span data-stu-id="d1446-141">The message is not a meeting request or update.</span></span>

<span data-ttu-id="d1446-p112">Zum Schluss wird die Nachricht für die Nachverfolgung am selben Tag gekennzeichnet. CreateManagerRule veranschaulicht auch die ordnungsgemäße Fehlerbehandlung für Bedingungen, die eine Ausnahme auslösen könnten, z. B. wenn der Benutzer offline ist oder die Verbindung im zwischengespeicherten Exchange-Modus getrennt ist. </span><span class="sxs-lookup"><span data-stu-id="d1446-p112">Finally, the message is flagged for follow-up today. CreateManagerRule also illustrates appropriate error handling for conditions that could raise an exception such as the user being offline or disconnected in cached Exchange mode.</span></span>

<span data-ttu-id="d1446-144">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="d1446-144">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="d1446-145">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d1446-145">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="d1446-146">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="d1446-146">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d1446-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1446-147">See also</span></span>

- [<span data-ttu-id="d1446-148">Regeln</span><span class="sxs-lookup"><span data-stu-id="d1446-148">Rules</span></span>](rules.md)

