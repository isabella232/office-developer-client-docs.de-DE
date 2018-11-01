---
title: RecordTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6427a98d13231575bdc90fb89fe740fd9cd0f073
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868350"
---
# <a name="recordtypeenum"></a><span data-ttu-id="d3d61-102">RecordTypeEnum</span><span class="sxs-lookup"><span data-stu-id="d3d61-102">RecordTypeEnum</span></span>

<span data-ttu-id="d3d61-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3d61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3d61-104">Gibt den Typ des [Record](record-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d3d61-104">Specifies the type of [Record](record-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3d61-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="d3d61-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d3d61-106">Wert</span><span class="sxs-lookup"><span data-stu-id="d3d61-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d3d61-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3d61-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3d61-108"><strong>adSimpleRecord</strong></span><span class="sxs-lookup"><span data-stu-id="d3d61-108"><strong>adSimpleRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="d3d61-109">0</span><span class="sxs-lookup"><span data-stu-id="d3d61-109">0</span></span></p></td>
<td><p><span data-ttu-id="d3d61-110">Gibt einen <em>einfachen</em> Datensatz an (enthält keine untergeordneten Knoten).</span><span class="sxs-lookup"><span data-stu-id="d3d61-110">Indicates a <em>simple</em> record (does not contain child nodes).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d61-111"><strong>adCollectionRecord</strong></span><span class="sxs-lookup"><span data-stu-id="d3d61-111"><strong>adCollectionRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="d3d61-112">1</span><span class="sxs-lookup"><span data-stu-id="d3d61-112">1</span></span></p></td>
<td><p><span data-ttu-id="d3d61-113">Gibt einen <em>Auflistungsdatensatz</em> an (enthält untergeordnete Knoten).</span><span class="sxs-lookup"><span data-stu-id="d3d61-113">Indicates a <em>collection</em> record (contains child nodes).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3d61-114"><strong>adRecordUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="d3d61-114"><strong>adRecordUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="d3d61-115">-1</span><span class="sxs-lookup"><span data-stu-id="d3d61-115">-1</span></span></p></td>
<td><p><span data-ttu-id="d3d61-116">Gibt an, dass der Typ dieses <strong>Datensatzes</strong> unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="d3d61-116">Indicates that the type of this <strong>Record</strong> is unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d61-117"><strong>adStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="d3d61-117"><strong>adStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="d3d61-118">2</span><span class="sxs-lookup"><span data-stu-id="d3d61-118">2</span></span></p></td>
<td><p><span data-ttu-id="d3d61-119">Gibt einen besonderen Typ von <em>Auflistungsdatensatz</em> an, der strukturierte COM-Dokumente darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3d61-119">Indicates a special kind of <em>collection</em> record that represents COM structured documents.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d3d61-120">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="d3d61-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="d3d61-121">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="d3d61-121">These constants do not have ADO/WFC equivalents.</span></span>

