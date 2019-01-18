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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703020"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="6f33f-102">CreateRecordset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="6f33f-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="6f33f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f33f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f33f-104">Erstellt ein leeres, getrenntes [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f33f-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f33f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f33f-105">Syntax</span></span>

<span data-ttu-id="6f33f-106">- *Objekt*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="6f33f-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6f33f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f33f-107">Parameters</span></span>

|<span data-ttu-id="6f33f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f33f-108">Parameter</span></span>|<span data-ttu-id="6f33f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f33f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6f33f-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="6f33f-110">*Object*</span></span> |<span data-ttu-id="6f33f-111">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)- oder [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6f33f-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="6f33f-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="6f33f-112">*ColumnsInfos*</span></span> |<span data-ttu-id="6f33f-113">Ein **Variant** -Array mit Attributen, das alle Spalten im erstellten **Recordset** -Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="6f33f-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="6f33f-114">Jede Spaltendefinition enthält ein Array mit vier erforderlichen Attributen und einem optionalen Attribut.</span><span class="sxs-lookup"><span data-stu-id="6f33f-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="6f33f-115">Der Satz der Spaltenarrays wird anschließend in einem Array gruppiert, das das **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="6f33f-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="6f33f-116">Eine Liste der Attribute finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6f33f-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="6f33f-117">Variant-Array-Attribute</span><span class="sxs-lookup"><span data-stu-id="6f33f-117">Variant array attributes</span></span>

|<span data-ttu-id="6f33f-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="6f33f-118">Attribute</span></span>|<span data-ttu-id="6f33f-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f33f-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6f33f-120">Name</span><span class="sxs-lookup"><span data-stu-id="6f33f-120">Name</span></span> |<span data-ttu-id="6f33f-121">Bezeichnung des Spaltenkopfs</span><span class="sxs-lookup"><span data-stu-id="6f33f-121">Name of the column header.</span></span>|
|<span data-ttu-id="6f33f-122">Type</span><span class="sxs-lookup"><span data-stu-id="6f33f-122">Type</span></span> |<span data-ttu-id="6f33f-123">Ganzzahl des Datentyps.</span><span class="sxs-lookup"><span data-stu-id="6f33f-123">Integer of the data type.</span></span>|
|<span data-ttu-id="6f33f-124">Size</span><span class="sxs-lookup"><span data-stu-id="6f33f-124">Size</span></span> |<span data-ttu-id="6f33f-125">Ganzzahl der Breite in Zeichen, unabhängig vom Datentyp.</span><span class="sxs-lookup"><span data-stu-id="6f33f-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="6f33f-126">Nullability</span><span class="sxs-lookup"><span data-stu-id="6f33f-126">Nullability</span></span> |<span data-ttu-id="6f33f-127">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="6f33f-127">Boolean value.</span></span>|
|<span data-ttu-id="6f33f-128">Skalierung (optional)</span><span class="sxs-lookup"><span data-stu-id="6f33f-128">Scale (optional)</span></span> |<span data-ttu-id="6f33f-p102">Dieses optionale Attribut definiert die Dezimalstellen von numerischen Feldern. Ist dieser Wert nicht angegeben, werden numerische Werte auf drei Dezimalstellen beschränkt. Dies wirkt sich nicht auf die Genauigkeit aus, die Anzahl der Ziffern nach dem Dezimaltrennzeichen ist jedoch auf drei Stellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6f33f-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6f33f-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f33f-132">Remarks</span></span>

<span data-ttu-id="6f33f-133">Das serverseitige Geschäftsobjekt kann das resultierende **Recordset** -Objekt mit Daten von einem Nicht-OLE DB-Datenanbieter wie einer Betriebssystemdatei, die Bestandsquoten enthält, auffüllen.</span><span class="sxs-lookup"><span data-stu-id="6f33f-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="6f33f-p103">In der folgenden Liste sind die [DataTypeEnum](datatypeenum.md)-Werte aufgeführt, die von der **CreateRecordset** -Methode unterstützt werden. Bei der angegebenen Zahl handelt es sich um die Referenznummer, die zum Definieren von Feldern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f33f-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="6f33f-p104">Die einzelnen Datentypen haben entweder eine feste oder eine variable Länge. Bei Typen mit fester Länge sollte die Größe auf den Wert -1 festgelegt werden, da die Größe vorher festgelegt werden muss und eine Definition der Größe noch erforderlich ist. Bei Datentypen mit variabler Länge ist eine Größe zwischen 1 und 32767 zulässig.</span><span class="sxs-lookup"><span data-stu-id="6f33f-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="6f33f-p105">Bei einigen Datentypen mit variabler Länge wird der Typ möglicherweise in den Typ umgewandelt, der in der Spalte Ersetzung angegeben ist. Diese Ersetzungen werden erst angezeigt, nachdem das Recordset-Objekt erstellt und aufgefüllt wurde. Anschließend können Sie bei Bedarf den tatsächlichen Datentyp anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6f33f-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f33f-142">Länge</span><span class="sxs-lookup"><span data-stu-id="6f33f-142">Length</span></span></p></th>
<th><p><span data-ttu-id="6f33f-143">Konstante</span><span class="sxs-lookup"><span data-stu-id="6f33f-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="6f33f-144">Zahl</span><span class="sxs-lookup"><span data-stu-id="6f33f-144">Number</span></span></p></th>
<th><p><span data-ttu-id="6f33f-145">Ersetzung</span><span class="sxs-lookup"><span data-stu-id="6f33f-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-146">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-148">16</span><span class="sxs-lookup"><span data-stu-id="6f33f-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-149">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-151">2</span><span class="sxs-lookup"><span data-stu-id="6f33f-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-152">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-154">3</span><span class="sxs-lookup"><span data-stu-id="6f33f-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-155">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-157">20</span><span class="sxs-lookup"><span data-stu-id="6f33f-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-158">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-160">17</span><span class="sxs-lookup"><span data-stu-id="6f33f-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-161">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-163">18</span><span class="sxs-lookup"><span data-stu-id="6f33f-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-164">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-166">19</span><span class="sxs-lookup"><span data-stu-id="6f33f-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-167">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-169">21</span><span class="sxs-lookup"><span data-stu-id="6f33f-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-170">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-172">4</span><span class="sxs-lookup"><span data-stu-id="6f33f-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-173">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-175">5</span><span class="sxs-lookup"><span data-stu-id="6f33f-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-176">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-178">6</span><span class="sxs-lookup"><span data-stu-id="6f33f-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-179">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-181">14</span><span class="sxs-lookup"><span data-stu-id="6f33f-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-182">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-184">131</span><span class="sxs-lookup"><span data-stu-id="6f33f-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-185">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-187">11</span><span class="sxs-lookup"><span data-stu-id="6f33f-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-188">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-190">10</span><span class="sxs-lookup"><span data-stu-id="6f33f-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-191">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-193">72</span><span class="sxs-lookup"><span data-stu-id="6f33f-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-194">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-196">7</span><span class="sxs-lookup"><span data-stu-id="6f33f-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-197">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-199">133</span><span class="sxs-lookup"><span data-stu-id="6f33f-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-200">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-202">134</span><span class="sxs-lookup"><span data-stu-id="6f33f-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-203">Fest</span><span class="sxs-lookup"><span data-stu-id="6f33f-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6f33f-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-205">135</span><span class="sxs-lookup"><span data-stu-id="6f33f-205">135</span></span></p></td>
<td><p><span data-ttu-id="6f33f-206">7</span><span class="sxs-lookup"><span data-stu-id="6f33f-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-207">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-209">8</span><span class="sxs-lookup"><span data-stu-id="6f33f-209">8</span></span></p></td>
<td><p><span data-ttu-id="6f33f-210">130</span><span class="sxs-lookup"><span data-stu-id="6f33f-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-211">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-213">129</span><span class="sxs-lookup"><span data-stu-id="6f33f-213">129</span></span></p></td>
<td><p><span data-ttu-id="6f33f-214">200</span><span class="sxs-lookup"><span data-stu-id="6f33f-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-215">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-217">200</span><span class="sxs-lookup"><span data-stu-id="6f33f-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-218">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-220">201</span><span class="sxs-lookup"><span data-stu-id="6f33f-220">201</span></span></p></td>
<td><p><span data-ttu-id="6f33f-221">200</span><span class="sxs-lookup"><span data-stu-id="6f33f-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-222">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-224">130</span><span class="sxs-lookup"><span data-stu-id="6f33f-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-225">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-227">202</span><span class="sxs-lookup"><span data-stu-id="6f33f-227">202</span></span></p></td>
<td><p><span data-ttu-id="6f33f-228">130</span><span class="sxs-lookup"><span data-stu-id="6f33f-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-229">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-231">203</span><span class="sxs-lookup"><span data-stu-id="6f33f-231">203</span></span></p></td>
<td><p><span data-ttu-id="6f33f-232">130</span><span class="sxs-lookup"><span data-stu-id="6f33f-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-233">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-235">128</span><span class="sxs-lookup"><span data-stu-id="6f33f-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f33f-236">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-238">204</span><span class="sxs-lookup"><span data-stu-id="6f33f-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f33f-239">Variabel</span><span class="sxs-lookup"><span data-stu-id="6f33f-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="6f33f-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6f33f-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6f33f-241">205</span><span class="sxs-lookup"><span data-stu-id="6f33f-241">205</span></span></p></td>
<td><p><span data-ttu-id="6f33f-242">204</span><span class="sxs-lookup"><span data-stu-id="6f33f-242">204</span></span></p></td>
</tr>
</tbody>
</table>

