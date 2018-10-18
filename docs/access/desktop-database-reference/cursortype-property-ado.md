---
<<<<<<< HEAD-Titel: CursorType-Eigenschaft (ADO) TOCTitle: CursorType-Eigenschaft (ADO) === Titel: CursorType-Eigenschaft (ADO) TOCTitle: CursorType-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) Ms:contentKeyID: 48548682 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="cursortype-property-ado"></a>CursorType-Eigenschaft (ADO)
=======
# <a name="cursortype-property-ado"></a>CursorType-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den Typ des Cursors an, der in einem [Recordset](recordset-object-ado.md)-Objekt verwendet wird.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird ein [CursorTypeEnum](cursortypeenum.md)-Wert festgelegt oder zurückgegeben. Der Standardwert ist **adOpenForwardOnly**.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CursorType** -Eigenschaft, um den Cursortyp anzugeben, der beim Öffnen des **Recordset** -Objekts verwendet werden soll.

Nur die Einstellung **adOpenStatic** wird unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Falls ein nicht unterstützter Wert festgelegt wird, wird kein Fehler gemeldet. Stattdessen wird die ähnlichste unterstützte **CursorType** -Eigenschaft verwendet.

Wenn ein Anbieter den angeforderten Cursortyp nicht unterstützt, gibt er möglicherweise einen anderen Cursortyp zurück. Die **CursorType** -Eigenschaft wird so geändert, dass sie zu dem tatsächlichen Cursortyp passt, der verwendet wird, wenn das [Recordset](recordset-object-ado.md)-Objekt geöffnet ist. Verwenden Sie die [Supports](supports-method-ado.md)-Methode, um die spezifische Funktionalität des zurückgegebenen Cursors zu überprüfen. Nachdem Sie das **Recordset** -Objekt geschlossen haben, wird die **CursorType** -Eigenschaft auf ihre ursprüngliche Einstellung zurückgesetzt.

Im folgenden Diagramm ist die für jeden Cursortyp erforderliche Anbieterfunktionalität (identifiziert durch die Konstanten der **Supports** -Methode) dargestellt.

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
<td><p>n/v</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>zulässt</strong>, <strong>AdHoldRecords</strong>, <strong>AdMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>zulässt</strong>, <strong>AdHoldRecords</strong>, <strong>AdMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Supports(adUpdateBatch) gibt zwar für dynamische Cursor und Vorwärtscursor True zurück, aber für Batchaktualisierungen sollten Sie einen Keysetcursor oder einen statischen Cursor verwenden. Legen Sie die LockType-Eigenschaft auf adLockBatchOptimistic sowie die CursorLocation-Eigenschaft auf adUseClient fest, um den für Batchaktualisierungen erforderlichen Cursordienst für OLE DB zu aktivieren.</P>



Die CursorType-Eigenschaft hat Lese-/Schreibzugriff, wenn das Recordset-Objekt geschlossen ist. Wenn das Recordset-Objekt geöffnet ist, ist sie schreibgeschützt.

**Remote Data Service-Verwendung** Wenn für ein clientseitiges Recordset-Objekt verwendet, kann die **CursorType** -Eigenschaft nur auf **AdOpenStatic**festgelegt werden.

