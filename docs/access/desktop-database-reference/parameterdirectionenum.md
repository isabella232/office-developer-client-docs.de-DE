---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fac07165416841691ee7bc3ca5dfcdc366861023
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287972"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="da89b-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="da89b-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="da89b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da89b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da89b-104">Gibt an, ob der [Parameter](parameter-object-ado.md) einen Eingabeparameter, einen Ausgabeparameter, sowohl einen Eingabe- als auch einen Ausgabeparameter oder den Rückgabewert aus einer gespeicherten Prozedur darstellt.</span><span class="sxs-lookup"><span data-stu-id="da89b-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da89b-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="da89b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="da89b-106">Wert</span><span class="sxs-lookup"><span data-stu-id="da89b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="da89b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da89b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da89b-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="da89b-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="da89b-109">1</span><span class="sxs-lookup"><span data-stu-id="da89b-109">1</span></span></p></td>
<td><p><span data-ttu-id="da89b-p101">Standardwert. Gibt an, dass der Parameter einen Eingabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="da89b-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da89b-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="da89b-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="da89b-113">3</span><span class="sxs-lookup"><span data-stu-id="da89b-113">3</span></span></p></td>
<td><p><span data-ttu-id="da89b-114">Gibt an, dass der Parameter sowohl einen Eingabe- als auch einen Ausgabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="da89b-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da89b-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="da89b-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="da89b-116">2</span><span class="sxs-lookup"><span data-stu-id="da89b-116">2</span></span></p></td>
<td><p><span data-ttu-id="da89b-117">Gibt an, dass der Parameter einen Ausgabeparameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="da89b-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da89b-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="da89b-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="da89b-119">4</span><span class="sxs-lookup"><span data-stu-id="da89b-119">4</span></span></p></td>
<td><p><span data-ttu-id="da89b-120">Gibt an, dass der Parameter einen Rückgabewert darstellt.</span><span class="sxs-lookup"><span data-stu-id="da89b-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da89b-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="da89b-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="da89b-122">0</span><span class="sxs-lookup"><span data-stu-id="da89b-122">0</span></span></p></td>
<td><p><span data-ttu-id="da89b-123">Gibt an, dass die Parameterrichtung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="da89b-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="da89b-124">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="da89b-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="da89b-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="da89b-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da89b-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="da89b-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da89b-127">AdoEnums. ParameterDirection. INPUT</span><span class="sxs-lookup"><span data-stu-id="da89b-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da89b-128">AdoEnums. ParameterDirection. Input Output</span><span class="sxs-lookup"><span data-stu-id="da89b-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da89b-129">AdoEnums. ParameterDirection. OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da89b-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da89b-130">AdoEnums. ParameterDirection. RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="da89b-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da89b-131">AdoEnums. ParameterDirection. UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="da89b-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

