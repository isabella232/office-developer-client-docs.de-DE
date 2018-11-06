---
title: Requery-Makroaktion
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e59a1f5ce676ceaa1b0b346a38b4487b3233e514
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997378"
---
# <a name="requery-macro-action"></a><span data-ttu-id="23506-102">Requery-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="23506-102">Requery macro action</span></span>

<span data-ttu-id="23506-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23506-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23506-p101">Sie können die **AktualisierenDaten** -Aktion verwenden, um die Daten in einem angegebenen Steuerelement des aktiven Objekts durch erneutes Abfragen der Steuerelementquelle zu aktualisieren. Wenn kein Steuerelement angegeben ist, fragt diese Aktion die Objektquelle selbst erneut ab. Verwenden Sie diese Aktion, um sicherzustellen, dass das aktive Objekt oder eines seiner Steuerelemente die neuesten Daten anzeigt.</span><span class="sxs-lookup"><span data-stu-id="23506-p101">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control. If no control is specified, this action requeries the source of the object itself. Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="23506-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="23506-107">Setting</span></span>

<span data-ttu-id="23506-108">Die **AktualisierenDaten** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="23506-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23506-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="23506-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="23506-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23506-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23506-111"><strong>Steuerelementname</strong></span><span class="sxs-lookup"><span data-stu-id="23506-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="23506-p102">Der Name des Steuerelements, das Sie aktualisieren möchten. Geben Sie den Namen des Steuerelements im Feld Steuerelementname im Abschnitt Aktionsargumente des Bereichs Makro-Generator ein. Sie sollten nur den Namen des Steuerelements, nicht den vollqualifizierten Bezeichner verwenden (wie Formulare!Formularname!Steuerelementname). Lassen Sie dieses Argument leer, um die Quelle des aktiven Objekts zu aktualisieren. Wenn das aktive Objekt ein Datenblatt oder ein Resultset einer Abfrage ist, müssen Sie dieses Argument leer lassen.</span><span class="sxs-lookup"><span data-stu-id="23506-p102">The name of the control you want to update. Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>). Leave this argument blank to requery the source of the active object. If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="23506-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23506-117">Remarks</span></span>

<span data-ttu-id="23506-118">Die **AktualisierenDaten** -Aktion wendet eines der folgenden Verfahren an:</span><span class="sxs-lookup"><span data-stu-id="23506-118">The **Requery** action does one of the following:</span></span>

- <span data-ttu-id="23506-119">Erneutes Ausführen der Abfrage, auf der das Steuerelement oder Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="23506-119">Reruns the query on which the control or object is based.</span></span>

- <span data-ttu-id="23506-120">Anzeigen aller neuen oder geänderten Datensätze und Entfernen aller gelöschten Datensätze aus der Tabelle, auf der das Steuerelement bzw. Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="23506-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>

> [!NOTE]
> <span data-ttu-id="23506-121">[!HINWEIS] Die **AktualisierenDaten** -Aktion wirkt sich nicht auf die Position des Datensatzzeigers aus.</span><span class="sxs-lookup"><span data-stu-id="23506-121">The **Requery** action does not affect the position of the record pointer.</span></span>

<span data-ttu-id="23506-122">Folgende Steuerelemente können auf einer Abfrage oder Tabelle basieren:</span><span class="sxs-lookup"><span data-stu-id="23506-122">Controls based on a query or table include:</span></span>

- <span data-ttu-id="23506-123">Listenfelder und Kombinationsfelder.</span><span class="sxs-lookup"><span data-stu-id="23506-123">List boxes and combo boxes.</span></span>

- <span data-ttu-id="23506-124">Unterformularsteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="23506-124">Subform controls.</span></span>

- <span data-ttu-id="23506-125">OLE-Objekte, z. B. Diagramme.</span><span class="sxs-lookup"><span data-stu-id="23506-125">OLE objects, such as charts.</span></span>

- <span data-ttu-id="23506-126">Steuerelemente, die Domänen-Aggregatfunktionen wie **DBSUMME** enthalten.</span><span class="sxs-lookup"><span data-stu-id="23506-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="23506-127">Wenn das angegebene Steuerelement nicht auf einer Abfrage oder einer Tabelle basiert, erzwingt diese Aktion eine Neuberechnung des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="23506-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="23506-p103">Wenn Sie das Argument **Steuerelementname** leer lassen, hat die **AktualisierenDaten** -Aktion dieselbe Wirkung wie das Drücken von UMSCHALTTASTE+F9, falls das Objekt den Fokus besitzt. Wenn ein Unterformularsteuerelement den Fokus hat, fragt diese Aktion nur die Quelle des Unterformulars erneut ab (wie beim Drücken von UMSCHALTTASTE+F9).</span><span class="sxs-lookup"><span data-stu-id="23506-p103">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>

> [!NOTE]
> <span data-ttu-id="23506-p104">[!HINWEIS] Die **AktualisierenDaten** -Aktion fragt die Herkunft des Steuerelements oder des Objekts erneut ab. Die **AktualisierenObjekt** -Aktion aktualisiert Steuerelemente im angegebenen Objekt, fragt jedoch die Datenbank nicht erneut ab oder zeigt keine neuen Datensätze an. Die **AnzeigenAlleDatensätze** -Aktion fragt nicht nur das aktive Objekt ab, sondern entfernt auch alle angewendeten Filter, was die **AktualisierenDaten** -Aktion nicht vornimmt.</span><span class="sxs-lookup"><span data-stu-id="23506-p104">The **Requery** action requeries the source of the control or object. In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records. The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span></span>

<span data-ttu-id="23506-133">Wenn Sie ein Steuerelement erneut abfragen, die für das aktive Objekt ist nicht möchten, müssen Sie die **Requery** -Methode in einem Visual Basic für Applikationen (VBA) Modul, nicht die **AktualisierenDaten** -Aktion oder die entsprechende **Requery** -Methode des **DoCmd** -Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="23506-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="23506-134">Die **Requery** -Methode in VBA ist schneller als die **AktualisierenDaten** -Aktion oder die **Requery** -Methode.</span><span class="sxs-lookup"><span data-stu-id="23506-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="23506-135">Darüber hinaus wird, wenn Sie die **AktualisierenDaten** -Aktion oder die **Requery** -Methode verwenden, schließt Microsoft Access die Abfrage und lädt ihn erneut aus der Datenbank, aber bei Verwendung die **Requery** -Methode führt Access ohne Schließen und neu zu laden.</span><span class="sxs-lookup"><span data-stu-id="23506-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="23506-136">Beachten Sie, dass das ActiveX-Objekt (ADO) **Requery** -Methode die gleiche Weise wie die Access **Requery** -Methode funktioniert.</span><span class="sxs-lookup"><span data-stu-id="23506-136">Note that the ActiveX Data object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

