---
title: Clone-Methode - ActiveX Data Objects (ADO)
TOCTitle: Clone Method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5cbf11605c13094d0595b44d804deb2169a9e9b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475431"
---
# <a name="clone-method-ado"></a><span data-ttu-id="e074e-102">Clone-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="e074e-102">Clone Method (ADO)</span></span>


<span data-ttu-id="e074e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e074e-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="e074e-p101">Ein [Recordset](recordset-object-ado.md)-Objektduplikat wird aus einem vorhandenen **Recordset** -Objekt erstellt. Optional wird angegeben, dass der Klon schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="e074e-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e074e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e074e-106">Syntax</span></span>

<span data-ttu-id="e074e-107">**Festlegen** *rstDuplicate*  =  *RstOriginal*. Wenn Sie den Klon (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="e074e-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="e074e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e074e-108">Return Value</span></span>

<span data-ttu-id="e074e-109">Ein **Recordset** -Objektverweis wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e074e-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="e074e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e074e-110">Parameters</span></span>

  - <span data-ttu-id="e074e-111">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="e074e-111">*rstDuplicate*</span></span>

  - <span data-ttu-id="e074e-112">Eine Objektvariable, durch die das zu erstellende **Recordset** -Objektduplikat identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e074e-112">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

  - <span data-ttu-id="e074e-113">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="e074e-113">*rstOriginal*</span></span>

  - <span data-ttu-id="e074e-114">Eine Objektvariable, durch die das zu duplizierende **Recordset** -Objekt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e074e-114">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

  - <span data-ttu-id="e074e-115">*LockType*</span><span class="sxs-lookup"><span data-stu-id="e074e-115">*LockType*</span></span>

  - <span data-ttu-id="e074e-p102">Optional. Ein [LockTypeEnum](locktypeenum.md)-Wert, durch den der Sperrtyp des Original **recordsets** oder ein schreibgeschütztes **Recordset** angegeben wird. Gültige Werte sind **adLockUnspecified** oder **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="e074e-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e074e-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e074e-119">Remarks</span></span>

<span data-ttu-id="e074e-p103">Verwenden Sie die **Clone** -Methode zum Erstellen mehrerer **Recordset** -Objektduplikate, insbesondere, wenn Sie mehrere aktuelle Datensätze in einem bestimmten Satz mit Datensätzen aufrechterhalten möchten. Das Verwenden der **Clone** -Methode ist effizienter als das Erstellen und Öffnen eines neuen **Recordset** -Objekts mit der gleichen Definition wie das Original.</span><span class="sxs-lookup"><span data-stu-id="e074e-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="e074e-p104">Die [Filter](filter-property-ado.md)-Eigenschaft des Original **recordsets**, falls vorhanden, wird nicht auf den Klon angewendet. Legen Sie die **Filter** -Eigenschaft des neuen **Recordsets** fest, um die Ergebnisse zu filtern. Die einfachste Möglichkeit zum Kopieren vorhandener **Filter** -Werte ist das direkte Zuweisen:</span><span class="sxs-lookup"><span data-stu-id="e074e-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="e074e-125">Der aktuelle Datensatz eines neu erstellten Klons wird auf den ersten Datensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e074e-125">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="e074e-p105">An einem **Recordset** -Objekt vorgenommene Änderungen werden unabhängig vom Cursortyp in allen Klonen des Objekts angezeigt. Nach dem Ausführen von [Requery](requery-method-ado.md) für das ursprüngliche **Recordset** -Objekt werden die Klone jedoch nicht mehr mit dem Original synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e074e-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="e074e-128">Durch das Schließen des Original **recordsets** werden die Kopien nicht geschlossen, und durch das Schließen einer Kopie werden das Original oder andere Kopien nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e074e-128">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="e074e-p106">Sie können nur **Recordset** -Objekte klonen, von denen Textmarken unterstützt werden. Textmarkenwerte sind austauschbar; d. h., ein Textmarkenverweis eines **Recordset** -Objekts verweist auf den gleichen Datensatz in den Klonen.</span><span class="sxs-lookup"><span data-stu-id="e074e-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="e074e-p107">Einige ausgelöste **Recordset** -Ereignisse werden auch in allen **Recordset** klonen ausgeführt. Die Ereignisse sind für den Klon jedoch möglicherweise nicht gültig, da sich der aktuelle Datensatz zwischen geklonten **Recordsets** unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="e074e-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="e074e-133">Beispielsweise, wenn Sie einen Wert eines Felds zu ändern, wird ein Ereignis [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) im geänderten **Recordset-Objekt** und in allen Klonen auftreten.</span><span class="sxs-lookup"><span data-stu-id="e074e-133">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="e074e-134">Der Parameter *Felder* des Ereignisses **WillChangeField** eines geklonte **Recordset-Objekt** (, in dem die Änderung nicht vorgenommen wurde) wird einfach finden Sie in die Felder des aktuellen Datensatzes des Klons, die möglicherweise von einem anderen Datensatz als der aktuelle Datensatz zu der ursprüngliche **Recordset-Objekt** , das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e074e-134">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="e074e-135">In der folgenden Tabelle wird eine vollständige Liste aller **Recordset** -Ereignisse bereitgestellt, und es wird angegeben, ob sie gültig sind und für mit der **Clone** -Methode generierte Recordsetklone ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="e074e-135">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e074e-136">Ereignis</span><span class="sxs-lookup"><span data-stu-id="e074e-136">Event</span></span></p></th>
<th><p><span data-ttu-id="e074e-137">Auslösung in Klonen</span><span class="sxs-lookup"><span data-stu-id="e074e-137">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e074e-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e074e-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-139">Nein</span><span class="sxs-lookup"><span data-stu-id="e074e-139">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e074e-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="e074e-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-141">Nein</span><span class="sxs-lookup"><span data-stu-id="e074e-141">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e074e-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="e074e-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-143">Nein</span><span class="sxs-lookup"><span data-stu-id="e074e-143">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e074e-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e074e-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-145">Ja</span><span class="sxs-lookup"><span data-stu-id="e074e-145">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e074e-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="e074e-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-147">Nein</span><span class="sxs-lookup"><span data-stu-id="e074e-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e074e-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e074e-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-149">Ja</span><span class="sxs-lookup"><span data-stu-id="e074e-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e074e-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e074e-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-151">Nein</span><span class="sxs-lookup"><span data-stu-id="e074e-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e074e-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="e074e-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-153">Ja</span><span class="sxs-lookup"><span data-stu-id="e074e-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e074e-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="e074e-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-155">Ja</span><span class="sxs-lookup"><span data-stu-id="e074e-155">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e074e-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e074e-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-157">Nein</span><span class="sxs-lookup"><span data-stu-id="e074e-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e074e-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="e074e-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="e074e-159">Nein</span><span class="sxs-lookup"><span data-stu-id="e074e-159">No</span></span></p></td>
</tr>
</tbody>
</table>

