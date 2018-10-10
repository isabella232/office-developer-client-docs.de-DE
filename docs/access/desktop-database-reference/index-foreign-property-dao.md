---
title: Index.Foreign Property (DAO)
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
ms.openlocfilehash: 410629c3e5ebec47dd8acefd852379ee74568832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474377"
---
# <a name="indexforeign-property-dao"></a>Index.Foreign Property (DAO)

**Betrifft**: Access 2013 | Office 2013

Gibt einen Wert zurück, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen Fremdschlüssel in einer Tabelle angibt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Fremdschlüssel

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist vom Datentyp **Boolean** und gibt **True** zurück, wenn das **Index**-Objekt ein Fremdschlüssel ist.

Ein Fremdschlüssel besteht aus einem oder mehreren Feldern in einer Fremdtabelle, die alle Zeilen in einer Primärtabelle eindeutig identifizieren.

Das Microsoft Access-Datenbankmodul erstellt ein **Index**-Objekt für die Fremdtabelle und legt die **Foreign**-Eigenschaft fest, wenn Sie eine Beziehung erstellen, die die referentielle Integrität erzwingt.

## <a name="example"></a>Beispiel

Dieses Beispiel veranschaulicht, wie mit der Foreign-Eigenschaft angeben werden kann, bei welchen Index-Objekten in einem TableDef-Objekt es sich um Fremdschlüsselindizes handelt. Diese Indizes werden beim Erstellen eines Relation-Objekts vom Microsoft Access-Datenbankmodul erstellt. Der Standardname für die Fremdschlüsselindizes setzt sich aus dem Namen der Primärtabelle und dem Namen der Fremdtabelle zusammen. Zum Ausführen dieser Prozedur ist die ForeignOutput-Funktion erforderlich.

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
