---
title: Database.MakeReplica Method (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8596548389b066b6ff11e7103090ef50906d79a9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475472"
---
# <a name="databasemakereplica-method-dao"></a>Database.MakeReplica Method (DAO)

**Betrifft**: Access 2013 | Office 2013

Macht aus einem Datenbankreplikat ein neues Replikat (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . MakeReplica (***Pfadname***, ***Beschreibung***, ***Optionen***)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

### <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Pfadname</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Pfad- und Dateiname des neuen Replikats. Wenn replica ein vorhandener Dateiname ist, tritt ein Fehler auf.</p></td>
</tr>
<tr class="even">
<td><p>Beschreibung</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ein <strong>String</strong>-Wert, der das Replikat beschreibt, das Sie erstellen.</p></td>
</tr>
<tr class="odd">
<td><p>Options</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> -Konstante, die Eigenschaften des Replikats angibt, die Sie erstellen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Für ein neu erstelltes Teilreplikat werden sämtliche **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** -Eigenschaften auf **False** festgelegt, was bedeutet, dass die Tabelle keine Daten enthält.

## <a name="example"></a>Beispiel

Diese Funktion verwendet die **MakeReplica** -Methode, um ein zusätzliches Replikat eines vorhandenen Designmasters zu erstellen. Das IntOptions-Argument kann eine Kombination aus Konstanten **DbRepMakeReadOnly** und **DbRepMakePartial**sein, oder es kann 0 sein. Beispielsweise zum Erstellen eines Teilreplikats schreibgeschützt sollten, übergeben Sie den Wert **DbRepMakeReadOnly** + **DbRepMakePartial** als Wert des IntOptions.

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

