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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320412"
---
# <a name="enumerate-and-add-categories"></a><span data-ttu-id="fd880-102">Aufzählen und Hinzufügen von Kategorien</span><span class="sxs-lookup"><span data-stu-id="fd880-102">Enumerate and add categories</span></span>

<span data-ttu-id="fd880-103">Dieses Beispiel zeigt, wie Sie Kategorien auflisten und eine Kategorie zur Hauptkategorieliste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd880-103">This example shows how to enumerate categories and add a category to the main category list.</span></span>

## <a name="example"></a><span data-ttu-id="fd880-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fd880-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fd880-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fd880-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fd880-106">Das Outlook-Objektmodell unterstützt zur besseren Organisation des Posteingangs von Benutzern Kategorien.</span><span class="sxs-lookup"><span data-stu-id="fd880-106">The Outlook object model supports categories that help organize items in a user’s Inbox.</span></span> <span data-ttu-id="fd880-107">Um eine höhere Organisationsebene beizubehalten, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="fd880-107">To maintain a higher level of organization, you can do the following:</span></span>

- <span data-ttu-id="fd880-108">Outlook-Elemente in Kategorien unterteilen und nach Kategorie anzeigen</span><span class="sxs-lookup"><span data-stu-id="fd880-108">Categorize Outlook items and display them by category.</span></span>
- <span data-ttu-id="fd880-109">Mehrere Farbkategorien auf ein einzelnes Outlook-Element anwenden</span><span class="sxs-lookup"><span data-stu-id="fd880-109">Apply multiple color categories to a single Outlook item.</span></span>
- <span data-ttu-id="fd880-110">Outlook-Elemente nach Farbkategorie gruppieren und sortieren</span><span class="sxs-lookup"><span data-stu-id="fd880-110">Group and sort Outlook items by color category.</span></span>
- <span data-ttu-id="fd880-111">Jeder Farbkategorie Tastenkombinationen zuordnen, damit Benutzer Elemente einfacher kategorisieren können</span><span class="sxs-lookup"><span data-stu-id="fd880-111">Assign shortcut keys to each color category, enabling users to more easily categorize items.</span></span>
- <span data-ttu-id="fd880-112">Farbkategorien entweder programmgesteuert oder über eine Benutzeraktion auf der Outlook-Benutzeroberfläche erstellen, löschen und ändern</span><span class="sxs-lookup"><span data-stu-id="fd880-112">Create, delete, and change color categories either programmatically, or by user action within the Outlook user interface.</span></span>

<span data-ttu-id="fd880-113">Um die Funktionalität von Kategorien zur Verfügung zu stellen, bietet das Outlook-Objektmodell ein [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) -Objekt, das eine einzelne benutzerdefinierte Farbkategorie in der Hauptkategorieliste darstellt.</span><span class="sxs-lookup"><span data-stu-id="fd880-113">To expose the functionality of categories, the Outlook object model provides a [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object that represents a single user-defined color category in the main category list.</span></span> <span data-ttu-id="fd880-114">Die Hauptkategorieliste enthält Farbkategorien, die auf der Outlook-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd880-114">The main category list contains color categories that are presented in the Outlook user interface.</span></span> <span data-ttu-id="fd880-115">Die Liste wird von der [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) -Auflistung des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fd880-115">The list is represented by the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="fd880-116">Verwenden Sie zum Erstellen eines **Category**-Objekts die [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) -Methode der **Categories**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="fd880-116">To create a **Category** object, use the [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) method of the **Categories** collection.</span></span> <span data-ttu-id="fd880-117">Beim Erstellen eines **Category**-Objekts wird eine GUID (global eindeutige ID) erstellt, die nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd880-117">When you create a **Category** object, a globally unique identifier (GUID) is created, and this identifier cannot be changed.</span></span> <span data-ttu-id="fd880-118">Diese wird von der [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\))-Eigenschaft dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fd880-118">It is represented by the [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)) property.</span></span> <span data-ttu-id="fd880-119">Sie können jedoch den Namen, die Farbe und die Tastenkombination ändern, der/die einer Farbkategorie zugeordnet ist, indem Sie die Eigenschaften [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)) und [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) des **Category**-Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="fd880-119">You can, however, change the name, color, and shortcut key associated with a color category by setting the [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)), and [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) properties, respectively, of the **Category** object.</span></span> <span data-ttu-id="fd880-120">Sie können die **Color**-Eigenschaft ändern, indem Sie ihre [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\))-Konstante festlegen oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="fd880-120">You can change the **Color** property by setting or getting its [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)) constant.</span></span> <span data-ttu-id="fd880-121">Verwenden Sie zum Reproduzieren der Farben in einem benutzerdefinierten Steuerelement die folgenden schreibgeschützten Eigenschaften des **Category**-Objekts:</span><span class="sxs-lookup"><span data-stu-id="fd880-121">To reproduce the color in a custom control, use the following read-only properties of the **Category** object:</span></span>

  - <span data-ttu-id="fd880-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="fd880-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span></span>

  - <span data-ttu-id="fd880-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="fd880-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span></span>

  - <span data-ttu-id="fd880-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="fd880-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span></span>

