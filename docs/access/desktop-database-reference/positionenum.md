---
title: PositionEnum (Access PC-Datenbank-Referenz)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c2ef44c804a413b85bcf393e1487ff4423c40f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473155"
---
# <a name="positionenum"></a><span data-ttu-id="6993c-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="6993c-102">PositionEnum</span></span>


<span data-ttu-id="6993c-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6993c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6993c-104">Gibt die aktuelle Position des Datensatzzeigers innerhalb eines [Recordsets](recordset-object-ado.md) an.</span><span class="sxs-lookup"><span data-stu-id="6993c-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6993c-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="6993c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6993c-106">Wert</span><span class="sxs-lookup"><span data-stu-id="6993c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6993c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6993c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6993c-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="6993c-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="6993c-109">-2</span><span class="sxs-lookup"><span data-stu-id="6993c-109">-2</span></span></p></td>
<td><p><span data-ttu-id="6993c-110">Gibt an, dass der aktuelle Datensatzzeiger bei BOF liegt (das heißt, die <a href="bof-eof-properties-ado.md">BOF</a>-Eigenschaft lautet <strong>Wahr</strong>).</span><span class="sxs-lookup"><span data-stu-id="6993c-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6993c-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="6993c-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="6993c-112">-3</span><span class="sxs-lookup"><span data-stu-id="6993c-112">-3</span></span></p></td>
<td><p><span data-ttu-id="6993c-113">Gibt an, dass der aktuelle Datensatzzeiger bei EOF liegt (das heißt, die <a href="bof-eof-properties-ado.md">EOF</a>-Eigenschaft lautet <strong>Wahr</strong>).</span><span class="sxs-lookup"><span data-stu-id="6993c-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6993c-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="6993c-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="6993c-115">-1</span><span class="sxs-lookup"><span data-stu-id="6993c-115">-1</span></span></p></td>
<td><p><span data-ttu-id="6993c-116">Gibt an, dass das <strong>Recordset</strong> leer ist, die aktuelle Position unbekannt ist oder der Anbieter nicht die <a href="absolutepage-property-ado.md">AbsolutePage-</a> oder <a href="absoluteposition-property-ado.md">AbsolutePosition</a> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6993c-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6993c-117">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="6993c-117">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="6993c-118">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6993c-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6993c-119">Konstante</span><span class="sxs-lookup"><span data-stu-id="6993c-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6993c-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="6993c-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6993c-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="6993c-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6993c-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="6993c-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

