---
title: ADCPROP_UPDATECRITERIA_ENUM
TOCTitle: ADCPROP_UPDATECRITERIA_ENUM
ms:assetid: 70da63fa-fa75-9bb4-683d-0fcb4c4a2934
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249450(v=office.15)
ms:contentKeyID: 48545571
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8be93b0b7e4b32e3c040e871ff7d97a95f1e247e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282852"
---
# <a name="adcpropupdatecriteriaenum"></a><span data-ttu-id="15bb7-102">ADCPROP\_-\_UPDATECRITERIA-Enumeration</span><span class="sxs-lookup"><span data-stu-id="15bb7-102">ADCPROP\_UPDATECRITERIA\_ENUM</span></span>

<span data-ttu-id="15bb7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15bb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15bb7-104">Gibt an, welche Felder zum Erkennen von Konflikten während einer optimistischen Aktualisierung einer Zeile der Datenquelle mit einem [Recordset](recordset-object-ado.md)-Objekt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="15bb7-104">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="15bb7-105">Verwenden Sie diese Konstanten mit der dynamischen **Recordset**-Eigenschaft **Update Criteria**, auf die im [Index zu dynamischen ADO-Eigenschaften](ado-dynamic-property-index.md) verwiesen wird und die in der Dokumentation [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) beschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="15bb7-105">Use these constants with the **Recordset** "**Update Criteria**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15bb7-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="15bb7-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="15bb7-107">Wert</span><span class="sxs-lookup"><span data-stu-id="15bb7-107">Value</span></span></p></th>
<th><p><span data-ttu-id="15bb7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15bb7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15bb7-109"><strong>adCriteriaAllCols</strong></span><span class="sxs-lookup"><span data-stu-id="15bb7-109"><strong>adCriteriaAllCols</strong></span></span></p></td>
<td><p><span data-ttu-id="15bb7-110">1</span><span class="sxs-lookup"><span data-stu-id="15bb7-110">1</span></span></p></td>
<td><p><span data-ttu-id="15bb7-111">Erkennt Konflikte, wenn eine Spalte der Datenquellenzeile geändert worden ist.</span><span class="sxs-lookup"><span data-stu-id="15bb7-111">Detects conflicts if any column of the data source row has been changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15bb7-112"><strong>adCriteriaKey</strong></span><span class="sxs-lookup"><span data-stu-id="15bb7-112"><strong>adCriteriaKey</strong></span></span></p></td>
<td><p><span data-ttu-id="15bb7-113">0</span><span class="sxs-lookup"><span data-stu-id="15bb7-113">0</span></span></p></td>
<td><p><span data-ttu-id="15bb7-114">Erkennt Konflikte, wenn die Schlüsselspalte der Datenquellenzeile geändert wurde, was darauf hinweist, dass die Zeile gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="15bb7-114">Detects conflicts if the key column of the data source row has been changed, which means that the row has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15bb7-115"><strong>adCriteriaTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="15bb7-115"><strong>adCriteriaTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="15bb7-116">3</span><span class="sxs-lookup"><span data-stu-id="15bb7-116">3</span></span></p></td>
<td><p><span data-ttu-id="15bb7-117">Erkennt Konflikte, wenn der Zeitstempel der Datenquellenzeile geändert wurde, was darauf hinweist, dass auf die Zeile zugegriffen wurde, nachdem das Recordset abgerufen worden war.</span><span class="sxs-lookup"><span data-stu-id="15bb7-117">Detects conflicts if the timestamp of the data source row has been changed, which means the row has been accessed after the <strong>Recordset</strong> was obtained.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15bb7-118"><strong>adCriteriaUpdCols</strong></span><span class="sxs-lookup"><span data-stu-id="15bb7-118"><strong>adCriteriaUpdCols</strong></span></span></p></td>
<td><p><span data-ttu-id="15bb7-119">2</span><span class="sxs-lookup"><span data-stu-id="15bb7-119">2</span></span></p></td>
<td><p><span data-ttu-id="15bb7-120">Erkennt Konflikte, wenn eine der Spalten der Datenquellenzeile geändert wurde, die den aktualisierten Feldern des Recordsets entsprechen.</span><span class="sxs-lookup"><span data-stu-id="15bb7-120">Detects conflicts if any of the columns of the data source row that correspond to updated fields of the <strong>Recordset</strong> have been changed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="15bb7-121">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="15bb7-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="15bb7-122">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="15bb7-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15bb7-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="15bb7-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15bb7-124">AdoEnums. AdcPropUpdateCriteria. allSPALTEN</span><span class="sxs-lookup"><span data-stu-id="15bb7-124">AdoEnums.AdcPropUpdateCriteria.ALLCOLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15bb7-125">AdoEnums. AdcPropUpdateCriteria. KEY</span><span class="sxs-lookup"><span data-stu-id="15bb7-125">AdoEnums.AdcPropUpdateCriteria.KEY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15bb7-126">AdoEnums. AdcPropUpdateCriteria. TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="15bb7-126">AdoEnums.AdcPropUpdateCriteria.TIMESTAMP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15bb7-127">AdoEnums. AdcPropUpdateCriteria. UPDCOLS</span><span class="sxs-lookup"><span data-stu-id="15bb7-127">AdoEnums.AdcPropUpdateCriteria.UPDCOLS</span></span></p></td>
</tr>
</tbody>
</table>

