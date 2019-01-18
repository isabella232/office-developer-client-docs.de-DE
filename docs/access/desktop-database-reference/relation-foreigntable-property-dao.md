---
title: Relation.ForeignTable-Eigenschaft (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718973"
---
# <a name="relationforeigntable-property-dao"></a>Relation.ForeignTable-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Legt den Namen der Fremdtabelle in einer Beziehung fest oder gibt den Namen zurück (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . ForeignTable

*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Für diese Eigenschaft besteht bei einem neuen **[Relation](relation-object-dao.md)** -Objekt, das noch keiner Auflistung angefügt wurde, Lese-/Schreibzugriff, und bei einem vorhandenen **Relation**-Objekt in der **[Relations](relations-collection-dao.md)** -Auflistung ist sie schreibgeschützt.

Die Einstellung der **ForeignTable**-Eigenschaft eines **Relation**-Objekts ist die Einstellung der **[Name](connection-name-property-dao.md)** -Eigenschaft des **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekts, das die Fremdtabelle oder Abfrage darstellt. Die Einstellung der **[Table](relation-table-property-dao.md)** -Eigenschaft ist die Einstellung der **Name**-Eigenschaft des **TableDef**- oder **QueryDef**-Objekts, das die Primärtabelle oder Abfrage darstellt.

Angenommen, Sie besitzen eine Liste mit gültigen Artikelcodes (in einem Feld namens Artikelnr) in einer GültigeArtikel-Tabelle. Sie können dann eine Beziehung zu einer Bestellelement-Tabelle erstellen, sodass ein Artikelcode, der in der Bestellelement-Tabelle eingegeben wird, bereits in der GültigeArtikel-Tabelle vorhanden sein muss. Ist der Artikelcode nicht in der GültigeArtikel-Tabelle vorhanden, und Sie legen die Attributes-Eigenschaft des Relation-Objekts nicht auf dbRelationDontEnforce fest, tritt ein abfangbarer Fehler auf.

In diesem Fall ist die Tabelle Artikel der Primärtabelle, damit die **Table** -Eigenschaft des **Relation** -Objekts auf Artikel fest und "Bestellung" die **ForeignTable** -Eigenschaft des **Relation** -Objekts festgelegt werden würde. PartNo würde die Eigenschaften **Name** und **ForeignName** des **Field** -Objekts in **Fields** -Auflistung für das **Relation** -Objekt fest.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie die Eigenschaften **Table**, **ForeignTable** und **ForeignName** die Bedingungen eines **Relation**-Objekts zwischen zwei Tabellen definieren.

```vb 
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
