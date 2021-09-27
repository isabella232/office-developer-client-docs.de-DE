---
title: Field.Attributes-Eigenschaft (DAO)
TOCTitle: Attributes Property
description: Attributes-Eigenschaft
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/14/2021
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 77cae4e2d4c3a09d75afa3c9f2228f72bccfd5d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626757"
---
# <a name="fieldattributes-property-dao"></a>Field.Attributes-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest oder gibt einen Wert zurück, der ein oder mehrere Merkmale eines **[Feld](field-object-dao.md)**-Objekts angibt. Lese-/Schreibzugriff **Lang**.

## <a name="syntax"></a>Syntax

*expression* .Attributes

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **Attributes** -Eigenschaft eines **Feld** -Objekts gibt die Merkmale des Feldes an, das durch das **Feld** -Objekt dargestellt wird. Die **Attributes-Eigenschaft** wird als einzelne lange ganze Zahl gespeichert und ist die Summe der folgenden Long -Konstanten:


|**Konstante**|**Wert**|**Beschreibung**|
|:----------|:----------|:----------|
|**dbAutoIncrField**|**16**|Der Feldwert für neue Datensätze wird automatisch auf einen eindeutigen Long Integer-Wert erhöht, der nicht geändert werden kann (wird in einem Microsoft Access-Arbeitsbereich nur bei Microsoft Access-Datenbanktabellen unterstützt).|
|**dbDescending**|**1**|Das Feld wird in absteigender Reihenfolge sortiert (von Z bis A oder von 100 bis 0). Diese Option trifft nur auf ein <strong>Feld</strong>-Objekt in einer <strong>Feld</strong>-Auflistung eines <strong>Index</strong>-Objekts zu. Wenn Sie diese Konstante auslassen, wird das Feld in aufsteigender Reihenfolge sortiert (von A bis Z oder von 0 bis 100). Das ist der Standardwert für <strong>Index</strong>- und <strong>TableDef</strong>-Felder (gilt nur für Microsoft Access-Arbeitsbereiche)..|
|**dbFixedField**|**1**|Die Feldgröße ist fest (Standard bei numerischen Feldern).|
|**dbHyperlinkField**|**32768**
|Das Feld enthält Hyperlinkinformationen (nur Memofelder).|
|**dbSystemField**|**8192**|Das Feld speichert Replikationsinformationen für Replikate. Dieser Typ von Feld kann nicht gelöscht werden (nur Microsoft Access-Arbeitsbereich).|
|**dbUpdatableField**|**32**|Der Wert des Felds kann geändert werden.|
|**dbVariableField**|**2**|Die Feldgröße ist variabel (nur Textfelder).\

Bei Objekten, die noch keiner Auflistung angefügt sind, besteht für diese Eigenschaft Lese-/Schreibzugriff. Bei einem angefügten **Field**-Objekt hängt die Verfügbarkeit der **Attributes**-Eigenschaft vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist.

|**Wenn das Field-Objekt zu einem** gehört|**Dann ist Attribute**|
|:----------|:----------|
|**Index** -Objekt|Lese-/Schreibzugriff, bis das **TableDef**-Objekt, an das das **Index**-Objekt angefügt ist, an ein **Database**-Objekt angefügt wird; die Eigenschaft ist dann schreibgeschützt.|
|**QueryDef** -Objekt|Schreibgeschützt|
|**Recordset** -Objekt|Schreibgeschützt|
|**Relation** -Objekt|Nicht unterstützt|
|**TableDef** -Objekt|Lesen/Schreiben|

Wenn Sie mehrere Attribute festlegen, können Sie sie kombinieren, indem Sie die entsprechenden Konstanten addieren. Ungültige Werte werden ohne Auftreten eines Fehlers ignoriert.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Attributes**-Eigenschaft für **Field**-, **Relation**- und **TableDef**-Objekte in der Northwind-Datenbank angezeigt.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

