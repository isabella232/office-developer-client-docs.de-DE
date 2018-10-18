---
title: Ausführen einer Regel auf einem lokalen Computer
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 76587a72d9c77a5484d9aa9788173f9f40f57614
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405840"
---
# <a name="execute-a-rule-on-a-local-computer"></a><span data-ttu-id="ce288-102">Ausführen einer Regel auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="ce288-102">Execute a rule on a local computer</span></span>

<span data-ttu-id="ce288-103">Dieses Beispiel zeigt, wie Sie mithilfe der [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\))-Eigenschaft des [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\))-Objekts eine Regel auf einem lokalen Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce288-103">This example shows how to execute a rule on a local computer by using the [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="ce288-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ce288-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ce288-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ce288-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="ce288-p101">Wenn Ihr Postfach auf einem Exchange-Server gehostet wird, kann auf dem Exchange-Server oder Outlook-Client eine Regel ausgeführt werden. Bei Ausführung der Regel auf dem Server muss Outlook nicht ausgeführt werden, damit die Regelbedingungen ausgewertet und die Regelaktionen ausgeführt werden. Bei Ausführung der Regel auf dem Client muss Outlook ausgeführt werden, damit die Regel ausgeführt wird. Wenn die [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) -Eigenschaft des [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) -Objekts **true** zurückgibt, wird die Regel auf dem Client ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce288-p101">If your mailbox is hosted on an Exchange server, a rule can be executed on the Exchange server or on the Outlook client. If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed. If the rule is executed on the client, Outlook must be running for the rule to execute. If the [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object returns **true**, the rule is executed on the client.</span></span>

<span data-ttu-id="ce288-110">Für Regelaktionen (z. B. Anzeigen einer Benachrichtigung bei neuen E-Mails) wird die **OnLocalMachine**-Bedingung automatisch aktiviert, und die [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\))-Eigenschaft wird für ein nur clientseitig vorhandenes [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\))-Objekt auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce288-110">For rule actions that execute on the client by default (such as displaying a new mail alert), the **OnLocalMachine** condition will automatically be enabled, and the [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) property is set to **true** for a client-side-only [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) object.</span></span> <span data-ttu-id="ce288-111">Legen Sie für die Regelaktionen, die in der Regel auf dem Server ausgeführt werden, die **Enabled**-Eigenschaft des nur clientseitig vorhandenen **RuleAction**-Objekt so fest, dass die **OnLocalMachine**-Bedingung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ce288-111">For rule actions that generally execute on the server, set the **Enabled** property of the client-side-only **RuleAction** object to enable the **OnLocalMachine** condition.</span></span> <span data-ttu-id="ce288-112">Dadurch wird erzwungen, dass die Regel lokal auf dem Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce288-112">This will force the rule to execute locally on the client.</span></span> 

<span data-ttu-id="ce288-113">Wenn die **OnLocalMachine**-Bedingung für eine Regel aktiviert ist, wird auch die [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\))-Bedingung aktiviert, wenn dieselbe Regel auf einem anderen Computer überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="ce288-113">When the **OnLocalMachine** condition for a rule is enabled, the [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) condition will also be enabled when the same rule is examined from another machine.</span></span> <span data-ttu-id="ce288-114">Eine Regelbedingung des Typs [OlConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) gibt an, dass die Regel nur auf einem bestimmten Computer ausgeführt werden kann, der nicht der aktuelle Computer ist, und dass sie nicht programmgesteuert aktiviert oder deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce288-114">A rule condition of type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indicates that the rule can execute only on a specific computer other than the current one, and cannot be programmatically enabled or disabled.</span></span> <span data-ttu-id="ce288-115">Wenn eine Regel beispielsweise auf dem aktuellen Computer erstellt wird und die **OnLocalMachine**-Bedingung aktiviert ist, kann die Regel nur auf diesem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ce288-115">For example, if a rule is created on the current computer and the **OnLocalMachine** rule condition is enabled, the rule can execute only on that computer.</span></span> <span data-ttu-id="ce288-116">Wenn die gleiche Regel auf einem anderen Computer ausgeführt wird, zeigt die Regel an, dass die **OlConditionOtherMachine**-Regelbedingung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ce288-116">When you run the same rule on another computer, the rule will show that the condition **olConditionOtherMachine** is enabled.</span></span>

<span data-ttu-id="ce288-117">Im folgenden Codebeispiel erstellt DemoOnMachineOnly eine Regel und aktiviert die [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\))-Bedingung und [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\))-Aktion, indem die **Enabled**-Eigenschaften auf **true** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ce288-117">In the following code example,   creates a rule and enables the OnlyToMe condition and Forward action by setting the Enabled properties to true.</span></span> <span data-ttu-id="ce288-118">Die **OnLocalMachine**-Bedingung dann aktiviert, wodurch erzwungen wird, dass eine serverseitige Regel lokal ausgeführt wird, und die Regeln werden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ce288-118">The **OnLocalMachine** condition is then enabled, forcing a server-side rule to execute locally, and the rules are saved.</span></span> <span data-ttu-id="ce288-119">Eine **Forward**-Aktion und eine **OnlyToMe**-Bedingung werden standardmäßig auf den Server angewendet.</span><span class="sxs-lookup"><span data-stu-id="ce288-119">By default, a **Forward** action and **OnlyToMe** condition will operate on the server.</span></span> <span data-ttu-id="ce288-120">Nachdem die **OnLocalMachine**-Bedingung aktiviert wurde, fungieren diese als clientseitige Regel.</span><span class="sxs-lookup"><span data-stu-id="ce288-120">Once the **OnLocalMachine** condition has been enabled, they will operate as a client-side rule.</span></span>

<span data-ttu-id="ce288-121">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="ce288-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="ce288-122">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ce288-122">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="ce288-123">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ce288-123">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoOnMachineOnly()
{
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule rule =
        rules.Create("Demo Machine Only Rule",
        Outlook.OlRuleType.olRuleReceive);
    rule.Conditions.OnlyToMe.Enabled = true;
    rule.Actions.Forward.Enabled = true;
    rule.Actions.Forward.Recipients.Add("someone@example.com");
    rule.Actions.Forward.Recipients.ResolveAll();

    // Force the rule to execute locally
    rule.Conditions.OnLocalMachine.Enabled = true;
    rules.Save(true);
}
```

## <a name="see-also"></a><span data-ttu-id="ce288-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce288-124">See also</span></span>

- [<span data-ttu-id="ce288-125">Regeln</span><span class="sxs-lookup"><span data-stu-id="ce288-125">Rules</span></span>](rules.md)

