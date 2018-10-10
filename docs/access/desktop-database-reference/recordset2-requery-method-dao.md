---
title: Recordset2.Requery Method (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7019b0e4d3ffa916aea8436db14f3a8476f2e36f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472711"
---
# <a name="recordset2requery-method-dao"></a>Recordset2.Requery Method (DAO)


**Betrifft**: Access 2013 | Office 2013

Die Daten in einem **[Recordset](recordset-object-dao.md)** -Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Requery (***NewQueryDef***)

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

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
<td><p>NewQueryDef</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Stellt den <strong>Name</strong> -Eigenschaftenwert eines <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekts dar</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um sicherzustellen, dass ein **Recordset** die aktuellsten Daten enthält. Diese Methode füllt das aktuelle **Recordset** erneut mithilfe der aktuellen Abfrageparameter oder (in einem Microsoft Access-Arbeitsbereich) die neuen Dateien durch das Argument Newquerydef angegeben.

Wenn Sie ein Argument Newquerydef nicht angeben, wird das **Recordset-Objekt** neu aufgefüllt basierend auf dem gleichen Abfragedefinition und Parameter verwendet, um das **Recordset**ursprünglich aufzufüllen. Änderungen an zugrunde liegenden Daten werden während des Auffüllvorgangs angezeigt. Wenn Sie zum Erstellen des **Recordset**-Objekts kein **QueryDef**-Objekt verwendet haben, wird das **Recordset** ganz neu erstellt.

Wenn Sie die ursprünglichen **QueryDef-Objekt** im Newquerydef Argument angeben, wird das **Recordset** erneut abgefragt mit den Parametern von **QueryDef-Objekt**angegeben. Änderungen an zugrunde liegenden Daten werden während des Auffüllvorgangs angezeigt. Alle Änderungen an der Abfrageparameterwerte im **Recordset-Objekt**aktualisiert, müssen Sie das Argument Newquerydef angeben.

Wenn Sie ein anderes **QueryDef** angeben als das, mit dem das **Recordset** ursprünglich erstellt wurde, wird das **Recordset** völlig neu erstellt.

Beim Anwenden von **Requery** wird der erste Datensatz im **Recordset** zum aktuellen Datensatz.

Sie können die **Requery** -Methode nicht für **Recordset** -Objekte des dynaset- oder snapshot-Typs verwenden, deren **[Restartable](recordset2-restartable-property-dao.md)** -Eigenschaft auf **False** festgelegt ist. Wenn Sie das Argument optional Newquerydef angeben, wird jedoch die **Restartable** -Eigenschaft ignoriert.

Ist für die beiden Eigenschafteneinstellungen **[BOF](recordset2-bof-property-dao.md)** und **[EOF](recordset2-eof-property-dao.md)** des **Recordset**-Objekts nach dem Verwenden der **Requery**-Methode **True** festgelegt, hat die Abfrage keine Datensätze zurückgegeben, und das **Recordset** enthält keine Daten.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie die **Requery** -Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die zugrunde liegenden Daten geändert wurden.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel zeigt, wie die **Requery** -Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die Abfrageparamter geändert wurden.

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

