---
title: Recordset2.EOF Property (DAO)
TOCTitle: EOF Property
ms:assetid: 9d4e1ee2-e866-3ebf-e08b-b31b0cb47ed9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198245(v=office.15)
ms:contentKeyID: 48546622
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052886
f1_categories:
- Office.Version=v15
ms.openlocfilehash: abb99f58b151c9bafe554486f8b6f1308322560f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474569"
---
# <a name="recordset2eof-property-dao"></a><span data-ttu-id="ec6a0-102">Recordset2.EOF Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="ec6a0-102">Recordset2.EOF Property (DAO)</span></span>


<span data-ttu-id="ec6a0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec6a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ec6a0-p101">Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition hinter dem letzten Datensatz in einem **Recordset**-Objekt liegt. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-p101">Returns a value that indicates whether the current record position is after the last record in a **Recordset** object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec6a0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec6a0-106">Syntax</span></span>

<span data-ttu-id="ec6a0-107">*Ausdruck* . EOF</span><span class="sxs-lookup"><span data-stu-id="ec6a0-107">*expression* .EOF</span></span>

<span data-ttu-id="ec6a0-108">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec6a0-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec6a0-109">Remarks</span></span>

<span data-ttu-id="ec6a0-110">Mit den Eigenschaften **BOF** und **EOF** können Sie feststellen, ob ein **Recordset**-Objekt Datensätze enthält oder ob Sie beim Wechsel zwischen Datensätzen über die Grenzen eines **Recordset**-Objekts navigiert sind.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="ec6a0-111">Die Position des aktuellen Datensatzzeigers legt die Rückgabewerte von **BOF** und **EOF** fest.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="ec6a0-112">Wenn die **BOF**- oder die **EOF**-Eigenschaft **True** ist, gibt es keinen aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="ec6a0-p102">Wenn Sie ein **Recordset**-Objekt öffnen, das keine Datensätze enthält, erhalten die Eigenschaften **BOF** und **EOF** den Wert **True** und der Wert der **RecordCount**-Eigenschaft des **Recordset**-Objekts wird auf 0 festgelegt. Wenn Sie ein **Recordset**-Objekt öffnen, das mindestens einen Datensatz enthält, ist der erste Datensatz der aktuelle Datensatz, und die Eigenschaften **BOF** und **EOF** haben den Wert **False**. Die Einstellung **False** wird beibehalten, bis Sie vor den Anfang oder hinter das Ende des **Recordset**-Objekts navigieren oder die **MovePrevious**- oder **MoveNext**-Methode verwenden. Wenn Sie vor den Anfang oder hinter das Ende des **Recordset**-Objekts navigieren, gibt es keinen aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-p102">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0. When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively. When you move beyond the beginning or end of the **Recordset**, there is no current record or no record exists.</span></span>

