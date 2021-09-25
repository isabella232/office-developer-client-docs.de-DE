---
title: Index.Unique-Eigenschaft (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 45428f15c0bca259703e0f95fb7ad8693d841044
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615340"
---
# <a name="indexunique-property-dao"></a>Index.Unique-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen eindeutigen Index (Schlüssel) für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Einzigartige

*Ausdruck* Eine Variable, die ein **Index-Objekt** darstellt.

## <a name="remarks"></a>Bemerkungen

Es besteht Lese-/Schreibzugriff für den Wert dieser Eigenschaft, bis das Objekt an eine Auflistung angefügt wird. Ab diesem Zeitpunkt ist die Eigenschaft schreibgeschützt.

Ein eindeutiger Index besteht aus einem oder mehreren Feldern, die alle Datensätze in einer Tabelle in einer eindeutigen, vordefinierten Reihenfolge logisch anordnen. Wenn der Index aus einem Feld besteht, müssen die Werte in diesem Feld für die gesamte Tabelle eindeutig sein. Wenn der Index aus mehreren Feldern besteht, kann jedes Feld doppelte Werte enthalten, doch jede Kombination der Werte der indizierten Felder muss eindeutig sein.

Wenn sowohl die **Unique**- als auch die **[Primary](index-primary-property-dao.md)** -Eigenschaft eines **Index**-Objekts den Wert **True** hat, ist der Index eindeutig und primär, d. h. er identifiziert alle Datensätze in der Tabelle in einer vordefinierten, logischen Reihenfolge eindeutig. Wenn die **Primary**-Eigenschaft den Wert **False** hat, ist der Index ein sekundärer Index. Sekundäre Indizes (Schlüssel- als auch Nicht-Schlüsselindizes) ordnen Datensätze in einer vordefinierten Weise logisch an, ohne als Bezeichner für Datensätze in der Tabelle zu dienen.

> [!NOTE]
> - Sie müssen keine Indizes für Tabellen erstellen, doch in großen, nicht-indizierten Tabellen kann der Zugriff auf einen Datensatz einige Zeit in Anspruch nehmen.
> - Datensätze, die aus Tabellen ohne Indizes abgerufen werden, werden in einer unbestimmten Reihenfolge zurückgegeben.
> - Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft der einzelnen **[Field](field-object-dao.md)** -Objekte im **Index**-Objekt legt die Reihenfolge der Datensätze fest und bestimmt daher das für das betreffende **Index**-Objekt zu verwendende Zugriffsverfahren.
> - Mithilfe eines eindeutigen Indexes wird die Suche nach Datensätzen optimiert.
> - Indizes wirken sich nicht auf die physische Reihenfolge einer Basistabelle aus. Indizes wirken sich nur darauf aus, wie das **[Recordset-Objekt](recordset-object-dao.md)** vom Tabellentyp auf die Datensätze zugreift, wenn ein bestimmter Index ausgewählt wird oder wenn das Microsoft Access-Datenbankmodul **Recordset-Objekte** erstellt.

## <a name="example"></a>Beispiel

This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table. It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**. The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
