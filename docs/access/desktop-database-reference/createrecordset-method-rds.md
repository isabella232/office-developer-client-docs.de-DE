---
title: CreateRecordset-Methode (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d975faf45cf6a16bdae9f800084ebbbbaec3127d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868532"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="96713-102">CreateRecordset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="96713-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="96713-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96713-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="96713-104">Erstellt ein leeres, getrenntes [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="96713-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="96713-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96713-105">Syntax</span></span>

<span data-ttu-id="96713-106">- *Objekt*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="96713-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="96713-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="96713-107">Parameters</span></span>

  - <span data-ttu-id="96713-108">*Object*</span><span class="sxs-lookup"><span data-stu-id="96713-108">*Object*</span></span>

  - <span data-ttu-id="96713-109">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)- oder [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="96713-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="96713-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="96713-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="96713-p101">Ein **Variant** -Array mit Attributen, das alle Spalten im erstellten **Recordset** -Objekt definiert. Jede Spaltendefinition enthält ein Array mit vier erforderlichen Attributen und einem optionalen Attribut. Der Satz der Spaltenarrays wird anschließend in einem Array gruppiert, das das **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="96713-p101">A **Variant** array of attributes that defines each column in the **Recordset** created. Each column definition contains an array of four required attributes and one optional attribute. The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="96713-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="96713-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="96713-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96713-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="96713-116">Name</span><span class="sxs-lookup"><span data-stu-id="96713-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="96713-117">Bezeichnung des Spaltenkopfs</span><span class="sxs-lookup"><span data-stu-id="96713-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="96713-118">Type</span><span class="sxs-lookup"><span data-stu-id="96713-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="96713-119">Ganzzahl des Datentyps.</span><span class="sxs-lookup"><span data-stu-id="96713-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="96713-120">Size</span><span class="sxs-lookup"><span data-stu-id="96713-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="96713-121">Ganzzahl der Breite in Zeichen, unabhängig vom Datentyp.</span><span class="sxs-lookup"><span data-stu-id="96713-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="96713-122">Nullability</span><span class="sxs-lookup"><span data-stu-id="96713-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="96713-123">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="96713-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="96713-124">Skalieren</span><span class="sxs-lookup"><span data-stu-id="96713-124">Scale</span></span><br />
<span data-ttu-id="96713-125">(Optional)</span><span class="sxs-lookup"><span data-stu-id="96713-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="96713-p102">Dieses optionale Attribut definiert die Dezimalstellen von numerischen Feldern. Ist dieser Wert nicht angegeben, werden numerische Werte auf drei Dezimalstellen beschränkt. Dies wirkt sich nicht auf die Genauigkeit aus, die Anzahl der Ziffern nach dem Dezimaltrennzeichen ist jedoch auf drei Stellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="96713-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="96713-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96713-129">Remarks</span></span>

<span data-ttu-id="96713-130">Das serverseitige Geschäftsobjekt kann das resultierende **Recordset** -Objekt mit Daten von einem Nicht-OLE DB-Datenanbieter wie einer Betriebssystemdatei, die Bestandsquoten enthält, auffüllen.</span><span class="sxs-lookup"><span data-stu-id="96713-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="96713-p103">In der folgenden Liste sind die [DataTypeEnum](datatypeenum.md)-Werte aufgeführt, die von der **CreateRecordset** -Methode unterstützt werden. Bei der angegebenen Zahl handelt es sich um die Referenznummer, die zum Definieren von Feldern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96713-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="96713-p104">Die einzelnen Datentypen haben entweder eine feste oder eine variable Länge. Bei Typen mit fester Länge sollte die Größe auf den Wert -1 festgelegt werden, da die Größe vorher festgelegt werden muss und eine Definition der Größe noch erforderlich ist. Bei Datentypen mit variabler Länge ist eine Größe zwischen 1 und 32767 zulässig.</span><span class="sxs-lookup"><span data-stu-id="96713-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="96713-p105">Bei einigen Datentypen mit variabler Länge wird der Typ möglicherweise in den Typ umgewandelt, der in der Spalte Ersetzung angegeben ist. Diese Ersetzungen werden erst angezeigt, nachdem das Recordset-Objekt erstellt und aufgefüllt wurde. Anschließend können Sie bei Bedarf den tatsächlichen Datentyp anzeigen.</span><span class="sxs-lookup"><span data-stu-id="96713-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96713-139">Länge</span><span class="sxs-lookup"><span data-stu-id="96713-139">Length</span></span></p></th>
<th><p><span data-ttu-id="96713-140">Konstante</span><span class="sxs-lookup"><span data-stu-id="96713-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="96713-141">Zahl</span><span class="sxs-lookup"><span data-stu-id="96713-141">Number</span></span></p></th>
<th><p><span data-ttu-id="96713-142">Ersetzung</span><span class="sxs-lookup"><span data-stu-id="96713-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96713-143">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="96713-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-145">16</span><span class="sxs-lookup"><span data-stu-id="96713-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-146">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="96713-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-148">2</span><span class="sxs-lookup"><span data-stu-id="96713-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-149">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-150"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="96713-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-151">3</span><span class="sxs-lookup"><span data-stu-id="96713-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-152">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="96713-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-154">20</span><span class="sxs-lookup"><span data-stu-id="96713-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-155">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="96713-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-157">17</span><span class="sxs-lookup"><span data-stu-id="96713-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-158">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="96713-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-160">18</span><span class="sxs-lookup"><span data-stu-id="96713-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-161">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="96713-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-163">19</span><span class="sxs-lookup"><span data-stu-id="96713-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-164">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="96713-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-166">21</span><span class="sxs-lookup"><span data-stu-id="96713-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-167">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="96713-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-169">4</span><span class="sxs-lookup"><span data-stu-id="96713-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-170">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-171"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="96713-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-172">5</span><span class="sxs-lookup"><span data-stu-id="96713-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-173">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="96713-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-175">6</span><span class="sxs-lookup"><span data-stu-id="96713-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-176">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="96713-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-178">14</span><span class="sxs-lookup"><span data-stu-id="96713-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-179">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="96713-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-181">131</span><span class="sxs-lookup"><span data-stu-id="96713-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-182">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="96713-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-184">11</span><span class="sxs-lookup"><span data-stu-id="96713-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-185">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="96713-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-187">10</span><span class="sxs-lookup"><span data-stu-id="96713-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-188">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="96713-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-190">72</span><span class="sxs-lookup"><span data-stu-id="96713-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-191">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="96713-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-193">7</span><span class="sxs-lookup"><span data-stu-id="96713-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-194">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="96713-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-196">133</span><span class="sxs-lookup"><span data-stu-id="96713-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-197">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="96713-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-199">134</span><span class="sxs-lookup"><span data-stu-id="96713-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-200">Fest</span><span class="sxs-lookup"><span data-stu-id="96713-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="96713-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="96713-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-202">135</span><span class="sxs-lookup"><span data-stu-id="96713-202">135</span></span></p></td>
<td><p><span data-ttu-id="96713-203">7</span><span class="sxs-lookup"><span data-stu-id="96713-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-204">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="96713-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-206">8</span><span class="sxs-lookup"><span data-stu-id="96713-206">8</span></span></p></td>
<td><p><span data-ttu-id="96713-207">130</span><span class="sxs-lookup"><span data-stu-id="96713-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-208">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-209"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="96713-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-210">129</span><span class="sxs-lookup"><span data-stu-id="96713-210">129</span></span></p></td>
<td><p><span data-ttu-id="96713-211">200</span><span class="sxs-lookup"><span data-stu-id="96713-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-212">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-213"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="96713-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-214">200</span><span class="sxs-lookup"><span data-stu-id="96713-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-215">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="96713-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-217">201</span><span class="sxs-lookup"><span data-stu-id="96713-217">201</span></span></p></td>
<td><p><span data-ttu-id="96713-218">200</span><span class="sxs-lookup"><span data-stu-id="96713-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-219">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="96713-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-221">130</span><span class="sxs-lookup"><span data-stu-id="96713-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-222">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="96713-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-224">202</span><span class="sxs-lookup"><span data-stu-id="96713-224">202</span></span></p></td>
<td><p><span data-ttu-id="96713-225">130</span><span class="sxs-lookup"><span data-stu-id="96713-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-226">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="96713-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-228">203</span><span class="sxs-lookup"><span data-stu-id="96713-228">203</span></span></p></td>
<td><p><span data-ttu-id="96713-229">130</span><span class="sxs-lookup"><span data-stu-id="96713-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-230">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="96713-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-232">128</span><span class="sxs-lookup"><span data-stu-id="96713-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96713-233">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="96713-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-235">204</span><span class="sxs-lookup"><span data-stu-id="96713-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96713-236">Variabel</span><span class="sxs-lookup"><span data-stu-id="96713-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="96713-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="96713-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="96713-238">205</span><span class="sxs-lookup"><span data-stu-id="96713-238">205</span></span></p></td>
<td><p><span data-ttu-id="96713-239">204</span><span class="sxs-lookup"><span data-stu-id="96713-239">204</span></span></p></td>
</tr>
</tbody>
</table>