<span data-ttu-id="ec6a0-116">Wenn Sie den letzten verbleibenden Datensatz im **Recordset**-Objekt löschen, bleiben die Eigenschaften **BOF** und **EOF** so lange **False**, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="ec6a0-p103">Wenn Sie die **MoveLast**-Methode auf ein **Recordset**-Objekt anwenden, das Datensätze enthält, wird der letzte Datensatz zum aktuellen Datensatz. Wenn Sie dann die **MoveNext**-Methode verwenden, wird der aktuelle Datensatz ungültig und die **EOF**-Eigenschaft wird auf **True** festgelegt. Wenn Sie dagegen die **MoveFirst**-Methode auf ein **Recordset**-Objekt anwenden, das Datensätze enthält, wird der erste Datensatz zum aktuellen Datensatz. Wenn Sie dann die **MovePrevious**-Methode verwenden, gibt es keinen aktuellen Datensatz, und die **BOF**-Eigenschaft erhält den Wert **True**.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-p103">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**. Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="ec6a0-119">Wenn Sie alle Datensätze in einem **Recordset**-Objekt verwenden, durchsucht Ihr Code gewöhnlich unter Verwendung der **MoveNext**-Methode die Datensätze, bis die **EOF**-Eigenschaft den Wert **True** hat.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="ec6a0-120">Wenn Sie die **MoveNext**-Methode verwenden, während die **EOF**-Eigenschaft den Wert **True** hat, oder wenn Sie die **MovePrevious**-Methode verwenden, während die **BOF**-Eigenschaft den Wert **True** hat, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="ec6a0-121">In dieser Tabelle ist dargestellt, welche Move-Methoden für verschiedene Kombinationen der Eigenschaften **BOF** und **EOF** zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="ec6a0-122">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="ec6a0-122">MoveFirst,</span></span><br />
<span data-ttu-id="ec6a0-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="ec6a0-123">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="ec6a0-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="ec6a0-124">MovePrevious,</span></span><br />
<span data-ttu-id="ec6a0-125">Verschieben von &lt; 0</span><span class="sxs-lookup"><span data-stu-id="ec6a0-125">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="ec6a0-126">Move 0</span><span class="sxs-lookup"><span data-stu-id="ec6a0-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="ec6a0-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="ec6a0-127">MoveNext,</span></span><br />
<span data-ttu-id="ec6a0-128">Verschieben von &gt; 0</span><span class="sxs-lookup"><span data-stu-id="ec6a0-128">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec6a0-129"><strong>BOF = "true"</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-129"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="ec6a0-130">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-130">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="ec6a0-131">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-132">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-132">Error</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-133">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-133">Error</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-134">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec6a0-135"><strong>BOF = "false"</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-135"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="ec6a0-136">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-136">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="ec6a0-137">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-138">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-139">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-139">Error</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-140">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec6a0-141">Beide <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="ec6a0-142">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-142">Error</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-143">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-143">Error</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-144">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-144">Error</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-145">Fehler</span><span class="sxs-lookup"><span data-stu-id="ec6a0-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec6a0-146">Beide <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="ec6a0-147">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-148">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-149">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-150">Zulässig</span><span class="sxs-lookup"><span data-stu-id="ec6a0-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec6a0-p104">Wenn eine Move-Methode zulässig ist, heißt das nicht, dass die Methode einen Datensatz findet. Es bedeutet nur, dass die Ausführung der betreffenden Move-Methode gestattet ist und keinen Fehler generiert. Der Status der Eigenschaften **BOF** und **EOF** kann sich durch die versuchte Ausführung der Move-Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-p104">Allowing a Move method doesn't mean that the method will successfully locate a record. It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error. The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="ec6a0-p105">Eine **OpenRecordset**-Methode ruft intern eine **MoveFirst**-Methode auf. Wenn Sie daher eine **OpenRecordset**-Methode auf eine leere Gruppe von Datensätzen anwenden, werden die Eigenschaften **BOF** und **EOF** auf **True** gesetzt. (In der folgenden Tabelle ist das Verhalten einer fehlgeschlagenen **MoveFirst**-Methode aufgeführt.)</span><span class="sxs-lookup"><span data-stu-id="ec6a0-p105">An **OpenRecordset** method internally invokes a **MoveFirst** method. Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**. (See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="ec6a0-157">Alle Move-Methoden, die einen Datensatz erfolgreich finden, legen für die Eigenschaften **BOF** und **EOF** den Wert **False** fest.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="ec6a0-158">Wenn Sie in einem Microsoft Access-Arbeitsbereich einem leeren **Recordset**-Objekt einen Datensatz hinzufügen, wird die **BOF**-Eigenschaft auf **False** festgelegt, **EOF** bleibt jedoch **True** und gibt dadurch an, dass sich die aktuelle Position am Ende des **Recordset**-Objekts befindet.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-158">In a Microsoft Access workspace, if you add a record to an empty **Recordset**, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of **Recordset**.</span></span>

<span data-ttu-id="ec6a0-159">**Delete**-Methoden ändern in keinem Fall die Einstellung der Eigenschaften **BOF** und **EOF**, selbst wenn durch die Methode der letzte Datensatz aus einem **Recordset**-Objekt entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-159">Any **Delete** method, even if it removes the only remaining record from a **Recordset**, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="ec6a0-160">Die folgende Tabelle zeigt, welche Auswirkungen Move-Methoden, bei denen ein Datensatz nicht gefunden wird, auf die Einstellungen der Eigenschaften **BOF** und **EOF** haben.</span><span class="sxs-lookup"><span data-stu-id="ec6a0-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="ec6a0-161">BOF</span><span class="sxs-lookup"><span data-stu-id="ec6a0-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="ec6a0-162">EOF</span><span class="sxs-lookup"><span data-stu-id="ec6a0-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec6a0-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="ec6a0-164"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="ec6a0-165"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec6a0-166"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="ec6a0-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-167">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="ec6a0-167">No change</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-168">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="ec6a0-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec6a0-169"><strong>MovePrevious</strong>, <strong>Verschieben Sie</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="ec6a0-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-170"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="ec6a0-171">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="ec6a0-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec6a0-172"><strong>MoveNext</strong>, <strong>Verschieben Sie</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="ec6a0-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-173">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="ec6a0-173">No change</span></span></p></td>
<td><p><span data-ttu-id="ec6a0-174"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ec6a0-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

