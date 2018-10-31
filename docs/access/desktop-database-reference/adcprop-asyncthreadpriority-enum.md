---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b84a06efde252ca6c128e0bcc0baccaf3676e06e
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862947"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="b15eb-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span><span class="sxs-lookup"><span data-stu-id="b15eb-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="b15eb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b15eb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b15eb-104">Gibt für ein RDS-[Recordset](recordset-object-ado.md)-Objekt die Ausführungspriorität des asynchronen Threads an, der Daten abruft.</span><span class="sxs-lookup"><span data-stu-id="b15eb-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="b15eb-105">Verwenden Sie diese Konstanten mit der dynamischen **Recordset**-Eigenschaft **Background Thread Priority**, auf die im Index für dynamische ADO-Eigenschaften verwiesen wird und die in der Dokumentation [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) beschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="b15eb-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b15eb-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="b15eb-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="b15eb-107">Wert</span><span class="sxs-lookup"><span data-stu-id="b15eb-107">Value</span></span></p></th>
<th><p><span data-ttu-id="b15eb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b15eb-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-110">4</span><span class="sxs-lookup"><span data-stu-id="b15eb-110">4</span></span></p></td>
<td><p><span data-ttu-id="b15eb-111">Legt die Priorität zwischen dem normalen Wert und dem Höchstwert fest.</span><span class="sxs-lookup"><span data-stu-id="b15eb-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15eb-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-113">2</span><span class="sxs-lookup"><span data-stu-id="b15eb-113">2</span></span></p></td>
<td><p><span data-ttu-id="b15eb-114">Legt die Priorität zwischen dem niedrigsten und dem normalen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b15eb-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-116">5</span><span class="sxs-lookup"><span data-stu-id="b15eb-116">5</span></span></p></td>
<td><p><span data-ttu-id="b15eb-117">Legt die Priorität auf den höchst möglichen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b15eb-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15eb-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-119">1</span><span class="sxs-lookup"><span data-stu-id="b15eb-119">1</span></span></p></td>
<td><p><span data-ttu-id="b15eb-120">Legt die Priorität auf den niedrigsten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b15eb-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-122">3</span><span class="sxs-lookup"><span data-stu-id="b15eb-122">3</span></span></p></td>
<td><p><span data-ttu-id="b15eb-123">Legt die Priorität auf den normalen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b15eb-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="b15eb-124">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="b15eb-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="b15eb-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b15eb-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b15eb-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="b15eb-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="b15eb-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15eb-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="b15eb-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="b15eb-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15eb-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="b15eb-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="b15eb-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

