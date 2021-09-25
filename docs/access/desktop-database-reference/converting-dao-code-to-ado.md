---
title: Konvertieren von DAO-Code in ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 175f168fdc384570ad99c86db9e0c185b7d6cf38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569251"
---
# <a name="convert-dao-code-to-ado"></a>Konvertieren von DAO-Code in ADO

**Gilt für**: Access 2013, Office 2013

> [!NOTE]
> Versionen der DAO-Bibliothek, die älter als Version 3.6 sind, werden in Access nicht bereitgestellt und nicht unterstützt.

## <a name="dao-to-ado-object-map"></a>Umwandlung von DAO-Objekten in ADO-Objekte

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO (ADODB)</strong></p></th>
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
<td><p>Datenbank</p></td>
<td><p>Verbindung</p></td>
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
<td><p>Ruft eine Gruppe von Zeigern für die Datensätze der Datensatzgruppe ab.</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>Rufen beide vollständige Datensätze ab, doch eine Datensatzgruppe vom Typ Static kann aktualisiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset mit Option adCmdTableDirect.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Feld</p></td>
<td><p>Feld</p></td>
<td><p>Wenn darauf in einer Datensatzgruppe verwiesen wird.</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Recordset öffnen

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Recordset bearbeiten

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Recordset öffnen

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Recordset bearbeiten

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> Wenn der Fokus über **MoveNext, MoveLast, MoveFirst, MovePrevious** vom aktuellen Datensatz verschoben wird, ohne zuerst die **CancelUpdate**-Methode zu verwenden, wird die **Update**-Methode implizit ausgeführt.

### <a name="about-the-contributors"></a>Informationen zu den Mitwirkenden

**Link zur Verfügung gestellt von:** [UtterAccess](https://www.utteraccess.com)-Community. UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [Entscheidung zwischen DAO und ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

