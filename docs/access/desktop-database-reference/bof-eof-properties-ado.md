---
<<<<<<< HEAD-Titel: BOF- und EOF-Eigenschaften (ADO) TOCTitle: BOF- und EOF-Eigenschaften (ADO) === Titel: BOF-und EOF-Eigenschaft (ADO) TOCTitle: BOF-und EOF-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) Ms:contentKeyID: 48548768 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="bof-eof-properties-ado"></a>BOF- und EOF-Eigenschaft (ADO)
=======
# <a name="bof-eof-properties-ado"></a>BOF-und EOF-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

  - **BOF** - Gibt an, dass die aktuelle Datensatzposition vor dem ersten Datensatz in einem [Recordset](recordset-object-ado.md)-Objekt liegt.

  - **EOF** - Gibt an, dass die aktuelle Datensatzposition nach dem letzten Datensatz in einem **Recordset** -Objekt liegt.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Die **BOF** - und die **EOF** -Eigenschaft geben Werte vom Datentyp **Boolean** zurück.

## <a name="remarks"></a>Hinweise

Bestimmen Sie mithilfe der Eigenschaften **BOF** und **EOF**, ob ein **Recordset** -Objekt Datensätze enthält oder ob Sie beim Navigieren in den Datensätzen die Grenzen eines **Recordset** -Objekts überschritten haben.

Die **BOF** -Eigenschaft gibt **True** (-1) zurück, falls sich die aktuelle Datensatzposition vor dem ersten Datensatz befindet, und **False** (0), falls sich die aktuelle Datensatzposition im oder nach dem ersten Datensatz befindet.

Die **EOF** -Eigenschaft gibt **True** zurück, falls sich die aktuelle Datensatzposition nach dem letzten Datensatz befindet, und **False**, falls sich die aktuelle Datensatzposition im oder vor dem letzten Datensatz befindet.

Wenn die **BOF** - oder die **EOF** -Eigenschaft **True** ist, gibt es keinen aktuellen Datensatz.

Wenn Sie ein **Recordset**-Objekt öffnen, das keine Datensätze enthält, werden die Eigenschaften **BOF** und **EOF** auf **True** festgelegt (weitere Informationen zu diesem Status eines **Recordset**-Objekts finden Sie unter der [RecordCount](recordcount-property-ado.md)-Eigenschaft). Wenn Sie ein **Recordset**-Objekt öffnen, das mindestens einen Datensatz enthält, ist der erste Datensatz der aktuelle Datensatz, und die Eigenschaften **BOF** und **EOF** sind **False**.

Wenn Sie den letzten verbleibenden Datensatz im **Recordset** -Objekt löschen, bleiben die Eigenschaften **BOF** und **EOF** so lange **False**, bis Sie versuchen, den aktuellen Datensatz neu zu positionieren.

In dieser Tabelle ist dargestellt, welche **Move** -Methoden für verschiedene Kombinationen der Eigenschaften **BOF** und **EOF** zulässig sind.

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
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Verschieben von &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Verschieben von &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = "true"</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>Zulässig</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
<td><p>Zulässig</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = "false"</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
</tr>
<tr class="odd">
<td><p>Beide <strong>True</strong></p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
<td><p>Fehler</p></td>
</tr>
<tr class="even">
<td><p>Beide <strong>False</strong></p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
<td><p>Zulässig</p></td>
</tr>
</tbody>
</table>


Das Zulassen einer **Move** -Methode garantiert nicht, dass die Methode einen Datensatz erfolgreich findet. Es bedeutet nur, dass beim Aufrufen der angegebenen **Move** -Methode kein Fehler generiert wird.

Die folgende Tabelle zeigt, was mit den Einstellungen der Eigenschaften **BOF** und **EOF** passiert, wenn Sie verschiedene **Move** -Methoden aufrufen, einen Datensatz aber nicht finden können.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p>Auf <strong>True</strong> festgelegt</p></td>
<td><p>Auf <strong>True</strong> festgelegt</p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Keine Änderung</p></td>
<td><p>Keine Änderung</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>Verschieben Sie</strong> &lt; 0</p></td>
<td><p>Festgelegt auf <strong>True</strong></p></td>
<td><p>Keine Änderung</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>Verschieben Sie</strong> &gt; 0</p></td>
<td><p>Keine Änderung</p></td>
<td><p>Festgelegt auf <strong>True</strong></p></td>
</tr>
</tbody>
</table>
