---
<span data-ttu-id="f2055-101"><<<<<<< HEAD-Titel: BOF- und EOF-Eigenschaften (ADO) TOCTitle: BOF- und EOF-Eigenschaften (ADO) === Titel: BOF-und EOF-Eigenschaft (ADO) TOCTitle: BOF-und EOF-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2055-101"><<<<<<< HEAD title: BOF, EOF Properties (ADO) TOCTitle: BOF, EOF Properties (ADO) ======= title: BOF, EOF properties (ADO) TOCTitle: BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2055-102">Master Ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) Ms:contentKeyID: 48548768 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="f2055-102">master ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f2055-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="f2055-103"><<<<<<< HEAD</span></span>
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="f2055-104">BOF- und EOF-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2055-104">BOF, EOF Properties (ADO)</span></span>
=======
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="f2055-105">BOF-und EOF-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2055-105">BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2055-106">master</span><span class="sxs-lookup"><span data-stu-id="f2055-106">master</span></span>


<span data-ttu-id="f2055-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2055-107">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="f2055-108">**BOF** - Gibt an, dass die aktuelle Datensatzposition vor dem ersten Datensatz in einem [Recordset](recordset-object-ado.md)-Objekt liegt.</span><span class="sxs-lookup"><span data-stu-id="f2055-108">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="f2055-109">**EOF** - Gibt an, dass die aktuelle Datensatzposition nach dem letzten Datensatz in einem **Recordset** -Objekt liegt.</span><span class="sxs-lookup"><span data-stu-id="f2055-109">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

<span data-ttu-id="f2055-110"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="f2055-110"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f2055-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2055-111">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f2055-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2055-112">Return value</span></span>
>>>>>>> <span data-ttu-id="f2055-113">master</span><span class="sxs-lookup"><span data-stu-id="f2055-113">master</span></span>

<span data-ttu-id="f2055-114">Die **BOF** - und die **EOF** -Eigenschaft geben Werte vom Datentyp **Boolean** zurück.</span><span class="sxs-lookup"><span data-stu-id="f2055-114">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2055-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2055-115">Remarks</span></span>

