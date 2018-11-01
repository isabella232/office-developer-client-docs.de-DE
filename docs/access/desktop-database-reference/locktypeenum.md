---
title: LockTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 4613b6eca1048f80d7e2aabda35abf3c92d31255
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884226"
---
# <a name="locktypeenum"></a><span data-ttu-id="f98dc-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="f98dc-102">LockTypeEnum</span></span>

<span data-ttu-id="f98dc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f98dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f98dc-104">Gibt den Sperrentyp für Datensätze während der Bearbeitung an.</span><span class="sxs-lookup"><span data-stu-id="f98dc-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f98dc-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="f98dc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f98dc-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f98dc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f98dc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f98dc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f98dc-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="f98dc-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="f98dc-109">4</span><span class="sxs-lookup"><span data-stu-id="f98dc-109">4</span></span></p></td>
<td><p><span data-ttu-id="f98dc-p101">Gibt optimistische Batchaktualisierungen an. Erforderlich für den Batchaktualisierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="f98dc-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98dc-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="f98dc-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="f98dc-113">3</span><span class="sxs-lookup"><span data-stu-id="f98dc-113">3</span></span></p></td>
<td><p><span data-ttu-id="f98dc-p102">Gibt das optimistische Sperren auf Datensatzbasis an. Der Anbieter verwendet optimistische Sperren, wobei die Datensätze nur gesperrt werden, wenn Sie die <a href="update-method-ado.md">Update</a>-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f98dc-p102">Indicates optimistic locking, record by record. The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98dc-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="f98dc-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="f98dc-117">2</span><span class="sxs-lookup"><span data-stu-id="f98dc-117">2</span></span></p></td>
<td><p><span data-ttu-id="f98dc-p103">Gibt das pessimistische Sperren auf Datensatzbasis an. Der Anbieter führt die erforderlichen Schritte aus, um eine erfolgreiche Bearbeitung der Datensätze sicherzustellen, indem die Datensätze unmittelbar nach der Bearbeitung an der Datenquelle gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="f98dc-p103">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98dc-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="f98dc-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="f98dc-121">1</span><span class="sxs-lookup"><span data-stu-id="f98dc-121">1</span></span></p></td>
<td><p><span data-ttu-id="f98dc-p104">Gibt schreibgeschützte Datensätze an. Sie können die Daten nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f98dc-p104">Indicates read-only records. You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98dc-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="f98dc-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="f98dc-125">-1</span><span class="sxs-lookup"><span data-stu-id="f98dc-125">-1</span></span></p></td>
<td><p><span data-ttu-id="f98dc-p105">Gibt keinen Sperrentyp an. Für Klone wird der Klon mit demselben Sperrentyp wie das Original erstellt.</span><span class="sxs-lookup"><span data-stu-id="f98dc-p105">Does not specify a type of lock. For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f98dc-128">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f98dc-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="f98dc-129">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f98dc-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f98dc-130">Konstante</span><span class="sxs-lookup"><span data-stu-id="f98dc-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f98dc-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="f98dc-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98dc-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="f98dc-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98dc-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="f98dc-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f98dc-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="f98dc-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f98dc-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="f98dc-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

