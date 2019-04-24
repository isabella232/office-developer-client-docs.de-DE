---
title: Field-Objekt – Datenzugriffsobjekte (Data Access Objects, DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293042"
---
# <a name="field-object-dao"></a>Field-Objekt (DAO)

**Gilt für**: Access 2013, Office 2013

Ein **Field**-Objekt stellt eine Spalte mit Daten mit einem gemeinsamen Datentyp und einem gemeinsamen Satz von Eigenschaften dar.

## <a name="remarks"></a>Bemerkungen

Die **Fields**-Auflistung der Objekte **Index**, **QueryDef**, **Relation** und **TableDef** enthält die Spezifikationen für die Felder, die diese Objekte darstellen. Die **Fields**-Auflistung eines **Recordset**-Objekts stellt die **Field**-Objekte in einer Zeile mit Daten oder einem Datensatz dar. Verwenden Sie die **Field**-Objekte in einem **Recordset**-Objekt, um Werte für die Felder im aktuellen Datensatz des **Recordset**-Objekts zu lesen oder festzulegen.

In einem Microsoft Access-Arbeitsbereich verwenden Sie ein **Field**-Objekt und dessen Methoden und Eigenschaften, um ein Feld zu bearbeiten. Sie können z. B. die folgenden Aktionen ausführen:

  - Verwenden Sie die **OrdinalPosition**-Eigenschaft, um die Präsentationsreihenfolge des **Field**-Objekts in einer **Fields**-Auflistung festzulegen oder zurückzugeben.

  - Verwenden Sie die **Value**-Eigenschaft eines Felds in einem **Recordset**-Objekt, um gespeicherte Daten festzulegen oder zurückzugeben.

  - Verwenden Sie die Methoden **AppendChunk** und **GetChunk** sowie die **FieldSize**-Eigenschaft, um einen Wert in einem OLE-Objekt- oder Memofeld eines **Recordset**-Objekts abzurufen oder festzulegen.

  - Ermitteln Sie mit den Eigenschaften **Type**, **Size** und **Attributes**, welche Art Daten in einem Feld gespeichert werden können.

  - Ermitteln Sie mit den Eigenschaften **SourceField** und **SourceTable** die ursprüngliche Datenquelle.

  - Verwenden Sie die **ForeignName**-Eigenschaft, um Informationen zu einem fremden Feld in einem **Relation**-Objekt festzulegen oder zurückzugeben.

  - Verwenden Sie die Eigenschaften **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** oder **ValidationText**, um Gültigkeitsbedingungen festzulegen oder zurückzugeben.

  - Verwenden Sie die **DefaultValue**-Eigenschaft eines Felds für ein **TableDef**-Objekt, um den Standardwert beim Hinzfügen neuer Datensätze für dieses Feld festzulegen.

Verwenden Sie zum Erstellen eines neuen **Field**-Objekts in einem der Objekte **Index**, **TableDef** oder **Relation** die **CreateField**-Methode.

Wenn Sie auf ein **Field**-Objekt zugreifen, das Teil eines **Recordset**-Objekts ist, sind Daten aus dem aktuellen Datensatz in der **Value**-Eigenschaft des **Field**-Objekts sichtbar. In der Regel verweisen Sie zum Bearbeiten von Daten im **Recordset**-Objekt nicht direkt auf die **Fields**-Auflistung. Sie verweisen stattdessen indirekt auf die **Value**-Eigenschaft des **Field**-Objekts in der **Fields**-Auflistung des **Recordset**-Objekts.

Wenn Sie auf ein **Field**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:

- **Fields**(0)

- **Fields**("name")

- **Fields**\!\[name\]

Mit denselben Syntaxformen können Sie auch auf die **Value**-Eigenschaft eines von Ihnen erstellten **Field**-Objekts verweisen, das Sie einer **Fields**-Auflistung anfügen. Der Kontext des Feldverweises bestimmt, ob sich der Verweis auf das **Field**-Objekt oder die **Value**-Eigenschaft des **Field**-Objekts bezieht.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, welche Eigenschaften für ein **Field**-Objekt gültig sind, abhängig davon, wo sich das **Field**-Objekt befindet (z. B. **Fields**-Auflistung eines **TableDef**-Objekts, **Fields**-Auflistung eines **QueryDef**-Objekts usw.). Zum Ausführen dieser Prozedur ist die FieldOutput-Prozedur erforderlich.

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

In diesem Beispiel wird die **CreateField**-Methode zum Erstellen dreier **Fields**-Objekte für ein neues **TableDef**-Objekt verwendet. Anschließend werden die Eigenschaften der Field-Objekte angezeigt, die nicht automatisch von der **CreateField**-Methode festgelegt werden. (Eigenschaften, deren Werte zum Zeitpunkt der Erstellung des **Field**-Objekts leer sind, werden nicht gezeigt.)

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
