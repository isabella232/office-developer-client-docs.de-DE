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
# <a name="cursortype-property-ado"></a>CursorType-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Typ des Cursors an, der in einem [Recordset](recordset-object-ado.md)-Objekt verwendet wird.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein [CursorTypeEnum](cursortypeenum.md)-Wert festgelegt oder zurückgegeben. Der Standardwert ist **adOpenForwardOnly**.

## <a name="remarks"></a>Bemerkungen

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
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>Bookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>Bookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Obwohl **unterstützt**(**adUpdateBatch**) für dynamische und Vorwärtscursor möglicherweise true ist, sollten Sie bei Batchaktualisierungen entweder ein Keyset oder einen statischen Cursor verwenden. Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.

Die **CursorType** -Eigenschaft ist schreibgeschützt, wenn das **Recordset** -Objekt geschlossen und schreibgeschützt ist, wenn es geöffnet ist.

**Remote Data Service-Verwendung** Wenn die **CursorType** -Eigenschaft für ein clientseitiges Recordset-Objekt verwendet wird, kann Sie nur auf **adOpenStatic**festgelegt werden.

