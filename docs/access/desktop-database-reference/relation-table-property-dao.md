---
title: Relation.Table Property (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ba1c70a9aded0ce26cd24d2dc25ecb65c30b1f8e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474688"
---
# <a name="relationtable-property-dao"></a>Relation.Table Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Namen der Primärtabelle eines **[Relation](relation-object-dao.md)** -Objekts an. Dieser Name sollte mit dem Wert der **[Name](connection-name-property-dao.md)** -Eigenschaft eines **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekts übereinstimmen (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Tabelle

*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ein neues **Relation**-Objekt, das noch an keine Auflistung angefügt wurde, hat Lese-/Schreibzugriff auf den Wert der **Table**-Eigenschaft. Für ein vorhandenes **Relation**-Objekt in einer **[Relations](relations-collection-dao.md)** -Auflistung ist die Eigenschaft schreibgeschützt.

Verwenden Sie die **Table**-Eigenschaft zusammen mit der **[ForeignTable](relation-foreigntable-property-dao.md)** -Eigenschaft, um ein **Relation**-Objekt zu definieren, das die Beziehung zwischen Feldern in zwei Tabellen oder Abfragen darstellt. Legen Sie die **Table**-Eigenschaft auf den Wert der **Name**-Eigenschaft des **TableDef**- oder **QueryDef**-Objekts der Primärtabelle fest und die **ForeignTable**-Eigenschaft auf den Wert der **Name**-Eigenschaft des verweisenden **TableDef**- oder **QueryDef**-Objekts der Fremdtabelle. Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft bestimmt den Typ der Beziehung zwischen den beiden Objekten.

Wenn Sie z. B. eine Liste gültiger Teilecodes (in einem Feld namens PartNo) in der Tabelle ValidParts gespeichert haben, könnten Sie eine 1:n-Beziehung mit einer Tabelle namens OrderItem einrichten. Wenn ein Teilecode in die Tabelle OrderItem eingegeben wird, muss dieser bereits in der Tabelle ValidParts vorhanden sein. Wenn der Teilecode in der Tabelle ValidParts nicht vorhanden ist und Sie die Attributes-Eigenschaft des Relation-Objekts nicht auf den Wert dbRelationDontEnforce festgelegt haben, tritt ein auffangbarer Fehler auf.

In diesem Fall ist die Tabelle ValidParts die Primärtabelle, sodass die Table-Eigenschaft des Relation-Objekts auf den Wert ValidParts und die ForeignTable-Eigenschaft des Relation-Objekts auf OrderItem festgelegt wird. Die Eigenschaften Name und ForeignName des Field-Objekts in der Fields-Auflistung des Relation-Objekts werden dann auf PartNo gesetzt.

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
