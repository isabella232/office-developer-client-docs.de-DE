---
<span data-ttu-id="5fce5-101"><<<<<<< HEAD-Titel: CursorType-Eigenschaft (ADO) TOCTitle: CursorType-Eigenschaft (ADO) === Titel: CursorType-Eigenschaft (ADO) TOCTitle: CursorType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5fce5-101"><<<<<<< HEAD title: CursorType Property (ADO) TOCTitle: CursorType Property (ADO) ======= title: CursorType property (ADO) TOCTitle: CursorType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5fce5-102">Master Ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) Ms:contentKeyID: 48548682 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="5fce5-102">master ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID: 48548682 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5fce5-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="5fce5-103"><<<<<<< HEAD</span></span>
# <a name="cursortype-property-ado"></a><span data-ttu-id="5fce5-104">CursorType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5fce5-104">CursorType Property (ADO)</span></span>
=======
# <a name="cursortype-property-ado"></a><span data-ttu-id="5fce5-105">CursorType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="5fce5-105">CursorType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5fce5-106">master</span><span class="sxs-lookup"><span data-stu-id="5fce5-106">master</span></span>


<span data-ttu-id="5fce5-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fce5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5fce5-108">Gibt den Typ des Cursors an, der in einem [Recordset](recordset-object-ado.md)-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fce5-108">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="5fce5-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="5fce5-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="5fce5-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5fce5-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="5fce5-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5fce5-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="5fce5-112">master</span><span class="sxs-lookup"><span data-stu-id="5fce5-112">master</span></span>

<span data-ttu-id="5fce5-p101">Mit dieser Eigenschaft wird ein [CursorTypeEnum](cursortypeenum.md)-Wert festgelegt oder zurückgegeben. Der Standardwert ist **adOpenForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="5fce5-p101">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value. The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fce5-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5fce5-115">Remarks</span></span>

<span data-ttu-id="5fce5-116">Verwenden Sie die **CursorType** -Eigenschaft, um den Cursortyp anzugeben, der beim Öffnen des **Recordset** -Objekts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fce5-116">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="5fce5-p102">Nur die Einstellung **adOpenStatic** wird unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Falls ein nicht unterstützter Wert festgelegt wird, wird kein Fehler gemeldet. Stattdessen wird die ähnlichste unterstützte **CursorType** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fce5-p102">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="5fce5-p103">Wenn ein Anbieter den angeforderten Cursortyp nicht unterstützt, gibt er möglicherweise einen anderen Cursortyp zurück. Die **CursorType** -Eigenschaft wird so geändert, dass sie zu dem tatsächlichen Cursortyp passt, der verwendet wird, wenn das [Recordset](recordset-object-ado.md)-Objekt geöffnet ist. Verwenden Sie die [Supports](supports-method-ado.md)-Methode, um die spezifische Funktionalität des zurückgegebenen Cursors zu überprüfen. Nachdem Sie das **Recordset** -Objekt geschlossen haben, wird die **CursorType** -Eigenschaft auf ihre ursprüngliche Einstellung zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5fce5-p103">If a provider does not support the requested cursor type, it may return another cursor type. The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open. To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method. After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="5fce5-123">Im folgenden Diagramm ist die für jeden Cursortyp erforderliche Anbieterfunktionalität (identifiziert durch die Konstanten der **Supports** -Methode) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5fce5-123">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fce5-124">Für ein Recordset mit diesem "CursorType"</span><span class="sxs-lookup"><span data-stu-id="5fce5-124">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="5fce5-125">Die Supports-Methode muss für alle diese Konstanten "True" zurückgeben</span><span class="sxs-lookup"><span data-stu-id="5fce5-125">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fce5-126"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="5fce5-126"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="5fce5-127">n/v</span><span class="sxs-lookup"><span data-stu-id="5fce5-127">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fce5-128"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="5fce5-128"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="5fce5-129"><strong>zulässt</strong>, <strong>AdHoldRecords</strong>, <strong>AdMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="5fce5-129"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fce5-130"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="5fce5-130"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="5fce5-131"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="5fce5-131"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fce5-132"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="5fce5-132"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="5fce5-133"><strong>zulässt</strong>, <strong>AdHoldRecords</strong>, <strong>AdMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="5fce5-133"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="5fce5-p104">Supports(adUpdateBatch) gibt zwar für dynamische Cursor und Vorwärtscursor True zurück, aber für Batchaktualisierungen sollten Sie einen Keysetcursor oder einen statischen Cursor verwenden. Legen Sie die LockType-Eigenschaft auf adLockBatchOptimistic sowie die CursorLocation-Eigenschaft auf adUseClient fest, um den für Batchaktualisierungen erforderlichen Cursordienst für OLE DB zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5fce5-p104">Although <STRONG>Supports</STRONG>(<STRONG>adUpdateBatch</STRONG>) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor. Set the <A href="locktype-property-ado.md">LockType</A> property to <STRONG>adLockBatchOptimistic</STRONG> and the <STRONG>CursorLocation</STRONG> property to <STRONG>adUseClient</STRONG> to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span></P>



<span data-ttu-id="5fce5-136">Die CursorType-Eigenschaft hat Lese-/Schreibzugriff, wenn das Recordset-Objekt geschlossen ist. Wenn das Recordset-Objekt geöffnet ist, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5fce5-136">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="5fce5-137">**Remote Data Service-Verwendung** Wenn für ein clientseitiges Recordset-Objekt verwendet, kann die **CursorType** -Eigenschaft nur auf **AdOpenStatic**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5fce5-137">**Remote Data Service Usage**When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

