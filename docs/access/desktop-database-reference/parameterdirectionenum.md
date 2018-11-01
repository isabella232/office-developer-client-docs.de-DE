---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a570171386a1ff00e1740e42cf914683ad5eb03
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871528"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="1a1e7-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="1a1e7-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="1a1e7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a1e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a1e7-104">Gibt an, ob der [Parameter](parameter-object-ado.md) einen Eingabeparameter, einen Ausgabeparameter, sowohl einen Eingabe- als auch einen Ausgabeparameter oder den Rückgabewert aus einer gespeicherten Prozedur darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a1e7-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="1a1e7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1a1e7-106">Wert</span><span class="sxs-lookup"><span data-stu-id="1a1e7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1a1e7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a1e7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a1e7-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="1a1e7-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="1a1e7-109">1</span><span class="sxs-lookup"><span data-stu-id="1a1e7-109">1</span></span></p></td>
<td><p><span data-ttu-id="1a1e7-p101">Standardwert. Gibt an, dass der Parameter einen Eingabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a1e7-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="1a1e7-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="1a1e7-113">3</span><span class="sxs-lookup"><span data-stu-id="1a1e7-113">3</span></span></p></td>
<td><p><span data-ttu-id="1a1e7-114">Gibt an, dass der Parameter sowohl einen Eingabe- als auch einen Ausgabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a1e7-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="1a1e7-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="1a1e7-116">2</span><span class="sxs-lookup"><span data-stu-id="1a1e7-116">2</span></span></p></td>
<td><p><span data-ttu-id="1a1e7-117">Gibt an, dass der Parameter einen Ausgabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a1e7-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="1a1e7-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="1a1e7-119">4</span><span class="sxs-lookup"><span data-stu-id="1a1e7-119">4</span></span></p></td>
<td><p><span data-ttu-id="1a1e7-120">Gibt an, dass der Parameter einen Rückgabewert darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a1e7-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="1a1e7-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="1a1e7-122">0</span><span class="sxs-lookup"><span data-stu-id="1a1e7-122">0</span></span></p></td>
<td><p><span data-ttu-id="1a1e7-123">Gibt an, dass die Parameterrichtung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1a1e7-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="1a1e7-124">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="1a1e7-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="1a1e7-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="1a1e7-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a1e7-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="1a1e7-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a1e7-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="1a1e7-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a1e7-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a1e7-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a1e7-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a1e7-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a1e7-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="1a1e7-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a1e7-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="1a1e7-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

