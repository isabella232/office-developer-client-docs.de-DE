---
title: Field.ForeignName-Eigenschaft (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7c340eee9972e8247654ec863ba0ef4588ef65f8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708466"
---
# <a name="fieldforeignname-property-dao"></a>Field.ForeignName-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Namen des **[Field](field-object-dao.md)** -Objekts in einer Fremdtabelle angibt, das einem Feld in einer Primärtabelle für eine Beziehung entspricht (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . ForeignName

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn das **[Relation](relation-object-dao.md)** -Objekt nicht dem **[Database](database-object-dao.md)** -Objekt sondern das **Field**-Objekt dem **Relation**-Objekt angefügt wird, ist die **ForeignName**-Eigenschaft nicht schreibgeschützt. Sobald das **Relation**-Objekt der Datenbank angefügt wurde, ist die **ForeignName**-Eigenschaft schreibgeschützt.

Nur ein **Field**-Objekt, das zur **Fields**-Auflistung eines **Relation**-Objekts gehört, kann die **ForeignName**-Eigenschaft unterstützten.

Die Einstellungen der Eigenschaften **[Name](connection-name-property-dao.md)** und **ForeignName** für ein **Field**-Objekt geben die Namen der entsprechenden Felder in den Primär- und Fremdtabellen einer Beziehung an. Die Einstellungen der Eigenschaften **[Table](relation-table-property-dao.md)** und **[ForeignTable](relation-foreigntable-property-dao.md)** für ein **Relation**-Objekt bestimmen die Primär- und Fremdtabellen einer Beziehung.

Angenommen, Sie besitzen eine Liste mit gültigen Artikelcodes (in einem Feld namens Artikelnr) in einer GültigeArtikel-Tabelle. Sie können dann eine Beziehung zu einer Bestellelement-Tabelle erstellen, sodass ein Artikelcode, der in der Bestellelement-Tabelle eingegeben wird, bereits in der GültigeArtikel-Tabelle vorhanden sein muss. Ist der Artikelcode nicht in der GültigeArtikel-Tabelle vorhanden, und Sie legen die Attributes-Eigenschaft des Relation-Objekts nicht auf dbRelationDontEnforce fest, tritt ein abfangbarer Fehler auf.

In diesem Fall ist die GültigeArtikel-Tabelle die Fremdtabelle, deshalb wird die ForeignTable-Eigenschaft des Relation-Objekts auf GültigeArtikel und die Table-Eigenschaft des Relation-Objekts auf Bestellelement festgelegt. Die Eigenschaften Name und ForeignName des Field-Objekts in der Fields-Auflistung des Relation-Objekts werden auf Artikelnr festgelegt.

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
