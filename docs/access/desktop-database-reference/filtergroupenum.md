---
title: FilterGroupEnum (Access PC-Datenbank-Referenz)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: fc2c41ddd672ff303584762f6091bab4c128de99
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862695"
---
# <a name="filtergroupenum"></a><span data-ttu-id="070fa-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="070fa-102">FilterGroupEnum</span></span>

<span data-ttu-id="070fa-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="070fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="070fa-104">Gibt die Gruppe der Datensätze an, die aus einem [Recordset](recordset-object-ado.md) gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="070fa-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="070fa-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="070fa-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="070fa-106">Wert</span><span class="sxs-lookup"><span data-stu-id="070fa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="070fa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="070fa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="070fa-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="070fa-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="070fa-109">2</span><span class="sxs-lookup"><span data-stu-id="070fa-109">2</span></span></p></td>
<td><p><span data-ttu-id="070fa-110">Filter zum Anzeigen von Datensätzen, die vom letzten <a href="delete-method-ado-recordset.md">Delete</a>-, <a href="resync-method-ado.md">Resync</a>-, <a href="updatebatch-method-ado.md">UpdateBatch</a>- oder <a href="cancelbatch-method-ado.md">CancelBatch</a>-Aufruf betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="070fa-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070fa-111"><strong>vorliegt</strong></span><span class="sxs-lookup"><span data-stu-id="070fa-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="070fa-112">5</span><span class="sxs-lookup"><span data-stu-id="070fa-112">5</span></span></p></td>
<td><p><span data-ttu-id="070fa-113">Filter zum Anzeigen der Datensätze, für die die letzte Batchaktualisierung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="070fa-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070fa-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="070fa-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="070fa-115">3</span><span class="sxs-lookup"><span data-stu-id="070fa-115">3</span></span></p></td>
<td><p><span data-ttu-id="070fa-116">Filter zum Anzeigen der Datensätze im aktuellen Cache – also die Ergebnisse des letzten Aufrufs zum Abrufen von Datensätzen aus der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="070fa-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070fa-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="070fa-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="070fa-118">0</span><span class="sxs-lookup"><span data-stu-id="070fa-118">0</span></span></p></td>
<td><p><span data-ttu-id="070fa-119">Entfernt den aktuellen Filter und stellt alle Datensätze für die Ansicht wieder her.</span><span class="sxs-lookup"><span data-stu-id="070fa-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070fa-120"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="070fa-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="070fa-121">1</span><span class="sxs-lookup"><span data-stu-id="070fa-121">1</span></span></p></td>
<td><p><span data-ttu-id="070fa-p101">Filter zum Anzeigen von Datensätzen, die geändert, jedoch noch nicht an den Server gesendet wurden. Nur für den Batchaktualisierungsmodus anwendbar.</span><span class="sxs-lookup"><span data-stu-id="070fa-p101">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="070fa-124">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="070fa-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="070fa-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="070fa-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="070fa-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="070fa-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="070fa-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="070fa-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070fa-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="070fa-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070fa-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="070fa-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="070fa-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="070fa-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="070fa-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="070fa-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

