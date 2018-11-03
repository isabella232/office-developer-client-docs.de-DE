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
ms.openlocfilehash: 5986b8e891b42ce37cb68d8ce06e7f33feba1b8f
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937729"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="c7e84-102">GoToRecord-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="c7e84-102">GoToRecord macro action</span></span>


<span data-ttu-id="c7e84-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7e84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7e84-104">Mit der **GeheZuDatensatz** -Aktion können Sie den angegebenen Datensatz zum aktuellen Datensatz in einer geöffneten Tabelle oder einem geöffneten Formular oder Abfrageresultset machen.</span><span class="sxs-lookup"><span data-stu-id="c7e84-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="c7e84-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c7e84-105">Setting</span></span>

<span data-ttu-id="c7e84-106">Die **GeheZuDatensatz** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="c7e84-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7e84-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="c7e84-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c7e84-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7e84-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7e84-109"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="c7e84-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e84-p101">Der Typ des Objekts, das den Datensatz enthält, den Sie zum aktuellen Datensatz machen möchten. Klicken Sie auf Tabelle, auf Abfrage, auf Formular, auf Serversicht, auf Gespeicherte Prozedur oder auf Funktion im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator. Lassen Sie dieses Argument leer, um das aktive Objekt auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c7e84-p101">The type of object that contains the record you want to make current. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7e84-113"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="c7e84-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e84-p102">Der Name des Objekts, das den Datensatz enthält, den sie zum aktuellen Datensatz machen möchten. Im Feld <strong>Objektname</strong> werden alle Objekte in der aktuellen Datenbank angezeigt, die den durch das Argument <strong>Objekttyp</strong> angegebenen Typ aufweisen. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</span><span class="sxs-lookup"><span data-stu-id="c7e84-p102">The name of the object that contains the record you want to make the current record. The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7e84-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="c7e84-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e84-p103">Der Datensatz, der zum aktuellen Datensatz werden soll. Klicken Sie im Feld <strong>Datensatz</strong> auf <strong>Vorheriger</strong>, <strong>Nächster</strong>, <strong>Erster</strong>, <strong>Letzter</strong>, <strong>Gehe zu</strong> oder <strong>Neu</strong>. Die Standardeinstellung ist <strong>Nächster</strong>.</span><span class="sxs-lookup"><span data-stu-id="c7e84-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7e84-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="c7e84-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="c7e84-122">Eine ganze Zahl oder ein Ausdruck, der eine ganze Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="c7e84-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="c7e84-123">Ein Ausdruck muss ein Gleichheitszeichen vorangestellt werden (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="c7e84-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="c7e84-124">Dieses Argument gibt den Datensatz zum aktuellen Datensatz machen.</span><span class="sxs-lookup"><span data-stu-id="c7e84-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="c7e84-125">Sie können das Argument <strong>Offset</strong> auf zwei Arten verwenden:</span><span class="sxs-lookup"><span data-stu-id="c7e84-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="c7e84-126">Wenn das Argument <strong>Datensatz</strong> auf <strong>Nächster</strong> oder <strong>Vorheriger</strong> festgelegt ist, verschiebt Microsoft Office Access 2007 den Fokus um die Anzahl von Datensätzen nach vorn oder hinten, die im Argument <strong>Offset</strong> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c7e84-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="c7e84-p105">Wenn das Argument <strong>Datensatz</strong> auf <strong>Gehe zu</strong> festgelegt ist, wechselt Access zu dem Datensatz mit der Nummer, die dem Argument <strong>Offset</strong> entspricht. Die Datensatznummer wird im Datensatznummernfeld am unteren Rand des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7e84-p105">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>

> [!NOTE]
> <span data-ttu-id="c7e84-p106">Wenn Sie für das Argument **Datensatz** die Einstellung **Erster**, **Letzter** oder **Neu** verwenden, ignoriert Access das Argument **Offset**. Wenn Sie einen Wert für **Offset** eingeben, der zu groß ist, zeigt Access eine Fehlermeldung an. Sie können keine negative Zahlen für das Argument **Offset** eingeben.</span><span class="sxs-lookup"><span data-stu-id="c7e84-p106">If you use the **First**, **Last**, or **New** setting for the **Record** argument, Access ignores the **Offset** argument. If you enter an **Offset** argument that is too large, Access displays an error message. You can't enter negative numbers for the **Offset** argument.</span></span>


<p></p>
<ul>
<li><p><span data-ttu-id="c7e84-132">Wenn das Argument <strong>Datensatz</strong> auf <strong>Nächster</strong> oder <strong>Vorheriger</strong> festgelegt ist, verschiebt Microsoft Office Access 2007 den Fokus um die Anzahl von Datensätzen nach vorn oder hinten, die im Argument <strong>Offset</strong> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c7e84-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="c7e84-p107">Wenn das Argument <strong>Datensatz</strong> auf <strong>Gehe zu</strong> festgelegt ist, wechselt Access zu dem Datensatz mit der Nummer, die dem Argument <strong>Offset</strong> entspricht. Die Datensatznummer wird im Datensatznummernfeld am unteren Rand des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7e84-p107">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c7e84-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7e84-135">Remarks</span></span>

<span data-ttu-id="c7e84-136">Wenn sich der Fokus in einem bestimmten Steuerelement in einem Datensatz befindet, belässt diese Aktion den Fokus im selben Steuerelement für den neuen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="c7e84-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="c7e84-137">Sie können die Einstellung **Neu** für das Argument **Datensatz** verwenden, um sich zum leeren Datensatz am Ende eines Formulars oder einer Tabelle zu bewegen, sodass Sie neue Daten eingeben können.</span><span class="sxs-lookup"><span data-stu-id="c7e84-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="c7e84-p108">Diese Aktion ist mit dem Klicken auf den Pfeil unterhalb der Schaltfläche **Suchen** auf der Registerkarte **Start** und dem anschließenden Klicken auf **Gehe zu** vergleichbar. Die Unterbefehle **Erster**, **Letzter**, **Nächster**, **Vorheriger** und **Neuer Datensatz** des Befehls **Gehe zu** haben dieselbe Wirkung auf das ausgewählte Objekt wie die Einstellungen **Erster**, **Letzter**, **Nächster**, **Vorheriger** und **Neu** für das Argument **Datensatz**. Sie können auch zu Datensätzen wechseln, indem Sie die Navigationsschaltflächen am unteren Rand des Fensters verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7e84-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="c7e84-141">Sie können die **GeheZuDatensatz** -Aktion verwenden, um einen Datensatz in einem ausgeblendeten Formular zum aktuellen Datensatz zu machen, indem Sie das ausgeblendete Formular in den Argumenten **Objekttyp** und **Objektname** angeben.</span><span class="sxs-lookup"><span data-stu-id="c7e84-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="c7e84-142">Verwenden Sie die **GoToRecord** -Methode des **DoCmd** -Objekts, um die **GeheZuDatensatz** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c7e84-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

