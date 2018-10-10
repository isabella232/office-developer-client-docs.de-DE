---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3da089a1369905b78d1a0724990afc22eb1d0dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473564"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="0bab2-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="0bab2-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="0bab2-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bab2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0bab2-104">Gibt an, ob der [Parameter](parameter-object-ado.md) einen Eingabeparameter, einen Ausgabeparameter, sowohl einen Eingabe- als auch einen Ausgabeparameter oder den Rückgabewert aus einer gespeicherten Prozedur darstellt.</span><span class="sxs-lookup"><span data-stu-id="0bab2-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bab2-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="0bab2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0bab2-106">Wert</span><span class="sxs-lookup"><span data-stu-id="0bab2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0bab2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bab2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bab2-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="0bab2-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="0bab2-109">1</span><span class="sxs-lookup"><span data-stu-id="0bab2-109">1</span></span></p></td>
<td><p><span data-ttu-id="0bab2-p101">Standardwert. Gibt an, dass der Parameter einen Eingabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="0bab2-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bab2-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="0bab2-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="0bab2-113">3</span><span class="sxs-lookup"><span data-stu-id="0bab2-113">3</span></span></p></td>
<td><p><span data-ttu-id="0bab2-114">Gibt an, dass der Parameter sowohl einen Eingabe- als auch einen Ausgabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="0bab2-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bab2-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="0bab2-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="0bab2-116">2</span><span class="sxs-lookup"><span data-stu-id="0bab2-116">2</span></span></p></td>
<td><p><span data-ttu-id="0bab2-117">Gibt an, dass der Parameter einen Ausgabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="0bab2-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bab2-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="0bab2-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="0bab2-119">4</span><span class="sxs-lookup"><span data-stu-id="0bab2-119">4</span></span></p></td>
<td><p><span data-ttu-id="0bab2-120">Gibt an, dass der Parameter einen Rückgabewert darstellt.</span><span class="sxs-lookup"><span data-stu-id="0bab2-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bab2-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="0bab2-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="0bab2-122">0</span><span class="sxs-lookup"><span data-stu-id="0bab2-122">0</span></span></p></td>
<td><p><span data-ttu-id="0bab2-123">Gibt an, dass die Parameterrichtung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0bab2-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0bab2-124">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="0bab2-124">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="0bab2-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0bab2-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bab2-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="0bab2-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bab2-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="0bab2-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bab2-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bab2-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bab2-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bab2-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bab2-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="0bab2-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bab2-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="0bab2-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

