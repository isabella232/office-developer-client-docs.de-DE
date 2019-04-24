---
title: CursorType-Eigenschaft (ADO)
TOCTitle: CursorType property (ADO)
ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15)
ms:contentKeyID: 48548682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7cdb32bb8ff9bb6e0556a87de0efe82cd919dbe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295184"
---
# <a name="cursortype-property-ado"></a><span data-ttu-id="7c196-102">CursorType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="7c196-102">CursorType property (ADO)</span></span>


<span data-ttu-id="7c196-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c196-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c196-104">Gibt den Typ des Cursors an, der in einem [Recordset](recordset-object-ado.md)-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c196-104">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7c196-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7c196-105">Settings and return values</span></span>

<span data-ttu-id="7c196-106">Mit dieser Eigenschaft wird ein [CursorTypeEnum](cursortypeenum.md)-Wert festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c196-106">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value.</span></span> <span data-ttu-id="7c196-107">Der Standardwert ist **adOpenForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="7c196-107">The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c196-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c196-108">Remarks</span></span>

<span data-ttu-id="7c196-109">Verwenden Sie die **CursorType**-Eigenschaft, um den Cursortyp anzugeben, der beim Öffnen des **Recordset**-Objekts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c196-109">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="7c196-p102">Nur die Einstellung **adOpenStatic** wird unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Falls ein nicht unterstützter Wert festgelegt wird, wird kein Fehler gemeldet. Stattdessen wird die ähnlichste unterstützte **CursorType** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c196-p102">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="7c196-p103">Wenn ein Anbieter den angeforderten Cursortyp nicht unterstützt, gibt er möglicherweise einen anderen Cursortyp zurück. Die **CursorType** -Eigenschaft wird so geändert, dass sie zu dem tatsächlichen Cursortyp passt, der verwendet wird, wenn das [Recordset](recordset-object-ado.md)-Objekt geöffnet ist. Verwenden Sie die [Supports](supports-method-ado.md)-Methode, um die spezifische Funktionalität des zurückgegebenen Cursors zu überprüfen. Nachdem Sie das **Recordset** -Objekt geschlossen haben, wird die **CursorType** -Eigenschaft auf ihre ursprüngliche Einstellung zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7c196-p103">If a provider does not support the requested cursor type, it may return another cursor type. The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open. To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method. After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="7c196-116">Im folgenden Diagramm ist die für jeden Cursortyp erforderliche Anbieterfunktionalität (identifiziert durch die Konstanten der **Supports**-Methode) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c196-116">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c196-117">Für ein Recordset mit diesem "CursorType"</span><span class="sxs-lookup"><span data-stu-id="7c196-117">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="7c196-118">Die Supports-Methode muss für alle diese Konstanten "True" zurückgeben</span><span class="sxs-lookup"><span data-stu-id="7c196-118">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c196-119"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="7c196-119"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="7c196-120">none</span><span class="sxs-lookup"><span data-stu-id="7c196-120">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c196-121"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="7c196-121"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="7c196-122"><strong>Bookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="7c196-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c196-123"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="7c196-123"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="7c196-124"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="7c196-124"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c196-125"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="7c196-125"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="7c196-126"><strong>Bookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="7c196-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="7c196-127">Obwohl **unterstützt**(**adUpdateBatch**) für dynamische und Vorwärtscursor möglicherweise true ist, sollten Sie bei Batchaktualisierungen entweder ein Keyset oder einen statischen Cursor verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c196-127">Although **Supports**(**adUpdateBatch**) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor.</span></span> <span data-ttu-id="7c196-128">Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.</span><span class="sxs-lookup"><span data-stu-id="7c196-128">Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span>

<span data-ttu-id="7c196-129">Die **CursorType** -Eigenschaft ist schreibgeschützt, wenn das **Recordset** -Objekt geschlossen und schreibgeschützt ist, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="7c196-129">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="7c196-130">**Remote Data Service-Verwendung** Wenn die **CursorType** -Eigenschaft für ein clientseitiges Recordset-Objekt verwendet wird, kann Sie nur auf **adOpenStatic**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7c196-130">**Remote Data Service Usage**When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

