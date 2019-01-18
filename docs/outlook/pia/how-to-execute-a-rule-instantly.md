---
title: Sofortiges Ausführen einer Regel
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6bb6ac5422b9785660cb3ec0020c01244002c6b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708648"
---
# <a name="execute-a-rule-instantly"></a>Sofortiges Ausführen einer Regel

Dieses Beispiel zeigt, wie eine Regel sofort mithilfe der [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\))-Methode des [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\))-Objekts ausgeführt wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Sie können veranlassen, dass eine Regel sofort ausgeführt wird, indem Sie die **Execute**-Methode für das **Rule**-Objekt aufrufen. Die Parameter für die **Execute**-Methode sind optional. Wenn Sie sie nicht angeben, wird die Regel auf alle Nachrichten im Posteingang angewendet, jedoch nicht auf die untergeordneten Ordner des Posteingangs, und für die Parameter werden Standardwerte verwendet. In der folgenden Tabelle werden die Standardwerte für die optionalen Parameter der **Execute**-Methode aufgelistet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parameter</p></th>
<th><p>Standardwert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ShowProgress</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Ordner</p></td>
<td><p>Posteingang</p></td>
</tr>
<tr class="odd">
<td><p>IncludeSubfolders</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>RuleExecuteOption</p></td>
<td><p>OlRuleExecuteOption.olRuleExecuteAllMessages</p></td>
</tr>
</tbody>
</table>


Sie können eine Regelausführung mithilfe des Regel- und Benachrichtigungs-Assistenten abbrechen. Eine andere Möglichkeit besteht darin, den *ShowProgress*-Parameter auf **true** festzulegen und dann das Dialogfeld mit der Fortschrittsanzeige abzubrechen. Nachdem Sie das Fortschrittsdialogfeld abgebrochen haben, gibt **Execute** einen Fehler zurück.

Im nachstehenden Codebeispiel ruft ExecuteManagerRule die Regel ab, die im Verfahren „CreateManagerRule“ aus dem Thema [Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md) erstellt wurde. ExecuteManagerRule prüft dann, ob die Regel kein NULL-Verweis ist. Wenn die Regel kein NULL-Verweis ist, ruft ExecuteManagerRule die **Execute**-Methode in der Regel mit Standardparametern auf, wodurch die Regel sofort ausgeführt wird.

> [!NOTE]
> Wenn eine Regel nur einmal angewendet werden soll, unabhängig davon, ob die [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) -Eigenschaft **true** zurückgibt, verwenden Sie die **Rule.Execute**-Methode. Soll die Regel für die aktuelle Sitzung und darüber hinaus verwendet werden, verwenden Sie sowohl die **Rule.Enabled**-Eigenschaft als auch die [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) -Methode.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ExecuteManagerRule()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            string managerName = currentUser.
                GetExchangeUser().GetExchangeUserManager().Name;
            Outlook.Rule managerRule =
                Application.Session.DefaultStore.GetRules()[managerName];
            if (managerRule != null)
            {
                managerRule.Execute(false, Type.Missing,
                    Type.Missing, Type.Missing);
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Regeln](rules.md)

