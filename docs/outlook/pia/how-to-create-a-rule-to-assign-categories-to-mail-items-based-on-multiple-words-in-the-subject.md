---
title: Erstellen einer Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 50966b99febe03500feb4b693cfba50819d9b7a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560634"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a>Erstellen einer Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff

In diesem Beispiel wird gezeigt, wie eine Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff eingerichtet wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

In Outlook können Elemente zur einfacheren Organisation und Anzeige kategorisiert werden. Das Outlook-Objektmodell stellt das [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\))-Objekt und die [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\))-Auflistung zur Darstellung von Kategorien bereit. Weitere Informationen zum **Category**-Objekt und zur **Categories**-Auflistung für ein Outlook-Element finden Sie unter [Auflisten und Hinzufügen von Kategorien](how-to-enumerate-and-add-categories.md).

Eine Regel, die von einem [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\))-Objekt dargestellt wird, kann mehreren Bedingungen zugewiesen werden. Sie können ein Array abrufen oder festlegen, das auszuwertende Bedingungen oder auszuführende Aktionen darstellt. Beispielsweise wird von der [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) -Eigenschaft des [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) -Objekts ein Array von Zeichenfolgenelementen zurückgegeben oder festgelegt, das den von der Regelbedingung auszuwertenden Text darstellt. Sie müssen ein Array mit einer oder mehreren Zeichenfolgen für die Auswertung zuordnen. Um mehrere Textzeichenfolgen auszuwerten, die in einem Array zugewiesen sind, verwenden Sie die logische ODER-Operation. 

Folgende Eigenschaften können Sie zum Abrufen oder Festlegen eines Arrays verwenden: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) und **TextRuleCondition.Text**. Weitere Informationen zu Regeln finden Sie unter [Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).

Im folgenden Beispiel verwendet CreateTextAndCategoryRule die CategoryExists-Methode, um die E-Mail-Elemente des Benutzers anhand des Namens "Office" oder "Outlook" in der **Categories**-Auflistung auf Kategorien zu durchsuchen. Wenn keine Kategorien gefunden werden, werden diese hinzugefügt. Anschließend wird in dem Beispiel ein Array von Zeichenfolgen erstellt, die “Office", “Outlook” und “2007” enthalten. Dieses Array stellt die Kriterien dar, die ausgewertet werden sollen. Danach wird von CreateTextAndCategoryRule eine Regel erstellt, die durch Untersuchen des Betreffs auf die Bedingungen in dem Array mithilfe der **Text**-Eigenschaft des **TextRuleCondition**-Objekts und der [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\))-Eigenschaft der [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\))-Auflistung Kategorien zuordnet. Ist die Bedingung erfüllt, werden dem Element mithilfe der [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) -Methode des [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) -Objekts die Kategorien Office und Outlook zugeordnet.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateTextAndCategoryRule()
{
    if (!CategoryExists("Office"))
    {
        Application.Session.Categories.Add(
            "Office", Type.Missing, Type.Missing);
    }
    if (!CategoryExists("Outlook"))
    {
        Application.Session.Categories.Add(
            "Outlook", Type.Missing, Type.Missing);
    }
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule textRule =
        rules.Create("Demo Text and Category Rule",
        Outlook.OlRuleType.olRuleReceive);
    Object[] textCondition = 
        { "Office", "Outlook", "2007" };
    Object[] categoryAction = 
        { "Office", "Outlook" };
    textRule.Conditions.BodyOrSubject.Text =
        textCondition;
    textRule.Conditions.BodyOrSubject.Enabled = true;
    textRule.Actions.AssignToCategory.Categories =
        categoryAction;
    textRule.Actions.AssignToCategory.Enabled = true;
    rules.Save(true);
}

// Determines if categoryName exists in Categories collection
private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category =
            Application.Session.Categories[categoryName];
        if (category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>Siehe auch

- [Regeln](rules.md)

