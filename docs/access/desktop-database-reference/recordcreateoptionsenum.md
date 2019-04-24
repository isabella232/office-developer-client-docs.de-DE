---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300693"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="8a2ad-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="8a2ad-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="8a2ad-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a2ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a2ad-p101">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method. The values can be combined with an AND operator.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-p101">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method. The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a2ad-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="8a2ad-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8a2ad-107">Wert</span><span class="sxs-lookup"><span data-stu-id="8a2ad-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8a2ad-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a2ad-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a2ad-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="8a2ad-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2ad-110">0x2000</span><span class="sxs-lookup"><span data-stu-id="8a2ad-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="8a2ad-111">Erstellt einen neuen <strong>Datensatz</strong> an dem durch <em>Source</em> -Parameter angegebenen Knoten, anstatt einen vorhandenen <strong>Datensatz</strong>zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-111">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>.</span></span> <span data-ttu-id="8a2ad-112">Wenn die Quelle auf einen vorhandenen Knoten zeigt, tritt ein Laufzeitfehler auf, es sei <strong></strong> denn, die addcreatecollection wird mit <strong>adOpenIfExists</strong> oder <strong>adCreateOverwrite</strong>kombiniert.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-112">If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2ad-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="8a2ad-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2ad-114">0</span><span class="sxs-lookup"><span data-stu-id="8a2ad-114">0</span></span></p></td>
<td><p><span data-ttu-id="8a2ad-115">Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">adSimpleRecord</a>.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2ad-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="8a2ad-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2ad-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="8a2ad-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="8a2ad-118">Ändert die Erstellungskennzeichen <strong></strong>addcreatecollection, <strong>adCreateNonCollection</strong>und <strong>adCreateStructDoc</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-118">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="8a2ad-119">Wenn oder mit diesem Wert und einem der Werte für die Erstellungs Kennzeichnung verwendet wird, wenn die Quell-URL auf einen vorhandenen Knoten oder <strong>Datensatz</strong>verweist, wird der vorhandene <strong>Datensatz</strong> überschrieben, und an seiner Stelle wird ein neuer erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-119">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place.</span></span> <span data-ttu-id="8a2ad-120">Dieser Wert kann nicht zusammen mit <strong>adOpenIfExists</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-120">This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2ad-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="8a2ad-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2ad-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="8a2ad-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="8a2ad-123">Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">adStructDoc</a>, statt einen vorhandenen <strong>Datensatz</strong>zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2ad-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="8a2ad-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2ad-125">-1</span><span class="sxs-lookup"><span data-stu-id="8a2ad-125">-1</span></span></p></td>
<td><p><span data-ttu-id="8a2ad-p104">Standardwert. Führt zu einem Laufzeitfehler, wenn <em>Quelle</em> auf einen nicht vorhandenen Knoten verweist.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-p104">Default. Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2ad-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="8a2ad-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2ad-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="8a2ad-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="8a2ad-130">Ändert die Erstellungskennzeichen <strong></strong>addcreatecollection, <strong>adCreateNonCollection</strong>und <strong>adCreateStructDoc</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-130">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="8a2ad-131">Wenn oder mit diesem Wert und einem der Werte für die Erstellungs Kennzeichnung verwendet wird, wenn die Quell-URL auf ein vorhandenes Node-oder <strong>Record</strong> -Objekt verweist, muss der Anbieter den vorhandenen <strong>Datensatz</strong> öffnen, statt eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-131">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one.</span></span> <span data-ttu-id="8a2ad-132">Dieser Wert kann nicht zusammen mit <strong>adCreateOverwrite</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-132">This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8a2ad-133">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="8a2ad-133">ADO/WFC equivalent</span></span>

<span data-ttu-id="8a2ad-134">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="8a2ad-134">These constants do not have ADO/WFC equivalents.</span></span>

