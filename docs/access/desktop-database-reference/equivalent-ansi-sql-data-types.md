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
ms.openlocfilehash: cac58601277079f6843df6ac9ac7bcae7824b18a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869526"
---
# <a name="equivalent-ansi-sql-data-types"></a><span data-ttu-id="e5a08-102">Gleichwertige ANSI SQL-Datentypen</span><span class="sxs-lookup"><span data-stu-id="e5a08-102">Equivalent ANSI SQL Data Types</span></span>


<span data-ttu-id="e5a08-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5a08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5a08-p101">In der folgenden Tabelle werden ANSI SQL-Datentypen, die gleichwertigen Datentypen für das Microsoft Access-Datenbankmodul SQL sowie die gültigen Synonyme aufgelistet. Zusätzlich werden die gleichwertigen Microsoft® SQL Server-Datentypen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e5a08-p101">The following table lists ANSI SQL data types, their equivalent Microsoft Access database engine SQL data types, and their valid synonyms. It also lists the equivalent Microsoft® SQL Server™ data types.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5a08-106">ANSI SQL-Datentyp</span><span class="sxs-lookup"><span data-stu-id="e5a08-106">ANSI SQL data type</span></span></p></th>
<th><p><span data-ttu-id="e5a08-107">Microsoft Access SQL-Datentyp</span><span class="sxs-lookup"><span data-stu-id="e5a08-107">Microsoft Access SQL data type</span></span></p></th>
<th><p><span data-ttu-id="e5a08-108">
Synonym</span><span class="sxs-lookup"><span data-stu-id="e5a08-108">Synonym</span></span></p></th>
<th><p><span data-ttu-id="e5a08-109">Microsoft SQL Server-Datentyp</span><span class="sxs-lookup"><span data-stu-id="e5a08-109">Microsoft SQL Server data type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-110">BIT, BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="e5a08-110">BIT, BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="e5a08-111">BINARY (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-111">BINARY (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-112">VARBINARY, BINARY VARYING BIT VARYING</span><span class="sxs-lookup"><span data-stu-id="e5a08-112">VARBINARY, BINARY VARYING BIT VARYING</span></span></p></td>
<td><p><span data-ttu-id="e5a08-113">BINARY, VARBINARY</span><span class="sxs-lookup"><span data-stu-id="e5a08-113">BINARY, VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-114">Not supported</span></span></p></td>
<td><p><span data-ttu-id="e5a08-115">BIT (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-115">BIT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span><span class="sxs-lookup"><span data-stu-id="e5a08-116">BOOLEAN, LOGICAL, LOGICAL1, YESNO</span></span></p></td>
<td><p><span data-ttu-id="e5a08-117">BIT</span><span class="sxs-lookup"><span data-stu-id="e5a08-117">BIT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-118">Not supported</span></span></p></td>
<td><p><span data-ttu-id="e5a08-119">TINYINT</span><span class="sxs-lookup"><span data-stu-id="e5a08-119">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="e5a08-120">INTEGER1, BYTE</span><span class="sxs-lookup"><span data-stu-id="e5a08-120">INTEGER1, BYTE</span></span></p></td>
<td><p><span data-ttu-id="e5a08-121">TINYINT</span><span class="sxs-lookup"><span data-stu-id="e5a08-121">TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-122">Not supported</span></span></p></td>
<td><p><span data-ttu-id="e5a08-123">COUNTER (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-123">COUNTER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-124">AUTOINCREMENT</span><span class="sxs-lookup"><span data-stu-id="e5a08-124">AUTOINCREMENT</span></span></p></td>
<td><p><span data-ttu-id="e5a08-125">(Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-125">(See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-126">Not supported</span></span></p></td>
<td><p><span data-ttu-id="e5a08-127">MONEY</span><span class="sxs-lookup"><span data-stu-id="e5a08-127">MONEY</span></span></p></td>
<td><p><span data-ttu-id="e5a08-128">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="e5a08-128">CURRENCY</span></span></p></td>
<td><p><span data-ttu-id="e5a08-129">MONEY</span><span class="sxs-lookup"><span data-stu-id="e5a08-129">MONEY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-130">DATE, TIME, TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="e5a08-130">DATE, TIME, TIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="e5a08-131">DATETIME</span><span class="sxs-lookup"><span data-stu-id="e5a08-131">DATETIME</span></span></p></td>
<td><p><span data-ttu-id="e5a08-132">DATE, TIME (siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-132">DATE, TIME (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="e5a08-133">DATETIME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-134">Not supported</span></span></p></td>
<td><p><span data-ttu-id="e5a08-135">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="e5a08-135">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="e5a08-136">GUID</span><span class="sxs-lookup"><span data-stu-id="e5a08-136">GUID</span></span></p></td>
<td><p><span data-ttu-id="e5a08-137">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="e5a08-137">UNIQUEIDENTIFIER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-138">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="e5a08-138">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="e5a08-139">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="e5a08-139">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="e5a08-140">NUMERIC, DEC</span><span class="sxs-lookup"><span data-stu-id="e5a08-140">NUMERIC, DEC</span></span></p></td>
<td><p><span data-ttu-id="e5a08-141">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="e5a08-141">DECIMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-142">REAL</span><span class="sxs-lookup"><span data-stu-id="e5a08-142">REAL</span></span></p></td>
<td><p><span data-ttu-id="e5a08-143">REAL</span><span class="sxs-lookup"><span data-stu-id="e5a08-143">REAL</span></span></p></td>
<td><p><span data-ttu-id="e5a08-144">SINGLE, FLOAT4, IEEESINGLE</span><span class="sxs-lookup"><span data-stu-id="e5a08-144">SINGLE, FLOAT4, IEEESINGLE</span></span></p></td>
<td><p><span data-ttu-id="e5a08-145">REAL</span><span class="sxs-lookup"><span data-stu-id="e5a08-145">REAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-146">DOUBLE PRECISION, FLOAT</span><span class="sxs-lookup"><span data-stu-id="e5a08-146">DOUBLE PRECISION, FLOAT</span></span></p></td>
<td><p><span data-ttu-id="e5a08-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e5a08-147">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="e5a08-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-148">DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e5a08-149">FLOAT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-150">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="e5a08-150">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="e5a08-151">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="e5a08-151">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="e5a08-152">SHORT, INTEGER2</span><span class="sxs-lookup"><span data-stu-id="e5a08-152">SHORT, INTEGER2</span></span></p></td>
<td><p><span data-ttu-id="e5a08-153">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="e5a08-153">SMALLINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-154">INTEGER</span><span class="sxs-lookup"><span data-stu-id="e5a08-154">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="e5a08-155">INTEGER</span><span class="sxs-lookup"><span data-stu-id="e5a08-155">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="e5a08-156">LONG, INT, INTEGER4</span><span class="sxs-lookup"><span data-stu-id="e5a08-156">LONG, INT, INTEGER4</span></span></p></td>
<td><p><span data-ttu-id="e5a08-157">INTEGER</span><span class="sxs-lookup"><span data-stu-id="e5a08-157">INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-158">INTERVAL</span><span class="sxs-lookup"><span data-stu-id="e5a08-158">INTERVAL</span></span></p></td>
<td><p><span data-ttu-id="e5a08-159">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-159">Not supported</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e5a08-160">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-160">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-161">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-161">Not supported</span></span></p></td>
<td><p><span data-ttu-id="e5a08-162">IMAGE</span><span class="sxs-lookup"><span data-stu-id="e5a08-162">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="e5a08-163">LONGBINARY GENERAL, OLEOBJECT</span><span class="sxs-lookup"><span data-stu-id="e5a08-163">LONGBINARY, GENERAL, OLEOBJECT</span></span></p></td>
<td><p><span data-ttu-id="e5a08-164">IMAGE</span><span class="sxs-lookup"><span data-stu-id="e5a08-164">IMAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5a08-165">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e5a08-165">Not supported</span></span></p></td>
<td><p><span data-ttu-id="e5a08-166">TEXT (siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-166">TEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-167">LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-168">TEXT</span><span class="sxs-lookup"><span data-stu-id="e5a08-168">TEXT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5a08-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span><span class="sxs-lookup"><span data-stu-id="e5a08-169">CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</span></span></p></td>
<td><p><span data-ttu-id="e5a08-170">CHAR (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-170">CHAR (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-171">Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="e5a08-171">TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="e5a08-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span><span class="sxs-lookup"><span data-stu-id="e5a08-172">CHAR, VARCHAR, NCHAR, NVARCHAR</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - <span data-ttu-id="e5a08-p102">Der ANSI SQL BIT-Datentyp entspricht nicht dem Microsoft Access SQL BIT-Datentyp, sondern dem BINARY-Datentyp. Es gibt keinen gleichwertigen ANSI SQL-Datentyp für den Microsoft Access SQL BIT-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="e5a08-p102">The ANSI SQL BIT data type does not correspond to the Microsoft Access SQL BIT data type. It corresponds to the BINARY data type instead. There is no ANSI SQL equivalent for the Microsoft Access SQL BIT data type.</span></span>
> - <span data-ttu-id="e5a08-176">Der TIMESTAMP-Datentyp wird nicht mehr als ein Synonym des DATETIME-Datentyps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a08-176">TIMESTAMP is no longer supported as a synonym for DATETIME.</span></span>
> - <span data-ttu-id="e5a08-p103">Der NUMERIC-Datentyp wird nicht mehr als ein Synonym der Datentypen FLOAT oder DOUBLE unterstützt. Der NUMERIC-Datentyp wird jetzt als ein Synonym des DECIMAL-Datentyps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5a08-p103">NUMERIC is no longer supported as a synonym for FLOAT or DOUBLE. NUMERIC is now used as a synonym for DECIMAL.</span></span>
> - <span data-ttu-id="e5a08-179">Ein LONGTEXT-Feld wird immer im Unicode-Darstellungsformat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e5a08-179">A LONGTEXT field is always stored in the Unicode representation format.</span></span>
> - <span data-ttu-id="e5a08-p104">Wird der TEXT-Datentypname ohne Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), wird ein LONGTEXT-Feld erstellt. Auf diese Weise können [CREATE TABLE-Anweisungen](create-table-statement-microsoft-access-sql.md) geschrieben werden, die Microsoft SQL Server-konsistente Datentypen generieren.</span><span class="sxs-lookup"><span data-stu-id="e5a08-p104">If the data type name TEXT is used without specifying the optional length, for example TEXT(25), a LONGTEXT field is created. This enables [CREATE TABLE statements](create-table-statement-microsoft-access-sql.md) to be written that will yield data types consistent with Microsoft SQL Server.</span></span>
> - <span data-ttu-id="e5a08-182">Ein CHAR-Feld wird immer im Unicode-Darstellungsformat gespeichert, das gleichwertig mit dem ANSI SQL NATIONAL CHAR-Datentyp ist.</span><span class="sxs-lookup"><span data-stu-id="e5a08-182">A CHAR field is always stored in the Unicode representation format, which is the equivalent of the ANSI SQL NATIONAL CHAR data type.</span></span>
> - <span data-ttu-id="e5a08-p105">Wird der TEXT-Datentypname unter Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), ist der Datentyp des Felds gleichwertig mit dem CHAR-Datentyp. Auf diese Weise wird die Abwärtskompatibilität für die meisten Microsoft Jet-Anwendungen gewährleistet und ermöglicht, dass der TEXT-Datentyp (ohne Längenangabe) auf Microsoft SQL Server ausgerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5a08-p105">If the data type name TEXT is used and the optional length is specified, for example TEXT(25), the data type of the field is equivalent to the CHAR data type. This preserves backwards compatibility for most Microsoft Jet applications, while enabling the TEXT data type (without a length specification) to be aligned with Microsoft SQL Server.</span></span>


