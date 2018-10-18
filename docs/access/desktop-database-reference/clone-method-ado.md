---
title: Clone-Methode - ActiveX Data Objects (ADO)
TOCTitle: Clone Method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a93fb7fd333156c6939311c0e247f4b5f8aec16
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607039"
---
# <a name="clone-method-ado"></a><span data-ttu-id="0d3a1-102">Clone-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d3a1-102">Clone Method (ADO)</span></span>


<span data-ttu-id="0d3a1-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d3a1-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="0d3a1-p101">Ein [Recordset](recordset-object-ado.md)-Objektduplikat wird aus einem vorhandenen **Recordset** -Objekt erstellt. Optional wird angegeben, dass der Klon schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3a1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d3a1-106">Syntax</span></span>

<span data-ttu-id="0d3a1-107">**Festlegen** *rstDuplicate*  =  *RstOriginal*. Wenn Sie den Klon (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="0d3a1-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

<span data-ttu-id="0d3a1-108"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="0d3a1-108"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="0d3a1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d3a1-109">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="0d3a1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d3a1-110">Return value</span></span>
>>>>>>> <span data-ttu-id="0d3a1-111">master</span><span class="sxs-lookup"><span data-stu-id="0d3a1-111">master</span></span>

<span data-ttu-id="0d3a1-112">Ein **Recordset** -Objektverweis wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-112">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d3a1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d3a1-113">Parameters</span></span>

  - <span data-ttu-id="0d3a1-114">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="0d3a1-114">*rstDuplicate*</span></span>

  - <span data-ttu-id="0d3a1-115">Eine Objektvariable, durch die das zu erstellende **Recordset** -Objektduplikat identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-115">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

  - <span data-ttu-id="0d3a1-116">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="0d3a1-116">*rstOriginal*</span></span>

  - <span data-ttu-id="0d3a1-117">Eine Objektvariable, durch die das zu duplizierende **Recordset** -Objekt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-117">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

  - <span data-ttu-id="0d3a1-118">*LockType*</span><span class="sxs-lookup"><span data-stu-id="0d3a1-118">*LockType*</span></span>

  - <span data-ttu-id="0d3a1-p102">Optional. Ein [LockTypeEnum](locktypeenum.md)-Wert, durch den der Sperrtyp des Original **recordsets** oder ein schreibgeschütztes **Recordset** angegeben wird. Gültige Werte sind **adLockUnspecified** oder **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d3a1-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d3a1-122">Remarks</span></span>

<span data-ttu-id="0d3a1-p103">Verwenden Sie die **Clone** -Methode zum Erstellen mehrerer **Recordset** -Objektduplikate, insbesondere, wenn Sie mehrere aktuelle Datensätze in einem bestimmten Satz mit Datensätzen aufrechterhalten möchten. Das Verwenden der **Clone** -Methode ist effizienter als das Erstellen und Öffnen eines neuen **Recordset** -Objekts mit der gleichen Definition wie das Original.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="0d3a1-p104">Die [Filter](filter-property-ado.md)-Eigenschaft des Original **recordsets**, falls vorhanden, wird nicht auf den Klon angewendet. Legen Sie die **Filter** -Eigenschaft des neuen **Recordsets** fest, um die Ergebnisse zu filtern. Die einfachste Möglichkeit zum Kopieren vorhandener **Filter** -Werte ist das direkte Zuweisen:</span><span class="sxs-lookup"><span data-stu-id="0d3a1-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="0d3a1-128">Der aktuelle Datensatz eines neu erstellten Klons wird auf den ersten Datensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-128">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="0d3a1-p105">An einem **Recordset** -Objekt vorgenommene Änderungen werden unabhängig vom Cursortyp in allen Klonen des Objekts angezeigt. Nach dem Ausführen von [Requery](requery-method-ado.md) für das ursprüngliche **Recordset** -Objekt werden die Klone jedoch nicht mehr mit dem Original synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="0d3a1-131">Durch das Schließen des Original **recordsets** werden die Kopien nicht geschlossen, und durch das Schließen einer Kopie werden das Original oder andere Kopien nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-131">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="0d3a1-p106">Sie können nur **Recordset** -Objekte klonen, von denen Textmarken unterstützt werden. Textmarkenwerte sind austauschbar; d. h., ein Textmarkenverweis eines **Recordset** -Objekts verweist auf den gleichen Datensatz in den Klonen.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="0d3a1-p107">Einige ausgelöste **Recordset** -Ereignisse werden auch in allen **Recordset** klonen ausgeführt. Die Ereignisse sind für den Klon jedoch möglicherweise nicht gültig, da sich der aktuelle Datensatz zwischen geklonten **Recordsets** unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="0d3a1-136">Beispielsweise, wenn Sie einen Wert eines Felds zu ändern, wird ein Ereignis [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) im geänderten **Recordset-Objekt** und in allen Klonen auftreten.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-136">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="0d3a1-137">Der Parameter *Felder* des Ereignisses **WillChangeField** eines geklonte **Recordset-Objekt** (, in dem die Änderung nicht vorgenommen wurde) wird einfach finden Sie in die Felder des aktuellen Datensatzes des Klons, die möglicherweise von einem anderen Datensatz als der aktuelle Datensatz zu der ursprüngliche **Recordset-Objekt** , das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-137">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="0d3a1-138">In der folgenden Tabelle wird eine vollständige Liste aller **Recordset** -Ereignisse bereitgestellt, und es wird angegeben, ob sie gültig sind und für mit der **Clone** -Methode generierte Recordsetklone ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0d3a1-138">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d3a1-139">Ereignis</span><span class="sxs-lookup"><span data-stu-id="0d3a1-139">Event</span></span></p></th>
<th><p><span data-ttu-id="0d3a1-140">Auslösung in Klonen</span><span class="sxs-lookup"><span data-stu-id="0d3a1-140">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d3a1-141"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-141"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-142">Nein</span><span class="sxs-lookup"><span data-stu-id="0d3a1-142">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d3a1-143"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-143"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-144">Nein</span><span class="sxs-lookup"><span data-stu-id="0d3a1-144">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d3a1-145"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-145"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-146">Nein</span><span class="sxs-lookup"><span data-stu-id="0d3a1-146">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d3a1-147"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-147"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-148">Ja</span><span class="sxs-lookup"><span data-stu-id="0d3a1-148">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d3a1-149"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-149"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-150">Nein</span><span class="sxs-lookup"><span data-stu-id="0d3a1-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d3a1-151"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-151"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-152">Ja</span><span class="sxs-lookup"><span data-stu-id="0d3a1-152">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d3a1-153"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-153"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-154">Nein</span><span class="sxs-lookup"><span data-stu-id="0d3a1-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d3a1-155"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-155"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-156">Ja</span><span class="sxs-lookup"><span data-stu-id="0d3a1-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d3a1-157"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-157"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-158">Ja</span><span class="sxs-lookup"><span data-stu-id="0d3a1-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d3a1-159"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-159"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-160">Nein</span><span class="sxs-lookup"><span data-stu-id="0d3a1-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d3a1-161"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="0d3a1-161"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="0d3a1-162">Nein</span><span class="sxs-lookup"><span data-stu-id="0d3a1-162">No</span></span></p></td>
</tr>
</tbody>
</table>

