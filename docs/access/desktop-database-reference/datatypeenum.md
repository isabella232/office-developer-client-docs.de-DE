---
title: DataTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b70ad0067083373679286bdb452cb667d3de0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475331"
---
# <a name="datatypeenum"></a><span data-ttu-id="31fde-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="31fde-102">DataTypeEnum</span></span>


<span data-ttu-id="31fde-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="31fde-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="31fde-p101">Gibt den Datentyp eines [Felds](field-object-ado.md), eines [Parameters](parameter-object-ado.md) oder einer [Eigenschaft](property-object-ado.md) an. Der entsprechende OLE DB-Typindikator wird in der Beschreibungsspalte der folgenden Tabelle in Klammern angezeigt. Weitere Informationen zu OLE DB-Datentypen finden Sie in Kapitel 13 und in Anhang A der *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="31fde-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31fde-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="31fde-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="31fde-108">Wert</span><span class="sxs-lookup"><span data-stu-id="31fde-108">Value</span></span></p></th>
<th><p><span data-ttu-id="31fde-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31fde-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31fde-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="31fde-110"><strong>AdArray</span></span><br /><span data-ttu-id="31fde-111">
</strong>(Gilt nicht für ADOX.)</span><span class="sxs-lookup"><span data-stu-id="31fde-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="31fde-112">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="31fde-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="31fde-113">Ein Flagwert, immer kombiniert mit einer anderen Datentypkonstante, die einen Array dieses anderen Datentyps angibt.</span><span class="sxs-lookup"><span data-stu-id="31fde-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-115">20</span><span class="sxs-lookup"><span data-stu-id="31fde-115">20</span></span></p></td>
<td><p><span data-ttu-id="31fde-116">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 8 Bytes an (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="31fde-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-118">128</span><span class="sxs-lookup"><span data-stu-id="31fde-118">128</span></span></p></td>
<td><p><span data-ttu-id="31fde-119">Gibt einen Binärwert an (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="31fde-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-121">11</span><span class="sxs-lookup"><span data-stu-id="31fde-121">11</span></span></p></td>
<td><p><span data-ttu-id="31fde-122">Gibt einen booleschen Wert an (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="31fde-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-124">8</span><span class="sxs-lookup"><span data-stu-id="31fde-124">8</span></span></p></td>
<td><p><span data-ttu-id="31fde-125">Gibt eine mit Null endende Zeichenfolge (Unicode) an (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="31fde-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-127">136</span><span class="sxs-lookup"><span data-stu-id="31fde-127">136</span></span></p></td>
<td><p><span data-ttu-id="31fde-128">Gibt einen Kapitelwert mit 4 Bytes an, der Zeilen in einem untergeordneten Rowset (DBTYPE_HCHAPTER) kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31fde-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-130">129</span><span class="sxs-lookup"><span data-stu-id="31fde-130">129</span></span></p></td>
<td><p><span data-ttu-id="31fde-131">Gibt einen Zeichenfolgenwert an (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="31fde-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-133">6</span><span class="sxs-lookup"><span data-stu-id="31fde-133">6</span></span></p></td>
<td><p><span data-ttu-id="31fde-p102">Gibt einen Währungswert an (DBTYPE_CY). Die Währung ist eine Festkommazahl mit vier Ziffern rechts vom Dezimalkomma. Sie ist in einer ganzen Zahl mit Vorzeichen und einer Länge von 8 Bytes gespeichert, die um 10.000 skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="31fde-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-138">7</span><span class="sxs-lookup"><span data-stu-id="31fde-138">7</span></span></p></td>
<td><p><span data-ttu-id="31fde-p103">Gibt einen Datumswert an (DBTYPE_DATE). Ein Datum wird als Double gespeichert, wobei der ganze Teil davon die Zahl der Tage seit dem 30. Dezember 1899 und der Bruchteil davon den Teil des Tages darstellt.</span><span class="sxs-lookup"><span data-stu-id="31fde-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-142">133</span><span class="sxs-lookup"><span data-stu-id="31fde-142">133</span></span></p></td>
<td><p><span data-ttu-id="31fde-143">Gibt einen Datumswert (jjjjmmtt) an (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="31fde-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-145">134</span><span class="sxs-lookup"><span data-stu-id="31fde-145">134</span></span></p></td>
<td><p><span data-ttu-id="31fde-146">Gibt einen Zeitwert (hhmmss) an (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="31fde-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-148">135</span><span class="sxs-lookup"><span data-stu-id="31fde-148">135</span></span></p></td>
<td><p><span data-ttu-id="31fde-149">Gibt einen Datums-/Uhrzeitstempel (jjjjmmtthhmmss plus einen Bruchteil in Milliardstel) an (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="31fde-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-151">14</span><span class="sxs-lookup"><span data-stu-id="31fde-151">14</span></span></p></td>
<td><p><span data-ttu-id="31fde-152">Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="31fde-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-154">5</span><span class="sxs-lookup"><span data-stu-id="31fde-154">5</span></span></p></td>
<td><p><span data-ttu-id="31fde-155">Gibt einen Gleitkommawert mit doppelter Genauigkeit an (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="31fde-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-157">0</span><span class="sxs-lookup"><span data-stu-id="31fde-157">0</span></span></p></td>
<td><p><span data-ttu-id="31fde-158">Gibt keinen Wert an (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="31fde-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-160">10</span><span class="sxs-lookup"><span data-stu-id="31fde-160">10</span></span></p></td>
<td><p><span data-ttu-id="31fde-161">Gibt einen 32-Bit-Fehlercode an (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="31fde-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-163">64</span><span class="sxs-lookup"><span data-stu-id="31fde-163">64</span></span></p></td>
<td><p><span data-ttu-id="31fde-164">Gibt einen 64-Bit-Wert an, der die Zahl der 100-Nanosekunden-Intervalle seit 1. Januar 1601 darstellt (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="31fde-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-166">72</span><span class="sxs-lookup"><span data-stu-id="31fde-166">72</span></span></p></td>
<td><p><span data-ttu-id="31fde-167">Gibt einen global eindeutigen Bezeichner (GUID) an (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="31fde-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-169">9</span><span class="sxs-lookup"><span data-stu-id="31fde-169">9</span></span></p></td>
<td><p><span data-ttu-id="31fde-170">Gibt einen Zeiger auf eine <strong>IDispatch</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IDISPATCH).
</span><span class="sxs-lookup"><span data-stu-id="31fde-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="31fde-p104">Dieser Datentyp wird derzeit nicht von ADO unterstützt. Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="31fde-p104">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-174">3</span><span class="sxs-lookup"><span data-stu-id="31fde-174">3</span></span></p></td>
<td><p><span data-ttu-id="31fde-175">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 4 Bytes an (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="31fde-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-177">13</span><span class="sxs-lookup"><span data-stu-id="31fde-177">13</span></span></p></td>
<td><p><span data-ttu-id="31fde-178">Gibt einen Zeiger auf eine <strong>IUnknown</strong>-Schnittstelle in einem COM-Objekt an (DBTYPE_IUNKNOWN).
</span><span class="sxs-lookup"><span data-stu-id="31fde-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="31fde-p105">Dieser Datentyp wird derzeit nicht von ADO unterstützt. Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="31fde-p105">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-182">205</span><span class="sxs-lookup"><span data-stu-id="31fde-182">205</span></span></p></td>
<td><p><span data-ttu-id="31fde-183">Gibt einen langen Binärwert an.</span><span class="sxs-lookup"><span data-stu-id="31fde-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-185">201</span><span class="sxs-lookup"><span data-stu-id="31fde-185">201</span></span></p></td>
<td><p><span data-ttu-id="31fde-186">Gibt einen langen Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="31fde-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-188">203</span><span class="sxs-lookup"><span data-stu-id="31fde-188">203</span></span></p></td>
<td><p><span data-ttu-id="31fde-189">Gibt einen mit Null endenden Unicode-Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="31fde-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-191">131</span><span class="sxs-lookup"><span data-stu-id="31fde-191">131</span></span></p></td>
<td><p><span data-ttu-id="31fde-192">Gibt einen genauen numerischen Wert mit einer festen Genauigkeit und einem festen Maßstab an (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="31fde-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-194">138</span><span class="sxs-lookup"><span data-stu-id="31fde-194">138</span></span></p></td>
<td><p><span data-ttu-id="31fde-195">Gibt eine Automatisierungs-PROPVARIANT an (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="31fde-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-197">4</span><span class="sxs-lookup"><span data-stu-id="31fde-197">4</span></span></p></td>
<td><p><span data-ttu-id="31fde-198">Gibt einen Gleitkommawert mit einfacher Genauigkeit an (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="31fde-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-200">2</span><span class="sxs-lookup"><span data-stu-id="31fde-200">2</span></span></p></td>
<td><p><span data-ttu-id="31fde-201">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 2 Bytes an (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="31fde-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-203">16</span><span class="sxs-lookup"><span data-stu-id="31fde-203">16</span></span></p></td>
<td><p><span data-ttu-id="31fde-204">Gibt eine ganze Zahl mit Vorzeichen und einer Länge von 1 Byte an (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="31fde-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-206">21</span><span class="sxs-lookup"><span data-stu-id="31fde-206">21</span></span></p></td>
<td><p><span data-ttu-id="31fde-207">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 8 Bytes an (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="31fde-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-209">19</span><span class="sxs-lookup"><span data-stu-id="31fde-209">19</span></span></p></td>
<td><p><span data-ttu-id="31fde-210">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 4 Bytes an (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="31fde-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-212">18</span><span class="sxs-lookup"><span data-stu-id="31fde-212">18</span></span></p></td>
<td><p><span data-ttu-id="31fde-213">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 2 Bytes an (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="31fde-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-215">17</span><span class="sxs-lookup"><span data-stu-id="31fde-215">17</span></span></p></td>
<td><p><span data-ttu-id="31fde-216">Gibt eine ganze Zahl ohne Vorzeichen und mit einer Länge von 1 Byte an (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="31fde-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-218">132</span><span class="sxs-lookup"><span data-stu-id="31fde-218">132</span></span></p></td>
<td><p><span data-ttu-id="31fde-219">Gibt eine benutzerdefinierte Variable an (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="31fde-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-221">204</span><span class="sxs-lookup"><span data-stu-id="31fde-221">204</span></span></p></td>
<td><p><span data-ttu-id="31fde-222">Gibt einen Binärwert an (nur für <strong>Parameter</strong>-Objekt).</span><span class="sxs-lookup"><span data-stu-id="31fde-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-224">200</span><span class="sxs-lookup"><span data-stu-id="31fde-224">200</span></span></p></td>
<td><p><span data-ttu-id="31fde-225">Gibt einen Zeichenfolgenwert an.</span><span class="sxs-lookup"><span data-stu-id="31fde-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-227">12</span><span class="sxs-lookup"><span data-stu-id="31fde-227">12</span></span></p></td>
<td><p><span data-ttu-id="31fde-228">Gibt ein Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="31fde-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="31fde-p106">Dieser Datentyp wird derzeit nicht von ADO unterstützt. Seine Verwendung kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="31fde-p106">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-232">139</span><span class="sxs-lookup"><span data-stu-id="31fde-232">139</span></span></p></td>
<td><p><span data-ttu-id="31fde-233">Gibt einen numerischen Wert an (nur für <strong>Parameter</strong>-Objekt).</span><span class="sxs-lookup"><span data-stu-id="31fde-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-235">202</span><span class="sxs-lookup"><span data-stu-id="31fde-235">202</span></span></p></td>
<td><p><span data-ttu-id="31fde-236">Gibt eine mit Null endende Unicode-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="31fde-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="31fde-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="31fde-238">130</span><span class="sxs-lookup"><span data-stu-id="31fde-238">130</span></span></p></td>
<td><p><span data-ttu-id="31fde-239">Gibt eine mit Null endende Unicode-Zeichenfolge an (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="31fde-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31fde-240">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="31fde-240">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="31fde-241">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="31fde-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31fde-242">Konstante</span><span class="sxs-lookup"><span data-stu-id="31fde-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31fde-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="31fde-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="31fde-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="31fde-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="31fde-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="31fde-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="31fde-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="31fde-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="31fde-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="31fde-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="31fde-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="31fde-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="31fde-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="31fde-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="31fde-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="31fde-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="31fde-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="31fde-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="31fde-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="31fde-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="31fde-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="31fde-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="31fde-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="31fde-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="31fde-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="31fde-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="31fde-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="31fde-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="31fde-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="31fde-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="31fde-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="31fde-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="31fde-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="31fde-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="31fde-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="31fde-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="31fde-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="31fde-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="31fde-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31fde-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="31fde-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31fde-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="31fde-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

