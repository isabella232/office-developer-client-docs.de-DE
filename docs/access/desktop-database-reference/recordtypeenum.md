---
title: RecordTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c95e4b78a3e2259c3dc5961e87b98ca65ea55692
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704917"
---
# <a name="recordtypeenum"></a><span data-ttu-id="29d35-102">RecordTypeEnum</span><span class="sxs-lookup"><span data-stu-id="29d35-102">RecordTypeEnum</span></span>

<span data-ttu-id="29d35-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29d35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29d35-104">Gibt den Typ des [Record](record-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="29d35-104">Specifies the type of [Record](record-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29d35-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="29d35-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="29d35-106">Wert</span><span class="sxs-lookup"><span data-stu-id="29d35-106">Value</span></span></p></th>
<th><p><span data-ttu-id="29d35-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29d35-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29d35-108"><strong>adSimpleRecord</strong></span><span class="sxs-lookup"><span data-stu-id="29d35-108"><strong>adSimpleRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="29d35-109">0</span><span class="sxs-lookup"><span data-stu-id="29d35-109">0</span></span></p></td>
<td><p><span data-ttu-id="29d35-110">Gibt einen <em>einfachen</em> Datensatz an (enthält keine untergeordneten Knoten).</span><span class="sxs-lookup"><span data-stu-id="29d35-110">Indicates a <em>simple</em> record (does not contain child nodes).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29d35-111"><strong>adCollectionRecord</strong></span><span class="sxs-lookup"><span data-stu-id="29d35-111"><strong>adCollectionRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="29d35-112">1</span><span class="sxs-lookup"><span data-stu-id="29d35-112">1</span></span></p></td>
<td><p><span data-ttu-id="29d35-113">Gibt einen <em>Auflistungsdatensatz</em> an (enthält untergeordnete Knoten).</span><span class="sxs-lookup"><span data-stu-id="29d35-113">Indicates a <em>collection</em> record (contains child nodes).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29d35-114"><strong>adRecordUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="29d35-114"><strong>adRecordUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="29d35-115">-1</span><span class="sxs-lookup"><span data-stu-id="29d35-115">-1</span></span></p></td>
<td><p><span data-ttu-id="29d35-116">Gibt an, dass der Typ dieses <strong>Datensatzes</strong> unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="29d35-116">Indicates that the type of this <strong>Record</strong> is unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29d35-117"><strong>adStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="29d35-117"><strong>adStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="29d35-118">2</span><span class="sxs-lookup"><span data-stu-id="29d35-118">2</span></span></p></td>
<td><p><span data-ttu-id="29d35-119">Gibt einen besonderen Typ von <em>Auflistungsdatensatz</em> an, der strukturierte COM-Dokumente darstellt.</span><span class="sxs-lookup"><span data-stu-id="29d35-119">Indicates a special kind of <em>collection</em> record that represents COM structured documents.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="29d35-120">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="29d35-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="29d35-121">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="29d35-121">These constants do not have ADO/WFC equivalents.</span></span>

