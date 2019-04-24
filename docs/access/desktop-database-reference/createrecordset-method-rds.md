---
title: CreateRecordset-Methode (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295338"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="5a99a-102">CreateRecordset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="5a99a-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="5a99a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a99a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a99a-104">Erstellt ein leeres, getrenntes [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5a99a-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a99a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a99a-105">Syntax</span></span>

<span data-ttu-id="5a99a-106">- *Objekt*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="5a99a-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="5a99a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a99a-107">Parameters</span></span>

|<span data-ttu-id="5a99a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a99a-108">Parameter</span></span>|<span data-ttu-id="5a99a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a99a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5a99a-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="5a99a-110">*Object*</span></span> |<span data-ttu-id="5a99a-111">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)- oder [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a99a-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="5a99a-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="5a99a-112">*ColumnsInfos*</span></span> |<span data-ttu-id="5a99a-113">Ein **Variant** -Array mit Attributen, das alle Spalten im erstellten **Recordset** -Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="5a99a-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="5a99a-114">Jede Spaltendefinition enthält ein Array mit vier erforderlichen Attributen und einem optionalen Attribut.</span><span class="sxs-lookup"><span data-stu-id="5a99a-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="5a99a-115">Der Satz der Spaltenarrays wird anschließend in einem Array gruppiert, das das **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="5a99a-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="5a99a-116">Eine Liste der Attribute finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a99a-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="5a99a-117">Variant-Array Attribute</span><span class="sxs-lookup"><span data-stu-id="5a99a-117">Variant array attributes</span></span>

|<span data-ttu-id="5a99a-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="5a99a-118">Attribute</span></span>|<span data-ttu-id="5a99a-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a99a-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5a99a-120">Name</span><span class="sxs-lookup"><span data-stu-id="5a99a-120">Name</span></span> |<span data-ttu-id="5a99a-121">Bezeichnung des Spaltenkopfs</span><span class="sxs-lookup"><span data-stu-id="5a99a-121">Name of the column header.</span></span>|
|<span data-ttu-id="5a99a-122">Typ</span><span class="sxs-lookup"><span data-stu-id="5a99a-122">Type</span></span> |<span data-ttu-id="5a99a-123">Ganzzahl des Datentyps.</span><span class="sxs-lookup"><span data-stu-id="5a99a-123">Integer of the data type.</span></span>|
|<span data-ttu-id="5a99a-124">Größe</span><span class="sxs-lookup"><span data-stu-id="5a99a-124">Size</span></span> |<span data-ttu-id="5a99a-125">Ganzzahl der Breite in Zeichen, unabhängig vom Datentyp.</span><span class="sxs-lookup"><span data-stu-id="5a99a-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="5a99a-126">Zulässigkeit</span><span class="sxs-lookup"><span data-stu-id="5a99a-126">Nullability</span></span> |<span data-ttu-id="5a99a-127">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="5a99a-127">Boolean value.</span></span>|
|<span data-ttu-id="5a99a-128">Skalierung (optional)</span><span class="sxs-lookup"><span data-stu-id="5a99a-128">Scale (optional)</span></span> |<span data-ttu-id="5a99a-p102">Dieses optionale Attribut definiert die Dezimalstellen von numerischen Feldern. Ist dieser Wert nicht angegeben, werden numerische Werte auf drei Dezimalstellen beschränkt. Dies wirkt sich nicht auf die Genauigkeit aus, die Anzahl der Ziffern nach dem Dezimaltrennzeichen ist jedoch auf drei Stellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="5a99a-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5a99a-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a99a-132">Remarks</span></span>

<span data-ttu-id="5a99a-133">Das serverseitige Geschäftsobjekt kann das resultierende **Recordset**-Objekt mit Daten von einem Nicht-OLE DB-Datenanbieter wie einer Betriebssystemdatei, die Bestandsquoten enthält, auffüllen.</span><span class="sxs-lookup"><span data-stu-id="5a99a-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="5a99a-p103">In der folgenden Liste sind die [DataTypeEnum](datatypeenum.md)-Werte aufgeführt, die von der **CreateRecordset** -Methode unterstützt werden. Bei der angegebenen Zahl handelt es sich um die Referenznummer, die zum Definieren von Feldern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a99a-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="5a99a-p104">Die einzelnen Datentypen haben entweder eine feste oder eine variable Länge. Bei Typen mit fester Länge sollte die Größe auf den Wert -1 festgelegt werden, da die Größe vorher festgelegt werden muss und eine Definition der Größe noch erforderlich ist. Bei Datentypen mit variabler Länge ist eine Größe zwischen 1 und 32767 zulässig.</span><span class="sxs-lookup"><span data-stu-id="5a99a-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="5a99a-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span><span class="sxs-lookup"><span data-stu-id="5a99a-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a99a-142">Länge</span><span class="sxs-lookup"><span data-stu-id="5a99a-142">Length</span></span></p></th>
<th><p><span data-ttu-id="5a99a-143">Konstante</span><span class="sxs-lookup"><span data-stu-id="5a99a-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="5a99a-144">Zahl</span><span class="sxs-lookup"><span data-stu-id="5a99a-144">Number</span></span></p></th>
<th><p><span data-ttu-id="5a99a-145">Ersetzung</span><span class="sxs-lookup"><span data-stu-id="5a99a-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-146">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-147"><strong>addTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-148">16</span><span class="sxs-lookup"><span data-stu-id="5a99a-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-149">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-150"><strong>SmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-151">2</span><span class="sxs-lookup"><span data-stu-id="5a99a-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-152">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-153"><strong>Ganzzahl</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-154">3</span><span class="sxs-lookup"><span data-stu-id="5a99a-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-155">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-156"><strong>Bigint</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-157">20</span><span class="sxs-lookup"><span data-stu-id="5a99a-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-158">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-160">17</span><span class="sxs-lookup"><span data-stu-id="5a99a-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-161">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-163">18</span><span class="sxs-lookup"><span data-stu-id="5a99a-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-164">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-166">19</span><span class="sxs-lookup"><span data-stu-id="5a99a-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-167">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-169">21</span><span class="sxs-lookup"><span data-stu-id="5a99a-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-170">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-171"><strong>Einzel</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-172">4</span><span class="sxs-lookup"><span data-stu-id="5a99a-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-173">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-175">5</span><span class="sxs-lookup"><span data-stu-id="5a99a-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-176">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-177"><strong>Währung</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-178">6</span><span class="sxs-lookup"><span data-stu-id="5a99a-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-179">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-181">14</span><span class="sxs-lookup"><span data-stu-id="5a99a-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-182">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-184">131</span><span class="sxs-lookup"><span data-stu-id="5a99a-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-185">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-186"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-187">11</span><span class="sxs-lookup"><span data-stu-id="5a99a-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-188">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-189"><strong>Fehler</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-190">10</span><span class="sxs-lookup"><span data-stu-id="5a99a-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-191">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-192"><strong>GUID</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-193">72</span><span class="sxs-lookup"><span data-stu-id="5a99a-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-194">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-195"><strong>Datum</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-196">7</span><span class="sxs-lookup"><span data-stu-id="5a99a-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-197">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-199">133</span><span class="sxs-lookup"><span data-stu-id="5a99a-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-200">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-202">134</span><span class="sxs-lookup"><span data-stu-id="5a99a-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-203">Fest</span><span class="sxs-lookup"><span data-stu-id="5a99a-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5a99a-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-205">135</span><span class="sxs-lookup"><span data-stu-id="5a99a-205">135</span></span></p></td>
<td><p><span data-ttu-id="5a99a-206">7</span><span class="sxs-lookup"><span data-stu-id="5a99a-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-207">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-208"><strong>-BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-209">8</span><span class="sxs-lookup"><span data-stu-id="5a99a-209">8</span></span></p></td>
<td><p><span data-ttu-id="5a99a-210">130</span><span class="sxs-lookup"><span data-stu-id="5a99a-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-211">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-212"><strong>Char</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-213">129</span><span class="sxs-lookup"><span data-stu-id="5a99a-213">129</span></span></p></td>
<td><p><span data-ttu-id="5a99a-214">200</span><span class="sxs-lookup"><span data-stu-id="5a99a-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-215">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-216"><strong>-VarChar</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-217">200</span><span class="sxs-lookup"><span data-stu-id="5a99a-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-218">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-220">201</span><span class="sxs-lookup"><span data-stu-id="5a99a-220">201</span></span></p></td>
<td><p><span data-ttu-id="5a99a-221">200</span><span class="sxs-lookup"><span data-stu-id="5a99a-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-222">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-224">130</span><span class="sxs-lookup"><span data-stu-id="5a99a-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-225">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-227">202</span><span class="sxs-lookup"><span data-stu-id="5a99a-227">202</span></span></p></td>
<td><p><span data-ttu-id="5a99a-228">130</span><span class="sxs-lookup"><span data-stu-id="5a99a-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-229">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-231">203</span><span class="sxs-lookup"><span data-stu-id="5a99a-231">203</span></span></p></td>
<td><p><span data-ttu-id="5a99a-232">130</span><span class="sxs-lookup"><span data-stu-id="5a99a-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-233">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-234"><strong>die Binärdatei</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-235">128</span><span class="sxs-lookup"><span data-stu-id="5a99a-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a99a-236">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-237"><strong>VarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-238">204</span><span class="sxs-lookup"><span data-stu-id="5a99a-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a99a-239">Variable</span><span class="sxs-lookup"><span data-stu-id="5a99a-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="5a99a-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5a99a-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5a99a-241">205</span><span class="sxs-lookup"><span data-stu-id="5a99a-241">205</span></span></p></td>
<td><p><span data-ttu-id="5a99a-242">204</span><span class="sxs-lookup"><span data-stu-id="5a99a-242">204</span></span></p></td>
</tr>
</tbody>
</table>

