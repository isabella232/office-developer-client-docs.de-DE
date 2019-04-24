---
title: FieldAttributeEnum (Access Desktop Database Reference)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292601"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="96550-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="96550-102">FieldAttributeEnum</span></span>

<span data-ttu-id="96550-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96550-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96550-104">Gibt mindestens ein Attribut eines [Field](field-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="96550-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96550-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="96550-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="96550-106">Wert</span><span class="sxs-lookup"><span data-stu-id="96550-106">Value</span></span></p></th>
<th><p><span data-ttu-id="96550-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96550-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96550-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="96550-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="96550-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="96550-110">Gibt an, dass der Anbieter Feldwerte zwischenspeichert und dass nachfolgende Lesevorgänge aus dem Cache durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="96550-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="96550-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-112">0x10</span><span class="sxs-lookup"><span data-stu-id="96550-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="96550-113">Gibt an, dass das Feld Daten fester Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="96550-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="96550-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="96550-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="96550-p101">Gibt an, dass das Feld einen Kapitelwert enthält, der ein bestimmtes untergeordnetes Recordset angibt, das sich auf dieses übergeordnete Feld bezieht. Kapitelfelder werden normalerweise zur Datenstrukturierung oder für Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="96550-p101">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field. Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="96550-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="96550-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="96550-120">Gibt an, dass das Feld angibt, dass die Ressource, die vom Datensatz dargestellt wird, eine Auflistung anderer Ressourcen ist, wie z. B. ein Ordner, statt eine einfache Ressource, wie z. B. eine Textdatei.</span><span class="sxs-lookup"><span data-stu-id="96550-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="96550-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="96550-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="96550-123">Gibt an, dass das Feld den Standarddatenstrom für die Ressource enthält, die vom Datensatz dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="96550-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="96550-124">Der Standarddatenstrom kann beispielsweise der HTML-Inhalt eines Stammordners auf einer Website sein, der automatisch bei Angabe der Stamm-URL bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="96550-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="96550-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-126">0x20</span><span class="sxs-lookup"><span data-stu-id="96550-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="96550-127">Gibt an, dass das Feld Nullwerte annimmt.</span><span class="sxs-lookup"><span data-stu-id="96550-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="96550-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-129">0x10000</span><span class="sxs-lookup"><span data-stu-id="96550-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="96550-130">Gibt an, dass das Feld die URL enthält, die die Ressource aus dem Datenspeicher bezeichnet, der vom Datensatz dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="96550-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="96550-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-132">0x80</span><span class="sxs-lookup"><span data-stu-id="96550-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="96550-p103">Gibt an, dass es sich bei dem Feld um ein langes binäres Feld handelt. Gibt außerdem an, dass Sie die Methoden <a href="appendchunk-method-ado.md">AppendChunk</a> und <a href="getchunk-method-ado.md">GetChunk</a> verwenden können.</span><span class="sxs-lookup"><span data-stu-id="96550-p103">Indicates that the field is a long binary field. Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="96550-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-136">0x40</span><span class="sxs-lookup"><span data-stu-id="96550-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="96550-137">Gibt an, dass Sie Nullwerte aus dem Feld lesen können.</span><span class="sxs-lookup"><span data-stu-id="96550-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="96550-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-139">0x2</span><span class="sxs-lookup"><span data-stu-id="96550-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="96550-140">Gibt an, dass das Feld verzögert ist – das heißt, die Feldwerte werden von der Datenquelle nicht mit dem gesamten Datensatz abgerufen, sondern nur, wenn Sie ausdrücklich darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="96550-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="96550-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="96550-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="96550-p104">Gibt an, dass das Feld einen numerischen Wert aus einer Spalte darstellt, die negative Skalierungswerte unterstützt. Der Maßstab wird durch die <a href="numericscale-property-ado.md">NumericScale</a>-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="96550-p104">Indicates that the field represents a numeric value from a column that supports negative scale values. The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="96550-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-146">0x100</span><span class="sxs-lookup"><span data-stu-id="96550-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="96550-147">Gibt an, dass das Feld einen permanenten Zeilenbezeichner enthält, in den nicht geschrieben werden kann und der keinen Zweck hat, außer die Zeile zu identifizieren (wie Datensatznummer, eindeutiger Bezeichner usw.).</span><span class="sxs-lookup"><span data-stu-id="96550-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="96550-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-149">0x200</span><span class="sxs-lookup"><span data-stu-id="96550-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="96550-150">Gibt an, dass das Feld einen Zeit- und Datumstempel zum Verfolgen von Aktualisierungen enthält.</span><span class="sxs-lookup"><span data-stu-id="96550-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="96550-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-152">0x8</span><span class="sxs-lookup"><span data-stu-id="96550-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="96550-153">Gibt an, dass der Anbieter nicht ermitteln kann, ob Sie in das Feld schreiben können.</span><span class="sxs-lookup"><span data-stu-id="96550-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="96550-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-155">-1</span><span class="sxs-lookup"><span data-stu-id="96550-155">-1</span></span><br />
<span data-ttu-id="96550-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="96550-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="96550-157">Gibt an, dass der Anbieter die Feldattribute nicht angibt.</span><span class="sxs-lookup"><span data-stu-id="96550-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="96550-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="96550-159">0x4</span><span class="sxs-lookup"><span data-stu-id="96550-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="96550-160">Gibt an, dass Sie in das Feld schreiben können.</span><span class="sxs-lookup"><span data-stu-id="96550-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="96550-161">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="96550-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="96550-162">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="96550-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96550-163">Konstante</span><span class="sxs-lookup"><span data-stu-id="96550-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96550-164">AdoEnums. Fieldattribute. CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="96550-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-165">AdoEnums. Fieldattribute. FIXED</span><span class="sxs-lookup"><span data-stu-id="96550-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-166">AdoEnums. Fieldattribute. isNULLable</span><span class="sxs-lookup"><span data-stu-id="96550-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-167">AdoEnums. Fieldattribute. LONG</span><span class="sxs-lookup"><span data-stu-id="96550-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-168">AdoEnums. Fieldattribute. MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="96550-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-169">AdoEnums. Fieldattribute. MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="96550-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-170">AdoEnums. Fieldattribute. NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="96550-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-171">AdoEnums. Fieldattribute. ROWID</span><span class="sxs-lookup"><span data-stu-id="96550-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-172">AdoEnums. Fieldattribute. ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="96550-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-173">AdoEnums. Fieldattribute. UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="96550-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96550-174">AdoEnums. Fieldattribute. unSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="96550-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96550-175">AdoEnums. Fieldattribute. AKTUALISIERBAR</span><span class="sxs-lookup"><span data-stu-id="96550-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

