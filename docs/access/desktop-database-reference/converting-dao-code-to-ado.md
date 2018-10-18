---
<<<<<<< HEAD-Titel: Konvertieren von DAO-Code in ADO TOCTitle: Konvertieren von DAO-Code in ADO Ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae Ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) Ms:contentKeyID: 48544585 ms.date: 09/18/2015 === Titel: Konvertieren von DAO Code in ADO TOCTitle: Konvertieren von DAO-Code in ADO Ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae Ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) Ms:contentKeyID: 48544585 ms.date: 10/16/2018
>>>>>>> Master-Shape Mtps_version: Office. 15 f1_keywords:
- vbaac10.chm5267115 f1_categories:
- Office.Version=v15
---

<<<<<<< Kopf
# <a name="converting-dao-code-to-ado"></a>Konvertieren von DAO-Code in ADO
=======
# <a name="convert-dao-code-to-ado"></a>Konvertieren von DAO-Code in ADO
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

> [!NOTE]
> Versionen der DAO-Bibliothek vor Version 3.6 nicht bereitgestellt oder in Access unterstützt.

## <a name="dao-to-ado-object-map"></a>DAO-Objekten in ADO-objektzuordnung

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<<<<<<< Kopf
<th><p><strong>ADO(ADODB)</strong></p></th>
=======
<th><p><strong>ADO (ADODB)</strong></p></th>
>>>>>>>Master-Shape
<th><p><strong>Hinweis</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>Keine</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Workspace</p></td>
<td><p>Keine</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Database</p></td>
<td><p>Connection</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Recordset</p></td>
<td><p>Recordset</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Dynaset-Type</p></td>
<td><p>Keyset</p></td>
<<<<<<< Kopf
<td><p>Ruft eine Gruppe von Zeigern auf die Datensätze im Recordset ab.</p></td>
=======
<td><p>Ruft eine Gruppe von Zeigern für die Datensätze im Recordset-Objekt ab.</p></td>
>>>>>>>Master-Shape
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<<<<<<< Kopf
<td><p>Beide rufen vollständige Datensätze ab, ein statisches Recordset kann jedoch aktualisiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset mit adCmdTableDirect-Option</p></td>
=======
<td><p>Beide vollständige Datensätze abrufen, jedoch kann eine statische Datensatzgruppe aktualisiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset mit Option AdCmdTableDirect.</p></td>
>>>>>>>Master-Shape
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Field</p></td>
<td><p>Field</p></td>
<<<<<<< Kopf
<td><p>Wenn auf einen Recordset verwiesen wird</p></td>
=======
<td><p>Wenn in einem Recordset bezeichnet.</p></td>
>>>>>>>Master-Shape
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Öffnen eines Recordsets

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Bearbeiten eines Recordsets

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Öffnen eines Recordsets

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Bearbeiten eines Recordsets

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
<<<<<<< Vom aktuellen Datensatz über **MoveNext, MoveLast, MoveFirst, MovePrevious** konzentrieren HEAD verschieben, ohne zuerst mit der **CancelUpdate** -Methode implizit die **Update** -Methode ausgeführt wird.
> === Verschieben den Fokus vom aktuellen Datensatz über **MoveNext, MoveLast, MoveFirst, MovePrevious** ohne zuerst die **CancelUpdate** -Methode implizit führt die **Update** -Methode.
>>>>>>> master

### <a name="about-the-contributors"></a>Informationen zu den Mitwirkenden

**Link bereitgestellt, von** der Community [UtterAccess](https://www.utteraccess.com) . UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [Choosing between DAO and ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado) (Wählen zwischen DAO und ADO)

<<<<<<< Kopf

=======
<br/>
>>>>>>> master

