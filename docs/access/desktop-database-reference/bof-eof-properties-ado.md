---
title: BOF- und EOF-Eigenschaft (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b71e48f3fe0b596f085f02d371b0775695ffd5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874244"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="4802c-102">BOF- und EOF-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4802c-102">BOF, EOF properties (ADO)</span></span>


<span data-ttu-id="4802c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4802c-103">**Applies to**: Access 2013, Office 2013</span></span>

  - <span data-ttu-id="4802c-104">**BOF** - Gibt an, dass die aktuelle Datensatzposition vor dem ersten Datensatz in einem [Recordset](recordset-object-ado.md)-Objekt liegt.</span><span class="sxs-lookup"><span data-stu-id="4802c-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="4802c-105">**EOF** - Gibt an, dass die aktuelle Datensatzposition nach dem letzten Datensatz in einem **Recordset** -Objekt liegt.</span><span class="sxs-lookup"><span data-stu-id="4802c-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="4802c-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4802c-106">Return value</span></span>

<span data-ttu-id="4802c-107">Die **BOF** - und die **EOF** -Eigenschaft geben Werte vom Datentyp **Boolean** zurück.</span><span class="sxs-lookup"><span data-stu-id="4802c-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4802c-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4802c-108">Remarks</span></span>

<span data-ttu-id="4802c-109">Bestimmen Sie mithilfe der Eigenschaften **BOF** und **EOF**, ob ein **Recordset** -Objekt Datensätze enthält oder ob Sie beim Navigieren in den Datensätzen die Grenzen eines **Recordset** -Objekts überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="4802c-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="4802c-110">Die **BOF** -Eigenschaft gibt **True** (-1) zurück, falls sich die aktuelle Datensatzposition vor dem ersten Datensatz befindet, und **False** (0), falls sich die aktuelle Datensatzposition im oder nach dem ersten Datensatz befindet.</span><span class="sxs-lookup"><span data-stu-id="4802c-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="4802c-111">Die **EOF** -Eigenschaft gibt **True** zurück, falls sich die aktuelle Datensatzposition nach dem letzten Datensatz befindet, und **False**, falls sich die aktuelle Datensatzposition im oder vor dem letzten Datensatz befindet.</span><span class="sxs-lookup"><span data-stu-id="4802c-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="4802c-112">Wenn die **BOF** - oder die **EOF** -Eigenschaft **True** ist, gibt es keinen aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="4802c-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="4802c-p101">Wenn Sie ein **Recordset**-Objekt öffnen, das keine Datensätze enthält, werden die Eigenschaften **BOF** und **EOF** auf **True** festgelegt (weitere Informationen zu diesem Status eines **Recordset**-Objekts finden Sie unter der [RecordCount](recordcount-property-ado.md)-Eigenschaft). Wenn Sie ein **Recordset**-Objekt öffnen, das mindestens einen Datensatz enthält, ist der erste Datensatz der aktuelle Datensatz, und die Eigenschaften **BOF** und **EOF** sind **False**.</span><span class="sxs-lookup"><span data-stu-id="4802c-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="4802c-115">Wenn Sie den letzten verbleibenden Datensatz im **Recordset** -Objekt löschen, bleiben die Eigenschaften **BOF** und **EOF** so lange **False**, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="4802c-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="4802c-116">In dieser Tabelle ist dargestellt, welche **Move** -Methoden für verschiedene Kombinationen der Eigenschaften **BOF** und **EOF** zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4802c-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="4802c-117">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="4802c-117">MoveFirst,</span></span><br />
<span data-ttu-id="4802c-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="4802c-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="4802c-119">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="4802c-119">MovePrevious,</span></span><br />
<span data-ttu-id="4802c-120">Verschieben von &lt; 0</span><span class="sxs-lookup"><span data-stu-id="4802c-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="4802c-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="4802c-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="4802c-122">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="4802c-122">MoveNext,</span></span><br />
<span data-ttu-id="4802c-123">Verschieben von &gt; 0</span><span class="sxs-lookup"><span data-stu-id="4802c-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4802c-124"><strong>BOF = "true"</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="4802c-125">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="4802c-126">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="4802c-127">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-127">Error</span></span></p></td>
<td><p><span data-ttu-id="4802c-128">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-128">Error</span></span></p></td>
<td><p><span data-ttu-id="4802c-129">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4802c-130"><strong>BOF = "false"</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="4802c-131">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="4802c-132">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="4802c-133">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="4802c-134">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-134">Error</span></span></p></td>
<td><p><span data-ttu-id="4802c-135">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4802c-136">Beide <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="4802c-137">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-137">Error</span></span></p></td>
<td><p><span data-ttu-id="4802c-138">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-138">Error</span></span></p></td>
<td><p><span data-ttu-id="4802c-139">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-139">Error</span></span></p></td>
<td><p><span data-ttu-id="4802c-140">Fehler</span><span class="sxs-lookup"><span data-stu-id="4802c-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4802c-141">Beide <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="4802c-142">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="4802c-143">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="4802c-144">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="4802c-145">Zulässig</span><span class="sxs-lookup"><span data-stu-id="4802c-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4802c-146">Das Zulassen einer **Move** -Methode garantiert nicht, dass die Methode einen Datensatz erfolgreich findet. Es bedeutet nur, dass beim Aufrufen der angegebenen **Move** -Methode kein Fehler generiert wird.</span><span class="sxs-lookup"><span data-stu-id="4802c-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="4802c-147">Die folgende Tabelle zeigt, was mit den Einstellungen der Eigenschaften **BOF** und **EOF** passiert, wenn Sie verschiedene **Move** -Methoden aufrufen, einen Datensatz aber nicht finden können.</span><span class="sxs-lookup"><span data-stu-id="4802c-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="4802c-148">BOF</span><span class="sxs-lookup"><span data-stu-id="4802c-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="4802c-149">EOF</span><span class="sxs-lookup"><span data-stu-id="4802c-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4802c-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="4802c-151">Auf <strong>True</strong> festgelegt</span><span class="sxs-lookup"><span data-stu-id="4802c-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="4802c-152">Auf <strong>True</strong> festgelegt</span><span class="sxs-lookup"><span data-stu-id="4802c-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4802c-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="4802c-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="4802c-154">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="4802c-154">No change</span></span></p></td>
<td><p><span data-ttu-id="4802c-155">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="4802c-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4802c-156"><strong>MovePrevious</strong>, <strong>Verschieben Sie</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="4802c-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="4802c-157">Festgelegt auf <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="4802c-158">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="4802c-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4802c-159"><strong>MoveNext</strong>, <strong>Verschieben Sie</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="4802c-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="4802c-160">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="4802c-160">No change</span></span></p></td>
<td><p><span data-ttu-id="4802c-161">Festgelegt auf <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="4802c-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

