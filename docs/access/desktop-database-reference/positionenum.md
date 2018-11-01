---
title: PositionEnum (Access PC-Datenbank-Referenz)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: aff2956659d71606b8da7fc206bf91501f091d2e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867964"
---
# <a name="positionenum"></a><span data-ttu-id="85b8f-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="85b8f-102">PositionEnum</span></span>

<span data-ttu-id="85b8f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85b8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85b8f-104">Gibt die aktuelle Position des Datensatzzeigers innerhalb eines [Recordsets](recordset-object-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="85b8f-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85b8f-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="85b8f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="85b8f-106">Wert</span><span class="sxs-lookup"><span data-stu-id="85b8f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="85b8f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85b8f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85b8f-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="85b8f-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="85b8f-109">-2</span><span class="sxs-lookup"><span data-stu-id="85b8f-109">-2</span></span></p></td>
<td><p><span data-ttu-id="85b8f-110">Gibt an, dass der aktuelle Datensatzzeiger bei BOF liegt (das heißt, die <a href="bof-eof-properties-ado.md">BOF</a>-Eigenschaft lautet <strong>Wahr</strong>).</span><span class="sxs-lookup"><span data-stu-id="85b8f-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b8f-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="85b8f-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="85b8f-112">-3</span><span class="sxs-lookup"><span data-stu-id="85b8f-112">-3</span></span></p></td>
<td><p><span data-ttu-id="85b8f-113">Gibt an, dass der aktuelle Datensatzzeiger bei EOF liegt (das heißt, die <a href="bof-eof-properties-ado.md">EOF</a>-Eigenschaft lautet <strong>Wahr</strong>).</span><span class="sxs-lookup"><span data-stu-id="85b8f-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b8f-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="85b8f-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="85b8f-115">-1</span><span class="sxs-lookup"><span data-stu-id="85b8f-115">-1</span></span></p></td>
<td><p><span data-ttu-id="85b8f-116">Gibt an, dass das <strong>Recordset</strong> leer ist, die aktuelle Position unbekannt ist oder der Anbieter nicht die <a href="absolutepage-property-ado.md">AbsolutePage-</a> oder <a href="absoluteposition-property-ado.md">AbsolutePosition</a> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="85b8f-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="85b8f-117">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="85b8f-117">ADO/WFC equivalent</span></span>

<span data-ttu-id="85b8f-118">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="85b8f-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85b8f-119">Konstante</span><span class="sxs-lookup"><span data-stu-id="85b8f-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85b8f-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="85b8f-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85b8f-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="85b8f-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85b8f-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="85b8f-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

