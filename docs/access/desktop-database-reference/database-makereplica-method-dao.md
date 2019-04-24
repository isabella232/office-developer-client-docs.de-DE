---
title: Database. MakeReplica-Methode (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294918"
---
# <a name="databasemakereplica-method-dao"></a>Database. MakeReplica-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Macht aus einem Datenbankreplikat ein neues Replikat (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . MakeReplica (***Pfadname***, ***Beschreibung***, ***Optionen***)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>PathName</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Der Pfad- und Dateiname des neuen Replikats. Wenn replica ein vorhandener Dateiname ist, tritt ein Fehler auf.</p></td>
</tr>
<tr class="even">
<td><p><em>Description</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ein <strong>String</strong>-Wert, der das Replikat beschreibt, das Sie erstellen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> -Konstante, die die Merkmale des Replikats angibt, das Sie erstellen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Für ein neu erstelltes Teilreplikat werden sämtliche **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** -Eigenschaften auf **False** festgelegt, was bedeutet, dass die Tabelle keine Daten enthält.

## <a name="example"></a>Beispiel

This function uses the **MakeReplica** method to create an additional replica of an existing Design Master. Das intOptions-Argument kann eine Kombination aus den Konstanten **dbRepMakeReadOnly** und **dbRepMakePartial**oder 0 sein. Wenn Sie beispielsweise ein nur-Lese-Teilreplikat erstellen möchten, sollten Sie den Wert **dbRepMakeReadOnly** + **dbRepMakePartial** als Wert von intOptions.

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

