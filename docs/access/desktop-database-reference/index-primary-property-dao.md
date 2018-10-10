---
title: Index.Primary Property (DAO)
TOCTitle: Primary Property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2d551b60919b1fb3d48c7ac75bbf7c6183aee04d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476162"
---
# <a name="indexprimary-property-dao"></a>Index.Primary Property (DAO)


**Betrifft**: Access 2013 | Office 2013


Legt einen Wert fest, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen Primärschlüsselindex für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Primäre

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein neues **Index**-Objekt, das noch nicht an eine Auflistung angehängt wurde, hat den Lese-/Schreibzugriff für die **Primary**-Eigenschaft. Für ein vorhandenes **Index**-Objekt in einer **[Indexes](indexes-collection-dao.md)** -Auflistung ist die Eigenschaft schreibgeschützt. Wenn das **Index**-Objekt an das **[TableDef](tabledef-object-dao.md)** -Objekt angehängt wurde, aber das **TableDef**-Objekt nicht an die **[TableDefs](tabledefs-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für die **Index**-Eigenschaft.

Ein Primärschlüsselindex besteht aus einem oder mehreren Feldern, die alle Datensätze in einer Tabelle in einer vordefinierten Reihenfolge eindeutig identifizieren. Da das Indexfeld eindeutig sein muss, wird die **[Unique](index-unique-property-dao.md)** -Eigenschaft des **Index**-Objekts auf **True** festgelegt. Wenn der Primärschlüsselindex aus mehreren Feldern besteht, kann jedes Feld Duplikatwerte enthalten. Jede Kombination von Werten aus den indizierten Feldern muss jedoch eindeutig sein. Ein Primärschlüsselindex besteht aus einem Schlüssel für die Tabelle und enthält gewöhnlich dieselben Felder wie der Primärschlüssel.


> [!NOTE]
> <P>[!HINWEIS] Sie müssen keine Indizes für Tabellen erstellen, doch in großen, nicht-indizierten Tabellen kann der Zugriff auf einen Datensatz einige Zeit in Anspruch nehmen. Die <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> -Eigenschaft der einzelnen <STRONG><A href="field-object-dao.md">Field</A></STRONG> -Objekte im <STRONG>Index</STRONG>-Objekt legt die Reihenfolge der Datensätze fest und bestimmt daher die für den betreffenden Index zu verwendenden Zugriffsverfahren. Wenn Sie in Ihrer Datenbank eine neue Tabelle erstellen, sollten Sie einen Index mit einem oder mehreren Feldern erstellen, der jeden Datensatz eindeutig identifiziert, und anschließend die <STRONG>Primary</STRONG>-Eigenschaft des <STRONG>Index</STRONG>-Objekts auf <STRONG>True</STRONG> festlegen.</P>



Wenn Sie einen Primärschlüssel für eine Tabelle festlegen, wird der Primärschlüssel automatisch als Primärschlüsselindex für die Tabelle definiert.

## <a name="example"></a>Beispiel

In diesem Beispiel wird mithilfe der **Primary**-Eigenschaft ein neues **Index**-Objekt in einem neuen **TableDef**-Objekt als primärer **Index** für die Tabelle festgelegt. Beachten Sie, dass beim Festlegen der **Primary**-Eigenschaft auf **True** die Eigenschaften **Unique** und **Required** automatisch auf **True** gesetzt werden.

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
