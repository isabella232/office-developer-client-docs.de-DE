---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b018402f6a2d48819a3f97c69e2a8db77fa9e84c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476110"
---
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="c8719-102">ADCPROP\_UPDATECRITERIA\_ENUM</span><span class="sxs-lookup"><span data-stu-id="c8719-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="c8719-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8719-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c8719-104">Gibt an, welche Felder zum Erkennen von Konflikten während einer optimistischen Aktualisierung einer Zeile der Datenquelle mit einem [Recordset](recordset-object-ado.md)-Objekt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c8719-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="c8719-105">Verwenden Sie diese Konstanten mit der dynamischen **Recordset**-Eigenschaft **Update Criteria**, auf die im [Index zu dynamischen ADO-Eigenschaften](ado-dynamic-property-index.md) verwiesen wird und die in der Dokumentation [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) beschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="c8719-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8719-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="c8719-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="c8719-107">Wert</span><span class="sxs-lookup"><span data-stu-id="c8719-107">Value</span></span></p></th>
<th><p><span data-ttu-id="c8719-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8719-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8719-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="c8719-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="c8719-110">1</span><span class="sxs-lookup"><span data-stu-id="c8719-110">1</span></span></p></td>
<td><p><span data-ttu-id="c8719-111">Erkennt Konflikte, wenn eine Spalte der Datenquellenzeile geändert worden ist.</span><span class="sxs-lookup"><span data-stu-id="c8719-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8719-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="c8719-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="c8719-113">0</span><span class="sxs-lookup"><span data-stu-id="c8719-113">0</span></span></p></td>
<td><p><span data-ttu-id="c8719-114">Erkennt Konflikte, wenn die Schlüsselspalte der Datenquellenzeile geändert wurde, was darauf hinweist, dass die Zeile gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="c8719-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8719-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="c8719-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="c8719-116">3</span><span class="sxs-lookup"><span data-stu-id="c8719-116">3</span></span></p></td>
<td><p><span data-ttu-id="c8719-117">Erkennt Konflikte, wenn der Zeitstempel der Datenquellenzeile geändert wurde, was bedeutet, dass die Zeile zugegriffen wurde, nachdem das <strong>Recordset</strong> abgerufen worden war.</span><span class="sxs-lookup"><span data-stu-id="c8719-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8719-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="c8719-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="c8719-119">2</span><span class="sxs-lookup"><span data-stu-id="c8719-119">2</span></span></p></td>
<td><p><span data-ttu-id="c8719-120">Erkennt Konflikte, wenn eine der, die aktualisierten Feldern des <strong>Recordsets</strong> entsprechen Spalten der Datenquellenzeile geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="c8719-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8719-121">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="c8719-121">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c8719-122">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c8719-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8719-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="c8719-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8719-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span><span class="sxs-lookup"><span data-stu-id="c8719-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8719-125">AdoEnums.AdcPropUpdateCriteria.KEY</span><span class="sxs-lookup"><span data-stu-id="c8719-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8719-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="c8719-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8719-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="c8719-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

