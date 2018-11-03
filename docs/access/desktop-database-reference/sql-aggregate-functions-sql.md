---
title: SQL-Aggregatfunktionen (SQL)
TOCTitle: SQL aggregate functions (SQL)
ms:assetid: 8866cd71-0216-25b4-6a6a-02cb7acad9a2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197054(v=office.15)
ms:contentKeyID: 48546136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 946afd4ad9c1a2976e4833b59fa8467911ac1c56
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945978"
---
# <a name="sql-aggregate-functions-sql"></a><span data-ttu-id="4f63f-102">SQL-Aggregatfunktionen (SQL)</span><span class="sxs-lookup"><span data-stu-id="4f63f-102">SQL aggregate functions (SQL)</span></span>


<span data-ttu-id="4f63f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f63f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f63f-p101">Mithilfe der SQL-Aggregatfunktionen können Sie verschiedene Statistiken zu Wertgruppen ermitteln. Sie können diese Funktionen in einer Abfrage und in Aggregatausdrücken in der **SQL** -Eigenschaft eines **QueryDef** -Objekts verwenden, wenn Sie ein **Recordset** -Objekt basierend auf einer SQL-Abfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f63f-p101">Using the SQL aggregate functions, you can determine various statistics on sets of values. You can use these functions in a query and aggregate expressions in the **SQL** property of a **QueryDef** object or when creating a **Recordset** object based on an SQL query.</span></span>

- <span data-ttu-id="4f63f-106">[AVG-Funktion](https://msdn.microsoft.com/library/ff822755\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4f63f-106">[Avg function](https://msdn.microsoft.com/library/ff822755\(v=office.15\))</span></span>

- <span data-ttu-id="4f63f-107">[Count-Funktion](https://msdn.microsoft.com/library/ff844748\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4f63f-107">[Count function](https://msdn.microsoft.com/library/ff844748\(v=office.15\))</span></span>

- <span data-ttu-id="4f63f-108">[First-und Last](https://msdn.microsoft.com/library/ff197381\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4f63f-108">[First, Last functions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))</span></span>

- <span data-ttu-id="4f63f-109">[Min-Funktion und Max-Funktion](https://msdn.microsoft.com/library/ff194490\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4f63f-109">[Min, Max functions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))</span></span>

- <span data-ttu-id="4f63f-110">[StDev-Funktion, StDevP-Funktion](https://msdn.microsoft.com/library/ff197043\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4f63f-110">[StDev, StDevP functions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))</span></span>

- <span data-ttu-id="4f63f-111">[SUM-Funktion](https://msdn.microsoft.com/library/ff844764\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4f63f-111">[Sum function](https://msdn.microsoft.com/library/ff844764\(v=office.15\))</span></span>

- <span data-ttu-id="4f63f-112">[Var-Funktion, VarP-Funktion](https://msdn.microsoft.com/library/ff192105\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="4f63f-112">[Var, VarP functions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))</span></span>

