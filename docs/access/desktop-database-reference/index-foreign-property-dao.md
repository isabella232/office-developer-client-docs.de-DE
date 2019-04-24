---
title: Index. Foreign-Eigenschaft (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a3c6adfaf9648147a763f997ce2a91aadc4f7637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291817"
---
# <a name="indexforeign-property-dao"></a>Index. Foreign-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen Fremdschlüssel in einer Tabelle darstellt (nur Microsoft Access-Arbeitsbereiche). .

## <a name="syntax"></a>Syntax

*Ausdruck* . Außen

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist vom Datentyp **Boolean** und gibt **True** zurück, wenn das **Index**-Objekt ein Fremdschlüssel ist.

Ein Fremdschlüssel besteht aus einem oder mehreren Feldern in einer Fremdtabelle, die alle Zeilen in einer Primärtabelle eindeutig identifizieren.

Das Microsoft Access-Datenbankmodul erstellt ein **Index**-Objekt für die Fremdtabelle und legt die **Foreign**-Eigenschaft fest, wenn Sie eine Beziehung erstellen, die die referentielle Integrität erzwingt.

## <a name="example"></a>Beispiel

This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes. Such indexes are created by the Microsoft Access database engine when a **Relation** is created. The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table. The ForeignOutput function is required for this procedure to run.

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
