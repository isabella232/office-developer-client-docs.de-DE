---
title: LockTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715368"
---
# <a name="locktypeenum"></a><span data-ttu-id="cd1e1-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="cd1e1-102">LockTypeEnum</span></span>

<span data-ttu-id="cd1e1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd1e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd1e1-104">Gibt den Sperrentyp für Datensätze während der Bearbeitung an.</span><span class="sxs-lookup"><span data-stu-id="cd1e1-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd1e1-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="cd1e1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cd1e1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="cd1e1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cd1e1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd1e1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd1e1-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="cd1e1-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="cd1e1-109">4</span><span class="sxs-lookup"><span data-stu-id="cd1e1-109">4</span></span></p></td>
<td><p><span data-ttu-id="cd1e1-p101">Gibt optimistische Batchaktualisierungen an. Erforderlich für den Batchaktualisierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="cd1e1-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd1e1-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="cd1e1-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="cd1e1-113">3</span><span class="sxs-lookup"><span data-stu-id="cd1e1-113">3</span></span></p></td>
<td><p><span data-ttu-id="cd1e1-p102">Gibt das optimistische Sperren auf Datensatzbasis an. Der Anbieter verwendet optimistische Sperren, wobei die Datensätze nur gesperrt werden, wenn Sie die <a href="update-method-ado.md">Update</a>-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cd1e1-p102">Indicates optimistic locking, record by record. The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd1e1-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="cd1e1-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="cd1e1-117">2</span><span class="sxs-lookup"><span data-stu-id="cd1e1-117">2</span></span></p></td>
<td><p><span data-ttu-id="cd1e1-p103">Gibt das pessimistische Sperren auf Datensatzbasis an. Der Anbieter führt die erforderlichen Schritte aus, um eine erfolgreiche Bearbeitung der Datensätze sicherzustellen, indem die Datensätze unmittelbar nach der Bearbeitung an der Datenquelle gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="cd1e1-p103">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd1e1-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="cd1e1-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="cd1e1-121">1</span><span class="sxs-lookup"><span data-stu-id="cd1e1-121">1</span></span></p></td>
<td><p><span data-ttu-id="cd1e1-p104">Gibt schreibgeschützte Datensätze an. Sie können die Daten nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="cd1e1-p104">Indicates read-only records. You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd1e1-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="cd1e1-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="cd1e1-125">-1</span><span class="sxs-lookup"><span data-stu-id="cd1e1-125">-1</span></span></p></td>
<td><p><span data-ttu-id="cd1e1-p105">Gibt keinen Sperrentyp an. Für Klone wird der Klon mit demselben Sperrentyp wie das Original erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd1e1-p105">Does not specify a type of lock. For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cd1e1-128">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="cd1e1-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="cd1e1-129">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cd1e1-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd1e1-130">Konstante</span><span class="sxs-lookup"><span data-stu-id="cd1e1-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd1e1-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="cd1e1-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd1e1-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="cd1e1-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd1e1-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="cd1e1-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd1e1-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="cd1e1-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd1e1-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="cd1e1-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

