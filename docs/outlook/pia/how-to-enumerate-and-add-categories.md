---
title: Aufzählen und Hinzufügen von Kategorien
TOCTitle: Enumerate and add categories
ms:assetid: 17a94a01-c463-4332-851e-7d280c66d8c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424467(v=office.15)
ms:contentKeyID: 55119829
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 488e00971adb1f2fa38555039478ac830d3c9f7a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717755"
---
# <a name="enumerate-and-add-categories"></a>Aufzählen und Hinzufügen von Kategorien

Dieses Beispiel zeigt, wie Sie Kategorien auflisten und eine Kategorie zur Hauptkategorieliste hinzufügen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Das Outlook-Objektmodell unterstützt zur besseren Organisation des Posteingangs von Benutzern Kategorien. Um eine höhere Organisationsebene beizubehalten, gehen Sie folgendermaßen vor:

- Outlook-Elemente in Kategorien unterteilen und nach Kategorie anzeigen
- Mehrere Farbkategorien auf ein einzelnes Outlook-Element anwenden
- Outlook-Elemente nach Farbkategorie gruppieren und sortieren
- Jeder Farbkategorie Tastenkombinationen zuordnen, damit Benutzer Elemente einfacher kategorisieren können
- Farbkategorien entweder programmgesteuert oder über eine Benutzeraktion auf der Outlook-Benutzeroberfläche erstellen, löschen und ändern

Um die Funktionalität von Kategorien zur Verfügung zu stellen, bietet das Outlook-Objektmodell ein [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) -Objekt, das eine einzelne benutzerdefinierte Farbkategorie in der Hauptkategorieliste darstellt. Die Hauptkategorieliste enthält Farbkategorien, die auf der Outlook-Benutzeroberfläche angezeigt werden. Die Liste wird von der [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) -Auflistung des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts dargestellt. Verwenden Sie zum Erstellen eines **Category**-Objekts die [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) -Methode der **Categories**-Auflistung. Beim Erstellen eines **Category**-Objekts wird eine GUID (global eindeutige ID) erstellt, die nicht geändert werden kann. Diese wird von der [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\))-Eigenschaft dargestellt. Sie können jedoch den Namen, die Farbe und die Tastenkombination ändern, der/die einer Farbkategorie zugeordnet ist, indem Sie die Eigenschaften [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)) und [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) des **Category**-Objekts festlegen. Sie können die **Color**-Eigenschaft ändern, indem Sie ihre [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\))-Konstante festlegen oder abrufen. Verwenden Sie zum Reproduzieren der Farben in einem benutzerdefinierten Steuerelement die folgenden schreibgeschützten Eigenschaften des **Category**-Objekts:

  - [CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))

  - [CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))

  - [CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))

Diese Eigenschaften geben einen **OLE\_COLOR**-Wert zurück, der von der **Color**-Eigenschaft des **Category**-Objekts abhängt.

Outlook-Elemente werden basierend auf dem Kategorienamen angezeigt. Jedes Elementobjekt hat eine **Categories**-Eigenschaft, in der eine Zeichenfolge mit Kommas als Trennzeichen gespeichert wird, die Kategorienamen darstellt. (Für das [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) -Objekt verwenden Sie z. B. die **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) -Eigenschaft). Dadurch können Sie dem Element eine Kategorie hinzufügen, auch wenn die Kategorie nicht in der Hauptkategorieliste vorhanden ist.


> [!NOTE]
> Wenn die **Categories**-Eigenschaft eines Elements einen Kategorienamen enthält, der nicht in der **Categories**-Auflistung des **NameSpace**-Objekts vorhanden ist, wird der Kategoriename, der diesem Outlook-Element zugeordnet ist, ohne zugeordnete Farbe angezeigt. Die **Categories**-Eigenschaft eines **Item**-Objekts gibt keine **Categories**-Auflistung zurück.

Im folgenden Codebeispiel ruft die erste Prozedur EnumerateCategories die Hauptkategorieliste des aktuellen Benutzers ab, die von der **Categories**-Auflistung dargestellt wird. Sie zählt anschließend die **Category**-Objekte in diese Auflistung auf und schreibt die Eigenschaften **Name** und **CategoryID** in die Listeners für die Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung. Die zweite Prozedur AddACategory ruft die Hauptkategorieliste des aktuellen Benutzers ab und verwendet die CategoryExists-Methode zum Überprüfen, ob die Kategorie "ISV" in der Auflistung vorhanden ist. Wenn keine Kategorie mit dem Namen "ISV" vorhanden ist, fügt AddACategory der Hauptkategorieliste die Kategorie "ISV" hinzu und ordnet ihr die Farbe Dunkelblau mithilfe der **Add**-Methode der **Categories**-Auflistung zu. Sie weist auch STRG + F11 als die Tastenkombination für die Kategorie.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateCategories()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    foreach (Outlook.Category category in categories)
    {
        Debug.WriteLine(category.Name);
        Debug.WriteLine(category.CategoryID);
    }
}

private void AddACategory()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    if (!CategoryExists("ISV"))
    {
        Outlook.Category category = categories.Add("ISV",
            Outlook.OlCategoryColor.olCategoryColorDarkBlue,
            Outlook.OlCategoryShortcutKey.olCategoryShortcutKeyCtrlF11);
    }
}

private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category = 
            Application.Session.Categories[categoryName];
        if(category != null)
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

- [Farbkategorien](color-categories.md)

