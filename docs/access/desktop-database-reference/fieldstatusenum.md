---
title: FieldStatusEnum (Access-Desktopdatenbankreferenz)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5fd8afb1d1c8210b81629a004a9b58791d08fab6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573040"
---
# <a name="fieldstatusenum"></a>FieldStatusEnum

**Gilt für**: Access 2013, Office 2013

Gibt den Status eines **Field** -Objekts an.

Die **AdFieldPending\*** -Werte geben den Vorgang an, der zum Festlegen des Status geführt hat, und können mit anderen Statuswerten kombiniert werden.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFieldAlreadyExists</strong></p></td>
<td><p>26</p></td>
<td><p>Gibt an, dass das angegebene Feld bereits vorhanden ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldBadStatus</strong></p></td>
<td><p>12 </p></td>
<td><p>Gibt an, dass aus ADO ein ungültiger Statuswert an den OLE DB-Anbieter gesendet wurde. Mögliche Ursachen sind u. a. ein OLE DB 1.0- oder 1.1-Anbieter oder eine fehlerhafte Kombination aus <a href="value-property-ado.md">Wert</a> und <a href="status-property-ado-field.md">Status</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCannotComplete</strong></p></td>
<td><p>20</p></td>
<td><p>Gibt an, dass der Server der URL, die von <a href="source-property-ado-record.md">Quelle</a> angegeben wird, den Vorgang nicht abschließen konnte.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCannotDeleteSource</strong></p></td>
<td><p>23</p></td>
<td><p>Gibt an, dass eine Struktur oder eine Unterstruktur während eines Verschiebevorgangs an eine neue Position verschoben wurde, aber die Quelle nicht gelöscht werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt an, dass das Feld ohne Datenverlust nicht abgerufen oder gespeichert werden kann.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCantCreate</strong></p></td>
<td><p>7 </p></td>
<td><p>Gibt an, dass das Feld nicht hinzugefügt werden konnte, da der Anbieter eine Einschränkung (wie die Anzahl zulässiger Felder) überschritten hat.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6 </p></td>
<td><p>Gibt an, dass die vom Anbieter zurückgegebenen Daten einen Datentypüberlauf des Felds verursacht haben.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Gibt an, dass beim Festlegen von Daten der Standardwert für das Feld verwendet wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDoesNotExist</strong></p></td>
<td><p>16 </p></td>
<td><p>Gibt an, dass das angegebene Feld nicht vorhanden ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15 </p></td>
<td><p>Gibt an, dass dieses Feld übersprungen wurde, als in der Quelle Datenwerte festgelegt wurden. Der Anbieter legte keinen Wert fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Gibt an, dass das Feld nicht geändert werden kann, da es eine berechnete oder abgeleitete Einheit ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldInvalidURL</strong></p></td>
<td><p>17 </p></td>
<td><p>Gibt an, dass die URL der Datenquelle ungültige Zeichen enthält.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Gibt an, dass der Anbieter einen VARIANT-Wert vom Typ VT_NULL zurückgegeben hat und das Feld nicht leer ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Standardwert. Gibt an, dass das Feld erfolgreich hinzugefügt oder gelöscht wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Gibt an, dass der Anbieter nicht genügend Speicherplatz zum Abschließen eines Verschiebe- oder Kopiervorgangs in Anspruch nehmen kann.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingChange</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Gibt an, dass das Feld gelöscht und dann erneut hinzugefügt wurde, möglicherweise mit einem anderen Datentyp, oder dass sich der Wert des Felds, das zuvor den Status "adFieldOK" aufwies, geändert hat. Die endgültige Form des Felds ändert die <a href="fields-collection-ado.md">Fields-Auflistung,</a> nachdem die <a href="update-method-ado.md">Update-Methode</a> aufgerufen wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingDelete</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Gibt an, dass der <strong>Delete</strong>-Vorgang zum Festlegen des Status führte. Nachdem die <strong>Update</strong>-Methode aufgerufen wurde, wurde das Feld zum Löschen aus der <strong>Fields</strong>-Auflistung markiert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingInsert</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Gibt an, dass der Status durch den <strong>Append-Vorgang</strong> festgelegt wurde. The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingUnknown</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Gibt an, dass der Anbieter nicht ermitteln kann, welcher Vorgang zum Festlegen des Feldstatus führte.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingUnknownDelete</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Gibt an, dass der Anbieter nicht ermitteln kann, welcher Vorgang zum Festlegen des Status führte, und dass das Feld aus der <strong>Fields</strong>-Auflistung gelöscht wird, nachdem die <strong>Update</strong>-Methode aufgerufen wurde.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPermissionDenied</strong></p></td>
<td><p>9 </p></td>
<td><p>Gibt an, dass das Feld nicht geändert werden kann, da es als schreibgeschützt definiert ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldReadOnly</strong></p></td>
<td><p>24</p></td>
<td><p>Gibt an, dass das Feld in der Datenquelle als schreibgeschützt definiert ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceExists</strong></p></td>
<td><p>19</p></td>
<td><p>Gibt an, dass der Anbieter den Vorgang nicht ausführen konnte, da an der Ziel-URL bereits ein Objekt vorhanden ist und das Objekt nicht überschrieben werden kann.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldResourceLocked</strong></p></td>
<td><p>18 </p></td>
<td><p>Gibt an, dass der Anbieter den Vorgang nicht ausführen konnte, da die Datenquelle von mindestens einer Anwendung oder mindestens einem Prozess gesperrt ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceOutOfScope</strong></p></td>
<td><p>25</p></td>
<td><p>Gibt an, dass sich eine Quell- oder Ziel-URL außerhalb des aktuellen Datensatzbereichs befindet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Gibt an, dass der Wert die Datenquellschemaeinschränkung des Felds verletzt hat.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>Gibt an, dass der vom Anbieter zurückgegebene Datenwert Vorzeichen hatte, der Datentyp des ADO-Feldwerts jedoch nicht.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldTruncated</strong></p></td>
<td><p>4 </p></td>
<td><p>Gibt an, dass Daten variabler Länge beim Lesen aus der Datenquelle abgeschnitten wurden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldUnavailable</strong></p></td>
<td><p>8 </p></td>
<td><p>Gibt an, dass der Anbieter den Wert beim Lesen aus der Datenquelle nicht ermitteln konnte. Beispielsweise wurde die Zeile gerade erstellt, der Standardwert für die Spalte war nicht verfügbar und ein neuer Wert wurde noch nicht angegeben.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldVolumeNotFound</strong></p></td>
<td><p> 21</p></td>
<td><p>Gibt an, dass der Anbieter das von der URL angegebene Speichervolume nicht finden kann.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

