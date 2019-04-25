---
title: SQL-Datentypen (Access-Desktopdatenbankreferenz)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308582"
---
# <a name="sql-data-types"></a><span data-ttu-id="b7bfe-102">SQL-Datentypen</span><span class="sxs-lookup"><span data-stu-id="b7bfe-102">SQL data types</span></span>

<span data-ttu-id="b7bfe-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7bfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7bfe-104">Die SQL-Datentypen für das Microsoft Access-Datenbankmodul bestehen aus 13 primären Datentypen. Diese Datentypen werden von dem Microsoft Jet-Datenbankmodul und verschiedenen gültigen Synonymen für diese Datentypen definiert.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft® Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="b7bfe-105">In der folgenden Tabelle werden die primären Datentypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-105">The following table lists the primary data types.</span></span> <span data-ttu-id="b7bfe-106">Die Synonyme werden unter [Reservierte Wörter für das Microsoft Access-Datenbankmodul SQL](sql-reserved-words.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-106">The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7bfe-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b7bfe-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="b7bfe-108">Speicherbedarf</span><span class="sxs-lookup"><span data-stu-id="b7bfe-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="b7bfe-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7bfe-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7bfe-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="b7bfe-110">Binary</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-111">1 Byte pro Zeichen</span><span class="sxs-lookup"><span data-stu-id="b7bfe-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-p102">In einem Feld dieses Typs können beliebige Datentypen gespeichert werden. Es erfolgt keine Konvertierung der Daten (z. B. in Text). Die Art und Weise, wie die Daten in ein binäres Feld eingegeben werden, bestimmt, wie sie als Ausgabe angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7bfe-115">BIT</span><span class="sxs-lookup"><span data-stu-id="b7bfe-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-116">1 Byte</span><span class="sxs-lookup"><span data-stu-id="b7bfe-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-117">Ja- und Nein-Werte sowie Felder, die nur einen von zwei Werten enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7bfe-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="b7bfe-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-119">1 Byte</span><span class="sxs-lookup"><span data-stu-id="b7bfe-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-120">Ein ganzzahliger Wert von 0 bis 255.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7bfe-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="b7bfe-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-122">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="b7bfe-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-123">Eine skalierte ganze Zahl zwischen – 922,337,203,685,477.5808 und 922,337,203,685,477.5807.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7bfe-124">DATETIME (Siehe DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="b7bfe-124">DATETIME
(See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-125">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="b7bfe-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-126">Ein Datums- oder Uhrzeitwert zwischen den Jahren 100 und 9999.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7bfe-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="b7bfe-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-128">128 Bits</span><span class="sxs-lookup"><span data-stu-id="b7bfe-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-129">Eine bei Remoteprozeduraufrufen verwendete eindeutige Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7bfe-130">REAL</span><span class="sxs-lookup"><span data-stu-id="b7bfe-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-131">4 Byte</span><span class="sxs-lookup"><span data-stu-id="b7bfe-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-132">Ein Gleitkommawert mit einfacher Genauigkeit von -3,402823E38 bis -1,401298E-45 für negative Wert und 1,401298E-45 bis 3,402823E38 für positive Werte und 0.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7bfe-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b7bfe-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-134">8 Byte</span><span class="sxs-lookup"><span data-stu-id="b7bfe-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-135">Ein Gleitkommawert mit doppelter Genauigkeit von -1,79769313486232E308 bis -4,94065645841247E-324 für negative Werte und 4,94065645841247E-324 bis 1,79769313486232E308 für positive Werte und 0.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7bfe-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="b7bfe-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-137">2 Byte</span><span class="sxs-lookup"><span data-stu-id="b7bfe-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-p103">Eine ganze Zahl vom Short Integer-Datentyp zwischen – 32,768 und 32,767. (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="b7bfe-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7bfe-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="b7bfe-140">Integer</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-141">4 Byte</span><span class="sxs-lookup"><span data-stu-id="b7bfe-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-p104">Eine ganze Zahl vom Long Integer-Datentyp zwischen – 2,147,483,648 und 2,147,483,647. (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="b7bfe-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7bfe-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="b7bfe-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-145">17 Byte</span><span class="sxs-lookup"><span data-stu-id="b7bfe-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-p105">Ein genauer numerischer Datentyp, der Werte von 1028-1 bis -1028-1 enthält. Sie können die Genauigkeit (1-28) und die Dezimalstellen (0 - definierte Genauigkeit) definieren. Die Standardwerte für Genauigkeit und Dezimalstellen sind 18 und 0.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7bfe-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="b7bfe-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-150">2 Bytes pro Zeichen (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="b7bfe-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-151">0 bis maximal 2,14 Gigabyte.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7bfe-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="b7bfe-152">Image</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-153">Je nach Bedarf</span><span class="sxs-lookup"><span data-stu-id="b7bfe-153">As required</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-p106">0 bis maximal 2,14 Gigabyte. Wird für OLE-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7bfe-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="b7bfe-156">Character</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-157">2 Byte pro Zeichen. (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="b7bfe-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="b7bfe-158">0 bis 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - <span data-ttu-id="b7bfe-p107">Sowohl der Ausgangswert als auch der inkrementelle Werte können unter Verwendung der [ALTER TABLE-Anweisung](alter-table-statement-microsoft-access-sql.md) geändert werden. Neue Zeilen, die in die Tabelle eingefügt werden, weisen Werte auf, die auf den neuen Ausgangs- bzw. inkrementellen Werten basieren und die automatisch für die Spalte generiert werden. Wenn basierend auf den neuen Ausgangs- bzw. inkrementellen  Werten Werte generiert werden können, die auf vorhergehenden Ausgangs- bzw. inkrementellen Werten basieren, werden Duplikate generiert. Handelt es sich bei der Spalte um einen Primärschlüssel, kann beim Einfügen neuer Zeilen ein Fehler verursacht werden, wenn duplizierte Werte generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-p107">Both the seed and the increment can be modified using an [ALTER TABLE statement](alter-table-statement-microsoft-access-sql.md). New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span>
> - <span data-ttu-id="b7bfe-p108">Verwenden Sie die SELECT @@IDENTITY-Anweisung, um den letzten Wert zu ermitteln, der für automatisch inkrementierte Spalten generiert wurde. Es ist nicht möglich, einen Tabellennamen anzugeben. Der zurückgegebene Wert stammt aus der Tabelle mit einer automatisch inkrementierten Spalte, die zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b7bfe-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span>
