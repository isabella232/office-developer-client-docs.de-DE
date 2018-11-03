---
title: Gleichwertige ANSI SQL-Datentypen
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed13aab8d1f6851dd05ea2d79877e34c14665a3f
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937162"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="cae7e-102">Gleichwertige ANSI SQL-Datentypen</span><span class="sxs-lookup"><span data-stu-id="cae7e-102">Equivalent ANSI SQL Data Types</span></span>


<span data-ttu-id="cae7e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cae7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cae7e-104">In der folgenden Tabelle werden ANSI SQL-Datentypen, die gleichwertigen Datentypen für das Microsoft Access-Datenbankmodul SQL sowie die gültigen Synonyme aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cae7e-104">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms.</span></span> <span data-ttu-id="cae7e-105">Es sind auch die entsprechenden Microsoft SQL Server™-Datentypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cae7e-105">It also lists the equivalent Microsoft SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cae7e-106">ANSI SQL-Datentyp</span><span class="sxs-lookup"><span data-stu-id="cae7e-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="cae7e-107">Microsoft Access SQL-Datentyp</span><span class="sxs-lookup"><span data-stu-id="cae7e-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="cae7e-108">
Synonym</span><span class="sxs-lookup"><span data-stu-id="cae7e-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="cae7e-109">Microsoft SQL Server-Datentyp</span><span class="sxs-lookup"><span data-stu-id="cae7e-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="cae7e-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="cae7e-111">BINARY (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-112">VARBINARY, BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="cae7e-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="cae7e-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="cae7e-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cae7e-115">BIT (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="cae7e-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="cae7e-117">BIT</span><span class="sxs-lookup"><span data-stu-id="cae7e-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cae7e-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="cae7e-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="cae7e-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="cae7e-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="cae7e-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="cae7e-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cae7e-123">COUNTER (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="cae7e-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="cae7e-125">(Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cae7e-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="cae7e-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="cae7e-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="cae7e-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="cae7e-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="cae7e-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="cae7e-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="cae7e-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="cae7e-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="cae7e-132">DATE, TIME (siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="cae7e-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cae7e-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="cae7e-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="cae7e-136">GUID</span><span class="sxs-lookup"><span data-stu-id="cae7e-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="cae7e-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="cae7e-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cae7e-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="cae7e-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cae7e-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="cae7e-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="cae7e-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="cae7e-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="cae7e-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-142">REAL</span><span class="sxs-lookup"><span data-stu-id="cae7e-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="cae7e-143">REAL</span><span class="sxs-lookup"><span data-stu-id="cae7e-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="cae7e-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="cae7e-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="cae7e-145">REAL</span><span class="sxs-lookup"><span data-stu-id="cae7e-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="cae7e-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="cae7e-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cae7e-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="cae7e-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cae7e-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="cae7e-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="cae7e-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="cae7e-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="cae7e-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="cae7e-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="cae7e-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="cae7e-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cae7e-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="cae7e-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cae7e-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="cae7e-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="cae7e-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="cae7e-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cae7e-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="cae7e-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="cae7e-159">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="cae7e-160">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-161">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cae7e-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="cae7e-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="cae7e-163">LONGBINARY GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="cae7e-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="cae7e-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="cae7e-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cae7e-165">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae7e-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="cae7e-166">TEXT (siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="cae7e-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cae7e-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="cae7e-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="cae7e-170">CHAR (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cae7e-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="cae7e-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="cae7e-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="cae7e-p102">Der ANSI SQL BIT-Datentyp entspricht nicht dem Microsoft Access SQL BIT-Datentyp, sondern dem BINARY-Datentyp. Es gibt keinen gleichwertigen ANSI SQL-Datentyp für den Microsoft Access SQL BIT-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="cae7e-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="cae7e-176">Der TIMESTAMP-Datentyp wird nicht mehr als ein Synonym des DATETIME-Datentyps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cae7e-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="cae7e-p103">Der NUMERIC-Datentyp wird nicht mehr als ein Synonym der Datentypen FLOAT oder DOUBLE unterstützt. Der NUMERIC-Datentyp wird jetzt als ein Synonym des DECIMAL-Datentyps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cae7e-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="cae7e-179">Ein LONGTEXT-Feld wird immer im Unicode-Darstellungsformat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cae7e-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="cae7e-p104">Wird der TEXT-Datentypname ohne Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), wird ein LONGTEXT-Feld erstellt. Auf diese Weise können [CREATE TABLE-Anweisungen](create-table-statement-microsoft-access-sql.md) geschrieben werden, die Microsoft SQL Server-konsistente Datentypen generieren.</span><span class="sxs-lookup"><span data-stu-id="cae7e-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="cae7e-182">Ein CHAR-Feld wird immer im Unicode-Darstellungsformat gespeichert, das gleichwertig mit dem ANSI SQL NATIONAL CHAR-Datentyp ist.</span><span class="sxs-lookup"><span data-stu-id="cae7e-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="cae7e-p105">Wird der TEXT-Datentypname unter Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), ist der Datentyp des Felds gleichwertig mit dem CHAR-Datentyp. Auf diese Weise wird die Abwärtskompatibilität für die meisten Microsoft Jet-Anwendungen gewährleistet und ermöglicht, dass der TEXT-Datentyp (ohne Längenangabe) auf Microsoft SQL Server ausgerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cae7e-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


