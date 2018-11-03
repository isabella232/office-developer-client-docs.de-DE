---
title: SQL-Datentypen (Access PC-Datenbank-Referenz)
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
ms.openlocfilehash: bd5deb6d14aaf5911cd87c4d562dbec74e7ad1f2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944487"
---
# <a name="sql-data-types"></a><span data-ttu-id="72dd9-102">SQL-Datentypen</span><span class="sxs-lookup"><span data-stu-id="72dd9-102">SQL data types</span></span>

<span data-ttu-id="72dd9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72dd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72dd9-104">Microsoft Access-Datenbank-Engine SQL-Datentypen bestehen aus 13 vom Microsoft Jet-Datenbankmodul definierten primären Datentypen und mehreren gültigen Synonymen für diese Datentypen erkannt.</span><span class="sxs-lookup"><span data-stu-id="72dd9-104">The Microsoft Access database engine SQL data types consist of 13 primary data types defined by the Microsoft Jet database engine and several valid synonyms recognized for these data types.</span></span>

<span data-ttu-id="72dd9-p101">In der folgenden Tabelle werden die primären Datentypen aufgelistet. Die Synonyme werden unter [Reservierte Wörter für das Microsoft Access-Datenbankmodul SQL](sql-reserved-words.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="72dd9-p101">The following table lists the primary data types. The synonyms are identified in [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72dd9-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="72dd9-107">Data type</span></span></p></th>
<th><p><span data-ttu-id="72dd9-108">Speichergröße</span><span class="sxs-lookup"><span data-stu-id="72dd9-108">Storage size</span></span></p></th>
<th><p><span data-ttu-id="72dd9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72dd9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72dd9-110">BINARY</span><span class="sxs-lookup"><span data-stu-id="72dd9-110">BINARY</span></span></p></td>
<td><p><span data-ttu-id="72dd9-111">1 Byte pro Zeichen</span><span class="sxs-lookup"><span data-stu-id="72dd9-111">1 byte per character</span></span></p></td>
<td><p><span data-ttu-id="72dd9-p102">In einem Feld dieses Datentyps kann ein beliebiges Zeichen gespeichert werden. Es erfolgt keine Übersetzung der Daten (zum Beispiel in Text). Die Daten in einem binären Feld werden so angezeigt wie sie eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="72dd9-p102">Any type of data may be stored in a field of this type. No translation of the data (for example, to text) is made. How the data is input in a binary field dictates how it will appear as output.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dd9-115">BIT</span><span class="sxs-lookup"><span data-stu-id="72dd9-115">BIT</span></span></p></td>
<td><p><span data-ttu-id="72dd9-116">1 Byte</span><span class="sxs-lookup"><span data-stu-id="72dd9-116">1 byte</span></span></p></td>
<td><p><span data-ttu-id="72dd9-117">Felder mit den Werten Ja oder Nein, die jeweils nur einen der beiden Werte enthalten können.</span><span class="sxs-lookup"><span data-stu-id="72dd9-117">Yes and No values and fields that contain only one of two values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dd9-118">TINYINT</span><span class="sxs-lookup"><span data-stu-id="72dd9-118">TINYINT</span></span></p></td>
<td><p><span data-ttu-id="72dd9-119">1 Byte</span><span class="sxs-lookup"><span data-stu-id="72dd9-119">1 byte</span></span></p></td>
<td><p><span data-ttu-id="72dd9-120">Ein Wert bestehend aus einer ganzen Zahl zwischen 0 und 255.</span><span class="sxs-lookup"><span data-stu-id="72dd9-120">An integer value between 0 and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dd9-121">MONEY</span><span class="sxs-lookup"><span data-stu-id="72dd9-121">MONEY</span></span></p></td>
<td><p><span data-ttu-id="72dd9-122">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="72dd9-122">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="72dd9-123">Eine skalierte ganze Zahl zwischen – 922,337,203,685,477.5808 und 922,337,203,685,477.5807.</span><span class="sxs-lookup"><span data-stu-id="72dd9-123">A scaled integer between – 922,337,203,685,477.5808 and 922,337,203,685,477.5807.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dd9-124">DATETIME (siehe DOUBLE)</span><span class="sxs-lookup"><span data-stu-id="72dd9-124">DATETIME (See DOUBLE)</span></span></p></td>
<td><p><span data-ttu-id="72dd9-125">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="72dd9-125">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="72dd9-126">Ein Datum- oder Uhrzeitwert, der zwischen der Jahresangabe 100 und 9999 liegt.</span><span class="sxs-lookup"><span data-stu-id="72dd9-126">A date or time value between the years 100 and 9999.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dd9-127">UNIQUEIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="72dd9-127">UNIQUEIDENTIFIER</span></span></p></td>
<td><p><span data-ttu-id="72dd9-128">128 Bit</span><span class="sxs-lookup"><span data-stu-id="72dd9-128">128 bits</span></span></p></td>
<td><p><span data-ttu-id="72dd9-129">Eine eindeutige ID-Nummer, die für Remoteprozeduraufrufe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72dd9-129">A unique identification number used with remote procedure calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dd9-130">REAL</span><span class="sxs-lookup"><span data-stu-id="72dd9-130">REAL</span></span></p></td>
<td><p><span data-ttu-id="72dd9-131">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="72dd9-131">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="72dd9-132">Ein Wert, der aus einer Gleitkommazahl mit einfacher Genauigkeit besteht und für negative Werte in einem Bereich von – 3.402823E38 bis – 1.401298E-45, für positive Werte in einem Bereich von 1.401298E-45 bis 3.402823E38 liegt oder den Wert 0 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="72dd9-132">A single-precision floating-point value with a range of – 3.402823E38 to – 1.401298E-45 for negative values, 1.401298E-45 to 3.402823E38 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dd9-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="72dd9-133">FLOAT</span></span></p></td>
<td><p><span data-ttu-id="72dd9-134">8 Bytes</span><span class="sxs-lookup"><span data-stu-id="72dd9-134">8 bytes</span></span></p></td>
<td><p><span data-ttu-id="72dd9-135">Ein Wert, der aus einer Gleitkommazahl mit doppelter Genauigkeit besteht und für negative Werte in einem Bereich von – 1.79769313486232E308 bis – 4.94065645841247E-324, für positive Werte in einem Bereich von 4.94065645841247E-324 bis 1.79769313486232E308 liegt und den Wert 0 annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="72dd9-135">A double-precision floating-point value with a range of – 1.79769313486232E308 to – 4.94065645841247E-324 for negative values, 4.94065645841247E-324 to 1.79769313486232E308 for positive values, and 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dd9-136">SMALLINT</span><span class="sxs-lookup"><span data-stu-id="72dd9-136">SMALLINT</span></span></p></td>
<td><p><span data-ttu-id="72dd9-137">2 Bytes</span><span class="sxs-lookup"><span data-stu-id="72dd9-137">2 bytes</span></span></p></td>
<td><p><span data-ttu-id="72dd9-p103">Eine ganze Zahl vom Short Integer-Datentyp zwischen – 32,768 und 32,767. (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="72dd9-p103">A short integer between – 32,768 and 32,767. (See Notes)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dd9-140">INTEGER</span><span class="sxs-lookup"><span data-stu-id="72dd9-140">INTEGER</span></span></p></td>
<td><p><span data-ttu-id="72dd9-141">4 Bytes</span><span class="sxs-lookup"><span data-stu-id="72dd9-141">4 bytes</span></span></p></td>
<td><p><span data-ttu-id="72dd9-p104">Eine ganze Zahl vom Long Integer-Datentyp zwischen – 2,147,483,648 und 2,147,483,647. (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="72dd9-p104">A long integer between – 2,147,483,648 and 2,147,483,647. (See Notes)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dd9-144">DECIMAL</span><span class="sxs-lookup"><span data-stu-id="72dd9-144">DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="72dd9-145">17 Bytes</span><span class="sxs-lookup"><span data-stu-id="72dd9-145">17 bytes</span></span></p></td>
<td><p><span data-ttu-id="72dd9-p105">Ein Datentyp zur Angabe eines exakten numerischen Werts von 1028 - 1 bis - 1028 - 1. Sie können für diesen Wert eine Genauigkeit (1 - 28) und eine Skala (0 - definierte Genauigkeit) definieren. Die Standardwerte für Genauigkeit und Skala sind jeweils 18 und 0.</span><span class="sxs-lookup"><span data-stu-id="72dd9-p105">An exact numeric data type that holds values from 1028 - 1 through - 1028 - 1. You can define both precision (1 - 28) and scale (0 - defined precision). The default precision and scale are 18 and 0, respectively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dd9-149">TEXT</span><span class="sxs-lookup"><span data-stu-id="72dd9-149">TEXT</span></span></p></td>
<td><p><span data-ttu-id="72dd9-150">2 Bytes pro Zeichen (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="72dd9-150">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="72dd9-151">Null bis maximal 2,14 Gigabytes.</span><span class="sxs-lookup"><span data-stu-id="72dd9-151">Zero to a maximum of 2.14 gigabytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dd9-152">IMAGE</span><span class="sxs-lookup"><span data-stu-id="72dd9-152">IMAGE</span></span></p></td>
<td><p><span data-ttu-id="72dd9-153">Wie erforderlich</span><span class="sxs-lookup"><span data-stu-id="72dd9-153">As required</span></span></p></td>
<td><p><span data-ttu-id="72dd9-p106">Null bis maximal 2,14 Gigabytes. Verwendung für OLE-Objekte.</span><span class="sxs-lookup"><span data-stu-id="72dd9-p106">Zero to a maximum of 2.14 gigabytes. Used for OLE objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dd9-156">CHARACTER</span><span class="sxs-lookup"><span data-stu-id="72dd9-156">CHARACTER</span></span></p></td>
<td><p><span data-ttu-id="72dd9-157">2 Byte pro Zeichen. (Siehe Hinweise)</span><span class="sxs-lookup"><span data-stu-id="72dd9-157">2 bytes per character (See Notes)</span></span></p></td>
<td><p><span data-ttu-id="72dd9-158">Null bis 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="72dd9-158">Zero to 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="72dd9-p107">Sowohl der Ausgangswert als auch der inkrementelle Werte können unter Verwendung der <A href="alter-table-statement-microsoft-access-sql.md">ALTER TABLE-Anweisung</A> geändert werden. Neue Zeilen, die in die Tabelle eingefügt werden, weisen Werte auf, die auf den neuen Ausgangs- bzw. inkrementellen Werten basieren und die automatisch für die Spalte generiert werden. Wenn basierend auf den neuen Ausgangs- bzw. inkrementellen Werten Werte generiert werden können, die auf vorhergehenden Ausgangs- bzw. inkrementellen Werten basieren, werden Duplikate generiert. Handelt es sich bei der Spalte um einen Primärschlüssel, kann beim Einfügen neuer Zeilen ein Fehler verursacht werden, wenn duplizierte Werte generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="72dd9-p107">Both the seed and the increment can be modified using an <A href="alter-table-statement-microsoft-access-sql.md">ALTER TABLE statement</A>. New rows inserted into the table will have values, based on the new seed and increment values, that are automatically generated for the column. If the new seed and increment can yield values that match values generated based on the preceding seed and increment, duplicates will be generated. If the column is a primary key, then inserting new rows may result in errors when duplicate values are generated.</span></span></P>
> <LI>
> <P><span data-ttu-id="72dd9-p108">Verwenden Sie die SELECT @@IDENTITY-Anweisung, um den letzten Wert zu ermitteln, der für automatisch inkrementierte Spalten generiert wurde. Es ist nicht möglich, einen Tabellennamen anzugeben. Der zurückgegebene Wert stammt aus der Tabelle mit einer automatisch inkrementierten Spalte, die zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="72dd9-p108">To find the last value that was used for an auto-increment column, you can use the following statement: SELECT @@IDENTITY. You cannot specify a table name. The value returned is from the last table, containing an auto-increment column, that was updated.</span></span></P></LI></UL>


