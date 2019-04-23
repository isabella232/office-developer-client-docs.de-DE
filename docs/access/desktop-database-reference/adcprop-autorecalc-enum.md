---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280522"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="b4004-102">ADCPROP\_-\_AUTORECALC-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b4004-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="b4004-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4004-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4004-104">Gibt an, wann der [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)-Anbieter aggregierte und berechnete Spalten eines hierarchischen Recordsets erneut berechnet.</span><span class="sxs-lookup"><span data-stu-id="b4004-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="b4004-105">Diese Konstanten werden nur zusammen mit dem **MSDataShape** -Anbieter und der dynamischen Eigenschaft "**Auto Recalc**" des Recordsets verwendet, auf die im [Index der dynamischen ADO-Eigenschaft](ado-dynamic-property-index.md) verwiesen wird und die im \*\*\*\* [Microsoft Cursor-Dienst für OLE dokumentiert ist. DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) -oder [Microsoft Data Shaping-Dienst für die OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b4004-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4004-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="b4004-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="b4004-107">Wert</span><span class="sxs-lookup"><span data-stu-id="b4004-107">Value</span></span></p></th>
<th><p><span data-ttu-id="b4004-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4004-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4004-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="b4004-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="b4004-110">1</span><span class="sxs-lookup"><span data-stu-id="b4004-110">1</span></span></p></td>
<td><p><span data-ttu-id="b4004-p101">Standardwert. Es wird eine Neuberechnung ausgeführt, sobald der <strong>MSDataShape</strong>-Anbieter festgestellt hat, dass sich Werte geändert haben, von den die berechneten Spalten abhängen.</span><span class="sxs-lookup"><span data-stu-id="b4004-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4004-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="b4004-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="b4004-114">0</span><span class="sxs-lookup"><span data-stu-id="b4004-114">0</span></span></p></td>
<td><p><span data-ttu-id="b4004-115">Eine Berechnung wird lediglich bei der ersten Erstellung des hierarchischen Recordsets durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4004-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b4004-116">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="b4004-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="b4004-117">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="b4004-117">These constants do not have ADO/WFC equivalents.</span></span>

