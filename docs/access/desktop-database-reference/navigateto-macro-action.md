---
title: NavigateTo-Makroaktion
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288602"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="0b189-102">NavigateTo-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="0b189-102">NavigateTo macro action</span></span>

<span data-ttu-id="0b189-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b189-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b189-p101">Sie können mit der **NavigierenZu** -Aktion das Anzeigen von Datenbankobjekten im Navigationsbereich steuern. Sie können beispielsweise die Kategorisierungsweise von Datenbankobjekten ändern und die Objekte filtern, sodass nur bestimmte Objekte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b189-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="0b189-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="0b189-106">Setting</span></span>

<span data-ttu-id="0b189-107">Die **NavigierenZu**-Aktion hat folgende Argumente.</span><span class="sxs-lookup"><span data-stu-id="0b189-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b189-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="0b189-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0b189-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b189-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b189-110"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="0b189-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="0b189-p102">Erforderlich. Die Kategorie, gemäß der Objekte im Navigationsbereich angezeigt werden sollen. Klicken Sie im Feld <strong>Kategorie</strong> auf <strong>Objekttyp</strong>, <strong>Tabellen und Ansichten</strong>, <strong>Änderungsdatum</strong>, <strong>Erstellungsdatum</strong> oder <strong>Benutzerdefiniert</strong>.</span><span class="sxs-lookup"><span data-stu-id="0b189-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b189-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="0b189-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="0b189-115">Optional.</span><span class="sxs-lookup"><span data-stu-id="0b189-115">Optional.</span></span> <span data-ttu-id="0b189-116">Durch das Argument <strong>Gruppe</strong> wird beschränkt, welche Objekte im Navigationsbereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b189-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="0b189-117">Wenn Sie das Argument <strong>Gruppe</strong> leer lassen, werden im Navigationsbereich alle Datenbankobjekte angezeigt, die nach den Kriterien kategorisiert werden, die Sie im <strong>Category</strong> -Argument angeben.</span><span class="sxs-lookup"><span data-stu-id="0b189-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="0b189-118">In der folgenden Tabelle werden Beispiele gültiger Argumente vom Typ <strong>Gruppe</strong> für die zahlreichen Argumente vom Typ <strong>Kategorie</strong> gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b189-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0b189-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b189-119">Remarks</span></span>

- <span data-ttu-id="0b189-120">Diese Aktion ähnelt der Auswahl von Kategorien und Gruppen in der Titelleiste des Navigationsbereichs.</span><span class="sxs-lookup"><span data-stu-id="0b189-120">This action is similar to selecting categories and groups from the title bar of the navigation pane.</span></span>

- <span data-ttu-id="0b189-p104">Gültige Argumente vom Typ **Gruppe** hängen vom verwendeten Argument **Kategorie** ab. Wenn Sie für **Gruppe** ein ungültiges Argument eingeben, wird eine Fehlermeldung angezeigt.Die folgende Tabelle enthält Beispiele gültiger Argumente vom Typ **Gruppe** für jedes Argument vom Typ **Kategorie**.</span><span class="sxs-lookup"><span data-stu-id="0b189-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p><span data-ttu-id="0b189-123">Argument "Category"</span><span class="sxs-lookup"><span data-stu-id="0b189-123">Category argument</span></span></p></th>
  <th><p><span data-ttu-id="0b189-124">Beispiel für Argumente "Group"</span><span class="sxs-lookup"><span data-stu-id="0b189-124">Example Group arguments</span></span></p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p><span data-ttu-id="0b189-125">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="0b189-125">Object Type</span></span></p></td>
  <td><p><span data-ttu-id="0b189-126">Tabellen; Formulare; Abfragen; Seiten; Makros; Module</span><span class="sxs-lookup"><span data-stu-id="0b189-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="0b189-127">Tabellen und Sichten</span><span class="sxs-lookup"><span data-stu-id="0b189-127">Tables and Views</span></span></p></td>
  <td><p><span data-ttu-id="0b189-128">Namen bestimmter Tabellen in der Datenbank</span><span class="sxs-lookup"><span data-stu-id="0b189-128">Names of specific tables in your database</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="0b189-129">Geändert am</span><span class="sxs-lookup"><span data-stu-id="0b189-129">Modified Date</span></span></p></td>
  <td><p><span data-ttu-id="0b189-130">Heute; Gestern; Letzten Monat; Älter</span><span class="sxs-lookup"><span data-stu-id="0b189-130">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="even">
  <td><p><span data-ttu-id="0b189-131">Erstellt am</span><span class="sxs-lookup"><span data-stu-id="0b189-131">Created Date</span></span></p></td>
  <td><p><span data-ttu-id="0b189-132">Heute, Gestern, Letzten Monat, Älter</span><span class="sxs-lookup"><span data-stu-id="0b189-132">Today; Yesterday; Last Month; Older</span></span></p></td>
  </tr>
  <tr class="odd">
  <td><p><span data-ttu-id="0b189-133">Benutzerdefinierte Kategorie</span><span class="sxs-lookup"><span data-stu-id="0b189-133">Custom category</span></span></p></td>
  <td><p><span data-ttu-id="0b189-134">Namen von Gruppen, die Sie für die angegebene benutzerdefinierte Kategorie erstellt haben</span><span class="sxs-lookup"><span data-stu-id="0b189-134">Names of groups you have created for the specified custom category</span></span></p></td>
  </tr>
  </tbody>
  </table>

- <span data-ttu-id="0b189-135">Verwenden Sie zum Ausführen der **NavigierenZu**-Aktion in einem VBA-Modul die **NavigateTo**-Methode des **DoCmd**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0b189-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>

> [!NOTE]
> <span data-ttu-id="0b189-p105">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span><span class="sxs-lookup"><span data-stu-id="0b189-p105">To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.</span></span>


