---
title: DataTypeEnum (Access Desktop Database Reference)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294442"
---
# <a name="datatypeenum"></a><span data-ttu-id="4c8de-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="4c8de-102">DataTypeEnum</span></span>

<span data-ttu-id="4c8de-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c8de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c8de-p101">Gibt den Datentyp eines [Felds](field-object-ado.md), eines [Parameters](parameter-object-ado.md) oder einer [Eigenschaft](property-object-ado.md) an. Der entsprechende OLE DB-Typindikator wird in der Beschreibungsspalte der folgenden Tabelle in Klammern angezeigt. Weitere Informationen zu OLE DB-Datentypen finden Sie in Kapitel 13 und in Anhang A der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="4c8de-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c8de-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="4c8de-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="4c8de-108">Wert</span><span class="sxs-lookup"><span data-stu-id="4c8de-108">Value</span></span></p></th>
<th><p><span data-ttu-id="4c8de-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c8de-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-110"><strong>AnSammlung</span><span class="sxs-lookup"><span data-stu-id="4c8de-110"><strong>AdArray</span></span><br /><span data-ttu-id="4c8de-111">
</strong>(Gilt nicht für ADOX.)</span><span class="sxs-lookup"><span data-stu-id="4c8de-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="4c8de-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="4c8de-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="4c8de-113">Ein Flagwert, immer kombiniert mit einer anderen Datentypkonstante, die einen Array dieses anderen Datentyps angibt.</span><span class="sxs-lookup"><span data-stu-id="4c8de-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-114"><strong>Bigint</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-115">20</span><span class="sxs-lookup"><span data-stu-id="4c8de-115">20</span></span></p></td>
<td><p><span data-ttu-id="4c8de-116">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 8 Bytes an (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="4c8de-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-117"><strong>die Binärdatei</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-118">128</span><span class="sxs-lookup"><span data-stu-id="4c8de-118">128</span></span></p></td>
<td><p><span data-ttu-id="4c8de-119">Gibt einen Binärwert an (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="4c8de-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-120"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-121">11</span><span class="sxs-lookup"><span data-stu-id="4c8de-121">11</span></span></p></td>
<td><p><span data-ttu-id="4c8de-122">Gibt einen booleschen Wert an (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="4c8de-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-123"><strong>-BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-124">8</span><span class="sxs-lookup"><span data-stu-id="4c8de-124">8</span></span></p></td>
<td><p><span data-ttu-id="4c8de-125">Gibt eine mit Null endende Zeichenfolge (Unicode) an (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="4c8de-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-127">136</span><span class="sxs-lookup"><span data-stu-id="4c8de-127">136</span></span></p></td>
<td><p><span data-ttu-id="4c8de-128">Gibt einen Kapitelwert mit 4 Bytes an, der Zeilen in einem untergeordneten Rowset (DBTYPE_HCHAPTER) kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="4c8de-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-129"><strong>Char</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-130">129</span><span class="sxs-lookup"><span data-stu-id="4c8de-130">129</span></span></p></td>
<td><p><span data-ttu-id="4c8de-131">Gibt einen Zeichenfolgenwert an (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="4c8de-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-132"><strong>Währung</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-133">6</span><span class="sxs-lookup"><span data-stu-id="4c8de-133">6</span></span></p></td>
<td><p><span data-ttu-id="4c8de-p102">Gibt einen Währungswert an (DBTYPE_CY). Die Währung ist eine Festkommazahl mit vier Ziffern rechts vom Dezimalkomma. Sie ist in einer ganzen Zahl mit Vorzeichen und einer Länge von 8 Bytes gespeichert, die um 10.000 skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="4c8de-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-137"><strong>Datum</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-138">7</span><span class="sxs-lookup"><span data-stu-id="4c8de-138">7</span></span></p></td>
<td><p><span data-ttu-id="4c8de-p103">Gibt einen Datumswert an (DBTYPE_DATE). Ein Datum wird als Double gespeichert, wobei der ganze Teil davon die Zahl der Tage seit dem 30. Dezember 1899 und der Bruchteil davon den Teil des Tages darstellt.</span><span class="sxs-lookup"><span data-stu-id="4c8de-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-142">133</span><span class="sxs-lookup"><span data-stu-id="4c8de-142">133</span></span></p></td>
<td><p><span data-ttu-id="4c8de-143">Gibt einen Datumswert (jjjjmmtt) an (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="4c8de-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-145">134</span><span class="sxs-lookup"><span data-stu-id="4c8de-145">134</span></span></p></td>
<td><p><span data-ttu-id="4c8de-146">Gibt einen Zeitwert (hhmmss) an (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="4c8de-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-148">135</span><span class="sxs-lookup"><span data-stu-id="4c8de-148">135</span></span></p></td>
<td><p><span data-ttu-id="4c8de-149">Gibt einen Datums-/Uhrzeitstempel (jjjjmmtthhmmss plus einen Bruchteil in Milliardstel) an (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="4c8de-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-151">14</span><span class="sxs-lookup"><span data-stu-id="4c8de-151">14</span></span></p></td>
<td><p><span data-ttu-id="4c8de-152">Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="4c8de-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-154">5</span><span class="sxs-lookup"><span data-stu-id="4c8de-154">5</span></span></p></td>
<td><p><span data-ttu-id="4c8de-155">Gibt einen Gleitkommawert mit doppelter Genauigkeit an (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="4c8de-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-156"><strong>Leer</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-157">0</span><span class="sxs-lookup"><span data-stu-id="4c8de-157">0</span></span></p></td>
<td><p><span data-ttu-id="4c8de-158">Gibt keinen Wert an (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="4c8de-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-159"><strong>Fehler</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-160">10</span><span class="sxs-lookup"><span data-stu-id="4c8de-160">10</span></span></p></td>
<td><p><span data-ttu-id="4c8de-161">Gibt einen 32-Bit-Fehlercode an (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="4c8de-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-162"><strong>Dateien</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-163">64</span><span class="sxs-lookup"><span data-stu-id="4c8de-163">64</span></span></p></td>
<td><p><span data-ttu-id="4c8de-164">Gibt einen 64-Bit-Wert an, der die Zahl der 100-Nanosekunden-Intervalle seit 1. Januar 1601 darstellt (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="4c8de-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-165"><strong>GUID</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-166">72</span><span class="sxs-lookup"><span data-stu-id="4c8de-166">72</span></span></p></td>
<td><p><span data-ttu-id="4c8de-167">Gibt einen global eindeutigen Bezeichner (GUID) an (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="4c8de-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-169">9</span><span class="sxs-lookup"><span data-stu-id="4c8de-169">9</span></span></p></td>
<td><p><span data-ttu-id="4c8de-170">Gibt einen Zeiger auf eine <strong>IDispatch</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="4c8de-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="4c8de-171"><strong>Hinweis</strong>: dieser Datentyp wird derzeit von ADO nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c8de-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="4c8de-172">Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="4c8de-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-173"><strong>Ganzzahl</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-174">3</span><span class="sxs-lookup"><span data-stu-id="4c8de-174">3</span></span></p></td>
<td><p><span data-ttu-id="4c8de-175">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 4 Bytes an (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="4c8de-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-177">13</span><span class="sxs-lookup"><span data-stu-id="4c8de-177">13</span></span></p></td>
<td><p><span data-ttu-id="4c8de-178">Gibt einen Zeiger auf eine <strong>IUnknown</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="4c8de-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="4c8de-179"><strong>Hinweis</strong>: dieser Datentyp wird derzeit von ADO nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c8de-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="4c8de-180">Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="4c8de-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-182">205</span><span class="sxs-lookup"><span data-stu-id="4c8de-182">205</span></span></p></td>
<td><p><span data-ttu-id="4c8de-183">Gibt einen langen Binärwert an.</span><span class="sxs-lookup"><span data-stu-id="4c8de-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-185">201</span><span class="sxs-lookup"><span data-stu-id="4c8de-185">201</span></span></p></td>
<td><p><span data-ttu-id="4c8de-186">Gibt einen langen Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="4c8de-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-188">203</span><span class="sxs-lookup"><span data-stu-id="4c8de-188">203</span></span></p></td>
<td><p><span data-ttu-id="4c8de-189">Gibt einen mit Null endenden Unicode-Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="4c8de-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-191">131</span><span class="sxs-lookup"><span data-stu-id="4c8de-191">131</span></span></p></td>
<td><p><span data-ttu-id="4c8de-192">Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="4c8de-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-194">138</span><span class="sxs-lookup"><span data-stu-id="4c8de-194">138</span></span></p></td>
<td><p><span data-ttu-id="4c8de-195">Gibt eine Automatisierungs-PROPVARIANT an (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="4c8de-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-196"><strong>Einzel</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-197">4</span><span class="sxs-lookup"><span data-stu-id="4c8de-197">4</span></span></p></td>
<td><p><span data-ttu-id="4c8de-198">Gibt einen Gleitkommawert mit einfacher Genauigkeit an (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="4c8de-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-199"><strong>SmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-200">2</span><span class="sxs-lookup"><span data-stu-id="4c8de-200">2</span></span></p></td>
<td><p><span data-ttu-id="4c8de-201">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 2 Bytes an (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="4c8de-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-202"><strong>addTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-203">16</span><span class="sxs-lookup"><span data-stu-id="4c8de-203">16</span></span></p></td>
<td><p><span data-ttu-id="4c8de-204">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 1 Byte an (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="4c8de-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-206">21</span><span class="sxs-lookup"><span data-stu-id="4c8de-206">21</span></span></p></td>
<td><p><span data-ttu-id="4c8de-207">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 8 Bytes an (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="4c8de-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-209">19</span><span class="sxs-lookup"><span data-stu-id="4c8de-209">19</span></span></p></td>
<td><p><span data-ttu-id="4c8de-210">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 4 Bytes an (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="4c8de-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-212">18</span><span class="sxs-lookup"><span data-stu-id="4c8de-212">18</span></span></p></td>
<td><p><span data-ttu-id="4c8de-213">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 2 Bytes an (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="4c8de-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-215">17</span><span class="sxs-lookup"><span data-stu-id="4c8de-215">17</span></span></p></td>
<td><p><span data-ttu-id="4c8de-216">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 1 Byte an (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="4c8de-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-218">132</span><span class="sxs-lookup"><span data-stu-id="4c8de-218">132</span></span></p></td>
<td><p><span data-ttu-id="4c8de-219">Gibt eine benutzerdefinierte Variable an (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="4c8de-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-220"><strong>VarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-221">204</span><span class="sxs-lookup"><span data-stu-id="4c8de-221">204</span></span></p></td>
<td><p><span data-ttu-id="4c8de-222">Gibt einen Binärwert an (nur für <strong>Parameter</strong>-Objekt).</span><span class="sxs-lookup"><span data-stu-id="4c8de-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-223"><strong>-VarChar</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-224">200</span><span class="sxs-lookup"><span data-stu-id="4c8de-224">200</span></span></p></td>
<td><p><span data-ttu-id="4c8de-225">Gibt einen Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="4c8de-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-227">12</span><span class="sxs-lookup"><span data-stu-id="4c8de-227">12</span></span></p></td>
<td><p><span data-ttu-id="4c8de-228">Gibt eine Automatisierungsvariante an (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="4c8de-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="4c8de-229"><strong>Hinweis</strong>: dieser Datentyp wird derzeit von ADO nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c8de-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="4c8de-230">Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="4c8de-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-232">139</span><span class="sxs-lookup"><span data-stu-id="4c8de-232">139</span></span></p></td>
<td><p><span data-ttu-id="4c8de-233">Gibt einen numerischen Wert an (nur für <strong>Parameter</strong>-Objekt).</span><span class="sxs-lookup"><span data-stu-id="4c8de-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-235">202</span><span class="sxs-lookup"><span data-stu-id="4c8de-235">202</span></span></p></td>
<td><p><span data-ttu-id="4c8de-236">Gibt eine mit Null endende Unicode-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="4c8de-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="4c8de-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4c8de-238">130</span><span class="sxs-lookup"><span data-stu-id="4c8de-238">130</span></span></p></td>
<td><p><span data-ttu-id="4c8de-239">Gibt eine mit Null endende Unicode-Zeichenfolge an (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="4c8de-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4c8de-240">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="4c8de-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="4c8de-241">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4c8de-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c8de-242">Konstante</span><span class="sxs-lookup"><span data-stu-id="4c8de-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-243">AdoEnums. DataType. ARRAY</span><span class="sxs-lookup"><span data-stu-id="4c8de-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-244">AdoEnums. DataType. BIGINt</span><span class="sxs-lookup"><span data-stu-id="4c8de-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-245">AdoEnums. DataType. BINARY</span><span class="sxs-lookup"><span data-stu-id="4c8de-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-246">AdoEnums. DataType. BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4c8de-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-247">AdoEnums. DataType. BSTR</span><span class="sxs-lookup"><span data-stu-id="4c8de-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-248">AdoEnums. DataType. CHAPTER</span><span class="sxs-lookup"><span data-stu-id="4c8de-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-249">AdoEnums. DataType. CHAR</span><span class="sxs-lookup"><span data-stu-id="4c8de-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-250">AdoEnums. DataType. CURRENCY</span><span class="sxs-lookup"><span data-stu-id="4c8de-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-251">AdoEnums. DataType. DATE</span><span class="sxs-lookup"><span data-stu-id="4c8de-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-252">AdoEnums. DataType. dbDATE</span><span class="sxs-lookup"><span data-stu-id="4c8de-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-253">AdoEnums. DataType. dbTIME</span><span class="sxs-lookup"><span data-stu-id="4c8de-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-254">AdoEnums. DataType. dbTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="4c8de-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-255">AdoEnums. DataType. DECIMAL</span><span class="sxs-lookup"><span data-stu-id="4c8de-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-256">AdoEnums. DataType. DOUBLE</span><span class="sxs-lookup"><span data-stu-id="4c8de-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-257">AdoEnums. DataType. EMPTY</span><span class="sxs-lookup"><span data-stu-id="4c8de-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-258">AdoEnums. DataType. ERROR</span><span class="sxs-lookup"><span data-stu-id="4c8de-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-259">AdoEnums. DataType. fileTIME</span><span class="sxs-lookup"><span data-stu-id="4c8de-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-260">AdoEnums. DataType. GUID</span><span class="sxs-lookup"><span data-stu-id="4c8de-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-261">AdoEnums. DataType. IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="4c8de-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-262">AdoEnums. DataType. INTEGER</span><span class="sxs-lookup"><span data-stu-id="4c8de-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-263">AdoEnums. DataType. IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="4c8de-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-264">AdoEnums. DataType. LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="4c8de-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-265">AdoEnums. DataType. LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="4c8de-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-266">AdoEnums. DataType. LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="4c8de-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-267">AdoEnums. DataType. NUMERIC</span><span class="sxs-lookup"><span data-stu-id="4c8de-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-268">AdoEnums. DataType. PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="4c8de-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-269">AdoEnums. DataType. SINGLE</span><span class="sxs-lookup"><span data-stu-id="4c8de-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-270">AdoEnums. DataType. SMALLINT</span><span class="sxs-lookup"><span data-stu-id="4c8de-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-271">AdoEnums. DataType. TINYINT</span><span class="sxs-lookup"><span data-stu-id="4c8de-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-272">AdoEnums. DataType. UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="4c8de-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-273">AdoEnums. DataType. UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="4c8de-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-274">AdoEnums. DataType. UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="4c8de-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-275">AdoEnums. DataType. UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="4c8de-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-276">AdoEnums. DataType. USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="4c8de-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-277">AdoEnums. DataType. VARBINARY</span><span class="sxs-lookup"><span data-stu-id="4c8de-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-278">AdoEnums. DataType. VARCHAR</span><span class="sxs-lookup"><span data-stu-id="4c8de-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-279">AdoEnums. DataType. VARIANT</span><span class="sxs-lookup"><span data-stu-id="4c8de-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-280">AdoEnums. DataType. VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="4c8de-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c8de-281">AdoEnums. DataType. VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="4c8de-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c8de-282">AdoEnums. DataType. Typ WCHAR</span><span class="sxs-lookup"><span data-stu-id="4c8de-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

