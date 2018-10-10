---
title: CreateRecordset-Methode (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 696daaeb060387d5f3ca454ef665517a8ff7be74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472897"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="2cbc0-102">CreateRecordset-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="2cbc0-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="2cbc0-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cbc0-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2cbc0-104">Erstellt ein leeres, getrenntes [Recordset](recordset-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbc0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cbc0-105">Syntax</span></span>

<span data-ttu-id="2cbc0-106">- *Objekt*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="2cbc0-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="2cbc0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cbc0-107">Parameters</span></span>

  - <span data-ttu-id="2cbc0-108">*Object*</span><span class="sxs-lookup"><span data-stu-id="2cbc0-108">*Object*</span></span>

  - <span data-ttu-id="2cbc0-109">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)- oder [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="2cbc0-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="2cbc0-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="2cbc0-p101">Ein **Variant** -Array mit Attributen, das alle Spalten im erstellten **Recordset** -Objekt definiert. Jede Spaltendefinition enthält ein Array mit vier erforderlichen Attributen und einem optionalen Attribut. Der Satz der Spaltenarrays wird anschließend in einem Array gruppiert, das das **Recordset** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-p101">A **Variant** array of attributes that defines each column in the **Recordset** created. Each column definition contains an array of four required attributes and one optional attribute. The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="2cbc0-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="2cbc0-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="2cbc0-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cbc0-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="2cbc0-116">Name</span><span class="sxs-lookup"><span data-stu-id="2cbc0-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="2cbc0-117">Bezeichnung des Spaltenkopfs</span><span class="sxs-lookup"><span data-stu-id="2cbc0-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="2cbc0-118">Type</span><span class="sxs-lookup"><span data-stu-id="2cbc0-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="2cbc0-119">Ganzzahl des Datentyps.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="2cbc0-120">Size</span><span class="sxs-lookup"><span data-stu-id="2cbc0-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="2cbc0-121">Ganzzahl der Breite in Zeichen, unabhängig vom Datentyp.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="2cbc0-122">Nullability</span><span class="sxs-lookup"><span data-stu-id="2cbc0-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="2cbc0-123">Boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="2cbc0-124">Skalieren</span><span class="sxs-lookup"><span data-stu-id="2cbc0-124">Scale</span></span><br />
<span data-ttu-id="2cbc0-125">(Optional)</span><span class="sxs-lookup"><span data-stu-id="2cbc0-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="2cbc0-p102">Dieses optionale Attribut definiert die Dezimalstellen von numerischen Feldern. Ist dieser Wert nicht angegeben, werden numerische Werte auf drei Dezimalstellen beschränkt. Dies wirkt sich nicht auf die Genauigkeit aus, die Anzahl der Ziffern nach dem Dezimaltrennzeichen ist jedoch auf drei Stellen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="2cbc0-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2cbc0-129">Remarks</span></span>

<span data-ttu-id="2cbc0-130">Das serverseitige Geschäftsobjekt kann das resultierende **Recordset** -Objekt mit Daten von einem Nicht-OLE DB-Datenanbieter wie einer Betriebssystemdatei, die Bestandsquoten enthält, auffüllen.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="2cbc0-p103">In der folgenden Liste sind die [DataTypeEnum](datatypeenum.md)-Werte aufgeführt, die von der **CreateRecordset** -Methode unterstützt werden. Bei der angegebenen Zahl handelt es sich um die Referenznummer, die zum Definieren von Feldern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="2cbc0-p104">Die einzelnen Datentypen haben entweder eine feste oder eine variable Länge. Bei Typen mit fester Länge sollte die Größe auf den Wert -1 festgelegt werden, da die Größe vorher festgelegt werden muss und eine Definition der Größe noch erforderlich ist. Bei Datentypen mit variabler Länge ist eine Größe zwischen 1 und 32767 zulässig.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="2cbc0-p105">Bei einigen Datentypen mit variabler Länge wird der Typ möglicherweise in den Typ umgewandelt, der in der Spalte Ersetzung angegeben ist. Diese Ersetzungen werden erst angezeigt, nachdem das Recordset-Objekt erstellt und aufgefüllt wurde. Anschließend können Sie bei Bedarf den tatsächlichen Datentyp anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2cbc0-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cbc0-139">Länge</span><span class="sxs-lookup"><span data-stu-id="2cbc0-139">Length</span></span></p></th>
<th><p><span data-ttu-id="2cbc0-140">Konstante</span><span class="sxs-lookup"><span data-stu-id="2cbc0-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="2cbc0-141">Zahl</span><span class="sxs-lookup"><span data-stu-id="2cbc0-141">Number</span></span></p></th>
<th><p><span data-ttu-id="2cbc0-142">Ersetzung</span><span class="sxs-lookup"><span data-stu-id="2cbc0-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-143">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-145">16</span><span class="sxs-lookup"><span data-stu-id="2cbc0-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-146">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-148">2</span><span class="sxs-lookup"><span data-stu-id="2cbc0-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-149">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-150"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-151">3</span><span class="sxs-lookup"><span data-stu-id="2cbc0-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-152">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-154">20</span><span class="sxs-lookup"><span data-stu-id="2cbc0-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-155">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-157">17</span><span class="sxs-lookup"><span data-stu-id="2cbc0-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-158">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-160">18</span><span class="sxs-lookup"><span data-stu-id="2cbc0-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-161">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-163">19</span><span class="sxs-lookup"><span data-stu-id="2cbc0-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-164">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-166">21</span><span class="sxs-lookup"><span data-stu-id="2cbc0-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-167">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-169">4</span><span class="sxs-lookup"><span data-stu-id="2cbc0-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-170">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-171"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-172">5</span><span class="sxs-lookup"><span data-stu-id="2cbc0-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-173">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-175">6</span><span class="sxs-lookup"><span data-stu-id="2cbc0-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-176">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-178">14</span><span class="sxs-lookup"><span data-stu-id="2cbc0-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-179">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-181">131</span><span class="sxs-lookup"><span data-stu-id="2cbc0-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-182">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-184">11</span><span class="sxs-lookup"><span data-stu-id="2cbc0-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-185">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-187">10</span><span class="sxs-lookup"><span data-stu-id="2cbc0-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-188">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-190">72</span><span class="sxs-lookup"><span data-stu-id="2cbc0-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-191">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-193">7</span><span class="sxs-lookup"><span data-stu-id="2cbc0-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-194">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-196">133</span><span class="sxs-lookup"><span data-stu-id="2cbc0-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-197">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-199">134</span><span class="sxs-lookup"><span data-stu-id="2cbc0-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-200">Fest</span><span class="sxs-lookup"><span data-stu-id="2cbc0-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-202">135</span><span class="sxs-lookup"><span data-stu-id="2cbc0-202">135</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-203">7</span><span class="sxs-lookup"><span data-stu-id="2cbc0-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-204">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-206">8</span><span class="sxs-lookup"><span data-stu-id="2cbc0-206">8</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-207">130</span><span class="sxs-lookup"><span data-stu-id="2cbc0-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-208">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-209"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-210">129</span><span class="sxs-lookup"><span data-stu-id="2cbc0-210">129</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-211">200</span><span class="sxs-lookup"><span data-stu-id="2cbc0-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-212">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-213"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-214">200</span><span class="sxs-lookup"><span data-stu-id="2cbc0-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-215">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-217">201</span><span class="sxs-lookup"><span data-stu-id="2cbc0-217">201</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-218">200</span><span class="sxs-lookup"><span data-stu-id="2cbc0-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-219">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-221">130</span><span class="sxs-lookup"><span data-stu-id="2cbc0-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-222">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-224">202</span><span class="sxs-lookup"><span data-stu-id="2cbc0-224">202</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-225">130</span><span class="sxs-lookup"><span data-stu-id="2cbc0-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-226">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-228">203</span><span class="sxs-lookup"><span data-stu-id="2cbc0-228">203</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-229">130</span><span class="sxs-lookup"><span data-stu-id="2cbc0-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-230">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-232">128</span><span class="sxs-lookup"><span data-stu-id="2cbc0-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cbc0-233">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-235">204</span><span class="sxs-lookup"><span data-stu-id="2cbc0-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cbc0-236">Variabel</span><span class="sxs-lookup"><span data-stu-id="2cbc0-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2cbc0-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2cbc0-238">205</span><span class="sxs-lookup"><span data-stu-id="2cbc0-238">205</span></span></p></td>
<td><p><span data-ttu-id="2cbc0-239">204</span><span class="sxs-lookup"><span data-stu-id="2cbc0-239">204</span></span></p></td>
</tr>
</tbody>
</table>