<span data-ttu-id="fd880-125">Diese Eigenschaften geben einen **OLE\_COLOR**-Wert zurück, der von der **Color**-Eigenschaft des **Category**-Objekts abhängt.</span><span class="sxs-lookup"><span data-stu-id="fd880-125">These properties return an **OLE\_COLOR** value, which is dependent on the **Color** property of the **Category** object.</span></span>

<span data-ttu-id="fd880-p103">Outlook-Elemente werden basierend auf dem Kategorienamen angezeigt. Jedes Elementobjekt hat eine **Categories**-Eigenschaft, in der eine Zeichenfolge mit Kommas als Trennzeichen gespeichert wird, die Kategorienamen darstellt. (Für das [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) -Objekt verwenden Sie z. B. die **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) -Eigenschaft). Dadurch können Sie dem Element eine Kategorie hinzufügen, auch wenn die Kategorie nicht in der Hauptkategorieliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fd880-p103">Outlook items are displayed based on the category name. Each item object has a **Categories** property that stores a comma-delimited string that represents category names. (For example, for the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object, you would use the **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) property). This enables you to add a category to the item, even if the category is not present in the main category list.</span></span>


> [!NOTE]
> <span data-ttu-id="fd880-p104">[!HINWEIS] Wenn die **Categories**-Eigenschaft eines Elements einen Kategorienamen enthält, der nicht in der **Categories**-Auflistung des **NameSpace**-Objekts vorhanden ist, wird der Kategoriename, der diesem Outlook-Element zugeordnet ist, ohne zugeordnete Farbe angezeigt. Die **Categories**-Eigenschaft eines **Item**-Objekts gibt keine **Categories**-Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="fd880-p104">If the **Categories** property of an item contains a category name that is not in the **Categories** collection of the **NameSpace** object, the category name associated with that Outlook item is displayed, but without an associated color. The **Categories** property on an **Item** object does not return a **Categories** collection.</span></span>

<span data-ttu-id="fd880-132">Im folgenden Codebeispiel ruft die erste Prozedur EnumerateCategories die Hauptkategorieliste des aktuellen Benutzers ab, die von der **Categories**-Auflistung dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd880-132">In the following code example, the first procedure, EnumerateCategories, gets the current user’s main list of categories, represented by the **Categories** collection.</span></span> <span data-ttu-id="fd880-133">Sie zählt anschließend die **Category**-Objekte in diese Auflistung auf und schreibt die Eigenschaften **Name** und **CategoryID** in die Listeners für die Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="fd880-133">It then enumerates the **Category** objects in that collection, and writes the **Name** and **CategoryID** properties to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="fd880-134">Die zweite Prozedur AddACategory ruft die Hauptkategorieliste des aktuellen Benutzers ab und verwendet die CategoryExists-Methode zum Überprüfen, ob die Kategorie "ISV" in der Auflistung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fd880-134">The second procedure, AddACategory, gets the current user’s main list of categories and uses the CategoryExists method to check whether a category named “ISV” exists in the collection.</span></span> <span data-ttu-id="fd880-135">Wenn keine Kategorie mit dem Namen "ISV" vorhanden ist, fügt AddACategory der Hauptkategorieliste die Kategorie "ISV" hinzu und ordnet ihr die Farbe Dunkelblau mithilfe der **Add**-Methode der **Categories**-Auflistung zu.</span><span class="sxs-lookup"><span data-stu-id="fd880-135">If no category with the name “ISV” exists, AddACategory adds a category named “ISV” to the main category list and assigns it a dark blue color by using the **Add** method of the **Categories** collection.</span></span> <span data-ttu-id="fd880-136">Sie weist auch STRG + F11 als die Tastenkombination für die Kategorie.</span><span class="sxs-lookup"><span data-stu-id="fd880-136">It also assigns CTRL+F11 as the shortcut key for the category.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fd880-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd880-137">See also</span></span>

- [<span data-ttu-id="fd880-138">Farbkategorien</span><span class="sxs-lookup"><span data-stu-id="fd880-138">Color categories</span></span>](color-categories.md)

