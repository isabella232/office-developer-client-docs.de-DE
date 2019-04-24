---
title: Clone-Methode-ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296346"
---
# <a name="clone-method-ado"></a><span data-ttu-id="e3f1c-102">Clone-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="e3f1c-102">Clone method (ADO)</span></span>

<span data-ttu-id="e3f1c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3f1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3f1c-104">Ein [Recordset](recordset-object-ado.md)-Objektduplikat wird aus einem vorhandenen **Recordset** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="e3f1c-105">Optional wird angegeben, dass der Klon schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f1c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3f1c-106">Syntax</span></span>

<span data-ttu-id="e3f1c-107">**Festgelegt** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="e3f1c-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="e3f1c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3f1c-108">Return value</span></span>

<span data-ttu-id="e3f1c-109">Ein **Recordset**-Objektverweis wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3f1c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3f1c-110">Parameters</span></span>

|<span data-ttu-id="e3f1c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3f1c-111">Parameter</span></span>|<span data-ttu-id="e3f1c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3f1c-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e3f1c-113">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="e3f1c-113">*rstDuplicate*</span></span> |<span data-ttu-id="e3f1c-114">Eine Objektvariable, durch die das zu erstellende **Recordset** -Objektduplikat identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="e3f1c-115">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="e3f1c-115">*rstOriginal*</span></span> |<span data-ttu-id="e3f1c-116">Eine Objektvariable, durch die das zu duplizierende **Recordset** -Objekt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="e3f1c-117">*LockType*</span><span class="sxs-lookup"><span data-stu-id="e3f1c-117">*LockType*</span></span> |<span data-ttu-id="e3f1c-p102">Optional. Ein [LockTypeEnum](locktypeenum.md)-Wert, durch den der Sperrtyp des Original **recordsets** oder ein schreibgeschütztes **Recordset** angegeben wird. Gültige Werte sind **adLockUnspecified** oder **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e3f1c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3f1c-121">Remarks</span></span>

<span data-ttu-id="e3f1c-p103">Verwenden Sie die **Clone** -Methode zum Erstellen mehrerer **Recordset** -Objektduplikate, insbesondere, wenn Sie mehrere aktuelle Datensätze in einem bestimmten Satz mit Datensätzen aufrechterhalten möchten. Das Verwenden der **Clone** -Methode ist effizienter als das Erstellen und Öffnen eines neuen **Recordset** -Objekts mit der gleichen Definition wie das Original.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="e3f1c-p104">Die [Filter](filter-property-ado.md)-Eigenschaft des Original **recordsets**, falls vorhanden, wird nicht auf den Klon angewendet. Legen Sie die **Filter** -Eigenschaft des neuen **Recordsets** fest, um die Ergebnisse zu filtern. Die einfachste Möglichkeit zum Kopieren vorhandener **Filter** -Werte ist das direkte Zuweisen:</span><span class="sxs-lookup"><span data-stu-id="e3f1c-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="e3f1c-127">Der aktuelle Datensatz eines neu erstellten Klons wird auf den ersten Datensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="e3f1c-p105">An einem **Recordset** -Objekt vorgenommene Änderungen werden unabhängig vom Cursortyp in allen Klonen des Objekts angezeigt. Nach dem Ausführen von [Requery](requery-method-ado.md) für das ursprüngliche **Recordset** -Objekt werden die Klone jedoch nicht mehr mit dem Original synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="e3f1c-130">Durch das Schließen des Original **recordsets** werden die Kopien nicht geschlossen, und durch das Schließen einer Kopie werden das Original oder andere Kopien nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="e3f1c-p106">Sie können nur **Recordset** -Objekte klonen, von denen Textmarken unterstützt werden. Textmarkenwerte sind austauschbar; d. h., ein Textmarkenverweis eines **Recordset** -Objekts verweist auf den gleichen Datensatz in den Klonen.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="e3f1c-p107">Einige ausgelöste **Recordset** -Ereignisse werden auch in allen **Recordset** klonen ausgeführt. Die Ereignisse sind für den Klon jedoch möglicherweise nicht gültig, da sich der aktuelle Datensatz zwischen geklonten **Recordsets** unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="e3f1c-p108">Wenn Sie z. B. einen Wert eines Felds ändern, tritt im geänderten **Recordset** und in allen Klonen ein [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md)-Ereignis auf. Durch den *Fields*-Parameter des **WillChangeField**-Ereignisses eines geklonten **Recordsets** (in dem die Änderung nicht vorgenommen wurde) wird einfach auf die Felder des aktuellen Datensatzes des Klons verwiesen, der ein anderer Datensatz sein kann als der aktuelle Datensatz des Original**recordsets**, in dem die Änderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-p108">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones. The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="e3f1c-137">In der folgenden Tabelle wird eine vollständige Liste aller **Recordset**-Ereignisse bereitgestellt, und es wird angegeben, ob sie gültig sind und für mit der **Clone**-Methode generierte Recordsetklone ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="e3f1c-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3f1c-138">Ereignis</span><span class="sxs-lookup"><span data-stu-id="e3f1c-138">Event</span></span></p></th>
<th><p><span data-ttu-id="e3f1c-139">Auslösung in Klonen</span><span class="sxs-lookup"><span data-stu-id="e3f1c-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3f1c-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-141">Nein</span><span class="sxs-lookup"><span data-stu-id="e3f1c-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f1c-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-143">Nein</span><span class="sxs-lookup"><span data-stu-id="e3f1c-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f1c-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-145">Nein</span><span class="sxs-lookup"><span data-stu-id="e3f1c-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f1c-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-147">Ja</span><span class="sxs-lookup"><span data-stu-id="e3f1c-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f1c-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-149">Nein</span><span class="sxs-lookup"><span data-stu-id="e3f1c-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f1c-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-151">Ja</span><span class="sxs-lookup"><span data-stu-id="e3f1c-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f1c-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-153">Nein</span><span class="sxs-lookup"><span data-stu-id="e3f1c-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f1c-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-155">Ja</span><span class="sxs-lookup"><span data-stu-id="e3f1c-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f1c-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-157">Ja</span><span class="sxs-lookup"><span data-stu-id="e3f1c-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3f1c-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-159">Nein</span><span class="sxs-lookup"><span data-stu-id="e3f1c-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3f1c-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="e3f1c-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="e3f1c-161">Nein</span><span class="sxs-lookup"><span data-stu-id="e3f1c-161">No</span></span></p></td>
</tr>
</tbody>
</table>

