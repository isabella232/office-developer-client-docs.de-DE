---
title: CreateRecordset-Methode (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b4d68ac2dfca344cb98885846f2cd09fafd0ea0
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950237"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="e8760-102">CreateRecordset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="e8760-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="e8760-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8760-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8760-104">Erstellt ein leeres, getrenntes [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e8760-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8760-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8760-105">Syntax</span></span>

<span data-ttu-id="e8760-106">- *Objekt*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="e8760-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="e8760-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8760-107">Parameters</span></span>

|<span data-ttu-id="e8760-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8760-108">Parameter</span></span>|<span data-ttu-id="e8760-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8760-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e8760-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="e8760-110">*Object*</span></span> |<span data-ttu-id="e8760-111">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)- oder [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e8760-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="e8760-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="e8760-112">*ColumnsInfos*</span></span> |<span data-ttu-id="e8760-113">Ein **Variant** -Array mit Attributen, das alle Spalten im erstellten **Recordset** -Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="e8760-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="e8760-114">Jede Spaltendefinition enthält ein Array mit vier erforderlichen Attributen und einem optionalen Attribut.</span><span class="sxs-lookup"><span data-stu-id="e8760-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="e8760-115">Der Satz der Spaltenarrays wird anschließend in einem Array gruppiert, das das **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="e8760-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="e8760-116">Eine Liste der Attribute finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e8760-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="e8760-117">Variant-Array-Attribute</span><span class="sxs-lookup"><span data-stu-id="e8760-117">Variant array attributes</span></span>

|<span data-ttu-id="e8760-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="e8760-118">Attribute</span></span>|<span data-ttu-id="e8760-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8760-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e8760-120">Name</span><span class="sxs-lookup"><span data-stu-id="e8760-120">Name</span></span> |<span data-ttu-id="e8760-121">Bezeichnung des Spaltenkopfs</span><span class="sxs-lookup"><span data-stu-id="e8760-121">Name of the column header.</span></span>|
|<span data-ttu-id="e8760-122">Type</span><span class="sxs-lookup"><span data-stu-id="e8760-122">Type</span></span> |<span data-ttu-id="e8760-123">Ganzzahl des Datentyps.</span><span class="sxs-lookup"><span data-stu-id="e8760-123">Integer of the data type.</span></span>|
|<span data-ttu-id="e8760-124">Size</span><span class="sxs-lookup"><span data-stu-id="e8760-124">Size</span></span> |<span data-ttu-id="e8760-125">Ganzzahl der Breite in Zeichen, unabhängig vom Datentyp.</span><span class="sxs-lookup"><span data-stu-id="e8760-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="e8760-126">Nullability</span><span class="sxs-lookup"><span data-stu-id="e8760-126">Nullability</span></span> |<span data-ttu-id="e8760-127">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="e8760-127">Boolean value.</span></span>|
|<span data-ttu-id="e8760-128">Skalierung (optional)</span><span class="sxs-lookup"><span data-stu-id="e8760-128">Scale (optional)</span></span> |<span data-ttu-id="e8760-p102">Dieses optionale Attribut definiert die Dezimalstellen von numerischen Feldern. Ist dieser Wert nicht angegeben, werden numerische Werte auf drei Dezimalstellen beschränkt. Dies wirkt sich nicht auf die Genauigkeit aus, die Anzahl der Ziffern nach dem Dezimaltrennzeichen ist jedoch auf drei Stellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="e8760-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e8760-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8760-132">Remarks</span></span>

<span data-ttu-id="e8760-133">Das serverseitige Geschäftsobjekt kann das resultierende **Recordset** -Objekt mit Daten von einem Nicht-OLE DB-Datenanbieter wie einer Betriebssystemdatei, die Bestandsquoten enthält, auffüllen.</span><span class="sxs-lookup"><span data-stu-id="e8760-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="e8760-p103">In der folgenden Liste sind die [DataTypeEnum](datatypeenum.md)-Werte aufgeführt, die von der **CreateRecordset** -Methode unterstützt werden. Bei der angegebenen Zahl handelt es sich um die Referenznummer, die zum Definieren von Feldern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8760-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="e8760-p104">Die einzelnen Datentypen haben entweder eine feste oder eine variable Länge. Bei Typen mit fester Länge sollte die Größe auf den Wert -1 festgelegt werden, da die Größe vorher festgelegt werden muss und eine Definition der Größe noch erforderlich ist. Bei Datentypen mit variabler Länge ist eine Größe zwischen 1 und 32767 zulässig.</span><span class="sxs-lookup"><span data-stu-id="e8760-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="e8760-p105">Bei einigen Datentypen mit variabler Länge wird der Typ möglicherweise in den Typ umgewandelt, der in der Spalte Ersetzung angegeben ist. Diese Ersetzungen werden erst angezeigt, nachdem das Recordset-Objekt erstellt und aufgefüllt wurde. Anschließend können Sie bei Bedarf den tatsächlichen Datentyp anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e8760-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8760-142">Länge</span><span class="sxs-lookup"><span data-stu-id="e8760-142">Length</span></span></p></th>
<th><p><span data-ttu-id="e8760-143">Konstante</span><span class="sxs-lookup"><span data-stu-id="e8760-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="e8760-144">Zahl</span><span class="sxs-lookup"><span data-stu-id="e8760-144">Number</span></span></p></th>
<th><p><span data-ttu-id="e8760-145">Ersetzung</span><span class="sxs-lookup"><span data-stu-id="e8760-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8760-146">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-148">16</span><span class="sxs-lookup"><span data-stu-id="e8760-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-149">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-151">2</span><span class="sxs-lookup"><span data-stu-id="e8760-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-152">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-154">3</span><span class="sxs-lookup"><span data-stu-id="e8760-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-155">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-157">20</span><span class="sxs-lookup"><span data-stu-id="e8760-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-158">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-160">17</span><span class="sxs-lookup"><span data-stu-id="e8760-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-161">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-163">18</span><span class="sxs-lookup"><span data-stu-id="e8760-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-164">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-166">19</span><span class="sxs-lookup"><span data-stu-id="e8760-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-167">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-169">21</span><span class="sxs-lookup"><span data-stu-id="e8760-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-170">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-172">4</span><span class="sxs-lookup"><span data-stu-id="e8760-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-173">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-175">5</span><span class="sxs-lookup"><span data-stu-id="e8760-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-176">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-178">6</span><span class="sxs-lookup"><span data-stu-id="e8760-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-179">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-181">14</span><span class="sxs-lookup"><span data-stu-id="e8760-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-182">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-184">131</span><span class="sxs-lookup"><span data-stu-id="e8760-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-185">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-187">11</span><span class="sxs-lookup"><span data-stu-id="e8760-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-188">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-190">10</span><span class="sxs-lookup"><span data-stu-id="e8760-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-191">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-193">72</span><span class="sxs-lookup"><span data-stu-id="e8760-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-194">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-196">7</span><span class="sxs-lookup"><span data-stu-id="e8760-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-197">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-199">133</span><span class="sxs-lookup"><span data-stu-id="e8760-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-200">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-202">134</span><span class="sxs-lookup"><span data-stu-id="e8760-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-203">Fest</span><span class="sxs-lookup"><span data-stu-id="e8760-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e8760-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-205">135</span><span class="sxs-lookup"><span data-stu-id="e8760-205">135</span></span></p></td>
<td><p><span data-ttu-id="e8760-206">7</span><span class="sxs-lookup"><span data-stu-id="e8760-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-207">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-209">8</span><span class="sxs-lookup"><span data-stu-id="e8760-209">8</span></span></p></td>
<td><p><span data-ttu-id="e8760-210">130</span><span class="sxs-lookup"><span data-stu-id="e8760-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-211">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-213">129</span><span class="sxs-lookup"><span data-stu-id="e8760-213">129</span></span></p></td>
<td><p><span data-ttu-id="e8760-214">200</span><span class="sxs-lookup"><span data-stu-id="e8760-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-215">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-217">200</span><span class="sxs-lookup"><span data-stu-id="e8760-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-218">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-220">201</span><span class="sxs-lookup"><span data-stu-id="e8760-220">201</span></span></p></td>
<td><p><span data-ttu-id="e8760-221">200</span><span class="sxs-lookup"><span data-stu-id="e8760-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-222">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-224">130</span><span class="sxs-lookup"><span data-stu-id="e8760-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-225">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-227">202</span><span class="sxs-lookup"><span data-stu-id="e8760-227">202</span></span></p></td>
<td><p><span data-ttu-id="e8760-228">130</span><span class="sxs-lookup"><span data-stu-id="e8760-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-229">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-231">203</span><span class="sxs-lookup"><span data-stu-id="e8760-231">203</span></span></p></td>
<td><p><span data-ttu-id="e8760-232">130</span><span class="sxs-lookup"><span data-stu-id="e8760-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-233">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-235">128</span><span class="sxs-lookup"><span data-stu-id="e8760-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8760-236">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-238">204</span><span class="sxs-lookup"><span data-stu-id="e8760-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8760-239">Variabel</span><span class="sxs-lookup"><span data-stu-id="e8760-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="e8760-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e8760-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e8760-241">205</span><span class="sxs-lookup"><span data-stu-id="e8760-241">205</span></span></p></td>
<td><p><span data-ttu-id="e8760-242">204</span><span class="sxs-lookup"><span data-stu-id="e8760-242">204</span></span></p></td>
</tr>
</tbody>
</table>

