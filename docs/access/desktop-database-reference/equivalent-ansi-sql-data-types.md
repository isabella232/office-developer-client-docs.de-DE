---
title: Äquivalente ANSI SQL-Datentypen
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293511"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="bc5f8-102">Äquivalente ANSI SQL-Datentypen</span><span class="sxs-lookup"><span data-stu-id="bc5f8-102">Equivalent ANSI SQL data types</span></span>


<span data-ttu-id="bc5f8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc5f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc5f8-104">In der folgenden Tabelle sind die ANSI-SQL-Datentypen, ihre entsprechenden SQL-Datentypen im Microsoft Access-Datenbankmodul und deren gültige Synonyme aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="bc5f8-105">Zusätzlich werden die gleichwertigen Microsoft SQL Server™-Datentypen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-105">It also lists the equivalent Microsoft® SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc5f8-106">ANSI SQL-Datentyp</span><span class="sxs-lookup"><span data-stu-id="bc5f8-106">ANSI SQL
data type</span></span></p></th>
<th><p><span data-ttu-id="bc5f8-107">Microsoft Access-SQL-Datentyp</span><span class="sxs-lookup"><span data-stu-id="bc5f8-107">Microsoft Access
SQL data type</span></span></p></th>
<th><p><span data-ttu-id="bc5f8-108">Synonym</span><span class="sxs-lookup"><span data-stu-id="bc5f8-108">Synonym lookup</span></span></p></th>
<th><p><span data-ttu-id="bc5f8-109">Microsoft SQL Server-Datentyp</span><span class="sxs-lookup"><span data-stu-id="bc5f8-109">Microsoft SQL
Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="bc5f8-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-111">BINARY (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-112">VARBINARY, BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="bc5f8-112">VARBINARY,
BINARY VARYING
BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="bc5f8-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-115">BIT (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="bc5f8-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-117">BIT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="bc5f8-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-123">COUNTER (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-125">(Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="bc5f8-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="bc5f8-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="bc5f8-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="bc5f8-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="bc5f8-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-132">DATE, TIME (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-132">DATE, TIME  (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="bc5f8-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="bc5f8-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-136">GUID</span><span class="sxs-lookup"><span data-stu-id="bc5f8-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="bc5f8-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="bc5f8-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="bc5f8-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="bc5f8-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="bc5f8-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-142">REAL</span><span class="sxs-lookup"><span data-stu-id="bc5f8-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-143">REAL</span><span class="sxs-lookup"><span data-stu-id="bc5f8-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="bc5f8-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-145">REAL</span><span class="sxs-lookup"><span data-stu-id="bc5f8-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="bc5f8-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="bc5f8-154">Integer</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="bc5f8-155">Integer</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="bc5f8-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="bc5f8-157">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="bc5f8-158">Interval</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-159">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="bc5f8-160">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-161">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="bc5f8-162">Image</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-163">LONGBINARY, GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-163">LONGBINARY,  GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="bc5f8-164">Image</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc5f8-165">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc5f8-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-166">TEXT (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-166">TEXT  (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="bc5f8-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc5f8-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="bc5f8-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-170">CHAR (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span><span class="sxs-lookup"><span data-stu-id="bc5f8-171">TEXT(n), ALPHANUMERIC,  CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="bc5f8-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="bc5f8-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="bc5f8-p102">Der ANSI SQL BIT-Datentyp entspricht nicht dem Microsoft Access SQL BIT-Datentyp, sondern dem BINARY-Datentyp. Es gibt keinen gleichwertigen ANSI SQL-Datentyp für den Microsoft Access SQL BIT-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="bc5f8-176">Der TIMESTAMP-Datentyp wird nicht mehr als ein Synonym des DATETIME-Datentyps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="bc5f8-p103">Der NUMERIC-Datentyp wird nicht mehr als ein Synonym der Datentypen FLOAT oder DOUBLE unterstützt. Der NUMERIC-Datentyp wird jetzt als ein Synonym des DECIMAL-Datentyps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="bc5f8-179">Ein LONGTEXT-Feld wird immer im Unicode-Darstellungsformat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="bc5f8-p104">Wird der TEXT-Datentypname ohne Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), wird ein LONGTEXT-Feld erstellt. Auf diese Weise können [CREATE TABLE-Anweisungen](create-table-statement-microsoft-access-sql.md) geschrieben werden, die Microsoft SQL Server-konsistente Datentypen generieren.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="bc5f8-182">Ein CHAR-Feld wird immer im Unicode-Darstellungsformat gespeichert, das gleichwertig mit dem ANSI SQL NATIONAL CHAR-Datentyp ist.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="bc5f8-p105">Wird der TEXT-Datentypname unter Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), ist der Datentyp des Felds gleichwertig mit dem CHAR-Datentyp. Auf diese Weise wird die Abwärtskompatibilität für die meisten Microsoft Jet-Anwendungen gewährleistet und ermöglicht, dass der TEXT-Datentyp (ohne Längenangabe) auf Microsoft SQL Server ausgerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc5f8-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


