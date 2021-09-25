---
title: CursorType-Eigenschaft (ADO)
TOCTitle: CursorType property (ADO)
ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15)
ms:contentKeyID: 48548682
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6c94012224a75d52d7e9e096c8c98873fbf4a6a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581567"
---
# <a name="cursortype-property-ado"></a>CursorType-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Typ des Cursors an, der in einem [Recordset](recordset-object-ado.md)-Objekt verwendet wird.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein [CursorTypeEnum](cursortypeenum.md)-Wert festgelegt oder zurückgegeben. Der Standardwert ist **adOpenForwardOnly**.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **CursorType**-Eigenschaft, um den Cursortyp anzugeben, der beim Öffnen des **Recordset**-Objekts verwendet werden soll.

Nur die Einstellung **adOpenStatic** wird unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Falls ein nicht unterstützter Wert festgelegt wird, wird kein Fehler gemeldet. Stattdessen wird die ähnlichste unterstützte **CursorType** -Eigenschaft verwendet.

Wenn ein Anbieter den angeforderten Cursortyp nicht unterstützt, gibt er möglicherweise einen anderen Cursortyp zurück. Die **CursorType** -Eigenschaft wird so geändert, dass sie zu dem tatsächlichen Cursortyp passt, der verwendet wird, wenn das [Recordset](recordset-object-ado.md)-Objekt geöffnet ist. Verwenden Sie die [Supports](supports-method-ado.md)-Methode, um die spezifische Funktionalität des zurückgegebenen Cursors zu überprüfen. Nachdem Sie das **Recordset** -Objekt geschlossen haben, wird die **CursorType** -Eigenschaft auf ihre ursprüngliche Einstellung zurückgesetzt.

Im folgenden Diagramm ist die für jeden Cursortyp erforderliche Anbieterfunktionalität (identifiziert durch die Konstanten der **Supports**-Methode) dargestellt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Für ein Recordset mit diesem "CursorType"</p></th>
<th><p>Die Supports-Methode muss für alle diese Konstanten "True" zurückgeben</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>keine</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Obwohl **Supports**(**adUpdateBatch**) für dynamische und vorwärtsgerichtete Cursor wahr sein kann, sollten Sie für Batchaktualisierungen entweder einen Keyset oder einen statischen Cursor verwenden. Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.

The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.

**Remote data service usage** Bei Verwendung in einem clientseitigen Recordset -Objekt kann die **CursorType** -Eigenschaft nur auf **adOpenStatic** festgelegt werden.

