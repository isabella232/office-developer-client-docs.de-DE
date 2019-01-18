---
title: OpenView-Makroaktion
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 88bebab46cd6b76fb101c86c4fe33c5ab86a3e70
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699009"
---
# <a name="openview-macro-action"></a><span data-ttu-id="e08c7-102">OpenView-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="e08c7-102">OpenView macro action</span></span>

<span data-ttu-id="e08c7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e08c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e08c7-p101">In einem Access-Projekt können Sie die **ÖffnenSicht** -Aktion zum Öffnen einer Sicht in der Datenblattansicht, der Entwurfsansicht oder der Seitenansicht verwenden. Wenn die benannte Ansicht in der Datenblattansicht geöffnet wird, wird sie mit dieser Aktion ausgeführt. Für diese Ansicht können Sie die Dateneingabe auswählen und die in der Ansicht angezeigten Datensätze einschränken.</span><span class="sxs-lookup"><span data-stu-id="e08c7-p101">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview. This action runs the named view when opened in Datasheet view. You can select data entry for the view and restrict the records that the view displays.</span></span>

> [!NOTE]
> <span data-ttu-id="e08c7-107">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="e08c7-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="e08c7-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="e08c7-108">Setting</span></span>

<span data-ttu-id="e08c7-109">Die **ÖffnenSicht** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="e08c7-109">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e08c7-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="e08c7-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e08c7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e08c7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e08c7-112"><strong>Sichtname</strong></span><span class="sxs-lookup"><span data-stu-id="e08c7-112"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e08c7-113">Der Name der Ansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e08c7-113">The name of the view to open.</span></span> <span data-ttu-id="e08c7-114">Das Feld <strong>Sichtname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Ansichten in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e08c7-114">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="e08c7-115">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="e08c7-115">This is a required argument.</span></span> <span data-ttu-id="e08c7-116">Wenn Sie ein Makro, das die <strong>ÖffnenSicht</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Diagramm mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="e08c7-116">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e08c7-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="e08c7-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="e08c7-p103">Die Ansicht, in der die Sicht geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</span><span class="sxs-lookup"><span data-stu-id="e08c7-p103">The view in which the view will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e08c7-121"><strong>Data Mode</strong></span><span class="sxs-lookup"><span data-stu-id="e08c7-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="e08c7-p104">Der Dateneingabemodus für die Sicht. Dies gilt nur für Sichten, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, jedoch keine vorhandenen Datensätze anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="e08c7-p104">The data entry mode for the view. This applies only to views opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e08c7-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e08c7-126">Remarks</span></span>

<span data-ttu-id="e08c7-127">Diese Aktion ist mit dem Doppelklicken auf eine Ansicht im Navigationsbereich, dem Klicken mit der rechten Maustaste auf die Ansicht im Navigationsbereich und dem Klicken auf den gewünschten Befehl vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="e08c7-127">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

> [!TIP]
> - <span data-ttu-id="e08c7-p105">Sie können eine Tabelle aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine **ÖffnenSicht** -Aktion erstellt, die die Tabelle in der Datenblattansicht öffnet.</span><span class="sxs-lookup"><span data-stu-id="e08c7-p105">You can drag a view from the Navigation Pane to a macro action row. This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>
> - <span data-ttu-id="e08c7-130">Wenn Sie die Systemmeldungen nicht anzeigen möchten, die normalerweise angezeigt werden, wenn eine Ansicht ausgeführt wird (sie melden, dass es sich um eine Sicht handelt und wie viele Datensätze betroffen sind), können Sie die **Warnmeldungen** -Aktion verwenden, um die Anzeige dieser Meldungen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="e08c7-130">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="e08c7-131">Verwenden Sie die **OpenView** -Methode des **DoCmd** -Objekts, um die **ÖffnenSicht** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e08c7-131">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

