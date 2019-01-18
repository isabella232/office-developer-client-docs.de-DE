---
title: FilterGroupEnum (Access PC-Datenbank-Referenz)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2ce54fe743c46468850abc5dc16520e208ec9e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704066"
---
# <a name="filtergroupenum"></a><span data-ttu-id="9773b-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="9773b-102">FilterGroupEnum</span></span>

<span data-ttu-id="9773b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9773b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9773b-104">Gibt die Gruppe der Datensätze an, die aus einem [Recordset](recordset-object-ado.md) gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9773b-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9773b-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="9773b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9773b-106">Wert</span><span class="sxs-lookup"><span data-stu-id="9773b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9773b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9773b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9773b-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9773b-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9773b-109">2</span><span class="sxs-lookup"><span data-stu-id="9773b-109">2</span></span></p></td>
<td><p><span data-ttu-id="9773b-110">Filter zum Anzeigen von Datensätzen, die vom letzten <a href="delete-method-ado-recordset.md">Delete</a>-, <a href="resync-method-ado.md">Resync</a>-, <a href="updatebatch-method-ado.md">UpdateBatch</a>- oder <a href="cancelbatch-method-ado.md">CancelBatch</a>-Aufruf betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="9773b-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9773b-111"><strong>vorliegt</strong></span><span class="sxs-lookup"><span data-stu-id="9773b-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9773b-112">5</span><span class="sxs-lookup"><span data-stu-id="9773b-112">5</span></span></p></td>
<td><p><span data-ttu-id="9773b-113">Filter zum Anzeigen der Datensätze, für die die letzte Batchaktualisierung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="9773b-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9773b-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9773b-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9773b-115">3</span><span class="sxs-lookup"><span data-stu-id="9773b-115">3</span></span></p></td>
<td><p><span data-ttu-id="9773b-116">Filter zum Anzeigen der Datensätze im aktuellen Cache – also die Ergebnisse des letzten Aufrufs zum Abrufen von Datensätzen aus der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9773b-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9773b-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="9773b-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="9773b-118">0</span><span class="sxs-lookup"><span data-stu-id="9773b-118">0</span></span></p></td>
<td><p><span data-ttu-id="9773b-119">Entfernt den aktuellen Filter und stellt alle Datensätze für die Ansicht wieder her.</span><span class="sxs-lookup"><span data-stu-id="9773b-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9773b-120"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9773b-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9773b-121">1</span><span class="sxs-lookup"><span data-stu-id="9773b-121">1</span></span></p></td>
<td><p><span data-ttu-id="9773b-p101">Filter zum Anzeigen von Datensätzen, die geändert, jedoch noch nicht an den Server gesendet wurden. Nur für den Batchaktualisierungsmodus anwendbar.</span><span class="sxs-lookup"><span data-stu-id="9773b-p101">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9773b-124">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="9773b-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="9773b-125">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9773b-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9773b-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="9773b-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9773b-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="9773b-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9773b-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="9773b-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9773b-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="9773b-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9773b-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="9773b-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9773b-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="9773b-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

