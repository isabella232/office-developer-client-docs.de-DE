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
# <a name="indexforeign-property-dao"></a><span data-ttu-id="bc60d-102">Index.Foreign Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="bc60d-102">Index.Foreign Property (DAO)</span></span>

<span data-ttu-id="bc60d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc60d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bc60d-p101">Gibt einen Wert zurück, der angibt, ob ein **[Index](index-object-dao.md)** -Objekt einen Fremdschlüssel in einer Tabelle angibt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="bc60d-p101">Returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="bc60d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc60d-106">Syntax</span></span>

<span data-ttu-id="bc60d-107">*Ausdruck* . Fremdschlüssel</span><span class="sxs-lookup"><span data-stu-id="bc60d-107">*expression* .Foreign</span></span>

<span data-ttu-id="bc60d-108">*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc60d-108">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc60d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc60d-109">Remarks</span></span>

<span data-ttu-id="bc60d-110">Der Rückgabewert ist vom Datentyp **Boolean** und gibt **True** zurück, wenn das **Index**-Objekt ein Fremdschlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="bc60d-110">The return value is a **Boolean** data type that returns **True** if the **Index** object represents a foreign key.</span></span>

<span data-ttu-id="bc60d-111">Ein Fremdschlüssel besteht aus einem oder mehreren Feldern in einer Fremdtabelle, die alle Zeilen in einer Primärtabelle eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bc60d-111">A foreign key consists of one or more fields in a foreign table that uniquely identify all rows in a primary table.</span></span>

<span data-ttu-id="bc60d-112">Das Microsoft Access-Datenbankmodul erstellt ein **Index**-Objekt für die Fremdtabelle und legt die **Foreign**-Eigenschaft fest, wenn Sie eine Beziehung erstellen, die die referentielle Integrität erzwingt.</span><span class="sxs-lookup"><span data-stu-id="bc60d-112">The Microsoft Access database engine creates an **Index** object for the foreign table and sets the **Foreign** property when you create a relationship that enforces referential integrity.</span></span>

## <a name="example"></a><span data-ttu-id="bc60d-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bc60d-113">Example</span></span>

<span data-ttu-id="bc60d-p102">Dieses Beispiel veranschaulicht, wie mit der Foreign-Eigenschaft angeben werden kann, bei welchen Index-Objekten in einem TableDef-Objekt es sich um Fremdschlüsselindizes handelt. Diese Indizes werden beim Erstellen eines Relation-Objekts vom Microsoft Access-Datenbankmodul erstellt. Der Standardname für die Fremdschlüsselindizes setzt sich aus dem Namen der Primärtabelle und dem Namen der Fremdtabelle zusammen. Zum Ausführen dieser Prozedur ist die ForeignOutput-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc60d-p102">This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes. Such indexes are created by the Microsoft Access database engine when a **Relation** is created. The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table. The ForeignOutput function is required for this procedure to run.</span></span>

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
