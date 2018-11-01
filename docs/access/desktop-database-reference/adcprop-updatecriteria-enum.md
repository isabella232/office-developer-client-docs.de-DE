---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b1ebc5cf8df4a0eab125f788544dba40ec373d02
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880649"
---
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="fa8d9-102">ADCPROP\_UPDATECRITERIA\_ENUM</span><span class="sxs-lookup"><span data-stu-id="fa8d9-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="fa8d9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa8d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa8d9-104">Gibt an, welche Felder zum Erkennen von Konflikten während einer optimistischen Aktualisierung einer Zeile der Datenquelle mit einem [Recordset](recordset-object-ado.md)-Objekt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="fa8d9-105">Verwenden Sie diese Konstanten mit der dynamischen **Recordset**-Eigenschaft **Update Criteria**, auf die im [Index zu dynamischen ADO-Eigenschaften](ado-dynamic-property-index.md) verwiesen wird und die in der Dokumentation [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) beschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa8d9-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="fa8d9-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="fa8d9-107">Wert</span><span class="sxs-lookup"><span data-stu-id="fa8d9-107">Value</span></span></p></th>
<th><p><span data-ttu-id="fa8d9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa8d9-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa8d9-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="fa8d9-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="fa8d9-110">1</span><span class="sxs-lookup"><span data-stu-id="fa8d9-110">1</span></span></p></td>
<td><p><span data-ttu-id="fa8d9-111">Erkennt Konflikte, wenn eine Spalte der Datenquellenzeile geändert worden ist.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa8d9-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="fa8d9-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="fa8d9-113">0</span><span class="sxs-lookup"><span data-stu-id="fa8d9-113">0</span></span></p></td>
<td><p><span data-ttu-id="fa8d9-114">Erkennt Konflikte, wenn die Schlüsselspalte der Datenquellenzeile geändert wurde, was darauf hinweist, dass die Zeile gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa8d9-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="fa8d9-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="fa8d9-116">3</span><span class="sxs-lookup"><span data-stu-id="fa8d9-116">3</span></span></p></td>
<td><p><span data-ttu-id="fa8d9-117">Erkennt Konflikte, wenn der Zeitstempel der Datenquellenzeile geändert wurde, was bedeutet, dass die Zeile zugegriffen wurde, nachdem das <strong>Recordset</strong> abgerufen worden war.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa8d9-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="fa8d9-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="fa8d9-119">2</span><span class="sxs-lookup"><span data-stu-id="fa8d9-119">2</span></span></p></td>
<td><p><span data-ttu-id="fa8d9-120">Erkennt Konflikte, wenn eine der, die aktualisierten Feldern des <strong>Recordsets</strong> entsprechen Spalten der Datenquellenzeile geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fa8d9-121">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="fa8d9-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="fa8d9-122">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fa8d9-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa8d9-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="fa8d9-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa8d9-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span><span class="sxs-lookup"><span data-stu-id="fa8d9-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa8d9-125">AdoEnums.AdcPropUpdateCriteria.KEY</span><span class="sxs-lookup"><span data-stu-id="fa8d9-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa8d9-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="fa8d9-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa8d9-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="fa8d9-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

