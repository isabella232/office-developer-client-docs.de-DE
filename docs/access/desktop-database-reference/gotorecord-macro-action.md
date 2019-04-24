---
title: GoToRecord-Makroaktion
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292139"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="82a6d-102">GoToRecord-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="82a6d-102">GoToRecord macro action</span></span>


<span data-ttu-id="82a6d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82a6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82a6d-104">Mit der **GeheZuDatensatz**-Aktion können Sie den angegebenen Datensatz zum aktuellen Datensatz in einer geöffneten Tabelle oder einem geöffneten Formular oder Abfrageresultset machen.</span><span class="sxs-lookup"><span data-stu-id="82a6d-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="82a6d-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="82a6d-105">Setting</span></span>

<span data-ttu-id="82a6d-106">Die **GeheZuDatensatz**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="82a6d-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82a6d-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="82a6d-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="82a6d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82a6d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82a6d-109"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="82a6d-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="82a6d-110">Der Objekttyp, der den Datensatz enthält, den Sie aktuell machen möchten.</span><span class="sxs-lookup"><span data-stu-id="82a6d-110">The type of object that contains the record you want to make current.</span></span> <span data-ttu-id="82a6d-111">Klicken Sie im Feld <strong>Objekttyp</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Server Ansicht</strong>, <strong>gespeicherte Prozedur</strong>oder <strong>Funktion</strong> .</span><span class="sxs-lookup"><span data-stu-id="82a6d-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="82a6d-112">Lassen Sie dieses Argument leer, um das aktive Objekt auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="82a6d-112">Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82a6d-113"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="82a6d-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="82a6d-p102">Der Name des Objekts, das den Datensatz enthält, den sie zum aktuellen Datensatz machen möchten. Im Feld <strong>Objektname</strong> werden alle Objekte in der aktuellen Datenbank angezeigt, die den durch das Argument <strong>Objekttyp</strong> angegebenen Typ aufweisen. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</span><span class="sxs-lookup"><span data-stu-id="82a6d-p102">The name of the object that contains the record you want to make the current record. The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82a6d-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="82a6d-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="82a6d-p103">Der Datensatz, der zum aktuellen Datensatz werden soll. Klicken Sie im Feld <strong>Datensatz</strong> auf <strong>Vorheriger</strong>, <strong>Nächster</strong>, <strong>Erster</strong>, <strong>Letzter</strong>, <strong>Gehe zu</strong> oder <strong>Neu</strong>. Die Standardeinstellung ist <strong>Nächster</strong>.</span><span class="sxs-lookup"><span data-stu-id="82a6d-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82a6d-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="82a6d-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="82a6d-122">Eine ganze Zahl oder ein Ausdruck, der zu einer ganzen Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="82a6d-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="82a6d-123">Einem Ausdruck muss ein Gleichheitszeichen vorangestellt werden (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="82a6d-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="82a6d-124">Mit diesem Argument wird der Datensatz angegeben, der zum aktuellen Datensatz werden soll.</span><span class="sxs-lookup"><span data-stu-id="82a6d-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="82a6d-125">Sie können das Argument <strong>Offset</strong> auf zwei Arten verwenden:</span><span class="sxs-lookup"><span data-stu-id="82a6d-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="82a6d-126">Wenn das Argument <strong>Datensatz</strong> auf <strong>Nächster</strong> oder <strong>Vorheriger</strong> festgelegt ist, verschiebt Microsoft Office Access 2007 den Fokus um die Anzahl von Datensätzen nach vorn oder hinten, die im Argument <strong>Offset</strong> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="82a6d-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="82a6d-p105">Wenn das Argument <strong>Datensatz</strong> auf <strong>Gehe zu</strong> festgelegt ist, wechselt Access zu dem Datensatz mit der Nummer, die dem Argument <strong>Offset</strong> entspricht. Die Datensatznummer wird im Datensatznummernfeld am unteren Rand des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82a6d-p105">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p>
<p><span data-ttu-id="82a6d-129"><strong>Hinweis</strong>: Wenn Sie die <strong>erste</strong>, <strong>Letzte</strong>oder <strong>neue</strong> Einstellung für das Argument <strong>Record</strong> verwenden, ignoriert Access das <strong>Offset</strong> -Argument.</span><span class="sxs-lookup"><span data-stu-id="82a6d-129"><strong>NOTE</strong>: If you use the <strong>First</strong>, <strong>Last</strong>, or <strong>New</strong> setting for the <strong>Record</strong> argument, Access ignores the <strong>Offset</strong> argument.</span></span> <span data-ttu-id="82a6d-130">Wenn Sie einen Wert für <strong>Offset</strong> eingeben, der zu groß ist, zeigt Access eine Fehlermeldung an.</span><span class="sxs-lookup"><span data-stu-id="82a6d-130">If you enter an <strong>Offset</strong> argument that is too large, Access displays an error message.</span></span> <span data-ttu-id="82a6d-131">Sie können keine negative Zahlen für das Argument <strong>Offset</strong> eingeben.</span><span class="sxs-lookup"><span data-stu-id="82a6d-131">You can't enter negative numbers for the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="82a6d-132">Wenn das Argument <strong>Datensatz</strong> auf <strong>Nächster</strong> oder <strong>Vorheriger</strong> festgelegt ist, verschiebt Microsoft Office Access 2007 den Fokus um die Anzahl von Datensätzen nach vorn oder hinten, die im Argument <strong>Offset</strong> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="82a6d-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="82a6d-p107">Wenn das Argument <strong>Datensatz</strong> auf <strong>Gehe zu</strong> festgelegt ist, wechselt Access zu dem Datensatz mit der Nummer, die dem Argument <strong>Offset</strong> entspricht. Die Datensatznummer wird im Datensatznummernfeld am unteren Rand des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82a6d-p107">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="82a6d-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82a6d-135">Remarks</span></span>

<span data-ttu-id="82a6d-136">Wenn sich der Fokus in einem bestimmten Steuerelement in einem Datensatz befindet, belässt diese Aktion den Fokus im selben Steuerelement für den neuen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="82a6d-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="82a6d-137">Sie können die Einstellung **Neu** für das Argument **Datensatz** verwenden, um sich zum leeren Datensatz am Ende eines Formulars oder einer Tabelle zu bewegen, sodass Sie neue Daten eingeben können.</span><span class="sxs-lookup"><span data-stu-id="82a6d-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="82a6d-p108">Diese Aktion ist mit dem Klicken auf den Pfeil unterhalb der Schaltfläche **Suchen** auf der Registerkarte **Start** und dem anschließenden Klicken auf **Gehe zu** vergleichbar. Die Unterbefehle **Erster**, **Letzter**, **Nächster**, **Vorheriger** und **Neuer Datensatz** des Befehls **Gehe zu** haben dieselbe Wirkung auf das ausgewählte Objekt wie die Einstellungen **Erster**, **Letzter**, **Nächster**, **Vorheriger** und **Neu** für das Argument **Datensatz**. Sie können auch zu Datensätzen wechseln, indem Sie die Navigationsschaltflächen am unteren Rand des Fensters verwenden.</span><span class="sxs-lookup"><span data-stu-id="82a6d-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="82a6d-141">Sie können die **GeheZuDatensatz** -Aktion verwenden, um einen Datensatz in einem ausgeblendeten Formular zum aktuellen Datensatz zu machen, indem Sie das ausgeblendete Formular in den Argumenten **Objekttyp** und **Objektname** angeben.</span><span class="sxs-lookup"><span data-stu-id="82a6d-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="82a6d-142">Verwenden Sie die **GoToRecord** -Methode des **DoCmd** -Objekts, um die **GeheZuDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="82a6d-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

