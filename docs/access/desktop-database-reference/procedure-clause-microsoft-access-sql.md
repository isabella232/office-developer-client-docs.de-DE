---
title: PROCEDURE-Klausel (Microsoft Access SQL)
TOCTitle: PROCEDURE Clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 63b38a469c5de60588783381c24c61296b177bdd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877989"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="0ae1f-102">PROCEDURE-Klausel (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="0ae1f-102">PROCEDURE Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="0ae1f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ae1f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ae1f-104">Definiert einen Namen und optionale Parameter für eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="0ae1f-p101">[!HINWEIS] Die PROCEDURE-Klausel wurde durch die PROCEDURE-Anweisung abgelöst. Zwar wird die PROCEDURE-Klausel noch unterstützt, doch die PROCEDURE-Anweisung stellt eine Übermenge der Funktionen der PROCEDURE-Klausel bereit und wird als Syntax empfohlen.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-p101">The PROCEDURE clause has been superseded by the PROCEDURE statement. Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ae1f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ae1f-107">Syntax</span></span>

<span data-ttu-id="0ae1f-108">*Name* der Prozedur \[ *param1 Datentyp*\[, *param2 Datentyp*\[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="0ae1f-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="0ae1f-109">Die PROCEDURE-Klausel enthält die folgenden Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="0ae1f-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="0ae1f-110">Argument</span><span class="sxs-lookup"><span data-stu-id="0ae1f-110">Part</span></span> |<span data-ttu-id="0ae1f-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ae1f-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="0ae1f-112">*name*</span><span class="sxs-lookup"><span data-stu-id="0ae1f-112">*name*</span></span> |<span data-ttu-id="0ae1f-p102">Ein Name für die Prozedur. Bei der Namensgebung müssen die Standardbenennungsregeln beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-p102">A name for the procedure. It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="0ae1f-115">*Param1*, *Param2*</span><span class="sxs-lookup"><span data-stu-id="0ae1f-115">*param1*, *param2*</span></span> |<span data-ttu-id="0ae1f-p103">Ein oder mehrere Feldnamen oder Parameter. Beispiel:
</span><span class="sxs-lookup"><span data-stu-id="0ae1f-p103">One or more field names or parameters. For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="0ae1f-118">Weitere Informationen zu Parametern finden Sie unter [Parameter](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="0ae1f-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="0ae1f-119">*Datentyp*</span><span class="sxs-lookup"><span data-stu-id="0ae1f-119">*datatype*</span></span> | <span data-ttu-id="0ae1f-120">Einer der wichtigsten [Microsoft Access SQL-Datentypen](sql-data-types.md) oder eines der Synonyme.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="0ae1f-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0ae1f-121">Remarks</span></span>

<span data-ttu-id="0ae1f-122">Eine SQL-Prozedur besteht aus einer PROCEDURE-Klausel (die den Namen der Prozedur angibt), einer optionalen Liste mit Parameterdefinitionen und einer einzelnen SQL­Anweisung.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="0ae1f-123">Das Verfahren Get\_Teil\_Anzahl möglicherweise führen Sie eine Abfrage, die eine angegebene Teilenummer abruft.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="0ae1f-124">Wenn die Klausel mehr als eine Felddefinition (d. h., *Param-Datentyp* -Paare) enthält, müssen Sie diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="0ae1f-125">Auf die PROCEDURE-Klausel muss eine SQL-Anweisung folgen (z. B. eine [SELECT](select-statement-microsoft-access-sql.md)- oder eine [UPDATE](update-statement-microsoft-access-sql.md)-Anweisung).</span><span class="sxs-lookup"><span data-stu-id="0ae1f-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="0ae1f-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ae1f-126">Example</span></span>

<span data-ttu-id="0ae1f-127">In diesem Beispiel wird die Abfrage categoryList verwendet, und es wird die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.</span><span class="sxs-lookup"><span data-stu-id="0ae1f-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
