---
title: SQL-Aggregatfunktionen (SQL)
TOCTitle: SQL Aggregate Functions (SQL)
ms:assetid: 8866cd71-0216-25b4-6a6a-02cb7acad9a2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197054(v=office.15)
ms:contentKeyID: 48546136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fd06b02d4331a51e0f8a186f713d80d98bbed20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870562"
---
# <a name="sql-aggregate-functions-sql"></a><span data-ttu-id="d9cde-102">SQL-Aggregatfunktionen (SQL)</span><span class="sxs-lookup"><span data-stu-id="d9cde-102">SQL Aggregate Functions (SQL)</span></span>


<span data-ttu-id="d9cde-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9cde-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9cde-p101">Mithilfe der SQL-Aggregatfunktionen können Sie verschiedene Statistiken zu Wertgruppen ermitteln. Sie können diese Funktionen in einer Abfrage und in Aggregatausdrücken in der **SQL** -Eigenschaft eines **QueryDef** -Objekts verwenden, wenn Sie ein **Recordset** -Objekt basierend auf einer SQL-Abfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="d9cde-p101">Using the SQL aggregate functions, you can determine various statistics on sets of values. You can use these functions in a query and aggregate expressions in the **SQL** property of a **QueryDef** object or when creating a **Recordset** object based on an SQL query.</span></span>

<span data-ttu-id="d9cde-106">**[Avg-Funktion](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="d9cde-106">**[Avg Function](https://msdn.microsoft.com/library/ff822755\(v=office.15\))**</span></span>

<span data-ttu-id="d9cde-107">**[Count-Funktion](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="d9cde-107">**[Count Function](https://msdn.microsoft.com/library/ff844748\(v=office.15\))**</span></span>

<span data-ttu-id="d9cde-108">**[First-, Last-Funktionen](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="d9cde-108">**[First, Last Functions](https://msdn.microsoft.com/library/ff197381\(v=office.15\))**</span></span>

<span data-ttu-id="d9cde-109">**[Min-, Max-Funktionen](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="d9cde-109">**[Min, Max Functions](https://msdn.microsoft.com/library/ff194490\(v=office.15\))**</span></span>

<span data-ttu-id="d9cde-110">**[StDev-, StDevP-Funktionen](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="d9cde-110">**[StDev, StDevP Functions](https://msdn.microsoft.com/library/ff197043\(v=office.15\))**</span></span>

<span data-ttu-id="d9cde-111">**[Sum-Funktion](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="d9cde-111">**[Sum Function](https://msdn.microsoft.com/library/ff844764\(v=office.15\))**</span></span>

<span data-ttu-id="d9cde-112">**[Var-, VarP-Funktionen](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="d9cde-112">**[Var, VarP Functions](https://msdn.microsoft.com/library/ff192105\(v=office.15\))**</span></span>

