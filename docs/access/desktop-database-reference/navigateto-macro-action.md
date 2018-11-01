---
title: NavigierenZu-Makroaktion
TOCTitle: NavigateTo Macro Action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6cb9505eaf4a2002b0a4ae73ce4917ac250cda12
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876057"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="612a0-102">NavigierenZu-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="612a0-102">NavigateTo Macro Action</span></span>


<span data-ttu-id="612a0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="612a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="612a0-p101">Sie können mit der **NavigierenZu** -Aktion das Anzeigen von Datenbankobjekten im Navigationsbereich steuern. Sie können beispielsweise die Kategorisierungsweise von Datenbankobjekten ändern und die Objekte filtern, sodass nur bestimmte Objekte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="612a0-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="612a0-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="612a0-106">Setting</span></span>

<span data-ttu-id="612a0-107">Die **NavigierenZu** -Aktion hat folgende Argumente.</span><span class="sxs-lookup"><span data-stu-id="612a0-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="612a0-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="612a0-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="612a0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="612a0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="612a0-110"><strong>Category</strong></span><span class="sxs-lookup"><span data-stu-id="612a0-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="612a0-p102">Erforderlich. Die Kategorie, gemäß der Objekte im Navigationsbereich angezeigt werden sollen. Klicken Sie im Feld <strong>Kategorie</strong> auf <strong>Objekttyp</strong>, <strong>Tabellen und Ansichten</strong>, <strong>Änderungsdatum</strong>, <strong>Erstellungsdatum</strong> oder <strong>Benutzerdefiniert</strong>.</span><span class="sxs-lookup"><span data-stu-id="612a0-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="612a0-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="612a0-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="612a0-115">Optional.</span><span class="sxs-lookup"><span data-stu-id="612a0-115">Optional.</span></span> <span data-ttu-id="612a0-116"><strong>Das Argument Grenzwerte der Objekte in der Kategorie</strong> im Navigationsbereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="612a0-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="612a0-117">Wenn Sie das <strong>Gruppe</strong> Argument leer lassen, wird im Navigationsbereich alle Datenbankobjekte kategorisiert nach den Kriterien im Argument " <strong>Category"</strong> festgelegten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="612a0-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="612a0-118">In der folgenden Tabelle sind Beispiele gültiger Argumente <strong>Group</strong> für die verschiedenen <strong>Kategorie</strong> Argumente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="612a0-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="612a0-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="612a0-119">Remarks</span></span>

  - <span data-ttu-id="612a0-120">Diese Aktion ist mit dem Auswählen von Kategorien und Gruppen in der Titelleiste des Navigationsbereichs vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="612a0-120">This action is similar to selecting categories and groups from the title bar of the Navigation Pane.</span></span>

  - <span data-ttu-id="612a0-p104">Gültige Argumente vom Typ **Gruppe** hängen vom verwendeten Argument **Kategorie** ab. Wenn Sie für **Gruppe** ein ungültiges Argument eingeben, wird eine Fehlermeldung angezeigt.Die folgende Tabelle enthält Beispiele gültiger Argumente vom Typ **Gruppe** für jedes Argument vom Typ **Kategorie**.</span><span class="sxs-lookup"><span data-stu-id="612a0-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="612a0-123">Argument "Kategorie"</span><span class="sxs-lookup"><span data-stu-id="612a0-123">Category argument</span></span></p></th>
    <th><p><span data-ttu-id="612a0-124">Beispiel für Argumente vom Typ "Gruppe"</span><span class="sxs-lookup"><span data-stu-id="612a0-124">Example Group arguments</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="612a0-125">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="612a0-125">Object Type</span></span></p></td>
    <td><p><span data-ttu-id="612a0-126">Tabellen, Formulare, Abfragen, Seiten, Makros, Module</span><span class="sxs-lookup"><span data-stu-id="612a0-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="612a0-127">Tabellen und Sichten</span><span class="sxs-lookup"><span data-stu-id="612a0-127">Tables and Views</span></span></p></td>
    <td><p><span data-ttu-id="612a0-128">Namen bestimmter Tabellen in der Datenbank</span><span class="sxs-lookup"><span data-stu-id="612a0-128">Names of specific tables in your database</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="612a0-129">Geändert am</span><span class="sxs-lookup"><span data-stu-id="612a0-129">Modified Date</span></span></p></td>
    <td><p><span data-ttu-id="612a0-130">Heute, Gestern, Letzten Monat, Älter</span><span class="sxs-lookup"><span data-stu-id="612a0-130">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="612a0-131">Erstellt am</span><span class="sxs-lookup"><span data-stu-id="612a0-131">Created Date</span></span></p></td>
    <td><p><span data-ttu-id="612a0-132">Heute, Gestern, Letzten Monat, Älter</span><span class="sxs-lookup"><span data-stu-id="612a0-132">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="612a0-133">Benutzerdefinierte Kategorie</span><span class="sxs-lookup"><span data-stu-id="612a0-133">Custom category</span></span></p></td>
    <td><p><span data-ttu-id="612a0-134">Namen von Gruppen, die Sie für die angegebene benutzerdefinierte Kategorie erstellt haben</span><span class="sxs-lookup"><span data-stu-id="612a0-134">Names of groups you have created for the specified custom category</span></span></p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="612a0-135">Verwenden Sie zum Ausführen der **NavigierenZu** -Aktion in einem VBA-Modul die **NavigateTo** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="612a0-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="612a0-p105">Sie müssen zum Navigieren zur obersten Ebene einer Kategorie (beispielsweise Alle Tabellen, Alle Access-Objekte oder Alle Datumswerte) das Argument Gruppe leer lassen. Wenn beispielsweise das Argument Kategorie den Wert Objekttyp aufweist, wird durch Alle Access-Objekte als Argument Gruppe ein Fehler hervorgerufen.</span><span class="sxs-lookup"><span data-stu-id="612a0-p105">To navigate to the top level of a category (for example, <STRONG>All Tables</STRONG>, <STRONG>All Access Objects</STRONG>, or <STRONG>All Dates</STRONG>), you must leave the Group argument blank. For example, when the <STRONG>Category</STRONG> argument is <STRONG>Object Type</STRONG>, entering <STRONG>All Access Objects</STRONG> as a <STRONG>Group</STRONG> argument results in an error.</span></span></P>


