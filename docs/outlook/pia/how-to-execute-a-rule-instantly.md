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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320370"
---
# <a name="execute-a-rule-instantly"></a><span data-ttu-id="fdd00-102">Sofortiges Ausführen einer Regel</span><span class="sxs-lookup"><span data-stu-id="fdd00-102">Execute a rule instantly</span></span>

<span data-ttu-id="fdd00-103">Dieses Beispiel zeigt, wie eine Regel sofort mithilfe der [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\))-Methode des [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\))-Objekts ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd00-103">This example shows how to execute a rule instantly by using the [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) method of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="fdd00-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fdd00-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fdd00-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fdd00-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fdd00-p101">Sie können veranlassen, dass eine Regel sofort ausgeführt wird, indem Sie die **Execute**-Methode für das **Rule**-Objekt aufrufen. Die Parameter für die **Execute**-Methode sind optional. Wenn Sie sie nicht angeben, wird die Regel auf alle Nachrichten im Posteingang angewendet, jedoch nicht auf die untergeordneten Ordner des Posteingangs, und für die Parameter werden Standardwerte verwendet. In der folgenden Tabelle werden die Standardwerte für die optionalen Parameter der **Execute**-Methode aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fdd00-p101">You can cause a rule to execute immediately by calling the **Execute** method on the **Rule** object. The parameters to the **Execute** method are optional; if they are not specified, the rule will be applied to all messages in the Inbox but not to the subfolders of the Inbox, and default values for the parameters will be used. The following table lists the default values for the optional parameters of the **Execute** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fdd00-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdd00-109">Parameter</span></span></p></th>
<th><p><span data-ttu-id="fdd00-110">Standardwert</span><span class="sxs-lookup"><span data-stu-id="fdd00-110">Default value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fdd00-111">ShowProgress</span><span class="sxs-lookup"><span data-stu-id="fdd00-111">ShowProgress</span></span></p></td>
<td><p><span data-ttu-id="fdd00-112">False</span><span class="sxs-lookup"><span data-stu-id="fdd00-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdd00-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="fdd00-113">Folder</span></span></p></td>
<td><p><span data-ttu-id="fdd00-114">Posteingang</span><span class="sxs-lookup"><span data-stu-id="fdd00-114">Inbox</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fdd00-115">IncludeSubfolders</span><span class="sxs-lookup"><span data-stu-id="fdd00-115">IncludeSubfolders</span></span></p></td>
<td><p><span data-ttu-id="fdd00-116">False</span><span class="sxs-lookup"><span data-stu-id="fdd00-116">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fdd00-117">RuleExecuteOption</span><span class="sxs-lookup"><span data-stu-id="fdd00-117">RuleExecuteOption</span></span></p></td>
<td><p><span data-ttu-id="fdd00-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span><span class="sxs-lookup"><span data-stu-id="fdd00-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fdd00-119">Sie können eine Regelausführung mithilfe des Regel- und Benachrichtigungs-Assistenten abbrechen.</span><span class="sxs-lookup"><span data-stu-id="fdd00-119">You can cancel a rule execution by using the Rules and Alerts Wizard.</span></span> <span data-ttu-id="fdd00-120">Eine andere Möglichkeit besteht darin, den *ShowProgress*-Parameter auf **true** festzulegen und dann das Dialogfeld mit der Fortschrittsanzeige abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="fdd00-120">You can also cancel a rule execution by setting the *ShowProgress* parameter to **true** and then canceling the progress dialog box.</span></span> <span data-ttu-id="fdd00-121">Nachdem Sie das Fortschrittsdialogfeld abgebrochen haben, gibt **Execute** einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd00-121">Once you cancel the progress dialog box, **Execute** will return an error.</span></span>

<span data-ttu-id="fdd00-122">Im nachstehenden Codebeispiel ruft ExecuteManagerRule die Regel ab, die im Verfahren „CreateManagerRule“ aus dem Thema [Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fdd00-122">In the following code example, ExecuteManagerRule gets the rule that was created in the procedure CreateManagerRule from the topic [Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span> <span data-ttu-id="fdd00-123">ExecuteManagerRule prüft dann, ob die Regel kein NULL-Verweis ist.</span><span class="sxs-lookup"><span data-stu-id="fdd00-123">ExecuteManagerRule then checks whether the rule is not a null reference.</span></span> <span data-ttu-id="fdd00-124">Wenn die Regel kein NULL-Verweis ist, ruft ExecuteManagerRule die **Execute**-Methode in der Regel mit Standardparametern auf, wodurch die Regel sofort ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd00-124">If the rule is not a null reference, ExecuteManagerRule calls the **Execute** method on the rule with default parameters, instantly executing the rule.</span></span>

> [!NOTE]
> <span data-ttu-id="fdd00-p104">Wenn eine Regel nur einmal angewendet werden soll, unabhängig davon, ob die [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) -Eigenschaft **true** zurückgibt, verwenden Sie die **Rule.Execute**-Methode. Soll die Regel für die aktuelle Sitzung und darüber hinaus verwendet werden, verwenden Sie sowohl die **Rule.Enabled**-Eigenschaft als auch die [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="fdd00-p104">To apply a rule once, regardless of whether the [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) property returns **true**, use the **Rule.Execute** method. To apply the rule for the current session and beyond the current session, use both the **Rule.Enabled** property and the [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) method.</span></span>

<span data-ttu-id="fdd00-127">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="fdd00-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fdd00-128">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd00-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fdd00-129">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="fdd00-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fdd00-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdd00-130">See also</span></span>

- [<span data-ttu-id="fdd00-131">Regeln</span><span class="sxs-lookup"><span data-stu-id="fdd00-131">Rules</span></span>](rules.md)

