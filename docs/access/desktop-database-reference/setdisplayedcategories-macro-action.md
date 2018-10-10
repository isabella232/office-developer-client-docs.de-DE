---
title: FestlegenAngezeigteKategorien-Makroaktion
TOCTitle: SetDisplayedCategories Macro Action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
ms.openlocfilehash: af4b491ff76a28c998e1ec195a861dbf065d36c8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475385"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="b68ee-102">FestlegenAngezeigteKategorien-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="b68ee-102">SetDisplayedCategories Macro Action</span></span>


<span data-ttu-id="b68ee-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b68ee-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b68ee-p101">Sie können mithilfe der **FestlegenAngezeigteKategorien** -Aktion festlegen, welche Kategorien in der Titelleiste des Navigationsbereichs unter **Navigieren zur Kategorie** angezeigt werden. Wenn Sie beispielsweise verhindern möchten, dass Benutzer den Navigationsbereich wechseln, sodass nach **Erstellt am** sortierte Objekte angezeigt werden, können Sie mit dieser Aktion die Option in der Dropdownliste der Titelleiste ausblenden.</span><span class="sxs-lookup"><span data-stu-id="b68ee-p101">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="b68ee-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="b68ee-106">Setting</span></span>

<span data-ttu-id="b68ee-107">Die **FestlegenAngezeigteKategorien** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="b68ee-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b68ee-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="b68ee-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b68ee-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b68ee-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b68ee-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="b68ee-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="b68ee-p102">Wählen Sie <strong>Ja</strong> aus, um die Kategorien einzublenden, und <strong>Nein</strong>, um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="b68ee-p102">Select <strong>Yes</strong> to show the category or categories. Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b68ee-113"><strong>Category</strong></span><span class="sxs-lookup"><span data-stu-id="b68ee-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="b68ee-p103">Geben Sie den Namen der Kategorie ein, die Sie ein- oder ausblenden möchten, oder wählen Sie ihn aus. Lassen Sie das Feld leer, um alle Kategorien ein- oder auszublenden.</span><span class="sxs-lookup"><span data-stu-id="b68ee-p103">Enter or select the name of the category you want to show or hide. Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b68ee-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b68ee-116">Remarks</span></span>

  - <span data-ttu-id="b68ee-p104">Die Beschriftung in der Titelleiste des Navigationsbereichs gibt an, welcher Filter ggf. derzeit aktiv ist. Klicken Sie auf eine beliebige Stelle in der Leiste, um die Dropdownliste anzuzeigen. Die durch diese Makroaktion gesteuerten Elemente werden unter **Navigieren zur Kategorie** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b68ee-p104">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active. Click anywhere in the bar to display the drop-down list. The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="b68ee-120">Diese Aktion ist nur aktiviert oder deaktiviert die Anzeige des angegebenen Kategorie oder Kategorien; Wechseln der Anzeige im Navigationsbereich wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b68ee-120">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display.</span></span> <span data-ttu-id="b68ee-121">Angenommen, wenn Sie Objekte nach **Erstellungsdatum** sortiert anzeigen, und Sie die **FestlegenAngezeigteKategorien** -Aktion verwenden, um **die Option** zu deaktivieren, wechselt Access im Navigationsbereich zu einer anderen Kategorie nicht.</span><span class="sxs-lookup"><span data-stu-id="b68ee-121">For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="b68ee-122">Verwenden Sie die **FestlegenAngezeigteKategorien** -Methode des **DoCmd** -Objekts, um die **FestlegenAngezeigteKategorien** -Aktion in einem VBA-Modul auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b68ee-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