<span data-ttu-id="f2055-116">Bestimmen Sie mithilfe der Eigenschaften **BOF** und **EOF**, ob ein **Recordset** -Objekt Datensätze enthält oder ob Sie beim Navigieren in den Datensätzen die Grenzen eines **Recordset** -Objekts überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="f2055-116">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="f2055-117">Die **BOF** -Eigenschaft gibt **True** (-1) zurück, falls sich die aktuelle Datensatzposition vor dem ersten Datensatz befindet, und **False** (0), falls sich die aktuelle Datensatzposition im oder nach dem ersten Datensatz befindet.</span><span class="sxs-lookup"><span data-stu-id="f2055-117">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="f2055-118">Die **EOF** -Eigenschaft gibt **True** zurück, falls sich die aktuelle Datensatzposition nach dem letzten Datensatz befindet, und **False**, falls sich die aktuelle Datensatzposition im oder vor dem letzten Datensatz befindet.</span><span class="sxs-lookup"><span data-stu-id="f2055-118">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="f2055-119">Wenn die **BOF** - oder die **EOF** -Eigenschaft **True** ist, gibt es keinen aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="f2055-119">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="f2055-p101">Wenn Sie ein **Recordset**-Objekt öffnen, das keine Datensätze enthält, werden die Eigenschaften **BOF** und **EOF** auf **True** festgelegt (weitere Informationen zu diesem Status eines **Recordset**-Objekts finden Sie unter der [RecordCount](recordcount-property-ado.md)-Eigenschaft). Wenn Sie ein **Recordset**-Objekt öffnen, das mindestens einen Datensatz enthält, ist der erste Datensatz der aktuelle Datensatz, und die Eigenschaften **BOF** und **EOF** sind **False**.</span><span class="sxs-lookup"><span data-stu-id="f2055-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="f2055-122">Wenn Sie den letzten verbleibenden Datensatz im **Recordset** -Objekt löschen, bleiben die Eigenschaften **BOF** und **EOF** so lange **False**, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="f2055-122">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="f2055-123">In dieser Tabelle ist dargestellt, welche **Move** -Methoden für verschiedene Kombinationen der Eigenschaften **BOF** und **EOF** zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f2055-123">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="f2055-124">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="f2055-124">MoveFirst,</span></span><br />
<span data-ttu-id="f2055-125">MoveLast</span><span class="sxs-lookup"><span data-stu-id="f2055-125">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="f2055-126">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="f2055-126">MovePrevious,</span></span><br />
<span data-ttu-id="f2055-127">Verschieben von &lt; 0</span><span class="sxs-lookup"><span data-stu-id="f2055-127">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="f2055-128">Move 0</span><span class="sxs-lookup"><span data-stu-id="f2055-128">Move 0</span></span></p></th>
<th><p><span data-ttu-id="f2055-129">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="f2055-129">MoveNext,</span></span><br />
<span data-ttu-id="f2055-130">Verschieben von &gt; 0</span><span class="sxs-lookup"><span data-stu-id="f2055-130">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2055-131"><strong>BOF = "true"</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-131"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="f2055-132">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-132">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="f2055-133">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f2055-134">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-134">Error</span></span></p></td>
<td><p><span data-ttu-id="f2055-135">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-135">Error</span></span></p></td>
<td><p><span data-ttu-id="f2055-136">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-136">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2055-137"><strong>BOF = "false"</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-137"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="f2055-138">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-138">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="f2055-139">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-139">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f2055-140">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-140">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f2055-141">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-141">Error</span></span></p></td>
<td><p><span data-ttu-id="f2055-142">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-142">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2055-143">Beide <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-143">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="f2055-144">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-144">Error</span></span></p></td>
<td><p><span data-ttu-id="f2055-145">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-145">Error</span></span></p></td>
<td><p><span data-ttu-id="f2055-146">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-146">Error</span></span></p></td>
<td><p><span data-ttu-id="f2055-147">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2055-147">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2055-148">Beide <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-148">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="f2055-149">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f2055-150">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-150">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f2055-151">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-151">Allowed</span></span></p></td>
<td><p><span data-ttu-id="f2055-152">Zulässig</span><span class="sxs-lookup"><span data-stu-id="f2055-152">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2055-153">Das Zulassen einer **Move** -Methode garantiert nicht, dass die Methode einen Datensatz erfolgreich findet. Es bedeutet nur, dass beim Aufrufen der angegebenen **Move** -Methode kein Fehler generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2055-153">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="f2055-154">Die folgende Tabelle zeigt, was mit den Einstellungen der Eigenschaften **BOF** und **EOF** passiert, wenn Sie verschiedene **Move** -Methoden aufrufen, einen Datensatz aber nicht finden können.</span><span class="sxs-lookup"><span data-stu-id="f2055-154">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="f2055-155">BOF</span><span class="sxs-lookup"><span data-stu-id="f2055-155">BOF</span></span></p></th>
<th><p><span data-ttu-id="f2055-156">EOF</span><span class="sxs-lookup"><span data-stu-id="f2055-156">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2055-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="f2055-158">Auf <strong>True</strong> festgelegt</span><span class="sxs-lookup"><span data-stu-id="f2055-158">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="f2055-159">Auf <strong>True</strong> festgelegt</span><span class="sxs-lookup"><span data-stu-id="f2055-159">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2055-160"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="f2055-160"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="f2055-161">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="f2055-161">No change</span></span></p></td>
<td><p><span data-ttu-id="f2055-162">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="f2055-162">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2055-163"><strong>MovePrevious</strong>, <strong>Verschieben Sie</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="f2055-163"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="f2055-164">Festgelegt auf <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-164">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="f2055-165">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="f2055-165">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2055-166"><strong>MoveNext</strong>, <strong>Verschieben Sie</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="f2055-166"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="f2055-167">Keine Änderung</span><span class="sxs-lookup"><span data-stu-id="f2055-167">No change</span></span></p></td>
<td><p><span data-ttu-id="f2055-168">Festgelegt auf <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="f2055-168">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

