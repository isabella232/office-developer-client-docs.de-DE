---
title: Vergleich von Microsoft Access SQL und ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd5350248c33b344695a02020b4b91bdbb1bb984
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937176"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="7e86c-102">Vergleich von Microsoft Access SQL und ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="7e86c-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>


<span data-ttu-id="7e86c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e86c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e86c-104">Das Microsoft Access-Datenbankmodul SQL ist im Allgemeinen mit ANSI-89 Level 1 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7e86c-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="7e86c-105">Bestimmte ANSI SQL-Features sind jedoch nicht in Microsoft Access SQL implementiert.</span><span class="sxs-lookup"><span data-stu-id="7e86c-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="7e86c-106">Umgekehrt umfasst Microsoft Access SQL reservierte Wörter und Features, die nicht in ANSI SQL unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7e86c-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="7e86c-107">Hauptunterschiede</span><span class="sxs-lookup"><span data-stu-id="7e86c-107">Major Differences</span></span>

  - <span data-ttu-id="7e86c-p102">Microsoft Access SQL und ANSI SQL verfügen über unterschiedliche reservierte Wörter und Datentypen. Weitere Informationen finden Sie unter [Reservierte Wörter für das Microsoft Access-Datenbankmodul SQL](sql-reserved-words.md) und [Gleichwertige ANSI SQL-Datentypen](equivalent-ansi-sql-data-types.md). Bei der Verwendung des OLE DB-Anbieters für das Microsoft Office 12.0 Access-Datenbankmodul sind zusätzliche reservierte Wörter vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7e86c-p102">Microsoft Access SQL and ANSI SQL each have different reserved words and data types. For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md). Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

  - <span data-ttu-id="7e86c-111">**[Between…And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**</span><span class="sxs-lookup"><span data-stu-id="7e86c-111">**[Between…And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**</span></span>
    
    <span data-ttu-id="7e86c-112">*expr1* \[Nicht\] **zwischen** *Wert1* **und** *Wert2*</span><span class="sxs-lookup"><span data-stu-id="7e86c-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
    <span data-ttu-id="7e86c-113">In Microsoft Access SQL kann *Wert1* größer sein als *Wert2*. In ANSI SQL dagegen muss *Wert1* kleiner oder gleich *Wert2* sein.</span><span class="sxs-lookup"><span data-stu-id="7e86c-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

  - <span data-ttu-id="7e86c-p103">Microsoft Access SQL unterstützt ANSI SQL-Platzhalterzeichen und [Platzhalterzeichen](using-wildcard-characters-in-string-comparisons.md), die speziell für das Microsoft Access-Datenbankmodul in Kombination mit dem **[Wie](https://msdn.microsoft.com/library/ff195752\(v=office.15\))** -Operator verwendet werden. Die Verwendung der ANSI-Platzhalterzeichen und der Platzhalterzeichen für das Microsoft Access-Datenbankmodul schließt sich gegenseitig aus. Sie können jeweils nur einen Satz Platzhalterzeichen verwenden, es ist nicht möglich, sie miteinander zu kombinieren. Die ANSI SQL-Platzhalter sind nur verfügbar, wenn das Microsoft Access-Datenbankmodul und der OLE DB-Anbieter für das Microsoft Office 12.0 Access-Datenbankmodul verwendet werden. Wenn Sie versuchen, die ANSI SQL-Platzhalter über Microsoft Access oder Datenzugriffsobjekte (DAO) zu verwenden, werden sie als Literale interpretiert. Umgekehrt verhält es sich, wenn Sie den OLE DB-Anbieter für das Microsoft Access-Datenbankmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e86c-p103">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))** operator. The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive. You must use one set or the other and cannot mix them. The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider. If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals. The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="7e86c-120">Übereinstimmendes Zeichen</span><span class="sxs-lookup"><span data-stu-id="7e86c-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="7e86c-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="7e86c-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="7e86c-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="7e86c-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="7e86c-123">Ein beliebiges Zeichen</span><span class="sxs-lookup"><span data-stu-id="7e86c-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="7e86c-124">?</span><span class="sxs-lookup"><span data-stu-id="7e86c-124"></span></span></p></td>
    <td><p><span data-ttu-id="7e86c-125">_ (Unterstrich)</span><span class="sxs-lookup"><span data-stu-id="7e86c-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7e86c-126">Null oder mehrere Zeichen</span><span class="sxs-lookup"><span data-stu-id="7e86c-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="7e86c-p104">Microsoft Access SQL ist im Allgemeinen weniger einschränkend, so können Ausdrücke beispielsweise gruppiert und sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="7e86c-p104">Microsoft Access SQL is generally less restrictive. For example, it permits grouping and ordering on expressions.</span></span>

  - <span data-ttu-id="7e86c-129">Microsoft Access SQL unterstützt leistungsstärkere Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="7e86c-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="7e86c-130">Erweiterte Microsoft Access SQL-Features</span><span class="sxs-lookup"><span data-stu-id="7e86c-130">Enhanced Features of Microsoft Access SQL</span></span>

<span data-ttu-id="7e86c-131">Microsoft Access SQL stellt die folgenden erweiterten Features bereit:</span><span class="sxs-lookup"><span data-stu-id="7e86c-131">Microsoft Access SQL provides the following enhanced features:</span></span>

  - <span data-ttu-id="7e86c-132">Die [TRANSFORM](transform-statement-microsoft-access-sql.md)-Anweisung, die Kreuztabellenabfragen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7e86c-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

  - <span data-ttu-id="7e86c-133">Zusätzliche [Aggregatfunktionen](sql-aggregate-functions-sql.md) wie **StDev** und **VarP**.</span><span class="sxs-lookup"><span data-stu-id="7e86c-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

  - <span data-ttu-id="7e86c-134">Die [PARAMETERS](parameters-declaration-microsoft-access-sql.md)-Deklaration zum Definieren von Parameterabfragen.</span><span class="sxs-lookup"><span data-stu-id="7e86c-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="7e86c-135">ANSI SQL-Features ohne Unterstützung in Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="7e86c-135">ANSI SQL Features Not Supported in Microsoft Access SQL</span></span>

<span data-ttu-id="7e86c-136">Microsoft Access SQL unterstützt folgende ANSI SQL-Features nicht:</span><span class="sxs-lookup"><span data-stu-id="7e86c-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

  - <span data-ttu-id="7e86c-p105">Verweise auf die DISTINCT-Aggregatfunktion. Microsoft Access SQL lässt beispielsweise die Syntax SUM(DISTINCT *Spaltenname*) nicht zu.</span><span class="sxs-lookup"><span data-stu-id="7e86c-p105">DISTINCT aggregate function references. For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

  - <span data-ttu-id="7e86c-139">Die LIMIT TO *Nn* ROWS-Klausel, zur Begrenzung der Anzahl von Zeilen, die von einer Abfrage zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e86c-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="7e86c-140">Es kann nur die [WHERE-Klausel](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) verwendet werden, um den Bereich einer Abfrage einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="7e86c-140">You can use only the [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) to limit the scope of a query.</span></span>

