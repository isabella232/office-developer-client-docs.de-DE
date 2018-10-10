---
title: Konvertieren von DAO-Code in ADO
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472658"
---
# <a name="converting-dao-code-to-ado"></a>Konvertieren von DAO-Code in ADO

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
<th><p><strong>ADO(ADODB)</strong></p></th>
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
<td><p>Ruft eine Gruppe von Zeigern auf die Datensätze im Recordset ab.</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>Beide rufen vollständige Datensätze ab, ein statisches Recordset kann jedoch aktualisiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset mit adCmdTableDirect-Option</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Field</p></td>
<td><p>Field</p></td>
<td><p>Wenn darauf in einer Datensatzgruppe verwiesen wird</p></td>
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
> [!HINWEIS] Wenn der Fokus über **MoveNext, MoveLast, MoveFirst, MovePrevious** vom aktuellen Datensatz verschoben wird, ohne zuerst die **CancelUpdate** -Methode zu verwenden, wird die **Update** -Methode implizit ausgeführt.

### <a name="about-the-contributors"></a>Informationen zu den Mitwirkenden

**Link bereitgestellt, von** der Community [UtterAccess](https://www.utteraccess.com) . UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [Choosing between DAO and ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado) (Wählen zwischen DAO und ADO)



