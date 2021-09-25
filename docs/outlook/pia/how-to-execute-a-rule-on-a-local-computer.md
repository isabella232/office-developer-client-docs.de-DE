---
title: Ausführen einer Regel auf einem lokalen Computer
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 169d99249d48890c8e7fb75978ef5540a162e8c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560543"
---
# <a name="execute-a-rule-on-a-local-computer"></a>Ausführen einer Regel auf einem lokalen Computer

Dieses Beispiel zeigt, wie Sie mithilfe der [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\))-Eigenschaft des [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\))-Objekts eine Regel auf einem lokalen Computer ausführen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Wenn Ihr Postfach auf einem Exchange-Server gehostet wird, kann auf dem Exchange-Server oder Outlook-Client eine Regel ausgeführt werden. Bei Ausführung der Regel auf dem Server muss Outlook nicht ausgeführt werden, damit die Regelbedingungen ausgewertet und die Regelaktionen ausgeführt werden. Bei Ausführung der Regel auf dem Client muss Outlook ausgeführt werden, damit die Regel ausgeführt wird. Wenn die [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) -Eigenschaft des [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) -Objekts **true** zurückgibt, wird die Regel auf dem Client ausgeführt.

Für Regelaktionen (z. B. Anzeigen einer Benachrichtigung bei neuen E-Mails) wird die **OnLocalMachine**-Bedingung automatisch aktiviert, und die [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\))-Eigenschaft wird für ein nur clientseitig vorhandenes [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\))-Objekt auf **true** festgelegt. Legen Sie für die Regelaktionen, die in der Regel auf dem Server ausgeführt werden, die **Enabled**-Eigenschaft des nur clientseitig vorhandenen **RuleAction**-Objekt so fest, dass die **OnLocalMachine**-Bedingung aktiviert wird. Dadurch wird erzwungen, dass die Regel lokal auf dem Client ausgeführt wird. 

Wenn die **OnLocalMachine**-Bedingung für eine Regel aktiviert ist, wird auch die [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\))-Bedingung aktiviert, wenn dieselbe Regel auf einem anderen Computer überprüft wird. Eine Regelbedingung des Typs [OlConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) gibt an, dass die Regel nur auf einem bestimmten Computer ausgeführt werden kann, der nicht der aktuelle Computer ist, und dass sie nicht programmgesteuert aktiviert oder deaktiviert werden kann. Wenn eine Regel beispielsweise auf dem aktuellen Computer erstellt wird und die **OnLocalMachine**-Bedingung aktiviert ist, kann die Regel nur auf diesem Computer ausgeführt werden. Wenn die gleiche Regel auf einem anderen Computer ausgeführt wird, zeigt die Regel an, dass die **OlConditionOtherMachine**-Regelbedingung aktiviert ist.

Im folgenden Codebeispiel erstellt DemoOnMachineOnly eine Regel und aktiviert die [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\))-Bedingung und [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\))-Aktion, indem die **Enabled**-Eigenschaften auf **true** festgelegt werden. Die **OnLocalMachine**-Bedingung dann aktiviert, wodurch erzwungen wird, dass eine serverseitige Regel lokal ausgeführt wird, und die Regeln werden gespeichert. Eine **Forward**-Aktion und eine **OnlyToMe**-Bedingung werden standardmäßig auf den Server angewendet. Nachdem die **OnLocalMachine**-Bedingung aktiviert wurde, fungieren diese als clientseitige Regel.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Regeln](rules.md)

