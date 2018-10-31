---
title: DataTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f5c192589f2c90b2ce7b6c7b376b80c92b341e2d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860658"
---
# <a name="datatypeenum"></a><span data-ttu-id="f33e8-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="f33e8-102">DataTypeEnum</span></span>

<span data-ttu-id="f33e8-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f33e8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f33e8-p101">Gibt den Datentyp eines [Felds](field-object-ado.md), eines [Parameters](parameter-object-ado.md) oder einer [Eigenschaft](property-object-ado.md) an. Der entsprechende OLE DB-Typindikator wird in der Beschreibungsspalte der folgenden Tabelle in Klammern angezeigt. Weitere Informationen zu OLE DB-Datentypen finden Sie in Kapitel 13 und in Anhang A der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="f33e8-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f33e8-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="f33e8-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="f33e8-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f33e8-108">Value</span></span></p></th>
<th><p><span data-ttu-id="f33e8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f33e8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="f33e8-110"><strong>AdArray</span></span><br /><span data-ttu-id="f33e8-111">
</strong>(Gilt nicht für ADOX.)</span><span class="sxs-lookup"><span data-stu-id="f33e8-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="f33e8-112">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="f33e8-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="f33e8-113">Ein Flagwert, immer kombiniert mit einer anderen Datentypkonstante, die einen Array dieses anderen Datentyps angibt.</span><span class="sxs-lookup"><span data-stu-id="f33e8-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-115">20</span><span class="sxs-lookup"><span data-stu-id="f33e8-115">20</span></span></p></td>
<td><p><span data-ttu-id="f33e8-116">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 8 Bytes an (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="f33e8-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-118">128</span><span class="sxs-lookup"><span data-stu-id="f33e8-118">128</span></span></p></td>
<td><p><span data-ttu-id="f33e8-119">Gibt einen Binärwert an (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="f33e8-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-121">11</span><span class="sxs-lookup"><span data-stu-id="f33e8-121">11</span></span></p></td>
<td><p><span data-ttu-id="f33e8-122">Gibt einen booleschen Wert an (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="f33e8-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-124">8</span><span class="sxs-lookup"><span data-stu-id="f33e8-124">8</span></span></p></td>
<td><p><span data-ttu-id="f33e8-125">Gibt eine mit Null endende Zeichenfolge (Unicode) an (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="f33e8-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-127">136</span><span class="sxs-lookup"><span data-stu-id="f33e8-127">136</span></span></p></td>
<td><p><span data-ttu-id="f33e8-128">Gibt einen Kapitelwert mit 4 Bytes an, der Zeilen in einem untergeordneten Rowset (DBTYPE_HCHAPTER) kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f33e8-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-130">129</span><span class="sxs-lookup"><span data-stu-id="f33e8-130">129</span></span></p></td>
<td><p><span data-ttu-id="f33e8-131">Gibt einen Zeichenfolgenwert an (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="f33e8-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-133">6</span><span class="sxs-lookup"><span data-stu-id="f33e8-133">6</span></span></p></td>
<td><p><span data-ttu-id="f33e8-p102">Gibt einen Währungswert an (DBTYPE_CY). Die Währung ist eine Festkommazahl mit vier Ziffern rechts vom Dezimalkomma. Sie ist in einer ganzen Zahl mit Vorzeichen und einer Länge von 8 Bytes gespeichert, die um 10.000 skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="f33e8-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-138">7</span><span class="sxs-lookup"><span data-stu-id="f33e8-138">7</span></span></p></td>
<td><p><span data-ttu-id="f33e8-p103">Gibt einen Datumswert an (DBTYPE_DATE). Ein Datum wird als Double gespeichert, wobei der ganze Teil davon die Zahl der Tage seit dem 30. Dezember 1899 und der Bruchteil davon den Teil des Tages darstellt.</span><span class="sxs-lookup"><span data-stu-id="f33e8-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-142">133</span><span class="sxs-lookup"><span data-stu-id="f33e8-142">133</span></span></p></td>
<td><p><span data-ttu-id="f33e8-143">Gibt einen Datumswert (jjjjmmtt) an (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="f33e8-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-145">134</span><span class="sxs-lookup"><span data-stu-id="f33e8-145">134</span></span></p></td>
<td><p><span data-ttu-id="f33e8-146">Gibt einen Zeitwert (hhmmss) an (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="f33e8-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-148">135</span><span class="sxs-lookup"><span data-stu-id="f33e8-148">135</span></span></p></td>
<td><p><span data-ttu-id="f33e8-149">Gibt einen Datums-/Uhrzeitstempel (jjjjmmtthhmmss plus einen Bruchteil in Milliardstel) an (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="f33e8-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-151">14</span><span class="sxs-lookup"><span data-stu-id="f33e8-151">14</span></span></p></td>
<td><p><span data-ttu-id="f33e8-152">Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="f33e8-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-154">5</span><span class="sxs-lookup"><span data-stu-id="f33e8-154">5</span></span></p></td>
<td><p><span data-ttu-id="f33e8-155">Gibt einen Gleitkommawert mit doppelter Genauigkeit an (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="f33e8-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-157">0</span><span class="sxs-lookup"><span data-stu-id="f33e8-157">0</span></span></p></td>
<td><p><span data-ttu-id="f33e8-158">Gibt keinen Wert an (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="f33e8-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-160">10</span><span class="sxs-lookup"><span data-stu-id="f33e8-160">10</span></span></p></td>
<td><p><span data-ttu-id="f33e8-161">Gibt einen 32-Bit-Fehlercode an (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="f33e8-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-163">64</span><span class="sxs-lookup"><span data-stu-id="f33e8-163">64</span></span></p></td>
<td><p><span data-ttu-id="f33e8-164">Gibt einen 64-Bit-Wert an, der die Zahl der 100-Nanosekunden-Intervalle seit 1. Januar 1601 darstellt (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="f33e8-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-166">72</span><span class="sxs-lookup"><span data-stu-id="f33e8-166">72</span></span></p></td>
<td><p><span data-ttu-id="f33e8-167">Gibt einen global eindeutigen Bezeichner (GUID) an (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="f33e8-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-169">9</span><span class="sxs-lookup"><span data-stu-id="f33e8-169">9</span></span></p></td>
<td><p><span data-ttu-id="f33e8-170">Gibt einen Zeiger auf eine <strong>IDispatch</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IDISPATCH).
</span><span class="sxs-lookup"><span data-stu-id="f33e8-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="f33e8-171"><strong>Hinweis</strong>: Dieser Datentyp wird derzeit nicht von ADO unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f33e8-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="f33e8-172">Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="f33e8-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-174">3</span><span class="sxs-lookup"><span data-stu-id="f33e8-174">3</span></span></p></td>
<td><p><span data-ttu-id="f33e8-175">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 4 Bytes an (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="f33e8-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-177">13</span><span class="sxs-lookup"><span data-stu-id="f33e8-177">13</span></span></p></td>
<td><p><span data-ttu-id="f33e8-178">Gibt einen Zeiger auf eine <strong>IUnknown</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IUNKNOWN).
</span><span class="sxs-lookup"><span data-stu-id="f33e8-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="f33e8-179"><strong>Hinweis</strong>: Dieser Datentyp wird derzeit nicht von ADO unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f33e8-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="f33e8-180">Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="f33e8-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-182">205</span><span class="sxs-lookup"><span data-stu-id="f33e8-182">205</span></span></p></td>
<td><p><span data-ttu-id="f33e8-183">Gibt einen langen Binärwert an.</span><span class="sxs-lookup"><span data-stu-id="f33e8-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-185">201</span><span class="sxs-lookup"><span data-stu-id="f33e8-185">201</span></span></p></td>
<td><p><span data-ttu-id="f33e8-186">Gibt einen langen Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="f33e8-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-188">203</span><span class="sxs-lookup"><span data-stu-id="f33e8-188">203</span></span></p></td>
<td><p><span data-ttu-id="f33e8-189">Gibt einen mit Null endenden Unicode-Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="f33e8-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-191">131</span><span class="sxs-lookup"><span data-stu-id="f33e8-191">131</span></span></p></td>
<td><p><span data-ttu-id="f33e8-192">Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="f33e8-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-194">138</span><span class="sxs-lookup"><span data-stu-id="f33e8-194">138</span></span></p></td>
<td><p><span data-ttu-id="f33e8-195">Gibt eine Automatisierungs-PROPVARIANT an (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="f33e8-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-197">4</span><span class="sxs-lookup"><span data-stu-id="f33e8-197">4</span></span></p></td>
<td><p><span data-ttu-id="f33e8-198">Gibt einen Gleitkommawert mit einfacher Genauigkeit an (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="f33e8-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-200">2</span><span class="sxs-lookup"><span data-stu-id="f33e8-200">2</span></span></p></td>
<td><p><span data-ttu-id="f33e8-201">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 2 Bytes an (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="f33e8-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-203">16</span><span class="sxs-lookup"><span data-stu-id="f33e8-203">16</span></span></p></td>
<td><p><span data-ttu-id="f33e8-204">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 1 Byte an (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="f33e8-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-206">21</span><span class="sxs-lookup"><span data-stu-id="f33e8-206">21</span></span></p></td>
<td><p><span data-ttu-id="f33e8-207">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 8 Bytes an (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="f33e8-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-209">19</span><span class="sxs-lookup"><span data-stu-id="f33e8-209">19</span></span></p></td>
<td><p><span data-ttu-id="f33e8-210">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 4 Bytes an (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="f33e8-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-212">18</span><span class="sxs-lookup"><span data-stu-id="f33e8-212">18</span></span></p></td>
<td><p><span data-ttu-id="f33e8-213">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 2 Bytes an (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="f33e8-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-215">17</span><span class="sxs-lookup"><span data-stu-id="f33e8-215">17</span></span></p></td>
<td><p><span data-ttu-id="f33e8-216">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 1 Byte an (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="f33e8-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-218">132</span><span class="sxs-lookup"><span data-stu-id="f33e8-218">132</span></span></p></td>
<td><p><span data-ttu-id="f33e8-219">Gibt eine benutzerdefinierte Variable an (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="f33e8-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-221">204</span><span class="sxs-lookup"><span data-stu-id="f33e8-221">204</span></span></p></td>
<td><p><span data-ttu-id="f33e8-222">Gibt einen Binärwert an (nur für <strong>Parameter</strong>-Objekt).</span><span class="sxs-lookup"><span data-stu-id="f33e8-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-224">200</span><span class="sxs-lookup"><span data-stu-id="f33e8-224">200</span></span></p></td>
<td><p><span data-ttu-id="f33e8-225">Gibt einen Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="f33e8-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-227">12</span><span class="sxs-lookup"><span data-stu-id="f33e8-227">12</span></span></p></td>
<td><p><span data-ttu-id="f33e8-228">Gibt ein Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="f33e8-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="f33e8-229"><strong>Hinweis</strong>: Dieser Datentyp wird derzeit nicht von ADO unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f33e8-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="f33e8-230">Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="f33e8-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-232">139</span><span class="sxs-lookup"><span data-stu-id="f33e8-232">139</span></span></p></td>
<td><p><span data-ttu-id="f33e8-233">Gibt einen numerischen Wert an (nur für <strong>Parameter</strong>-Objekt).</span><span class="sxs-lookup"><span data-stu-id="f33e8-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-235">202</span><span class="sxs-lookup"><span data-stu-id="f33e8-235">202</span></span></p></td>
<td><p><span data-ttu-id="f33e8-236">Gibt eine mit Null endende Unicode-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="f33e8-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f33e8-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f33e8-238">130</span><span class="sxs-lookup"><span data-stu-id="f33e8-238">130</span></span></p></td>
<td><p><span data-ttu-id="f33e8-239">Gibt eine mit Null endende Unicode-Zeichenfolge an (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="f33e8-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f33e8-240">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f33e8-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="f33e8-241">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f33e8-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f33e8-242">Konstante</span><span class="sxs-lookup"><span data-stu-id="f33e8-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="f33e8-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="f33e8-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="f33e8-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f33e8-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="f33e8-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="f33e8-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="f33e8-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="f33e8-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="f33e8-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="f33e8-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="f33e8-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="f33e8-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="f33e8-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="f33e8-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="f33e8-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="f33e8-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="f33e8-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="f33e8-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="f33e8-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="f33e8-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="f33e8-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="f33e8-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="f33e8-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="f33e8-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="f33e8-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f33e8-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="f33e8-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="f33e8-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="f33e8-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="f33e8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="f33e8-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="f33e8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="f33e8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="f33e8-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="f33e8-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="f33e8-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="f33e8-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="f33e8-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33e8-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="f33e8-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33e8-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="f33e8-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

