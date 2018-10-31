---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b9c1aff21b62eff061a3f68ef3ad56e07e46388d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860084"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="f515b-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="f515b-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="f515b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f515b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f515b-104">Gibt an, wann der [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)-Anbieter aggregierte und berechnete Spalten eines hierarchischen Recordsets erneut berechnet.</span><span class="sxs-lookup"><span data-stu-id="f515b-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="f515b-105">Diese Konstanten werden nur mit dem **MSDataShape** -Anbieter und das **Recordset-Objekt** "**Auto Recalc**" dynamische-Eigenschaft, die im [Index für dynamische ADO-Eigenschaften](ado-dynamic-property-index.md) verwiesen wird und die in der Microsoft Cursor Service [dokumentiert für OLE verwendet DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) oder [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="f515b-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f515b-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="f515b-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="f515b-107">Wert</span><span class="sxs-lookup"><span data-stu-id="f515b-107">Value</span></span></p></th>
<th><p><span data-ttu-id="f515b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f515b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f515b-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="f515b-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="f515b-110">1</span><span class="sxs-lookup"><span data-stu-id="f515b-110">1</span></span></p></td>
<td><p><span data-ttu-id="f515b-p101">Standardwert. Es wird eine Neuberechnung ausgeführt, sobald der <strong>MSDataShape</strong>-Anbieter festgestellt hat, dass sich Werte geändert haben, von den die berechneten Spalten abhängen.</span><span class="sxs-lookup"><span data-stu-id="f515b-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f515b-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="f515b-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="f515b-114">0</span><span class="sxs-lookup"><span data-stu-id="f515b-114">0</span></span></p></td>
<td><p><span data-ttu-id="f515b-115">Berechnung wird lediglich bei zunächst das hierarchische <strong>Recordset-Objekt</strong>zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f515b-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f515b-116">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f515b-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="f515b-117">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="f515b-117">These constants do not have ADO/WFC equivalents.</span></span>

