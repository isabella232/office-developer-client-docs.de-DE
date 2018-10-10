---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3315fc0b6d72689e36530b7e7daf7b94732459f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474449"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="49d27-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="49d27-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="49d27-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="49d27-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="49d27-104">Gibt an, ob ein vorhandener **Datensatz** geöffnet werden soll, oder ein neuer **Datensatz** für das [Open](open-method-ado-record.md) -Methode des [Record](record-object-ado.md) -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="49d27-104">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="49d27-105">Die Werte können mit einem AND-Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="49d27-105">The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49d27-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="49d27-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="49d27-107">Wert</span><span class="sxs-lookup"><span data-stu-id="49d27-107">Value</span></span></p></th>
<th><p><span data-ttu-id="49d27-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49d27-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49d27-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="49d27-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="49d27-110">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="49d27-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="49d27-111">Erstellt einen neuen <strong>Datensatz</strong> an dem Knoten gemäß der <em>Source</em> -Parameter zu einem vorhandenen <strong>Datensatz</strong>zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="49d27-111">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>.</span></span> <span data-ttu-id="49d27-112">Wenn die Quelle auf einem vorhandenen Knoten verweist, tritt ein Laufzeitfehler, es sei denn, <strong>AdCreateCollection</strong> mit <strong>AdOpenIfExists</strong> oder <strong>AdCreateOverwrite</strong>kombiniert ist.</span><span class="sxs-lookup"><span data-stu-id="49d27-112">If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d27-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="49d27-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="49d27-114">0</span><span class="sxs-lookup"><span data-stu-id="49d27-114">0</span></span></p></td>
<td><p><span data-ttu-id="49d27-115">Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">AdSimpleRecord</a>.</span><span class="sxs-lookup"><span data-stu-id="49d27-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d27-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="49d27-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="49d27-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="49d27-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="49d27-118">Ändert die Erstellung Flags <strong>AdCreateCollection</strong>, <strong>AdCreateNonCollection</strong>und <strong>AdCreateStructDoc</strong>.</span><span class="sxs-lookup"><span data-stu-id="49d27-118">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="49d27-119">Wenn oder mit diesem Wert und einen der Werte für die Erstellung Kennzeichen verwendet wird, wenn die Quelle der URL auf einen vorhandenen Knoten oder <strong>Datensatz verweist</strong>, dann der vorhandene <strong>Datensatz</strong> überschrieben wird und an ihrer Stelle wird eine neue erstellt.</span><span class="sxs-lookup"><span data-stu-id="49d27-119">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place.</span></span> <span data-ttu-id="49d27-120">Dieser Wert kann nicht zusammen mit <strong>AdOpenIfExists</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49d27-120">This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d27-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="49d27-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="49d27-122">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="49d27-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="49d27-123">Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">AdStructDoc</a>statt einen bereits vorhandenen <strong>Datensatz</strong>zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="49d27-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d27-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="49d27-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="49d27-125">-1</span><span class="sxs-lookup"><span data-stu-id="49d27-125">-1</span></span></p></td>
<td><p><span data-ttu-id="49d27-p104">Standardwert. Führt zu einem Laufzeitfehler, wenn <em>Quelle</em> auf einen nicht vorhandenen Knoten verweist.</span><span class="sxs-lookup"><span data-stu-id="49d27-p104">Default. Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d27-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="49d27-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="49d27-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="49d27-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="49d27-130">Ändert die Erstellung Flags <strong>AdCreateCollection</strong>, <strong>AdCreateNonCollection</strong>und <strong>AdCreateStructDoc</strong>.</span><span class="sxs-lookup"><span data-stu-id="49d27-130">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="49d27-131">Wenn oder mit diesem Wert und einen der Werte für die Erstellung Kennzeichen verwendet wird, falls die Quell-URL zu einer vorhandenen Knoten oder <strong>Record</strong> -Objekts verweist, und klicken Sie dann der Anbieter muss den vorhandenen <strong>Datensatz</strong> statt Erstellen einer neuen öffnen.</span><span class="sxs-lookup"><span data-stu-id="49d27-131">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one.</span></span> <span data-ttu-id="49d27-132">Dieser Wert kann nicht zusammen mit <strong>AdCreateOverwrite</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49d27-132">This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49d27-133">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="49d27-133">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="49d27-134">Diese Konstanten haben keine ADO/WFC-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="49d27-134">These constants do not have ADO/WFC equivalents.</span></span>

