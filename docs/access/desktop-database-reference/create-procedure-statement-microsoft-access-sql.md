---
title: CREATE PROCEDURE-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295402"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="b0ab8-102">CREATE PROCEDURE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b0ab8-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b0ab8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0ab8-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="b0ab8-104">Erstellt eine gespeicherte Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="b0ab8-105">Vom Microsoft Access-Datenbankmodul wird die Verwendung der CREATE PROCEDURE- oder anderer DDL-Anweisungen in Datenbanken, die nicht aus dem Microsoft Jet-Datenbankmodul stammen, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ab8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0ab8-106">Syntax</span></span>

<span data-ttu-id="b0ab8-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span><span class="sxs-lookup"><span data-stu-id="b0ab8-107">CREATE PROCEDURE procedure
    [param1 datatype[, param2 datatype[, …]] AS sqlstatement</span></span>

<span data-ttu-id="b0ab8-108">Die CREATE PROCEDURE-Anweisung setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="b0ab8-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="b0ab8-109">Part</span><span class="sxs-lookup"><span data-stu-id="b0ab8-109">Part</span></span>|<span data-ttu-id="b0ab8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0ab8-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="b0ab8-111">*Prozedur*</span><span class="sxs-lookup"><span data-stu-id="b0ab8-111">*procedure*</span></span>|<span data-ttu-id="b0ab8-112">Der Name der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-112">A name for the procedure.</span></span> <span data-ttu-id="b0ab8-113">Bei der Namensgebung müssen die Standardbenennungsregeln beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-113">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="b0ab8-114">*Parameter1*, *Parameter2*</span><span class="sxs-lookup"><span data-stu-id="b0ab8-114">*param1*, *param2*</span></span>|<span data-ttu-id="b0ab8-115">1 bis 255 Feldnamen oder Parameter.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-115">From one to 255 field names or parameters.</span></span> <span data-ttu-id="b0ab8-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b0ab8-116">For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="b0ab8-117">Weitere Informationen zu Parametern finden Sie unter [PARAMETER](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="b0ab8-117">For more information on parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="b0ab8-118">*Datentyp*</span><span class="sxs-lookup"><span data-stu-id="b0ab8-118">*datatype*</span></span>|<span data-ttu-id="b0ab8-119">Einer der wichtigsten [Microsoft Access SQL-Datentypen](sql-data-types.md) oder eines der Synonyme.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="b0ab8-120">*SQL-Anweisung*</span><span class="sxs-lookup"><span data-stu-id="b0ab8-120">*SQLStatement*</span></span>|<span data-ttu-id="b0ab8-121">Eine SQL-Anweisung wie SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE usw.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="b0ab8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0ab8-122">Remarks</span></span>

<span data-ttu-id="b0ab8-123">Eine SQL-Prozedur besteht aus einer PROCEDURE-Klausel,die den Namen der Prozedur angibt, einer optionalen Liste von Parameterdefinitionen und einer einzelnen SQL-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="b0ab8-124">Der Name der Prozedur darf nicht mit dem Namen einer vorhandenen Tabelle übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="b0ab8-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0ab8-125">Example</span></span>

<span data-ttu-id="b0ab8-126">In diesem Beispiel wird die CategoryList-Abfrage benannt und die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b0ab8-126">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
