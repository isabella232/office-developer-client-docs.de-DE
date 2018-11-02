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
ms.openlocfilehash: 85d0ceec1cea782a8e43a2bebd6779841c2a56ff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926108"
---
# <a name="indexunique-property-dao"></a>Index.Unique-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen eindeutigen Index (Schlüssel) für eine Tabelle darstellt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Eindeutige

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Es besteht Lese-/Schreibzugriff für den Wert dieser Eigenschaft, bis das Objekt an eine Auflistung angefügt wird. Ab diesem Zeitpunkt ist die Eigenschaft schreibgeschützt.

Ein eindeutiger Index besteht aus einem oder mehreren Feldern, die alle Datensätze in einer Tabelle in einer eindeutigen, vordefinierten Reihenfolge logisch anordnen. Wenn der Index aus einem Feld besteht, müssen die Werte in diesem Feld für die gesamte Tabelle eindeutig sein. Wenn der Index aus mehreren Feldern besteht, kann jedes Feld doppelte Werte enthalten, doch jede Kombination der Werte der indizierten Felder muss eindeutig sein.

Wenn sowohl die **Unique**- als auch die **[Primary](index-primary-property-dao.md)** -Eigenschaft eines **Index**-Objekts den Wert **True** hat, ist der Index eindeutig und primär, d. h. er identifiziert alle Datensätze in der Tabelle in einer vordefinierten, logischen Reihenfolge eindeutig. Wenn die **Primary**-Eigenschaft den Wert **False** hat, ist der Index ein sekundärer Index. Sekundäre Indizes (Schlüssel- als auch Nicht-Schlüsselindizes) ordnen Datensätze in einer vordefinierten Weise logisch an, ohne als Bezeichner für Datensätze in der Tabelle zu dienen.


> [!NOTE]
> <UL>
> <LI>
> <P>Sie müssen keine Indizes für Tabellen erstellen, doch in großen, nicht-indizierten Tabellen kann der Zugriff auf einen Datensatz einige Zeit in Anspruch nehmen.</P>
> <LI>
> <P>Datensätze, die aus Tabellen ohne Indizes abgerufen werden, werden in einer unbestimmten Reihenfolge zurückgegeben.</P>
> <LI>
> <P>Die <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> -Eigenschaft der einzelnen <STRONG><A href="field-object-dao.md">Field</A></STRONG> -Objekte im <STRONG>Index</STRONG>-Objekt legt die Reihenfolge der Datensätze fest und bestimmt daher das für das betreffende <STRONG>Index</STRONG>-Objekt zu verwendende Zugriffsverfahren.</P>
> <LI>
> <P>Mithilfe eines eindeutigen Indexes wird die Suche nach Datensätzen optimiert.</P>
> <LI>
> <P>Indizes haben keine Auswirkung auf die physikalische Anordnung von Basistabellen. Sie wirken sich jedoch darauf aus, wie auf die Datensätze vom Recordset-Objekt vom Typ Tabelle zugegriffen wird, wenn ein bestimmter Index gewählt wird oder wenn die Microsoft Access-Datenbank-Engine Recordset-Objekte erstellt.</P></LI></UL>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die Unique-Eigenschaft eines neuen Index-Objekts auf den Wert True festgelegt, und der Index wird an die Indexes-Auflistung der Employees-Tabelle angefügt. Anschließend werden die Indexes-Auflistung des TableDef-Objekts und die Properties-Auflistungen aller Index-Objekte in einer Schleife durchlaufen. Das neue Index-Objekt lässt nur einen Datensatz mit einer bestimmten Kombination der Werte von Country, LastName und FirstName im TableDef-Objekt zu.

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
